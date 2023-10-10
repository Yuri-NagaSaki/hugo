---
title: "Advin Servers 荷兰7950x vds测评"
date: "2023-06-25"
categories: 
  - "vps"
  - "eu"
---

## bench.sh测试

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X 16-Core Processor
 CPU Cores          : 4 @ 4491.428 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 984.6 GB (1.9 GB Used)
 Total Mem          : 15.6 GB (138.3 MB Used)
 System uptime      : 0 days, 0 hour 4 min
 Load average       : 0.06, 0.20, 0.10
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-21-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Offline
 Organization       : AS206216 Advin Services LLC
 Location           : Kerkrade / NL
 Region             : Limburg
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.4 GB/s
 I/O Speed(2nd run) : 1.5 GB/s
 I/O Speed(3rd run) : 1.8 GB/s
 I/O Speed(average) : 1604.3 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    13052.28 Mbps     15632.96 Mbps       0.09 ms     
 Los Angeles, US  629.24 Mbps       406.68 Mbps         143.65 ms   
 Dallas, US       647.34 Mbps       503.76 Mbps         115.62 ms   
 Montreal, CA     179.94 Mbps       525.39 Mbps         86.82 ms    
 Shanghai, CN     664.47 Mbps       12495.12 Mbps       0.10 ms     
 Nanjing, CN      257.06 Mbps       18.14 Mbps          149.88 ms   
 Guangzhou, CN    342.12 Mbps       342.12 Mbps         191.57 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 55 sec
 Timestamp          : 2023-06-25 11:57:32 UTC
----------------------------------------------------------------------
```

## Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 14 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 4 @ 4491.428 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 15.6 GiB
Swap       : 0.0 KiB
Disk       : 984.6 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-21-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : Advin Services LLC
ASN        : AS206216 Advin Services LLC
Host       : MB \Lirutis\
Location   : Kerkrade, Limburg (LI)
Country    : Netherlands

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 41.04 MB/s   (10.2k) | 626.24 MB/s   (9.7k)
Write      | 41.13 MB/s   (10.2k) | 629.53 MB/s   (9.8k)
Total      | 82.17 MB/s   (20.5k) | 1.25 GB/s    (19.6k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.02 GB/s     (2.0k) | 1.29 GB/s     (1.2k)
Write      | 1.07 GB/s     (2.1k) | 1.38 GB/s     (1.3k)
Total      | 2.10 GB/s     (4.1k) | 2.67 GB/s     (2.6k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 5.74 Gbits/sec  | 535 Mbits/sec   | 13.9 ms        
Scaleway        | Paris, FR (10G)           | busy            | busy            | 13.5 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 8.08 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | busy            | 86.6 ms        
Clouvider       | NYC, NY, US (10G)         | busy            | busy            | 82.1 ms        
Clouvider       | Dallas, TX, US (10G)      | busy            | busy            | 123 ms         
Clouvider       | Los Angeles, CA, US (10G) | busy            | busy            | 143 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2588                          
Multi Core      | 7363                          
Full Test       | https://browser.geekbench.com/v6/cpu/1716743

YABS completed in 7 min 24 sec
```

