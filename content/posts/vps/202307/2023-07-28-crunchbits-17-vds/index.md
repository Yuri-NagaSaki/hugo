---
title: "Crunchbits 17$ 7950x VDS测评"
date: "2023-07-28"
categories: 
  - "vps"
  - "usa"
---

## 套餐

- 1 core / 2 threads \[DEDICATED\]

- 4GB DDR5 (4800MHz)

- 100GB Gen4 NVME

- 960GB RAID-10 HDD Storage

- 20TB @ 2.5Gbps

- 1 IPv4 & /64 IPv6 included

- 1 Backup Slot

- Price: $17/mo **$14.11/mo** -- 17% off lifetime w/code: _ZIGIGAGS_

## 测评

### YABS

```

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 59 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 2 @ 4499.984 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 0.0 KiB
Disk       : 96.8 GiB
Distro     : Ubuntu 22.04.2 LTS
Kernel     : 5.15.0-76-generic
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Redoubt Networks
ASN        : AS400304 REDOUBT NETWORKS
Host       : Redoubt Networks
Location   : Spokane, Washington (WA)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 610.96 MB/s (152.7k) | 5.65 GB/s    (88.3k)
Write      | 612.57 MB/s (153.1k) | 5.68 GB/s    (88.7k)
Total      | 1.22 GB/s   (305.8k) | 11.33 GB/s  (177.1k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 5.52 GB/s    (10.7k) | 4.69 GB/s     (4.5k)
Write      | 5.81 GB/s    (11.3k) | 5.01 GB/s     (4.8k)
Total      | 11.33 GB/s   (22.1k) | 9.70 GB/s     (9.4k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 949 Mbits/sec   | 334 Mbits/sec   | 129 ms         
Scaleway        | Paris, FR (10G)           | 1.54 Gbits/sec  | busy            | 143 ms         
NovoServe       | North Holland, NL (40G)   | 1.26 Gbits/sec  | busy            | 138 ms         
Uztelecom       | Tashkent, UZ (10G)        | 938 Mbits/sec   | 717 Mbits/sec   | 220 ms         
Clouvider       | NYC, NY, US (10G)         | 2.38 Gbits/sec  | 884 Mbits/sec   | 63.1 ms        
Clouvider       | Dallas, TX, US (10G)      | 2.62 Gbits/sec  | 1.53 Gbits/sec  | 67.1 ms        
Clouvider       | Los Angeles, CA, US (10G) | 2.67 Gbits/sec  | 1.54 Gbits/sec  | 40.8 ms        

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 911 Mbits/sec   | 332 Mbits/sec   | 129 ms         
Scaleway        | Paris, FR (10G)           | 1.45 Gbits/sec  | busy            | 132 ms         
NovoServe       | North Holland, NL (40G)   | 1.22 Gbits/sec  | busy            | 138 ms         
Uztelecom       | Tashkent, UZ (10G)        | 899 Mbits/sec   | 714 Mbits/sec   | 220 ms         
Clouvider       | NYC, NY, US (10G)         | 2.61 Gbits/sec  | 879 Mbits/sec   | 63.1 ms        
Clouvider       | Dallas, TX, US (10G)      | 2.40 Gbits/sec  | 1.79 Gbits/sec  | 66.9 ms        
Clouvider       | Los Angeles, CA, US (10G) | 2.65 Gbits/sec  | 1.67 Gbits/sec  | 40.5 ms 

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 3033                          
Multi Core      | 5324    
```

### CPU

