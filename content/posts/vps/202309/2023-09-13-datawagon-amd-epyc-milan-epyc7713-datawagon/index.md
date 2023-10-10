---
title: "DATAWAGON AMD Epyc Milan  (Epyc7713)  测试"
date: "2023-09-13"
categories: 
  - "vps"
  - "performance"
  - "usa"
---

> ## 套餐
> 
> **_Provider :_ DATAWAGON  
> _Type/Plan : DW-16G_  
> _Processor :_ AMD Epyc Milan Processors (Epyc 7713)  
> _Num of Core : 8 Cores_  
> _Memory : 16 GB_  
> _Storage : 80 GB NVMe_  
> _Bandwidth : 10T @ 1 Gbps IN | 1 Gbps OUT_  
> _Location :_ New York  
> _Price :_ $10 /month**

## 测评

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 22 minutes
Processor  : AMD EPYC 7713 64-Core Processor
CPU cores  : 8 @ 1999.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 15.6 GiB
Swap       : 1023.0 MiB
Disk       : 77.6 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-23-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : DataWagon LLC
ASN        : AS27176 DataWagon LLC
Host       : DataWagon LLC
Location   : New York, New York (NY)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 404.01 MB/s (101.0k) | 3.80 GB/s    (59.4k)
Write      | 405.07 MB/s (101.2k) | 3.82 GB/s    (59.7k)
Total      | 809.08 MB/s (202.2k) | 7.62 GB/s   (119.1k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.32 GB/s     (8.4k) | 4.24 GB/s     (4.1k)
Write      | 4.55 GB/s     (8.9k) | 4.52 GB/s     (4.4k)
Total      | 8.88 GB/s    (17.3k) | 8.77 GB/s     (8.5k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 47.5 Mbits/sec  | 60.8 Mbits/sec  | 140 ms         
Scaleway        | Paris, FR (10G)           | busy            | 449 Mbits/sec   | 87.6 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 146 ms         
Uztelecom       | Tashkent, UZ (10G)        | 305 Mbits/sec   | 302 Mbits/sec   | 231 ms         
Clouvider       | NYC, NY, US (10G)         | 391 Mbits/sec   | 359 Mbits/sec   | 75.6 ms        
Clouvider       | Dallas, TX, US (10G)      | 121 Mbits/sec   | 202 Mbits/sec   | 113 ms         
Clouvider       | Los Angeles, CA, US (10G) | 61.7 Mbits/sec  | 95.6 Mbits/sec  | 137 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 19.7 Mbits/sec  | 36.4 Mbits/sec  | 140 ms         
Scaleway        | Paris, FR (10G)           | 210 Mbits/sec   | 151 Mbits/sec   | 151 ms         
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 146 ms         
Uztelecom       | Tashkent, UZ (10G)        | 94.5 Mbits/sec  | 244 Mbits/sec   | 231 ms         
Clouvider       | NYC, NY, US (10G)         | 42.5 Mbits/sec  | 53.8 Mbits/sec  | 75.2 ms        
Clouvider       | Dallas, TX, US (10G)      | 26.6 Mbits/sec  | 52.7 Mbits/sec  | 113 ms         
Clouvider       | Los Angeles, CA, US (10G) | 20.0 Mbits/sec  | 34.1 Mbits/sec  | 137 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1481                          
Multi Core      | 8042                          
Full Test       | https://browser.geekbench.com/v6/cpu/2587468

YABS completed in 11 min 49 sec
```

### Benchy 测试

```

Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Debian GNU/Linux 11 (bullseye)     Model       : AMD EPYC 7713 64-Core Processor
Location   : United States                      Core        : 8 @ 1999.998 MHz
Kernel     : 5.10.0-23-amd64                    AES-NI      : ✔ Enabled
Uptime     : 0 days, 0 hrs, 1 mins, 17 secs     VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 1023.0 MiB

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 77.6 GiB                           ASN         : AS27176   
Disk Usage : 1.5 GiB (2% Used)                  ISP         : DataWagon LLC
Mem        : 15.6 GiB                           IPv4        : ✔ Enabled
Mem Usage  : 0.1 GiB (1% Used)                  IPv6        : ✔ Enabled

Disk Performance Check (ext4 on /dev/vda1) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 453.80 MB/s | 455.00 MB/s | 908.80 MB/s | 116.2k | 116.5k | 232.7k |
| 64k  | 3.85 GB/s   | 3.87 GB/s   | 7.72 GB/s   | 63.1k  | 63.4k  | 126.5k |
| 512k | 4.32 GB/s   | 4.55 GB/s   | 8.88 GB/s   | 8.9k   | 9.3k   | 18.2k  |
| 1m   | 5.45 GB/s   | 5.81 GB/s   | 11.26 GB/s  | 5.6k   | 6.0k   | 11.5k  |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |  949.5 Mb/s  |        busy  |   98.5 ms |
|       | Uztelecom   | Tashkent, UZ    |  263.9 Mb/s  |  311.4 Mb/s  |  231.0 ms |
|       | Novogara    | Amsterdam, NL   |  404.4 Mb/s  |  298.6 Mb/s  |  148.0 ms |
|       | FiberBy     | Copenhagen, DK  |  306.6 Mb/s  |  446.7 Mb/s  |  153.0 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |  402.0 Mb/s  |  267.0 Mb/s  |   98.5 ms |
|       | Uztelecom   | Tashkent, UZ    |  130.2 Mb/s  |  276.8 Mb/s  |  231.0 ms |
|       | Novogara    | Amsterdam, NL   |   20.7 Mb/s  |  190.2 Mb/s  |  147.9 ms |
|       | FiberBy     | Copenhagen, DK  |   88.3 Mb/s  |  187.9 Mb/s  |  153.1 ms |
+---------------------------------------------------------------------------------+

+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 1515                     |
| Multi Core         | 8185                     |
+-----------------------------------------------+
| https://browser.geekbench.com/v6/cpu/2587271  |
+-----------------------------------------------+
| Benchy time spent  | 10 Minutes 0 Seconds     |
+-----------------------------------------------+
| Benchy result      | http://sprunge.us/tnR4WM |
+-----------------------------------------------+
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7713 64-Core Processor
 CPU 核心数        : 8
 CPU 频率          : 1999.998 MHz
 CPU 缓存          : L1: 1.00 MB / L2: 4.00 MB / L3: 16.00 MB
 硬盘空间          : 1.49 GiB / 77.64 GiB
 启动盘路径        : /dev/vda1
 内存              : 155.93 MiB / 15.52 GiB
 Swap              : 0 KiB / 1023.00 MiB
 系统在线时间      : 0 days, 0 hour 15 min
 负载              : 0.24, 0.41, 0.28
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS27176 DataWagon LLC
 IPV4 位置         : Buffalo / New York / US
 IPV6 ASN          : AS27176 Datawagon LLC
 IPV6 位置         : Rye / US-NY
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           3511 Scores
 8 线程测试(多核)得分:          27997 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          40919.23 MB/s
 单线程写测试:          21623.90 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         87.7 MB/s (21.41 IOPS, 1.20s))          85.8 MB/s (20943 IOPS, 1.22s)
 1GB-1M Block           1.3 GB/s (1217 IOPS, 0.82s)             2.2 GB/s (2060 IOPS, 0.49s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 401.91 MB/s (100.4k) | 3.91 GB/s    (61.2k)
Write      | 402.97 MB/s (100.7k) | 3.93 GB/s    (61.5k)
Total      | 804.89 MB/s (201.2k) | 7.85 GB/s   (122.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.16 GB/s     (8.1k) | 5.25 GB/s     (5.1k)
Write      | 4.39 GB/s     (8.5k) | 5.60 GB/s     (5.4k)
Total      | 8.55 GB/s    (16.7k) | 10.86 GB/s   (10.6k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS15S45)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: LGA(LGA25S82)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：美国
[IPv6]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
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
 YouTube CDN:                           Amsterdam 
 Netflix Preferred CDN:                 Chicago, IL  
 Spotify Registration:                  No
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           New York, NY 
 Netflix Preferred CDN:                 New York, NY  
 Spotify Registration:                  No
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
欺诈分数(越低越好): 69②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  business⑨  
  公司类型(company_type):hosting①  hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes② ⑥   No⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ② ⑥ ⑦ ⑧ ⑨ 
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
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测88 ③
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
  qq邮箱: Yes
------以下为IPV6检测------
欺诈分数(越低越好): 69②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: US 城市: Buffalo 服务商: AS27176 DataWagon LLC
北京电信 219.141.136.12  电信163 [普通线路]           
北京联通 202.106.50.1    联通4837[普通线路]           
北京移动 221.179.155.161 移动CMI [普通线路]           
上海电信 202.96.209.133  电信163 [普通线路]           
上海联通 210.22.97.1     测试超时
上海移动 211.136.112.200 移动CMI [普通线路]           
广州电信 58.60.188.222   电信163 [普通线路]           
广州联通 210.21.196.6    测试超时
广州移动 120.196.165.24  移动CMI [普通线路]           
成都电信 61.139.2.69     电信163 [普通线路]           
成都联通 119.6.6.6       联通4837[普通线路]           
成都移动 211.137.96.205  移动CMI [普通线路]           
2023/09/13 05:15:08 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.35 ms         * RFC1918
0.75 ms         AS36352 美国 纽约州 水牛城 virmach.com
0.44 ms         * RFC1918
73.39 ms        * RFC1918
0.53 ms         AS1299 [ARELION-NET] 美国 纽约州 水牛城 arelion.com
10.36 ms        AS1299 [ARELION-NET] 美国 纽约州 纽约 arelion.com
9.92 ms         AS1299 [ARELION-NET] 美国 纽约州 纽约 arelion.com
17.55 ms        AS4134 [CHINANET-US] 美国 新泽西州 纽瓦克 CT-POP chinatelecom.com.cn 电信
73.05 ms        AS4134 [CHINANET-BB] 美国 加利福尼亚州 洛杉矶 上海 → 洛杉矶 chinatelecom.com.cn 电信
215.36 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
227.79 ms       AS134774 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.cn 电信
234.52 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
5.70 ms         * RFC1918
0.91 ms         AS36352 美国 纽约州 水牛城 virmach.com
0.35 ms         * RFC1918
0.53 ms         * RFC1918
0.55 ms         AS1299 [ARELION-NET] 美国 纽约州 水牛城 arelion.com
10.79 ms        AS1299 [ARELION-NET] 美国 纽约州 纽约 arelion.com
17.16 ms        AS1299 [ARELION-NET] 美国 纽约州 纽约 arelion.com
71.47 ms        AS1299 [ARELION-NET] 美国 加利福尼亚州 洛杉矶 arelion.com
广州移动 120.196.165.24
0.38 ms         * RFC1918
0.70 ms         AS36352 [CC-10] 美国 纽约州 水牛城 virmach.com
0.46 ms         * RFC1918
1.63 ms         * RFC1918
0.57 ms         AS1299 [ARELION-NET] 美国 纽约州 水牛城 arelion.com
10.42 ms        AS1299 [ARELION-NET] 美国 纽约州 纽约 arelion.com
79.00 ms        AS1299 [ARELION-NET] 美国 加利福尼亚州 圣何塞 arelion.com
70.11 ms        AS1299 [ARELION-NET] 美国 加利福尼亚州 圣何塞 Telia-CMI-Peer arelion.com
70.15 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 圣何塞 cmi.chinamobile.com 移动
229.49 ms       AS58453 [CMI-INT] 中国 香港 cmi.chinamobile.com 移动
229.16 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
229.23 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
230.16 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
232.83 ms       AS9808 [CMNET] 中国 海南省 海口市 chinamobile.com 移动
232.83 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    949.21 Mbps     782.44 Mbps     11.45    0.0%
洛杉矶           428.46 Mbps     966.22 Mbps     71.43    0.0%
法兰克福         241.05 Mbps     852.55 Mbps     153.77   0.0%
联通沈阳         15.14 Mbps      168.44 Mbps     264.95   3.0%
联通WuXi         6.01 Mbps       8.61 Mbps       239.39   0.0%
电信Zhenjiang5G  181.20 Mbps     635.47 Mbps     205.54   NULL
电信Nanjing5G    162.33 Mbps     814.35 Mbps     207.38   0.0%
移动Chengdu      213.00 Mbps     1063.67 Mbps    265.73   0.0%
------------------------------------------------------------------------
 总共花费      : 6 分 32 秒
 时间          : Wed Sep 13 05:20:19 EDT 2023
------------------------------------------------------------------------
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD EPYC 7713 64-Core Processor (x86_64)
8 cores @ 1999 MHz  |  15.6 GiB RAM
Number of Processes: 8  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          16210
  Integer Math                     40053 Million Operations/s
  Floating Point Math              32306 Million Operations/s
  Prime Numbers                    126 Million Primes/s
  Sorting                          23779 Thousand Strings/s
  Encryption                       8704 MB/s
  Compression                      172180 KB/s
  CPU Single Threaded              2268 Million Operations/s
  Physics                          2256 Frames/s
  Extended Instructions (SSE)      14890 Million Matrices/s

Memory Mark:                       2424
  Database Operations              6530 Thousand Operations/s
  Memory Read Cached               22364 MB/s
  Memory Read Uncached             16966 MB/s
  Memory Write                     17208 MB/s
  Available RAM                    15581 Megabytes
  Memory Latency                   72 Nanoseconds
  Memory Threaded                  98063 MB/s
--------------------------------------------------------------------------
```

### Speedtest

```

   Speedtest by Ookla

      Server: Spectrum - New York, NY (id: 16976)
         ISP: DataWagon LLC
Idle Latency:    11.19 ms   (jitter: 0.20ms, low: 11.13ms, high: 11.51ms)
    Download:   956.02 Mbps (data used: 972.3 MB)                                                   
                 11.77 ms   (jitter: 3.24ms, low: 11.14ms, high: 246.59ms)
      Upload:   943.07 Mbps (data used: 890.4 MB)                                                   
                 24.63 ms   (jitter: 0.90ms, low: 11.37ms, high: 27.22ms)
 Packet Loss:     0.0%
  Result URL: https://www.speedtest.net/result/c/f6fe394b-5d46-4f82-bdb9-1cc20691032d
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-76-1024x359.png)

### Network

```
---------------------------- network-speed.xyz ----------------------------
      A simple script to test network performance using speedtest-cli      
---------------------------------------------------------------------------
 Version            : v2023.09.04
 Global Speedtest   : wget -qO- network-speed.xyz | bash
 Region Speedtest   : wget -qO- network-speed.xyz | bash -s -- -r <region>
---------------------------------------------------------------------------
 Basic System Info
---------------------------------------------------------------------------
 CPU Model          : AMD EPYC 7713 64-Core Processor
 CPU Cores          : 8 @ 1999.998 MHz
 CPU Cache          : 512 KB
 AES-NI             : ✔ Enabled
 VM-x/AMD-V         : ✔ Enabled
 Total Disk         : 77.6 GB (1.5 GB Used)
 Total RAM          : 15.3 GB (125.6 MB Used)
 Total Swap         : 1023.0 MB (0 Used)
 System uptime      : 0 days, 0 hour 43 min
 Load average       : 0.25, 1.19, 0.87
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-23-amd64
 Virtualization     : KVM
---------------------------------------------------------------------------
 Basic Network Info
---------------------------------------------------------------------------
 Primary Network    : IPv6
 ISP                : DataWagon LLC
 ASN                : AS27176 DataWagon LLC
 Host               : DataWagon LLC
 Location           : New York, New York-NY, United States
---------------------------------------------------------------------------
 Speedtest.net (Region: GLOBAL)
---------------------------------------------------------------------------
 Location         Latency     Loss    DL Speed       UP Speed       Server      

 ISP: DataWagon LLC 

 Nearest          11.40 ms    0.0%    942.14 Mbps    941.36 Mbps    Windstream - New York, NY 

 Kochi, IN        329.31 ms   0.0%    632.26 Mbps    141.86 Mbps    Asianet Broadband - Cochin 
 Bangalore, IN    282.00 ms   0.0%    543.04 Mbps    149.07 Mbps    Bharti Airtel Ltd - Bangalore 
 Chennai, IN      FAILED                                                        
 Mumbai, IN       FAILED                                                        
 Delhi, IN        326.61 ms   0.0%    566.97 Mbps    142.14 Mbps    Tata Teleservices Ltd - New Delhi 

 Seattle, US      128.69 ms   0.0%    941.28 Mbps    290.01 Mbps    Ziply Fiber - Seattle, WA 
 Los Angeles, US  133.32 ms   0.0%    935.06 Mbps    217.80 Mbps    ReliableSite Hosting - Los Angeles, CA 
 Dallas, US       110.37 ms   0.0%    909.17 Mbps    293.88 Mbps    Hivelocity - Dallas, TX 
 Miami, US        46.46 ms    0.0%    916.12 Mbps    479.38 Mbps    AT&T - Miami, FL 
 New York, US     18.54 ms    0.0%    961.45 Mbps    927.50 Mbps    GSL Networks - New York, NY 
 Toronto, CA      86.67 ms    0.0%    945.20 Mbps    387.09 Mbps    Rogers - Toronto, ON 

 London, UK       139.91 ms   0.0%    985.45 Mbps    192.54 Mbps    VeloxServ Communications - London 
 Amsterdam, NL    86.68 ms    0.0%    986.00 Mbps    326.55 Mbps    31173 Services AB - Amsterdam 
 Paris, FR        101.09 ms   N/A     996.68 Mbps    299.84 Mbps    Axione - Paris 
 Frankfurt, DE    151.38 ms   0.0%    944.10 Mbps    251.13 Mbps    23M GmbH - Frankfurt am Main 
 Warsaw, PL       165.68 ms   0.0%    683.70 Mbps    223.79 Mbps    UPC Polska - Warszawa 
 Bucharest, RO    119.78 ms   0.0%    943.67 Mbps    222.18 Mbps    Vodafone Romania Fixed – Bucharest - Bucharest 

 Jeddah, SA       212.00 ms   0.0%    766.54 Mbps    233.63 Mbps    Saudi Telecom Company 
 Dubai, AE        209.59 ms   0.0%    863.00 Mbps    204.45 Mbps    du - Dubai  
 Fujairah, AE     FAILED                                                        

 Tokyo, JP        FAILED                                                        
 Shanghai, CU-CN  FAILED                                                        
 Nanjing, CT-CN   FAILED                                                        
 Hong Kong, CN    FAILED                                                        
 Singapore, SG    FAILED                                                        
 Jakarta, ID      FAILED                                                        
---------------------------------------------------------------------------
 Avg DL Speed       : 858.99 Mbps
 Avg UL Speed       : 329.12 Mbps

 Total DL Data      : 21.66 GB
 Total UL Data      : 6.91 GB
 Total Data         : 28.57 GB
---------------------------------------------------------------------------
 Duration           : 9 min 21 sec
 System Time        : 13/09/2023 - 05:50:43 EDT
 Total Script Runs  : 23106
---------------------------------------------------------------------------
 Result             : https://result.network-speed.xyz/r/1694598644_P15BJ5_GLOBAL.txt
---------------------------------------------------------------------------
```

## 9.28

```
Basic System Information:
---------------------------------
Uptime     : 3 days, 13 hours, 28 minutes
Processor  : AMD EPYC 7713 64-Core Processor
CPU cores  : 8 @ 1999.999 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 15.6 GiB
Swap       : 1023.0 MiB
Disk       : 77.6 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-25-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : DataWagon LLC
ASN        : AS27176 DataWagon LLC
Host       : DataWagon LLC
Location   : New York, New York (NY)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 314.00 MB/s  (78.5k) | 3.61 GB/s    (56.4k)
Write      | 314.82 MB/s  (78.7k) | 3.63 GB/s    (56.7k)
Total      | 628.83 MB/s (157.2k) | 7.24 GB/s   (113.1k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 5.04 GB/s     (9.8k) | 3.00 GB/s     (2.9k)
Write      | 5.31 GB/s    (10.3k) | 3.20 GB/s     (3.1k)
Total      | 10.35 GB/s   (20.2k) | 6.20 GB/s     (6.0k)

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1414                          
Multi Core      | 7029                          
Full Test       | https://browser.geekbench.com/v6/cpu/2810128
```

### 10.8日

```
Basic System Information:
---------------------------------
Uptime     : 13 days, 6 hours, 41 minutes
Processor  : AMD EPYC 7713 64-Core Processor
CPU cores  : 8 @ 1999.999 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 15.6 GiB
Swap       : 1023.0 MiB
Disk       : 77.6 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-25-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : DataWagon LLC
ASN        : AS27176 DataWagon LLC
Host       : DataWagon LLC
Location   : New York, New York (NY)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 273.27 MB/s  (68.3k) | 2.80 GB/s    (43.8k)
Write      | 273.99 MB/s  (68.4k) | 2.81 GB/s    (44.0k)
Total      | 547.27 MB/s (136.8k) | 5.62 GB/s    (87.8k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.85 GB/s     (5.5k) | 6.24 GB/s     (6.0k)
Write      | 3.00 GB/s     (5.8k) | 6.66 GB/s     (6.5k)
Total      | 5.85 GB/s    (11.4k) | 12.90 GB/s   (12.6k)

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1250                          
Multi Core      | 5357                          
Full Test       | https://browser.geekbench.com/v6/cpu/2974161

YABS completed in 7 min 3 sec
```
