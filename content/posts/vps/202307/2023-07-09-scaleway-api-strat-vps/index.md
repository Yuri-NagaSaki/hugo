---
title: "Scaleway API 开机教程"
date: "2023-07-09"
categories: 
  - "laboratory"
---

## 价格

虽然网页上面写的stardust需要0.0025欧元/小时，但是由于我们可以选择只使用IPV6，因此每天小时仅需0.0005欧，0.0005欧x24小时x30天x12月=当前汇率31元人民币/年

## 注册

注册前你需要一张信用卡 星尘家只支持信用卡开通 一般虚拟卡就给过 只要有余额就给过的  
[注册地址](https://www.scaleway.com/en/)  
先走一遍注册流程  
注册流程没有什么难处  
注册好后  
星尘会询问你如何验证 这里选择第二个 也就是初级验证

## 开机准备

### 获取你的账户id(在IAM下)

![](https://catcat.blog/wp-content/uploads/2023/07/image-18-1024x411.png)

## 创建SSH key

```
在你的服务器上 输入 
ssh-keygen -o -b 4096

出现提示时输入保存密钥的文件路径。或者，按Enter 键id_ed25519将其保留为默认设置（密钥将保存在用户目录中调用的文件中~/.ssh/）。

Enter file in which to save the key (~/.ssh/id_ed25519):`

复制
出现提示时输入密码。此步骤不是强制性的，但建议执行此步骤以提高安全性。密码可以自由选择。如果不想设置密码，直接按Enter 键。

Enter passphrase (empty for no passphrase):

复制
出现提示时再次输入密码进行确认，然后按Enter：

Enter same passphrase again:

得到生成的ssh key，导入到scaleway控制台
```

![](https://catcat.blog/wp-content/uploads/2023/07/image-19.png)

![](https://catcat.blog/wp-content/uploads/2023/07/image-20.png)

## 开机脚本

星尘巴黎的机子 基本上365天 能有5天有货就是不错了  
荷兰的货比较多  
但是总得来说没有巴黎的机子好  
访问[星尘官方cli项目](https://github.com/scaleway/scaleway-cli)

选择一个适合你的操作系统的下载  
下载好后解压 随便改一个名字 方便后续操作

![](https://catcat.blog/wp-content/uploads/2023/07/image-21-1024x453.png)

通过终端进入解压好的文件夹(管理员的权限)

```
scw init
```

首先先输入你的apikey  
然后他问你是否改进这个工具 就是提交你的信息给他们 选择n  
后来询问是否安装shell的全部功能 选择y  
然后询问用哪种方式作为shell的壳程序 选择默认的bash  
然后问我是否导入我的ssh文件进去 选择y

## 开机脚本

project-id 获取

[位置](https://console.scaleway.com/project/settings)

![](https://catcat.blog/wp-content/uploads/2023/07/image-22-1024x378.png)

荷兰

```
scw instance server create type=STARDUST1-S zone=nl-ams-1 image=debian_bullseye root-volume=l:10G name=OK ip=none ipv6=true project-id=51b4e5be-9xxx-4xxx-bxxx-4fxxxxx(换成你自己的)
```

法国

```
scw instance server create type=STARDUST1-S zone=fr-par-1 image=debian_bullseye root-volume=l:10G name=OK ip=none ipv6=true project-id=51b4e5be-9xxx-4xxx-bxxx-4fxxxxx(换成你自己的)
```

出现类似，即为成功

![](https://catcat.blog/wp-content/uploads/2023/07/image-23-1024x1013.png)

小鸡这时候大部分情况都是没有开好的  
这样子都是没得ip 开不了鸡

> 脸黑 运气好的话 到这步就已经结束了 如果你觉得你运气比较好的话 你可以删鸡重新再跑一下脚本 删鸡记得把储存那里也删掉 不然也还是会扣费的

这样子的话 你可以一直运行另一个开机脚本

```
scw instance server start xxxxxxx-xxxxxx-xxxx（机子ID）
```

BashCopy

弄个定时任务就OK啦  
将下列文本保存为bat文件，在scw.exe的目录执行，一直挂着就行

```
@echo off
:scw
scw instance server start f5xxxxx-1007-476c-a137-xxxxxxxxx
timeout /T 10 /NOBREAK
goto scw
echo. 
exit
```

BatCopy

开完机后记得去安全组放行端口

## 放行端口

![](https://catcat.blog/wp-content/uploads/2023/07/image-24-1024x528.png)

![](https://catcat.blog/wp-content/uploads/2023/07/image-25-1024x721.png)

添加刚才开机的实列

## Warp脚本添加ipv4

```
bash <(wget -qO- https://gitlab.com/rwkgyg/CFwarp/raw/main/CFwarp.sh 2> /dev/null)
```

## 结语

```
结语
我个人认为Scaleway的Stardust机器是远强于玩具的，机器虽然便宜，但是性能十分给力，并且在WARP优秀的网络加持下，机器本身虽然只有公网V6，但是也可以愉快的访问V4的资源.
这机器在挂载了scaleway赠送的75G对象储存之后可玩性更高了，并且同一区域的流量应该是不计费的，而星尘的流量也是无限的.
```