```
Architecture:            x86_64
  CPU op-mode(s):        32-bit, 64-bit
  Address sizes:         48 bits physical, 48 bits virtual
  Byte Order:            Little Endian
CPU(s):                  2
  On-line CPU(s) list:   0,1
Vendor ID:               AuthenticAMD
  Model name:            AMD Ryzen 9 7950X 16-Core Processor
    CPU family:          25
    Model:               97
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    Stepping:            2
    BogoMIPS:            8999.96
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx mmx
                         ext fxsr_opt pdpe1gb rdtscp lm rep_good nopl cpuid extd_apicid tsc_known_freq pni pclmulqdq ssse3 fma cx16 sse4_1 s
                         se4_2 x2apic movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand hypervisor lahf_lm cmp_legacy svm cr8_legacy
                          abm sse4a misalignsse 3dnowprefetch osvw perfctr_core ssbd ibrs ibpb stibp vmmcall fsgsbase tsc_adjust bmi1 avx2 s
                         mep bmi2 erms invpcid avx512f avx512dq rdseed adx smap avx512ifma clflushopt clwb avx512cd sha_ni avx512bw avx512vl
                          xsaveopt xsavec xgetbv1 xsaves avx512_bf16 clzero xsaveerptr wbnoinvd arat npt lbrv nrip_save tsc_scale vmcb_clean
                          pausefilter pfthreshold v_vmsave_vmload vgif avx512vbmi umip pku ospke avx512_vbmi2 gfni vaes vpclmulqdq avx512_vn
                         ni avx512_bitalg avx512_vpopcntdq rdpid fsrm arch_capabilities
Virtualization features: 
  Virtualization:        AMD-V
  Hypervisor vendor:     KVM
  Virtualization type:   full
Caches (sum of all):     
  L1d:                   64 KiB (2 instances)
  L1i:                   64 KiB (2 instances)
  L2:                    2 MiB (2 instances)
  L3:                    128 MiB (2 instances)
```

## **UnixBench**

```
Dhrystone 2 using register variables       79349675.4 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    13716.5 MWIPS (10.0 s, 7 samples)
Execl Throughput                               9492.4 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       2975381.6 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          806145.6 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       8233721.3 KBps  (30.0 s, 2 samples)
Pipe Throughput                             4549971.1 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 109043.6 lps   (10.0 s, 7 samples)
Process Creation                              13845.7 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  22165.4 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   4482.5 lpm   (60.0 s, 2 samples)
System Call Overhead                        4751109.0 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   79349675.4   6799.5
Double-Precision Whetstone                       55.0      13716.5   2493.9
Execl Throughput                                 43.0       9492.4   2207.5
File Copy 1024 bufsize 2000 maxblocks          3960.0    2975381.6   7513.6
File Copy 256 bufsize 500 maxblocks            1655.0     806145.6   4871.0
File Copy 4096 bufsize 8000 maxblocks          5800.0    8233721.3  14196.1
Pipe Throughput                               12440.0    4549971.1   3657.5
Pipe-based Context Switching                   4000.0     109043.6    272.6
Process Creation                                126.0      13845.7   1098.9
Shell Scripts (1 concurrent)                     42.4      22165.4   5227.7
Shell Scripts (8 concurrent)                      6.0       4482.5   7470.8
System Call Overhead                          15000.0    4751109.0   3167.4
                                                                   ========
System Benchmarks Index Score                                        3428.3

------------------------------------------------------------------------

Dhrystone 2 using register variables      160737649.8 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    27170.9 MWIPS (10.0 s, 7 samples)
Execl Throughput                              10767.6 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       5825996.5 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks         1571017.4 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks      16366218.9 KBps  (30.0 s, 2 samples)
Pipe Throughput                             9152522.5 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 959006.7 lps   (10.0 s, 7 samples)
Process Creation                              30253.8 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  31465.0 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   4587.1 lpm   (60.0 s, 2 samples)
System Call Overhead                        9623453.8 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  160737649.8  13773.6
Double-Precision Whetstone                       55.0      27170.9   4940.2
Execl Throughput                                 43.0      10767.6   2504.1
File Copy 1024 bufsize 2000 maxblocks          3960.0    5825996.5  14712.1
File Copy 256 bufsize 500 maxblocks            1655.0    1571017.4   9492.6
File Copy 4096 bufsize 8000 maxblocks          5800.0   16366218.9  28217.6
Pipe Throughput                               12440.0    9152522.5   7357.3
Pipe-based Context Switching                   4000.0     959006.7   2397.5
Process Creation                                126.0      30253.8   2401.1
Shell Scripts (1 concurrent)                     42.4      31465.0   7421.0
Shell Scripts (8 concurrent)                      6.0       4587.1   7645.1
System Call Overhead                          15000.0    9623453.8   6415.6
                                                                   ========
System Benchmarks Index Score                                        6832.6
```

