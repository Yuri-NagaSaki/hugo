---
title: "英国 AllHost AMD 7900 测评"
date: "2023-09-08"
categories: 
  - "vps"
  - "performance"
  - "eu"
---

> ## 套餐

![](https://catcat.blog/wp-content/uploads/2023/09/image-51-1024x85.png)

## 测评

### Yabs

```

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 2 minutes
Processor  : AMD Ryzen 9 7900 12-Core Processor
CPU cores  : 3 @ 3700.018 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ❌ Disabled
RAM        : 4.0 GiB
Swap       : 0.0 KiB
Disk       : 87.1 GiB
Distro     : Ubuntu 22.04.3 LTS
Kernel     : 5.15.0-78-generic
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : AH CLOUD LTD
ASN        : AS207108 AH CLOUD LTD
Host       : AH CLOUD LTD
Location   : Poplar, England (ENG)
Country    : United Kingdom

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 240.87 MB/s  (60.2k) | 1.01 GB/s    (15.9k)
Write      | 241.50 MB/s  (60.3k) | 1.02 GB/s    (15.9k)
Total      | 482.38 MB/s (120.5k) | 2.04 GB/s    (31.9k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 971.41 MB/s   (1.8k) | 960.96 MB/s    (938)
Write      | 1.02 GB/s     (1.9k) | 1.02 GB/s     (1.0k)
Total      | 1.99 GB/s     (3.8k) | 1.98 GB/s     (1.9k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 2.17 Gbits/sec  | 1.89 Gbits/sec  | 4.48 ms        
Scaleway        | Paris, FR (10G)           | 2.15 Gbits/sec  | busy            | 11.4 ms        
NovoServe       | North Holland, NL (40G)   | 2.13 Gbits/sec  | 1.55 Gbits/sec  | 9.63 ms        
Uztelecom       | Tashkent, UZ (10G)        | 2.00 Gbits/sec  | 730 Mbits/sec   | 118 ms         
Clouvider       | NYC, NY, US (10G)         | 2.05 Gbits/sec  | 210 Mbits/sec   | 73.4 ms        
Clouvider       | Dallas, TX, US (10G)      | 1.68 Gbits/sec  | 212 Mbits/sec   | 106 ms         
Clouvider       | Los Angeles, CA, US (10G) | 1.34 Gbits/sec  | 97.6 Mbits/sec  | 130 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 2.15 Gbits/sec  | 1.87 Gbits/sec  | 4.45 ms        
Scaleway        | Paris, FR (10G)           | busy            | busy            | 12.0 ms        
NovoServe       | North Holland, NL (40G)   | 2.19 Gbits/sec  | 1.59 Gbits/sec  | 9.67 ms        
Uztelecom       | Tashkent, UZ (10G)        | 1.50 Gbits/sec  | 732 Mbits/sec   | 119 ms         
Clouvider       | NYC, NY, US (10G)         | 2.06 Gbits/sec  | 211 Mbits/sec   | 73.4 ms        
Clouvider       | Dallas, TX, US (10G)      | 1.66 Gbits/sec  | 219 Mbits/sec   | 106 ms         
Clouvider       | Los Angeles, CA, US (10G) | 1.34 Gbits/sec  | 101 Mbits/sec   | 129 ms         
```

### **Bench**

```
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7900 12-Core Processor
 CPU Cores          : 3 @ 3700.018 MHz
 CPU Cache          : 1024 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Disabled
 Total Disk         : 87.1 GB (2.8 GB Used)
 Total Mem          : 4.0 GB (318.3 MB Used)
 System uptime      : 0 days, 0 hour 6 min
 Load average       : 0.28, 0.20, 0.07
 OS                 : Ubuntu 22.04.3 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.15.0-78-generic
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS207108 AH CLOUD LTD
 Location           : Coventry / GB
 Region             : England
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.0 GB/s
 I/O Speed(2nd run) : 1.1 GB/s
 I/O Speed(3rd run) : 1.0 GB/s
 I/O Speed(average) : 1058.1 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    1999.85 Mbps      1631.88 Mbps        3.68 ms     
 Los Angeles, US  599.38 Mbps       1023.09 Mbps        133.40 ms   
 Dallas, US       771.68 Mbps       1339.73 Mbps        105.47 ms   
 Montreal, CA     566.57 Mbps       930.99 Mbps         77.40 ms    
 Paris, FR        2005.91 Mbps      1868.20 Mbps        11.67 ms    
 Amsterdam, NL    1999.53 Mbps      1880.24 Mbps        10.56 ms    
 Shanghai, CN     331.28 Mbps       1528.05 Mbps        256.05 ms   
 Nanjing, CN      31.47 Mbps        1000.85 Mbps        269.06 ms   
 Hongkong, CN     411.59 Mbps       1813.66 Mbps        205.39 ms   
 Singapore, SG    479.52 Mbps       57.44 Mbps          165.44 ms   
 Tokyo, JP        294.26 Mbps       6.26 Mbps           262.67 ms   
----------------------------------------------------------------------
```

### **UnixBench**

```
3 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       74248937.5 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    12462.0 MWIPS (9.9 s, 7 samples)
Execl Throughput                               8568.0 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       2761452.2 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          739737.1 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       7633122.0 KBps  (30.0 s, 2 samples)
Pipe Throughput                             4181189.7 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 307501.5 lps   (10.0 s, 7 samples)
Process Creation                              18092.2 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  23124.3 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   6286.5 lpm   (60.0 s, 2 samples)
System Call Overhead                        4439258.8 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   74248937.5   6362.4
Double-Precision Whetstone                       55.0      12462.0   2265.8
Execl Throughput                                 43.0       8568.0   1992.6
File Copy 1024 bufsize 2000 maxblocks          3960.0    2761452.2   6973.4
File Copy 256 bufsize 500 maxblocks            1655.0     739737.1   4469.7
File Copy 4096 bufsize 8000 maxblocks          5800.0    7633122.0  13160.6
Pipe Throughput                               12440.0    4181189.7   3361.1
Pipe-based Context Switching                   4000.0     307501.5    768.8
Process Creation                                126.0      18092.2   1435.9
Shell Scripts (1 concurrent)                     42.4      23124.3   5453.8
Shell Scripts (8 concurrent)                      6.0       6286.5  10477.5
System Call Overhead                          15000.0    4439258.8   2959.5
                                                                   ========
System Benchmarks Index Score                                        3736.0

------------------------------------------------------------------------
3 CPUs in system; running 3 parallel copies of tests

Dhrystone 2 using register variables      216635558.8 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    37459.4 MWIPS (9.9 s, 7 samples)
Execl Throughput                              15703.7 lps   (29.5 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       7700330.2 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks         2121150.8 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks      15705533.8 KBps  (30.0 s, 2 samples)
Pipe Throughput                            12248121.5 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                1077421.4 lps   (10.0 s, 7 samples)
Process Creation                              34494.6 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  43806.4 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   6567.6 lpm   (60.0 s, 2 samples)
System Call Overhead                       12747363.3 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  216635558.8  18563.5
Double-Precision Whetstone                       55.0      37459.4   6810.8
Execl Throughput                                 43.0      15703.7   3652.0
File Copy 1024 bufsize 2000 maxblocks          3960.0    7700330.2  19445.3
File Copy 256 bufsize 500 maxblocks            1655.0    2121150.8  12816.6
File Copy 4096 bufsize 8000 maxblocks          5800.0   15705533.8  27078.5
Pipe Throughput                               12440.0   12248121.5   9845.8
Pipe-based Context Switching                   4000.0    1077421.4   2693.6
Process Creation                                126.0      34494.6   2737.7
Shell Scripts (1 concurrent)                     42.4      43806.4  10331.7
Shell Scripts (8 concurrent)                      6.0       6567.6  10946.0
System Call Overhead                          15000.0   12747363.3   8498.2
                                                                   ========
System Benchmarks Index Score                                        8806.0
```

### PassMark

```
AMD Ryzen 9 7900 12-Core Processor (x86_64)
3 cores @ 0 MHz  |  4.0 GiB RAM
Number of Processes: 3  |  Test Iterations: 2  |  Test Duration: Very Long
-
CPU Mark:                          10540
  Integer Math                     24328 Million Operations/s
  Floating Point Math              18313 Million Operations/s
  Prime Numbers                    85.9 Million Primes/s
  Sorting                          15115 Thousand Strings/s
  Encryption                       5353 MB/s
  Compression                      104091 KB/s
  CPU Single Threaded              3820 Million Operations/s
  Physics                          1371 Frames/s
  Extended Instructions (SSE)      9294 Million Matrices/s

Memory Mark:                       2204
  Database Operations              3487 Thousand Operations/s
  Memory Read Cached               38086 MB/s
  Memory Read Uncached             34425 MB/s
  Memory Write                     19909 MB/s
  Available RAM                    2548 Megabytes
  Memory Latency                   63 Nanoseconds
  Memory Threaded                  42070 MB/s
```

### Geekbench5

![](https://catcat.blog/wp-content/uploads/2023/09/image-52-1024x278.png)

### Geekbench6

![](https://catcat.blog/wp-content/uploads/2023/09/image-53-1024x239.png)

### SpeedTest

![](https://catcat.blog/wp-content/uploads/2023/09/image-54-1024x388.png)
