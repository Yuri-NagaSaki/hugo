---
title: "Spaceberg 4C6G512G 150T"
date: "2023-07-07"
categories: 
  - "vps"
  - "eu"
---

## 配置

- Processor : AMD EPYC 7402 24-Core Processor

- Cores Memory : 4 GB

- Storage ：512 GB NVMe

- Bandwidth : 150TB

## bench

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD EPYC 7402 24-Core Processor
 CPU Cores          : 4 @ 2794.748 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 512.0 GB (5.2 GB Used)
 Total Mem          : 3.8 GB (238.6 MB Used)
 System uptime      : 0 days, 0 hour 2 min
 Load average       : 0.15, 0.09, 0.03
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-20-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS16276 OVH SAS
 Location           : Roubaix / FR
 Region             : Hauts-de-France
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.6 GB/s
 I/O Speed(2nd run) : 1.7 GB/s
 I/O Speed(3rd run) : 1.8 GB/s
 I/O Speed(average) : 1740.8 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    1504.89 Mbps      2954.15 Mbps        5.04 ms     
 Los Angeles, US  675.75 Mbps       3227.23 Mbps        136.95 ms   
 Dallas, US       651.34 Mbps       2045.19 Mbps        109.85 ms   
 Montreal, CA     174.62 Mbps       696.12 Mbps         94.67 ms    
 Amsterdam, NL    1611.95 Mbps      4832.04 Mbps        12.34 ms    
 Shanghai, CN     184.00 Mbps       1957.64 Mbps        267.92 ms   
 Nanjing, CN      184.26 Mbps       26.45 Mbps          259.46 ms   
 Guangzhou, CN    3.02 Mbps         13.74 Mbps          349.33 ms   
 Singapore, SG    281.52 Mbps       94.87 Mbps          233.27 ms   
 Tokyo, JP        323.10 Mbps       2219.87 Mbps        245.77 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 24 sec
 Timestamp          : 2023-07-07 09:02:33 CST
----------------------------------------------------------------------
```

## Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 16 minutes
Processor  : AMD EPYC 7402 24-Core Processor
CPU cores  : 4 @ 2794.748 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 0.0 KiB
Disk       : 512.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-20-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : OVH SAS
ASN        : AS16276 OVH SAS
Host       : OVH
Location   : Gravelines, Hauts-de-France (HDF)
Country    : France

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 240.12 MB/s  (60.0k) | 3.80 GB/s    (59.4k)
Write      | 240.76 MB/s  (60.1k) | 3.82 GB/s    (59.7k)
Total      | 480.88 MB/s (120.2k) | 7.62 GB/s   (119.1k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 18.57 GB/s   (36.2k) | 20.09 GB/s   (19.6k)
Write      | 19.55 GB/s   (38.2k) | 21.43 GB/s   (20.9k)
Total      | 38.13 GB/s   (74.4k) | 41.52 GB/s   (40.5k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.64 Gbits/sec  | 6.26 Gbits/sec  | 3.54 ms        
Scaleway        | Paris, FR (10G)           | 1.64 Gbits/sec  | busy            | 6.11 ms        
NovoServe       | North Holland, NL (40G)   | 1.63 Gbits/sec  | 3.49 Gbits/sec  | 9.36 ms        
Uztelecom       | Tashkent, UZ (10G)        | 1.33 Gbits/sec  | 1.86 Gbits/sec  | 91.5 ms        
Clouvider       | NYC, NY, US (10G)         | 1.07 Gbits/sec  | 2.28 Gbits/sec  | 76.0 ms        
Clouvider       | Dallas, TX, US (10G)      | 988 Mbits/sec   | 1.53 Gbits/sec  | 117 ms         
Clouvider       | Los Angeles, CA, US (10G) | 1.05 Gbits/sec  | busy            | 133 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.65 Gbits/sec  | 3.27 Gbits/sec  | 3.42 ms        
Scaleway        | Paris, FR (10G)           | 1.65 Gbits/sec  | 3.21 Gbits/sec  | 4.87 ms        
NovoServe       | North Holland, NL (40G)   | busy            | 2.93 Gbits/sec  | 9.16 ms        
Uztelecom       | Tashkent, UZ (10G)        | 1.54 Gbits/sec  | 1.78 Gbits/sec  | 90.9 ms        
Clouvider       | NYC, NY, US (10G)         | 1.53 Gbits/sec  | 2.10 Gbits/sec  | 75.8 ms        
Clouvider       | Dallas, TX, US (10G)      | 1.12 Gbits/sec  | 1.46 Gbits/sec  | 117 ms         
Clouvider       | Los Angeles, CA, US (10G) | 937 Mbits/sec   | 1.31 Gbits/sec  | 132 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1340                          
Multi Core      | 4401                          
Full Test       | https://browser.geekbench.com/v6/cpu/1837688

YABS completed in 12 min 44 sec
```

