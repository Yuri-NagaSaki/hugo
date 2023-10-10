---
title: "Madcityservers 7950x 测评"
date: "2023-09-04"
categories: 
  - "vps"
  - "performance"
  - "usa"
---

> 风评不大好，谨慎购买

## 套餐

![](https://catcat.blog/wp-content/uploads/2023/09/image-1024x526.png)

## 测试

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 7 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 4 @ 4499.980 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 7.7 GiB
Swap       : 0.0 KiB
Disk       : 79.1 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-8-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Free Cloud Hosting Inc.
ASN        : AS23470 ReliableSite.Net LLC
Host       : Madcityservers LLC
Location   : West Chicago, Illinois (IL)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 593.96 MB/s (143.4k) | 4.26 GB/s    (66.1k)
Write      | 565.47 MB/s (143.8k) | 4.25 GB/s    (66.5k)
Total      | 1.14 GB/s   (287.3k) | 8.51 GB/s   (132.6k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.83 GB/s     (9.2k) | 4.61 GB/s     (4.5k)
Write      | 5.02 GB/s     (9.7k) | 4.91 GB/s     (4.8k)
Total      | 9.85 GB/s    (18.9k) | 9.53 GB/s     (9.3k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 709 Mbits/sec   | 1.79 Gbits/sec  | 67.2 ms        
Scaleway        | Paris, FR (10G)           | 641 Mbits/sec   | 2.39 Gbits/sec  | 76.6 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 77.6 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | busy            | 164 ms         
Clouvider       | NYC, NY, US (10G)         | 660 Mbits/sec   | 2.27 Gbits/sec  | 2.03 ms        
Clouvider       | Dallas, TX, US (10G)      | 593 Mbits/sec   | 5.04 Gbits/sec  | 37.5 ms        
Clouvider       | Los Angeles, CA, US (10G) | busy            | busy            | -- 

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 480 Mbits/sec   | 2.72 Gbits/sec  | 67.2 ms        
Scaleway        | Paris, FR (10G)           | 429 Mbits/sec   | 2.63 Gbits/sec  | 71.9 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 75.6 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | busy            | 164 ms         
Clouvider       | NYC, NY, US (10G)         | 821 Mbits/sec   | busy            | 2.10 ms        
Clouvider       | Dallas, TX, US (10G)      | 749 Mbits/sec   | 5.04 Gbits/sec  | 37.5 ms        
Clouvider       | Los Angeles, CA, US (10G) | busy            | busy            | 59.7 ms 

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2798                           
Multi Core      | 8281                          
       
```

### Benchmark

```
Dhrystone 2 using register variables       78754641.2 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    13316.1 MWIPS (10.0 s, 7 samples)
Execl Throughput                               8987.0 lps   (29.9 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       2925742.4 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          780580.9 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       8376783.4 KBps  (30.0 s, 2 samples)
Pipe Throughput                             4407756.1 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 143571.0 lps   (10.0 s, 7 samples)
Process Creation                              20785.7 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  28624.8 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   7930.7 lpm   (60.0 s, 2 samples)
System Call Overhead                        4687056.0 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   78754641.2   6748.5
Double-Precision Whetstone                       55.0      13316.1   2421.1
Execl Throughput                                 43.0       8987.0   2090.0
File Copy 1024 bufsize 2000 maxblocks          3960.0    2925742.4   7388.2
File Copy 256 bufsize 500 maxblocks            1655.0     780580.9   4716.5
File Copy 4096 bufsize 8000 maxblocks          5800.0    8376783.4  14442.7
Pipe Throughput                               12440.0    4407756.1   3543.2
Pipe-based Context Switching                   4000.0     143571.0    358.9
Process Creation                                126.0      20785.7   1649.7
Shell Scripts (1 concurrent)                     42.4      28624.8   6751.1
Shell Scripts (8 concurrent)                      6.0       7930.7  13217.9
System Call Overhead                          15000.0    4687056.0   3124.7
                                                                   ========
System Benchmarks Index Score                                        3832.9

------------------------------------------------------------------------
4 CPUs in system; running 4 parallel copies of tests

Dhrystone 2 using register variables      302860184.9 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    52184.5 MWIPS (10.0 s, 7 samples)
Execl Throughput                              19701.4 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks      10755422.7 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks         3029830.8 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks      20022095.1 KBps  (30.0 s, 2 samples)
Pipe Throughput                            17035367.2 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                1780152.4 lps   (10.0 s, 7 samples)
Process Creation                              38997.3 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  59806.0 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   8756.4 lpm   (60.0 s, 2 samples)
System Call Overhead                       18113612.1 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  302860184.9  25952.0
Double-Precision Whetstone                       55.0      52184.5   9488.1
Execl Throughput                                 43.0      19701.4   4581.7
File Copy 1024 bufsize 2000 maxblocks          3960.0   10755422.7  27160.2
File Copy 256 bufsize 500 maxblocks            1655.0    3029830.8  18307.1
File Copy 4096 bufsize 8000 maxblocks          5800.0   20022095.1  34520.9
Pipe Throughput                               12440.0   17035367.2  13694.0
Pipe-based Context Switching                   4000.0    1780152.4   4450.4
Process Creation                                126.0      38997.3   3095.0
Shell Scripts (1 concurrent)                     42.4      59806.0  14105.2
Shell Scripts (8 concurrent)                      6.0       8756.4  14594.0
System Call Overhead                          15000.0   18113612.1  12075.7
                                                                   ========
System Benchmarks Index Score                                       12018.2
```

### PassMark

```
AMD Ryzen 9 7950X 16-Core Processor (x86_64)
4 cores @ 0 MHz  |  7.8 GiB RAM
Number of Processes: 4  |  Test Iterations: 1  |  Test Duration: Very Long
-
CPU Mark:                          14817
  Integer Math                     34079 Million Operations/s
  Floating Point Math              30394 Million Operations/s
  Prime Numbers                    119 Million Primes/s
  Sorting                          20528 Thousand Strings/s
  Encryption                       7473 MB/s
  Compression                      144363 KB/s
  CPU Single Threaded              4097 Million Operations/s
  Physics                          1914 Frames/s
  Extended Instructions (SSE)      12949 Million Matrices/s

Memory Mark:                       2614
  Database Operations              4466 Thousand Operations/s
  Memory Read Cached               39491 MB/s
  Memory Read Uncached             35104 MB/s
  Memory Write                     19612 MB/s
  Available RAM                    6706 Megabytes
  Memory Latency                   68 Nanoseconds
  Memory Threaded                  44646 MB/s
```
