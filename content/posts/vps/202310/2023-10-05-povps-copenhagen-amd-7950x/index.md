---
title: "POVPS 哥本哈根 AMD 7950X 测评"
date: "2023-10-05"
categories: 
  - "vps"
  - "eu"
---

新开不久的一个商家,不建议购买，带宽实测跑不到1G。

> ## 套餐
> 
> **_Provider : POVPS  
> Type/Plan : Platinum VPS - P-VPS-01  
> Processor : AMD Ryzen 9 7950X3D (4.5 GHz++)  
> Num of Core : 2 Cores  
> Memory : 2 GB DDR5 RAM  
> Storage : 30 GB NVMe(PCIe 4.0)  
> Bandwidth : Unlimited @ 1 Gbps IN | 1 Gbps OUT  
> Location : Denmark (Copenhagen)  
> Price : $6.31 /month_**

## 测评

### lscpu

```
Architecture:            x86_64
  CPU op-mode(s):        32-bit, 64-bit
  Address sizes:         40 bits physical, 48 bits virtual
  Byte Order:            Little Endian
CPU(s):                  2
  On-line CPU(s) list:   0,1
Vendor ID:               AuthenticAMD
  Model name:            AMD Ryzen 9 7950X3D 16-Core Processor
    CPU family:          25
    Model:               97
    Thread(s) per core:  1
    Core(s) per socket:  1
    Socket(s):           2
    Stepping:            2
    BogoMIPS:            8384.20

Virtualization features: 
  Virtualization:        AMD-V
  Hypervisor vendor:     KVM
  Virtualization type:   full
Caches (sum of all):     
  L1d:                   64 KiB (2 instances)
  L1i:                   64 KiB (2 instances)
  L2:                    2 MiB (2 instances)
  L3:                    256 MiB (2 instances)
```

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 29 minutes
Processor  : AMD Ryzen 9 7950X3D 16-Core Processor
CPU cores  : 2 @ 4192.104 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 2.0 GiB
Disk       : 29.0 GiB
Distro     : Ubuntu 22.04.2 LTS
Kernel     : 5.15.0-76-generic
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : Dominic Scholz trading as ITP-Solutions GmbH \u0026 Co. KG
ASN        : AS213250 Dominic Scholz trading as ITP-Solutions GmbH \u0026 Co. KG
Host       : POVPS.NET
Location   : Frankfurt am Main, Hesse (HE)
Country    : Germany

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 464.38 MB/s (116.0k) | 1.20 GB/s    (18.9k)
Write      | 465.61 MB/s (116.4k) | 1.21 GB/s    (19.0k)
Total      | 930.00 MB/s (232.4k) | 2.42 GB/s    (37.9k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.50 GB/s     (2.9k) | 1.62 GB/s     (1.5k)
Write      | 1.58 GB/s     (3.1k) | 1.73 GB/s     (1.6k)
Total      | 3.09 GB/s     (6.0k) | 3.35 GB/s     (3.2k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 751 Mbits/sec   | busy            | 16.2 ms        
Scaleway        | Paris, FR (10G)           | busy            | 454 Mbits/sec   | 20.5 ms        
NovoServe       | North Holland, NL (40G)   | 731 Mbits/sec   | busy            | 11.5 ms        
Uztelecom       | Tashkent, UZ (10G)        | 624 Mbits/sec   | 325 Mbits/sec   | 77.2 ms        
Clouvider       | NYC, NY, US (10G)         | 577 Mbits/sec   | 77.1 Mbits/sec  | 84.5 ms        
Clouvider       | Dallas, TX, US (10G)      | 477 Mbits/sec   | 90.1 Mbits/sec  | 121 ms         
Clouvider       | Los Angeles, CA, US (10G) | 461 Mbits/sec   | 49.3 Mbits/sec  | 150 ms         
Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2861                          
Multi Core      | 5023
```

### Bench

```
Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU Cores          : 2 @ 4192.104 MHz
 CPU Cache          : 1024 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 29.0 GB (4.6 GB Used)
 Total Mem          : 1.9 GB (277.0 MB Used)
 Total Swap         : 2.0 GB (1.8 MB Used)
 System uptime      : 0 days, 0 hour 28 min
 Load average       : 0.10, 0.42, 0.44
 OS                 : Ubuntu 22.04.2 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.15.0-76-generic
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Offline
 Organization       : AS213250 Dominic Scholz trading as ITP-Solutions GmbH & Co. KG
 Location           : Frankfurt am Main / DE
 Region             : Hesse
----------------------------------------------------------------------
 I/O Speed(1st run) : 2.5 GB/s
 I/O Speed(2nd run) : 2.4 GB/s
 I/O Speed(3rd run) : 2.4 GB/s
 I/O Speed(average) : 2491.7 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    750.16 Mbps       766.31 Mbps         5.99 ms     
 Los Angeles, US  545.45 Mbps       207.61 Mbps         147.95 ms   
 Dallas, US       643.63 Mbps       290.02 Mbps         120.14 ms   
 Montreal, CA     625.35 Mbps       694.36 Mbps         92.04 ms    
 Paris, FR        757.68 Mbps       765.37 Mbps         16.81 ms    
 Amsterdam, NL    722.62 Mbps       312.86 Mbps         11.32 ms    
 Shanghai, CN     445.76 Mbps       501.53 Mbps         179.87 ms   
 Nanjing, CN      407.83 Mbps       404.29 Mbps         208.49 ms   
 Hongkong, CN     436.75 Mbps       723.02 Mbps         185.56 ms   
 Singapore, SG    464.08 Mbps       196.07 Mbps         167.49 ms   
 Tokyo, JP        347.61 Mbps       296.19 Mbps         231.88 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 17 sec
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD Ryzen 9 7950X3D 16-Core Processor (x86_64)
2 cores @ 0 MHz  |  1.9 GiB RAM
Number of Processes: 2  |  Test Iterations: 2  |  Test Duration: Very Long
-
CPU Mark:                          7451
  Integer Math                     16621 Million Operations/s
  Floating Point Math              14789 Million Operations/s
  Prime Numbers                    58.7 Million Primes/s
  Sorting                          10475 Thousand Strings/s
  Encryption                       3722 MB/s
  Compression                      71004 KB/s
  CPU Single Threaded              3970 Million Operations/s
  Physics                          973 Frames/s
  Extended Instructions (SSE)      5975 Million Matrices/s

Memory Mark:                       1878
  Database Operations              2841 Thousand Operations/s
  Memory Read Cached               38183 MB/s
  Memory Read Uncached             36001 MB/s
  Memory Write                     22488 MB/s
  Available RAM                    1457 Megabytes
  Memory Latency                   60 Nanoseconds
  Memory Threaded                  52188 MB/s
```

### byte-unixbench 性能测试

```
Benchmark Run: Thu Oct 05 2023 019:13:19 - 019:41:12
2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       74444796.3 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    12447.8 MWIPS (10.0 s, 7 samples)
Execl Throughput                               7755.5 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       2601910.9 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          694916.3 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       7002892.6 KBps  (30.0 s, 2 samples)
Pipe Throughput                             4108906.7 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 197658.7 lps   (10.0 s, 7 samples)
Process Creation                              18277.4 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  21305.9 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   4198.6 lpm   (60.0 s, 2 samples)
System Call Overhead                        4370098.6 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   74444796.3   6379.2
Double-Precision Whetstone                       55.0      12447.8   2263.2
Execl Throughput                                 43.0       7755.5   1803.6
File Copy 1024 bufsize 2000 maxblocks          3960.0    2601910.9   6570.5
File Copy 256 bufsize 500 maxblocks            1655.0     694916.3   4198.9
File Copy 4096 bufsize 8000 maxblocks          5800.0    7002892.6  12074.0
Pipe Throughput                               12440.0    4108906.7   3303.0
Pipe-based Context Switching                   4000.0     197658.7    494.1
Process Creation                                126.0      18277.4   1450.6
Shell Scripts (1 concurrent)                     42.4      21305.9   5025.0
Shell Scripts (8 concurrent)                      6.0       4198.6   6997.7
System Call Overhead                          15000.0    4370098.6   2913.4
                                                                   ========
System Benchmarks Index Score                                        3364.5

------------------------------------------------------------------------
Benchmark Run: Thu Oct 05 2023 19:41:12 - 20:09:10
2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables      146007625.0 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    24991.2 MWIPS (10.0 s, 7 samples)
Execl Throughput                              11330.7 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       5112727.6 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks         1395923.9 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks      12838887.9 KBps  (30.0 s, 2 samples)
Pipe Throughput                             8204151.0 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 802204.9 lps   (10.0 s, 7 samples)
Process Creation                              33941.6 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  30837.0 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   4221.2 lpm   (60.0 s, 2 samples)
System Call Overhead                        8671357.8 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  146007625.0  12511.4
Double-Precision Whetstone                       55.0      24991.2   4543.8
Execl Throughput                                 43.0      11330.7   2635.0
File Copy 1024 bufsize 2000 maxblocks          3960.0    5112727.6  12910.9
File Copy 256 bufsize 500 maxblocks            1655.0    1395923.9   8434.6
File Copy 4096 bufsize 8000 maxblocks          5800.0   12838887.9  22136.0
Pipe Throughput                               12440.0    8204151.0   6595.0
Pipe-based Context Switching                   4000.0     802204.9   2005.5
Process Creation                                126.0      33941.6   2693.8
Shell Scripts (1 concurrent)                     42.4      30837.0   7272.9
Shell Scripts (8 concurrent)                      6.0       4221.2   7035.3
System Call Overhead                          15000.0    8671357.8   5780.9
                                                                   ========
System Benchmarks Index Score                                        6285.9
```

### SpeedTest

```
   Speedtest by Ookla

      Server: WebseitenDesigner.com - Hannover (id: 47786)
         ISP: ITP-Solutions GmbH & Co. KG
Idle Latency:     7.01 ms   (jitter: 0.81ms, low: 6.31ms, high: 7.59ms)
    Download:   620.39 Mbps (data used: 852.3 MB)                                                   
                 16.42 ms   (jitter: 6.54ms, low: 7.29ms, high: 47.66ms)
      Upload:   660.69 Mbps (data used: 774.7 MB)                                                   
                 40.76 ms   (jitter: 24.37ms, low: 11.89ms, high: 333.10ms)
```

![](https://catcat.blog/wp-content/uploads/2023/10/image-3-1024x343.png)

### Network-Speed.xyz

```
---------------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU Cores          : 2 @ 4192.104 MHz
 CPU Cache          : 1024 KB
 AES-NI             : ✔ Enabled
 VM-x/AMD-V         : ✔ Enabled
 Total Disk         : 29.0 GB (4.6 GB Used)
 Total RAM          : 1.9 GB (261.5 MB Used)
 Total Swap         : 2.0 GB (1.8 MB Used)
 System uptime      : 0 days, 0 hour 39 min
 Load average       : 0.03, 0.12, 0.25
 OS                 : Ubuntu 22.04.2 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.15.0-76-generic
 Virtualization     : KVM
---------------------------------------------------------------------------
 Basic Network Info
---------------------------------------------------------------------------
 Primary Network    : IPv4
 ISP                : Dominic Scholz trading as ITP-Solutions GmbH & Co. KG
 ASN                : AS213250 Dominic Scholz trading as ITP-Solutions GmbH & Co. KG
 ASN (IPv4)         : AS213250 Dominic Scholz trading as ITP-Solutions GmbH & Co. KG
 Host               : POVPS.NET
 Location           : Frankfurt am Main, Hesse-HE, Germany
---------------------------------------------------------------------------
 Speedtest.net (Region: GLOBAL)
---------------------------------------------------------------------------
 Location         Latency     Loss    DL Speed       UP Speed       Server      

 ISP: ITP-Solutions GmbH & Co. KG 

 Nearest          6.10 ms     0.0%    768.98 Mbps    757.70 Mbps    WebseitenDesigner.com - Hannover 

 Kochi, IN        173.22 ms   0.0%    406.20 Mbps    478.53 Mbps    Asianet Broadband - Cochin 
 Bangalore, IN    135.38 ms   0.3%    451.21 Mbps    546.13 Mbps    Bharti Airtel Ltd - Bangalore 
 Chennai, IN      150.84 ms   0.3%    340.62 Mbps    531.80 Mbps    Tata Play Fiber - Chennai 
 Mumbai, IN       128.13 ms   1.3%    314.87 Mbps    515.06 Mbps    i3D.net - Mumbai 
 Delhi, IN        141.45 ms   0.3%    373.00 Mbps    554.65 Mbps    Tata Teleservices Ltd - New Delhi 

 Seattle, US      162.43 ms   0.0%    296.63 Mbps    476.52 Mbps    DediPath - Seattle, WA 
 Los Angeles, US  143.58 ms   0.0%    185.31 Mbps    564.82 Mbps    ReliableSite Hosting - Los Angeles, CA 
 Dallas, US       122.69 ms   0.3%    574.55 Mbps    609.98 Mbps    Hivelocity - Dallas, TX 
 Miami, US        127.44 ms   0.0%    278.75 Mbps    657.94 Mbps    AT&T - Miami, FL 
 New York, US     84.53 ms    0.0%    283.60 Mbps    514.41 Mbps    Clouvider Ltd - New York, NY 
 Toronto, CA      101.76 ms   0.0%    347.47 Mbps    679.89 Mbps    Rogers - Toronto, ON 

 London, UK       16.19 ms    5.7%    761.47 Mbps    758.28 Mbps    VeloxServ Communications - London 
 Amsterdam, NL    15.90 ms    0.0%    311.79 Mbps    737.58 Mbps    Clouvider Ltd - Amsterdam 
 Paris, FR        15.89 ms    N/A     766.37 Mbps    737.88 Mbps    Axione - Paris 
 Frankfurt, DE    5.79 ms     0.0%    754.62 Mbps    742.16 Mbps    23M GmbH - Frankfurt Am Main 
 Warsaw, PL       25.01 ms    0.0%    208.19 Mbps    711.29 Mbps    UPC Polska - Warszawa 
 Bucharest, RO    32.78 ms    0.0%    205.63 Mbps    661.26 Mbps    Vodafone Romania Fixed – Bucharest - Bucharest 

 Jeddah, KSA      83.20 ms    1.7%    560.22 Mbps    620.17 Mbps    Saudi Telecom Company 
 Dubai, AE        132.38 ms   0.0%    483.29 Mbps    612.51 Mbps    du - Dubai  
 Fujairah, AE     111.67 ms   6.7%    780.72 Mbps    650.93 Mbps    ETISALAT-UAE - Fujairah 

 Tokyo, JP        250.55 ms   N/A     592.03 Mbps    312.03 Mbps    fdcservers.net - Tokyo 
 Shanghai, CU-CN  192.94 ms   0.3%    596.43 Mbps    400.26 Mbps    China Unicom 5G - ShangHai 
 Nanjing, CT-CN   185.28 ms   0.0%    3.85 Mbps      421.72 Mbps    China Telecom JiangSu 5G - Nanjing 
 Hong Kong, HKG   172.87 ms   N/A     123.54 Mbps    430.27 Mbps    STC - Hong Kong 
 Singapore, SG    237.32 ms   0.0%    243.64 Mbps    331.19 Mbps    i3D.net - Singapore 
 Jakarta, ID      196.71 ms   1.0%    429.19 Mbps    422.09 Mbps    PT. Telekomunikasi Indonesia - Jakarta 
---------------------------------------------------------------------------
 Avg DL Speed       : 423.78 Mbps
 Avg UL Speed       : 571.74 Mbps
```
