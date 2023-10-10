---
title: "OVH 8 TB NVMe - 128 GB RAM - SPECIAL"
date: "2023-07-18"
categories: 
  - "vps"
  - "eu"
---

## 套餐配置

16 vCores (EPYC 2nd Gen / Xeon 2nd Scalable)  
128 GB RAM (ECC)  
8 TB NVMe SSD  
50 Gbit/s. Unmetered (Upload capped on 3 Gbit/s)

## VPS测试

### CPU

```
root@Azusa:~# lscpu
Architecture:            x86_64
  CPU op-mode(s):        32-bit, 64-bit
  Address sizes:         48 bits physical, 48 bits virtual
  Byte Order:            Little Endian
CPU(s):                  16
  On-line CPU(s) list:   0-15
Vendor ID:               AuthenticAMD
  BIOS Vendor ID:        QEMU
  Model name:            AMD EPYC 7402 24-Core Processor
    BIOS Model name:     pc-i440fx-7.2  CPU @ 2.0GHz
    BIOS CPU family:     1
    CPU family:          23
    Model:               49
    Thread(s) per core:  1
    Core(s) per socket:  1
    Socket(s):           16
    Stepping:            0
    BogoMIPS:            5589.49

Virtualization features: 
  Virtualization:        AMD-V
  Hypervisor vendor:     KVM
  Virtualization type:   full
Caches (sum of all):     
  L1d:                   512 KiB (16 instances)
  L1i:                   512 KiB (16 instances)
  L2:                    8 MiB (16 instances)
  L3:                    2 GiB (16 instances)
NUMA:                    
  NUMA node(s):          1
  NUMA node0 CPU(s):     0-15
Vulnerabilities:         
  Itlb multihit:         Not affected
  L1tf:                  Not affected
  Mds:                   Not affected
  Meltdown:              Not affected
  Mmio stale data:       Not affected
  Retbleed:              Mitigation; untrained return thunk; SMT disabled
  Spec store bypass:     Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:            Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:            Mitigation; Retpolines, IBPB conditional, STIBP disabled, RSB filling, PBRSB-e                         IBRS Not affected
  Srbds:                 Not affected
  Tsx async abort:       Not affected
```

