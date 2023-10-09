---
title: "HXServers 洛杉矶 AMD 7950X 测评"
date: "2023-10-03"
categories: 
  - "vps"
  - "special"
  - "usa"
---

最近在Low上挺火的一个商家，深受mjj的喜爱，是ReliableSite的二次经销商，但具体测试下来，商家的cpu超售的似乎很厉害，技术也存在很大问题，也无ipv6，cpu无法正常识别是7950X(已经和商家确认过，商家的解释是适合迁移?)，单核长期也只有1900分左右(商家解释说是因为大量人在运行yabs导致的)，对于一个7950X来说明显优点糟糕。不是很推荐为了性能而购买。

> ## 套餐
> 
> **_Provider :_ HXServers  
> _Type/Plan :_ LA - 1GB  
> _Processor :_ AMD Ryzen 9 7950X (4.5 GHz++)  
> _Num of Core : 2 Cores_  
> _Memory : 1 GB_ DDR5 RAM  
> _Storage : 25 GB NVMe_(PCIe 4.0)  
> _Bandwidth : Unmetered @ 10 Gbps IN | 1 Gbps OUT_  
> _Location :_ Los Angeles  
> _Price :_ $1.5 /month**

## 测评

### lscpu

```
root@catcat:~# lscpu
Architecture:            x86_64
  CPU op-mode(s):        32-bit, 64-bit
  Address sizes:         40 bits physical, 48 bits virtual
  Byte Order:            Little Endian
CPU(s):                  2
  On-line CPU(s) list:   0,1
Vendor ID:               AuthenticAMD
  BIOS Vendor ID:        QEMU
  Model name:            AMD EPYC-Milan Processor
    BIOS Model name:     pc-i440fx-6.2  CPU @ 2.0GHz
    BIOS CPU family:     1
    CPU family:          25
    Model:               1
    Thread(s) per core:  1
    Core(s) per socket:  1
    Socket(s):           2
    Stepping:            1
    BogoMIPS:            8983.07
    Flags:             
Virtualization features: 
  Virtualization:        AMD-V
  Hypervisor vendor:     KVM
  Virtualization type:   full
Caches (sum of all):     
  L1d:                   64 KiB (2 instances)
  L1i:                   64 KiB (2 instances)
  L2:                    1 MiB (2 instances)
  L3:                    64 MiB (2 instances)
NUMA:                    
  NUMA node(s):          1
  NUMA node0 CPU(s):     0,1
Vulnerabilities:         
  Itlb multihit:         Not affected
  L1tf:                  Not affected
  Mds:                   Not affected
  Meltdown:              Not affected
  Mmio stale data:       Not affected
  Retbleed:              Not affected
  Spec store bypass:     Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:            Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:            Mitigation; Retpolines, IBPB conditional, IBRS_FW, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected  Srbds:                 Not affected
  Tsx async abort:       Not affected
```

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 1 days, 11 hours, 42 minutes
Processor  : AMD EPYC-Milan Processor
CPU cores  : 2 @ 4491.536 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 942.7 MiB
Swap       : 975.0 MiB
Disk       : 23.5 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-10-cloud-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : Ipxo LLC
ASN        : AS23470 ReliableSite.Net LLC
Location   : Aliso Viejo, California (CA)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 582.42 MB/s (145.6k) | 2.62 GB/s    (40.9k)
Write      | 583.95 MB/s (145.9k) | 2.63 GB/s    (41.1k)
Total      | 1.16 GB/s   (291.5k) | 5.25 GB/s    (82.1k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.50 GB/s     (4.8k) | 2.97 GB/s     (2.9k)
Write      | 2.63 GB/s     (5.1k) | 3.16 GB/s     (3.0k)
Total      | 5.13 GB/s    (10.0k) | 6.14 GB/s     (5.9k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | busy            | 1.32 Gbits/sec  | 125 ms         
Scaleway        | Paris, FR (10G)           | 219 Mbits/sec   | 1.26 Gbits/sec  | 144 ms         
NovoServe       | North Holland, NL (40G)   | 167 Mbits/sec   | 1.17 Gbits/sec  | 148 ms         
Uztelecom       | Tashkent, UZ (10G)        | 189 Mbits/sec   | 695 Mbits/sec   | 242 ms         
Clouvider       | NYC, NY, US (10G)         | 273 Mbits/sec   | 2.24 Gbits/sec  | 56.5 ms        
Clouvider       | Dallas, TX, US (10G)      | 311 Mbits/sec   | 5.66 Gbits/sec  | 26.3 ms        
Clouvider       | Los Angeles, CA, US (10G) | 878 Mbits/sec   | 6.56 Gbits/sec  | 0.339 ms       

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1831                          
Multi Core      | 1990                          
Full Test       | https://browser.geekbench.com/v6/cpu/2887530

YABS completed in 10 min 42 sec
```

### Bench

```
----------------------------------------------------------------------
 CPU Model          : AMD EPYC-Milan Processor
 CPU Cores          : 2 @ 4491.536 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 23.5 GB (820.8 MB Used)
 Total Mem          : 942.7 MB (212.6 MB Used)
 Total Swap         : 975.0 MB (23.2 MB Used)
 System uptime      : 1 days, 11 hour 58 min
 Load average       : 0.05, 0.32, 0.28
 OS                 : Debian GNU/Linux 12
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.1.0-10-cloud-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Offline
 Organization       : AS23470 ReliableSite.Net LLC
 Location           : Los Angeles / US
 Region             : California
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.4 GB/s
 I/O Speed(2nd run) : 1.3 GB/s
 I/O Speed(3rd run) : 1.3 GB/s
 I/O Speed(average) : 1365.3 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    115.50 Mbps       5408.56 Mbps        40.77 ms    
 Los Angeles, US  667.02 Mbps       6078.93 Mbps        0.90 ms     
 Dallas, US       80.13 Mbps        3859.90 Mbps        28.98 ms    
 Montreal, CA     71.74 Mbps        872.32 Mbps         67.39 ms    
 Paris, FR        108.28 Mbps       4204.24 Mbps        138.59 ms   
 Amsterdam, NL    74.70 Mbps        3875.50 Mbps        126.09 ms   
 Shanghai, CN     0.89 Mbps         2607.45 Mbps        213.93 ms   
 Nanjing, CN      29.79 Mbps        1696.07 Mbps        166.16 ms   
 Hongkong, CN     58.49 Mbps        76.45 Mbps          350.51 ms   
 Singapore, SG    101.50 Mbps       1653.00 Mbps        161.25 ms   
 Tokyo, JP        37.95 Mbps        3385.97 Mbps        108.65 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 42 sec
 Timestamp          : 2023-10-03 22:48:25 CST
----------------------------------------------------------------------
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC-Milan Processor
 CPU 核心数        : 2
 CPU 频率          : 4491.536 MHz
 CPU 缓存          : L1: 64.00 KB / L2: 1.00 MB / L3: 64.00 MB
 硬盘空间          : 826.88 MiB / 24063.03 MiB
 启动盘路径        : /dev/vda1
 内存              : 144.82 MiB / 942.73 MiB
 Swap              : 21.93 MiB / 975.00 MiB
 系统在线时间      : 1 days, 12 hour 6 min
 负载              : 0.31, 0.15, 0.19
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-10-cloud-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS23470 ReliableSite.Net LLC
 IPV4 位置         : Los Angeles / California / US
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           6061 Scores
 2 线程测试(多核)得分:          11415 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          73111.11 MB/s
 单线程写测试:          41080.60 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         134 MB/s (32.74 IOPS, 0.78s))           170 MB/s (41468 IOPS, 0.62s)
 1GB-1M Block           1.3 GB/s (1194 IOPS, 0.84s)             3.9 GB/s (3702 IOPS, 0.27s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 546.12 MB/s (136.5k) | 2.31 GB/s    (36.1k)
Write      | 547.56 MB/s (136.8k) | 2.32 GB/s    (36.3k)
Total      | 1.09 GB/s   (273.4k) | 4.63 GB/s    (72.4k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.56 GB/s     (5.0k) | 2.94 GB/s     (2.8k)
Write      | 2.70 GB/s     (5.2k) | 3.14 GB/s     (3.0k)
Total      | 5.27 GB/s    (10.3k) | 6.09 GB/s     (5.9k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX17S56)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Unsupport
 HotStar:                               Yes (Region: US)
 Disney+:                               No
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Failed
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Los Angeles, CA 
 Netflix Preferred CDN:                 Associated with [] in [Los Angeles, CA ]
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 39②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  business⑨  
  公司类型(company_type):business①  hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes② ⑥   No⑨ 
  移动网络(mobile):  Yes⑥ 
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
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测88 ③
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: US 城市: Los Angeles 服务商: AS23470 ReliableSite.Net LLC
北京电信 219.141.136.12  电信163 [普通线路]           
北京联通 202.106.50.1    联通4837[普通线路]           
北京移动 221.179.155.161 移动CMI [普通线路]           
上海电信 202.96.209.133  电信163 [普通线路]           
上海联通 210.22.97.1     联通4837[普通线路]           
上海移动 211.136.112.200 移动CMI [普通线路]           
广州电信 58.60.188.222   电信163 [普通线路]           
广州联通 210.21.196.6    联通4837[普通线路]           
广州移动 120.196.165.24  移动CMI [普通线路]           
成都电信 61.139.2.69     电信163 [普通线路]           
成都联通 119.6.6.6       联通4837[普通线路]           
成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
2.60 ms         AS23470 美国 加利福尼亚州 洛杉矶 reliablesite.net
7.44 ms         AS3257 [GTT-BACKBONE] 美国 加利福尼亚州 圣何塞 gtt.net
12.93 ms        AS4134 [CHINANET-US] 美国 加利福尼亚州 圣何塞 CT-GTT-PoP chinatelecom.com.cn 电信
188.75 ms       AS4134 [CHINANET-BB] 中国 香港 chinatelecom.com.cn 电信
* ms    AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
201.73 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.96 ms         AS23470 美国 加利福尼亚州 洛杉矶 reliablesite.net
201.18 ms       AS3257 [GTT-GTT] 美国 加利福尼亚州 洛杉矶 gtt.net
7.21 ms         AS3257 [GTT-BACKBONE] 美国 加利福尼亚州 圣何塞 gtt.net
285.63 ms       AS3257 [TINET-TINET] 美国 加利福尼亚州 圣何塞 gtt.net
335.75 ms       AS4837 [CU169-BACKBONE] 中国 上海市 chinaunicom.cn 联通
337.72 ms       AS4837 [CU169-BACKBONE] 中国 上海市 chinaunicom.cn 联通
338.80 ms       AS4837 [CU169-BACKBONE] 中国 上海市 chinaunicom.cn 联通
357.38 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
356.27 ms       AS17816 [UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
375.86 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
385.01 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.88 ms         AS23470 美国 加利福尼亚州 洛杉矶 reliablesite.net
0.90 ms         AS6453 [CCBB-LVW] 美国 加利福尼亚州 洛杉矶 tatacommunications.com
1.02 ms         AS6453 [LVWTC1-TATAC] 美国 加利福尼亚州 洛杉矶 tatacommunications.com
0.90 ms         AS1299 美国 加利福尼亚州 洛杉矶 arelion.com
0.83 ms         AS1299 [ARELION-NET] 美国 加利福尼亚州 洛杉矶 arelion.com
1.23 ms         AS1299 [ARELION-NET] 美国 加利福尼亚州 洛杉矶 arelion.com
0.90 ms         AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
165.06 ms       AS58453 [CMI-INT] 中国 广东省 广州市 cmi.chinamobile.com 移动
186.66 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
182.86 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
294.16 ms       AS9808 [CMNET] 中国 上海市 chinamobile.com 移动
187.43 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
188.73 ms       AS9808 [CMNET] 中国 北京市 chinamobile.com 移动
185.13 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    140.75 Mbps     4749.34 Mbps    44.52    0.4%
洛杉矶           843.06 Mbps     6929.85 Mbps    0.62     0.0%
日本东京         125.15 Mbps     1052.72 Mbps    99.39    NULL
电信合肥5G       0.56 Mbps       1703.50 Mbps    184.34   14.3%
电信Suzhou5G     72.09 Mbps      3333.07 Mbps    155.90   NULL
移动Chengdu      56.71 Mbps      1153.45 Mbps    191.69   0.0%
------------------------------------------------------------------------
 总共花费      : 4 分 33 秒
 时间          : Tue Oct  3 22:55:54 CST 2023
------------------------------------------------------------------------
```

### SpeedTest

```

   Speedtest by Ookla

      Server: Cox - Wichita - Wichita, KS (id: 16623)
         ISP: ReliableSite.Net LLC
Idle Latency:    40.73 ms   (jitter: 0.01ms, low: 40.71ms, high: 40.75ms)
    Download:  5026.65 Mbps (data used: 7.0 GB)                                                   
                 41.09 ms   (jitter: 3.68ms, low: 40.53ms, high: 329.28ms)
      Upload:   108.51 Mbps (data used: 235.1 MB)                                                   
                 40.67 ms   (jitter: 0.07ms, low: 40.56ms, high: 42.32ms)
 Packet Loss:     0.0%
  Result URL: https://www.speedtest.net/result/c/885bbabc-3041-43a1-80b6-f47e0b6e4dae
```

![](https://catcat.blog/wp-content/uploads/2023/10/image-1-1024x378.png)

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD EPYC-Milan Processor (x86_64)
2 cores @ 0 MHz  |  942 MiB RAM
Number of Processes: 2  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          6647
  Integer Math                     15983 Million Operations/s
  Floating Point Math              14017 Million Operations/s
  Prime Numbers                    54.7 Million Primes/s
  Sorting                          9563 Thousand Strings/s
  Encryption                       3529 MB/s
  Compression                      53061 KB/s
  CPU Single Threaded              3384 Million Operations/s
  Physics                          815 Frames/s
  Extended Instructions (SSE)      5691 Million Matrices/s

Memory Mark:                       1043
  Database Operations              1878 Thousand Operations/s
  Memory Read Cached               38126 MB/s
  Memory Read Uncached             25107 MB/s
  Memory Write                     15894 MB/s
  Available RAM                    584 Megabytes
  Memory Latency                   77 Nanoseconds
  Memory Threaded                  31794 MB/s
--------------------------------------------------------------------------
```

### byte-unixbench 性能测试

```
========================================================================
   BYTE UNIX Benchmarks (Version 5.1.3)

   System: catcat: GNU/Linux
   OS: GNU/Linux -- 6.1.0-10-cloud-amd64 -- #1 SMP PREEMPT_DYNAMIC Debian 6.1.38-1 (2023-07-14)
   Machine: x86_64 (unknown)
   Language: en_US.utf8 (charmap="UTF-8", collate="UTF-8")
   CPU 0: AMD EPYC-Milan Processor (8983.1 bogomips)
          x86-64, MMX, AMD MMX, Physical Address Ext, SYSENTER/SYSEXIT, AMD virtualization, SYSCALL/SYSRET
   CPU 1: AMD EPYC-Milan Processor (8983.1 bogomips)
          x86-64, MMX, AMD MMX, Physical Address Ext, SYSENTER/SYSEXIT, AMD virtualization, SYSCALL/SYSRET
   23:04:17 up 1 day, 12:19,  1 user,  load average: 0.36, 0.41, 0.29; runlevel 5

------------------------------------------------------------------------
Benchmark Run: Tue Oct 03 2023 23:04:17 - 23:32:31
2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       77369816.0 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    12693.6 MWIPS (9.9 s, 7 samples)
Execl Throughput                               6334.2 lps   (29.8 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       2046653.8 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          527146.1 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       4526811.1 KBps  (30.0 s, 2 samples)
Pipe Throughput                             3060854.9 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 296528.2 lps   (10.0 s, 7 samples)
Process Creation                              15029.3 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  17365.7 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   3219.5 lpm   (60.0 s, 2 samples)
System Call Overhead                        3298296.1 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   77369816.0   6629.8
Double-Precision Whetstone                       55.0      12693.6   2307.9
Execl Throughput                                 43.0       6334.2   1473.1
File Copy 1024 bufsize 2000 maxblocks          3960.0    2046653.8   5168.3
File Copy 256 bufsize 500 maxblocks            1655.0     527146.1   3185.2
File Copy 4096 bufsize 8000 maxblocks          5800.0    4526811.1   7804.8
Pipe Throughput                               12440.0    3060854.9   2460.5
Pipe-based Context Switching                   4000.0     296528.2    741.3
Process Creation                                126.0      15029.3   1192.8
Shell Scripts (1 concurrent)                     42.4      17365.7   4095.7
Shell Scripts (8 concurrent)                      6.0       3219.5   5365.9
System Call Overhead                          15000.0    3298296.1   2198.9
                                                                   ========
System Benchmarks Index Score                                        2863.9

------------------------------------------------------------------------
Benchmark Run: Tue Oct 03 2023 23:32:31 - 00:00:51
2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables      148093965.1 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    25036.1 MWIPS (10.0 s, 7 samples)
Execl Throughput                              10447.2 lps   (29.9 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       2874821.5 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          691634.0 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       6741965.3 KBps  (30.0 s, 2 samples)
Pipe Throughput                             5945470.8 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 670481.4 lps   (10.0 s, 7 samples)
Process Creation                              29153.4 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  24396.9 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   3190.2 lpm   (60.0 s, 2 samples)
System Call Overhead                        5418752.9 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  148093965.1  12690.1
Double-Precision Whetstone                       55.0      25036.1   4552.0
Execl Throughput                                 43.0      10447.2   2429.6
File Copy 1024 bufsize 2000 maxblocks          3960.0    2874821.5   7259.7
File Copy 256 bufsize 500 maxblocks            1655.0     691634.0   4179.1
File Copy 4096 bufsize 8000 maxblocks          5800.0    6741965.3  11624.1
Pipe Throughput                               12440.0    5945470.8   4779.3
Pipe-based Context Switching                   4000.0     670481.4   1676.2
Process Creation                                126.0      29153.4   2313.8
Shell Scripts (1 concurrent)                     42.4      24396.9   5754.0
Shell Scripts (8 concurrent)                      6.0       3190.2   5317.1
System Call Overhead                          15000.0    5418752.9   3612.5
                                                                   ========
System Benchmarks Index Score                                        4647.0



======= Script description and score comparison completed! ======= 
```
