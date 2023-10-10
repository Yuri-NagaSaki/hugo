---
title: "Crunchbits 评测"
date: "2023-02-22"
categories: 
  - "vps"
  - "usa"
tags: 
  - "usa"
---

> 前言 Crunchbits，这是一家 2021 年 11 月 30 日成立的美国主机商，主营 NVMe KVM VPS、EPYC 高频 NVMe VPS、锐龙 5950X NVMe KVM VPS、大硬盘存储 VPS、GPU 显卡服务器和独立服务器，数据中心位于美国 爱达荷州。

## 前言

![](https://catcat.blog/wp-content/uploads/2023/10/image-10-1024x517.png)

Crunchbits，这是一家 2021 年 11 月 30 日成立的美国主机商，主营 NVMe KVM VPS、EPYC 高频 NVMe VPS、锐龙 5950X NVMe KVM VPS、大硬盘存储 VPS、GPU 显卡服务器和独立服务器，数据中心位于美国 爱达荷州。

美西，距离西雅图、圣荷西、洛杉矶都比较近。

目前网站仅支持信用卡、比特币和 Paypal 付款（暂不支持支付宝）。

本次推荐套餐：

**4GB 锐龙 5950X 带 450GB 硬盘！**

- 1 锐龙 5950X vCore

- 4GB DDR4 **ECC** 内存

- 50GB 第 4 代 NVMe 操作系统 / 主磁盘

- **450GB 硬盘**存储磁盘

- 10TB 带宽 @ **2.5Gbps**

- 1 个 IPv4 + 1 个 IPv6 /64

- $ 8 / 月 **$ 6.8 / 月** 带优惠券：**ONLYTOWEL**

- [**购买地址**](https://crunchbits.com/)

> 注意：HDD 块存储必须在成功订购后发工单让老板添加。

工单参考：

> 标题：
> 
> Add a 450GB HDD to my hard drive
> 
> 内容：
> 
> Dear crunchbits,
> 
> I don’t currently have a 450GB HDD as a drive, please help add it, thanks!

特色：

- NVMe

- 大存储

- 5950X

- 带免费备份功能，可以设置指定时间自动备份（备份保留一份，仅备份 50GB NVMe 上的内容，无法备份 450G HDD 上的内容）

- 美西

缺陷：

- 新商家，不知道会不会跑路（可以月付，PayPal 上车，消除风险）

- 线路可能没那么好（美西其实还凑合，实在不行可以反代解决）

## 1\. 官方网站

官网：[https://crunchbits.com/](https://loll.cc/crunchbits)

## 2\. 注意点

- 个人信息里面的街道啥的也要完善好

- 地址什么的要填合乎逻辑的地址，可以不准确但是不要乱填

如果万一订单被判定欺诈，可以发工单和客服沟通。

如果需要翻译，可以用这个：[https://www.deepl.com/translator](https://www.deepl.com/translator)

## 3\. 套餐介绍

### 3.1 Ryzen 5950X CPU NVMe VPS Plans

最低配折后 **$6.8/** 月，优惠码：`ONLYTOWEL`（85 折循环优惠码）

| **内存** | **Ryzen 5950X Cores**CPU | 固态硬盘 | HDD 硬盘 | **Bandwidth @ 2.5Gbps** | **IPv4 | IPv6** | 折前价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 4GB | **1** 5950X Cores | 50GB NVMe | 450GB HDD | 10TB | 1 IPv4 | 1 /64 | **$8/mo** | [购买链接](https://loll.cc/crunchbits) |
| 8GB | **2** 5950X Cores | 100GB NVMe | 900GB HDD | 20TB | 1 IPv4 | 1 /64 | **$16/mo** | [购买链接](https://loll.cc/crunchbits) |
| 16GB | **4** 5950X Cores | 200GB NVMe | **1.8TB** HDD | 40TB | 1 IPv4 | 1 /64 | **$32/mo** | [购买链接](https://loll.cc/crunchbits) |
| 32GB | **8** 5950X Cores | 400GB NVMe | **3.6TB** HDD | 80TB | 1 IPv4 | 1 /64 | **$64/mo** | [购买链接](https://loll.cc/crunchbits) |

本次测试款为最低配 6.8 刀 / 月款。

## 4\. VPS 测试（1C4G）

### 4.1 基本情况

鸡况如下：

![](https://catcat.blog/wp-content/uploads/2023/10/image-11-1024x1011.png)

### 4.2 速度测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-12-1024x480.png)

测试我们重点看`Upload Speed`, 我们从 VPS 上取东西（下载），对 VPS 来说就是上传。

以上海`Shanghai 5G`为例子，显示的`Upload Speed`是`305.71 Mbit/s`，差不多是平时说的 300M 带宽，对应到我们实际的理论下载速度就 =`305.71/8`\=`38.21M/s`

开启 BBR 之后：

![](https://catcat.blog/wp-content/uploads/2023/10/image-13-1024x827.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-14-1024x482.png)

### 4.4 PING 值

![](https://catcat.blog/wp-content/uploads/2023/10/image-15-1024x473.png)

### 4.5 网络测试

#### 4.5.1 机器

Test IPv4: 204.9.39.100

Test IPv6: 2606:a8c0:1:99::a

#### 4.5.2 官网节点测速

Looking glass: [https://lg-cda.crunchbits.com](https://lg-cda.crunchbits.com/)

### 回程测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-16-1024x715.png)

## 融合怪脚本测速

```
-----------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD Ryzen 9 5950X 16-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 3393.624 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 492.0 GB (352.0 GB 已用)
 内存              : 3898 MB (692 MB 已用)
 Swap              : 4095 MB (305 MB 已用)
 系统在线时间      : 4 days, 15 hour 3 min
 负载              : 0.08, 0.04, 0.00
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-10-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 ASN组织           : AS400304 REDOUBT NETWORKS
 位置              : Coeur d'Alene / US
 地区              : Idaho
-------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		5308 Scores
-------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		65489.81 MB/s
 单线程写测试:		32928.62 MB/s
----------------磁盘IO读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		->
 100MB-4K Block		95.4 MB/s (0.04K IOPS, 1.10s)		->
 100MB-4K Block		95.4 MB/s (0.04 IOPS, 1.10s)		111 MB/s (27153 IOPS, 0.94s)
 1GB-1M Block		->
 1GB-1M Block		2.4 GB/s (2302 IOPS, 0.43s)		->
 1GB-1M Block		2.4 GB/s (2302 IOPS, 0.43s)		4.4 GB/s (4197 IOPS, 0.24s)
-------------------磁盘IO读写测试--感谢yabs开源-----------------------
  ------ | --- ---- | ---- ---- 
Read       | 399.53 MB/s  (99.8k) | 3.53 GB/s    (55.2k)
Write      | 400.59 MB/s (100.1k) | 3.55 GB/s    (55.4k)
Total      | 800.13 MB/s (200.0k) | 7.08 GB/s   (110.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.26 GB/s     (6.3k) | 2.77 GB/s     (2.7k)
Write      | 3.44 GB/s     (6.7k) | 2.95 GB/s     (2.8k)
Total      | 6.71 GB/s    (13.1k) | 5.72 GB/s     (5.5k)
--------------------流媒体解锁--感谢sjlleo开源------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA30S12)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA30S12)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：美国
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
---------------流媒体解锁--感谢RegionRestrictionCheck开源-------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: US)
 Netflix:				Originals Only
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				Seattle, WA 
 Netflix Preferred CDN:			Seattle, WA  
 Spotify Registration:			No
 Steam Currency:			USD
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				Yes (Region: US)
 Disney+:				Yes (Region: US)
 Netflix:				Yes (Region: US)
 YouTube Premium:			Yes
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Seattle, WA 
 Netflix Preferred CDN:			Seattle, WA  
 Spotify Registration:			Yes (Region: US)
 Steam Currency:			Failed (Network Connection)
=======================================
-------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【US】
--------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化--------
[IPv4]
Your IP supports access to OpenAI. Region: US
[IPv6]
Your IP supports access to OpenAI. Region: US
-----------------欺诈分数以及IP质量检测--本频道原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：57
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：0
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：100
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
-----------------三网回程--感谢zhanghanyun/backtrace开源--------------
2023/04/23 10:39:35 北京电信 219.141.136.12  测试超时
2023/04/23 10:39:35 北京联通 202.106.50.1    联通4837[普通线路]           
2023/04/23 10:39:35 北京移动 221.179.155.161 测试超时
2023/04/23 10:39:35 上海电信 202.96.209.133  测试超时
2023/04/23 10:39:35 上海联通 210.22.97.1     联通4837[普通线路]           
2023/04/23 10:39:35 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/04/23 10:39:35 广州电信 58.60.188.222   电信163 [普通线路]           
2023/04/23 10:39:35 广州联通 210.21.196.6    联通4837[普通线路]           
2023/04/23 10:39:35 广州移动 120.196.165.24  测试超时
2023/04/23 10:39:35 成都电信 61.139.2.69     测试超时
2023/04/23 10:39:35 成都联通 119.6.6.6       联通4837[普通线路]           
2023/04/23 10:39:35 成都移动 211.137.96.205  测试超时
------------------回程路由--感谢fscarmen开源及PR----------------------
IPv4 ASN: Crunchbits
IPv6 ASN: Crunchbits
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.29 ms  AS400304  美国, 爱达荷州, 科达伦, redoubtnet.com
0.73 ms  AS964  美国, 爱达荷州, 科达伦, ionswitch.com
1.00 ms  AS20055  美国, 爱达荷州, 科达伦, ziplyfiber.com
8.93 ms  AS20055  美国, 华盛顿州, 斯波坎, ziplyfiber.com
17.95 ms  AS20055  美国, 华盛顿州, 斯波坎, ziplyfiber.com
9.30 ms  AS20055  美国, 华盛顿州, 亚基马, ziplyfiber.com
8.42 ms  AS6461  美国, 华盛顿州, 西雅图, zayo.com
27.97 ms  AS6461  美国, 华盛顿州, 西雅图, zayo.com
36.68 ms  AS6461  美国, 加利福尼亚州, 圣何塞, zayo.com
27.83 ms  AS6461  美国, 加利福尼亚州, 圣何塞, zayo.com
29.47 ms  AS6461  美国, 加利福尼亚州, 圣何塞, zayo.com
203.67 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
184.30 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
192.37 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.28 ms  AS400304  美国, 爱达荷州, 科达伦, redoubtnet.com
0.60 ms  AS964  美国, 爱达荷州, 科达伦, ionswitch.com
0.86 ms  AS20055  美国, 爱达荷州, 科达伦, ziplyfiber.com
9.39 ms  AS20055  美国, 华盛顿州, 斯波坎, ziplyfiber.com
17.71 ms  AS20055  美国, 华盛顿州, 斯波坎, ziplyfiber.com
9.07 ms  AS20055  美国, 华盛顿州, 亚基马, ziplyfiber.com
8.89 ms  AS20055  美国, 华盛顿州, 西雅图, ziplyfiber.com
27.15 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
28.45 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
40.33 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
40.68 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
39.42 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
234.74 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
242.67 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
244.65 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
210.43 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.2
0.31 ms  AS400304  美国, 爱达荷州, 科达伦, redoubtnet.com
0.66 ms  AS964  美国, 爱达荷州, 科达伦, ionswitch.com
2.84 ms  AS20055  美国, 爱达荷州, 科达伦, ziplyfiber.com
11.32 ms  AS20055  美国, 爱达荷州, 科达伦, ziplyfiber.com
11.73 ms  AS20055  美国, 华盛顿州, 普尔曼, ziplyfiber.com
11.49 ms  AS20055  美国, 华盛顿州, 肯纳威克, ziplyfiber.com
11.34 ms  AS20055  美国, 华盛顿州, 肯纳威克, ziplyfiber.com
11.66 ms  AS20055  美国, 华盛顿州, 肯纳威克, ziplyfiber.com
11.62 ms  AS20055  美国, 华盛顿州, 肯纳威克, ziplyfiber.com
11.20 ms  AS20055  美国, 俄勒冈州, 比弗顿, ziplyfiber.com
10.99 ms  AS20055  美国, 俄勒冈州, 希尔斯伯勒, ziplyfiber.com
11.20 ms  AS20055  美国, 俄勒冈州, 希尔斯伯勒, ziplyfiber.com
10.75 ms  AS1299  美国, 俄勒冈州, 波特兰, telia.com
26.23 ms  AS1299  美国, 加利福尼亚州, 帕洛阿尔托, telia.com
27.85 ms  AS1299  美国, 加利福尼亚州, 圣何塞, telia.com
28.78 ms  AS1299  美国, 加利福尼亚州, 圣何塞, telia.com
28.68 ms  AS58453  美国, 加利福尼亚州, 圣何塞, chinamobile.com, 移动
209.50 ms  AS58453  中国, 上海, chinamobile.com, 移动
210.42 ms  AS9808  中国, 上海, chinamobile.com, 移动
210.99 ms  AS9808  中国, 上海, chinamobile.com, 移动
249.85 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
------------------------ ecs-net--本频道独创 -------------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 990.38 Mbps	 2314.60 Mbps	 41.54	  0.0%
洛杉矶		 2375.41 Mbps	 2285.41 Mbps	 34.53	  0.0%
新加坡		 349.30 Mbps	 2005.06 Mbps	 209.75	  0.0%
联通上海5G	 284.81 Mbps	 1445.38 Mbps	 296.07	  0.0%
联通WuXi	 352.44 Mbps	 2002.90 Mbps	 226.15	  0.0%
电信上海	 14.89 Mbps	 1511.09 Mbps	 172.03	  NULL
移动陕西5G	 347.38 Mbps	 1747.94 Mbps	 244.12	  0.0%
移动Chengdu	 186.43 Mbps	 1643.57 Mbps	 230.34	  0.0%
----------------------------------------------------------------------
 总共花费      : 7 分 1 秒
 时间          : Sun 23 Apr 2023 10:45:24 AM CST
```

## 2023年9月5日观察测试

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 3 minutes
Processor  : AMD Ryzen 9 5950X 16-Core Processor
CPU cores  : 1 @ 3400.000 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 0.0 KiB
Disk       : 50.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-20-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Redoubt Networks
ASN        : AS400304 REDOUBT NETWORKS
Host       : Redoubt Networks
Location   : Spokane, Washington (WA)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 381.00 MB/s  (95.2k) | 2.06 GB/s    (32.2k)
Write      | 382.01 MB/s  (95.5k) | 2.07 GB/s    (32.4k)
Total      | 763.01 MB/s (190.7k) | 4.14 GB/s    (64.6k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.85 GB/s     (5.5k) | 2.77 GB/s     (2.7k)
Write      | 3.00 GB/s     (5.8k) | 2.96 GB/s     (2.8k)
Total      | 5.85 GB/s    (11.4k) | 5.73 GB/s     (5.6k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 29.5 Mbits/sec  | 39.2 Mbits/sec  | 136 ms         
Scaleway        | Paris, FR (10G)           | 1.31 Gbits/sec  | 3.29 Mbits/sec  | 155 ms         
NovoServe       | North Holland, NL (40G)   | 1.16 Gbits/sec  | 1.19 Gbits/sec  | 201 ms         
Uztelecom       | Tashkent, UZ (10G)        | 885 Mbits/sec   | 455 Mbits/sec   | 234 ms         
Clouvider       | NYC, NY, US (10G)         | 61.0 Mbits/sec  | 102 Mbits/sec   | 67.2 ms        
Clouvider       | Dallas, TX, US (10G)      | 59.0 Mbits/sec  | 197 Mbits/sec   | 69.7 ms        
Clouvider       | Los Angeles, CA, US (10G) | 107 Mbits/sec   | 146 Mbits/sec   | 68.8 ms        
Biznet          | Jakarta, ID (10G)         | 803 Mbits/sec   | 57.7 Mbits/sec  | -- 

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 29.1 Mbits/sec  | 38.2 Mbits/sec  | 136 ms         
Scaleway        | Paris, FR (10G)           | 1.41 Gbits/sec  | 590 Mbits/sec   | 141 ms         
NovoServe       | North Holland, NL (40G)   | 728 Mbits/sec   | 852 Mbits/sec   | 205 ms         
Uztelecom       | Tashkent, UZ (10G)        | 898 Mbits/sec   | busy            | 220 ms         
Clouvider       | NYC, NY, US (10G)         | busy            | 92.4 Mbits/sec  | 67.0 ms        
Clouvider       | Dallas, TX, US (10G)      | 58.4 Mbits/sec  | 235 Mbits/sec   | 67.6 ms        
Clouvider       | Los Angeles, CA, US (10G) | 102 Mbits/sec   | 164 Mbits/sec   | 38.9 ms        
Biznet          | Jakarta, ID (10G)         | busy            | busy            | -- 

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2272                          
Multi Core      | 2284                          
Full Test       | https://browser.geekbench.com/v6/cpu/2500151
```

### SpeedTest

```
   Speedtest by Ookla

      Server: Intechtel - Managed IT Services - Coeur d'Alene, ID (id: 51640)
         ISP: Crunchbits, LLC
Idle Latency:    10.61 ms   (jitter: 0.12ms, low: 10.52ms, high: 10.70ms)
    Download:  2272.51 Mbps (data used: 2.7 GB)                                                   
                 10.58 ms   (jitter: 0.12ms, low: 10.35ms, high: 12.20ms)
      Upload:  2011.29 Mbps (data used: 3.9 GB)                                                   
                 10.52 ms   (jitter: 0.14ms, low: 10.22ms, high: 11.55ms)
 Packet Loss:     0.0%
  Result URL: https://www.speedtest.net/result/c/1707743e-bbde-4dfb-b771-19e91a6287ff
```

![](https://cdn.lirica.cn/wordpress/2023/09/image-20-1024x399.png)

### 融合怪脚本

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 5950X 16-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 3400.000 MHz
 CPU 缓存          : L1: 64.00 KB / L2: 512.00 KB / L3: 64.00 MB
 硬盘空间          : 1.88 GiB / 49.87 GiB
 启动盘路径        : /dev/sda3
 内存              : 229.36 MiB / 3.80 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 23 min
 负载              : 0.07, 0.22, 0.16
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-20-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS400304 REDOUBT NETWORKS
 IPV4 位置         : Liberty Lake / Washington / US
 IPV6 ASN          : AS400304 Crunchbits
 IPV6 位置         : Spokane / Washington
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           5560 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          65502.36 MB/s
 单线程写测试:          31958.25 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         61.2 MB/s (14.95 IOPS, 1.71s))          84.8 MB/s (20705 IOPS, 1.24s)
 1GB-1M Block           704 MB/s (671 IOPS, 1.49s)              4.5 GB/s (4305 IOPS, 0.23s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 388.28 MB/s  (97.0k) | 2.06 GB/s    (32.2k)
Write      | 389.30 MB/s  (97.3k) | 2.07 GB/s    (32.4k)
Total      | 777.58 MB/s (194.3k) | 4.13 GB/s    (64.6k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.79 GB/s     (5.4k) | 2.80 GB/s     (2.7k)
Write      | 2.93 GB/s     (5.7k) | 2.98 GB/s     (2.9k)
Total      | 5.72 GB/s    (11.1k) | 5.79 GB/s     (5.6k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA09S34)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA09S34)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：美国
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: US)
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Seattle, WA 
 Netflix Preferred CDN:                 Seattle, WA  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Seattle, WA 
 Netflix Preferred CDN:                 Seattle, WA  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  business⑨  
  公司类型(company_type):isp①  hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ② ⑥ ⑦ ⑧ ⑨ ⑩ 
  VPN(vpn):  No① ② ⑦ ⑧ 
  TOR(tor):  No① ② ⑦ ⑧ ⑨ 
  TOR出口(tor_exit):  No⑧ 
  搜索引擎机器人(search_engine_robot):  No② 
  匿名代理(anonymous):  No⑦ ⑧ ⑨ 
  攻击方(attacker):  No⑧ ⑨ 
  滥用者(abuser):  No⑧ ⑨ 
  威胁(threat):  No⑧ ⑨ 
  iCloud中继(icloud_relay):  No① ⑧ ⑨ 
  未分配IP(bogon):  No⑧ ⑨ 
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测87 ③
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  qq邮箱：No
  yandex邮箱: Yes
------以下为IPV6检测------
欺诈分数(越低越好): 100②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: US 城市: Liberty Lake 服务商: AS400304 REDOUBT NETWORKS
北京电信 219.141.136.12  测试超时
北京联通 202.106.50.1    联通4837[普通线路]           
北京移动 221.179.155.161 测试超时
上海电信 202.96.209.133  电信163 [普通线路]           
上海联通 210.22.97.1     联通4837[普通线路]           
上海移动 211.136.112.200 移动CMI [普通线路]           
广州电信 58.60.188.222   电信163 [普通线路]           
广州联通 210.21.196.6    测试超时
广州移动 120.196.165.24  测试超时
成都电信 61.139.2.69     电信163 [普通线路]           
成都联通 119.6.6.6       联通4837[普通线路]           
成都移动 211.137.96.205  测试超时
2023/09/05 09:31:01 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
26.27 ms        AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
18.46 ms        AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
1.94 ms         * 美国 爱达荷州 科达伦
2.36 ms         AS20055 [WHOLESAIL-IPV4] 美国 爱达荷州 科达伦 wholesailnetworks.com
10.03 ms        AS20055 [WHOLESAIL-IPV4] 美国 爱达荷州 科达伦 wholesailnetworks.com
10.35 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 斯波坎 wholesailnetworks.com
14.89 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 斯波坎 wholesailnetworks.com
10.36 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 雅基马 wholesailnetworks.com
9.85 ms         AS6461 [NETBLK-ABOVENET] 美国 华盛顿州 西雅图 zayo.com
32.93 ms        AS6461 美国 华盛顿州 西雅图 zayo.com
29.05 ms        AS6461 美国 加利福尼亚州 圣何塞 zayo.com
28.68 ms        AS6461 美国 加利福尼亚州 圣何塞 zayo.com
174.93 ms       AS4134 [CHINANET-BB] 中国 chinatelecom.com.cn 电信
185.00 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
206.90 ms       AS134774 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.cn 电信
193.77 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
34.85 ms        AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
0.57 ms         AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
2.06 ms         * 美国 爱达荷州 科达伦
1.71 ms         AS20055 [WHOLESAIL-IPV4] 美国 爱达荷州 科达伦 wholesailnetworks.com
10.04 ms        AS20055 [WHOLESAIL-IPV4] 美国 爱达荷州 科达伦 wholesailnetworks.com
10.30 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 斯波坎 wholesailnetworks.com
18.27 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 斯波坎 wholesailnetworks.com
10.26 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 雅基马 wholesailnetworks.com
10.11 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 西雅图 wholesailnetworks.com
28.46 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 旧金山 cogentco.com
30.49 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 圣何塞 cogentco.com
41.92 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
42.21 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
41.08 ms        AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
194.90 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
201.72 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
194.41 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
199.37 ms       AS17816 [UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
205.46 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
202.25 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
151.83 ms       AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
0.54 ms         AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
1.88 ms         * 美国 爱达荷州 科达伦
1.96 ms         AS20055 [WHOLESAIL-IPV4] 美国 爱达荷州 科达伦 wholesailnetworks.com
12.72 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 普尔曼 wholesailnetworks.com
12.43 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 肯纳威克 wholesailnetworks.com
12.27 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 肯纳威克 wholesailnetworks.com
12.96 ms        AS20055 [WHOLESAIL-IPV4] 美国 俄勒冈州 尤马蒂拉 wholesailnetworks.com
12.73 ms        AS20055 [WHOLESAIL-IPV4] 美国 俄勒冈州 尤马蒂拉 wholesailnetworks.com
12.51 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 西雅图 wholesailnetworks.com
13.09 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 西雅图 wholesailnetworks.com
12.17 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 西雅图 wholesailnetworks.com
12.16 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 西雅图 wholesailnetworks.com
12.56 ms        AS20055 [WHOLESAIL-IPV4] 美国 俄勒冈州 西萨默塞特 wholesailnetworks.com
12.50 ms        * United States of America Washington Yakima
12.44 ms        AS20055 [WHOLESAIL-IPV4] 美国 俄勒冈州 希尔斯伯勒 wholesailnetworks.com
12.85 ms        AS1299 [ARELION-NET] 美国 俄勒冈州 波特兰 arelion.com
26.21 ms        AS1299 [ARELION-NET] 美国 加利福尼亚州 帕洛阿托 arelion.com
27.67 ms        AS1299 [ARELION-NET] 美国 加利福尼亚州 圣何塞 arelion.com
81.16 ms        AS1299 [ARELION-NET] 美国 加利福尼亚州 圣何塞 Telia-CMI-Peer arelion.com
80.91 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 圣何塞 cmi.chinamobile.com 移动
240.61 ms       AS58453 [CMI-INT] 中国 香港 cmi.chinamobile.com 移动
239.37 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
238.88 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
240.66 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
190.55 ms       AS9808 [CMNET] 中国 北京市 chinamobile.com 移动
190.31 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    2379.58 Mbps    2305.66 Mbps    10.51    0.0%
洛杉矶           1328.58 Mbps    2311.48 Mbps    36.91    0.0%
日本东京         33.29 Mbps      1218.57 Mbps    114.20   NULL
联通郑州5G       140.94 Mbps     765.33 Mbps     203.23   NULL
联通Fuzhou       403.19 Mbps     1117.76 Mbps    210.72   0.0%
电信Nanjing5G    113.19 Mbps     1710.00 Mbps    172.74   0.0%
电信Suzhou5G     1249.99 Mbps    2007.62 Mbps    166.84   NULL
移动Chengdu      460.34 Mbps     14.28 Mbps      281.92   0.0%
移动Lanzhou      0.55 Mbps       9.56 Mbps       291.70   NULL
------------------------------------------------------------------------
 总共花费      : 6 分 45 秒
 时间          : Tue Sep  5 09:36:38 CST 2023
------------------------------------------------------------------------
```

总结  
\-- 不跑路的话香中香
