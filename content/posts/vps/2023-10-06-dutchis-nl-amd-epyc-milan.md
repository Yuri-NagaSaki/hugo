---
title: 'DutchIS  荷兰 AMD EPYC Milan 7313  测评'
author: 猫猫博客
type: post
date: 2023-10-06T08:08:00+00:00
url: /dutchis-nl-amd-epyc-milan.html
ai_summon_excerpt:
  - 荷兰AMD EPYC Milan 7313测评结果显示，该服务器配备了AMD EPYC 7313处理器，拥有16个核心，性能较好。它在运行lscpu命令时显示出的体系结构和特性与AMD EPYC处理器一致。在Yabs测试中，服务器显示良好的运行状态，具有高速的网络连接和稳定的性能。在fio Disk Speed Tests和iperf3 Network Speed Tests中，该服务器展现出出色的磁盘和网络速度性能。根据Geekbench 6 Benchmark测试，单核性能达到1734分，显示出较高的计算性能。总体来说，这台荷兰AMD EPYC Milan 7313服务器表现出色，适合在VPS和独立服务器等应用场景中使用。
views:
  - 41
categories:
  - vps
  - 性能鸡
  - 欧洲

---
荷兰的商家，主要经营vps和独立服务器两种分类，商家注册严格，需要先花1欧进行身份验证，后台是商家自研面板，颜值还算可以。vps主要是标准版EPYC和高性能版5950X两种。商家还提供免费的10G **SpeedIX**的对等连接(条件必须是自己也是SpeedIX的会员)。

<blockquote class="wp-block-quote">
  <h2 class="wp-block-heading">
    套餐
  </h2>
  
  <cite><strong><em>Provider :&nbsp;DutchIS <br />Type/Plan :&nbsp;Virtual Servers - Standard<br />Processor :&nbsp;AMD EPYC Milan<br />Num of Core : 2 Cores<br />Memory : 4 GB&nbsp;DDR4 RAM<br />Storage : 50 GB NVMe(PCIe 4.0)<br />Bandwidth : Unlimited @ 1 Gbps IN | 1 Gbps OUT<br />Location :&nbsp;Netherlands (Apeldoorn)<br />Price :&nbsp;€ 8,40/月</em></strong></cite>
</blockquote>

## LG {.wp-block-heading}

**Test Information**  
IPv4: 194.107.78.212  
IPv6: 2001:67c:1330::3  
YABS:&nbsp;<a href="https://pastebin.com/DL1pQijY" target="_blank"  rel="nofollow" >https://pastebin.com/DL1pQijY</a>  
Data center's looking glass:&nbsp;<a href="https://lg.serverius.net/" target="_blank"  rel="nofollow" >https://lg.serverius.net/</a>

## 测评 {.wp-block-heading}

### lscpu {.wp-block-heading}

<pre class="wp-block-code"><code>Architecture:            x86_64
  CPU op-mode(s):        32-bit, 64-bit
  Address sizes:         48 bits physical, 48 bits virtual
  Byte Order:            Little Endian
CPU(s):                  2
  On-line CPU(s) list:   0,1
Vendor ID:               AuthenticAMD
  Model name:            AMD EPYC 7313 16-Core Processor
    CPU family:          25
    Model:               1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    Stepping:            1
    BogoMIPS:            5999.99
Virtualization features:
  Virtualization:        AMD-V
  Hypervisor vendor:     KVM
  Virtualization type:   full
Caches (sum of all):
  L1d:                   128 KiB (2 instances)
  L1i:                   128 KiB (2 instances)
  L2:                    1 MiB (2 instances)
  L3:                    32 MiB (2 instances)</code></pre>

### Yabs {.wp-block-heading}