## 融合怪脚本测试

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD Ryzen 9 7950X 16-Core Processor
 CPU 核心数        : 4
 CPU 频率          : 4491.428 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 985.0 GB (2.0 GB 已用)
 内存              : 16008 MB (118 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 31 min
 负载              : 0.00, 0.07, 0.18
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-21-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS206216 Advin Services LLC
 位置              : Kerkrade / NL
 地区              : Limburg
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		6070 Scores
 4 线程测试(多核)得分: 		22861 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		68929.63 MB/s
 单线程写测试:		35451.05 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		47.3 MB/s (11.55 IOPS, 2.22s)		64.7 MB/s (15784 IOPS, 1.62s)
 1GB-1M Block		2.6 GB/s (2468 IOPS, 0.41s)		2.4 GB/s (2313 IOPS, 0.43s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 40.66 MB/s   (10.1k) | 502.19 MB/s   (7.8k)
Write      | 40.75 MB/s   (10.1k) | 504.83 MB/s   (7.8k)
Total      | 81.41 MB/s   (20.3k) | 1.00 GB/s    (15.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.12 GB/s     (2.1k) | 1.12 GB/s     (1.0k)
Write      | 1.18 GB/s     (2.3k) | 1.19 GB/s     (1.1k)
Total      | 2.30 GB/s     (4.4k) | 2.31 GB/s     (2.2k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA16S31)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：荷兰
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：荷兰区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: US)
 Netflix:				Originals Only
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: NL)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				Frankfurt 
 Netflix Preferred CDN:			Associated with [RETN Limited] in [Budapest ]
 Spotify Registration:			Yes (Region: NL)
 Steam Currency:			EUR
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【GB】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：0
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
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/25 12:21:01 北京电信 219.141.136.12  测试超时
2023/06/25 12:21:01 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/25 12:21:01 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/25 12:21:01 上海电信 202.96.209.133  测试超时
2023/06/25 12:21:01 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/25 12:21:01 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/25 12:21:01 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/25 12:21:01 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/25 12:21:01 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/25 12:21:01 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/25 12:21:01 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/25 12:21:01 成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS206216 Advin Services LLC
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
13.11 ms  AS206216  荷兰, 林堡省, 艾赫尔斯霍芬, buyvm.net
17.27 ms  *  局域网
47.62 ms  AS49581  荷兰, 林堡省, 艾赫尔斯霍芬, tube-hosting.de
8.42 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
8.48 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
15.10 ms  AS1299  英国, 伦敦, telia.com
15.98 ms  AS1299  英国, 伦敦, telia.com
203.74 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
204.75 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
21.81 ms  AS206216  荷兰, 林堡省, 艾赫尔斯霍芬, buyvm.net
22.14 ms  *  局域网
16.49 ms  AS49581  荷兰, 林堡省, 艾赫尔斯霍芬, tube-hosting.de
8.81 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
8.60 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
8.32 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
8.14 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
175.04 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
170.72 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
162.26 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
165.88 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
181.56 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
14.14 ms  AS206216  荷兰, 林堡省, 艾赫尔斯霍芬, buyvm.net
16.85 ms  *  局域网
0.32 ms  AS49581  荷兰, 林堡省, 艾赫尔斯霍芬, tube-hosting.de
8.53 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
8.55 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
16.04 ms  AS1299  英国, 伦敦, telia.com
16.36 ms  AS1299  英国, 伦敦, telia.com
15.18 ms  AS1299  英国, 伦敦, telia.com
298.28 ms  AS58453  中国, 上海, chinamobile.com, 移动
296.52 ms  AS9808  中国, 上海, chinamobile.com, 移动
301.45 ms  AS9808  中国, 上海, chinamobile.com, 移动
320.94 ms  AS9808  中国, 北京, chinamobile.com, 移动
321.62 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 10393.23 Mbps	 16871.41 Mbps	 0.12	  0.0%
洛杉矶		 1298.87 Mbps	 142.87 Mbps	 151.91	  0.0%
新加坡		 1203.65 Mbps	 560.75 Mbps	 184.41	  0.0%
联通上海5G	 607.40 Mbps	 3961.20 Mbps	 175.41	  0.0%
联通湖南5G	 336.03 Mbps	 246.45 Mbps	 182.17	  NULL
电信天津	 1.06 Mbps	 3257.68 Mbps	 174.02	  NULL
移动Chengdu	 5.60 Mbps	 4180.42 Mbps	 299.88	  0.0%
移动杭州5G	 0.99 Mbps	 1846.79 Mbps	 294.82	  3.7%
------------------------------------------------------------------------
 总共花费      : 6 分 27 秒
 时间          : Sun Jun 25 12:25:59 UTC 2023
------------------------------------------------------------------------
```

## SpeedTest

![](https://catcat.blog/wp-content/uploads/2023/06/image-12.png)
