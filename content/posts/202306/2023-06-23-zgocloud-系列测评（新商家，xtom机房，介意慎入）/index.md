---
title: "ZgoCloud 系列测评（新商家，xtom机房，介意慎入）"
date: "2023-06-23"
categories: 
  - "vps"
  - "jp"
---

## 9004套餐系列

<table><tbody><tr><td>Starter</td><td>1<br>Core&nbsp;EPYC&nbsp;<br>9004系列</td><td>1GB DDR5 ECC RAM</td><td>30G PCIe 4.0 NVMe SSD</td><td>700GB/Month/400Mbps</td><td><strong>OsakaJapan</strong></td><td><a href="https://www.zgocloud.cc/aff.php?aff=75&amp;pid=4">购买链接</a></td></tr><tr><td>Standard</td><td>1 Core&nbsp;EPYC&nbsp;<br>9004系列</td><td>2GB DDR5 ECC RAM</td><td>50G PCIe 4.0 NVMe SSD</td><td>1T/Month/400Mbps</td><td><strong>OsakaJapan</strong></td><td><a href="https://www.zgocloud.cc/aff.php?aff=75&amp;pid=5">购买链接</a></td></tr><tr><td>Pro</td><td>2 Core&nbsp;EPYC&nbsp;<br>9004系列</td><td>4GB DDR5 ECC RAM</td><td>80G PCIe 4.0 NVMe SSD</td><td>1.5T/Month/800Mbps</td><td><strong>OsakaJapan</strong></td><td><a href="https://www.zgocloud.cc/aff.php?aff=75&amp;pid=6">购买链接</a></td></tr><tr><td>Premium</td><td>3 Core&nbsp;EPYC<br>9004系列</td><td>6GB DDR5 ECC RAM</td><td>100G PCIe 4.0 NVMe SSD</td><td>2T/Month/800Mbps</td><td><strong>OsakaJapan</strong></td><td><a href="https://www.zgocloud.cc/aff.php?aff=75&amp;pid=7">购买链接</a></td></tr><tr><td>Ultra</td><td>4 Core&nbsp;EPYC&nbsp;<br>9004系列</td><td>8GB DDR5 ECC RAM</td><td>120G PCIe 4.0 NVMe SSD</td><td>2.5T/Month/800Mbps</td><td><strong>OsakaJapan</strong></td><td><a href="https://www.zgocloud.cc/aff.php?aff=75&amp;pid=8">购买链接</a></td></tr></tbody></table>

## 融合怪脚本测试

