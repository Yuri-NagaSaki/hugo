---
title: "OP杜甫 Raid1改Raid0 折腾记录"
date: "2023-06-19"
categories: 
  - "laboratory"
---

![](https://catcat.blog/wp-content/uploads/2023/06/image-8-1024x98.png)

```
  
完整命令  请不要一味照抄，根据自己的磁盘状况做修改
lsblk
df -h
cat /proc/mdstat   #查看当前Raid模式及阵列中的磁盘
mdadm /dev/md1 --fail /dev/sdb2  #告知系统磁盘挂了
mdadm /dev/md1 --remove /dev/sdb2  #热卸载磁盘
由于R1互为备份所以同步完成后卸载任意磁盘均不会宕机
/dev/md1还是md2，可以用lsblk或者df -h可以查看，我这个就是md1
wipefs -a /dev/sdb2   ## 清除sdb2磁盘分区的数据 根据自己输出来！
mdadm --grow /dev/md1 --level=0    #转换为R0
#把卸载下来的磁盘作为device2安装并开始转换
mdadm --grow /dev/md1 --level=0 --raid-devices=2 --add /dev/sdb2  

## 输入命令后就已经在后台开始自动转换，转换时间较长
期间可以使用watch cat /proc/mdstat  来查看转换进度，第一次会先转换为Raid4，其后再变成Raid0，时间较长，建议晚上睡觉前挂机，早上起来
cat /proc/mdstat 查看转换进度和Raid模式
watch cat /proc/mdstat
cat /proc/mdstat
resize2fs /dev/md1  ##重新计算磁盘空间
df -h  ## 检查是否成功
reboot  ## 重启
```

![](https://catcat.blog/wp-content/uploads/2023/06/ac10bd79143b4df11cbf1d8584768efb-1024x310.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-165.png)