## Benchy测试

```
# # # # # # # # # # # # # # # # # # # # #
#             Benchy v2.7               #
#    https://github.com/L1so/benchy     #
# # # # # # # # # # # # # # # # # # # # #
#        07 Jul 2023 09:26 CST          #
# # # # # # # # # # # # # # # # # # # # #

Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Debian GNU/Linux 11 (bullseye)     Model       : AMD EPYC 7402 24-Core Processor
Location   : Germany                            Core        : 4 @ 2794.748 MHz
Kernel     : 5.10.0-20-amd64                    AES-NI      : ✔ Enabled
Uptime     : 0 days, 0 hrs, 31 mins, 29 secs    VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 0.0 KiB   

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 511.9 GiB                          ASN         : AS16276   
Disk Usage : 5.2 GiB (1% Used)                  ISP         : OVH SAS   
Mem        : 3.8 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.2 GiB (6% Used)                  IPv6        : ✔ Enabled

Disk Performance Check (xfs on /dev/vda3) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 223.45 MB/s | 224.04 MB/s | 447.50 MB/s | 57.2k  | 57.4k  | 114.5k |
| 64k  | 2.99 GB/s   | 3.00 GB/s   | 5.99 GB/s   | 49.0k  | 49.2k  | 98.2k  |
| 512k | 16.94 GB/s  | 17.84 GB/s  | 34.78 GB/s  | 34.7k  | 36.5k  | 71.2k  |
| 1m   | 18.61 GB/s  | 19.84 GB/s  | 38.46 GB/s  | 19.1k  | 20.3k  | 39.4k  |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |    1.3 Gb/s  |    1.7 Gb/s  |  102.0 ms |
|       | Uztelecom   | Tashkent, UZ    |        busy  |        busy  |   90.7 ms |
|       | Novogara    | Amsterdam, NL   |    1.6 Gb/s  |    2.0 Gb/s  |   12.0 ms |
|       | FiberBy     | Copenhagen, DK  |    1.6 Gb/s  |    3.1 Gb/s  |   20.8 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |    1.5 Gb/s  |    1.7 Gb/s  |  101.7 ms |
|       | Uztelecom   | Tashkent, UZ    |    1.5 Gb/s  |        busy  |   90.8 ms |
|       | Novogara    | Amsterdam, NL   |    1.7 Gb/s  |    3.1 Gb/s  |   12.0 ms |
|       | FiberBy     | Copenhagen, DK  |    1.6 Gb/s  |    3.0 Gb/s  |   20.9 ms |
+---------------------------------------------------------------------------------+

+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 1340                     |
| Multi Core         | 4394                     |
+-----------------------------------------------+
| https://browser.geekbench.com/v6/cpu/1837768  |
+-----------------------------------------------+
| Benchy time spent  | 9 Minutes 52 Seconds     |
+-----------------------------------------------+
| Benchy result      | http://sprunge.us/vA9hju |
+-----------------------------------------------+
```