### PerformanceTest测试

```
AMD Ryzen 9 7950X 16-Core Processor (x86_64)
2 cores @ 0 MHz  |  3.8 GiB RAM
Number of Processes: 2  |  Test Iterations: 2  |  Test Duration: Very Long
-
CPU Mark:                          8031
  Integer Math                     17800 Million Operations/s
  Floating Point Math              15879 Million Operations/s
  Prime Numbers                    64.7 Million Primes/s
  Sorting                          11149 Thousand Strings/s
  Encryption                       3905 MB/s
  Compression                      75985 KB/s
  CPU Single Threaded              4179 Million Operations/s
  Physics                          1046 Frames/s
  Extended Instructions (SSE)      6997 Million Matrices/s

Memory Mark:                       2641
  Database Operations              3021 Thousand Operations/s
  Memory Read Cached               40365 MB/s
  Memory Read Uncached             39559 MB/s
  Memory Write                     25959 MB/s
  Available RAM                    3406 Megabytes
  Memory Latency                   55 Nanoseconds
  Memory Threaded                  63104 MB/s
```

### **Bench** 测试

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X 16-Core Processor
 CPU Cores          : 2 @ 4499.984 MHz
 CPU Cache          : 1024 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 96.8 GB (2.8 GB Used)
 Total Mem          : 3.8 GB (203.5 MB Used)
 System uptime      : 0 days, 0 hour 59 min
 Load average       : 0.16, 0.14, 0.45
 OS                 : Ubuntu 22.04.2 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.15.0-76-generic
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS400304 REDOUBT NETWORKS
 Location           : Liberty Lake / US
 Region             : Washington
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.8 GB/s
 I/O Speed(2nd run) : 1.9 GB/s
 I/O Speed(3rd run) : 1.9 GB/s
 I/O Speed(average) : 1911.5 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    2078.70 Mbps      2322.68 Mbps        44.16 ms    
 Los Angeles, US  1946.37 Mbps      2297.01 Mbps        37.03 ms    
 Dallas, US       1380.71 Mbps      2292.02 Mbps        54.87 ms    
 Montreal, CA     146.58 Mbps       934.69 Mbps         65.98 ms    
 Paris, FR        688.10 Mbps       2163.58 Mbps        135.74 ms   
 Amsterdam, NL    574.17 Mbps       1525.80 Mbps        146.10 ms   
 Shanghai, CN     55.49 Mbps        403.25 Mbps         249.70 ms   
 Nanjing, CN      55.07 Mbps        1055.99 Mbps        233.98 ms   
 Singapore, SG    448.30 Mbps       1532.01 Mbps        178.35 ms   
 Tokyo, JP        646.37 Mbps       1802.46 Mbps        92.65 ms    
----------------------------------------------------------------------
```

### **Benchy** 测试

```
Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Ubuntu 22.04.2 LTS                 Model       : AMD Ryzen 9 7950X 16-Core Processor
Location   : United States                      Core        : 2 @ 4499.984 MHz
Kernel     : 5.15.0-76-generic                  AES-NI      : ✔ Enabled
Uptime     : 0 days, 1 hrs, 19 mins, 18 secs    VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 0.0 KiB   

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 96.7 GiB                           ASN         : AS400304  
Disk Usage : 2.8 GiB (3% Used)                  ISP         : REDOUBT NETWORKS
Mem        : 3.8 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.2 GiB (6% Used)                  IPv6        : ✔ Enabled