### YABS

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 2 minutes
Processor  : AMD EPYC 7402 24-Core Processor
CPU cores  : 16 @ 2794.748 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 127.7 GiB
Swap       : 0.0 KiB
Disk       : 8.1 TiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-9-amd64
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
Read       | 204.07 MB/s  (51.0k) | 2.84 GB/s    (44.5k)
Write      | 204.61 MB/s  (51.1k) | 2.86 GB/s    (44.7k)
Total      | 408.68 MB/s (102.1k) | 5.71 GB/s    (89.2k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.74 GB/s     (5.3k) | 2.68 GB/s     (2.6k)
Write      | 2.88 GB/s     (5.6k) | 2.86 GB/s     (2.8k)
Total      | 5.62 GB/s    (10.9k) | 5.55 GB/s     (5.4k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 3.29 Gbits/sec  | 5.19 Gbits/sec  | 3.30 ms        
Scaleway        | Paris, FR (10G)           | 3.29 Gbits/sec  | busy            | 4.76 ms        
NovoServe       | North Holland, NL (40G)   | 3.29 Gbits/sec  | 3.11 Gbits/sec  | 9.77 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | busy            | 96.0 ms        
Clouvider       | NYC, NY, US (10G)         | 1.91 Gbits/sec  | 93.2 Mbits/sec  | 81.8 ms        
Clouvider       | Dallas, TX, US (10G)      | 1.38 Gbits/sec  | 1.43 Gbits/sec  | 128 ms         
Clouvider       | Los Angeles, CA, US (10G) | 1.27 Gbits/sec  | 1.30 Gbits/sec  | 137 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 3.28 Gbits/sec  | 5.19 Gbits/sec  | 3.26 ms        
Scaleway        | Paris, FR (10G)           | busy            | busy            | 4.90 ms        
NovoServe       | North Holland, NL (40G)   | 3.27 Gbits/sec  | 2.92 Gbits/sec  | 9.39 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | 2.00 Gbits/sec  | 96.0 ms        
Clouvider       | NYC, NY, US (10G)         | 1.63 Gbits/sec  | 238 Mbits/sec   | 81.5 ms        
Clouvider       | Dallas, TX, US (10G)      | 1.33 Gbits/sec  | 1.49 Gbits/sec  | 128 ms         
Clouvider       | Los Angeles, CA, US (10G) | 1.18 Gbits/sec  | 1.31 Gbits/sec  | 136 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1294                          
Multi Core      | 8891                          
Full Test       | https://browser.geekbench.com/v6/cpu/1957381

YABS completed in 12 min 43 sec
```

### Bench

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD EPYC 7402 24-Core Processor
 CPU Cores          : 16 @ 2794.748 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 8.1 TB (61.0 GB Used)
 Total Mem          : 127.7 GB (1.5 GB Used)
 System uptime      : 0 days, 0 hour 18 min
 Load average       : 0.04, 0.54, 0.41
 OS                 : Debian GNU/Linux 12
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.1.0-9-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS16276 OVH SAS
 Location           : Gravelines / FR
 Region             : Hauts-de-France
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.2 GB/s
 I/O Speed(2nd run) : 1.4 GB/s
 I/O Speed(3rd run) : 1.4 GB/s
 I/O Speed(average) : 1365.3 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    3011.25 Mbps      3475.01 Mbps        4.95 ms     
 Los Angeles, US  651.18 Mbps       4730.37 Mbps        140.33 ms   
 Dallas, US       714.20 Mbps       4371.31 Mbps        111.88 ms   
 Montreal, CA     169.80 Mbps       908.58 Mbps         87.62 ms    
 Amsterdam, NL    3195.70 Mbps      3544.79 Mbps        11.46 ms    
 Shanghai, CN     330.36 Mbps       2379.08 Mbps        240.65 ms   
 Nanjing, CN      1.97 Mbps         2037.53 Mbps        340.03 ms   
 Hongkong, CN     2.83 Mbps         319.71 Mbps         429.06 ms   
 Singapore, SG    162.48 Mbps       189.85 Mbps         231.20 ms   
 Tokyo, JP        306.91 Mbps       3190.71 Mbps        230.12 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 25 sec
 Timestamp          : 2023-07-18 17:06:12 CST
----------------------------------------------------------------------
```

### benchy

```
root@Azusa:~# wget -qO- benchy.pw | sh
# # # # # # # # # # # # # # # # # # # # #
#             Benchy v2.7               #
#    https://github.com/L1so/benchy     #
# # # # # # # # # # # # # # # # # # # # #
#        18 Jul 2023 17:06 CST          #
# # # # # # # # # # # # # # # # # # # # #

Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Debian GNU/Linux 12 (bookworm)     Model       : AMD EPYC 7402 24-Core Processor
Location   : France                             Core        : 16 @ 2794.748 MHz
Kernel     : 6.1.0-9-amd64                      AES-NI      : ✔ Enabled
Uptime     : 0 days, 0 hrs, 24 mins, 41 secs    VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 0.0 KiB   

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 8.1 TiB                            ASN         : AS16276   
Disk Usage : 61.0 GiB (1% Used)                 ISP         : OVH SAS   
Mem        : 127.7 GiB                          IPv4        : ✔ Enabled
Mem Usage  : 1.5 GiB (1% Used)                  IPv6        : ✔ Enabled

Disk Performance Check (xfs on /dev/vda3) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 196.19 MB/s | 196.70 MB/s | 392.90 MB/s | 50.2k  | 50.4k  | 100.6k |
| 64k  | 2.59 GB/s   | 2.61 GB/s   | 5.20 GB/s   | 42.5k  | 42.8k  | 85.3k  |
| 512k | 2.46 GB/s   | 2.59 GB/s   | 5.06 GB/s   | 5.0k   | 5.3k   | 10.4k  |
| 1m   | 2.41 GB/s   | 2.58 GB/s   | 5.00 GB/s   | 2.5k   | 2.6k   | 5.1k   |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |    1.7 Gb/s  |        busy  |  105.3 ms |
|       | Uztelecom   | Tashkent, UZ    |   12.5 Mb/s  |        busy  |   96.2 ms |
|       | Novogara    | Amsterdam, NL   |    3.3 Gb/s  |    1.6 Gb/s  |   12.0 ms |
|       | FiberBy     | Copenhagen, DK  |    2.3 Gb/s  |    2.6 Gb/s  |   20.9 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |    1.7 Gb/s  |    1.2 Gb/s  |  105.2 ms |
|       | Uztelecom   | Tashkent, UZ    |        busy  |        busy  |   96.2 ms |
|       | Novogara    | Amsterdam, NL   |    3.3 Gb/s  |    3.0 Gb/s  |   12.0 ms |
|       | FiberBy     | Copenhagen, DK  |    2.7 Gb/s  |    2.7 Gb/s  |   20.9 ms |
+---------------------------------------------------------------------------------+

+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 1291                     |
| Multi Core         | 8792                     |
+-----------------------------------------------+
| https://browser.geekbench.com/v6/cpu/1957524  |
+-----------------------------------------------+
| Benchy time spent  | 9 Minutes 38 Seconds     |
+-----------------------------------------------+
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7402 24-Core Processor
 CPU 核心数        : 16
 CPU 频率          : 2794.748 MHz
 CPU 缓存          : L1: 512.00 KB / L2: 8.00 MB / L3: 2048.00 MB
 硬盘空间          : 61.00 GiB / 8.12 TiB
 启动盘路径        : /dev/vda3
 内存              : 641.45 MiB / 127.73 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 35 min
 负载              : 0.91, 1.27, 0.78
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS16276 OVH SAS
 IPV4 位置         : Gravelines / Hauts-de-France / FR
 IPV6 ASN          : AS16276 OVH SAS
 IPV6 位置         : Gravelines / FR-59
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           1615 Scores
 16 线程测试(多核)得分:                 25793 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          42749.64 MB/s
 单线程写测试:          19332.86 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         28.3 MB/s (6897 IOPS, 3.71s)            36.3 MB/s (8854 IOPS, 2.89s)
 1GB-1M Block           1.1 GB/s (1025 IOPS, 0.98s)             1.2 GB/s (1153 IOPS, 0.87s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 216.63 MB/s  (54.1k) | 2.83 GB/s    (44.3k)
Write      | 217.20 MB/s  (54.3k) | 2.85 GB/s    (44.5k)
Total      | 433.83 MB/s (108.4k) | 5.69 GB/s    (88.9k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.68 GB/s     (5.2k) | 2.69 GB/s     (2.6k)
Write      | 2.82 GB/s     (5.5k) | 2.87 GB/s     (2.8k)
Total      | 5.50 GB/s    (10.7k) | 5.56 GB/s     (5.4k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: ATMAN
视频缓存节点地域: 波兰 华沙(WAW3)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: DTELIX
视频缓存节点地域: KBP(KBP3)
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
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               No
 Netflix:                               No
 YouTube Premium:                       Yes (Region: FR)
 Amazon Prime Video:                    Yes (Region: FR)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   FR
 Viu.com:                               No
 YouTube CDN:                           Associated with [ATMAN]
 Netflix Preferred CDN:                 Failed
 Spotify Registration:                  No
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: FR)
 Netflix:                               No
 YouTube Premium:                       Yes (Region: FR)
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Associated with [DTELIX]
 Netflix Preferred CDN:                 Failed
 Spotify Registration:                  No
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【FR】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：30
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
  欺诈分数(越低越好)：42
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
  欺诈分数(越低越好)：30
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
2023/07/18 17:19:43 北京电信 219.141.136.12  电信163 [普通线路]           
2023/07/18 17:19:43 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/18 17:19:43 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/18 17:19:43 上海电信 202.96.209.133  测试超时
2023/07/18 17:19:43 上海联通 210.22.97.1     联通4837[普通线路]           
2023/07/18 17:19:43 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/18 17:19:43 广州电信 58.60.188.222   电信163 [普通线路]           
2023/07/18 17:19:43 广州联通 210.21.196.6    联通4837[普通线路]           
2023/07/18 17:19:43 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/07/18 17:19:43 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/18 17:19:43 成都联通 119.6.6.6       联通4837[普通线路]           
2023/07/18 17:19:43 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
1.42 ms  *  局域网
0.51 ms  *  局域网
0.36 ms  *  局域网
1.72 ms  *  局域网
4.99 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
5.20 ms  *  局域网
8.13 ms  AS3356  英国, 伦敦, level3.com
107.88 ms  AS3356  英国, 伦敦, level3.com
360.59 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
374.19 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
372.71 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
371.82 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
365.47 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.39 ms  *  局域网
0.48 ms  *  局域网
0.46 ms  *  局域网
1.34 ms  *  局域网
5.23 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
5.17 ms  *  局域网
151.98 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
265.08 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
243.07 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
234.60 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
241.51 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
236.21 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
243.73 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
234.37 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.42 ms  *  局域网
0.60 ms  *  局域网
0.46 ms  *  局域网
1.30 ms  *  局域网
4.72 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
4.87 ms  *  局域网
5.81 ms  AS16276  美国, 伊利诺伊州, 芝加哥, ovh.com
107.49 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
293.38 ms  AS9808  中国, 上海, chinamobile.com, 移动
272.21 ms  AS9808  中国, 上海, chinamobile.com, 移动
259.34 ms  AS9808  中国, 北京, chinamobile.com, 移动
314.22 ms  AS9808  中国, 北京, chinamobile.com, 移动
268.23 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    3013.89 Mbps    6233.02 Mbps    5.21     0.0%
日本东京         271.42 Mbps     2759.72 Mbps    234.79   15.7%
新加坡           396.97 Mbps     2938.65 Mbps    237.70   0.0%
联通Fuzhou       433.51 Mbps     1289.41 Mbps    200.21   0.0%
联通湖南5G       465.89 Mbps     281.98 Mbps     178.46   NULL
电信上海         4.50 Mbps       2369.24 Mbps    234.10   NULL
电信天津         0.71 Mbps       3203.38 Mbps    242.05   NULL
移动Beijing      7.52 Mbps       2890.23 Mbps    313.46   3.7%
移动Chengdu      8.69 Mbps       10.99 Mbps      277.24   2.1%
------------------------------------------------------------------------
 总共花费      : 6 分 52 秒
 时间          : Tue Jul 18 17:25:24 CST 2023
------------------------------------------------------------------------
```

### UnixBench测试

```
------------------------------------------------------------------------
Benchmark Run: Tue Jul 18 2023 17:27:09 - 17:55:09
16 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       40002099.3 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     7272.3 MWIPS (10.0 s, 7 samples)
Execl Throughput                               2799.2 lps   (29.9 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        728902.7 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          203174.5 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       2105691.9 KBps  (30.0 s, 2 samples)
Pipe Throughput                             1451251.6 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                  43938.9 lps   (10.0 s, 7 samples)
Process Creation                               2930.6 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                   5147.8 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   2837.0 lpm   (60.0 s, 2 samples)
System Call Overhead                        1612809.8 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   40002099.3   3427.8
Double-Precision Whetstone                       55.0       7272.3   1322.2
Execl Throughput                                 43.0       2799.2    651.0
File Copy 1024 bufsize 2000 maxblocks          3960.0     728902.7   1840.7
File Copy 256 bufsize 500 maxblocks            1655.0     203174.5   1227.6
File Copy 4096 bufsize 8000 maxblocks          5800.0    2105691.9   3630.5
Pipe Throughput                               12440.0    1451251.6   1166.6
Pipe-based Context Switching                   4000.0      43938.9    109.8
Process Creation                                126.0       2930.6    232.6
Shell Scripts (1 concurrent)                     42.4       5147.8   1214.1
Shell Scripts (8 concurrent)                      6.0       2837.0   4728.3
System Call Overhead                          15000.0    1612809.8   1075.2
                                                                   ========
System Benchmarks Index Score                                        1132.5

------------------------------------------------------------------------
Benchmark Run: Tue Jul 18 2023 17:55:09 - 18:23:13
16 CPUs in system; running 16 parallel copies of tests

Dhrystone 2 using register variables      638847500.4 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                   115990.1 MWIPS (9.9 s, 7 samples)
Execl Throughput                              17476.1 lps   (29.7 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        430580.5 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          114744.4 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       1411334.4 KBps  (30.0 s, 2 samples)
Pipe Throughput                            22932463.7 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                1893026.0 lps   (10.0 s, 7 samples)
Process Creation                              35708.3 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  59491.8 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   7910.6 lpm   (60.1 s, 2 samples)
System Call Overhead                        2965300.5 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  638847500.4  54742.7
Double-Precision Whetstone                       55.0     115990.1  21089.1
Execl Throughput                                 43.0      17476.1   4064.2
File Copy 1024 bufsize 2000 maxblocks          3960.0     430580.5   1087.3
File Copy 256 bufsize 500 maxblocks            1655.0     114744.4    693.3
File Copy 4096 bufsize 8000 maxblocks          5800.0    1411334.4   2433.3
Pipe Throughput                               12440.0   22932463.7  18434.5
Pipe-based Context Switching                   4000.0    1893026.0   4732.6
Process Creation                                126.0      35708.3   2834.0
Shell Scripts (1 concurrent)                     42.4      59491.8  14031.1
Shell Scripts (8 concurrent)                      6.0       7910.6  13184.3
System Call Overhead                          15000.0    2965300.5   1976.9
                                                                   ========
System Benchmarks Index Score                                        5507.1



======= Script description and score comparison completed! ======= 
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD EPYC 7402 24-Core Processor (x86_64)
16 cores @ 0 MHz  |  127.7 GiB RAM
Number of Processes: 16  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          27384
  Integer Math                     74848 Million Operations/s
  Floating Point Math              53863 Million Operations/s
  Prime Numbers                    239 Million Primes/s
  Sorting                          43032 Thousand Strings/s
  Encryption                       18245 MB/s
  Compression                      327055 KB/s
  CPU Single Threaded              2079 Million Operations/s
  Physics                          3750 Frames/s
  Extended Instructions (SSE)      27495 Million Matrices/s

Memory Mark:                       1738
  Database Operations              9225 Thousand Operations/s
  Memory Read Cached               23539 MB/s
  Memory Read Uncached             9380 MB/s
  Memory Write                     9728 MB/s
  Available RAM                    129492 Megabytes
  Memory Latency                   114 Nanoseconds
  Memory Threaded                  94585 MB/s
--------------------------------------------------------------------------
```

### 四网回程测试

```
----------------------------------------------------------------------
北京电信
traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  192.168.0.1  0.39 ms  *  局域网
 2  *
 3  10.73.1.79  0.42 ms  *  局域网
 4  10.73.1.76  0.50 ms  *  局域网
 5  10.95.33.8  5.71 ms  *  局域网
 6  be102.par-gsw-sbb1-nc5.fr.eu (91.121.215.177)  4.94 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
 7  10.200.2.75  5.05 ms  *  局域网
 8  *
 9  ae3.3202.edge3.London15.level3.net (4.69.143.246)  7.55 ms  AS3356  英国, 伦敦, level3.com
10  195.50.126.218  89.52 ms  AS3356  英国, 伦敦, level3.com
11  202.97.76.33  304.37 ms  AS4134  中国, 北京, chinatelecom.com.cn, 电信
12  *
13  202.97.34.89  305.85 ms  AS4134  中国, 北京, chinatelecom.com.cn, 电信
14  *
15  6.254.120.106.static.bjtelecom.net (106.120.254.6)  415.86 ms  AS4847  中国, 北京, chinatelecom.com.cn, 电信
16  bj141-147-210.bjtelecom.net (219.141.147.210)  325.00 ms  AS4847  中国, 北京, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
上海电信
traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  192.168.0.1  0.43 ms  *  局域网
 2  *
 3  10.73.1.95  0.43 ms  *  局域网
 4  10.73.1.88  0.38 ms  *  局域网
 5  10.95.33.8  1.35 ms  *  局域网
 6  be102.par-gsw-sbb1-nc5.fr.eu (91.121.215.177)  4.89 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
 7  10.200.2.65  4.77 ms  *  局域网
 8  *
 9  be3001.ccr41.par01.atlas.cogentco.com (154.54.60.221)  30.99 ms  AS174  法国, 法兰西岛大区, 巴黎, cogentco.com
10  be12497.ccr41.lon13.atlas.cogentco.com (154.54.56.129)  8.27 ms  AS174  英国, 伦敦, cogentco.com
11  be2375.rcr21.b015533-1.lon13.atlas.cogentco.com (154.54.61.158)  8.31 ms  AS174  英国, 伦敦, cogentco.com
12  chinatelecom.demarc.cogentco.com (149.14.81.226)  9.19 ms  AS174  英国, 伦敦, cogentco.com
13  202.97.93.153  240.63 ms  AS4134  中国, 上海, chinatelecom.com.cn, 电信
14  *
15  202.97.71.29  236.96 ms  AS4134  中国, 上海, chinatelecom.com.cn, 电信
16  *
17  101.95.89.158  224.01 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信
18  180.169.255.114  229.90 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信
19  ns-pd.online.sh.cn (202.96.209.133)  222.59 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
深圳电信
traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  192.168.0.1  0.49 ms  *  局域网
 2  *
 3  10.73.1.103  0.30 ms  *  局域网
 4  10.73.1.96  0.54 ms  *  局域网
 5  10.95.33.8  1.42 ms  *  局域网
 6  be102.par-gsw-sbb1-nc5.fr.eu (91.121.215.177)  5.06 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
 7  10.200.2.67  5.01 ms  *  局域网
 8  *
 9  ae3.3202.edge3.London15.level3.net (4.69.143.246)  7.51 ms  AS3356  英国, 伦敦, level3.com
10  195.50.126.218  86.57 ms  AS3356  英国, 伦敦, level3.com
11  *
12  202.97.12.38  374.34 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
13  *
14  14.147.127.82  368.41 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
15  *
16  58.60.188.222  267.37 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
北京联通
traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  192.168.0.1  0.29 ms  *  局域网
 2  *
 3  10.73.1.79  0.31 ms  *  局域网
 4  10.73.1.76  0.35 ms  *  局域网
 5  10.95.33.8  1.28 ms  *  局域网
 6  be102.par-gsw-sbb1-nc5.fr.eu (91.121.215.177)  4.89 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
 7  10.200.2.71  6.87 ms  *  局域网
 8  verizon-2.par.franceix.net (37.49.237.174)  5.10 ms  *  法国, 法兰西岛大区, 巴黎, franceix.net
 9  0.et-5-0-2.GW3.FFT3.ALTER.NET (140.222.235.165)  12.16 ms  *  德国, 黑森州, 法兰克福, verizon.com
10  *
11  219.158.19.121  165.58 ms  AS4837  中国, 北京, chinaunicom.com, 联通
12  219.158.3.133  165.95 ms  AS4837  中国, 北京, chinaunicom.com, 联通
13  219.158.5.145  177.14 ms  AS4837  中国, 北京, chinaunicom.com, 联通
14  125.33.186.198  163.58 ms  AS4808  中国, 北京, chinaunicom.com, 联通
15  202.106.50.1  166.19 ms  AS4808  中国, 北京, chinaunicom.com, 联通

----------------------------------------------------------------------
上海联通
traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  192.168.0.1  0.28 ms  *  局域网
 2  *
 3  10.73.1.103  0.34 ms  *  局域网
 4  10.73.1.102  0.43 ms  *  局域网
 5  10.95.33.10  1.20 ms  *  局域网
 6  be102.par-th2-sbb1-nc5.fr.eu (213.186.32.215)  4.89 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
 7  10.200.2.67  5.23 ms  *  局域网
 8  *
 9  4.69.209.165  151.72 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
10  CHINA-NETCO.edge1.SanJose3.Level3.net (4.53.208.102)  243.95 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
11  219.158.97.181  235.80 ms  AS4837  中国, 上海, chinaunicom.com, 联通
12  219.158.19.90  235.67 ms  AS4837  中国, 上海, chinaunicom.com, 联通
13  219.158.19.69  231.62 ms  AS4837  中国, 上海, chinaunicom.com, 联通
14  *
15  112.64.250.202  232.59 ms  AS17621  中国, 上海, chinaunicom.com, 联通
16  210.22.97.1  245.00 ms  AS17621  中国, 上海, chinaunicom.com, 联通

----------------------------------------------------------------------
深圳联通
traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  192.168.0.1  0.34 ms  *  局域网
 2  *
 3  10.73.1.87  0.44 ms  *  局域网
 4  10.73.1.86  0.48 ms  *  局域网
 5  10.95.33.10  1.47 ms  *  局域网
 6  be102.par-th2-sbb1-nc5.fr.eu (213.186.32.215)  5.16 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
 7  10.200.2.75  5.00 ms  *  局域网
 8  *
 9  ae3.30.edge1.LosAngeles6.level3.net (4.69.153.125)  151.66 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
10  CHINA-UNICO.edge1.LosAngeles6.Level3.net (4.26.1.134)  267.41 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
11  219.158.96.233  245.74 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
12  219.158.4.53  239.46 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
13  219.158.3.85  241.51 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
14  120.86.0.58  235.64 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
15  120.80.147.254  241.44 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
16  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  234.48 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通

----------------------------------------------------------------------
北京移动
traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  192.168.0.1  0.33 ms  *  局域网
 2  *
 3  10.73.1.95  0.33 ms  *  局域网
 4  10.73.1.94  0.45 ms  *  局域网
 5  10.95.33.10  1.17 ms  *  局域网
 6  be102.par-th2-sbb1-nc5.fr.eu (213.186.32.215)  5.46 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
 7  10.200.2.85  4.82 ms  *  局域网
 8  chinmb.as58453.fr.eu (54.36.50.153)  6.08 ms  AS16276  美国, 伊利诺伊州, 芝加哥, ovh.com
 9  223.120.10.141  119.64 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
10  223.120.16.22  232.27 ms  AS58453  中国, 北京, chinamobile.com, 移动
11  221.183.55.110  226.25 ms  AS9808  中国, 北京, chinamobile.com, 移动
12  221.183.25.201  253.49 ms  AS9808  中国, 北京, chinamobile.com, 移动
13  221.183.89.122  254.65 ms  AS9808  中国, 北京, chinamobile.com, 移动
14  221.183.46.178  251.50 ms  AS9808  中国, 北京, chinamobile.com, 移动
15  221.183.130.142  222.65 ms  AS9808  中国, 北京, chinamobile.com, 移动
16  cachedns03.bj.chinamobile.com (221.179.155.161)  202.20 ms  AS56048  中国, 北京, chinamobile.com, 移动

----------------------------------------------------------------------
上海移动
traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  192.168.0.1  0.41 ms  *  局域网
 2  *
 3  10.73.1.103  0.89 ms  *  局域网
 4  10.73.1.96  0.43 ms  *  局域网
 5  10.95.33.8  1.62 ms  *  局域网
 6  be102.par-gsw-sbb1-nc5.fr.eu (91.121.215.177)  4.91 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
 7  10.200.2.21  4.71 ms  *  局域网
 8  chinmb.as58453.fr.eu (54.36.50.153)  5.88 ms  AS16276  美国, 伊利诺伊州, 芝加哥, ovh.com
 9  223.120.10.141  116.97 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
10  223.120.14.150  297.48 ms  AS58453  中国, 上海, chinamobile.com, 移动
11  221.183.89.178  279.75 ms  AS9808  中国, 上海, chinamobile.com, 移动
12  *
13  *
14  *
15  221.181.125.138  334.29 ms  AS24400  中国, 上海, chinamobile.com, 移动
16  211.136.112.252  296.82 ms  AS24400  中国, 上海, chinamobile.com, 移动
17  211.136.112.200  280.96 ms  AS24400  中国, 上海, chinamobile.com, 移动

----------------------------------------------------------------------
深圳移动
traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  192.168.0.1  0.32 ms  *  局域网
 2  *
 3  10.73.1.95  0.37 ms  *  局域网
 4  10.73.1.92  0.43 ms  *  局域网
 5  10.95.33.8  1.26 ms  *  局域网
 6  be102.par-gsw-sbb1-nc5.fr.eu (91.121.215.177)  5.24 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
 7  10.200.2.21  4.66 ms  *  局域网
 8  chinmb.as58453.fr.eu (54.36.50.153)  6.51 ms  AS16276  美国, 伊利诺伊州, 芝加哥, ovh.com
 9  223.120.10.145  116.70 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
10  *
11  221.183.89.182  341.24 ms  AS9808  中国, 上海, chinamobile.com, 移动
12  221.183.89.69  316.33 ms  AS9808  中国, 上海, chinamobile.com, 移动
13  *
14  *
15  221.183.46.174  304.06 ms  AS9808  中国, 北京, chinamobile.com, 移动
16  *
17  ns6.gd.cnmobile.net (120.196.165.24)  311.95 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动

----------------------------------------------------------------------
成都教育网
traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  192.168.0.1  0.32 ms  *  局域网
 2  *
 3  10.73.1.79  0.39 ms  *  局域网
 4  10.73.1.72  0.46 ms  *  局域网
 5  10.95.33.8  1.50 ms  *  局域网
 6  be102.par-gsw-sbb1-nc5.fr.eu (91.121.215.177)  4.74 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
 7  10.200.2.21  4.70 ms  *  局域网
 8  chinmb.as58453.fr.eu (54.36.50.153)  5.68 ms  AS16276  美国, 伊利诺伊州, 芝加哥, ovh.com
 9  223.120.10.141  64.00 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
10  223.120.15.174  268.38 ms  AS58453  中国, 香港, chinamobile.com, 移动
11  *
12  223.120.3.86  353.20 ms  AS58453  中国, 香港, chinamobile.com, 移动
13  223.119.81.94  386.07 ms  AS58453  中国, 香港, chinamobile.com, 移动
14  101.4.117.70  364.13 ms  AS4538  中国, 香港, edu.cn, 教育网
15  101.4.114.181  404.75 ms  AS4538  中国, 北京, edu.cn, 教育网
16  *
17  *
18  101.4.112.14  460.99 ms  AS4538  中国, 陕西, 西安, edu.cn, 教育网
19  *
20  *
21  *
22  *
23  *
24  *
25  202.112.14.151  460.57 ms  AS24355  中国, 四川, 成都, 电子科技大学CERNET西南地区网络中心, edu.cn, 教育网

----------------------------------------------------------------------
```