## 融合怪脚本

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD EPYC 7402 24-Core Processor
 CPU 核心数        : 4
 CPU 频率          : 2794.748 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 512.1 GB (5.2 GB 已用)
 内存              : 3895 MB (252 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 48 min
 负载              : 0.07, 0.22, 0.34
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-20-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS16276 OVH SAS
 IPV4 位置         : Roubaix / Hauts-de-France / FR
 IPV6 ASN          : AS16276 OVH SAS
 IPV6 位置         : Gravelines / FR-59
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1642 Scores
 4 线程测试(多核)得分: 		6596 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		45583.94 MB/s
 单线程写测试:		19973.90 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		37.9 MB/s (9246 IOPS, 2.77s)		45.5 MB/s (11116 IOPS, 2.30s)
 1GB-1M Block		2.3 GB/s (2153 IOPS, 0.46s)		2.6 GB/s (2457 IOPS, 0.41s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 256.41 MB/s  (64.1k) | 3.78 GB/s    (59.2k)
Write      | 257.09 MB/s  (64.2k) | 3.80 GB/s    (59.5k)
Total      | 513.50 MB/s (128.3k) | 7.59 GB/s   (118.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 18.24 GB/s   (35.6k) | 19.70 GB/s   (19.2k)
Write      | 19.20 GB/s   (37.5k) | 21.01 GB/s   (20.5k)
Total      | 37.44 GB/s   (73.1k) | 40.72 GB/s   (39.7k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: LHR(LHR25S41)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: LILLIXFR
视频缓存节点地域: 法国 里尔(LIL1)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
Netflix在您的出口IP所在的国家不提供服务
[IPv6]
Netflix在您的出口IP所在的国家不提供服务
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：法国区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：法国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				No
 YouTube Premium:			Yes (Region: FR)
 Amazon Prime Video:			Yes (Region: FR)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			FR
 Viu.com:				No
 YouTube CDN:				London 
 Netflix Preferred CDN:			Failed
 Spotify Registration:			No
 Steam Currency:			EUR
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				No
 Disney+:				Yes (Region: FR)
 Netflix:				No
 YouTube Premium:			Yes (Region: FR)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Associated with [LILLIXFR]
 Netflix Preferred CDN:			Failed
 Spotify Registration:			No
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【FR】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：35
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：39
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
  qq邮箱: Yes
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：34
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
2023/07/07 09:44:45 北京电信 219.141.136.12  电信163 [普通线路]           
2023/07/07 09:44:45 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/07 09:44:45 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/07 09:44:45 上海电信 202.96.209.133  电信163 [普通线路]           
2023/07/07 09:44:45 上海联通 210.22.97.1     联通4837[普通线路]           
2023/07/07 09:44:45 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/07 09:44:45 广州电信 58.60.188.222   电信163 [普通线路]           
2023/07/07 09:44:45 广州联通 210.21.196.6    联通4837[普通线路]           
2023/07/07 09:44:45 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/07/07 09:44:45 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/07 09:44:45 成都联通 119.6.6.6       联通4837[普通线路]           
2023/07/07 09:44:45 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
1.92 ms  AS16276  法国, 上法兰西大区, 鲁贝, ovh.com
2.21 ms  *  局域网
1.91 ms  *  局域网
2.84 ms  *  局域网
6.02 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
5.85 ms  *  局域网
9.27 ms  AS3356  英国, 伦敦, level3.com
110.01 ms  AS3356  英国, 伦敦, level3.com
373.89 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
362.44 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
1.88 ms  AS16276  法国, 上法兰西大区, 鲁贝, ovh.com
2.27 ms  *  局域网
1.87 ms  *  局域网
56.32 ms  *  局域网
6.05 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
6.20 ms  *  局域网
153.57 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
234.54 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
245.99 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
235.57 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
231.56 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
232.73 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
232.27 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
237.61 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
2.12 ms  AS16276  法国, 上法兰西大区, 鲁贝, ovh.com
2.22 ms  *  局域网
1.89 ms  *  局域网
2.99 ms  *  局域网
5.82 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
5.63 ms  *  局域网
7.02 ms  AS16276  美国, 伊利诺伊州, 芝加哥, ovh.com
15.24 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
12.89 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
229.91 ms  AS58453  中国, 上海, chinamobile.com, 移动
229.56 ms  AS9808  中国, 上海, chinamobile.com, 移动
230.35 ms  AS9808  中国, 上海, chinamobile.com, 移动
231.32 ms  AS9808  中国, 上海, chinamobile.com, 移动
201.35 ms  AS9808  中国, 北京, chinamobile.com, 移动
201.43 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 1503.08 Mbps	 2672.59 Mbps	 4.91	  0.0%
洛杉矶		 631.77 Mbps	 6005.60 Mbps	 137.69	  NULL
新加坡		 603.22 Mbps	 4915.78 Mbps	 159.31	  0.0%
联通湖南5G	 226.97 Mbps	 18.86 Mbps	 192.99	  NULL
联通海南	 404.95 Mbps	 697.97 Mbps	 200.41	  NULL
电信天津	 102.55 Mbps	 1883.11 Mbps	 222.78	  NULL
电信天津5G	 92.77 Mbps	 135.99 Mbps	 229.30	  NULL
移动Beijing	 1003.65 Mbps	 3178.89 Mbps	 203.70	  0.3%
移动Chengdu	 70.07 Mbps	 284.74 Mbps	 186.41	  0.0%
------------------------------------------------------------------------
 总共花费      : 6 分 37 秒
 时间          : Fri Jul  7 09:50:11 CST 2023
------------------------------------------------------------------------
```

## Lscpu

![](https://catcat.blog/wp-content/uploads/2023/07/image-9-1024x752.png)

## Memory

![](https://catcat.blog/wp-content/uploads/2023/07/image-10-1024x131.png)

## Disk

![](https://catcat.blog/wp-content/uploads/2023/07/image-11-1024x354.png)

## SpeedTest

![](https://catcat.blog/wp-content/uploads/2023/10/image-167.png)
