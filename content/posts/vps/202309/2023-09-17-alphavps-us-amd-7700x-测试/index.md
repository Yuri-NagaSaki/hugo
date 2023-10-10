---
title: "AlphaVPS US AMD 7700X 测试"
date: "2023-09-17"
categories: 
  - "vps"
  - "usa"
---

> ## 套餐
> 
> **_Provider : AlphaVPS  
> Type/Plan : 2G - RYZEN  
> Processor : AMD Ryzen 9 7700X  
> Num of Core : 2 Cores  
> Memory : 2 GB DDR5 RAM  
> Storage : 30 GB NVMe(PCIe 4.0)  
> Bandwidth : 2TB @ 10 Gbps IN | 10 Gbps OUT  
> Location : USA (Los Angeles)  
> Price : €5.99/m_**

## 测评

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
Model name:                      AMD Ryzen 7 7700X 8-Core Processor
Stepping:                        2
CPU MHz:                         4491.540
BogoMIPS:                        8983.08
Virtualization:                  AMD-V
Hypervisor vendor:               KVM
Virtualization type:             full
L1d cache:                       128 KiB
L1i cache:                       128 KiB
L2 cache:                        1 MiB
L3 cache:                        32 MiB
```

### 硬盘

```
Filesystem     Type      Size  Used Avail Use% Mounted on
udev           devtmpfs  947M     0  947M   0% /dev
tmpfs          tmpfs     199M  952K  198M   1% /run
/dev/vda2      ext4       29G  3.4G   24G  13% /
tmpfs          tmpfs     992M     0  992M   0% /dev/shm
tmpfs          tmpfs     5.0M     0  5.0M   0% /run/lock
tmpfs          tmpfs     992M     0  992M   0% /sys/fs/cgroup

tmpfs          tmpfs     199M     0  199M   0% /run/user/0
total          - 33G  3.8G   27G  13% -
```

### 内存

```
              total        used        free      shared  buff/cache   available
Mem:          1.9Gi       136Mi       1.5Gi       2.0Mi       288Mi       1.7Gi
Swap:         1.0Gi          0B       1.0Gi
Total:        2.9Gi       136Mi       2.5Gi
```

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 52 minutes
Processor  : AMD Ryzen 7 7700X 8-Core Processor
CPU cores  : 2 @ 4491.540 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 1024.0 MiB
Disk       : 28.4 GiB
Distro     : Ubuntu 20.04.6 LTS
Kernel     : 5.4.0-147-generic
VM Type    : KVM
Net Online : IPv4 & IPv6

IPv6 Network Information:
---------------------------------
ISP        : WebNX, Inc.
ASN        : AS18450 WebNX, Inc.
Host       : WebNX, Inc.
Location   : Cheyenne, Wyoming (WY)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ----
Read       | 873.75 MB/s (218.4k) | 1.09 GB/s    (17.0k)
Write      | 876.06 MB/s (219.0k) | 1.09 GB/s    (17.1k)
Total      | 1.74 GB/s   (437.4k) | 2.19 GB/s    (34.2k)
           |                      |
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ----
Read       | 3.79 GB/s     (7.4k) | 4.84 GB/s     (4.7k)
Write      | 3.99 GB/s     (7.7k) | 5.16 GB/s     (5.0k)
Total      | 7.78 GB/s    (15.1k) | 10.01 GB/s    (9.7k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 637 Mbits/sec   | 852 Mbits/sec   | 127 ms
Scaleway        | Paris, FR (10G)           | 687 Mbits/sec   | 855 Mbits/sec   | 141 ms
NovoServe       | North Holland, NL (40G)   | 635 Mbits/sec   | 677 Mbits/sec   | 179 ms
Uztelecom       | Tashkent, UZ (10G)        | 628 Mbits/sec   | 691 Mbits/sec   | 242 ms
Clouvider       | NYC, NY, US (10G)         | 875 Mbits/sec   | 467 Mbits/sec   | 74.1 ms
Clouvider       | Dallas, TX, US (10G)      | 926 Mbits/sec   | 932 Mbits/sec   | 40.4 ms
Clouvider       | Los Angeles, CA, US (10G) | 941 Mbits/sec   | 941 Mbits/sec   | 21.9 ms

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 628 Mbits/sec   | 44.2 Mbits/sec  | 127 ms
Scaleway        | Paris, FR (10G)           | 697 Mbits/sec   | 652 Mbits/sec   | 138 ms
NovoServe       | North Holland, NL (40G)   | 620 Mbits/sec   | busy            | 179 ms
Uztelecom       | Tashkent, UZ (10G)        | 550 Mbits/sec   | 517 Mbits/sec   | 242 ms
Clouvider       | NYC, NY, US (10G)         | 808 Mbits/sec   | 690 Mbits/sec   | 72.5 ms
Clouvider       | Dallas, TX, US (10G)      | 905 Mbits/sec   | 912 Mbits/sec   | 40.3 ms
Clouvider       | Los Angeles, CA, US (10G) | 911 Mbits/sec   | 921 Mbits/sec   | 21.9 ms

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2830                          
Multi Core      | 5001   
```

