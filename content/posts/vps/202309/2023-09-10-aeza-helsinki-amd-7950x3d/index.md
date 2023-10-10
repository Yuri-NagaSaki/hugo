---
title: "Aeza Helsinki AMD 7950X3D 测评"
date: "2023-09-10"
categories: 
  - "vps"
  - "eu"
---

> ## 套餐
> 
> Provider : Aeza  
> Type/Plan : AMD Ryzen KVM VPS - Corporate Power  
> Processor : AMD Ryzen 9 7950X3D  
> Num of Core : 2 Cores  
> Memory : 4 GB  
> Storage : 60 GB NVMe  
> Bandwidth : Unlimited @ 1 Gbps IN | 1 Gbps OUT  
> Location : Helsinki  
> Price : 120RMB

## 测评

### CPU

```
root@overt-plant:~# lscpu
Architecture:                    x86_64
CPU op-mode(s):                  32-bit, 64-bit
Byte Order:                      Little Endian
Address sizes:                   48 bits physical, 48 bits virtual
CPU(s):                          2
On-line CPU(s) list:             0,1
Thread(s) per core:              1
Core(s) per socket:              2
Socket(s):                       1
NUMA node(s):                    1
Vendor ID:                       AuthenticAMD
CPU family:                      25
Model:                           97
Model name:                      AMD Ryzen 9 7950X3D 16-Core Processor
Stepping:                        2
CPU MHz:                         4192.104
BogoMIPS:                        8384.20
Hypervisor vendor:               KVM
Virtualization type:             full
L1d cache:                       128 KiB
L1i cache:                       128 KiB
L2 cache:                        1 MiB
L3 cache:                        16 MiB
NUMA node0 CPU(s):               0,1
Vulnerability Itlb multihit:     Not affected
Vulnerability L1tf:              Not affected
Vulnerability Mds:               Not affected
Vulnerability Meltdown:          Not affected
Vulnerability Mmio stale data:   Not affected
Vulnerability Retbleed:          Not affected
Vulnerability Spec store bypass: Mitigation; Speculative Store Bypass disabled via prctl and seccom                                 p
Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitizati                                 on
Vulnerability Spectre v2:        Mitigation; Retpolines, IBPB conditional, IBRS_FW, STIBP disabled,                                  RSB filling, PBRSB-eIBRS Not affected
Vulnerability Srbds:             Not affected
Vulnerability Tsx async abort:   Not affected
```

### 硬盘

