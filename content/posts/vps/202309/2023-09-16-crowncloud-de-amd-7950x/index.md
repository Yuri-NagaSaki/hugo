---
title: "CrownCloud DE AMD 7950X测试"
date: "2023-09-16"
categories: 
  - "vps"
  - "jp"
---

> ## 套餐
> 
> **_Provider :_ CrownCloud  
> _Type/Plan :_ Frankfurt KVM Ryzen 9 7950X SSD Series  
> _Processor :_ AMD Ryzen 9 7950X (4.5 GHz++)  
> _Num of Core : 2 Cores_  
> _Memory : 2 GB_ DDR5 RAM  
> _Storage : 60 GB NVMe_(PCIe 4.0)  
> _Bandwidth : 1000GB @ 10 Gbps IN | 10 Gbps OUT_  
> _Location :_ Germany (Frankfurt)  
> _Price :_ $17 /month**

![](https://catcat.blog/wp-content/uploads/2023/09/image-100.png)

## 套餐

### lscpu

```
Architecture:                    x86_64
CPU op-mode(s):                  32-bit, 64-bit
Byte Order:                      Little Endian
Address sizes:                   48 bits physical, 48 bits virtual
CPU(s):                          2
On-line CPU(s) list:             0,1
Thread(s) per core:              1
Core(s) per socket:              1
Socket(s):                       2
NUMA node(s):                    1
Vendor ID:                       AuthenticAMD
CPU family:                      25
Model:                           97
Model name:                      AMD Ryzen 9 7950X 16-Core Processor
Stepping:                        2
CPU MHz:                         4491.560
BogoMIPS:                        8983.12
Virtualization:                  AMD-V
Hypervisor vendor:               KVM
Virtualization type:             full
L1d cache:                       128 KiB
L1i cache:                       128 KiB
L2 cache:                        1 MiB
L3 cache:                        32 MiB
```

### 内存

```
              total        used        free      shared  buff/cache   available
Mem:          1.9Gi       167Mi       409Mi       0.0Ki       1.4Gi       1.6Gi
Swap:         511Mi       1.0Mi       510Mi
Total:        2.4Gi       169Mi       919Mi
```

### 硬盘

```
Filesystem     Type      Size  Used Avail Use% Mounted on
udev           devtmpfs  948M     0  948M   0% /dev
tmpfs          tmpfs     199M  1.0M  198M   1% /run
/dev/vda3      ext4       59G  2.9G   53G   6% /
tmpfs          tmpfs     992M     0  992M   0% /dev/shm
tmpfs          tmpfs     5.0M     0  5.0M   0% /run/lock
tmpfs          tmpfs     992M     0  992M   0% /sys/fs/cgroup
/dev/loop0     squashfs   62M   62M     0 100% /snap/core20/1611
/dev/loop1     squashfs   47M   47M     0 100% /snap/snapd/16292
/dev/loop2     squashfs   68M   68M     0 100% /snap/lxd/22753
tmpfs          tmpfs     199M     0  199M   0% /run/user/0
/dev/loop3     squashfs   64M   64M     0 100% /snap/core20/1852
/dev/loop4     squashfs   92M   92M     0 100% /snap/lxd/24061
total          - 63G  3.2G   56G   6% -
```

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 1 hours, 7 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 2 @ 4491.560 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 512.0 MiB
Disk       : 58.5 GiB
Distro     : Ubuntu 20.04.6 LTS
Kernel     : 5.4.0-135-generic
VM Type    : KVM
IPv4/IPv6  : ✔ Online | ✔ Online

IPv4 Network Information:
---------------------------------
ISP        : diva-e Datacenters GmbH
ASN        : AS31400 firstcolo GmbH
Host       : GWY IT PTY LTD
Location   : Frankfurt Am Main, Hesse (HE)
Country    : Germany

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ----
Read       | 720.71 MB/s (180.1k) | 4.54 GB/s    (71.0k)
Write      | 722.61 MB/s (180.6k) | 4.57 GB/s    (71.4k)
Total      | 1.44 GB/s   (360.8k) | 9.11 GB/s   (142.4k)
           |                      |
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ----
Read       | 4.73 GB/s     (9.2k) | 4.71 GB/s     (4.6k)
Write      | 4.99 GB/s     (9.7k) | 5.03 GB/s     (4.9k)
Total      | 9.73 GB/s    (19.0k) | 9.75 GB/s     (9.5k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 910 Mbits/sec   | 929 Mbits/sec   | 12.4 ms
Scaleway        | Paris, FR (10G)           | 923 Mbits/sec   | 909 Mbits/sec   | 15.7 ms
NovoServe       | North Holland, NL (40G)   | 929 Mbits/sec   | 938 Mbits/sec   | 6.85 ms
Uztelecom       | Tashkent, UZ (10G)        | 798 Mbits/sec   | 510 Mbits/sec   | 90.2 ms
Clouvider       | Ashburn, VA, US (10G)     | 814 Mbits/sec   | 795 Mbits/sec   | 84.2 ms
Clouvider       | Dallas, TX, US (10G)      | 708 Mbits/sec   | 694 Mbits/sec   | 116 ms
Clouvider       | Los Angeles, CA, US (10G) | 764 Mbits/sec   | 743 Mbits/sec   | 137 ms

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 921 Mbits/sec   | 919 Mbits/sec   | 11.5 ms
Scaleway        | Paris, FR (10G)           | busy            | 909 Mbits/sec   | 16.1 ms
NovoServe       | North Holland, NL (40G)   | 921 Mbits/sec   | 924 Mbits/sec   | 8.29 ms
Uztelecom       | Tashkent, UZ (10G)        | 784 Mbits/sec   | 542 Mbits/sec   | 85.1 ms
Clouvider       | Ashburn, VA, US (10G)     | 820 Mbits/sec   | 806 Mbits/sec   | 85.1 ms
Clouvider       | Dallas, TX, US (10G)      | 722 Mbits/sec   | 707 Mbits/sec   | 116 ms
Clouvider       | Los Angeles, CA, US (10G) | 769 Mbits/sec   | 740 Mbits/sec   | 137 ms

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2800                          
Multi Core      | 5015                          
```

### Bench

```
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X 16-Core Processor
 CPU Cores          : 2 @ 4491.560 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 58.5 GB (4.0 GB Used)
 Total Mem          : 1.9 GB (133.8 MB Used)
 Total Swap         : 512.0 MB (9.5 MB Used)
 System uptime      : 0 days, 1 hour 2 min
 Load average       : 0.07, 0.29, 0.73
 OS                 : Ubuntu 20.04.6 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.4.0-135-generic
 TCP CC             : bbr
 Virtualization     : KVM
 Organization       : AS48314 Michael Sebastian Schinzel trading as IP-Projects GmbH & Co. KG
 Location           : Frankfurt am Main / DE
 Region             : Hesse
----------------------------------------------------------------------
 I/O Speed(1st run) : 769 MB/s
 I/O Speed(2nd run) : 761 MB/s
 I/O Speed(3rd run) : 783 MB/s
 I/O Speed(average) : 771.0 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency
 Speedtest.net    935.57 Mbps       941.68 Mbps         0.51 ms
 Los Angeles, US  564.52 Mbps       716.74 Mbps         144.29 ms
 Dallas, US       692.69 Mbps       782.87 Mbps         116.25 ms
 Montreal, CA     773.54 Mbps       934.48 Mbps         89.97 ms
 Paris, FR        897.79 Mbps       940.16 Mbps         11.90 ms
 Amsterdam, NL    923.41 Mbps       941.09 Mbps         10.03 ms
 Shanghai, CN     467.36 Mbps       541.15 Mbps         179.55 ms
 Nanjing, CN      338.46 Mbps       454.06 Mbps         238.29 ms
 Hongkong, CN     337.22 Mbps       851.83 Mbps         246.09 ms
 Tokyo, JP        330.50 Mbps       483.16 Mbps         236.52 ms
----------------------------------------------------------------------
```

### **Benchy**

```
Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Ubuntu 20.04.6 LTS                 Model       : AMD Ryzen 9 7950X 16-Core Processor
Location   : Germany                            Core        : 2 @ 4491.560 MHz
Kernel     : 5.4.0-135-generic                  AES-NI      : ✔ Enabled
Uptime     : 0 days, 1 hrs, 32 mins, 37 secs    VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 512.0 MiB

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 58.5 GiB                           ASN         : AS31400
Disk Usage : 4.0 GiB (7% Used)                  ISP         : firstcolo GmbH
Mem        : 1.9 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.1 GiB (7% Used)                  IPv6        : ❌ Disabled

Ookla Network Speedtest (Region: Europe)
+---------------------------------------------------------------------------------------+
| Provider    | Location          | Download     | Upload       | Data Used | Latency   |
+---------------------------------------------------------------------------------------+
| TestDebit   | Marseille, FR     |  945.9 Mb/s  |  915.4 Mb/s  |    2.1 GB |   19.4 ms |
| Vancis      | Amsterdam, NL     |  934.4 Mb/s  |  930.4 Mb/s  |    1.6 GB |    6.6 ms |
| CoreIX      | London, GB        |  924.4 Mb/s  |  906.3 Mb/s  |    1.8 GB |   12.9 ms |
| Skynet      | Warsaw, PL        |  939.3 Mb/s  |  904.4 Mb/s  |    2.2 GB |   18.9 ms |
| Vodafone    | Milan, IT         |  950.9 Mb/s  |  911.1 Mb/s  |    2.0 GB |   12.7 ms |
+---------------------------------------------------------------------------------------+

Network Performance Test (Region: Europe)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | FiberBy     | Copenhagen, DK  |  941.2 Mb/s  |  901.3 Mb/s  |   19.5 ms |
|       | WOBCOM      | Wolfsburg, DE   |  949.7 Mb/s  |  963.1 Mb/s  |    7.7 ms |
|       | Novogara    | Amsterdam, NL   |  948.9 Mb/s  |  948.8 Mb/s  |    7.5 ms |
|       | Sasag       | Schaff, CH      |  949.7 Mb/s  |  949.2 Mb/s  |    7.2 ms |
|       | Alwyzon     | Vienna, AT      |  947.8 Mb/s  |  936.7 Mb/s  |   12.8 ms |
+---------------------------------------------------------------------------------+
+---------------------------------------------------------------------------------+
| IPv6  | FiberBy     | Copenhagen, DK  |  934.1 Mb/s  |  911.9 Mb/s  |   18.0 ms |
|       | WOBCOM      | Wolfsburg, DE   |  939.6 Mb/s  |  948.4 Mb/s  |    7.9 ms |
|       | Novogara    | Amsterdam, NL   |  942.5 Mb/s  |  936.3 Mb/s  |    8.0 ms |
|       | Sasag       | Schaff, CH      |  943.0 Mb/s  |  926.1 Mb/s  |    7.4 ms |
|       | Alwyzon     | Vienna, AT      |  941.5 Mb/s  |  934.8 Mb/s  |   12.0 ms |
+---------------------------------------------------------------------------------+
```

### byte-unixbench 性能测试

```
2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       79491429.9 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    13505.9 MWIPS (10.0 s, 7 samples)
Execl Throughput                              11769.6 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       2441552.1 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          638121.7 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       7645245.8 KBps  (30.0 s, 2 samples)
Pipe Throughput                             3673670.7 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 222437.1 lps   (10.0 s, 7 samples)
Process Creation                              19139.3 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  22833.9 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   4330.9 lpm   (60.0 s, 2 samples)
System Call Overhead                        5490546.5 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   79491429.9   6811.6
Double-Precision Whetstone                       55.0      13505.9   2455.6
Execl Throughput                                 43.0      11769.6   2737.1
File Copy 1024 bufsize 2000 maxblocks          3960.0    2441552.1   6165.5
File Copy 256 bufsize 500 maxblocks            1655.0     638121.7   3855.7
File Copy 4096 bufsize 8000 maxblocks          5800.0    7645245.8  13181.5
Pipe Throughput                               12440.0    3673670.7   2953.1
Pipe-based Context Switching                   4000.0     222437.1    556.1
Process Creation                                126.0      19139.3   1519.0
Shell Scripts (1 concurrent)                     42.4      22833.9   5385.3
Shell Scripts (8 concurrent)                      6.0       4330.9   7218.2
System Call Overhead                          15000.0    5490546.5   3660.4
                                                                   ========
System Benchmarks Index Score                                        3621.7

------------------------------------------------------------------------

2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables      160561986.0 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    27204.0 MWIPS (10.0 s, 7 samples)
Execl Throughput                              13651.9 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       2641656.7 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          674856.8 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       8972836.1 KBps  (30.0 s, 2 samples)
Pipe Throughput                             7299920.9 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 883943.5 lps   (10.0 s, 7 samples)
Process Creation                              26568.7 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  29286.7 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   4446.5 lpm   (60.0 s, 2 samples)
System Call Overhead                       10823516.4 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  160561986.0  13758.5
Double-Precision Whetstone                       55.0      27204.0   4946.2
Execl Throughput                                 43.0      13651.9   3174.9
File Copy 1024 bufsize 2000 maxblocks          3960.0    2641656.7   6670.9
File Copy 256 bufsize 500 maxblocks            1655.0     674856.8   4077.7
File Copy 4096 bufsize 8000 maxblocks          5800.0    8972836.1  15470.4
Pipe Throughput                               12440.0    7299920.9   5868.1
Pipe-based Context Switching                   4000.0     883943.5   2209.9
Process Creation                                126.0      26568.7   2108.6
Shell Scripts (1 concurrent)                     42.4      29286.7   6907.3
Shell Scripts (8 concurrent)                      6.0       4446.5   7410.9
System Call Overhead                          15000.0   10823516.4   7215.7
                                                                   ========
System Benchmarks Index Score                                        5583.6
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD Ryzen 9 7950X 16-Core Processor (x86_64)
2 cores @ 4491 MHz  |  1.9 GiB RAM
Number of Processes: 2  |  Test Iterations: 2  |  Test Duration: Very Long
--------------------------------------------------------------------------
CPU Mark:                          7897
  Integer Math                     17528 Million Operations/s
  Floating Point Math              16413 Million Operations/s
  Prime Numbers                    64.0 Million Primes/s
  Sorting                          10015 Thousand Strings/s
  Encryption                       3845 MB/s
  Compression                      75123 KB/s
  CPU Single Threaded              4213 Million Operations/s
  Physics                          1045 Frames/s
  Extended Instructions (SSE)      7075 Million Matrices/s

Memory Mark:                       1902
  Database Operations              2953 Thousand Operations/s
  Memory Read Cached               40369 MB/s
  Memory Read Uncached             39036 MB/s
  Memory Write                     22450 MB/s
  Available RAM                    1497 Megabytes
  Memory Latency                   60 Nanoseconds
  Memory Threaded                  48475 MB/s
--------------------------------------------------------------------------
```

### **Speedtest**

```
   Speedtest by Ookla

      Server: Clouvider Ltd - Frankfurt Am Main (id: 35692)
         ISP: IP-Projects GmbH & Co. KG
Idle Latency:     0.99 ms   (jitter: 0.02ms, low: 0.97ms, high: 1.03ms)
    Download:   927.97 Mbps (data used: 419.0 MB)
                  3.59 ms   (jitter: 0.36ms, low: 1.22ms, high: 4.05ms)
      Upload:   926.64 Mbps (data used: 418.0 MB)
                  1.98 ms   (jitter: 0.12ms, low: 1.29ms, high: 2.38ms)
 Packet Loss:     0.0%
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-97-1024x363.png)

### Network-Speed.xyz

```
---------------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X 16-Core Processor
 CPU Cores          : 2 @ 4491.560 MHz
 CPU Cache          : 512 KB
 AES-NI             : ✔ Enabled
 VM-x/AMD-V         : ✔ Enabled
 Total Disk         : 58.5 GB (4.0 GB Used)
 Total RAM          : 1.9 GB (135.9 MB Used)
 Total Swap         : 512.0 MB (9.8 MB Used)
 System uptime      : 0 days, 1 hour 9 min
 Load average       : 0.02, 0.11, 0.46
 OS                 : Ubuntu 20.04.6 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.4.0-135-generic
 Virtualization     : KVM
---------------------------------------------------------------------------
 Basic Network Info
---------------------------------------------------------------------------
 Primary Network    : IPv4
 ISP                : diva-e Datacenters GmbH
 ASN                : AS31400 firstcolo GmbH
 Host               : GWY IT PTY LTD
 Location           : Frankfurt Am Main, Hesse-HE, Germany
---------------------------------------------------------------------------
 Speedtest.net (Region: GLOBAL)
---------------------------------------------------------------------------
 Location         Latency     Loss    DL Speed       UP Speed       Server

 ISP: IP-Projects GmbH & Co. KG

 Nearest          0.59 ms     0.0%    938.95 Mbps    935.17 Mbps    meerfarbig GmbH & Co. KG - Frankfurt

 Kochi, IN        188.47 ms   0.0%    443.96 Mbps    350.74 Mbps    Asianet Broadband - Cochin
 Bangalore, IN    147.59 ms   0.0%    470.52 Mbps    588.74 Mbps    Bharti Airtel Ltd - Bangalore
 Chennai, IN      146.46 ms   N/A     517.06 Mbps    555.28 Mbps    Jio - Chennai
 Mumbai, IN       282.63 ms   0.0%    516.65 Mbps    285.99 Mbps    i3D.net - Mumbai
 Delhi, IN        149.38 ms   0.0%    482.29 Mbps    524.71 Mbps    Tata Play Fiber - New Delhi

 Los Angeles, US  148.83 ms   0.0%    486.73 Mbps    537.01 Mbps    ReliableSite Hosting - Los Angeles, CA
 Dallas, US       116.85 ms   0.0%    664.37 Mbps    689.57 Mbps    Hivelocity - Dallas, TX
 New York, US     157.04 ms   0.0%    743.12 Mbps    530.28 Mbps    Clouvider Ltd - New York, NY
 Seattle, US      161.27 ms   N/A     489.53 Mbps    483.33 Mbps    Comcast - Seattle, WA
 Miami, US        133.87 ms   0.0%    753.78 Mbps    578.48 Mbps    AT&T - Miami, FL
 Toronto, CA      97.20 ms    0.0%    895.06 Mbps    824.65 Mbps    Rogers - Toronto, ON

 Paris, FR        11.91 ms    0.0%    938.77 Mbps    915.65 Mbps    ORANGE FRANCE - Paris
 Amsterdam, NL    6.47 ms     0.0%    937.29 Mbps    922.55 Mbps    Clouvider Ltd - Amsterdam
 Warsaw, PL       20.70 ms    0.0%    938.44 Mbps    902.34 Mbps    UPC Polska - Warszawa
 London, UK       12.96 ms    0.0%    924.54 Mbps    915.51 Mbps    VeloxServ Communications - London
 Frankfurt, DE    1.35 ms     0.0%    942.02 Mbps    936.90 Mbps    23M GmbH - Frankfurt Am Main

 Dubai, AE        137.78 ms   0.0%    937.25 Mbps    604.40 Mbps    du - Dubai
 Fujairah, AE     109.38 ms   0.0%    946.65 Mbps    721.13 Mbps    ETISALAT-UAE - Fujairah
 Jeddah, KSA      68.49 ms    0.0%    929.13 Mbps    740.25 Mbps    Saudi Telecom Company

 Shanghai, CU-CN  192.21 ms   0.0%    529.69 Mbps    456.09 Mbps    China Unicom 5G - ShangHai
 Nanjing, CT-CN   232.16 ms   0.0%    405.21 Mbps    353.91 Mbps    China Telecom JiangSu 5G - Nanjing
 Hong Kong, HKG   156.33 ms   N/A     775.29 Mbps    511.17 Mbps    STC - Hong Kong
 Singapore, SG    155.86 ms   0.0%    577.66 Mbps    502.36 Mbps    i3D.net - Singapore
 Jakarta, ID      175.37 ms   0.0%    767.65 Mbps    281.72 Mbps    PT Indosat Tbk - Jakarta
 Tokyo, JP        263.54 ms   N/A     621.78 Mbps    313.76 Mbps    fdcservers.net - Tokyo
---------------------------------------------------------------------------
 Avg DL Speed       : 714.36 Mbps
 Avg UL Speed       : 613.91 Mbps

 Total DL Data      : 23.76 GB
 Total UL Data      : 18.89 GB
 Total Data         : 42.65 GB
---------------------------------------------------------------------------
```

### 国内延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-98-1024x456.png)

### 全球延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-99-1024x538.png)