### Bench

```
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 7 7700X 8-Core Processor
 CPU Cores          : 2 @ 4491.540 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 28.5 GB (4.1 GB Used)
 Total Mem          : 1.9 GB (134.7 MB Used)
 Total Swap         : 1024.0 MB (5.2 MB Used)
 System uptime      : 0 days, 0 hour 46 min
 Load average       : 0.12, 0.74, 0.93
 OS                 : Ubuntu 20.04.6 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.4.0-147-generic
 TCP CC             : bbr
 Virtualization     : KVM
 Organization       : AS18450 WebNX, Inc.
 Location           : Los Angeles / US
 Region             : California
----------------------------------------------------------------------
 I/O Speed(1st run) : 3.1 GB/s
 I/O Speed(2nd run) : 3.1 GB/s
 I/O Speed(3rd run) : 3.1 GB/s
 I/O Speed(average) : 3174.4 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency
 Speedtest.net    858.14 Mbps       931.92 Mbps         40.99 ms
 Los Angeles, US  916.78 Mbps       929.13 Mbps         16.70 ms
 Dallas, US       892.39 Mbps       930.09 Mbps         37.19 ms
 Montreal, CA     768.86 Mbps       935.20 Mbps         68.06 ms
 Paris, FR        493.41 Mbps       932.15 Mbps         160.63 ms
 Amsterdam, NL    601.68 Mbps       950.40 Mbps         141.50 ms
 Shanghai, CN     258.37 Mbps       899.73 Mbps         283.84 ms
 Nanjing, CN      523.82 Mbps       943.74 Mbps         158.09 ms
 Guangzhou, CN    3.95 Mbps         703.90 Mbps         172.48 ms
 Hongkong, CN     4.96 Mbps         3.93 Mbps           150.86 ms
 Singapore, SG    488.17 Mbps       881.54 Mbps         161.51 ms
 Tokyo, JP        710.17 Mbps       887.66 Mbps         121.40 ms
----------------------------------------------------------------------
```

### Benchy

