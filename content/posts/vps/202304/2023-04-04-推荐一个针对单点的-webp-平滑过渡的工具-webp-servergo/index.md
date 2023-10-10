---
title: "推荐一个针对单点的 WebP 平滑过渡的工具 WebP-ServerGo"
date: "2023-04-04"
categories: 
  - "laboratory"
---

好长时间没有关注 WebP 的支持性了，乍一看欸好像连 QQ 浏览器都能完美支持 WebP 了。很早之前就有关注 WebP-Server 这一过渡工具，恰好最近糖哥送了博主一台腾讯云无忧轻量，在国内的轻量上部署一番，感受一下 WebP 带来的提升。

## 一、概述

WebP 是由 Google 开发的一种高效的图片压缩方案（ Google WebP ），相比无损的 png 一般情况下 WebP 20%有损压缩能够达到最高 75%的压缩比例。也正如 Google 宣传的那样，WebP 的压缩率通常比 JPEG 和 JPEG 2000 平均高出 30%，而又不会降低图片质量。

![](https://catcat.blog/wp-content/uploads/2023/10/image-147.png)

但是直至 2023 年，纯 WebP 存储依然面临着很大的历史遗留问题。访问方面问题相对比较小，仅是 iOS 14 以前的 Safari 并不支持，国内外主流的现代浏览器都已经悉数支持了 WebP 图片的加载（支持性统计）。但是各类生产力工具，比如 Ps 、Ai 等依然不支持加载 WebP 图像，如果原始图片仅保留 WebP 的话意味着放弃了一小部分旧设备加上失去了编辑的便利性。一边是 WebP 带来极致的媒体加载体验，一边是失去部分编辑的便利性，博主之前常常纠结于这些取舍，碍于不能完美解决问题而对新技术望而却步。

前一段时间，偶然的机会我的群友提到了 WebP-Server 这个过渡工具。这是一个基于 go 语言的 WebP 转换中间件，与很多 CDN 提供的过渡策略一样，能够在使用原图储存的基础上，通过访客 UA 判断浏览器支持性决定返回 WebP 或原图。相应的，WebP-Server 也能够支持生成 WebP 缓存，以及像 CDN 一样作为边缘访问节点实现对源站请求的压缩。

- 项目主页： [https://webp.sh](https://webp.sh/)

- 项目文档： [https://docs.webp.sh/usage/basic-usage](https://docs.webp.sh/usage/basic-usage)

- GitHub： [https://github.com/webp-sh/webp\_server\_go](https://github.com/webp-sh/webp_server_go)

纵观我们国内的服务器市场，在个人经济能力能够承受范围的带宽最大也就 4-5M 。基于这样的假设，我们可以理论计算一下，5M 的带宽大约能为你提供 640k/s 的传出能力，以博主的经验平均 8 张图 /页面、100k/图，单个 PV 下就要占满带宽 1.25 秒完成图片的加载。但是在 20%有损 WebP 压缩的情况下，图片平均大小降至 16-25k ，能够使 1 秒内 PV 并发能力提高 5 倍，这在服务器带宽非常捉襟见肘的国内网络环境下对站点的负载能力提升是立竿见影的。也是基于这个现状，如果自用的图床能够配置 WebP ，很可能就不必再为 CDN 额外付费，仅通过高质量的 BGP 网络完成服务的提供。

在疫情后降本增效的大环境下，也只有腾讯云 4 月上云精选依然在提供三年 408 2C/2G/4M 和 628 2C/4G/5M 的轻量应用服务器了。最近糖哥送了我一台腾讯云的无忧轻量，1C/2G/5M 的配置与活动款带宽基本一致。题外话，最近腾讯云开放了无忧的付费升配通道，持有无忧的小伙伴在有需要的情况下可以按需选择升级到更高的配置。

## 二、WebP Server

由于 WebP-Server 需要 libaom 组件，并且需要 libc6>2.34 ，博主建议使用 CentOS 8 / Debian 11 及以上的系统。尽管较早的系统可以通过编译来对 libc6 版本进行升级，但这是一个十分危险的操作，很可能会导致系统关键组件出现问题。因此对于较早的系统，博主更加推荐直接使用 docker 进行部署（官方文档），支持 ARMv7 （ 32bit ）、ARM64 （ Aarch64 ）和 AMD64 （ x86-64 ），可以在 DockerHub 上查看（点击前往）。

```
#  [/path/to/pics ] 指的是图片路径， [/opt/pics ] 指的是生成的 WebP 缓存路径
docker run -d -p 3333:3333 -v /path/to/pics:/opt/pics --name webp-server webpsh/webp-server-go
```

手动安装的话，必要的组件就是 libaom3 ，这个组件略微有点坑，预编译包会默认读取 libaom.so.3 [这个.so](http://xn--ciq341n.so/) ，安装好之后如果还是提示找不到 libaom3 ，可以试试通过 ln -s 做一个软连接。

```
# 安装 libaom 库
apt install libaom-dev
yum install libaom-devel
# 在 RHEL 系（ CentOS ）中解决找不到依赖的问题
ln -s /usr/lib64/libaom.so.0 /usr/lib64/libaom.so.3
#在 Debian 系中解决找不到依赖的问题
ln -s /usr/lib/x86_64-linux-gnu/libaom.so.0 /usr/lib64/libaom.so.3
```

预编译包可以从 GitHub 下载（点击前往），配置文件请按你的实际需要选择模式并修改参数，以下各项参数的解释已写在注释里面，修改完成后可以保存为 config.json 文件。

```
#代理模式
{
  "HOST": "127.0.0.1", //监听本地主机，使用 0.0.0.0 可监听全部
  "PORT": "3333", //WebP Server 使用的本地端口
  "QUALITY": "80", //压缩质量，越低图片压缩比越高
  "IMG_PATH": "https://test.webp.sh", //反代的站点
  "EXHAUST_PATH": "/path/to/exhaus", //缓存 WebP 的保存路径
  "ALLOWED_TYPES": ["jpg","png","jpeg","bmp","gif"], //压缩的后缀类型
}
#本地模式
{
  "HOST": "127.0.0.1", //监听本地主机，使用 0.0.0.0 可监听全部
  "PORT": "3333", //WebP Server 使用的本地端口
  "QUALITY": "80", //压缩质量，越低图片压缩比越高
  "IMG_PATH": "/path/to/pics", //本地图片路径，一般设置为站点根目录
  "EXHAUST_PATH": "/path/to/exhaust", //缓存 WebP 的保存路径
  "ALLOWED_TYPES": ["jpg","png","jpeg","bmp","gif"], //压缩的后缀类型
  "ENABLE_AVIF": false //av1 压缩支持，暂不建议使用
}
```

直接安装的话建议使用 systemd 启动服务，以下是一个一键写入 webp.service 的示例，修改好 webp-server 二进制文件和 config.json 文件的路径，直接粘贴进 ssh 窗口即可。

```
cat > /etc/systemd/system/webp.service <<EOF
[Unit]
Description=WebP Server
Documentation=https://github.com/n0vad3v/webp_server_go
After=nginx.target

[Service]
Type=simple
StandardError=journal
AmbientCapabilities=CAP_NET_BIND_SERVICE
WorkingDirectory=/[程序目录]/webp-server
ExecStart=/[程序目录]/webp-server/webp-server-linux-amd64 --config /[程序目录]/webp-server/config.json
ExecReload=/bin/kill -HUP $MAINPID
Restart=always
RestartSec=3s

[Install]
WantedBy=multi-user.target
EOF
```

至此，你就可以使用 service webp start|stop|status 来控制 WebP Server 的运行了，确认无误后使用 systemctl enable webp 来允许其开机启动。

## 三、NGINX 设置

在 WebP-Server 工作正常之后，我们需要在 NGINX 上配置一个反向代理，将 jpg|jpeg|gif|png|bmp 这些后缀的媒体文件交给 WebP-Server 来处理。以下是一个示例，加在 NGINX 对应的 vhost 中即可。需要注意的是，开启了 WebP 自动返回之后，同时需要在 vhost 中删除掉 NGINX 对相关媒体后缀的缓存内容，以免将 WebP 返回给了不支持的设备。

![](https://catcat.blog/wp-content/uploads/2023/10/image-148.png)

```
# 将 jpg|jpeg|gif|png|bmp 请求转发至本地 3333 端口
location ~* \.(?:jpg|jpeg|gif|png|bmp)$ {
    proxy_pass http://127.0.0.1:3333;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_hide_header X-Powered-By;
    proxy_set_header HOST $http_host;
    add_header Cache-Control 'no-store, no-cache, must-revalidate, proxy-revalidate, max-age=0';
}
```

## 四、补充&总结

在撰写文章的过程中，有朋友提醒说目前该程序存在内存泄漏的情况（点击前往），作者建议使用 Docker 通过限制内存使用来避免这个问题。这个问题是在多人同时访问单个媒体资源时 WebP Server 会对同个文件启动多个压缩进程，进而导致异常的内存占用。如果直接安装同时为了更好的体验，缓存预热是一个非常明智的选择。

```
# 启用 4 进程对配置目录进行缓存预热
./webp-server -prefetch -jobs=4 --config /[程序目录]/webp-server/config.json
```

作者在 GitHub 上的预编译包仅提供了 64 位 x86 的架构，博主感觉作者是在 RHEL8 系上构建的预编译包，如果想在其他平台使用可以考虑使用 docker 或者按照文档（点击前往）进行编译，整个流程并不复杂。配置好后打开 F12 Network 选项卡，勾选类型选项或者在图片的 content-type 可以看到，我们实际访问的图片已经被压缩成了 webp 。最后也再次感谢作者写出这样一个好用的小工具吧~

* * *

**原文链接**： [https://luotianyi.vc/6907.html](https://luotianyi.vc/6907.html)

若有任何问题，欢迎大家批评指正~
