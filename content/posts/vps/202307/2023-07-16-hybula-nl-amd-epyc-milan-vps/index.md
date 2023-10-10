---
title: "Hybula 荷兰 AMD EPYC Milan VPS 16美元测试"
date: "2023-07-16"
categories: 
  - "vps"
  - "eu"
---

## 套餐配置

```
EPYC-PROMO1
- 2x AMD Milan EPYC vCPU (2.2-2.5 Ghz cores)
- 50 GB Enterprise U.2 NVMe SSD (PCIe 4.0)
- 4 GB DDR4 ECC 3200 MT/s
- 5000 GB Traffic
- 1 Gbit/s Uplink
- 1x IPv4 Address
- /64 IPv6 Subnet
- Advanced DDoS Shield
- Located in the Doetinchem, the Netherlands
- Free 1x Manual Backup
- VirtFusion Control Panel
```

## 促销地址

[Hybula Sector Enterprise Cloud | EPYC Milan - 50GB NVMe - 4GB RAM - Anti-DDoS - NL - !!!FREE VPS!!!](https://lowendtalk.com/discussion/187476/hybula-sector-enterprise-cloud-epyc-milan-50gb-nvme-4gb-ram-anti-ddos-nl-free-vps/p1)（无aff）

Pick one of the two options!

- Upgrade traffic to 10 TB

- Upgrade to Custom Scheduled Backup (7x)

### Looking

**IP/LG：**[https://lg-nl-dtc.hybula.net/](https://lg-nl-dtc.hybula.net/)  
**位置：**荷兰，杜廷赫姆

## VPS测试

### CPU

```
root@Sakura:~# lscpu
Architecture:            x86_64
  CPU op-mode(s):        32-bit, 64-bit
  Address sizes:         48 bits physical, 48 bits virtual
  Byte Order:            Little Endian
CPU(s):                  4
  On-line CPU(s) list:   0-3
Vendor ID:               AuthenticAMD
  BIOS Vendor ID:        Red Hat
  Model name:            AMD EPYC 7B13 64-Core Processor
    BIOS Model name:     RHEL 7.6.0 PC (i440FX + PIIX, 1996)  CPU @ 2.0GHz
    BIOS CPU family:     1
    CPU family:          25
    Model:               1
    Thread(s) per core:  1
    Core(s) per socket:  1
    Socket(s):           4
    Stepping:            1
    BogoMIPS:            4499.99
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush m                         mx fxsr sse sse2 syscall nx mmxext fxsr_opt pdpe1gb rdtscp lm rep_good nopl cpuid                          extd_apicid tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2api                         c movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm cm                         p_legacy svm cr8_legacy abm sse4a misalignsse 3dnowprefetch osvw perfctr_core inv                         pcid_single ssbd ibrs ibpb stibp vmmcall fsgsbase tsc_adjust bmi1 avx2 smep bmi2 
                         invpcid rdseed adx smap clflushopt clwb sha_ni xsaveopt xsavec xgetbv1 xsaves clz                         ero xsaveerptr wbnoinvd arat npt lbrv nrip_save tsc_scale vmcb_clean pausefilter 
                         pfthreshold v_vmsave_vmload vgif umip pku ospke vaes vpclmulqdq rdpid arch_capabi                         lities
Virtualization features: 
  Virtualization:        AMD-V
  Hypervisor vendor:     KVM
  Virtualization type:   full
Caches (sum of all):     
  L1d:                   128 KiB (4 instances)
  L1i:                   128 KiB (4 instances)
  L2:                    2 MiB (4 instances)
  L3:                    1 GiB (4 instances)
NUMA:                    
  NUMA node(s):          1
  NUMA node0 CPU(s):     0-3
Vulnerabilities:         
  Itlb multihit:         Not affected
  L1tf:                  Not affected
  Mds:                   Not affected
  Meltdown:              Not affected
  Mmio stale data:       Not affected
  Retbleed:              Not affected
  Spec store bypass:     Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:            Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:            Mitigation; Retpolines, IBPB conditional, IBRS_FW, STIBP disabled, RSB filling, P                         BRSB-eIBRS Not affected
  Srbds:                 Not affected
  Tsx async abort:       Not affected
```

### Memory

```
root@Sakura:~# free -h --total
               total        used        free      shared  buff/cache   available
Mem:           7.7Gi       365Mi       7.4Gi       552Ki       110Mi       7.4Gi
Swap:             0B          0B          0B
Total:         7.7Gi       365Mi       7.4Gi
```

### Storage

```
root@Sakura:~# df -hT --total
Filesystem     Type      Size  Used Avail Use% Mounted on
udev           devtmpfs  3.9G     0  3.9G   0% /dev
tmpfs          tmpfs     791M  552K  791M   1% /run
/dev/vda3      xfs       9.9G  2.0G  7.9G  20% /
tmpfs          tmpfs     3.9G     0  3.9G   0% /dev/shm
tmpfs          tmpfs     5.0M     0  5.0M   0% /run/lock
/dev/vda2      vfat      121M  142K  120M   1% /boot/efi
tmpfs          tmpfs     791M     0  791M   0% /run/user/0
total          - 20G  2.0G   18G  11% -
```

### Yabs

```
root@Sakura:~# curl -sL yabs.sh | bash
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2023-04-23                    #
# https://github.com/masonr/yet-another-bench-script #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

Sun Jul 16 12:23:30 PM CST 2023

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 0 minutes
Processor  : AMD EPYC 7B13 64-Core Processor
CPU cores  : 4 @ 2249.996 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 7.7 GiB
Swap       : 0.0 KiB
Disk       : 9.9 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-10-amd64
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
Read       | 357.52 MB/s  (89.3k) | 4.66 GB/s    (72.9k)
Write      | 358.46 MB/s  (89.6k) | 4.69 GB/s    (73.3k)
Total      | 715.99 MB/s (178.9k) | 9.36 GB/s   (146.2k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 6.38 GB/s    (12.4k) | 6.56 GB/s     (6.4k)
Write      | 6.72 GB/s    (13.1k) | 7.00 GB/s     (6.8k)
Total      | 13.10 GB/s   (25.5k) | 13.57 GB/s   (13.2k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.09 Gbits/sec  | 955 Mbits/sec   | 7.68 ms        
Scaleway        | Paris, FR (10G)           | 1.08 Gbits/sec  | busy            | 18.1 ms        
NovoServe       | North Holland, NL (40G)   | 1.10 Gbits/sec  | busy            | 3.17 ms        
Uztelecom       | Tashkent, UZ (10G)        | 1.03 Gbits/sec  | 630 Mbits/sec   | 95.0 ms        
Clouvider       | NYC, NY, US (10G)         | busy            | 584 Mbits/sec   | 77.7 ms        
Clouvider       | Dallas, TX, US (10G)      | 866 Mbits/sec   | 309 Mbits/sec   | 118 ms         
Clouvider       | Los Angeles, CA, US (10G) | 774 Mbits/sec   | 109 Mbits/sec   | 141 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.09 Gbits/sec  | 941 Mbits/sec   | 7.64 ms        
Scaleway        | Paris, FR (10G)           | 1.09 Gbits/sec  | 939 Mbits/sec   | 11.3 ms        
NovoServe       | North Holland, NL (40G)   | 1.09 Gbits/sec  | 921 Mbits/sec   | 2.93 ms        
Uztelecom       | Tashkent, UZ (10G)        | 1.03 Gbits/sec  | 837 Mbits/sec   | 95.0 ms        
Clouvider       | NYC, NY, US (10G)         | 638 Mbits/sec   | 146 Mbits/sec   | 77.5 ms        
Clouvider       | Dallas, TX, US (10G)      | 919 Mbits/sec   | 122 Mbits/sec   | 118 ms         
Clouvider       | Los Angeles, CA, US (10G) | 905 Mbits/sec   | 292 Mbits/sec   | 141 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1733                          
Multi Core      | 5717                          
Full Test       | https://browser.geekbench.com/v6/cpu/1935329

YABS completed in 11 min 45 sec
```

### Bench 测试

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD EPYC 7B13 64-Core Processor
 CPU Cores          : 4 @ 2249.996 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 9.9 GB (1.9 GB Used)
 Total Mem          : 7.7 GB (376.8 MB Used)
 System uptime      : 0 days, 0 hour 15 min
 Load average       : 0.07, 0.32, 0.21
 OS                 : Debian GNU/Linux 12
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.1.0-10-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS35133 Hybula B.V.
 Location           : Amsterdam / NL
 Region             : North Holland
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.5 GB/s
 I/O Speed(2nd run) : 1.7 GB/s
 I/O Speed(3rd run) : 1.8 GB/s
 I/O Speed(average) : 1706.7 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    996.71 Mbps       943.36 Mbps         2.35 ms     
 Los Angeles, US  394.08 Mbps       891.58 Mbps         147.21 ms   
 Dallas, US       388.86 Mbps       851.85 Mbps         119.01 ms   
 Montreal, CA     177.09 Mbps       928.14 Mbps         81.19 ms    
 Amsterdam, NL    999.35 Mbps       955.31 Mbps         8.73 ms     
 Shanghai, CN     240.37 Mbps       812.30 Mbps         231.49 ms   
 Nanjing, CN      245.60 Mbps       714.35 Mbps         197.69 ms   
 Hongkong, CN     77.19 Mbps        850.53 Mbps         251.42 ms   
 Singapore, SG    465.13 Mbps       739.93 Mbps         160.49 ms   
 Tokyo, JP        325.04 Mbps       521.98 Mbps         227.94 ms   
----------------------------------------------------------------------
 Finished in        : 4 min 50 sec
 Timestamp          : 2023-07-16 12:43:15 CST
----------------------------------------------------------------------
```

### benchy测试

```
# # # # # # # # # # # # # # # # # # # # #
#             Benchy v2.7               #
#    https://github.com/L1so/benchy     #
# # # # # # # # # # # # # # # # # # # # #
#        16 Jul 2023 12:43 CST          #
# # # # # # # # # # # # # # # # # # # # #

Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Debian GNU/Linux 12 (bookworm)     Model       : AMD EPYC 7B13 64-Core Processor
Location   : Netherlands                        Core        : 4 @ 2249.996 MHz
Kernel     : 6.1.0-10-amd64                     AES-NI      : ✔ Enabled
Uptime     : 0 days, 0 hrs, 21 mins, 7 secs     VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 0.0 KiB   

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 9.8 GiB                            ASN         : AS35133   
Disk Usage : 2.0 GiB (20% Used)                 ISP         : Hybula B.V.
Mem        : 7.7 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.4 GiB (5% Used)                  IPv6        : ✔ Enabled

Disk Performance Check (xfs on /dev/vda3) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 349.56 MB/s | 350.48 MB/s | 700.04 MB/s | 89.5k  | 89.7k  | 179.2k |
| 64k  | 4.38 GB/s   | 4.40 GB/s   | 8.79 GB/s   | 71.8k  | 72.2k  | 144.0k |
| 512k | 5.99 GB/s   | 6.31 GB/s   | 12.30 GB/s  | 12.3k  | 12.9k  | 25.2k  |
| 1m   | 6.32 GB/s   | 6.74 GB/s   | 13.07 GB/s  | 6.5k   | 6.9k   | 13.4k  |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |  964.7 Mb/s  |  107.8 Mb/s  |  101.9 ms |
|       | Uztelecom   | Tashkent, UZ    |    1.0 Gb/s  |  844.1 Mb/s  |   95.0 ms |
|       | Novogara    | Amsterdam, NL   |    1.1 Gb/s  |  958.8 Mb/s  |    4.8 ms |
|       | FiberBy     | Copenhagen, DK  |    1.1 Gb/s  |  960.3 Mb/s  |   17.8 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |  705.6 Mb/s  |  293.2 Mb/s  |  101.9 ms |
|       | Uztelecom   | Tashkent, UZ    |    1.0 Gb/s  |  885.0 Mb/s  |   95.0 ms |
|       | Novogara    | Amsterdam, NL   |    1.1 Gb/s  |  946.8 Mb/s  |    4.7 ms |
|       | FiberBy     | Copenhagen, DK  |    1.1 Gb/s  |  944.6 Mb/s  |   14.9 ms |
+---------------------------------------------------------------------------------+

+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 1729                     |
| Multi Core         | 5775                     |
+-----------------------------------------------+
| https://browser.geekbench.com/v6/cpu/1935444  |
+-----------------------------------------------+
| Benchy time spent  | 9 Minutes 32 Seconds     |
+-----------------------------------------------+
```

### 流媒体解锁测试

```
============[ Multination ]============
 Dazn:                                  Yes (Region: NL)
 HotStar:                               No
 Disney+:                               Yes (Region: NL)
 Netflix:                               Yes (Region: NL)
 YouTube Premium:                       Yes (Region: NL)
 Amazon Prime Video:                    Yes (Region: NL)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   LA
 Viu.com:                               No
 YouTube CDN:                           Amsterdam 
 Netflix Preferred CDN:                 Amsterdam  
 Spotify Registration:                  Yes (Region: NL)
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
===============[ Europe ]==============
 Rakuten TV:                            Yes
 Funimation:                            Failed
 SkyShowTime:                           Yes (Region: NL)
 HBO Max:                               Yes (Region: NL)
 Maths Spot:                            Failed
 ---GB---
 Sky Go:                                Yes
 BritBox:                               Yes
 ITV Hub:                               No
 Channel 4:                             No
 Channel 5:                             No
 BBC iPLAYER:                           No
 Discovery+ UK:                         No
 ---FR---
 Salto:                                 Failed (Network Connection)
 Canal+:                                No
 Molotov:                               No
 ---DE---
 Joyn:                                  No
 Sky:                                   No
 ZDF:                                   No
 ---NL---
 NLZIET:                                Failed
 videoland:                             Failed (Network Connection)
 NPO Start Plus:                        No
 ---ES---
 PANTAYA:                               Failed (Network Connection)
 ---IT---
 Rai Play:                              Yes
 ---RU---
 Amediateka:                            Yes
=======================================


 ** 正在测试IPv6解锁情况 
--------------------------------
 ** 您的网络为: Hybula B.V. (2a09:e240:22:*:*) 


============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: NL)
 Netflix:                               Yes (Region: NL)
 YouTube Premium:                       Yes (Region: NL)
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Amsterdam 
 Netflix Preferred CDN:                 Frankfurt  
 Spotify Registration:                  Yes (Region: NL)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
===============[ Europe ]==============
 Rakuten TV:                            Failed (Network Connection)
 Funimation:                            IPv6 Not Support
 SkyShowTime:                           Yes (Region: NL)
 HBO Max:                               Failed (Network Connection)
 Maths Spot:                            IPv6 Not Support
 ---GB---
 Sky Go:                                Failed (Network Connection)
 BritBox:                               Yes
 ITV Hub:                               Failed (Network Connection)
 Channel 4:                             Failed (Network Connection)
 Channel 5:                             IPv6 Not Support
 BBC iPLAYER:                           Failed
 Discovery+ UK:                         IPv6 Not Support
 ---FR---
 Salto:                                 Failed (Network Connection)
 Canal+:                                Failed (Network Connection)
 Molotov:                               No
 ---DE---
 Joyn:                                  Failed (Network Connection)
 Sky:                                   Failed (Network Connection)
 ZDF:                                   Failed (Network Connection)
 ---NL---
 NLZIET:                                Failed
 videoland:                             Failed (Network Connection)
 NPO Start Plus:                        Failed (Network Connection)
 ---ES---
 PANTAYA:                               Failed (Network Connection)
 ---IT---
 Rai Play:                              Failed (Network Connection)
 ---RU---
 Amediateka:                            Failed (Network Connection)
=======================================
```

### 融合怪脚本综合测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7B13 64-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 2249.996 MHz
 CPU 缓存          : L1: 128.00 KB / L2: 2.00 MB / L3: 1024.00 MB
 硬盘空间          : 1.97 GiB / 9.82 GiB
 启动盘路径        : /dev/vda3
 内存              : 253.55 MiB / 7.72 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 34 min
 负载              : 0.15, 0.35, 0.30
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-10-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS35133 Hybula B.V.
 IPV4 位置         : Amsterdam / North Holland / NL
 IPV6 ASN          : AS35133 Hybula B.V.
 IPV6 位置         : Amsterdam / NL-NH
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           3973 Scores
 4 线程测试(多核)得分:          15822 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          50295.62 MB/s
 单线程写测试:          29206.01 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         72.0 MB/s (17.58 IOPS, 1.46s))          94.7 MB/s (23113 IOPS, 1.11s)
 1GB-1M Block           1.2 GB/s (1106 IOPS, 0.90s)             5.3 GB/s (5073 IOPS, 0.20s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 360.97 MB/s  (90.2k) | 4.58 GB/s    (71.6k)
Write      | 361.92 MB/s  (90.4k) | 4.61 GB/s    (72.0k)
Total      | 722.90 MB/s (180.7k) | 9.19 GB/s   (143.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 6.50 GB/s    (12.7k) | 6.65 GB/s     (6.4k)
Write      | 6.85 GB/s    (13.3k) | 7.09 GB/s     (6.9k)
Total      | 13.35 GB/s   (26.0k) | 13.75 GB/s   (13.4k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS17S11)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS15S46)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：荷兰
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：荷兰
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：荷兰区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：荷兰区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: NL)
 HotStar:                               No
 Disney+:                               Yes (Region: NL)
 Netflix:                               Yes (Region: NL)
 YouTube Premium:                       Yes (Region: NL)
 Amazon Prime Video:                    Yes (Region: NL)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   LA
 Viu.com:                               No
 YouTube CDN:                           Amsterdam 
 Netflix Preferred CDN:                 Amsterdam  
 Spotify Registration:                  Yes (Region: NL)
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: NL)
 Netflix:                               Yes (Region: NL)
 YouTube Premium:                       Yes (Region: NL)
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Amsterdam 
 Netflix Preferred CDN:                 Frankfurt  
 Spotify Registration:                  Yes (Region: NL)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【NL】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：0
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：4
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
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
2023/07/16 12:58:45 北京电信 219.141.136.12  测试超时
2023/07/16 12:58:45 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/16 12:58:45 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/16 12:58:45 上海电信 202.96.209.133  电信163 [普通线路]           
2023/07/16 12:58:45 上海联通 210.22.97.1     联通4837[普通线路]           
2023/07/16 12:58:45 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/16 12:58:45 广州电信 58.60.188.222   电信163 [普通线路]           
2023/07/16 12:58:45 广州联通 210.21.196.6    联通4837[普通线路]           
2023/07/16 12:58:45 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/07/16 12:58:45 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/16 12:58:45 成都联通 119.6.6.6       联通4837[普通线路]           
2023/07/16 12:58:45 成都移动 211.137.96.205  电信163 [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.28 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com
0.34 ms  *  局域网
2.43 ms  *  局域网
2.27 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
2.34 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
2.70 ms  *  荷兰, 北荷兰省, 哈勒姆, novoserve.com
4.43 ms  *  荷兰, 北荷兰省, 阿姆斯特丹, cteurope.net
212.67 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
222.21 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
213.91 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
218.91 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
220.27 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.34 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com
0.19 ms  *  局域网
2.37 ms  *  局域网
2.35 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
2.26 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
2.59 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
9.83 ms  AS4837  德国, 黑森州, 法兰克福, chinaunicom.com, 联通
140.13 ms  AS4837  中国, 北京, chinaunicom.com, 联通
158.19 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
161.63 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
166.42 ms  AS17816  中国, 广东, 广州, chinaunicom.com, 联通
230.34 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
165.29 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.20 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com
0.22 ms  *  局域网
2.37 ms  *  局域网
2.26 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
2.32 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
2.63 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
3.00 ms  *  荷兰, novoserve.com
4.30 ms  AS58453  中国, 香港, chinamobile.com, 移动
10.68 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
236.80 ms  AS58453  中国, 上海, chinamobile.com, 移动
227.34 ms  AS9808  中国, 上海, chinamobile.com, 移动
222.67 ms  AS9808  中国, 上海, chinamobile.com, 移动
228.61 ms  AS9808  中国, 上海, chinamobile.com, 移动
194.81 ms  AS9808  中国, 北京, chinamobile.com, 移动
197.25 ms  AS9808  中国, 北京, chinamobile.com, 移动
196.25 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    997.17 Mbps     951.60 Mbps     2.37     0.0%
洛杉矶           208.83 Mbps     949.51 Mbps     146.24   0.0%
新加坡           496.74 Mbps     822.91 Mbps     160.40   0.0%
联通沈阳         15.54 Mbps      230.58 Mbps     140.00   0.7%
联通上海5G       481.48 Mbps     954.99 Mbps     257.34   0.0%
电信Lanzhou      0.59 Mbps       161.89 Mbps     331.67   NULL
电信天津         0.64 Mbps       574.92 Mbps     220.99   NULL
移动Chengdu      643.43 Mbps     1036.02 Mbps    210.52   0.0%
移动Zhengzhou5G  1.45 Mbps       522.91 Mbps     202.49   4.7%
------------------------------------------------------------------------
------------------------------------------------------------------------
 总共花费      : 6 分 26 秒
 时间          : Sun Jul 16 13:04:08 CST 2023
------------------------------------------------------------------------
```

### 多地区回程测试

```
----------------------------------------------------------------------
北京电信
traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  2.58.57.193.powered.by.hybu.la (2.58.57.193)  0.22 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com 2  10.1.0.2  0.20 ms  *  局域网
 3  10.0.0.1  2.36 ms  *  局域网
 4  unn-178-249-215-250.cdn77.com (178.249.215.250)  2.45 ms  *  CDN77.COM 骨干网, hostuj.to
 5  10.66.102.2  2.47 ms  *  局域网
 6  62.115.191.209  2.69 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
 7  *
 8  ldn-bb1-link.ip.twelve99.net (213.155.136.98)  10.52 ms  AS1299  英国, 伦敦, telia.com
 9  ldn-b2-link.ip.twelve99.net (62.115.122.189)  9.71 ms  AS1299  英国, 伦敦, telia.com
10  chinatelecom-ic-335946.ip.twelve99-cust.net (62.115.14.114)  10.68 ms  AS1299  英国, 伦敦, telia.com
11  *
12  *
13  *
14  *
15  *
16  bj141-147-210.bjtelecom.net (219.141.147.210)  200.33 ms  AS4847  中国, 北京, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
上海电信
traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  2.58.57.193.powered.by.hybu.la (2.58.57.193)  0.19 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com 2  10.1.0.2  0.32 ms  *  局域网
 3  10.0.0.1  2.22 ms  *  局域网
 4  185.147.12.182  2.21 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
 5  br1-haa.infra.novoserve.net (185.147.12.125)  2.65 ms  *  荷兰, 北荷兰省, 哈勒姆, novoserve.com
 6  81.173.26.5  4.74 ms  *  荷兰, 北荷兰省, 阿姆斯特丹, cteurope.net
 7  202.97.43.13  252.31 ms  AS4134  中国, 上海, chinatelecom.com.cn, 电信
 8  *
 9  *
10  61.152.24.85  207.79 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信
11  124.74.229.238  225.81 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信
12  ns-pd.online.sh.cn (202.96.209.133)  196.42 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
深圳电信
traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  2.58.57.193.powered.by.hybu.la (2.58.57.193)  0.29 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com 2  10.1.0.2  0.23 ms  *  局域网
 3  10.0.0.1  2.30 ms  *  局域网
 4  185.147.12.182  2.25 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
 5  er2-oum.infra.novoserve.net (185.147.12.35)  2.32 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 6  br1-haa.infra.novoserve.net (185.147.12.127)  2.61 ms  *  荷兰, 北荷兰省, 哈勒姆, novoserve.com
 7  81.173.26.5  4.82 ms  *  荷兰, 北荷兰省, 阿姆斯特丹, cteurope.net
 8  202.97.58.13  212.64 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
 9  202.97.94.97  208.94 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
10  202.97.94.137  222.07 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
11  202.105.158.53  228.81 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
12  *
13  58.60.188.222  213.42 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
北京联通
traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  2.58.57.193.powered.by.hybu.la (2.58.57.193)  0.27 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com 2  10.1.0.2  0.22 ms  *  局域网
 3  10.0.0.1  2.31 ms  *  局域网
 4  185.147.12.182  2.29 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
 5  lag-135.ear4.Amsterdam1.Level3.net (213.19.205.233)  2.55 ms  AS3356  荷兰, 北荷兰省, 阿姆斯特丹, level3.com
 6  *
 7  CHINA-UNICO.ear1.LosAngeles6.Level3.net (4.26.3.26)  246.89 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
 8  219.158.4.9  206.34 ms  AS4837  中国, 北京, chinaunicom.com, 联通
 9  219.158.9.218  212.98 ms  AS4837  中国, 北京, chinaunicom.com, 联通
10  *
11  *
12  202.106.50.1  227.68 ms  AS4808  中国, 北京, chinaunicom.com, 联通

----------------------------------------------------------------------
上海联通
traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  2.58.57.193.powered.by.hybu.la (2.58.57.193)  0.20 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com 2  10.1.0.2  0.25 ms  *  局域网
 3  10.0.0.1  2.26 ms  *  局域网
 4  185.147.12.182  2.29 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
 5  er2-oum.infra.novoserve.net (185.147.12.35)  2.27 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 6  185.147.12.161  2.52 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 7  219.158.40.5  10.13 ms  AS4837  德国, 黑森州, 法兰克福, chinaunicom.com, 联通
 8  219.158.98.133  133.16 ms  AS4837  中国, 北京, chinaunicom.com, 联通
 9  219.158.111.218  151.61 ms  AS4837  中国, 上海, chinaunicom.com, 联通
10  219.158.6.205  158.13 ms  AS4837  中国, 上海, chinaunicom.com, 联通
11  *
12  *
13  112.64.250.202  169.57 ms  AS17621  中国, 上海, chinaunicom.com, 联通
14  210.22.97.1  160.44 ms  AS17621  中国, 上海, chinaunicom.com, 联通

----------------------------------------------------------------------
深圳联通
traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  2.58.57.193.powered.by.hybu.la (2.58.57.193)  0.22 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com 2  10.1.0.2  0.27 ms  *  局域网
 3  10.0.0.1  2.30 ms  *  局域网
 4  185.147.12.182  2.27 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
 5  er2-oum.infra.novoserve.net (185.147.12.35)  2.29 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 6  185.147.12.161  2.66 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 7  219.158.40.5  10.02 ms  AS4837  德国, 黑森州, 法兰克福, chinaunicom.com, 联通
 8  219.158.3.117  143.83 ms  AS4837  中国, 北京, chinaunicom.com, 联通
 9  219.158.111.214  155.04 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
10  219.158.3.161  166.77 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
11  219.158.3.153  170.91 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
12  157.148.0.58  167.07 ms  AS17816  中国, 广东, 广州, chinaunicom.com, 联通
13  120.80.144.34  184.16 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
14  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  165.37 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通

----------------------------------------------------------------------
北京移动
traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  2.58.57.193.powered.by.hybu.la (2.58.57.193)  0.20 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com 2  10.1.0.2  0.25 ms  *  局域网
 3  10.0.0.1  2.33 ms  *  局域网
 4  185.147.12.182  2.22 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
 5  er2-oum.infra.novoserve.net (185.147.12.35)  2.26 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 6  185.147.12.161  2.54 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 7  185.147.12.163  2.94 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 8  223.119.65.40  4.36 ms  AS58453  中国, 香港, chinamobile.com, 移动
 9  223.120.10.133  122.82 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
10  223.120.16.26  250.70 ms  AS58453  中国, 北京, chinamobile.com, 移动
11  221.183.55.110  250.03 ms  AS9808  中国, 北京, chinamobile.com, 移动
12  221.183.25.201  229.69 ms  AS9808  中国, 北京, chinamobile.com, 移动
13  221.183.89.118  194.05 ms  AS9808  中国, 北京, chinamobile.com, 移动
14  221.183.46.174  237.90 ms  AS9808  中国, 北京, chinamobile.com, 移动
15  221.183.130.134  255.01 ms  AS9808  中国, 北京, chinamobile.com, 移动
16  *
17  cachedns03.bj.chinamobile.com (221.179.155.161)  252.42 ms  AS56048  中国, 北京, chinamobile.com, 移动

----------------------------------------------------------------------
上海移动
traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  2.58.57.193.powered.by.hybu.la (2.58.57.193)  0.21 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com 2  10.1.0.2  0.20 ms  *  局域网
 3  10.0.0.1  2.26 ms  *  局域网
 4  185.147.12.182  2.30 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
 5  er2-oum.infra.novoserve.net (185.147.12.35)  2.29 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 6  185.147.12.161  2.54 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 7  185.147.12.131  2.90 ms  *  荷兰, novoserve.com
 8  223.119.65.40  5.20 ms  AS58453  中国, 香港, chinamobile.com, 移动
 9  223.120.10.217  10.57 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
10  223.120.16.186  225.98 ms  AS58453  中国, 上海, chinamobile.com, 移动
11  221.183.89.182  227.45 ms  AS9808  中国, 上海, chinamobile.com, 移动
12  221.183.89.69  223.08 ms  AS9808  中国, 上海, chinamobile.com, 移动
13  221.183.89.50  229.22 ms  AS9808  中国, 上海, chinamobile.com, 移动
14  *
15  221.181.125.178  229.91 ms  AS24400  中国, 上海, chinamobile.com, 移动
16  211.136.112.252  230.19 ms  AS24400  中国, 上海, chinamobile.com, 移动
17  211.136.112.200  228.37 ms  AS24400  中国, 上海, chinamobile.com, 移动

----------------------------------------------------------------------
深圳移动
traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  2.58.57.193.powered.by.hybu.la (2.58.57.193)  0.25 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com 2  10.1.0.2  0.30 ms  *  局域网
 3  10.0.0.1  2.30 ms  *  局域网
 4  185.147.12.182  2.32 ms  *  荷兰, 南荷兰省, 代夫特, novoserve.com
 5  er2-oum.infra.novoserve.net (185.147.12.35)  2.29 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 6  185.147.12.161  2.58 ms  *  荷兰, 北荷兰省, 哈勒默梅尔, novoserve.com
 7  185.147.12.131  2.94 ms  *  荷兰, novoserve.com
 8  223.119.65.40  3.52 ms  AS58453  中国, 香港, chinamobile.com, 移动
 9  223.120.10.117  10.59 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
10  223.120.16.142  236.74 ms  AS58453  中国, 上海, chinamobile.com, 移动
11  221.183.89.174  227.21 ms  AS9808  中国, 上海, chinamobile.com, 移动
12  221.183.89.69  222.50 ms  AS9808  中国, 上海, chinamobile.com, 移动
13  221.183.89.50  229.24 ms  AS9808  中国, 上海, chinamobile.com, 移动
14  *
15  *
16  *
17  ns6.gd.cnmobile.net (120.196.165.24)  196.29 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动

----------------------------------------------------------------------
成都教育网
traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  2.58.57.193.powered.by.hybu.la (2.58.57.193)  0.19 ms  AS35133  荷兰, 北荷兰省, 阿姆斯特丹, hybula.com 2  10.1.0.2  0.31 ms  *  局域网
 3  10.0.0.1  2.35 ms  *  局域网
 4  *
 5  *
 6  *
 7  port-channel11.core2.ash1.he.net (184.105.222.190)  78.77 ms  AS6939  美国, 弗吉尼亚州, 阿什本, he.net 8  port-channel17.core2.lax1.he.net (184.104.198.225)  146.99 ms  AS6939  美国, 加利福尼亚州, 洛杉矶, he.net
 9  *
10  *
11  erx-cernet-bkb-as4538.10gigabitethernet3-2.core1.lax2.he.net (216.218.244.106)  141.32 ms  AS6939  美国, 加利福尼亚州, 洛杉矶, he.net
12  101.4.117.185  143.35 ms  AS4538  美国, 加利福尼亚州, 洛杉矶, edu.cn, 教育网
13  101.4.117.213  262.72 ms  AS4538  中国, 北京, edu.cn, 教育网
14  *
15  *
16  101.4.117.81  261.35 ms  AS4538  中国, 北京, edu.cn, 教育网
17  101.4.112.14  278.47 ms  AS4538  中国, 陕西, 西安, edu.cn, 教育网
18  101.4.112.18  317.77 ms  AS4538  中国, 四川, 成都, edu.cn, 教育网
19  *
20  *
21  *
22  *
23  *
24  202.112.14.151  288.63 ms  AS24355  中国, 四川, 成都, 电子科技大学CERNET西南地区网络中心, edu.cn, 教育网

----------------------------------------------------------------------
```

### UnixBench测试

```
========================================================================
   BYTE UNIX Benchmarks (Version 5.1.3)

   System: Sakura: GNU/Linux
   OS: GNU/Linux -- 6.1.0-10-amd64 -- #1 SMP PREEMPT_DYNAMIC Debian 6.1.37-1 (2023-07-03)
   Machine: x86_64 (unknown)
   Language: en_US.utf8 (charmap="UTF-8", collate="UTF-8")
   CPU 0: AMD EPYC 7B13 64-Core Processor (4500.0 bogomips)
          x86-64, MMX, AMD MMX, Physical Address Ext, SYSENTER/SYSEXIT, AMD virtualization, SYSCALL/SYSRET   CPU 1: AMD EPYC 7B13 64-Core Processor (4500.0 bogomips)
          x86-64, MMX, AMD MMX, Physical Address Ext, SYSENTER/SYSEXIT, AMD virtualization, SYSCALL/SYSRET   CPU 2: AMD EPYC 7B13 64-Core Processor (4500.0 bogomips)
          x86-64, MMX, AMD MMX, Physical Address Ext, SYSENTER/SYSEXIT, AMD virtualization, SYSCALL/SYSRET   CPU 3: AMD EPYC 7B13 64-Core Processor (4500.0 bogomips)
          x86-64, MMX, AMD MMX, Physical Address Ext, SYSENTER/SYSEXIT, AMD virtualization, SYSCALL/SYSRET   13:09:37 up 46 min,  1 user,  load average: 0.00, 0.07, 0.17; runlevel 5

------------------------------------------------------------------------
Benchmark Run: Sun Jul 16 2023 13:09:37 - 13:37:35
4 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       49612683.5 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     8327.5 MWIPS (10.0 s, 7 samples)
Execl Throughput                               3873.0 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1197145.1 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          312494.8 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       4236961.3 KBps  (30.0 s, 2 samples)
Pipe Throughput                             2172529.1 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                  62182.3 lps   (10.0 s, 7 samples)
Process Creation                               7831.2 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  12685.6 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   3472.5 lpm   (60.0 s, 2 samples)
System Call Overhead                        2552596.8 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   49612683.5   4251.3
Double-Precision Whetstone                       55.0       8327.5   1514.1
Execl Throughput                                 43.0       3873.0    900.7
File Copy 1024 bufsize 2000 maxblocks          3960.0    1197145.1   3023.1
File Copy 256 bufsize 500 maxblocks            1655.0     312494.8   1888.2
File Copy 4096 bufsize 8000 maxblocks          5800.0    4236961.3   7305.1
Pipe Throughput                               12440.0    2172529.1   1746.4
Pipe-based Context Switching                   4000.0      62182.3    155.5
Process Creation                                126.0       7831.2    621.5
Shell Scripts (1 concurrent)                     42.4      12685.6   2991.9
Shell Scripts (8 concurrent)                      6.0       3472.5   5787.6
System Call Overhead                          15000.0    2552596.8   1701.7
                                                                   ========
System Benchmarks Index Score                                        1805.8

------------------------------------------------------------------------
Benchmark Run: Sun Jul 16 2023 13:37:35 - 14:05:33
4 CPUs in system; running 4 parallel copies of tests

Dhrystone 2 using register variables      196290793.6 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    33371.4 MWIPS (9.9 s, 7 samples)
Execl Throughput                              10317.4 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        693222.7 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          192250.4 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       2357742.1 KBps  (30.0 s, 2 samples)
Pipe Throughput                             8725920.0 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 690779.6 lps   (10.0 s, 7 samples)
Process Creation                              32683.3 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  28628.1 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   3953.1 lpm   (60.0 s, 2 samples)
System Call Overhead                        3288062.3 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  196290793.6  16820.1
Double-Precision Whetstone                       55.0      33371.4   6067.5
Execl Throughput                                 43.0      10317.4   2399.4
File Copy 1024 bufsize 2000 maxblocks          3960.0     693222.7   1750.6
File Copy 256 bufsize 500 maxblocks            1655.0     192250.4   1161.6
File Copy 4096 bufsize 8000 maxblocks          5800.0    2357742.1   4065.1
Pipe Throughput                               12440.0    8725920.0   7014.4
Pipe-based Context Switching                   4000.0     690779.6   1726.9
Process Creation                                126.0      32683.3   2593.9
Shell Scripts (1 concurrent)                     42.4      28628.1   6751.9
Shell Scripts (8 concurrent)                      6.0       3953.1   6588.6
System Call Overhead                          15000.0    3288062.3   2192.0
                                                                   ========
System Benchmarks Index Score                                        3681.7



======= Script description and score comparison completed! ======= 
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD EPYC 7B13 64-Core Processor (x86_64)
4 cores @ 0 MHz  |  7.7 GiB RAM
Number of Processes: 4  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          9650
  Integer Math                     22610 Million Operations/s
  Floating Point Math              18231 Million Operations/s
  Prime Numbers                    73.5 Million Primes/s
  Sorting                          13494 Thousand Strings/s
  Encryption                       4905 MB/s
  Compression                      97456 KB/s
  CPU Single Threaded              2595 Million Operations/s
  Physics                          1309 Frames/s
  Extended Instructions (SSE)      8360 Million Matrices/s

Memory Mark:                       2649
  Database Operations              3989 Thousand Operations/s
  Memory Read Cached               26433 MB/s
  Memory Read Uncached             20981 MB/s
  Memory Write                     21781 MB/s
  Available RAM                    6859 Megabytes
  Memory Latency                   57 Nanoseconds
  Memory Threaded                  75489 MB/s
--------------------------------------------------------------------------
```

### SpeedTest测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-171.png)

### 全球延迟测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-172.png)

### 国内延迟测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-173.png)

## 总结

**Hybula**一如既往的优秀，配置CPU为AMD EPYC Milan系列CPU，搭配U.2 PCIE 4.0 NVMe企业级硬盘，1G带宽+5TB流量，自带备份空间，强劲的性能，优秀的网络质量，特别适合做站用户。