```
Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Ubuntu 20.04.6 LTS                 Model       : AMD Ryzen 7 7700X 8-Core Processor
Location   : United States                      Core        : 2 @ 4491.540 MHz
Kernel     : 5.4.0-147-generic                  AES-NI      : ✔ Enabled
Uptime     : 0 days, 1 hrs, 22 mins, 22 secs    VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 1024.0 MiB

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 28.5 GiB                           ASN         : AS18450
Disk Usage : 4.1 GiB (14% Used)                 ISP         : WebNX, Inc.
Mem        : 1.9 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.1 GiB (7% Used)                  IPv6        : ✔ Enabled

Network Performance Test (Region: North America)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |  917.9 Mb/s  |  933.8 Mb/s  |   56.2 ms |
|       | Clouvider   | Dallas, US      |  946.9 Mb/s  |  954.9 Mb/s  |   40.4 ms |
|       | Clouvider   | Phoenix, US     |  958.0 Mb/s  |  960.8 Mb/s  |   30.4 ms |
|       | Clouvider   | Los Angeles, US |  949.5 Mb/s  |  949.2 Mb/s  |   22.0 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |  902.2 Mb/s  |  872.2 Mb/s  |   55.9 ms |
|       | Clouvider   | Dallas, US      |  924.2 Mb/s  |  934.1 Mb/s  |   40.5 ms |
|       | Clouvider   | Phoenix, US     |  932.4 Mb/s  |  938.2 Mb/s  |   30.5 ms |
|       | Clouvider   | Los Angeles, US |  936.8 Mb/s  |  939.5 Mb/s  |   22.0 ms |
+---------------------------------------------------------------------------------+

Ookla Network Speedtest (Region: North America)
+---------------------------------------------------------------------------------------+
| Provider    | Location          | Download     | Upload       | Data Used | Latency   |
+---------------------------------------------------------------------------------------+
| Comcast     | Houston, US       |  933.0 Mb/s  |  788.1 Mb/s  |    2.2 GB |   64.4 ms |
| Spectrum    | New York, US      |  932.8 Mb/s  |  761.7 Mb/s  |    2.3 GB |   69.0 ms |
| Telus       | Edmonton, CA      |  929.3 Mb/s  |  758.2 Mb/s  |    2.1 GB |   73.6 ms |
| Airstream   | Wisconsin, US     |  843.7 Mb/s  |  805.0 Mb/s  |    2.4 GB |   56.2 ms |
| Hivelocity  | Dallas, US        |  925.1 Mb/s  |  821.6 Mb/s  |    2.4 GB |   58.8 ms |
+---------------------------------------------------------------------------------------+
```

### byte-unixbench 性能测试

