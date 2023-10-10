---
title: "server-factory 瑞典ipv6测评"
date: "2023-07-23"
categories: 
  - "vps"
  - "eu"
---

## 套餐配置

```
Provider      : server-factory
Type/Plan     : ipv6 only 
Processor     : AMD EPYC™ 7452
Num of Core(s): 1 Core(s) (25 % LIMIT)
Memory        : 2 GB DDR4 3200 MHZ ECC
Storage       : 2 GiB DDR4 3200 MHZ ECC
TRAFFIC       : 100 GiB FOR 24 HOURS
IPV6 SUBNET   : /64

```

## 性能测试

## Yabs

```
---------------------------------
Uptime     : 0 days, 0 hours, 6 minutes
Processor  : AMD EPYC 7452 32-Core Processor
CPU cores  : 1 @ 2349.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 0.0 KiB
Disk       : 24.5 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-10-amd64
VM Type    : KVM
IPv4/IPv6  : ❌ Offline / ✔ Online

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 222.02 MB/s  (55.5k) | 2.55 GB/s    (39.9k)
Write      | 222.61 MB/s  (55.6k) | 2.56 GB/s    (40.1k)
Total      | 444.64 MB/s (111.1k) | 5.12 GB/s    (80.0k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 8.07 GB/s    (15.7k) | 8.59 GB/s     (8.3k)
Write      | 8.50 GB/s    (16.6k) | 9.17 GB/s     (8.9k)
Total      | 16.57 GB/s   (32.3k) | 17.77 GB/s   (17.3k)

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | busy            | busy            | -- 
Scaleway        | Paris, FR (10G)           | 730 Mbits/sec   | 977 Mbits/sec   | 32.7 ms        
NovoServe       | North Holland, NL (40G)   | 698 Mbits/sec   | busy            | 24.5 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | busy            | -- 
Clouvider       | NYC, NY, US (10G)         | busy            | busy            | -- 
Clouvider       | Dallas, TX, US (10G)      | busy            | busy            | -- 
Clouvider       | Los Angeles, CA, US (10G) | busy            | busy            | -- 

Geekbench releases can only be downloaded over IPv4. FTP the Geekbench files and run manually.

YABS completed in 2 min 42 sec
```

## 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7452 32-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 2349.998 MHz
 CPU 缓存          : L1: 64.00 KB / L2: 512.00 KB / L3: 16.00 MB
 硬盘空间          : 2.20 GiB / 24.03 GiB
 启动盘路径        : /dev/sda2
 内存              : 411.04 MiB / 1.89 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 12 min
 负载              : 0.12, 0.17, 0.12
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-10-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 独立映射,独立过滤,不支持回环
 IPV4 ASN          : AS13335 Cloudflare, Inc.
 IPV4 位置         : Bielefeld / North Rhine-Westphalia / DE
 IPV6 ASN          : AS206075 Maximilian Jacobsen
 IPV6 位置         : Stockholm / SE-AB
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           1649 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          44822.73 MB/s
 单线程写测试:          19983.94 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         87.7 MB/s (21.41 IOPS, 1.20s))          101 MB/s (24625 IOPS, 1.04s)
 1GB-1M Block           3.3 GB/s (3129 IOPS, 0.32s)             3.5 GB/s (3330 IOPS, 0.30s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 197.04 MB/s  (49.2k) | 2.73 GB/s    (42.6k)
Write      | 197.56 MB/s  (49.3k) | 2.74 GB/s    (42.8k)
Total      | 394.60 MB/s  (98.6k) | 5.47 GB/s    (85.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 8.99 GB/s    (17.5k) | 10.51 GB/s   (10.2k)
Write      | 9.47 GB/s    (18.5k) | 11.21 GB/s   (10.9k)
Total      | 18.47 GB/s   (36.0k) | 21.73 GB/s   (21.2k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: IAD(IAD23S03)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS15S46)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：德国
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：瑞典
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：德国区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：瑞典区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: DE)
 HotStar:                               No
 Disney+:                               Yes (Region: DE)
 Netflix:                               Yes (Region: DE)
 YouTube Premium:                       Yes (Region: DE)
 Amazon Prime Video:                    Yes (Region: DE)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Washington DC 
 Netflix Preferred CDN:                 Dusseldorf  
 Spotify Registration:                  Yes (Region: DE)
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: DE)
 Netflix:                               Yes (Region: SE)
 YouTube Premium:                       Yes (Region: DE)
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Amsterdam 
 Netflix Preferred CDN:                 Stockholm  
 Spotify Registration:                  Yes (Region: DE)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【DE】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：100
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
  欺诈分数(越低越好)：3
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Content Delivery Network
Google搜索可行性：NO
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：0
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
2023/07/23 15:41:53 北京电信 219.141.136.12  电信163 [普通线路]           
2023/07/23 15:41:53 北京联通 202.106.50.1    测试超时
2023/07/23 15:41:53 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/23 15:41:53 上海电信 202.96.209.133  电信163 [普通线路]           
2023/07/23 15:41:53 上海联通 210.22.97.1     测试超时
2023/07/23 15:41:53 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/23 15:41:53 广州电信 58.60.188.222   电信163 [普通线路]           
2023/07/23 15:41:53 广州联通 210.21.196.6    测试超时
2023/07/23 15:41:53 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/07/23 15:41:53 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/23 15:41:53 成都联通 119.6.6.6       测试超时
2023/07/23 15:41:53 成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
2.26 ms  AS13335  中国, 香港, cloudflare.com
2.77 ms  AS13335  瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
2.69 ms  AS1299  瑞典, 斯德哥尔摩省, 斯德哥尔摩, telia.com
2.88 ms  AS1299  瑞典, 斯德哥尔摩省, 斯德哥尔摩, telia.com
34.57 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
27.03 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
105.11 ms  AS4134  德国, 黑森州, 法兰克福, chinatelecom.com.cn, 电信
318.00 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
329.89 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
312.38 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
2.19 ms  AS13335  中国, 香港, cloudflare.com
3.22 ms  AS13335  瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
2.75 ms  *  瑞典, 斯德哥尔摩省, 斯德哥尔摩, netnod.se
2.60 ms  AS1239  瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.com
13.15 ms  AS1239  丹麦, 首都大区, 哥本哈根, sprint.com
25.25 ms  AS1239  荷兰, 北荷兰省, 阿姆斯特丹, sprint.com
29.97 ms  AS1239  英国, 伦敦, sprint.com
102.36 ms  AS1239  英国, 伦敦, sprint.com
119.72 ms  AS1239  美国, 纽约州, 纽约, sprint.com
122.02 ms  AS1239  美国, 马里兰州, 阿比特斯, sprint.com
111.88 ms  AS1239  美国, 华盛顿, sprint.com
131.85 ms  AS1239  美国, 南卡罗来纳州, 费尔法克斯, sprint.com
136.04 ms  AS1239  美国, 乔治亚州, 亚特兰大, sprint.com
141.89 ms  AS1239  美国, 德克萨斯州, 沃思堡, sprint.com
171.41 ms  AS1239  美国, 加利福尼亚州, 里亚托, sprint.com
162.25 ms  AS1239  美国, 加利福尼亚州, 洛杉矶, sprint.com
312.03 ms  AS1239  美国, 加利福尼亚州, 洛杉矶, sprint.com
334.91 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
330.40 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
341.70 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
339.10 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
340.40 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
2.19 ms  AS13335  中国, 香港, cloudflare.com
3.30 ms  AS13335  瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
2.67 ms  AS1299  瑞典, 斯德哥尔摩省, 斯德哥尔摩, telia.com
2.94 ms  AS1299  瑞典, 斯德哥尔摩省, 斯德哥尔摩, telia.com
27.68 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
34.29 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
36.45 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
34.82 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
320.78 ms  AS58453  中国, 上海, chinamobile.com, 移动
241.76 ms  AS9808  中国, 上海, chinamobile.com, 移动
303.81 ms  AS9808  中国, 上海, chinamobile.com, 移动
325.40 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    725.08 Mbps     997.77 Mbps     23.99    0.0%
洛杉矶           65.47 Mbps      341.55 Mbps     162.64   2.0%
中国香港         460.65 Mbps     217.91 Mbps     216.96   9.1%
联通WuXi         609.96 Mbps     421.45 Mbps     278.96   0.0%
联通上海5G       123.19 Mbps     984.24 Mbps     259.27   0.0%
------------------------------------------------------------------------
 总共花费      : 6 分 2 秒
 时间          : Sun Jul 23 15:46:42 CEST 2023
