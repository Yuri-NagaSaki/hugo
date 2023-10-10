---
title: "Spaceberg 促销 7T存储 50G口下行不限流量测评"
date: "2023-06-17"
categories: 
  - "vps"
  - "eu"
---

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : Intel(R) Xeon(R) Gold 6226R CPU @ 2.90GHz
 CPU 核心数        : 4
 CPU 频率          : 2893.202 MHz
 CPU 缓存          : 22528 KB
 硬盘空间          : 7168.1 GB (53.0 GB 已用)
 内存              : 3895 MB (366 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 2 min
 负载              : 0.28, 0.16, 0.06
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-20-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS16276 OVH SAS
 位置              : Lille / FR
 地区              : Hauts-de-France
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1211 Scores
 4 线程测试(多核)得分: 		4820 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		23407.90 MB/s
 单线程写测试:		16189.10 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		77.4 MB/s (0.05 IOPS, 1.35s)		108 MB/s (26281 IOPS, 0.97s)
 1GB-1M Block		2.0 GB/s (1882 IOPS, 0.53s)		3.5 GB/s (3314 IOPS, 0.30s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 363.79 MB/s  (90.9k) | 4.23 GB/s    (66.1k)
Write      | 364.75 MB/s  (91.1k) | 4.25 GB/s    (66.5k)
Total      | 728.55 MB/s (182.1k) | 8.49 GB/s   (132.6k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 5.73 GB/s    (11.2k) | 7.30 GB/s     (7.1k)
Write      | 6.04 GB/s    (11.8k) | 7.78 GB/s     (7.6k)
Total      | 11.78 GB/s   (23.0k) | 15.08 GB/s   (14.7k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA16S31)
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
区域：荷兰区
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
 Amazon Prime Video:			Yes (Region: NL)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			FR
 Viu.com:				No
 YouTube CDN:				Frankfurt 
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
 Tiktok Region:		【NL】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：43
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：11
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：NO
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：42
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
2023/06/17 20:52:34 北京电信 219.141.136.12  电信163 [普通线路]           
2023/06/17 20:52:34 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/17 20:52:34 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/17 20:52:34 上海电信 202.96.209.133  测试超时
2023/06/17 20:52:34 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/17 20:52:34 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/17 20:52:34 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/17 20:52:34 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/17 20:52:34 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/17 20:52:34 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/17 20:52:34 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/17 20:52:34 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS16276 OVH SAS
IPv6 ASN: AS16276 OVH SAS
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.11 ms  *  局域网
0.19 ms  *  局域网
0.20 ms  *  局域网
5.73 ms  *  局域网
4.11 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
4.40 ms  *  局域网
7.56 ms  AS3356  英国, 伦敦, level3.com
9.66 ms  AS3356  英国, 伦敦, level3.com
270.25 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
273.36 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.70 ms  *  局域网
0.23 ms  *  局域网
0.23 ms  *  局域网
0.58 ms  *  局域网
4.28 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
4.02 ms  *  局域网
147.39 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
232.54 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
231.84 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
239.09 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
230.66 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
250.33 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
238.39 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.13 ms  *  局域网
0.23 ms  *  局域网
0.23 ms  *  局域网
1.29 ms  *  局域网
4.26 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
4.07 ms  *  局域网
5.12 ms  AS16276  美国, 伊利诺伊州, 芝加哥, ovh.com
11.45 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
11.54 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
233.00 ms  AS58453  中国, 上海, chinamobile.com, 移动
245.04 ms  AS9808  中国, 上海, chinamobile.com, 移动
236.18 ms  AS9808  中国, 上海, chinamobile.com, 移动
204.80 ms  AS9808  中国, 北京, chinamobile.com, 移动
206.94 ms  AS9808  中国, 北京, chinamobile.com, 移动
206.35 ms  AS9808  中国, 北京, chinamobile.com, 移动
208.20 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 2375.87 Mbps	 2990.87 Mbps	 4.38	  0.0%
洛杉矶		 467.87 Mbps	 2409.44 Mbps	 134.68	  0.0%
新加坡		 610.90 Mbps	 1835.42 Mbps	 153.20	  0.0%
联通沈阳	 94.16 Mbps	 133.10 Mbps	 174.86	  0.0%
联通海南	 501.32 Mbps	 743.56 Mbps	 185.02	  NULL
电信天津	 0.83 Mbps	 2005.90 Mbps	 241.55	  NULL
电信Zhenjiang5G	 2.87 Mbps	 2164.26 Mbps	 229.36	  NULL
移动Beijing	 654.75 Mbps	 3536.51 Mbps	 262.90	  0.0%
移动Chengdu	 537.41 Mbps	 4926.03 Mbps	 195.45	  0.0%
------------------------------------------------------------------------
 总共花费      : 6 分 41 秒
 时间          : Sat Jun 17 20:58:13 CST 2023
------------------------------------------------------------------------
```

## Speedtest

![](https://catcat.blog/wp-content/uploads/2023/06/image-7.png)

## Yabs

```
root@sakura:~# curl -sL yabs.sh | bash
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2023-04-23                    #
# https://github.com/masonr/yet-another-bench-script #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

Sat 17 Jun 2023 09:01:57 PM CST

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 12 minutes
Processor  : Intel(R) Xeon(R) Gold 6226R CPU @ 2.90GHz
CPU cores  : 4 @ 2893.202 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 0.0 KiB
Disk       : 6.9 TiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-20-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : OVH SAS
ASN        : AS16276 OVH SAS
Host       : OVH
Location   : Roubaix, Hauts-de-France (HDF)
Country    : France

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 359.92 MB/s  (89.9k) | 4.33 GB/s    (67.6k)
Write      | 360.87 MB/s  (90.2k) | 4.35 GB/s    (68.0k)
Total      | 720.79 MB/s (180.1k) | 8.68 GB/s   (135.6k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 5.77 GB/s    (11.2k) | 6.90 GB/s     (6.7k)
Write      | 6.07 GB/s    (11.8k) | 7.36 GB/s     (7.1k)
Total      | 11.84 GB/s   (23.1k) | 14.26 GB/s   (13.9k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 5.49 Gbits/sec  | 5.40 Gbits/sec  | 4.18 ms        
Scaleway        | Paris, FR (10G)           | busy            | busy            | 4.16 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 10.8 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | busy            | 90.4 ms        
Clouvider       | NYC, NY, US (10G)         | 1.02 Gbits/sec  | 233 Mbits/sec   | 78.4 ms        
Clouvider       | Dallas, TX, US (10G)      | 1.35 Gbits/sec  | 873 Mbits/sec   | 115 ms         
Clouvider       | Los Angeles, CA, US (10G) | 1.26 Gbits/sec  | 631 Mbits/sec   | 136 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 5.49 Gbits/sec  | 5.31 Gbits/sec  | 4.19 ms        
Scaleway        | Paris, FR (10G)           | busy            | 5.02 Gbits/sec  | 4.15 ms        
NovoServe       | North Holland, NL (40G)   | 5.47 Gbits/sec  | 4.31 Gbits/sec  | 10.7 ms        
Uztelecom       | Tashkent, UZ (10G)        | 1.98 Gbits/sec  | 1.05 Gbits/sec  | 90.1 ms        
Clouvider       | NYC, NY, US (10G)         | 1.57 Gbits/sec  | 240 Mbits/sec   | 78.3 ms        
Clouvider       | Dallas, TX, US (10G)      | 1.31 Gbits/sec  | 771 Mbits/sec   | 115 ms         
Clouvider       | Los Angeles, CA, US (10G) | 1.14 Gbits/sec  | 737 Mbits/sec   | 136 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1299                          
Multi Core      | 4049                          
Full Test       | https://browser.geekbench.com/v6/cpu/1628481

YABS completed in 12 min 34 sec
```

```
----------------------------------------------------------------------
 CPU Model          : Intel(R) Xeon(R) Gold 6226R CPU @ 2.90GHz
 CPU Cores          : 4 @ 2893.202 MHz
 CPU Cache          : 22528 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 6.9 TB (4.5 TB Used)
 Total Mem          : 3.8 GB (1.7 GB Used)
 Total Swap         : 4.0 GB (2.0 GB Used)
 System uptime      : 16 days, 0 hour 20 min
 Load average       : 1.01, 0.80, 0.69
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.1.0-0.deb11.7-amd64
 TCP CC             : bbrx
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS16276 OVH SAS
 Location           : Lille / FR
 Region             : Hauts-de-France
----------------------------------------------------------------------
 I/O Speed(1st run) : 649 MB/s
 I/O Speed(2nd run) : 687 MB/s
 I/O Speed(3rd run) : 744 MB/s
 I/O Speed(average) : 693.3 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    1682.65 Mbps      1484.89 Mbps        4.34 ms     
 Los Angeles, US  660.23 Mbps       1503.34 Mbps        138.17 ms   
 Dallas, US       806.01 Mbps       1007.79 Mbps        110.54 ms   
 Montreal, CA     497.25 Mbps       706.98 Mbps         84.97 ms    
 Paris, FR        1609.10 Mbps      2049.92 Mbps        4.33 ms     
 Amsterdam, NL    1983.41 Mbps      1153.91 Mbps        10.48 ms    
 Shanghai, CN     581.85 Mbps       541.91 Mbps         248.65 ms   
 Nanjing, CN      25.62 Mbps        720.79 Mbps         264.81 ms   
 Guangzhou, CN    0.31 Mbps         72.15 Mbps          0.05 ms     
 Singapore, SG    391.38 Mbps       348.14 Mbps         230.61 ms   
 Tokyo, JP        304.09 Mbps       1428.57 Mbps        232.74 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 45 sec
 Timestamp          : 2023-07-05 14:53:03 CST
----------------------------------------------------------------------
```

```
# # # # # # # # # # # # # # # # # # # # #
#             Benchy v2.7               #
#    https://github.com/L1so/benchy     #
# # # # # # # # # # # # # # # # # # # # #
#        05 Jul 2023 21:07 CST          #
# # # # # # # # # # # # # # # # # # # # #

Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Debian GNU/Linux 11 (bullseye)     Model       : Intel(R) Xeon(R) Gold 6226R CPU @ 2.90GHz
Location   : Netherlands                        Core        : 4 @ 2893.202 MHz
Kernel     : 6.1.0-0.deb11.7-amd64              AES-NI      : ✔ Enabled
Uptime     : 16 days, 6 hrs, 40 mins, 11 secs   VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 4.0 GiB   

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 6.9 TiB                            ASN         : AS16276   
Disk Usage : 4.5 TiB (65% Used)                 ISP         : OVH SAS   
Mem        : 3.8 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 1.7 GiB (45% Used)                 IPv6        : ✔ Enabled

Disk Performance Check (xfs on /dev/vda3) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 110.96 MB/s | 111.26 MB/s | 222.23 MB/s | 28.4k  | 28.5k  | 56.9k  |
| 64k  | 908.23 MB/s | 913.01 MB/s | 1.77 GB/s   | 14.5k  | 14.6k  | 29.1k  |
| 512k | 1.29 GB/s   | 1.36 GB/s   | 2.65 GB/s   | 2.6k   | 2.8k   | 5.4k   |
| 1m   | 1.66 GB/s   | 1.77 GB/s   | 3.43 GB/s   | 1.7k   | 1.8k   | 3.5k   |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |    1.7 Gb/s  |    1.0 Gb/s  |  106.8 ms |
|       | Uztelecom   | Tashkent, UZ    |    2.2 Gb/s  |  723.5 Mb/s  |   92.0 ms |
|       | Novogara    | Amsterdam, NL   |    2.4 Gb/s  |    1.4 Gb/s  |   11.4 ms |
|       | FiberBy     | Copenhagen, DK  |    2.4 Gb/s  |    1.5 Gb/s  |   19.9 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |    1.7 Gb/s  |  986.0 Mb/s  |  106.7 ms |
|       | Uztelecom   | Tashkent, UZ    |    1.9 Gb/s  |        busy  |   92.0 ms |
|       | Novogara    | Amsterdam, NL   |    2.1 Gb/s  |    2.1 Gb/s  |   11.4 ms |
|       | FiberBy     | Copenhagen, DK  |    2.0 Gb/s  |    1.9 Gb/s  |   19.9 ms |
+---------------------------------------------------------------------------------+

+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 1062                     |
| Multi Core         | 2258                     |
+-----------------------------------------------+
| https://browser.geekbench.com/v6/cpu/1821320  |
+-----------------------------------------------+
| Benchy time spent  | 12 Minutes 45 Seconds    |
+-----------------------------------------------+
| Benchy result      | http://sprunge.us/cdq4Go |
+-----------------------------------------------+
```