```
------------------------------------------------------------------------
2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       82250362.3 lps   (10.0 s, 10 samples)
Double-Precision Whetstone                    13671.1 MWIPS (10.0 s, 10 samples)
Execl Throughput                              11121.8 lps   (30.0 s, 4 samples)
File Copy 1024 bufsize 2000 maxblocks       2642904.5 KBps  (30.0 s, 4 samples)
File Copy 256 bufsize 500 maxblocks          704646.0 KBps  (30.0 s, 4 samples)
File Copy 4096 bufsize 8000 maxblocks       8256639.9 KBps  (30.0 s, 4 samples)
Pipe Throughput                             4228287.5 lps   (10.0 s, 10 samples)
Pipe-based Context Switching                 183162.8 lps   (10.0 s, 10 samples)
Process Creation                              35756.5 lps   (30.0 s, 4 samples)
Shell Scripts (1 concurrent)                  30712.4 lpm   (60.0 s, 4 samples)
Shell Scripts (8 concurrent)                   5431.8 lpm   (60.0 s, 4 samples)
System Call Overhead                        5519520.3 lps   (10.0 s, 10 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   82250362.3   7048.0
Double-Precision Whetstone                       55.0      13671.1   2485.7
Execl Throughput                                 43.0      11121.8   2586.5
File Copy 1024 bufsize 2000 maxblocks          3960.0    2642904.5   6674.0
File Copy 256 bufsize 500 maxblocks            1655.0     704646.0   4257.7
File Copy 4096 bufsize 8000 maxblocks          5800.0    8256639.9  14235.6
Pipe Throughput                               12440.0    4228287.5   3398.9
Pipe-based Context Switching                   4000.0     183162.8    457.9
Process Creation                                126.0      35756.5   2837.8
Shell Scripts (1 concurrent)                     42.4      30712.4   7243.5
Shell Scripts (8 concurrent)                      6.0       5431.8   9052.9
System Call Overhead                          15000.0    5519520.3   3679.7
                                                                   ========
System Benchmarks Index Score                                        4051.0

------------------------------------------------------------------------
2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables      160306340.0 lps   (10.0 s, 10 samples)
Double-Precision Whetstone                    27300.4 MWIPS (10.0 s, 10 samples)
Execl Throughput                              20533.8 lps   (29.9 s, 4 samples)
File Copy 1024 bufsize 2000 maxblocks       4787169.2 KBps  (30.0 s, 4 samples)
File Copy 256 bufsize 500 maxblocks         1279569.5 KBps  (30.0 s, 4 samples)
File Copy 4096 bufsize 8000 maxblocks      11688626.5 KBps  (30.0 s, 4 samples)
Pipe Throughput                             8434503.3 lps   (10.0 s, 10 samples)
Pipe-based Context Switching                 910565.9 lps   (10.0 s, 10 samples)
Process Creation                              61375.2 lps   (30.0 s, 4 samples)
Shell Scripts (1 concurrent)                  41571.0 lpm   (60.0 s, 4 samples)
Shell Scripts (8 concurrent)                   5929.4 lpm   (60.0 s, 4 samples)
System Call Overhead                       11243558.2 lps   (10.0 s, 10 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  160306340.0  13736.6
Double-Precision Whetstone                       55.0      27300.4   4963.7
Execl Throughput                                 43.0      20533.8   4775.3
File Copy 1024 bufsize 2000 maxblocks          3960.0    4787169.2  12088.8
File Copy 256 bufsize 500 maxblocks            1655.0    1279569.5   7731.5
File Copy 4096 bufsize 8000 maxblocks          5800.0   11688626.5  20152.8
Pipe Throughput                               12440.0    8434503.3   6780.1
Pipe-based Context Switching                   4000.0     910565.9   2276.4
Process Creation                                126.0      61375.2   4871.0
Shell Scripts (1 concurrent)                     42.4      41571.0   9804.5
Shell Scripts (8 concurrent)                      6.0       5929.4   9882.
System Call Overhead                          15000.0   11243558.2   7495.7
                                                                   ========
System Benchmarks Index Score                                        7534.8
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

### Speedtest

```
      Server: Hivelocity - Los Angeles, CA (id: 19230)
         ISP: WebNX
Idle Latency:     0.86 ms   (jitter: 0.04ms, low: 0.76ms, high: 0.87ms)
    Download:   941.12 Mbps (data used: 425.3 MB)
                 37.21 ms   (jitter: 0.98ms, low: 0.83ms, high: 45.38ms)
      Upload:   941.04 Mbps (data used: 423.9 MB)
                  1.86 ms   (jitter: 0.15ms, low: 1.03ms, high: 2.25ms)
 Packet Loss:     0.0%
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-101-1024x443.png)

### Network-Speed.xyz