Network Performance Test (Region: North America)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |    2.1 Gb/s  |    1.7 Gb/s  |   53.8 ms |
|       | Clouvider   | Dallas, US      |    2.4 Gb/s  |    1.3 Gb/s  |   67.2 ms |
|       | Clouvider   | Phoenix, US     |    2.7 Gb/s  |    1.2 Gb/s  |   45.9 ms |
|       | Clouvider   | Los Angeles, US |    2.6 Gb/s  |    1.3 Gb/s  |   40.7 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |    1.9 Gb/s  |    1.5 Gb/s  |   53.7 ms |
|       | Clouvider   | Dallas, US      |    2.2 Gb/s  |    1.3 Gb/s  |   67.2 ms |
|       | Clouvider   | Phoenix, US     |    2.6 Gb/s  |    1.3 Gb/s  |   45.8 ms |
|       | Clouvider   | Los Angeles, US |    2.6 Gb/s  |    1.7 Gb/s  |   40.6 ms |
```

## 2023年9月4日测试

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 3 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 2 @ 4499.992 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 0.0 KiB
Disk       : 100.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-20-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Redoubt Networks
ASN        : AS400304 REDOUBT NETWORKS
Host       : Redoubt Networks
Location   : Spokane, Washington (WA)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 504.30 MB/s (126.0k) | 3.53 GB/s    (55.2k)
Write      | 505.63 MB/s (126.4k) | 3.55 GB/s    (55.5k)
Total      | 1.00 GB/s   (252.4k) | 7.09 GB/s   (110.8k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.60 GB/s     (7.0k) | 3.59 GB/s     (3.5k)
Write      | 3.80 GB/s     (7.4k) | 3.83 GB/s     (3.7k)
Total      | 7.41 GB/s    (14.4k) | 7.43 GB/s     (7.2k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 29.6 Mbits/sec  | 39.7 Mbits/sec  | 133 ms         
Scaleway        | Paris, FR (10G)           | 1.08 Gbits/sec  | 11.9 Mbits/sec  | 153 ms         
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 205 ms         
Uztelecom       | Tashkent, UZ (10G)        | 738 Mbits/sec   | 469 Mbits/sec   | 221 ms         
Clouvider       | NYC, NY, US (10G)         | 54.0 Mbits/sec  | 96.9 Mbits/sec  | 88.7 ms        
Clouvider       | Dallas, TX, US (10G)      | 60.5 Mbits/sec  | 284 Mbits/sec   | 64.3 ms        
Clouvider       | Los Angeles, CA, US (10G) | 111 Mbits/sec   | 185 Mbits/sec   | 53.6 ms        
Biznet          | Jakarta, ID (10G)         | busy            | 63.4 Mbits/sec  | -- 

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | busy            | 40.4 Mbits/sec  | 133 ms         
Scaleway        | Paris, FR (10G)           | busy            | 500 Mbits/sec   | 141 ms         
NovoServe       | North Holland, NL (40G)   | 898 Mbits/sec   | 608 Mbits/sec   | 164 ms         
Uztelecom       | Tashkent, UZ (10G)        | 853 Mbits/sec   | busy            | 221 ms         
Clouvider       | NYC, NY, US (10G)         | 59.0 Mbits/sec  | 95.1 Mbits/sec  | 66.9 ms        
Clouvider       | Dallas, TX, US (10G)      | 60.5 Mbits/sec  | 186 Mbits/sec   | 63.8 ms        
Clouvider       | Los Angeles, CA, US (10G) | 101 Mbits/sec   | 210 Mbits/sec   | 36.9 ms        
Biznet          | Jakarta, ID (10G)         | busy            | busy            | -- 

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2885                          
Multi Core      | 5201                          
Full Test       | https://browser.geekbench.com/v6/cpu/2490848

YABS completed in 13 min 54 sec
```

### SpeedTest