```

-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD EPYC 9354P 32-Core Processor
 CPU 核心数        : 4
 CPU 频率          : 3249.998 MHz
 CPU 缓存          : 1024 KB
 硬盘空间          : 120.1 GB (25.0 GB 已用)
 内存              : 7825 MB (1431 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 9 days, 21 hour 40 min
 负载              : 0.07, 0.05, 0.05
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-20-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS4785 xTom
 位置              : Osaka / JP
 地区              : Ōsaka
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		4470 Scores
 4 线程测试(多核)得分: 		17873 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		52615.11 MB/s
 单线程写测试:		26845.41 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		76.3 MB/s (18.64 IOPS, 1.37s)		96.9 MB/s (23652 IOPS, 1.08s)
 1GB-1M Block		579 MB/s (552 IOPS, 1.81s)		2.5 GB/s (2381 IOPS, 0.42s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 252.15 MB/s  (63.0k) | 2.07 GB/s    (32.4k)
Write      | 252.81 MB/s  (63.2k) | 2.08 GB/s    (32.5k)
Total      | 504.97 MB/s (126.2k) | 4.16 GB/s    (65.0k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.42 GB/s     (6.6k) | 3.73 GB/s     (3.6k)
Write      | 3.60 GB/s     (7.0k) | 3.97 GB/s     (3.8k)
Total      | 7.03 GB/s    (13.7k) | 7.71 GB/s     (7.5k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 日本 大阪(KIX06S16)
Youtube识别地域: 日本(JP)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 日本 大阪(KIX07S05)
Youtube识别地域: 日本(JP)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：日本
[IPv6]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：日本
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：日本区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：日本区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: JP)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: JP)
 Amazon Prime Video:			Yes (Region: JP)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			JP
 Viu.com:				No
 YouTube CDN:				Osaka 
 Netflix Preferred CDN:			Osaka  
 Spotify Registration:			No
 Steam Currency:			JPY
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:			                Failed
 HotStar:				No
 Disney+:				Yes (Region: JP)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: JP)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:		                Failed
 iQyi Oversea Region:	                Failed
 Viu.com:		                Failed
 YouTube CDN:		                Osaka 
 Netflix Preferred CDN:			Osaka  
 Spotify Registration:			No
 Steam Currency:			Failed
 ChatGPT:				Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【JP】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：56
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：15
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：56
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/23 22:45:57 北京电信 219.141.136.12  电信163 [普通线路]           
2023/06/23 22:45:57 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/23 22:45:57 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/23 22:45:57 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/23 22:45:57 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/23 22:45:57 上海移动 211.136.112.200 测试超时
2023/06/23 22:45:57 广州电信 58.60.188.222   测试超时
2023/06/23 22:45:57 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/23 22:45:57 广州移动 120.196.165.24  测试超时
2023/06/23 22:45:57 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/23 22:45:57 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/23 22:45:57 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS4785 xTom
IPv6 ASN: AS4785 xTom
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.78 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.47 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.75 ms  AS4785  日本, 大阪府, 大阪, xtom.com
8.85 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
1.44 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
62.37 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
63.87 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.78 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.51 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
1.46 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
51.06 ms  AS17676  中国, 北京, bbtec.net
69.26 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
68.96 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
74.81 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
93.88 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
77.51 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.57 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.42 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
1.80 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
7.52 ms  AS17676  日本, 东京都, 东京, bbtec.net
60.33 ms  AS58453  中国, 上海, chinamobile.com, 移动
62.92 ms  AS9808  中国, 上海, chinamobile.com, 移动
62.77 ms  AS9808  中国, 上海, chinamobile.com, 移动
79.22 ms  AS9808  中国, 北京, chinamobile.com, 移动
80.29 ms  AS9808  中国, 北京, chinamobile.com, 移动
80.56 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 935.80 Mbps	 770.49 Mbps	 7.41	  NULL
日本东京	         890.72 Mbps	 760.71 Mbps	 11.45	  0.0%
新加坡		 844.77 Mbps	 761.73 Mbps	 77.61	  0.0%
联通上海5G	 512.79 Mbps	 761.18 Mbps	 51.36	  3.5%
联通WuXi	 30.83 Mbps	 749.09 Mbps	 47.98	  0.0%
电信Suzhou5G	 864.14 Mbps	 713.74 Mbps	 50.44	  NULL
电信上海	         350.87 Mbps	 775.58 Mbps	 37.38	  NULL
移动杭州5G	 827.67 Mbps	 26.66 Mbps	 82.33	  0.0%
移动Zhengzhou5G	 780.74 Mbps	 7.50 Mbps	 84.45	  0.0%
------------------------------------------------------------------------
 总共花费      : 5 分 59 秒
 时间          : Gum Qas 23 10:50:35 carra HKT 2023
------------------------------------------------------------------------
```

## Bench脚本测试

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD EPYC 9354P 32-Core Processor
 CPU Cores          : 4 @ 3249.998 MHz
 CPU Cache          : 1024 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 120.0 GB (24.9 GB Used)
 Total Mem          : 7.6 GB (1.2 GB Used)
 System uptime      : 9 days, 21 hour 54 min
 Load average       : 0.07, 0.06, 0.07
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-20-amd64
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS4785 xTom
 Location           : Osaka / JP
 Region             : Ōsaka
----------------------------------------------------------------------
 I/O Speed(1st run) : 884 MB/s
 I/O Speed(2nd run) : 975 MB/s
 I/O Speed(3rd run) : 954 MB/s
 I/O Speed(average) : 937.7 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    930.18 Mbps       767.05 Mbps         7.38 ms     
 Los Angeles, US  768.82 Mbps       758.71 Mbps         106.84 ms   
 Dallas, US       596.87 Mbps       767.28 Mbps         134.07 ms   
 Montreal, CA     381.11 Mbps       513.51 Mbps         180.65 ms   
 Paris, FR        371.89 Mbps       697.98 Mbps         226.24 ms   
 Amsterdam, NL    341.10 Mbps       752.17 Mbps         233.22 ms   
 Shanghai, CN     426.07 Mbps       749.84 Mbps         50.82 ms    
 Nanjing, CN      902.39 Mbps       768.77 Mbps         39.10 ms    
 Guangzhou, CN    4.65 Mbps         536.44 Mbps         60.36 ms    
 Hongkong, CN     305.69 Mbps       811.01 Mbps         112.03 ms   
 Singapore, SG    869.85 Mbps       776.75 Mbps         80.72 ms    
 Tokyo, JP        872.10 Mbps       753.84 Mbps         8.33 ms     