```
---------------------------------------------------------------------------
 Basic System Info
---------------------------------------------------------------------------
 CPU Model          : AMD Ryzen 7 7700X 8-Core Processor
 CPU Cores          : 2 @ 4491.540 MHz
 CPU Cache          : 512 KB
 AES-NI             : ✔ Enabled
 VM-x/AMD-V         : ✔ Enabled
 Total Disk         : 28.5 GB (4.1 GB Used)
 Total RAM          : 1.9 GB (137.4 MB Used)
 Total Swap         : 1024.0 MB (5.2 MB Used)
 System uptime      : 0 days, 0 hour 58 min
 Load average       : 0.00, 0.09, 0.43
 OS                 : Ubuntu 20.04.6 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.4.0-147-generic
 Virtualization     : KVM
---------------------------------------------------------------------------
 Basic Network Info
---------------------------------------------------------------------------
 Primary Network    : IPv6
 ISP                : WebNX, Inc.
 ASN                : AS18450 WebNX, Inc.
 Host               : WebNX, Inc.
 Location           : Cheyenne, Wyoming-WY, United States
 Location (IPv4)    : Los Angeles, California, US
---------------------------------------------------------------------------
 Speedtest.net (Region: GLOBAL)
---------------------------------------------------------------------------
 Location         Latency     Loss    DL Speed       UP Speed       Server

 ISP: WebNX

 Nearest          40.88 ms    0.0%    675.72 Mbps    883.50 Mbps    Cox - Wichita - Wichita, KS

 Kochi, IN        216.79 ms   0.0%    947.66 Mbps    369.13 Mbps    Asianet Broadband - Cochin
 Bangalore, IN    242.81 ms   0.0%    916.74 Mbps    339.99 Mbps    Bharti Airtel Ltd - Bangalore
 Chennai, IN      273.08 ms   N/A     918.73 Mbps    267.20 Mbps    Jio - Chennai
 Mumbai, IN       245.00 ms   0.0%    927.47 Mbps    337.99 Mbps    i3D.net - Mumbai
 Delhi, IN        239.77 ms   0.0%    939.47 Mbps    302.39 Mbps    Tata Play Fiber - New Delhi

 Los Angeles, US  15.33 ms    0.0%    930.17 Mbps    912.99 Mbps    ReliableSite Hosting - Los Angeles, CA
 Dallas, US       58.92 ms    0.0%    925.06 Mbps    806.53 Mbps    Hivelocity - Dallas, TX
 New York, US     57.04 ms    0.0%    932.00 Mbps    814.83 Mbps    Clouvider Ltd - New York, NY
 Seattle, US      41.37 ms    N/A     934.35 Mbps    860.31 Mbps    Comcast - Seattle, WA
 Miami, US        61.68 ms    0.0%    950.44 Mbps    785.47 Mbps    AT&T - Miami, FL
 Toronto, CA      57.10 ms    0.0%    938.55 Mbps    792.53 Mbps    Rogers - Toronto, ON

 Paris, FR        161.82 ms   0.0%    938.59 Mbps    488.65 Mbps    ORANGE FRANCE - Paris
 Amsterdam, NL    144.72 ms   0.0%    668.65 Mbps    519.87 Mbps    Clouvider Ltd - Amsterdam
 Warsaw, PL       202.08 ms   0.0%    939.64 Mbps    391.46 Mbps    UPC Polska - Warszawa
 London, UK       127.85 ms   0.0%    953.88 Mbps    622.42 Mbps    VeloxServ Communications - London
 Frankfurt, DE    141.68 ms   0.0%    946.90 Mbps    561.54 Mbps    23M GmbH - Frankfurt Am Main

 Dubai, AE        290.49 ms   0.0%    965.43 Mbps    290.18 Mbps    du - Dubai
 Fujairah, AE     258.15 ms   0.0%    907.97 Mbps    307.05 Mbps    ETISALAT-UAE - Fujairah
 Jeddah, KSA      230.81 ms   0.0%    937.54 Mbps    360.07 Mbps    Saudi Telecom Company

 Shanghai, CU-CN  304.11 ms   0.0%    916.34 Mbps    266.96 Mbps    China Unicom 5G - ShangHai
 Nanjing, CT-CN   152.04 ms   0.0%    945.34 Mbps    565.36 Mbps    China Telecom JiangSu 5G - Nanjing
 Hong Kong, HKG   158.87 ms   N/A     948.83 Mbps    498.29 Mbps    STC - Hong Kong
 Singapore, SG    181.80 ms   0.0%    941.40 Mbps    381.16 Mbps    i3D.net - Singapore
 Jakarta, ID      269.72 ms   0.0%    945.51 Mbps    198.96 Mbps    PT Indosat Tbk - Jakarta
 Tokyo, JP        99.16 ms    N/A     869.16 Mbps    703.42 Mbps    fdcservers.net - Tokyo
---------------------------------------------------------------------------
 Avg DL Speed       : 913.90 Mbps
 Avg UL Speed       : 524.17 Mbps

 Total DL Data      : 35.15 GB
 Total UL Data      : 18.10 GB
 Total Data         : 53.25 GB
---------------------------------------------------------------------------
```

### 国内延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-102-1024x455.png)

### 全球延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-103-1024x564.png)
