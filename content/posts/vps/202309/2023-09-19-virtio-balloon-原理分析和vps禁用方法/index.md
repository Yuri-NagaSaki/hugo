---
title: "Virtio-Balloon 原理分析和VPS禁用方法"
date: "2023-09-19"
categories: 
  - "laboratory"
---

![](https://catcat.blog/wp-content/uploads/2023/09/image-105.png)

## 前言

最近买了个VPS，商家自带了Virtio-Balloon服务，导致系统非常不稳定。于是乎来了解一下Virtio-Balloon。

Virtio-Balloon 驱动即内存气泡，可以用来动态调整内存。

## 功能介绍

Virtio-Balloon 驱动就是通过在虚拟机中申请内存，然后将申请的内存通知给 qemu，然后 qemu 侧再将内存释放掉，可以让其他虚拟机使用，达到内存复用的能力。

要开启这个功能，就是在启动时候需要添加 Virtio-Balloon 后端设备，并且要在 Guest 里面安装 Virtio-Balloon 驱动。

## 安装

- 添加设备 如果用 libvirt 启动 在 libvirt 的虚拟机配置侧添加如下 xml

```
 <devices>
 <memballoon model='virtio'>
      <alias name='balloon0'/>
      <address type='pci' domain='0x0000' bus='0x00' slot='0x06' function='0x0'/>
      <stats period='10'/>
    </memballoon>
  </devices>
```

在 qemu 中启动中添加如下设备

```
-device virtio-balloon-pci,id=balloon0,bus=pci.0,addr=0×4
```

- 安装驱动 windows 驱动这里省略了在网上教程很多。 linux 下在 kernel 很早就加入了 Virtio-Balloon 驱动，所以在主流 linux 发行版中一般都具有这个驱动。

```
[root@localhost _posts]# modinfo virtio-balloon
filename:       /lib/modules/3.10.0-327.el7.x86_64/kernel/drivers/virtio/virtio_balloon.ko
license:        GPL
description:    Virtio balloon driver
rhelversion:    7.2
srcversion:     F2D65C53D0AFD06A3668942
alias:          virtio:d00000005v*
depends:        virtio,virtio_ring
intree:         Y
vermagic:       3.10.0-327.el7.x86_64 SMP mod_unload modversions 
signer:         CentOS Linux kernel signing key
sig_key:        79:AD:88:6A:11:3C:A0:22:35:26:33:6C:0F:82:5B:8A:94:29:6A:B3
sig_hashalgo:   sha256
```

## 使用

有了上面的准备，启动虚拟机后就可以体验到内存气泡的功能。

- 查看内存： 在 libvirt 侧使用

```
virsh # dommemstat test
```

在 qemu 的 hmp 中查看内存

```
info balloon
```

- 设置目标虚拟机的内存，注意这里是直接设置虚拟机当前可以使用的内存。 比如起始的时候内存是 8G，然后想缩减 2G，实际这里操作要设置成目前为 6G。

libvirt 侧

```
virsh # setmem test 4096
```

在 qemu 的 hmp 中查看内存

```
balloon 4096
```

## 代码分析

从代码侧来具体分析 Virtio-Balloon 的。先从 linux 驱动侧看起吧 相对其他 virtio 驱动 ，内存气泡的驱动相对简单好看。 它的代码全部哎 driver/virtio/virtio\_balloon.c 中

首先来看 virtio\_balloon\_driver 驱动的定义， 这里很容易看到驱动的处理函数并不多 virtballoon\_probe，在驱动加载时候， virtballoon\_remove 在驱动卸载时候，剩下只有 virtballoon\_changed 那么肯定所有的功能都是在这个里面来实现。

```
static struct virtio_driver virtio_balloon_driver = {
    .feature_table = features,
    .feature_table_size = ARRAY_SIZE(features),
    .driver.name =  KBUILD_MODNAME,
    .driver.owner = THIS_MODULE,
    .id_table = id_table,
    .probe =    virtballoon_probe,
    .remove =   virtballoon_remove,
    .config_changed = virtballoon_changed,
#ifdef CONFIG_PM_SLEEP
    .freeze =   virtballoon_freeze,
    .restore =  virtballoon_restore,
#endif
};
```

virtballoon\_changed 的函数也相当简单，就是启动了一个 work 这个 work 主要来执行 update\_balloon\_size\_work 这个回调。

```
static void virtballoon_changed(struct virtio_device *vdev)
{
    struct virtio_balloon *vb = vdev->priv;
    unsigned long flags;

    spin_lock_irqsave(&vb->stop_update_lock, flags);
    if (!vb->stop_update)
        queue_work(system_freezable_wq, &vb->update_balloon_size_work);
    spin_unlock_irqrestore(&vb->stop_update_lock, flags);
}
```

为了弄清楚这个 work 我们还是需要看一下 virtio\_balloon 的初始化函数 virtballoon\_probe。 截取片段来看，初始化时候就注册了 stats\_request 这个 callback，用来响应后端发来的 stats 请求。定义了 2 个任务 update\_balloon\_size\_func 是用来修改内存， 而 update\_balloon\_stats\_func 这个是用来更新内存信息的，这个也是再次浏览代码时候的发现。

```
static int virtballoon_probe(struct virtio_device *vdev)
{
  struct virtqueue *vqs[3];
    vq_callback_t *callbacks[] = { balloon_ack, balloon_ack, stats_request };
    static const char * const names[] = { "inflate", "deflate", "stats" };
    int err, nvqs;

    nvqs = virtio_has_feature(vb->vdev, VIRTIO_BALLOON_F_STATS_VQ) ? 3 : 2;
    err = vb->vdev->config->find_vqs(vb->vdev, nvqs, vqs, callbacks, names,
            NULL);

 INIT_WORK(&vb->update_balloon_stats_work, update_balloon_stats_func);
 INIT_WORK(&vb->update_balloon_size_work, update_balloon_size_func);
}
```

先来介绍基本功能 update\_balloon\_size\_func，代码非常好理解，拿到 diff 和本身现在的内存进行比较，然后开始增加或者减少内存，接着 update\_balloon\_size 更新下当前内存的信息。

```
static void update_balloon_size_func(struct work_struct *work)
{
    struct virtio_balloon *vb;
    s64 diff;

    vb = container_of(work, struct virtio_balloon,
              update_balloon_size_work);
    diff = towards_target(vb);

    if (diff > 0)
        diff -= fill_balloon(vb, diff);
    else if (diff < 0)
        diff += leak_balloon(vb, -diff);
    update_balloon_size(vb);

    if (diff)
        queue_work(system_freezable_wq, work);
}
```

fill\_balloon 和 leak\_alloon 其实很相似，这里就看下 fill\_balloon 的实现。 调用 balloon\_page\_enqueue 函数进行内存的添加，然后 tell\_host 去更新表项。 balloon\_page\_enqueue 函数是 kernel 自己实现的堆内存进行增减的功能。 所以无论是 kvm 还是 xen 的气球驱动，最终都是调用这个函数去进行实现。 该函数在 mm/balloon\_compaction.c。这里就不继续往下追了，本编只是介绍 virtio-balloon 驱动原理。要想更细一步了解内存的实现，在以后专门讲内存操作时会再次提及该函数。

```
static unsigned fill_balloon(struct virtio_balloon *vb, size_t num)
{
    struct balloon_dev_info *vb_dev_info = &vb->vb_dev_info;
    unsigned num_allocated_pages;

    /* We can only do one array worth at a time. */
    num = min(num, ARRAY_SIZE(vb->pfns));

    mutex_lock(&vb->balloon_lock);
    for (vb->num_pfns = 0; vb->num_pfns < num;
         vb->num_pfns += VIRTIO_BALLOON_PAGES_PER_PAGE) {
        struct page *page = balloon_page_enqueue(vb_dev_info);

        if (!page) {
            dev_info_ratelimited(&vb->vdev->dev,
                         "Out of puff! Can't get %u pages\n",
                         VIRTIO_BALLOON_PAGES_PER_PAGE);
            /* Sleep for at least 1/5 of a second before retry. */
            msleep(200);
            break;
        }
        set_page_pfns(vb, vb->pfns + vb->num_pfns, page);
        vb->num_pages += VIRTIO_BALLOON_PAGES_PER_PAGE;
        if (!virtio_has_feature(vb->vdev,
                    VIRTIO_BALLOON_F_DEFLATE_ON_OOM))
            adjust_managed_page_count(page, -1);
    }

    num_allocated_pages = vb->num_pfns;
    /* Did we get any? */
    if (vb->num_pfns != 0)
        tell_host(vb, vb->inflate_vq);
    mutex_unlock(&vb->balloon_lock);

    return num_allocated_pages;
}
```

这个基本功能介绍完了，回到本篇最初的问题，Virtio-Balloon 驱动顺便还实现了一个内存的定时监控信息。 刚才在初始化的时候可以看到当后端主动调用 stat 指令时候，stats\_request 就会触发另一个 work update\_balloon\_stats\_func。

```
static void stats_request(struct virtqueue *vq)
{
    struct virtio_balloon *vb = vq->vdev->priv;

    spin_lock(&vb->stop_update_lock);
    if (!vb->stop_update)
        queue_work(system_freezable_wq, &vb->update_balloon_stats_work);
    spin_unlock(&vb->stop_update_lock);
}
```

update\_balloon\_stats\_func 这里主要调用 stats\_handle\_request

```
static void update_balloon_stats_func(struct work_struct *work)
{
    struct virtio_balloon *vb;

    vb = container_of(work, struct virtio_balloon,
              update_balloon_stats_work);
    stats_handle_request(vb);
}
```

然后 update\_balloon\_stats 这个函数将会收集所有的信息到达 vb 这个结构体，然后将 vb 发送给后端。

```
static void stats_handle_request(struct virtio_balloon *vb)
{
    struct virtqueue *vq;
    struct scatterlist sg;
    unsigned int len;

    update_balloon_stats(vb);

    vq = vb->stats_vq;
    if (!virtqueue_get_buf(vq, &len))
        return;
    sg_init_one(&sg, vb->stats, sizeof(vb->stats));
    virtqueue_add_outbuf(vq, &sg, 1, vb, GFP_KERNEL);
    virtqueue_kick(vq);
}
```

update\_balloon\_stats 这个函数就是实际采集 guest 连内存使用的情况。

```
static void update_balloon_stats(struct virtio_balloon *vb)
{
    unsigned long events[NR_VM_EVENT_ITEMS];
    struct sysinfo i;
    int idx = 0;
    long available;

    all_vm_events(events);
    si_meminfo(&i);

    available = si_mem_available();

    update_stat(vb, idx++, VIRTIO_BALLOON_S_SWAP_IN,
                pages_to_bytes(events[PSWPIN]));
    update_stat(vb, idx++, VIRTIO_BALLOON_S_SWAP_OUT,
                pages_to_bytes(events[PSWPOUT]));
    update_stat(vb, idx++, VIRTIO_BALLOON_S_MAJFLT, events[PGMAJFAULT]);
    update_stat(vb, idx++, VIRTIO_BALLOON_S_MINFLT, events[PGFAULT]);
    update_stat(vb, idx++, VIRTIO_BALLOON_S_MEMFREE,
                pages_to_bytes(i.freeram));
    update_stat(vb, idx++, VIRTIO_BALLOON_S_MEMTOT,
                pages_to_bytes(i.totalram));
    update_stat(vb, idx++, VIRTIO_BALLOON_S_AVAIL,
                pages_to_bytes(available));
}
```

到此，Vritio-Balloon 驱动的相关实现都描述完了。

qemu 后端代码比较简单了，首先来看气球初始化时候， 通过 qemu\_add\_balloon\_handler，注册了在调用 qmp 时候的回调函数，用来发起请求。 初始化了队列，ivq，dvq，svq 用来接收相关的信息，然后调用回调进行相应操作。

```
static void virtio_balloon_device_realize(DeviceState *dev, Error **errp)
{
    VirtIODevice *vdev = VIRTIO_DEVICE(dev);
    VirtIOBalloon *s = VIRTIO_BALLOON(dev);
    int ret;

    virtio_init(vdev, "virtio-balloon", VIRTIO_ID_BALLOON,
                sizeof(struct virtio_balloon_config));

    ret = qemu_add_balloon_handler(virtio_balloon_to_target,
                                   virtio_balloon_stat, s);

    if (ret < 0) {
        error_setg(errp, "Adding balloon handler failed");
        virtio_cleanup(vdev);
        return;
    }

    s->ivq = virtio_add_queue(vdev, 128, virtio_balloon_handle_output);
    s->dvq = virtio_add_queue(vdev, 128, virtio_balloon_handle_output);
    s->svq = virtio_add_queue(vdev, 128, virtio_balloon_receive_stats);
    reset_stats(s);

    register_savevm(dev, "virtio-balloon", -1, 1,
                    virtio_balloon_save, virtio_balloon_load, s);

    object_property_add(OBJECT(dev), "guest-stats", "guest statistics",
                        balloon_stats_get_all, NULL, NULL, s, NULL);

    object_property_add(OBJECT(dev), "guest-stats-polling-interval", "int",
                        balloon_stats_get_poll_interval,
                        balloon_stats_set_poll_interval,
                        NULL, s, NULL);
}
```

这里以刷新内存信息为例往下讲，内存增减功能类似。 在上面注册了 guest-stats-polling-interval 属性，这个是设置查询周期的，在设置了周期后，就可以看到启动了一个定时任务，balloon\_stats\_poll\_cb 来实时查询内存的信息。

```
static void balloon_stats_set_poll_interval(Object *obj, struct Visitor *v,
                                            void *opaque, const char *name,
                                            Error **errp)
{
    VirtIOBalloon *s = opaque;
    Error *local_err = NULL;
    int64_t value;

    visit_type_int(v, &value, name, &local_err);
    if (local_err) {
        error_propagate(errp, local_err);
        return;
    }

    if (value < 0) {
        error_setg(errp, "timer value must be greater than zero");
        return;
    }

    if (value > UINT32_MAX) {
        error_setg(errp, "timer value is too big");
        return;
    }

    if (value == s->stats_poll_interval) {
        return;
    }

    if (value == 0) {
        /* timer=0 disables the timer */
        balloon_stats_destroy_timer(s);
        return;
    }

    if (balloon_stats_enabled(s)) {
        /* timer interval change */
        s->stats_poll_interval = value;
        balloon_stats_change_timer(s, value);
        return;
    }

    /* create a new timer */
    g_assert(s->stats_timer == NULL);
    s->stats_timer = timer_new_ms(QEMU_CLOCK_VIRTUAL, balloon_stats_poll_cb, s);
    s->stats_poll_interval = value;
    balloon_stats_change_timer(s, 0);
}
```

而 virtio\_balloon\_receive\_stats 主要是从 vq 中取到前面讲的内存信息，然后用 balloon\_stats\_enabled 进行更新。

```
static void virtio_balloon_receive_stats(VirtIODevice *vdev, VirtQueue *vq)
{
    VirtIOBalloon *s = VIRTIO_BALLOON(vdev);
    VirtQueueElement *elem = &s->stats_vq_elem;
    VirtIOBalloonStat stat;
    size_t offset = 0;
    qemu_timeval tv;

    if (!virtqueue_pop(vq, elem)) {
        goto out;
    }

    /* Initialize the stats to get rid of any stale values.  This is only
     * needed to handle the case where a guest supports fewer stats than it
     * used to (ie. it has booted into an old kernel).
     */
    reset_stats(s);

    while (iov_to_buf(elem->out_sg, elem->out_num, offset, &stat, sizeof(stat))
           == sizeof(stat)) {
        uint16_t tag = virtio_tswap16(vdev, stat.tag);
        uint64_t val = virtio_tswap64(vdev, stat.val);

        offset += sizeof(stat);
        if (tag < VIRTIO_BALLOON_S_NR)
            s->stats[tag] = val;
    }
    s->stats_vq_offset = offset;

    if (qemu_gettimeofday(&tv) < 0) {
        fprintf(stderr, "warning: %s: failed to get time of day\n", __func__);
        goto out;
    }

    s->stats_last_update = tv.tv_sec;

out:
    if (balloon_stats_enabled(s)) {
        balloon_stats_change_timer(s, s->stats_poll_interval);
    }
}
```

## 总结

到此可以看到 Virtio-Balloon 的相关实现，和周期性查询内存信息的功能。 Virtio-Balloon 进行内存复用本身存在一些问题

- Guest 对内存变化会进行感知，Balloon 特性本身是 kernel 所具备的，本身是通过修改识别的内存信息来限制 Guest 中的使用。所以不是很友好。

- 内存复用需要实时监控，发现客户虚拟机内存使用过多还要及时归还内存，对于系统本身做这个功能有很大的局限性。

- Balloon 特性的内存复用并不是本质上进行内存的冗余复用，仅仅是借东墙补西墙，当虚拟机都大量使用内存时候，并不能实际突破物理内存上限。

## 如何禁用

1. 检查模块是否已加载：使用 `lsmod` 命令查看已加载的模块列表，确认 `virtio_balloon` 模块是否在其中。运行以下命令：`_**lsmod | grep virtio_balloon**_` 如果没有输出结果，则说明该模块尚未加载。

3. 使用 `rmmod` 命令卸载模块：如果 `virtio_balloon` 模块已加载，您可以使用 `rmmod` 命令进行卸载。运行以下命令：`**_sudo rmmod virtio_balloon_**` 这将尝试卸载 `virtio_balloon` 模块。如果成功卸载，您将不再看到任何错误消息。

## 如何防止开机启动

1. 打开 `/etc/modprobe.d/` 目录：运行以下命令以打开该目录：`**_sudo cd /etc/modprobe.d/_**`

3. 创建一个新的配置文件：在 `/etc/modprobe.d/` 目录中，创建一个新的配置文件，例如 `blacklist-virtio-balloon.conf`。运行以下命令：`**_sudo nano /etc/modprobe.d/blacklist-virtio-balloon.conf_**`

5. 在配置文件中添加禁用模块的规则：在打开的配置文件中，添加以下行：`**_blacklist virtio_balloon_**` 这将告诉系统在引导时禁用 `virtio_balloon` 模块。

7. 保存并关闭文件：按下 `Ctrl + X` 键，然后按下 `Y` 键以保存文件。

9. 更新 initramfs：运行以下命令以更新 initramfs：`**_sudo update-initramfs -u_**`

![](https://catcat.blog/wp-content/uploads/2023/09/image-104.png)