------------------------------------------------------------------------
```

## PassMark PerformanceTest Linux

```
AMD EPYC 7452 32-Core Processor (x86_64)
1 cores @ 0 MHz  |  1.9 GiB RAM
Number of Processes: 1  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          2094
  Integer Math                     4754 Million Operations/s
  Floating Point Math              3462 Million Operations/s
  Prime Numbers                    16.4 Million Primes/s
  Sorting                          2974 Thousand Strings/s
  Encryption                       1161 MB/s
  Compression                      20887 KB/s
  CPU Single Threaded              2018 Million Operations/s
  Physics                          283 Frames/s
  Extended Instructions (SSE)      1461 Million Matrices/s

Memory Mark:                       1292
  Database Operations              601 Thousand Operations/s
  Memory Read Cached               24928 MB/s
  Memory Read Uncached             11532 MB/s
  Memory Write                     11334 MB/s
  Available RAM                    1359 Megabytes
  Memory Latency                   52 Nanoseconds
  Memory Threaded                  11649 MB/s
--------------------------------------------------------------------------
```

## benchy

```
Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Debian GNU/Linux 12 (bookworm)     Model       : AMD EPYC 7452 32-Core Processor
Location   : Germany                            Core        : 1 @ 2349.998 MHz
Kernel     : 6.1.0-10-amd64                     AES-NI      : ✔ Enabled
Uptime     : 0 days, 0 hrs, 37 mins, 37 secs    VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 0.0 KiB   

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 24.0 GiB                           ASN         : AS13335   
Disk Usage : 2.2 GiB (9% Used)                  ISP         : Cloudflare, Inc.
Mem        : 1.9 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.5 GiB (27% Used)                 IPv6        : ✔ Enabled

Disk Performance Check (ext4 on /dev/sda2) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 230.58 MB/s | 231.19 MB/s | 461.78 MB/s | 59.0k  | 59.2k  | 118.2k |
| 64k  | 2.69 GB/s   | 2.70 GB/s   | 5.39 GB/s   | 44.1k  | 44.3k  | 88.4k  |
| 512k | 4.30 GB/s   | 4.53 GB/s   | 8.84 GB/s   | 8.8k   | 9.3k   | 18.1k  |
| 1m   | 9.44 GB/s   | 10.07 GB/s  | 19.51 GB/s  | 9.7k   | 10.3k  | 20.0k  |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |  909.8 Mb/s  |    1.2 Gb/s  |  117.4 ms |
|       | Uztelecom   | Tashkent, UZ    |        busy  |    1.4 Gb/s  |  174.8 ms |
|       | Novogara    | Amsterdam, NL   |  906.5 Mb/s  |  841.7 Mb/s  |   24.7 ms |
|       | FiberBy     | Copenhagen, DK  |  912.0 Mb/s  |    1.4 Gb/s  |   11.6 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |        busy  |        busy  |  113.3 ms |
|       | Uztelecom   | Tashkent, UZ    |  452.3 Mb/s  |  926.9 Mb/s  |   73.5 ms |
|       | Novogara    | Amsterdam, NL   |  873.7 Mb/s  |    1.0 Gb/s  |   22.3 ms |
|       | FiberBy     | Copenhagen, DK  |  666.4 Mb/s  |  963.5 Mb/s  |   11.5 ms |
+---------------------------------------------------------------------------------+
+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 1370                    |
| Multi Core         | 1324                     |
+-----------------------------------------------+
```

## Unix 测试

```
------------------------------------------------------------------------
Benchmark Run: Sun Jul 23 2023 16:21:45 - 16:49:43
1 CPU in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       41854819.6 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     7356.3 MWIPS (9.9 s, 7 samples)
Execl Throughput                               3447.4 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1006963.3 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          266730.0 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       3027208.7 KBps  (30.0 s, 2 samples)
Pipe Throughput                             1500560.5 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 182697.8 lps   (10.0 s, 7 samples)
Process Creation                              10549.8 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                   8809.0 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   1179.1 lpm   (60.0 s, 2 samples)
System Call Overhead                        1647071.1 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   41854819.6   3586.5
Double-Precision Whetstone                       55.0       7356.3   1337.5
Execl Throughput                                 43.0       3447.4    801.7
File Copy 1024 bufsize 2000 maxblocks          3960.0    1006963.3   2542.8
File Copy 256 bufsize 500 maxblocks            1655.0     266730.0   1611.7
File Copy 4096 bufsize 8000 maxblocks          5800.0    3027208.7   5219.3
Pipe Throughput                               12440.0    1500560.5   1206.2
Pipe-based Context Switching                   4000.0     182697.8    456.7
Process Creation                                126.0      10549.8    837.3
Shell Scripts (1 concurrent)                     42.4       8809.0   2077.6
Shell Scripts (8 concurrent)                      6.0       1179.1   1965.2
System Call Overhead                          15000.0    1647071.1   1098.0
                                                                   ========