<pre class="wp-block-code"><code>Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 7 minutes
Processor  : AMD EPYC 7313 16-Core Processor
CPU cores  : 2 @ 2999.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 0.0 KiB
Disk       : 48.4 GiB
Distro     : Ubuntu 22.04.3 LTS
Kernel     : 5.15.0-86-generic
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : Serverius Holding B.V.
ASN        : AS50673 Serverius
Host       : Serveriuscustomer
Location   : Amsterdam, North Holland (NH)
Country    : Netherlands

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------   | ---            ----  | ----           ----
Read       | 240.73 MB/s  (60.1k) | 2.70 GB/s    (42.3k)
Write      | 241.36 MB/s  (60.3k) | 2.72 GB/s    (42.5k)
Total      | 482.10 MB/s (120.5k) | 5.43 GB/s    (84.8k)
           |                      |
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------   | ---            ----  | ----           ----
Read       | 4.65 GB/s     (9.0k) | 5.65 GB/s     (5.5k)
Write      | 4.90 GB/s     (9.5k) | 6.02 GB/s     (5.8k)
Total      | 9.55 GB/s    (18.6k) | 11.68 GB/s   (11.4k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
-----           | -----                     | ----            | ----            | ----
Clouvider       | London, UK (10G)          | 1.04 Gbits/sec  | 928 Mbits/sec   | 8.61 ms
Scaleway        | Paris, FR (10G)           | 988 Mbits/sec   | 976 Mbits/sec   | 16.8 ms
NovoServe       | North Holland, NL (40G)   | 1.04 Gbits/sec  | 978 Mbits/sec   | 3.51 ms
Uztelecom       | Tashkent, UZ (10G)        | 927 Mbits/sec   | 916 Mbits/sec   | 101 ms
Clouvider       | NYC, NY, US (10G)         | 911 Mbits/sec   | 937 Mbits/sec   | 77.2 ms
Clouvider       | Dallas, TX, US (10G)      | 672 Mbits/sec   | 924 Mbits/sec   | 114 ms
Clouvider       | Los Angeles, CA, US (10G) | 691 Mbits/sec   | 880 Mbits/sec   | 153 ms

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1734                          
Multi Core      | 3312</code></pre>

### Bench {.wp-block-heading}

<pre class="wp-block-code"><code>-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD EPYC 7313 16-Core Processor
 CPU Cores          : 2 @ 2999.998 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 48.4 GB (2.3 GB Used)
 Total Mem          : 3.8 GB (182.8 MB Used)
 System uptime      : 0 days, 0 hour 2 min
 Load average       : 0.18, 0.05, 0.01
 OS                 : Ubuntu 22.04.3 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.15.0-86-generic
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Offline
 Organization       : AS50673 Serverius
 Location           : Dronten / NL
 Region             : Flevoland
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.1 GB/s
 I/O Speed(2nd run) : 1.2 GB/s
 I/O Speed(3rd run) : 1.2 GB/s
 I/O Speed(average) : 1194.7 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency
 Speedtest.net    1045.41 Mbps      993.33 Mbps         1.08 ms
 Los Angeles, US  581.92 Mbps       989.16 Mbps         140.08 ms
 Dallas, US       726.11 Mbps       1000.40 Mbps        112.13 ms
 Montreal, CA     567.23 Mbps       930.69 Mbps         83.56 ms
 Paris, FR        1043.68 Mbps      1011.32 Mbps        15.46 ms
 Amsterdam, NL    1044.70 Mbps      995.13 Mbps         4.89 ms
 Shanghai, CN     380.96 Mbps       837.67 Mbps         189.20 ms
 Hongkong, CN     300.74 Mbps       863.89 Mbps         268.61 ms
 Singapore, SG    495.27 Mbps       843.49 Mbps         161.97 ms
 Tokyo, JP        180.85 Mbps       856.79 Mbps         231.45 ms
----------------------------------------------------------------------</code></pre>

### <a href="https://www.passmark.com/products/pt_linux/download.php" target="_blank" rel="noreferrer noopener" rel="nofollow" >PerformanceTest Linux</a>&nbsp;测试 {.wp-block-heading}

<pre class="wp-block-code"><code>AMD EPYC 7313 16-Core Processor (x86_64)
2 cores @ 0 MHz  |  3.8 GiB RAM
Number of Processes: 2  |  Test Iterations: 2  |  Test Duration: Very Long
-
CPU Mark:                          5355
  Integer Math                     12245 Million Operations/s
  Floating Point Math              9898 Million Operations/s
  Prime Numbers                    42.7 Million Primes/s
  Sorting                          7234 Thousand Strings/s
  Encryption                       2612 MB/s
  Compression                      51624 KB/s
  CPU Single Threaded              2788 Million Operations/s
  Physics                          682 Frames/s
  Extended Instructions (SSE)      4788 Million Matrices/s

Memory Mark:                       2105
  Database Operations              2086 Thousand Operations/s
  Memory Read Cached               28068 MB/s
  Memory Read Uncached             18787 MB/s
  Memory Write                     19608 MB/s
  Available RAM                    2990 Megabytes
  Memory Latency                   59 Nanoseconds
  Memory Threaded                  36518 MB/s</code></pre>

### byte-unixbench 性能测试 {.wp-block-heading}

<pre class="wp-block-code"><code>------------------------------------------------------------------------

2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       50783651.2 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     8978.2 MWIPS (9.9 s, 7 samples)
Execl Throughput                               5209.7 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1483243.5 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          391146.6 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       4954121.8 KBps  (30.0 s, 2 samples)
Pipe Throughput                             2122401.2 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                  67333.2 lps   (10.0 s, 7 samples)
Process Creation                              13400.3 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  16400.6 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   3019.1 lpm   (60.0 s, 2 samples)
System Call Overhead                        1904415.4 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   50783651.2   4351.6
Double-Precision Whetstone                       55.0       8978.2   1632.4
Execl Throughput                                 43.0       5209.7   1211.6
File Copy 1024 bufsize 2000 maxblocks          3960.0    1483243.5   3745.6
File Copy 256 bufsize 500 maxblocks            1655.0     391146.6   2363.4
File Copy 4096 bufsize 8000 maxblocks          5800.0    4954121.8   8541.6
Pipe Throughput                               12440.0    2122401.2   1706.1
Pipe-based Context Switching                   4000.0      67333.2    168.3
Process Creation                                126.0      13400.3   1063.5
Shell Scripts (1 concurrent)                     42.4      16400.6   3868.1
Shell Scripts (8 concurrent)                      6.0       3019.1   5031.9
System Call Overhead                          15000.0    1904415.4   1269.6
                                                                   ========
System Benchmarks Index Score                                        2030.5

------------------------------------------------------------------------

2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables      100943856.8 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    17952.5 MWIPS (9.9 s, 7 samples)
Execl Throughput                               8106.1 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       2952334.0 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          780666.9 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       9106896.8 KBps  (30.0 s, 2 samples)
Pipe Throughput                             4247770.4 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 561525.8 lps   (10.0 s, 7 samples)
Process Creation                              21727.8 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  21472.2 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   3069.2 lpm   (60.0 s, 2 samples)
System Call Overhead                        3803274.9 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  100943856.8   8649.9
Double-Precision Whetstone                       55.0      17952.5   3264.1
Execl Throughput                                 43.0       8106.1   1885.2
File Copy 1024 bufsize 2000 maxblocks          3960.0    2952334.0   7455.4
File Copy 256 bufsize 500 maxblocks            1655.0     780666.9   4717.0
File Copy 4096 bufsize 8000 maxblocks          5800.0    9106896.8  15701.5
Pipe Throughput                               12440.0    4247770.4   3414.6
Pipe-based Context Switching                   4000.0     561525.8   1403.8
Process Creation                                126.0      21727.8   1724.4
Shell Scripts (1 concurrent)                     42.4      21472.2   5064.2
Shell Scripts (8 concurrent)                      6.0       3069.2   5115.3
System Call Overhead                          15000.0    3803274.9   2535.5
                                                                   ========
System Benchmarks Index Score                                        3983.3</code></pre>

### SpeedTest {.wp-block-heading}

<pre class="wp-block-code"><code>   Speedtest by Ookla

      Server: Serverius Connectivity - Amsterdam (id: 20005)
         ISP: Serverius Holding B.V.
Idle Latency:     1.05 ms   (jitter: 0.02ms, low: 1.04ms, high: 1.08ms)
    Download:   979.39 Mbps (data used: 539.0 MB)
                 67.49 ms   (jitter: 15.34ms, low: 1.50ms, high: 157.54ms)
      Upload:  1069.02 Mbps (data used: 485.9 MB)
                  1.12 ms   (jitter: 0.10ms, low: 1.04ms, high: 2.13ms)
 Packet Loss:     0.0%</code></pre><figure class="wp-block-image size-large">

<img decoding="async" loading="lazy" width="1024" height="427" src="https://cdn.lirica.cn/wordpress/2023/10/image-4-1024x427.png" alt="" class="wp-image-2298" srcset="https://catcat.blog/wp-content/uploads/2023/10/image-4-1024x427.png 1024w, https://catcat.blog/wp-content/uploads/2023/10/image-4-300x125.png 300w, https://catcat.blog/wp-content/uploads/2023/10/image-4-768x320.png 768w, https://catcat.blog/wp-content/uploads/2023/10/image-4.png 1163w" sizes="(max-width: 1024px) 100vw, 1024px" /> </figure> 

### Network-Speed.xyz {.wp-block-heading}

<pre class="wp-block-code"><code>Basic System Info
---------------------------------------------------------------------------
 CPU Model          : AMD EPYC 7313 16-Core Processor
 CPU Cores          : 2 @ 2999.998 MHz
 CPU Cache          : 512 KB
 AES-NI             : ✔ Enabled
 VM-x/AMD-V         : ✔ Enabled
 Total Disk         : 48.4 GB (2.3 GB Used)
 Total RAM          : 3.8 GB (186.2 MB Used)
 System uptime      : 0 days, 0 hour 11 min
 Load average       : 0.17, 0.15, 0.07
 OS                 : Ubuntu 22.04.3 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.15.0-86-generic
 Virtualization     : KVM
---------------------------------------------------------------------------
 Basic Network Info
---------------------------------------------------------------------------
 IPv6 Access        : ❌ Offline
 IPv4 Access        : ✔ Online
 ISP                : Serverius Holding B.V.
 ASN                : AS50673 Serverius
 Host               : Serveriuscustomer
 Location           : Amsterdam, North Holland-NH, Netherlands
 Location (IPv4)    : Dronten, Flevoland, NL
---------------------------------------------------------------------------
 Speedtest.net (Region: GLOBAL)
---------------------------------------------------------------------------
 Location         Latency     Loss    DL Speed       UP Speed       Server

 ISP: Serverius Holding B.V.

 Nearest          1.02 ms     0.0%    982.31 Mbps    1041.58 Mbps   Serverius Connectivity - Amsterdam

 Kochi, IN        154.99 ms   0.0%    997.74 Mbps    535.27 Mbps    Asianet Broadband - Cochin
 Bangalore, IN    136.90 ms   0.0%    997.95 Mbps    535.87 Mbps    Bharti Airtel Ltd - Bangalore
 Chennai, IN      181.43 ms   N/A     1000.32 Mbps   498.52 Mbps    Jio - Chennai
 Mumbai, IN       121.26 ms   0.0%    997.39 Mbps    661.34 Mbps    i3D.net - Mumbai
 Delhi, IN        139.96 ms   0.0%    986.98 Mbps    578.40 Mbps    Tata Teleservices Ltd - New Delhi

 Seattle, US      158.99 ms   0.0%    942.85 Mbps    550.76 Mbps    Ziply Fiber - Seattle, WA
 Los Angeles, US  156.99 ms   0.0%    970.41 Mbps    520.13 Mbps    ReliableSite Hosting - Los Angeles, CA
 Dallas, US       132.32 ms   0.0%    799.77 Mbps    647.87 Mbps    Hivelocity - Dallas, TX
 Miami, US        FAILED
 New York, US     83.96 ms    0.0%    968.67 Mbps    781.07 Mbps    GSL Networks - New York, NY
 Toronto, CA      90.25 ms    0.0%    987.06 Mbps    867.22 Mbps    Rogers - Toronto, ON

 London, UK       8.46 ms     0.0%    978.56 Mbps    1044.53 Mbps   VeloxServ Communications - London
 Amsterdam, NL    3.69 ms     0.0%    971.44 Mbps    1045.16 Mbps   31173 Services AB - Amsterdam
 Paris, FR        16.88 ms    N/A     980.34 Mbps    1050.01 Mbps   Axione - Paris
 Frankfurt, DE    9.20 ms     0.0%    959.81 Mbps    1048.44 Mbps   23M GmbH - Frankfurt am Main
 Warsaw, PL       24.22 ms    0.0%    976.00 Mbps    1038.36 Mbps   UPC Polska - Warszawa
 Bucharest, RO    37.78 ms    0.0%    973.69 Mbps    978.90 Mbps    Vodafone Romania Fixed – Bucharest - Bucharest

 Jeddah, SA       74.20 ms    0.0%    968.34 Mbps    813.85 Mbps    Saudi Telecom Company
 Dubai, AE        139.42 ms   0.0%    973.72 Mbps    543.82 Mbps    du - Dubai
 Fujairah, AE     115.93 ms   0.0%    975.27 Mbps    643.12 Mbps    ETISALAT-UAE - Fujairah

 Tokyo, JP        256.85 ms   N/A     709.84 Mbps    87.69 Mbps     fdcservers.net - Tokyo
 Shanghai, CU-CN  204.54 ms   0.0%    959.51 Mbps    388.92 Mbps    China Unicom 5G - Shanghai
 Nanjing, CT-CN   252.60 ms   1.3%    770.71 Mbps    91.92 Mbps     China Telecom JiangSu 5G - Nanjing
 Hong Kong, CN    FAILED
 Singapore, SG    153.68 ms   0.0%    986.87 Mbps    508.88 Mbps    i3D.net - Singapore
 Jakarta, ID      177.65 ms   0.0%    914.26 Mbps    362.10 Mbps    PT. Telekomunikasi Indonesia - Jakarta
---------------------------------------------------------------------------
 Avg DL Speed       : 952.40 Mbps
 Avg UL Speed       : 714.48 Mbps

 Total DL Data      : 34.73 GB
 Total UL Data      : 20.27 GB
 Total Data         : 54.00 GB
</code></pre>

### 国内延迟测速 {.wp-block-heading}<figure class="wp-block-image size-large">

<img decoding="async" loading="lazy" width="1024" height="457" src="https://cdn.lirica.cn/wordpress/2023/10/image-5-1024x457.png" alt="" class="wp-image-2299" srcset="https://catcat.blog/wp-content/uploads/2023/10/image-5-1024x457.png 1024w, https://catcat.blog/wp-content/uploads/2023/10/image-5-300x134.png 300w, https://catcat.blog/wp-content/uploads/2023/10/image-5-768x343.png 768w, https://catcat.blog/wp-content/uploads/2023/10/image-5-1536x686.png 1536w, https://catcat.blog/wp-content/uploads/2023/10/image-5.png 2045w" sizes="(max-width: 1024px) 100vw, 1024px" /> </figure> 

### 国际延迟测速 {.wp-block-heading}<figure class="wp-block-image size-large">

<img decoding="async" loading="lazy" width="1024" height="534" src="https://cdn.lirica.cn/wordpress/2023/10/image-6-1024x534.png" alt="" class="wp-image-2300" srcset="https://catcat.blog/wp-content/uploads/2023/10/image-6-1024x534.png 1024w, https://catcat.blog/wp-content/uploads/2023/10/image-6-300x156.png 300w, https://catcat.blog/wp-content/uploads/2023/10/image-6-768x400.png 768w, https://catcat.blog/wp-content/uploads/2023/10/image-6-1536x801.png 1536w, https://catcat.blog/wp-content/uploads/2023/10/image-6.png 1857w" sizes="(max-width: 1024px) 100vw, 1024px" /> </figure>