![](https://catcat.blog/wp-content/uploads/2023/09/image-59.png)

### 内存

![](https://catcat.blog/wp-content/uploads/2023/09/image-61-1024x149.png)

### Yabs

```
Sun 10 Sep 2023 08:23:25 AM MSK

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 1 minutes
Processor  : AMD Ryzen 9 7950X3D 16-Core Processor
CPU cores  : 2 @ 4192.104 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ❌ Disabled
RAM        : 3.8 GiB
Swap       : 1024.0 MiB
Disk       : 59.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-21-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv4 Network Information:
---------------------------------
ISP        : AEZA GROUP Ltd
ASN        : AS210644 AEZA GROUP Ltd
Host       : Aeza Group LLC
Location   : Helsinki, Uusimaa (18)
Country    : Finland

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 40.01 MB/s   (10.0k) | 656.51 MB/s  (10.2k)
Write      | 40.11 MB/s   (10.0k) | 659.96 MB/s  (10.3k)
Total      | 80.12 MB/s   (20.0k) | 1.31 GB/s    (20.5k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.05 GB/s     (5.9k) | 3.32 GB/s     (3.2k)
Write      | 3.22 GB/s     (6.2k) | 3.54 GB/s     (3.4k)
Total      | 6.27 GB/s    (12.2k) | 6.86 GB/s     (6.7k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 111 Mbits/sec   | 181 Mbits/sec   | 35.2 ms        
Scaleway        | Paris, FR (10G)           | 803 Mbits/sec   | 363 Mbits/sec   | 38.0 ms        
NovoServe       | North Holland, NL (40G)   | 803 Mbits/sec   | 797 Mbits/sec   | 36.0 ms        
Uztelecom       | Tashkent, UZ (10G)        | 772 Mbits/sec   | 381 Mbits/sec   | 95.7 ms        
Clouvider       | NYC, NY, US (10G)         | 21.1 Mbits/sec  | 26.5 Mbits/sec  | 174 ms         
Clouvider       | Dallas, TX, US (10G)      | 21.6 Mbits/sec  | 20.3 Mbits/sec  | 172 ms         
Clouvider       | Los Angeles, CA, US (10G) | 21.9 Mbits/sec  | 26.9 Mbits/sec  | 172 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 116 Mbits/sec   | 215 Mbits/sec   | 35.7 ms        
Scaleway        | Paris, FR (10G)           | 746 Mbits/sec   | busy            | 46.0 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 35.9 ms        
Uztelecom       | Tashkent, UZ (10G)        | 697 Mbits/sec   | 150 Mbits/sec   | 95.7 ms        
Clouvider       | NYC, NY, US (10G)         | 35.9 Mbits/sec  | 44.0 Mbits/sec  | 174 ms         
Clouvider       | Dallas, TX, US (10G)      | 26.2 Mbits/sec  | 32.5 Mbits/sec  | 172 ms         
Clouvider       | Los Angeles, CA, US (10G) | 22.1 Mbits/sec  | 25.9 Mbits/sec  | 172 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2652                          
Multi Core      | 4644                          
Full Test       | https://browser.geekbench.com/v6/cpu/2553291

YABS completed in 12 min 35 sec
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 4192.104 MHz
 CPU 缓存          : L1: 256.00 KB / L2: 1.00 MB / L3: 16.00 MB
 硬盘空间          : 2.75 GiB / 58.98 GiB
 启动盘路径        : /dev/vda1
 内存              : 160.44 MiB / 3.84 GiB
 Swap              : 0 KiB / 1024.00 MiB
 系统在线时间      : 0 days, 0 hour 15 min
 负载              : 0.33, 0.40, 0.19
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-21-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS210644 AEZA GROUP Ltd
 IPV4 位置         : Korpilahti / Central Finland / FI
 IPV6 ASN          : AS210644 AEZA GROUP Ltd
 IPV6 位置         : Amsterdam / North Holland
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           5676 Scores
 2 线程测试(多核)得分:          11328 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          73382.48 MB/s
 单线程写测试:          33130.64 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         42.6 MB/s (10.40 IOPS, 2.46s))          42.6 MB/s (10400 IOPS, 2.46s)
 1GB-1M Block           4.3 GB/s (4118 IOPS, 0.24s)             4.3 GB/s (4103 IOPS, 0.24s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 40.02 MB/s   (10.0k) | 656.51 MB/s  (10.2k)
Write      | 40.12 MB/s   (10.0k) | 659.96 MB/s  (10.3k)
Total      | 80.15 MB/s   (20.0k) | 1.31 GB/s    (20.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.90 GB/s     (5.6k) | 3.21 GB/s     (3.1k)
Write      | 3.06 GB/s     (5.9k) | 3.43 GB/s     (3.3k)
Total      | 5.96 GB/s    (11.6k) | 6.64 GB/s     (6.4k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: GIGANET
视频缓存节点地域: KBP(KBP9)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 德国汉堡(HAM11S06)
Youtube识别地域: 俄罗斯联邦(RU)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：芬兰
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：芬兰
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：芬兰区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：芬兰区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: FI)
 HotStar:                               No
 Disney+:                               Yes (Region: FI)
 Netflix:                               Yes (Region: FI)
 YouTube Premium:                       Failed
 Amazon Prime Video:                    Yes (Region: FI)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   INTL
 Viu.com:                               No
 YouTube CDN:                           GIGANET in Kiev 
 Netflix Preferred CDN:                 Helsinki  
 Spotify Registration:                  No
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: NL)
 Netflix:                               Yes (Region: FI)
 YouTube Premium:                       No 
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Hamburg 
 Netflix Preferred CDN:                 Helsinki  
 Spotify Registration:                  No
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【FI】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 72②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  business⑨  
  公司类型(company_type):hosting①  hosting⑧  
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
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
  qq邮箱: Yes
------以下为IPV6检测------
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: FI 城市: Korpilahti 服务商: AS210644 AEZA GROUP Ltd
北京电信 219.141.136.12  测试超时
北京联通 202.106.50.1    测试超时
北京移动 221.179.155.161 测试超时
上海电信 202.96.209.133  测试超时
上海联通 210.22.97.1     测试超时
上海移动 211.136.112.200 测试超时
广州电信 58.60.188.222   测试超时
广州联通 210.21.196.6    测试超时
广州移动 120.196.165.24  测试超时
成都电信 61.139.2.69     测试超时
成都联通 119.6.6.6       测试超时
成都移动 211.137.96.205  测试超时
2023/09/10 08:38:52 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.08 ms         * RFC1918
6.17 ms         AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
6.30 ms         AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
283.05 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.11 ms         * RFC1918
7.08 ms         AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
7.27 ms         AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
326.55 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.10 ms         * RFC1918
6.17 ms         AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
6.22 ms         AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
322.95 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    30.90 Mbps      78.09 Mbps      27.53    0.0%
法兰克福         786.80 Mbps     627.38 Mbps     29.06    0.0%
洛杉矶           418.94 Mbps     506.87 Mbps     189.16   1.3%
移动Lanzhou      490.06 Mbps     9.17 Mbps       378.54   NULL
------------------------------------------------------------------------
 总共花费      : 4 分 37 秒
 时间          : Sun Sep 10 08:41:38 MSK 2023
------------------------------------------------------------------------
```

### byte-unixbench 性能测试

```
========================================================================
BYTE UNIX Benchmarks (Version 5.1.3)

System: overt-plant.aeza.network: GNU/Linux
OS: GNU/Linux -- 5.10.0-21-amd64 -- #1 SMP Debian 5.10.162-1 (2023-01-21)
Machine: x86_64 (unknown)
Language: en_US.utf8 (charmap="UTF-8", collate="UTF-8")
CPU 0: AMD Ryzen 9 7950X3D 16-Core Processor (8384.2 bogomips)
Hyper-Threading, x86-64, MMX, AMD MMX, Physical Address Ext, SYSENTER/SYSEXIT, SYSCALL/SYSRET
CPU 1: AMD Ryzen 9 7950X3D 16-Core Processor (8384.2 bogomips)
Hyper-Threading, x86-64, MMX, AMD MMX, Physical Address Ext, SYSENTER/SYSEXIT, SYSCALL/SYSRET
08:48:02 up 26 min, 1 user, load average: 0.43, 0.49, 0.33; runlevel 5

Benchmark Run: Sun Sep 10 2023 08:48:02 - 09:15:57
2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables 71600995.5 lps (10.0 s, 7 samples)
Double-Precision Whetstone 11395.8 MWIPS (10.0 s, 7 samples)
Execl Throughput 10303.9 lps (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks 2426483.8 KBps (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks 660701.8 KBps (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks 7743450.3 KBps (30.0 s, 2 samples)
Pipe Throughput 4203526.6 lps (10.0 s, 7 samples)
Pipe-based Context Switching 99864.1 lps (10.0 s, 7 samples)
Process Creation 17611.6 lps (30.0 s, 2 samples)
Shell Scripts (1 concurrent) 23025.3 lpm (60.0 s, 2 samples)
Shell Scripts (8 concurrent) 4101.7 lpm (60.0 s, 2 samples)
System Call Overhead 4977991.1 lps (10.0 s, 7 samples)

System Benchmarks Index Values BASELINE RESULT INDEX
Dhrystone 2 using register variables 116700.0 71600995.5 6135.5
Double-Precision Whetstone 55.0 11395.8 2072.0
Execl Throughput 43.0 10303.9 2396.3
File Copy 1024 bufsize 2000 maxblocks 3960.0 2426483.8 6127.5
File Copy 256 bufsize 500 maxblocks 1655.0 660701.8 3992.2
File Copy 4096 bufsize 8000 maxblocks 5800.0 7743450.3 13350.8
Pipe Throughput 12440.0 4203526.6 3379.0
Pipe-based Context Switching 4000.0 99864.1 249.7
Process Creation 126.0 17611.6 1397.7
Shell Scripts (1 concurrent) 42.4 23025.3 5430.5
Shell Scripts (8 concurrent) 6.0 4101.7 6836.2
System Call Overhead 15000.0 4977991.1 3318.7
========
System Benchmarks Index Score 3260.8

Benchmark Run: Sun Sep 10 2023 09:15:57 - 09:43:53
2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables 144090587.8 lps (10.0 s, 7 samples)
Double-Precision Whetstone 23134.9 MWIPS (10.0 s, 7 samples)
Execl Throughput 16371.4 lps (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks 1770854.0 KBps (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks 469473.1 KBps (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks 7125527.1 KBps (30.0 s, 2 samples)
Pipe Throughput 8394510.7 lps (10.0 s, 7 samples)
Pipe-based Context Switching 796406.5 lps (10.0 s, 7 samples)
Process Creation 38689.8 lps (30.0 s, 2 samples)
Shell Scripts (1 concurrent) 29097.3 lpm (60.0 s, 2 samples)
Shell Scripts (8 concurrent) 4711.0 lpm (60.0 s, 2 samples)
System Call Overhead 4038203.5 lps (10.0 s, 7 samples)

System Benchmarks Index Values BASELINE RESULT INDEX
Dhrystone 2 using register variables 116700.0 144090587.8 12347.1
Double-Precision Whetstone 55.0 23134.9 4206.3
Execl Throughput 43.0 16371.4 3807.3
File Copy 1024 bufsize 2000 maxblocks 3960.0 1770854.0 4471.9
File Copy 256 bufsize 500 maxblocks 1655.0 469473.1 2836.7
File Copy 4096 bufsize 8000 maxblocks 5800.0 7125527.1 12285.4
Pipe Throughput 12440.0 8394510.7 6748.0
Pipe-based Context Switching 4000.0 796406.5 1991.0
Process Creation 126.0 38689.8 3070.6
Shell Scripts (1 concurrent) 42.4 29097.3 6862.6
Shell Scripts (8 concurrent) 6.0 4711.0 7851.7
System Call Overhead 15000.0 4038203.5 2692.1
========
System Benchmarks Index Score 4884.5
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD Ryzen 9 7950X3D 16-Core Processor (x86_64)
2 cores @ 4192 MHz  |  3.8 GiB RAM
Number of Processes: 2  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          6642
  Integer Math                     15501 Million Operations/s
  Floating Point Math              9434 Million Operations/s
  Prime Numbers                    58.6 Million Primes/s
  Sorting                          10159 Thousand Strings/s
  Encryption                       3530 MB/s
  Compression                      66326 KB/s
  CPU Single Threaded              3899 Million Operations/s
  Physics                          923 Frames/s
  Extended Instructions (SSE)      5580 Million Matrices/s

Memory Mark:                       2404
  Database Operations              2442 Thousand Operations/s
  Memory Read Cached               37117 MB/s
  Memory Read Uncached             33380 MB/s
  Memory Write                     20666 MB/s
  Available RAM                    3621 Megabytes
  Memory Latency                   62 Nanoseconds
  Memory Threaded                  49914 MB/s
--------------------------------------------------------------------------
```

### SpeedTest

```

   Speedtest by Ookla

      Server: 31173 Services AB - Amsterdam (id: 23094)
         ISP: AEZA GROUP Ltd
Idle Latency:    28.82 ms   (jitter: 0.48ms, low: 28.36ms, high: 29.47ms)
    Download:   820.02 Mbps (data used: 978.3 MB)                                                   
                 66.63 ms   (jitter: 35.92ms, low: 27.30ms, high: 326.54ms)
      Upload:   786.34 Mbps (data used: 913.1 MB)                                                   
                 27.81 ms   (jitter: 0.22ms, low: 27.32ms, high: 31.43ms)
 Packet Loss:     0.0%
  Result URL: https://www.speedtest.net/result/c/4f131512-56ad-4c6e-9546-64cd9201e9c1
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-63-1024x394.png)

### network-speed.xyz

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
 CPU Model          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU Cores          : 2 @ 4192.104 MHz
 CPU Cache          : 512 KB
 AES-NI             : ✔ Enabled
 VM-x/AMD-V         : ❌ Disabled
 Total Disk         : 59.0 GB (5.1 GB Used)
 Total RAM          : 3.8 GB (103.3 MB Used)
 Total Swap         : 1024.0 MB (0 Used)
 System uptime      : 0 days, 1 hour 27 min
 Load average       : 0.08, 2.82, 3.06
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-21-amd64
 Virtualization     : KVM
---------------------------------------------------------------------------
 Basic Network Info
---------------------------------------------------------------------------
 Primary Network    : IPv4
 ISP                : AEZA GROUP Ltd
 ASN                : AS210644 AEZA GROUP Ltd
 Host               : Aeza Group LLC
 Location           : Helsinki, Uusimaa-18, Finland
 Location (IPv4)    : Korpilahti, Central Finland, FI
---------------------------------------------------------------------------
 Speedtest.net (Region: GLOBAL)
---------------------------------------------------------------------------
 Location         Latency     Loss    DL Speed       UP Speed       Server      

 ISP: AEZA GROUP Ltd 

 Nearest          26.61 ms    0.0%    77.19 Mbps     30.67 Mbps     RETN - Amsterdam 

 Kochi, IN        220.00 ms   1.3%    404.30 Mbps    339.59 Mbps    Asianet Broadband - Cochin 
 Bangalore, IN    192.93 ms   1.3%    466.89 Mbps    378.39 Mbps    Bharti Airtel Ltd - Bangalore 
 Chennai, IN      216.32 ms   N/A     421.24 Mbps    333.21 Mbps    Jio - Chennai 
 Mumbai, IN       157.45 ms   0.9%    400.52 Mbps    494.63 Mbps    i3D.net - Mumbai 
 Delhi, IN        173.71 ms   1.4%    451.99 Mbps    434.66 Mbps    Tata Teleservices Ltd - New Delhi 

 Seattle, US      155.07 ms   1.4%    430.25 Mbps    519.92 Mbps    Ziply Fiber - Seattle, WA 
 Los Angeles, US  160.20 ms   2.0%    382.58 Mbps    363.93 Mbps    ReliableSite Hosting - Los Angeles, CA 
 Dallas, US       180.41 ms   0.0%    492.53 Mbps    461.95 Mbps    Hivelocity - Dallas, TX 
 Miami, US        196.70 ms   0.0%    506.00 Mbps    403.26 Mbps    AT&T - Miami, FL 
 New York, US     180.88 ms   0.0%    821.51 Mbps    448.01 Mbps    GSL Networks - New York, NY 
 Toronto, CA      194.43 ms   0.0%    568.55 Mbps    415.44 Mbps    Rogers - Toronto, ON 

 London, UK       37.10 ms    1.4%    786.90 Mbps    754.35 Mbps    VeloxServ Communications - London 
 Amsterdam, NL    38.16 ms    0.0%    92.48 Mbps     50.87 Mbps     Clouvider Ltd - Amsterdam 
 Paris, FR        38.12 ms    N/A     808.78 Mbps    777.14 Mbps    Axione - Paris 
 Frankfurt, DE    24.15 ms    0.0%    734.80 Mbps    783.95 Mbps    23M GmbH - Frankfurt am Main 
 Warsaw, PL       31.76 ms    0.9%    568.82 Mbps    740.95 Mbps    UPC Polska - Warszawa 
 Bucharest, RO    58.57 ms    0.0%    664.17 Mbps    789.05 Mbps    Vodafone Romania Fixed – Bucharest - Bucharest 

 Jeddah, SA       101.05 ms   1.0%    217.53 Mbps    667.61 Mbps    Saudi Telecom Company 
 Dubai, AE        155.72 ms   0.0%    705.91 Mbps    531.35 Mbps    du - Dubai  
 Fujairah, AE     140.84 ms   0.0%    821.05 Mbps    562.87 Mbps    ETISALAT-UAE - Fujairah 

 Tokyo, JP        269.57 ms   N/A     548.11 Mbps    199.67 Mbps    fdcservers.net - Tokyo 
 Shenyang, CU-CN  302.52 ms   28.1%   37.80 Mbps     23.83 Mbps     Unicom - Shenyang 
 Nanjing, CT-CN   191.61 ms   1.3%    396.55 Mbps    46.39 Mbps     China Telecom JiangSu 5G - Nanjing 
 Hong Kong, CN    261.19 ms   N/A     463.63 Mbps    302.99 Mbps    STC - Hong Kong 
 Singapore, SG    284.01 ms   1.0%    406.48 Mbps    73.36 Mbps     i3D.net - Singapore 
 Jakarta, ID      202.61 ms   1.3%    413.33 Mbps    353.23 Mbps    PT. Telekomunikasi Indonesia - Jakarta 
---------------------------------------------------------------------------
 Avg DL Speed       : 484.80 Mbps
 Avg UL Speed       : 417.83 Mbps

 Total DL Data      : 17.18 GB
 Total UL Data      : 15.42 GB
 Total Data         : 32.61 GB
---------------------------------------------------------------------------
 Duration           : 13 min 32 sec
 System Time        : 10/09/2023 - 10:02:37 MSK
 Total Script Runs  : 22856
---------------------------------------------------------------------------
 Result             : https://result.network-speed.xyz/r/1694329358_F4VUJR_GLOBAL.txt
---------------------------------------------------------------------------
```

### 流媒体测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-62-1024x821.png)

### 四网回程测试

```
----------------------------------------------------------------------
北京电信
traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  10.0.0.1  0.06 ms  http: 403  http: 403
 2  edge-sto2.aeza.network (121.127.46.113)  7.06 ms  http: 403  http: 403
 3  unn-121-127-46-125.datapacket.com (121.127.46.125)  7.25 ms  http: 403  http: 403
 4  *
 5  bj141-147-210.bjtelecom.net (219.141.147.210)  182.06 ms  http: 403  http: 403

----------------------------------------------------------------------
上海电信
traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  10.0.0.1  0.05 ms  http: 403  http: 403
 2  edge-sto2.aeza.network (121.127.46.113)  6.98 ms  http: 403  http: 403
 3  unn-121-127-46-125.datapacket.com (121.127.46.125)  7.40 ms  http: 403  http: 403
 4  *
 5  *
 6  *
 7  *
 8  *
 9  *
10  *
11  *
12  *
13  *
14  *
15  ns-pd.online.sh.cn (202.96.209.133)  297.89 ms  http: 403  http: 403

----------------------------------------------------------------------
深圳电信
traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  10.0.0.1  0.11 ms  http: 403  http: 403
 2  edge-sto1.aeza.network (121.127.46.114)  6.16 ms  http: 403  http: 403
 3  unn-121-127-46-125.datapacket.com (121.127.46.125)  6.30 ms  http: 403  http: 403
 4  vl203.sto-itx-core-1.cdn77.com (185.156.45.90)  6.28 ms  http: 403  http: 403
 5  s-b3-link.ip.twelve99.net (62.115.191.201)  6.67 ms  http: 403  http: 403
 6  s-bb2-link.ip.twelve99.net (62.115.118.108)  7.49 ms  http: 403  http: 403
 7  ffm-bb2-link.ip.twelve99.net (62.115.138.105)  23.74 ms  http: 403  http: 403
 8  ffm-b11-link.ip.twelve99.net (62.115.124.119)  24.20 ms  http: 403  http: 403
 9  202.97.58.149  74.81 ms  http: 403  http: 403
10  202.97.89.109  271.97 ms  http: 403  http: 403
11  202.97.12.22  274.08 ms  http: 403  http: 403
12  *
13  *
14  *
15  58.60.188.222  283.30 ms  http: 403  http: 403

----------------------------------------------------------------------
北京联通
traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  10.0.0.1  0.08 ms  http: 403  http: 403
 2  edge-sto1.aeza.network (121.127.46.114)  6.11 ms  http: 403  http: 403
 3  unn-121-127-46-125.datapacket.com (121.127.46.125)  6.36 ms  http: 403  http: 403
 4  vl203.sto-itx-core-1.cdn77.com (185.156.45.90)  6.24 ms  http: 403  http: 403
 5  202.106.50.1  289.73 ms  http: 403  http: 403

----------------------------------------------------------------------
上海联通
traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  10.0.0.1  0.05 ms  http: 403  http: 403
 2  edge-sto2.aeza.network (121.127.46.113)  8.32 ms  http: 403  http: 403
 3  unn-121-127-46-124.datapacket.com (121.127.46.124)  7.16 ms  http: 403  http: 403
 4  vl201.sto-itx-core-1.cdn77.com (185.156.45.88)  7.85 ms  http: 403  http: 403
 5  210.22.97.1  339.73 ms  http: 403  http: 403

----------------------------------------------------------------------
深圳联通
traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  10.0.0.1  0.07 ms  http: 403  http: 403
 2  edge-sto2.aeza.network (121.127.46.113)  7.17 ms  http: 403  http: 403
 3  unn-121-127-46-125.datapacket.com (121.127.46.125)  7.15 ms  http: 403  http: 403
 4  vl203.sto-itx-core-1.cdn77.com (185.156.45.90)  7.21 ms  http: 403  http: 403
 5  s-b3-link.ip.twelve99.net (62.115.191.201)  8.10 ms  http: 403  http: 403
 6  s-bb1-link.ip.twelve99.net (62.115.118.106)  8.11 ms  http: 403  http: 403
 7  *
 8  ffm-b11-link.ip.twelve99.net (62.115.124.117)  26.37 ms  http: 403  http: 403
 9  *
10  219.158.21.113  327.36 ms  http: 403  http: 403
11  219.158.98.93  333.55 ms  http: 403  http: 403
12  219.158.19.65  326.75 ms  http: 403  http: 403
13  120.82.0.162  328.22 ms  http: 403  http: 403
14  120.80.144.34  333.50 ms  http: 403  http: 403
15  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  331.79 ms  http: 403  http: 403

----------------------------------------------------------------------
北京移动
traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  10.0.0.1  0.08 ms  http: 403  http: 403
 2  edge-sto1.aeza.network (121.127.46.114)  6.12 ms  http: 403  http: 403
 3  unn-121-127-46-125.datapacket.com (121.127.46.125)  6.16 ms  http: 403  http: 403
 4  vl203.sto-itx-core-1.cdn77.com (185.156.45.90)  6.28 ms  http: 403  http: 403
 5  ae5-0.sth10.core-backbone.com (5.56.18.5)  6.84 ms  http: 403  http: 403
 6  ae2-2021.fra20.core-backbone.com (80.255.14.6)  22.65 ms  http: 403  http: 403
 7  ipv4.de-cix.fra.de.as58453.chinamobile.com (80.81.195.121)  36.81 ms  http: 403  http: 403
 8  223.120.10.85  36.63 ms  http: 403  http: 403
 9  223.120.16.30  351.77 ms  http: 403  http: 403
10  221.183.55.106  358.94 ms  http: 403  http: 403
11  221.183.46.250  353.86 ms  http: 403  http: 403
12  221.183.89.102  331.58 ms  http: 403  http: 403
13  221.183.46.178  343.33 ms  http: 403  http: 403
14  221.183.130.142  355.68 ms  http: 403  http: 403
15  cachedns03.bj.chinamobile.com (221.179.155.161)  348.31 ms  http: 403  http: 403

----------------------------------------------------------------------
上海移动
traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  10.0.0.1  0.10 ms  http: 403  http: 403
 2  edge-sto2.aeza.network (121.127.46.113)  7.18 ms  http: 403  http: 403
 3  unn-121-127-46-124.datapacket.com (121.127.46.124)  7.28 ms  http: 403  http: 403
 4  vl201.sto-itx-core-1.cdn77.com (185.156.45.88)  7.30 ms  http: 403  http: 403
 5  ae5-0.sth10.core-backbone.com (5.56.18.5)  7.96 ms  http: 403  http: 403
 6  ae2-2021.fra20.core-backbone.com (80.255.14.6)  23.55 ms  http: 403  http: 403
 7  ipv4.de-cix.fra.de.as58453.chinamobile.com (80.81.195.121)  43.16 ms  http: 403  http: 403
 8  223.120.10.14  39.53 ms  http: 403  http: 403
 9  223.120.16.150  316.67 ms  http: 403  http: 403
10  221.183.89.170  324.49 ms  http: 403  http: 403
11  221.183.89.33  330.56 ms  http: 403  http: 403
12  *
13  *
14  221.181.125.138  317.04 ms  http: 403  http: 403
15  211.136.112.252  330.26 ms  http: 403  http: 403
16  211.136.112.200  323.44 ms  http: 403  http: 403

----------------------------------------------------------------------
深圳移动
traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  10.0.0.1  0.05 ms  http: 403  http: 403
 2  edge-sto1.aeza.network (121.127.46.114)  6.08 ms  http: 403  http: 403
 3  unn-121-127-46-124.datapacket.com (121.127.46.124)  6.43 ms  http: 403  http: 403
 4  vl201.sto-itx-core-1.cdn77.com (185.156.45.88)  6.23 ms  http: 403  http: 403
 5  ae5-0.sth10.core-backbone.com (5.56.18.5)  6.87 ms  http: 403  http: 403
 6  ae2-2021.fra20.core-backbone.com (80.255.14.6)  22.67 ms  http: 403  http: 403
 7  ipv4.de-cix.fra.de.as58453.chinamobile.com (80.81.195.121)  37.34 ms  http: 403  http: 403
 8  223.120.10.85  36.66 ms  http: 403  http: 403
 9  223.120.15.226  293.80 ms  http: 403  http: 403
10  221.183.55.82  317.97 ms  http: 403  http: 403
11  221.183.92.21  322.87 ms  http: 403  http: 403
12  *
13  221.183.71.78  320.86 ms  http: 403  http: 403
14  221.183.110.166  325.53 ms  http: 403  http: 403
15  ns6.gd.cnmobile.net (120.196.165.24)  323.00 ms  http: 403  http: 403

----------------------------------------------------------------------
成都教育网
traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  10.0.0.1  0.09 ms  http: 403  http: 403
 2  edge-sto1.aeza.network (121.127.46.114)  6.05 ms  http: 403  http: 403
 3  unn-121-127-46-124.datapacket.com (121.127.46.124)  6.22 ms  http: 403  http: 403
 4  vl201.sto-itx-core-1.cdn77.com (185.156.45.88)  6.26 ms  http: 403  http: 403
 5  ae5-0.sth10.core-backbone.com (5.56.18.5)  6.76 ms  http: 403  http: 403
 6  ae2-2021.fra20.core-backbone.com (80.255.14.6)  22.76 ms  http: 403  http: 403
 7  ipv4.de-cix.fra.de.as58453.chinamobile.com (80.81.195.121)  47.88 ms  http: 403  http: 403
 8  223.120.10.85  40.88 ms  http: 403  http: 403
 9  223.120.15.174  205.49 ms  http: 403  http: 403
10  *
11  223.120.3.86  205.62 ms  http: 403  http: 403
12  223.119.81.94  266.50 ms  http: 403  http: 403
13  101.4.114.221  317.83 ms  http: 403  http: 403
14  101.4.114.129  307.56 ms  http: 403  http: 403
15  *
16  101.4.117.81  299.89 ms  http: 403  http: 403
17  *
18  101.4.112.18  328.25 ms  http: 403  http: 403
19  101.4.116.158  327.65 ms  http: 403  http: 403
20  *
21  *
22  *
23  *
24  202.112.14.151  334.53 ms  http: 403  http: 403

---------------------------------------------------------------------- 
```

### 国内延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-57-1024x474.png)

### 全球延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-58.png)

## 总结

性能很强，但是网络貌似很糟糕，经常容易开出被墙IP