```
   Speedtest by Ookla

      Server: Intechtel - Managed IT Services - Coeur d'Alene, ID (id: 51640)
         ISP: Crunchbits, LLC
Idle Latency:    10.66 ms   (jitter: 0.05ms, low: 10.64ms, high: 10.74ms)
    Download:  2296.48 Mbps (data used: 2.2 GB)                                                   
                 10.66 ms   (jitter: 0.14ms, low: 10.34ms, high: 11.10ms)
      Upload:  2490.90 Mbps (data used: 3.7 GB)                                                   
                 10.57 ms   (jitter: 0.17ms, low: 10.29ms, high: 11.46ms)
 Packet Loss:     0.0%
  Result URL: https://www.speedtest.net/result/c/4499fe79-9eb8-4f05-a204-5560d418e28b
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 7950X 16-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 4499.992 MHz
 CPU 缓存          : L1: 128.00 KB / L2: 2.00 MB / L3: 64.00 MB
 硬盘空间          : 2.24 GiB / 99.87 GiB
 启动盘路径        : /dev/sda3
 内存              : 182.05 MiB / 3.84 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 23 min
 负载              : 0.06, 0.12, 0.10
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-20-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS400304 REDOUBT NETWORKS
 IPV4 位置         : Liberty Lake / Washington / US
 IPV6 ASN          : AS400304 Crunchbits
 IPV6 位置         : Spokane / Washington
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           6555 Scores
 2 线程测试(多核)得分:          12911 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          74355.93 MB/s
 单线程写测试:          38250.63 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         82.2 MB/s (20.08 IOPS, 1.27s))          106 MB/s (25936 IOPS, 0.99s)
 1GB-1M Block           731 MB/s (698 IOPS, 1.43s)              4.4 GB/s (4167 IOPS, 0.24s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 533.05 MB/s (133.2k) | 2.50 GB/s    (39.1k)
Write      | 534.46 MB/s (133.6k) | 2.52 GB/s    (39.3k)
Total      | 1.06 GB/s   (266.8k) | 5.02 GB/s    (78.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.44 GB/s     (6.7k) | 3.56 GB/s     (3.4k)
Write      | 3.62 GB/s     (7.0k) | 3.80 GB/s     (3.7k)
Total      | 7.07 GB/s    (13.8k) | 7.37 GB/s     (7.1k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA09S34)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA30S12)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：美国
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Seattle, WA 
 Netflix Preferred CDN:                 Seattle, WA  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Seattle, WA 
 Netflix Preferred CDN:                 Seattle, WA  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 0②
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
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测87 ③
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
  qq邮箱：No
------以下为IPV6检测------
欺诈分数(越低越好): 100②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: US 城市: Liberty Lake 服务商: AS400304 REDOUBT NETWORKS
北京电信 219.141.136.12  测试超时
北京联通 202.106.50.1    联通4837[普通线路]           
北京移动 221.179.155.161 测试超时
上海电信 202.96.209.133  电信163 [普通线路]           
上海联通 210.22.97.1     联通4837[普通线路]           
上海移动 211.136.112.200 移动CMI [普通线路]           
广州电信 58.60.188.222   电信163 [普通线路]           
广州联通 210.21.196.6    测试超时
广州移动 120.196.165.24  测试超时
成都电信 61.139.2.69     测试超时
成都联通 119.6.6.6       联通4837[普通线路]           
成都移动 211.137.96.205  测试超时
2023/09/04 11:21:52 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
29.42 ms        AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
0.84 ms         AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
2.10 ms         * 美国 爱达荷州 科达伦
2.14 ms         AS20055 [WHOLESAIL-IPV4] 美国 爱达荷州 科达伦 wholesailnetworks.com
10.01 ms        AS20055 [WHOLESAIL-IPV4] 美国 爱达荷州 科达伦 wholesailnetworks.com
10.26 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 斯波坎 wholesailnetworks.com
15.77 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 斯波坎 wholesailnetworks.com
10.56 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 雅基马 wholesailnetworks.com
9.84 ms         AS6461 [NETBLK-ABOVENET] 美国 华盛顿州 西雅图 zayo.com
33.26 ms        AS6461 美国 华盛顿州 西雅图 zayo.com
32.96 ms        AS6461 美国 加利福尼亚州 圣何塞 zayo.com
29.21 ms        AS6461 美国 加利福尼亚州 圣何塞 zayo.com
198.94 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
224.03 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
331.85 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
428.61 ms       AS134774 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.cn 电信
297.11 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
26.41 ms        AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
3.26 ms         AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
2.12 ms         * 美国 爱达荷州 科达伦
1.96 ms         AS20055 [WHOLESAIL-IPV4] 美国 爱达荷州 科达伦 wholesailnetworks.com
9.88 ms         AS20055 [WHOLESAIL-IPV4] 美国 爱达荷州 科达伦 wholesailnetworks.com
10.36 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 斯波坎 wholesailnetworks.com
17.31 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 斯波坎 wholesailnetworks.com
10.42 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 雅基马 wholesailnetworks.com
9.93 ms         AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 西雅图 wholesailnetworks.com
10.60 ms        AS174 美国 华盛顿州 西雅图 cogentco.com
28.66 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 旧金山 cogentco.com
29.58 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 圣何塞 cogentco.com
41.56 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
42.37 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
41.57 ms        AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
191.40 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
188.88 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
187.62 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
203.23 ms       AS17816 [UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
202.04 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
193.56 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
73.70 ms        AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
0.64 ms         AS400304 美国 华盛顿州 利伯蒂湖 redoubtnet.com
2.30 ms         * 美国 爱达荷州 科达伦
1.96 ms         AS20055 [WHOLESAIL-IPV4] 美国 爱达荷州 科达伦 wholesailnetworks.com
12.80 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 普尔曼 wholesailnetworks.com
12.55 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 肯纳威克 wholesailnetworks.com
12.37 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 肯纳威克 wholesailnetworks.com
12.95 ms        AS20055 [WHOLESAIL-IPV4] 美国 俄勒冈州 尤马蒂拉 wholesailnetworks.com
13.06 ms        AS20055 [WHOLESAIL-IPV4] 美国 俄勒冈州 尤马蒂拉 wholesailnetworks.com
12.83 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 西雅图 wholesailnetworks.com
12.91 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 西雅图 wholesailnetworks.com
12.35 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 西雅图 wholesailnetworks.com
12.23 ms        AS20055 [WHOLESAIL-IPV4] 美国 华盛顿州 西雅图 wholesailnetworks.com
12.38 ms        AS20055 [WHOLESAIL-IPV4] 美国 俄勒冈州 希尔斯伯勒 wholesailnetworks.com
12.41 ms        AS20055 [WHOLESAIL-IPV4] 美国 俄勒冈州 希尔斯伯勒 wholesailnetworks.com
12.04 ms        AS1299 [ARELION-NET] 美国 俄勒冈州 波特兰 arelion.com
26.16 ms        AS1299 [ARELION-NET] 美国 加利福尼亚州 帕洛阿托 arelion.com
27.20 ms        AS1299 [ARELION-NET] 美国 加利福尼亚州 圣何塞 arelion.com
80.26 ms        AS1299 [ARELION-NET] 美国 加利福尼亚州 圣何塞 Telia-CMI-Peer arelion.com
80.79 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 圣何塞 cmi.chinamobile.com 移动
241.53 ms       AS58453 [CMI-INT] 中国 广东省 广州市 cmi.chinamobile.com 移动
240.37 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
240.33 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
242.40 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
246.28 ms       AS9808 [CMNET] 中国 海南省 海口市 chinamobile.com 移动
243.57 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    2265.29 Mbps    2296.69 Mbps    10.69    0.0%
洛杉矶           1162.66 Mbps    2285.11 Mbps    37.07    0.0%
日本东京         322.03 Mbps     29.61 Mbps      117.83   NULL
联通WuXi         494.48 Mbps     1705.45 Mbps    208.40   0.0%
移动Chengdu      102.86 Mbps     63.18 Mbps      327.97   0.0%
------------------------------------------------------------------------
 总共花费      : 5 分 4 秒
 时间          : Mon Sep  4 11:25:55 CST 2023
------------------------------------------------------------------------
```