----------------------------------------------------------------------
```

## Yabs

```
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2023-04-23                    #
# https://github.com/masonr/yet-another-bench-script #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

Fri 23 Jun 2023 11:08:31 PM HKT

Basic System Information:
---------------------------------
Uptime     : 9 days, 22 hours, 4 minutes
Processor  : AMD EPYC 9354P 32-Core Processor
CPU cores  : 4 @ 3249.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 7.6 GiB
Swap       : 0.0 KiB
Disk       : 120.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-20-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : xTom Limited
ASN        : AS4785 xTom
Host       : Cat Networks K.K
Location   : Osaka, Ōsaka (27)
Country    : Japan

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 256.28 MB/s  (64.0k) | 2.52 GB/s    (39.4k)
Write      | 256.96 MB/s  (64.2k) | 2.53 GB/s    (39.6k)
Total      | 513.25 MB/s (128.3k) | 5.06 GB/s    (79.1k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.57 GB/s     (6.9k) | 3.62 GB/s     (3.5k)
Write      | 3.76 GB/s     (7.3k) | 3.86 GB/s     (3.7k)
Total      | 7.33 GB/s    (14.3k) | 7.48 GB/s     (7.3k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 652 Mbits/sec   | 198 Mbits/sec   | 230 ms         
Scaleway        | Paris, FR (10G)           | 653 Mbits/sec   | busy            | 261 ms         
NovoServe       | North Holland, NL (40G)   | 616 Mbits/sec   | busy            | 243 ms         
Uztelecom       | Tashkent, UZ (10G)        | 700 Mbits/sec   | 556 Mbits/sec   | 214 ms         
Clouvider       | NYC, NY, US (10G)         | 754 Mbits/sec   | 343 Mbits/sec   | 157 ms         
Clouvider       | Dallas, TX, US (10G)      | 782 Mbits/sec   | 655 Mbits/sec   | 148 ms         
Clouvider       | Los Angeles, CA, US (10G) | 791 Mbits/sec   | 703 Mbits/sec   | 112 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 688 Mbits/sec   | 450 Mbits/sec   | 230 ms         
Scaleway        | Paris, FR (10G)           | 720 Mbits/sec   | 627 Mbits/sec   | 236 ms         
NovoServe       | North Holland, NL (40G)   | 648 Mbits/sec   | 541 Mbits/sec   | 243 ms         
Uztelecom       | Tashkent, UZ (10G)        | 591 Mbits/sec   | 1.73 Mbits/sec  | 214 ms         
Clouvider       | NYC, NY, US (10G)         | 743 Mbits/sec   | 617 Mbits/sec   | 156 ms         
Clouvider       | Dallas, TX, US (10G)      | 777 Mbits/sec   | 675 Mbits/sec   | 148 ms         
Clouvider       | Los Angeles, CA, US (10G) | 798 Mbits/sec   | 697 Mbits/sec   | 111 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1709                          
Multi Core      | 5233                          
Full Test       | https://browser.geekbench.com/v6/cpu/1696660

YABS completed in 13 min 24 sec
```

![](https://catcat.blog/wp-content/uploads/2023/06/image-9-1024x453.png)

![](https://catcat.blog/wp-content/uploads/2023/06/image-10-281x1024.png)

## 总结

平均国内ping值: 电信 66ms,联通 64ms,移动 100ms.三网软银接入  
体验还行, 少见的日本高，线路还行的服务器。CPU为 EPYC 9004系列(9354P)（老板估计挺舍得砸钱的h）  
适合对性能有要求的场景, 比如远程开发/编译/dd 建站等吧.  
新商家, xtom机房等特殊原因，购买请自行判断。