System Benchmarks Index Score                                        1534.3
```

## LemonBench

```
 -> System Information

 CPU Model Name:                AMD EPYC 7452 32-Core Processor
 CPU Cache Size:                L1: 64.00 KB / L2: 512.00 KB / L3: 16.00 MB
 CPU Specifications:            1 vCPU
 Virtualization Ready:          Yes (Based on AMD-V, Nested Virtualization Enabled)
 Virtualization Type:           KVM
 Memory Usage:                  481.09 MiB / 1.89 GiB
 Swap Usage:                    [ no swap partition or swap file detected ]
 Disk Usage:                    2.24 GiB / 24.03 GiB
 Boot Disk:                     /dev/sda2
 OS Release:                    Debian GNU/Linux 12 (bookworm) (x86_64)
 Kernel Version:                6.1.0-10-amd64

 -> Network Information

 IPv4-IP Address:               [DE] 104.28.221.34
 IPv4-AS Information:           AS13335 - CLOUDFLARENET
 IPv4-GeoIP Location:           Germany North Rhine-Westphalia Bielefeld
 IPv6-IP Address:               [SE] 2a07:e041:1:7e::1
 IPv6-AS Information:           null - null
 IPv6-GeoIP Location:           Sweden Stockholm County Stockholm

 -> Streaming Service Unlock Test

 Netflix:                       Netflix Only
 HBO Now:                       Yes
 Youtube Premium:               Yes (GeoIP: DE)
 Tiktok Region:                 No
 BBC iPlayer:                   Yes
 NicoNico:                      No
 Princonne Re:dive Japan:       Yes
 Pretty Derby Japan:            No
 Kantai Collection Japan:       No
 Bahamut Anime:                 No
 Bilibili (China Mainland):     No
 Bilibili (China SAR&Taiwan):   No
 Bilibili (China Taiwan):       No
 Steam Price Currency:          EUR

  -> CPU Performance Test (Fast mode, 1-Pass @ 5sec)

 1 Thread(s) Test:              1646.14 Scores (1.00x)

 -> Disk Performance Test (Using FIO, Direct mode, 32 IO-Depth)

 Write Test (4K-Block):         211.86 MB/s (54237 IOPS)
 Read  Test (4K-Block):         526.32 MB/s (134736 IOPS)
 Write Test (128K-Block):       5555.55 MB/s (44444 IOPS)
 Read  Test (128K-Block):       8333.33 MB/s (66666 IOPS)

 -> Network Speedtest Test (Using Ookla Speedtest, Fast Test Mode)

 Node Name                      Download Speed  Upload Speed    Ping Latency    Server Name
 Speedtest Default:             945.74 Mbps     762.14 Mbps     24.00 ms        Schlueter Onlinedienste, Germany Ruethen
 China Unicom Shanghai:         720.87 Mbps     140.68 Mbps     257.17 ms       China Unicom 5G, China ShangHai
 China Telecom Shanghai:        0.00 Mbps       0.00 Mbps       0.00 ms null, null null
 China Mobile Sichuan:          524.43 Mbps     682.83 Mbps     293.21 ms       China Mobile Group Sichuan, China Chengdu

 -> Traceroute Test (Fast Mode)

