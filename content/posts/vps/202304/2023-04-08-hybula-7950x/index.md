---
title: "Hybula 7950x 荷兰24欧"
date: "2023-04-08"
categories: 
  - "vps"
  - "eu"
tags: 
  - "eu"
---

![](https://catcat.blog/wp-content/uploads/2023/10/image-164.png)

powered by AMD Ryzen 7950X, DDR5 ECC, U.2 PCIe 4.0 NVMe drives, and dual 10G uplinks.

### offer

```
- 1x Ryzen 7950X vCPU
- 25 GB Enterprise U.2 NVMe SSD (PCIe 4.0)
- 2 GB DDR5 ECC 4800 MT/s
- 2500 GB Traffic
- 1 Gbit/s Uplink
- 1x IPv4 Address
- /64 IPv6 Subnet
- Advanced DDoS Shield L3/4 by CDN77
- Located in the Netherlands
- Free 1x Manual Backup
- VirtFusion Control Panel
ps:亚洲因延迟问题不允许退款
```

## 官网

[https://www.hybula.com/](https://www.hybula.com/)

### 测试ip

**Facility**: InterDC Doetinchem  
**Test IPv4**: 2.58.57.100  
**Test IPv6**: 2a09:e240:22:2::100  
looking glass : [https://lg-nl-dtc.hybula.net/](https://lg-nl-dtc.hybula.net/)

## 测评配置（2h2g50gb）

### 系统

![](https://catcat.blog/wp-content/uploads/2023/10/image-154.png)

### cpu测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-155.png)

```
Geekbench 4 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 9298                          
Multi Core      | 8951                          
Full Test       | https://browser.geekbench.com/v4/cpu/16739481

Geekbench 5 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2246                          
Multi Core      | 2241                          
Full Test       | https://browser.geekbench.com/v5/cpu/21023036

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2850                          
Multi Core      | 2945                          
Full Test       | https://browser.geekbench.com/v6/cpu/841083
```

### 内存测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-156.png)

### 硬盘读写测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-157.png)

### 流媒体解锁测试

```
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS15S46)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS17S06)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：老挝
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：荷兰
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口所在地区即将开通DisneyPlus，尽请期待哦！
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：荷兰区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
---------------流媒体解锁--感谢RegionRestrictionCheck开源-------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					Yes (Region: NL)
 HotStar:				No
 Disney+:				Yes (Region: NL)
 Netflix:				Yes (Region: LA)
 YouTube Premium:			Yes (Region: NL)
 Amazon Prime Video:			Yes (Region: NL)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			LA
 Viu.com:				No
 YouTube CDN:				Amsterdam 
 Netflix Preferred CDN:			Amsterdam  
 Spotify Registration:			Yes (Region: NL)
 Steam Currency:			EUR
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				No
 Disney+:				Yes (Region: NL)
 Netflix:				Yes (Region: NL)
 YouTube Premium:			Yes (Region: NL)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Amsterdam 
 Netflix Preferred CDN:			Frankfurt  
 Spotify Registration:			Yes (Region: NL)
 Steam Currency:			Failed (Network Connection)
=======================================
```

### Openai解锁测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-158.png)

### 回程测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-159.png)

### 网络测速

![](https://catcat.blog/wp-content/uploads/2023/10/image-160.png)

### 全球延迟测速

![](https://catcat.blog/wp-content/uploads/2023/10/image-161.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-162.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-163.png)

## Yabs

```
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2023-04-23                    #
# https://github.com/masonr/yet-another-bench-script #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

Fri 23 Jun 2023 11:21:09 PM CST

Basic System Information:
---------------------------------
Uptime     : 32 days, 20 hours, 0 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 2 @ 4499.968 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 0.0 KiB
Disk       : 50.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-20-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Hybula B.V.
ASN        : AS35133 Hybula B.V.
Host       : Hybula B.V
Location   : Amsterdam, North Holland (NH)
Country    : Netherlands

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 762.70 MB/s (190.6k) | 3.99 GB/s    (62.3k)
Write      | 764.71 MB/s (191.1k) | 4.01 GB/s    (62.6k)
Total      | 1.52 GB/s   (381.8k) | 8.00 GB/s   (125.0k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.99 GB/s     (5.8k) | 3.67 GB/s     (3.5k)
Write      | 3.14 GB/s     (6.1k) | 3.92 GB/s     (3.8k)
Total      | 6.14 GB/s    (11.9k) | 7.59 GB/s     (7.4k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.09 Gbits/sec  | busy            | 9.10 ms        
Scaleway        | Paris, FR (10G)           | 1.09 Gbits/sec  | 953 Mbits/sec   | 11.1 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 2.86 ms        
Uztelecom       | Tashkent, UZ (10G)        | 1.02 Gbits/sec  | 732 Mbits/sec   | 91.3 ms        
Clouvider       | NYC, NY, US (10G)         | 1.03 Gbits/sec  | busy            | 86.2 ms        
Clouvider       | Dallas, TX, US (10G)      | 994 Mbits/sec   | 464 Mbits/sec   | 128 ms         
Clouvider       | Los Angeles, CA, US (10G) | busy            | 367 Mbits/sec   | 151 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.09 Gbits/sec  | 942 Mbits/sec   | 9.14 ms        
Scaleway        | Paris, FR (10G)           | 1.09 Gbits/sec  | 940 Mbits/sec   | 14.9 ms        
NovoServe       | North Holland, NL (40G)   | 1.09 Gbits/sec  | 942 Mbits/sec   | 2.78 ms        
Uztelecom       | Tashkent, UZ (10G)        | 982 Mbits/sec   | 771 Mbits/sec   | 91.3 ms        
Clouvider       | NYC, NY, US (10G)         | busy            | 464 Mbits/sec   | 86.2 ms        
Clouvider       | Dallas, TX, US (10G)      | 969 Mbits/sec   | 376 Mbits/sec   | 127 ms         
Clouvider       | Los Angeles, CA, US (10G) | 926 Mbits/sec   | 387 Mbits/sec   | 151 ms 

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |       
Single Core     | 2837                        
Multi Core      | 5068                          
Full Test       | https://browser.geekbench.com/v6/cpu/1692070
```

## Bench脚本测试

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X 16-Core Processor
 CPU Cores          : 2 @ 4499.968 MHz
 CPU Cache          : 1024 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 50.0 GB (3.6 GB Used)
 Total Mem          : 1.9 GB (203.2 MB Used)
 System uptime      : 32 days, 0 hour 41 min
 Load average       : 0.00, 0.03, 0.07
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-20-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS35133 Hybula B.V.
 Location           : Amsterdam / NL
 Region             : North Holland
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.0 GB/s
 I/O Speed(2nd run) : 1.1 GB/s
 I/O Speed(3rd run) : 1.1 GB/s
 I/O Speed(average) : 1092.3 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    996.05 Mbps       943.08 Mbps         2.15 ms     
 Los Angeles, US  601.49 Mbps       894.83 Mbps         145.77 ms   
 Dallas, US       709.67 Mbps       942.11 Mbps         118.25 ms   
 Montreal, CA     211.60 Mbps       876.76 Mbps         90.08 ms    
 Paris, FR        987.53 Mbps       942.07 Mbps         14.09 ms    
 Amsterdam, NL    973.39 Mbps       955.50 Mbps         8.97 ms     
 Shanghai, CN     296.69 Mbps       731.70 Mbps         254.01 ms   
 Nanjing, CN      1.51 Mbps         645.94 Mbps         211.71 ms   
 Hongkong, CN     2.62 Mbps         540.40 Mbps         414.59 ms   
 Singapore, SG    21.15 Mbps        738.51 Mbps         174.33 ms   
 Tokyo, JP        1.99 Mbps         778.98 Mbps         231.19 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 34 sec
 Timestamp          : 2023-06-23 23:47:49 CST
----------------------------------------------------------------------
```

### 2023年9月21日测试

```
Basic System Information:
---------------------------------
Uptime     : 17 days, 2 hours, 15 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 2 @ 4499.968 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 0.0 KiB
Disk       : 50.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-20-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Hybula B.V.
ASN        : AS35133 Hybula B.V.
Host       : Hybula B.V
Location   : Amsterdam, North Holland (NH)
Country    : Netherlands

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 649.82 MB/s (162.4k) | 3.37 GB/s    (52.7k)
Write      | 651.54 MB/s (162.8k) | 3.39 GB/s    (53.0k)
Total      | 1.30 GB/s   (325.3k) | 6.77 GB/s   (105.8k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.29 GB/s     (6.4k) | 3.49 GB/s     (3.4k)
Write      | 3.47 GB/s     (6.7k) | 3.72 GB/s     (3.6k)
Total      | 6.76 GB/s    (13.2k) | 7.21 GB/s     (7.0k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.09 Gbits/sec  | 955 Mbits/sec   | 7.50 ms        
Scaleway        | Paris, FR (10G)           | 1.06 Gbits/sec  | busy            | 10.7 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 2.60 ms        
Uztelecom       | Tashkent, UZ (10G)        | 1.02 Gbits/sec  | 824 Mbits/sec   | 90.0 ms        
Clouvider       | NYC, NY, US (10G)         | 525 Mbits/sec   | busy            | 77.3 ms        
Clouvider       | Dallas, TX, US (10G)      | 990 Mbits/sec   | 398 Mbits/sec   | 115 ms         
Clouvider       | Los Angeles, CA, US (10G) | 706 Mbits/sec   | 212 Mbits/sec   | 142 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.09 Gbits/sec  | 941 Mbits/sec   | 7.50 ms        
Scaleway        | Paris, FR (10G)           | busy            | 940 Mbits/sec   | 11.2 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 2.64 ms        
Uztelecom       | Tashkent, UZ (10G)        | 1.01 Gbits/sec  | 804 Mbits/sec   | 89.7 ms        
Clouvider       | NYC, NY, US (10G)         | 904 Mbits/sec   | 153 Mbits/sec   | 78.3 ms        
Clouvider       | Dallas, TX, US (10G)      | 529 Mbits/sec   | 142 Mbits/sec   | 115 ms         
Clouvider       | Los Angeles, CA, US (10G) | 802 Mbits/sec   | 543 Mbits/sec   | 142 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2665                          
Multi Core      | 4852                          
Full Test       | https://browser.geekbench.com/v6/cpu/2697512

YABS completed in 11 min 15 sec
```

### 2023年10月1日测试

```
Basic System Information:
---------------------------------
Uptime     : 27 days, 3 hours, 1 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 2 @ 4499.968 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 0.0 KiB
Disk       : 49.9 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-9-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Hybula B.V.
ASN        : AS35133 Hybula B.V.
Host       : Hybula B.V
Location   : Amsterdam, North Holland (NH)
Country    : Netherlands

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 624.63 MB/s (156.1k) | 2.57 GB/s    (40.2k)
Write      | 626.27 MB/s (156.5k) | 2.59 GB/s    (40.5k)
Total      | 1.25 GB/s   (312.7k) | 5.17 GB/s    (80.8k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.80 GB/s     (5.4k) | 3.43 GB/s     (3.3k)
Write      | 2.95 GB/s     (5.7k) | 3.66 GB/s     (3.5k)
Total      | 5.76 GB/s    (11.2k) | 7.10 GB/s     (6.9k)

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2784                          
Multi Core      | 4868                          
Full Test       | https://browser.geekbench.com/v6/cpu/2855061
```

### 2023年10月7日测试

```
Basic System Information:
---------------------------------
Uptime     : 5 days, 21 hours, 20 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 2 @ 4499.968 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 0.0 KiB
Disk       : 49.9 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-9-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Hybula B.V.
ASN        : AS35133 Hybula B.V.
Host       : Hybula B.V
Location   : Amsterdam, North Holland (NH)
Country    : Netherlands

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 596.01 MB/s (149.0k) | 3.94 GB/s    (61.6k)
Write      | 597.58 MB/s (149.3k) | 3.96 GB/s    (61.9k)
Total      | 1.19 GB/s   (298.3k) | 7.91 GB/s   (123.6k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.86 GB/s     (7.5k) | 3.76 GB/s     (3.6k)
Write      | 4.06 GB/s     (7.9k) | 4.01 GB/s     (3.9k)
Total      | 7.92 GB/s    (15.4k) | 7.78 GB/s     (7.5k)

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2747                          
Multi Core      | 4776                          
Full Test       | https://browser.geekbench.com/v6/cpu/2960473
```

### sysbench测试

#### CPU Performance

指定 CPU 线程最大素数为 20000，多进程为4，运行 60s 所得测量值

```
root@catcat:~# sysbench cpu --cpu-max-prime=20000 --threads=4 --time=60 run
sysbench 1.0.20 (using system LuaJIT 2.1.0-beta3)

Running the test with following options:
Number of threads: 4
Initializing random number generator from current time


Prime numbers limit: 20000

Initializing worker threads...

Threads started!

CPU speed:
    events per second:  4686.45

General statistics:
    total time:                          60.0006s
    total number of events:              281191

Latency (ms):
         min:                                    0.40
         avg:                                    0.85
         max:                                   25.25
         95th percentile:                        4.41
         sum:                               239874.41

Threads fairness:
    events (avg/stddev):           70297.7500/139.31
    execution time (avg/stddev):   59.9686/0.01
```

指定 CPU 线程最大素数为 20000，单进程测试，运行 60s 所得测量值

```
root@catcat:~# sysbench cpu --cpu-max-prime=20000 --threads=1 --time=60 run
sysbench 1.0.20 (using system LuaJIT 2.1.0-beta3)

Running the test with following options:
Number of threads: 1
Initializing random number generator from current time


Prime numbers limit: 20000

Initializing worker threads...

Threads started!

CPU speed:
    events per second:  2430.61

General statistics:
    total time:                          60.0003s
    total number of events:              145838

Latency (ms):
         min:                                    0.40
         avg:                                    0.41
         max:                                    0.79
         95th percentile:                        0.42
         sum:                                59981.78

Threads fairness:
    events (avg/stddev):           145838.0000/0.00
    execution time (avg/stddev):   59.9818/0.00
```

### Memory Throughput

内存吞吐量测试，限制在 30s，多线程为 4，示例命令如下

`sysbench memory --memory-block-size=1K --memory-oper=read --memory-scope=global --memory-total-size=200G --threads=4 --time=30 run`

```
root@catcat:~# sysbench memory --memory-block-size=1K --memory-oper=read --memory-scope=global --memory-total-size=200G --threads=4 --time=30 run
sysbench 1.0.20 (using system LuaJIT 2.1.0-beta3)

Running the test with following options:
Number of threads: 4
Initializing random number generator from current time


Running memory speed test with the following options:
  block size: 1KiB
  total size: 204800MiB
  operation: read
  scope: global

Initializing worker threads...

Threads started!

Total operations: 209715200 (15755995.96 per second)

204800.00 MiB transferred (15386.71 MiB/sec)


General statistics:
    total time:                          13.3097s
    total number of events:              209715200

Latency (ms):
         min:                                    0.00
         avg:                                    0.00
         max:                                   20.46
         95th percentile:                        0.00
         sum:                                11003.24

Threads fairness:
    events (avg/stddev):           52428800.0000/0.00
    execution time (avg/stddev):   2.7508/0.04
```

## 总结：

Hybula是一家总部位于荷兰阿姆斯特丹的服务提供商，其主要网络坐落在该地，直接连接到 Doetinchem 机房。网络传输由一个大规模的 AS35133 骨干网络提供支持，同时结合了 peering 和 transit，保证了网络的高质量。该公司在阿姆斯特丹的主要数据中心：Equinix、Interxion/ DRE、Nikhef、Iron Mountain等均有业务。该网络目前由CDN77、NovoSrve和ERA-IX上游支持，因此具有接入Arelion（Telia）、Lumen（Level3）、Cogent、NTT、GTT、Core-Backbone、Liberty Global、Telecom Italia Sparkle、HE、AMS-IX、NL-ix、Cloudflare、Google等网络的能力。此外，该服务商还拥有优化到CTGNet（AS23764）、中国电信（AS4134）、中国移动（AS58453）、中国联通（AS4837）等网络的路由，以保障服务畅通。  
他们的家的服务并不便宜，但质量非常优秀，适合建站或者跑项目，口碑很好。但由于价格异常昂贵，不受普通人的喜欢。

Hybula 明确表示 CPU 是共享的，不得恶意大量占用，并且会对所有订单进行欺诈检查，包括 MaxMind minFraud，有14天退款保证。

从价格上看，Hybula 并不算便宜，但是提供高达 480G DDos 的保护，很适合那些需要高防的朋友，再套上 CF，基本非常安全了。