[+] Traceroute to China Unicom (Beijing, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.37ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 113.209.132.146, 30 hops max, 32 byte packets
1       104.28.0.0 2.33ms *, United States of America, Texas, Dallas
2       162.158.180.1 3.90ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       194.68.123.95 4.17ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
4       80.77.96.32 3.04ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
5       213.206.129.44 13.40ms AS1239, 丹麦, 首都大区, 哥本哈根, sprint.net 
6       213.206.129.58 25.25ms AS1239, 荷兰, 北荷兰省, 阿姆斯特丹, sprint.net 
7       213.206.129.95 30.67ms AS1239, 英国, 英格兰, 伦敦, sprint.net 
8       144.232.0.63 101.49ms AS1239, 美国, 纽约州, 纽约, sprint.net 
9       144.232.25.229 120.46ms AS1239, 美国, 马里兰州, 巴尔的摩, sprint.net 
10      144.232.14.5 110.39ms AS1239, 美国, 华盛顿哥伦比亚特区, 华盛顿, sprint.net 
11      144.232.13.193 138.27ms AS1239, 美国, 弗吉尼亚州, 费尔法克斯, sprint.net 
12      144.232.13.12 136.42ms AS1239, 美国, 佐治亚州, 亚历山大, sprint.net 
13      144.232.22.227 138.64ms AS1239, 美国, 佐治亚州, 亚特兰大, sprint.net 
14      144.232.13.81 174.26ms AS1239, 美国, 加利福尼亚州, 里亚托, sprint.net 
15      144.232.22.153 166.64ms AS1239, 美国, 加利福尼亚州, 斯托克顿, sprint.net 
16      *
17      219.158.16.97 454.19ms AS4837, 中国, 北京市, chinaunicom.cn  联通
18      219.158.16.77 439.87ms AS4837, 中国, 北京市, chinaunicom.cn  联通
19      *
20      124.65.194.18 466.02ms AS4808, 中国, 北京市, chinaunicom.cn  联通
21      61.148.157.122 467.48ms AS4808, 中国, 北京市, chinaunicom.cn  联通
22      *
23      *
24      *
25      *
26      *
27      113.209.132.146 437.26ms AS4808, 中国, 北京市, chinaunicom.cn  联通

[+] Traceroute to China Telecom (Beijing, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.19.29.108 - 1.45ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 45.126.112.33, 30 hops max, 32 byte packets
1       104.28.0.0 2.31ms *, United States of America, Texas, Dallas
2       162.158.180.1 3.79ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 3.39ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.210 3.63ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.143.29 40.78ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
6       62.115.124.117 26.42ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
7       202.97.58.149 132.82ms AS4134, 德国, 黑森州, 美因河畔法兰克福, chinatelecom.com.cn  电信
8       *
9       *
10      *
11      *
12      *
13      *
14      36.112.226.54 300.52ms AS4847, 中国, 北京市, chinatelecom.cn 
15      *
16      *
17      *
18      *
19      45.126.112.33 317.88ms AS4847, 中国, 北京市, chinatelecom.cn 

[+] Traceroute to China Mobile (Beijing, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.19.29.108 - 1.52ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 183.242.65.12, 30 hops max, 32 byte packets
1       104.28.0.0 2.22ms *, United States of America, Texas, Dallas
2       162.158.180.1 10.07ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 3.44ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.248 3.69ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.139.173 11.35ms AS1299, 丹麦, 首都大区, 哥本哈根, arelion.com 
6       80.91.254.91 109.06ms AS1299, 美国, 纽约州, 纽约, arelion.com 
7       62.115.119.229 169.04ms AS1299, 美国, 加利福尼亚州, 圣何塞, arelion.com 
8       *
9       *
10      *
11      221.183.55.106 364.49ms AS9808, 中国, 北京市, chinamobile.com  移动
12      *
13      *
14      221.183.76.78 347.40ms AS9808, 中国, 北京市, chinamobile.com  移动
15      221.179.171.41 367.64ms AS56048, 中国, 北京市, chinamobile.com  移动
16      *
17      *
18      223.70.199.10 362.83ms AS56048, 中国, 北京市, chinamobile.com  移动
19      *
20      *
21      183.242.65.12 365.52ms AS56048, 中国, 北京市, chinamobile.com  移动

[+] Traceroute to China Unicom (Shanghai, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.19.29.108 - 1.47ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 103.116.79.1, 30 hops max, 32 byte packets
1       104.28.0.0 2.25ms *, United States of America, Texas, Dallas
2       162.158.180.1 3.65ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       194.68.123.95 3.57ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
4       80.77.96.32 3.80ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
5       213.206.129.44 13.91ms AS1239, 丹麦, 首都大区, 哥本哈根, sprint.net 
6       213.206.129.58 24.02ms AS1239, 荷兰, 北荷兰省, 阿姆斯特丹, sprint.net 
7       213.206.129.95 30.39ms AS1239, 英国, 英格兰, 伦敦, sprint.net 
8       213.206.129.1 32.64ms AS1239, 英国, 英格兰, 伦敦, sprint.net 
9       144.232.9.109 104.44ms AS1239, 美国, 马萨诸塞州, 斯普林菲尔德, sprint.net 
10      144.232.10.240 129.33ms AS1239, 美国, 俄亥俄州, 阿克伦, sprint.net 
11      144.232.18.5 116.34ms AS1239, 美国, 伊利诺伊州, 芝加哥, sprint.net 
12      144.232.22.73 125.98ms AS1239, 美国, 内布拉斯加州, 奥马哈, sprint.net 
13      144.232.15.165 174.09ms AS1239, 美国, 加利福尼亚州, 奥罗维尔, sprint.net 
14      144.232.15.237 172.09ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
15      144.232.22.176 171.36ms AS1239, 美国, 加利福尼亚州, 圣何塞, sprint.net 
16      144.232.2.100 165.28ms AS1239, 美国, 加利福尼亚州, 圣何塞, sprint.net 
17      144.223.242.26 158.49ms AS1239, 美国, 加利福尼亚州, 帕洛阿尔托 / 圣何塞, sprint.net 
18      219.158.97.181 374.45ms AS4837, 中国, 上海市, chinaunicom.cn  联通
19      219.158.113.142 289.85ms AS4837, 中国, 北京市, chinaunicom.cn  联通
20      *
21      *
22      139.226.214.37 312.51ms AS17621, 中国, 上海市, chinaunicom.cn  联通
23      112.64.252.146 366.37ms AS17621, 中国, 上海市, chinaunicom.cn  联通
24      *
25      103.116.79.1 350.71ms AS17621, 中国, 上海市, chinaunicom.cn  联通

[+] Traceroute to China Telecom (Shanghai, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.35ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 210.5.157.1, 30 hops max, 32 byte packets
1       104.28.0.0 2.26ms *, United States of America, Texas, Dallas
2       162.158.180.1 3.85ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 3.71ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.248 4.11ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.138.105 28.06ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
6       62.115.124.119 27.98ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
7       *
8       202.97.70.141 339.09ms AS4134, 中国, 上海市, chinatelecom.com.cn  电信
9       *
10      *
11      61.152.25.73 366.33ms AS4812, 中国, 上海市, chinatelecom.cn  电信
12      101.95.89.62 363.08ms AS4812, 中国, 上海市, chinatelecom.cn  电信
13      *
14      101.95.91.26 365.82ms AS4812, 中国, 上海市, chinatelecom.cn  电信
15      58.40.245.94 358.33ms AS4812, 中国, 上海市, chinatelecom.cn  电信
16      *
17      *
18      *
19      210.5.157.1 343.18ms AS4812, 中国, 上海市, chinatelecom.cn  电信

[+] Traceroute to China Mobile (Shanghai, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.19.29.108 - 1.47ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 117.144.213.77, 30 hops max, 32 byte packets
1       104.28.0.0 2.43ms *, United States of America, Texas, Dallas
2       162.158.180.1 3.52ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 3.65ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.210 3.80ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.134.94 19.24ms AS1299, 德国, 汉堡州, 汉堡, arelion.com 
6       80.91.249.10 30.74ms AS1299, 英国, 英格兰, 伦敦, arelion.com 
7       62.115.121.27 33.10ms AS1299, 英国, 英格兰, 伦敦, arelion.com 
8       62.115.12.242 43.26ms AS1299, 英国, 英格兰, 伦敦, arelion.com 
9       223.120.15.26 323.25ms AS58453, 中国, 上海市, cmi.chinamobile.com  移动
10      221.183.89.174 249.26ms AS9808, 中国, 上海市, chinamobile.com  移动
11      221.183.89.69 309.13ms AS9808, 中国, 上海市, chinamobile.com  移动
12      *
13      *
14      211.136.190.242 331.80ms AS24400, 中国, 上海市, chinamobile.com  移动
15      *
16      117.144.213.77 321.66ms AS24400, 中国, 上海市, chinamobile.com  移动

[+] Traceroute to China Unicom (Guangzhou, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.8.231 - 1.21ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 210.21.4.130, 30 hops max, 32 byte packets
1       104.28.0.0 2.41ms *, United States of America, Texas, Dallas
2       162.158.180.1 12.00ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       194.68.123.95 3.69ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
4       80.77.96.32 3.40ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
5       213.206.129.44 13.27ms AS1239, 丹麦, 首都大区, 哥本哈根, sprint.net 
6       213.206.129.58 24.94ms AS1239, 荷兰, 北荷兰省, 阿姆斯特丹, sprint.net 
7       213.206.129.95 30.64ms AS1239, 英国, 英格兰, 伦敦, sprint.net 
8       213.206.129.1 31.62ms AS1239, 英国, 英格兰, 伦敦, sprint.net 
9       144.232.9.109 96.17ms AS1239, 美国, 马萨诸塞州, 斯普林菲尔德, sprint.net 
10      144.232.10.240 125.43ms AS1239, 美国, 俄亥俄州, 阿克伦, sprint.net 
11      144.232.18.5 119.52ms AS1239, 美国, 伊利诺伊州, 芝加哥, sprint.net 
12      144.232.22.73 140.43ms AS1239, 美国, 内布拉斯加州, 奥马哈, sprint.net 
13      144.232.15.165 168.60ms AS1239, 美国, 加利福尼亚州, 奥罗维尔, sprint.net 
14      144.232.15.237 163.72ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
15      144.232.22.176 174.70ms AS1239, 美国, 加利福尼亚州, 圣何塞, sprint.net 
16      144.232.2.100 163.41ms AS1239, 美国, 加利福尼亚州, 圣何塞, sprint.net 
17      144.223.242.30 179.74ms AS1239, 美国, 加利福尼亚州, 帕洛阿尔托 / 圣何塞, sprint.net 
18      219.158.97.177 366.19ms AS4837, 中国, 上海市, chinaunicom.cn  联通
19      219.158.6.185 342.51ms AS4837, 中国, 上海市, chinaunicom.cn  联通
20      219.158.7.129 350.74ms AS4837, 中国, 上海市, chinaunicom.cn  联通
21      *
22      120.83.0.166 392.73ms AS17816, 中国, 广东省, 广州市, chinaunicom.cn  联通
23      120.80.170.254 355.71ms AS17622, 中国, 广东省, 广州市, chinaunicom.cn  联通
24      210.21.4.130 383.38ms AS17622, 中国, 广东省, 广州市, chinaunicom.cn  联通

[+] Traceroute to China Telecom (Guangzhou, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.19.28.108 - 1.26ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 113.108.209.1, 30 hops max, 32 byte packets
1       104.28.0.0 2.54ms *, United States of America, Texas, Dallas
2       162.158.180.1 3.66ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 3.69ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.248 3.91ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.138.105 24.98ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
6       62.115.136.219 24.91ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
7       118.85.205.81 106.20ms AS4134, 德国, 黑森州, 美因河畔法兰克福, chinatelecom.com.cn  电信
8       *
9       202.97.12.34 270.47ms AS4134, 中国, 广东省, chinatelecom.com.cn  电信
10      *
11      *
12      *
13      113.108.209.1 290.19ms AS4134, 中国, 广东省, 广州市, chinatelecom.com.cn  电信

[+] Traceroute to China Mobile (Guangzhou, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.25ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 183.232.48.167, 30 hops max, 32 byte packets
1       104.28.0.0 2.24ms *, United States of America, Texas, Dallas
2       162.158.180.1 84.88ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 3.50ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.210 3.88ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.143.29 29.54ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
6       62.115.114.89 29.56ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
7       62.115.47.45 36.83ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
8       223.120.10.241 37.30ms AS58453, 德国, 黑森州, 美因河畔法兰克福, cmi.chinamobile.com  移动
9       *
10      223.120.22.10 306.51ms AS58453, 中国, 广东省, 广州市, cmi.chinamobile.com  移动
11      221.183.55.82 310.95ms AS9808, 中国, 广东省, chinamobile.com  移动
12      221.183.92.21 322.54ms AS9808, 中国, 上海市, chinamobile.com  移动
13      *
14      *
15      *
16      *
17      183.232.48.167 328.55ms AS56040, 中国, 广东省, 广州市, chinamobile.com  移动

[+] Traceroute to China Unicom CUII/AS9929 (Shanghai, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.19.29.108 - 1.43ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 210.13.66.238, 30 hops max, 32 byte packets
1       104.28.0.0 2.12ms *, United States of America, Texas, Dallas
2       162.158.180.1 6.22ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       194.68.128.95 3.64ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
4       80.77.96.32 3.62ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
5       213.206.129.44 14.07ms AS1239, 丹麦, 首都大区, 哥本哈根, sprint.net 
6       213.206.129.58 25.99ms AS1239, 荷兰, 北荷兰省, 阿姆斯特丹, sprint.net 
7       213.206.129.95 31.05ms AS1239, 英国, 英格兰, 伦敦, sprint.net 
8       213.206.129.1 30.51ms AS1239, 英国, 英格兰, 伦敦, sprint.net 
9       144.232.9.109 97.19ms AS1239, 美国, 马萨诸塞州, 斯普林菲尔德, sprint.net 
10      144.232.10.240 113.42ms AS1239, 美国, 俄亥俄州, 阿克伦, sprint.net 
11      144.232.18.5 114.75ms AS1239, 美国, 伊利诺伊州, 芝加哥, sprint.net 
12      144.232.22.73 127.83ms AS1239, 美国, 内布拉斯加州, 奥马哈, sprint.net 
13      144.232.15.165 176.37ms AS1239, 美国, 加利福尼亚州, 奥罗维尔, sprint.net 
14      144.232.15.237 164.70ms AS1239, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, sprint.net 
15      144.232.22.176 170.69ms AS1239, 美国, 加利福尼亚州, 圣何塞, sprint.net 
16      144.232.2.100 171.87ms AS1239, 美国, 加利福尼亚州, 圣何塞, sprint.net 
17      144.223.242.10 248.46ms AS1239, 美国, 加利福尼亚州, 圣何塞, sprint.net 
18      218.105.2.129 249.52ms AS9929, 中国, 广东省, 广州市, chinaunicom.cn  联通 CUII
19      218.105.131.198 307.82ms AS9929, 中国, 上海市, chinaunicom.cn  联通 CUII
20      218.105.2.210 305.26ms AS9929, 中国, 上海市, chinaunicom.cn  联通 CUII
21      210.13.116.82 313.86ms AS9929, 中国, 上海市, chinaunicom.cn  联通 CUII
22      *
23      210.13.64.110 310.26ms AS9929, 中国, 上海市, chinaunicom.cn  联通 CUII
24      210.13.66.237 313.33ms AS9929, 中国, 上海市, chinaunicom.cn  联通 CUII
25      210.13.66.238 318.53ms AS9929, 中国, 上海市, chinaunicom.cn  联通 CUII

[+] Traceroute to China Telecom CN2/AS4812 (Shanghai, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.19.29.108 - 1.56ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 58.32.0.1, 30 hops max, 32 byte packets
1       104.28.0.0 2.28ms *, United States of America, Texas, Dallas
2       162.158.180.1 3.64ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 3.56ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.248 4.02ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.127.22 16.69ms AS1299, 德国, 汉堡州, 汉堡, arelion.com 
6       *
7       62.115.120.239 30.10ms AS1299, 英国, 英格兰, 伦敦, arelion.com 
8       80.239.193.226 49.28ms AS1299, 英国, 英格兰, 伦敦, arelion.com 
9       59.43.250.1 251.54ms *, 中国, 上海市, chinatelecom.cn  电信
10      *
11      59.43.130.205 257.85ms *, 中国, 上海市, chinatelecom.cn  电信
12      61.152.24.186 292.14ms AS4812, 中国, 上海市, chinatelecom.cn  电信
13      *
14      58.32.0.1 253.59ms AS4812, 中国, 上海市, chinatelecom.cn  电信

[+] Traceroute to China Dr.Peng HomeNetwork (Beijing, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.67ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 14.131.128.1, 30 hops max, 32 byte packets
1       104.28.0.0 2.41ms *, United States of America, Texas, Dallas
2       162.158.180.1 4.23ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       *
4       *
5       *
6       *
7       *
8       *
9       *
10      *
11      *
12      *
13      *
14      *
15      *
16      *
17      *
18      *
19      *
20      *
21      *
22      *
23      *
24      *
25      *
26      *
27      *
28      *
29      *
30      *
        *

[+] Traceroute to China Dr.Peng BizNetwork (Beijing, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.44ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 211.167.230.100, 30 hops max, 32 byte packets
1       104.28.0.0 2.76ms *, United States of America, Texas, Dallas
2       162.158.180.1 9.28ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 3.59ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.248 3.54ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.138.105 28.89ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
6       62.115.124.119 28.05ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
7       *
8       219.158.3.253 262.99ms AS4837, 中国, 广东省, chinaunicom.cn  联通
9       219.158.97.30 279.42ms AS4837, 中国, 广东省, chinaunicom.cn  联通
10      219.158.19.65 253.62ms AS4837, 中国, 广东省, chinaunicom.cn  联通
11      219.158.15.37 269.90ms AS4837, 中国, 北京市, chinaunicom.cn  联通
12      125.33.186.14 284.72ms AS4808, 中国, 北京市, chinaunicom.cn  联通
13      123.126.0.174 264.61ms AS4808, 中国, 北京市, chinaunicom.cn  联通
14      61.149.212.242 296.24ms AS4808, 中国, 北京市, chinaunicom.cn  联通
15      *
16      218.241.255.138 263.40ms AS4808, 中国, 北京市, chinaunicom.cn  联通
17      218.241.253.134 273.15ms AS4808, 中国, 北京市, chinaunicom.cn  联通
18      211.167.230.100 280.31ms AS9819, 中国, 北京市, 鹏博士

[+] Traceroute to China CERNET (Beijing, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.19.28.108 - 1.65ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 101.6.6.6, 30 hops max, 32 byte packets
1       104.28.0.0 3.02ms *, United States of America, Texas, Dallas
2       162.158.180.1 14.63ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 3.82ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.248 3.69ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.139.187 3.79ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
6       *
7       130.117.50.225 4.34ms AS174, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cogentco.com 
8       154.54.61.237 18.97ms AS174, 丹麦, 丹麦首都地区, 哥本哈根, cogentco.com 
9       154.54.61.229 16.50ms AS174, 德国, 汉堡州, 汉堡, cogentco.com 
10      154.54.38.209 55.84ms AS174, 荷兰, 北荷兰省, 阿姆斯特丹, cogentco.com 
11      130.117.51.41 138.27ms AS174, 英国, 英格兰, 伦敦, cogentco.com 
12      154.54.42.85 136.10ms AS174, 美国, 新泽西州, 纽瓦克, cogentco.com 
13      154.54.82.245 136.86ms AS174, 美国, 俄亥俄州, 克里夫兰, cogentco.com 
14      154.54.7.129 116.87ms AS174, 美国, 伊利诺伊州, 芝加哥, cogentco.com 
15      154.54.44.169 130.23ms AS174, 美国, 密苏里州, 堪萨斯城, cogentco.com 
16      154.54.31.89 142.91ms AS174, 美国, 科罗拉多州, 丹佛, cogentco.com 
17      154.54.87.29 161.15ms AS174, 美国, 得克萨斯州, 埃尔帕索, cogentco.com 
18      154.54.26.53 165.33ms AS174, 美国, 亚利桑那州, 凤凰城, cogentco.com 
19      154.54.45.162 172.24ms AS174, 美国, 加利福尼亚州, 洛杉矶, cogentco.com 
20      154.54.25.150 168.54ms AS174, 美国, 加利福尼亚州, 洛杉矶, cogentco.com 
21      38.88.196.186 169.80ms AS174, 美国, 加利福尼亚州, 洛杉矶, cogentco.com 
22      101.4.117.169 275.84ms AS4538, 中国, 北京市, cernet.edu.cn  教育网
23      101.4.116.217 274.14ms AS4538, 中国, 北京市, cernet.edu.cn  教育网
24      *
25      101.4.117.81 276.05ms AS4538, 中国, 北京市, cernet.edu.cn  教育网
26      101.4.113.234 289.43ms AS4538, 中国, 北京市, cernet.edu.cn  教育网
27      202.112.38.70 275.26ms AS4538, 中国, 北京市, cernet.edu.cn  教育网
28      118.229.4.78 274.03ms AS4538, 中国, 北京市, cernet.edu.cn  教育网
29      118.229.2.78 275.87ms AS4538, 中国, 北京市, cernet.edu.cn  教育网
30      118.229.9.6 275.07ms AS4538, 中国, 北京市, cernet.edu.cn  教育网
        *

[+] Traceroute to China CSTNET (Beijing, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.29ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 159.226.254.1, 30 hops max, 32 byte packets
1       104.28.0.0 2.45ms *, United States of America, Texas, Dallas
2       162.158.180.1 13.83ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 3.62ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.210 3.77ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.139.181 3.93ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
6       *
7       154.54.36.89 4.48ms AS174, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cogentco.com 
8       154.54.61.241 16.78ms AS174, 丹麦, 丹麦首都地区, 哥本哈根, cogentco.com 
9       154.54.61.221 17.49ms AS174, 德国, 汉堡州, 汉堡, cogentco.com 
10      154.54.38.205 27.02ms AS174, 荷兰, 北荷兰省, 阿姆斯特丹, cogentco.com 
11      130.117.2.142 32.56ms AS174, 法国, 法兰西岛大区, 巴黎, cogentco.com 
12      154.54.72.110 42.33ms AS174, 法国, 普罗旺斯-阿尔卑斯-蓝色海岸大区, 马赛, cogentco.com 
13      154.54.0.42 198.98ms AS174, 中国, 香港, cogentco.com 
14      154.18.4.2 197.18ms AS174, 中国, 香港, cogentco.com 
15      159.226.254.213 198.08ms AS7497, 中国, 香港, cstnet.cn  科技网
16      159.226.254.61 237.63ms AS7497, 中国, 北京市, cstnet.cn  科技网
17      159.226.254.237 236.60ms AS7497, 中国, 香港, cstnet.cn  科技网
18      159.226.254.1 234.69ms AS7497, 中国, 北京市, cstnet.cn  科技网

[+] Traceroute to China RTVB (Beijing, IPv4)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.45ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 211.156.140.17, 30 hops max, 32 byte packets
1       104.28.0.0 2.44ms *, United States of America, Texas, Dallas
2       162.158.180.1 3.58ms AS13335, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cloudflare.com
3       62.115.46.92 4.00ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
4       62.115.125.248 4.01ms AS1299, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, arelion.com 
5       62.115.138.105 28.08ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
6       62.115.114.91 28.34ms AS1299, 德国, 黑森州, 美因河畔法兰克福, arelion.com 
7       118.85.205.81 105.57ms AS4134, 德国, 黑森州, 美因河畔法兰克福, chinatelecom.com.cn  电信
8       *
9       *
10      *
11      *
12      *
13      *
14      60.247.93.254 292.84ms AS4847, 中国, 北京市, chinatelecom.cn  电信
15      211.156.131.93 294.78ms AS7641, 中国, 北京市, cncatv.com 
16      211.156.140.17 309.51ms AS7641, 中国, 北京市, cncatv.com 

[+] Traceroute to China Unicom (Beijing, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.8.231 - 1.52ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 2408:80f0:4100:2005::3, 30 hops max, 32 byte packets
1       2a07:e041::1 1.71ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 0.58ms AS42675, obe.net, obe.net
3       2a07:5cc0:0:1::5f 0.66ms AS3399, obe.net, obe.net
4       2001:668:0:3:ffff:1:0:1b6d 0.87ms AS3257, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, gtt.net
5       *
6       2001:550:0:1000::9a36:2459 2.01ms AS174, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, cogentco.com
7       *
8       *
9       *
10      *
11      *
12      2408:8000:2:8083::1 235.84ms AS4837, 中国, 北京市, chinaunicom.cn 联通
13      *
14      2408:8000:2:804b:: 259.21ms AS4837, 中国, 北京市, chinaunicom.cn 联通
15      2408:8000:1100:3c4::3 286.17ms AS4808, 中国, 北京市, chinaunicom.cn 联通
16      2408:8000:1100:1900::3 291.47ms AS4808, 中国, 北京市, chinaunicom.cn 联通
17      2408:80f0:4100:2006::1 268.30ms AS4808, 中国, 北京市, chinaunicom.cn 联通
18      2408:80f0:4100:2006::b 295.99ms AS4808, 中国, 北京市, chinaunicom.cn 联通
19      *
20      *
21      *
22      *
23      *
24      *
25      *
26      *
27      *
28      *
30      *
        *

[+] Traceroute to China Telecom (Beijing, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.19.29.108 - 1.23ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 2400:da00:2::29, 30 hops max, 32 byte packets
1       2a07:e041::1 0.91ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 3.43ms AS42675, obe.net, obe.net
3       2a07:5cc0:0:1::4b 0.52ms AS3399, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, obe.net
4       2a03:8600:8600::102 20.56ms AS3399, 荷兰, 北荷兰省, 阿姆斯特丹, obe.net
5       2a04:f580:8291:100::1 21.76ms *, 荷兰, 北荷兰省, 阿姆斯特丹, 中国电信
6       240e:0:a::cc:5c08 227.06ms AS4134, chinatelecom.com.cn 电信, chinatelecom.com.cn 电信
7       240e:0:a::c9:40a5 227.78ms AS4134, 中国, 广东省, chinatelecom.com.cn 电信
8       240e::f:3:5901:302 232.43ms AS4134, 中国, 广东省, chinatelecom.com.cn 电信
9       240e:1f:5000:74::3 235.92ms AS58466, 中国, 广东省, 广州市, ofidc.com 电信
10      240e:1f:5000:f007::3 238.30ms AS58466, 中国, 广东省, 广州市, ofidc.com 电信
11      240e:1f:5800:2a::3 234.06ms AS58466, 中国, 广东省, 广州市, ofidc.com 电信
12      240e:97c:24:4000:: 232.35ms AS58466, 中国, 广东省, 广州市, ofidc.com 电信
13      *
14      *
15      *
16      *
17      *
18      *
19      *
20      *
21      *
22      *
23      *
24      *
25      *
26      *
27      *
28      *
30      *
        *

[+] Traceroute to China Mobile (Beijing, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.53ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 2409:8089:1020:50ff:1000::fd01, 30 hops max, 32 byte packets
1       2a07:e041::1 3.47ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 0.46ms AS42675, obe.net, obe.net
3       2a07:5cc0:0:1::4b 0.49ms AS3399, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, obe.net
4       *
5       2001:1900:2::3:167 32.83ms AS3356, 德国, 黑森州, 美因河畔法兰克福, level3.com
6       2001:1900:5:3::ce 49.06ms AS3356, 德国, 黑森州, 美因河畔法兰克福, level3.com
7       2402:4f00:2000:100::71e 40.03ms AS58453, 德国, 黑森州, 美因河畔法兰克福, cmi.chinamobile.com 移动
8       2402:4f00:2000:100::6aa 271.97ms AS58453, 中国, 香港, cmi.chinamobile.com
9       2409:8080:0:4:2f5:294:1:1 273.63ms AS9808, 中国, 上海市, chinamobile.com 移动
10      2409:8080:0:4:2c6:2f6:2:1 266.02ms AS9808, 中国, 上海市, chinamobile.com 移动
11      2409:8080:0:1:204:2c6:: 265.05ms AS9808, 中国, 上海市, chinamobile.com 移动
12      2409:8080:1:2:104:204:2:0 292.80ms AS9808, 中国, 上海市, chinamobile.com 移动
13      2409:8080:1:2:104:104:0:1 288.43ms AS9808, 中国, 北京市, chinamobile.com 移动
15      2409:8089:1020:50ff:1000::fd01 300.50ms AS9808, 中国, 北京市, chinamobile.com 移动

[+] Traceroute to China Unicom (Shanghai, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.51ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 2408:8000:9000:20e6::b7, 30 hops max, 32 byte packets
1       2a07:e041::1 7.75ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 0.56ms AS42675, obe.net, obe.net
3       2a07:5cc0:0:1::5f 0.57ms AS3399, obe.net, obe.net
4       2001:668:0:3:ffff:1:0:1b6d 5.41ms AS3257, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, gtt.net
5       *
6       *
7       *
8       *
9       *
10      2001:550:0:1000::9a36:38be 29.01ms AS174, 德国, 黑森州, 美因河畔法兰克福, cogentco.com
11      *
12      2001:978:2:42::12e:2 250.68ms AS174, 德国, 黑森州, 美因河畔法兰克福, cogentco.com
13      *
14      *
15      *
17      2408:8000:9000:20e6::b7 256.29ms AS17621, 中国, 上海市, chinaunicom.cn 联通

[+] Traceroute to China Telecom (Shanghai, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.8.231 - 1.47ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 240e:18:10:a01::1, 30 hops max, 32 byte packets
1       2a07:e041::1 61.86ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 0.44ms AS42675, obe.net, obe.net
3       2a07:5cc0:0:1::4b 0.52ms AS3399, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, obe.net
4       2a03:8600:8600::102 20.70ms AS3399, 荷兰, 北荷兰省, 阿姆斯特丹, obe.net
5       2a04:f580:8291:100::1 21.41ms *, 荷兰, 北荷兰省, 阿姆斯特丹, 中国电信
6       240e:0:a::cc:2b0c 267.26ms AS4134, 中国, 上海市, chinatelecom.com.cn 电信
7       *
8       240e::f:2:0:102 273.24ms AS4134, 中国, 上海市, chinatelecom.com.cn 电信
9       240e:18:10:430e::89 272.44ms AS4811, 中国, 上海市, chinatelecom.cn 电信
10      *
11      *
12      *
13      *
14      *
15      *
16      *
17      *
18      *
19      *
20      *
21      *
22      *
23      *
24      *
25      *
26      *
27      *
28      *
30      *
        *

[+] Traceroute to China Mobile (Shanghai, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.49ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 2409:801e:5c03:2000::207, 30 hops max, 32 byte packets
1       2a07:e041::1 5.90ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 0.49ms AS42675, obe.net, obe.net
3       2a07:5cc0:0:1::4b 0.52ms AS3399, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, obe.net
4       2001:1900:5:2:2::45fd 0.95ms AS3356, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, level3.com
5       2001:1900:2::3:167 65.36ms AS3356, 德国, 黑森州, 美因河畔法兰克福, level3.com
6       2001:1900:5:3::ce 32.09ms AS3356, 德国, 黑森州, 美因河畔法兰克福, level3.com
7       2402:4f00:2000:100::71e 40.07ms AS58453, 德国, 黑森州, 美因河畔法兰克福, cmi.chinamobile.com 移动
8       2402:4f00:2000:100::69e 271.89ms AS58453, 中国, 香港, cmi.chinamobile.com
9       2409:8080:0:4:2f5:294:1:1 273.53ms AS9808, 中国, 上海市, chinamobile.com 移动
10      2409:8080:0:4:2c6:2f6:2:1 265.99ms AS9808, 中国, 上海市, chinamobile.com 移动
11      2409:8080:0:1:206:2c6:: 274.88ms AS9808, 中国, 上海市, chinamobile.com 移动
12      2409:8080:0:2:206:276:0:1 267.09ms AS9808, 中国, 上海市, chinamobile.com 移动
13      2409:801e:f0:1::55b 276.03ms AS24400, 中国, 上海市, chinamobile.com 移动
14      2409:801e:5c01:2000::31 269.39ms AS24400, 中国, 上海市, chinamobile.com 移动
16      2409:801e:5c03:2000::207 267.84ms AS24400, 中国, 上海市, chinamobile.com 移动

[+] Traceroute to China Unicom (Guangzhou, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.19.29.108 - 1.25ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 2408:8001:3011:310::3, 30 hops max, 32 byte packets
1       2a07:e041::1 10.89ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 0.58ms AS42675, obe.net, obe.net
3       2a07:5cc0:0:1::5f 0.59ms AS3399, obe.net, obe.net
4       2001:668:0:3:ffff:1:0:1b6d 0.93ms AS3257, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, gtt.net
5       *
6       *
7       *
8       *
9       *
10      *
11      2001:550:0:1000::9a19:2a6 29.54ms AS174, 德国, 黑森州, 美因河畔法兰克福, cogentco.com
12      2001:978:2:42::e1:2 237.10ms AS174, 德国, 黑森州, 美因河畔法兰克福, cogentco.com
13      *
14      2408:8000:2:797::1 269.33ms AS4837, 中国, 广东省, chinaunicom.cn 联通
15      *
16      *
17      *
18      *
19      *
20      *
21      *
22      *
23      *
24      *
25      *
26      *
27      *
28      *
30      *
        *

[+] Traceroute to China Telecom (Guangzhou, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.46ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 240e:ff:e02c:1:21::, 30 hops max, 32 byte packets
1       2a07:e041::1 4.35ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 0.46ms AS42675, obe.net, obe.net
3       2a07:5cc0:0:1::4b 0.59ms AS3399, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, obe.net
4       2a03:8600:8600::102 20.65ms AS3399, 荷兰, 北荷兰省, 阿姆斯特丹, obe.net
5       2a04:f580:8291:100::1 24.20ms *, 荷兰, 北荷兰省, 阿姆斯特丹, 中国电信
6       240e:0:a::cc:3a0c 230.18ms AS4134, 中国, 广东省, chinatelecom.com.cn 电信
7       240e:0:a::c9:40a5 230.70ms AS4134, 中国, 广东省, chinatelecom.com.cn 电信
8       *
9       240e:1f:5000:5d::3 235.91ms AS58466, 中国, 广东省, 广州市, ofidc.com 电信
10      *
11      *
12      *
13      *
14      *
15      *
16      *
17      *
18      *
19      *
20      *
21      *
22      *
23      *
24      *
25      *
26      *
27      *
28      *
30      *
        *

[+] Traceroute to China Mobile (Guangzhou, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.8.231 - 1.36ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 2409:8057:5c00:30::6, 30 hops max, 32 byte packets
1       2a07:e041::1 9.31ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 0.58ms AS42675, obe.net, obe.net
3       2a07:5cc0:0:1::4b 0.38ms AS3399, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, obe.net
4       2001:1900:5:2:2::45fd 3.89ms AS3356, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, level3.com
5       2001:1900:2::3:167 32.17ms AS3356, 德国, 黑森州, 美因河畔法兰克福, level3.com
6       2001:1900:5:3::ce 32.25ms AS3356, 德国, 黑森州, 美因河畔法兰克福, level3.com
7       2402:4f00:2000:100::c9 38.70ms AS58453, 德国, 黑森州, 美茵河畔法兰克福, cmi.chinamobile.com 移动
8       2402:4f00:2000:100::516 285.40ms AS58453, 中国, 香港, cmi.chinamobile.com 移动
9       2409:8080:0:4:1f1:193:1:0 252.94ms AS9808, 中国, 北京市, chinamobile.com 移动
10      2409:8080:0:1:1c1:1f1:1:0 228.92ms AS9808, 中国, 北京市, chinamobile.com 移动
11      2409:8080:0:1:105:1c1:: 268.44ms AS9808, 中国, 北京市, chinamobile.com 移动
12      2409:8080:0:1:106:305:0:1 293.88ms AS9808, 中国, 广东省, chinamobile.com 移动
13      *
14      2409:8055:0:1318:: 306.79ms AS56040, 中国, 广东省, 广州市, chinamobile.com 移动
15      2409:8055:1:b301:: 285.26ms AS56040, 中国, 广东省, chinamobile.com 移动
16      2409:8055:5c00:0:4c30::1 300.93ms AS56040, 中国, 广东省, chinamobile.com 移动
17      2409:8055:5c00:0:4c00::5 317.67ms AS56040, 中国, 广东省, chinamobile.com 移动
18      *
19      *
21      2409:8057:5c00:30::6 343.73ms AS56040, 中国, 广东省, chinamobile.com 移动

[+] Traceroute to China CERNET2 (Beijing, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.59ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 2001:da8:a0:1001::1, 30 hops max, 32 byte packets
1       2a07:e041::1 5.59ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 0.44ms AS42675, obe.net, obe.net
3       *
4       *
5       *
6       *
7       2001:7fa:0:1::ca28:a1be 247.23ms *, 中国, 香港, hkix.net
8       2001:252:0:10c::1 237.07ms AS23911, 中国, 北京市, 海淀区清华园李兆基科技大楼, cernet.edu.cn 教育网
9       *
10      *
11      *
12      *
13      *
14      *
15      *
16      *
17      *
18      *
19      *
20      *
21      *
22      *
23      *
24      *
25      *
26      *
27      *
28      *
30      *
        *

[+] Traceroute to China CSTNET (Beijing, IPv6)(ICMP Mode, Max 30 Hops)
NextTrace v1.1.2 2023-02-20T05:07:06Z 88e69f7
[NextTrace API] prefered API IP - 104.26.9.231 - 1.28ms
IP Geo Data Provider: LeoMoeAPI
traceroute to 2400:dd00:0:37::213, 30 hops max, 32 byte packets
1       2a07:e041::1 11.35ms AS206075, 瑞典, 斯德哥尔摩省, 斯德哥尔摩
2       2a0c:dd40:0:2:: 0.59ms AS42675, obe.net, obe.net
3       2001:7f8:3e:0:a500:0:6939:1 1.31ms AS6939, 瑞典, 斯德哥尔摩省, 斯德哥尔摩, he.net
4       *
5       *
6       *
7       *
8       2001:7fa:0:1::ca28:a1be 237.21ms *, 中国, 香港, hkix.net
9       2001:252:0:10a::1 239.53ms AS23911, 中国, 北京市, 海淀区清华园李兆基科技大楼, cernet.edu.cn 教育网
10      *
12      2400:dd00:0:37::213 296.33ms AS7497, cstnet.cn 科技网, cstnet.cn 科技网


Generated by LemonBench v3 on 2023-07-23T15:07:45Z Version 2023.06.22-Stable
```
