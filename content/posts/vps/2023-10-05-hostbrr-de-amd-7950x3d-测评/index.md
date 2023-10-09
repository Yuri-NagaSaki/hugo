---
title: "Hostbrr DE AMD 7950X3D 测评"
date: "2023-10-05"
categories: 
  - "vps"
  - "eu"
---

商家最近推出了下单3倍CPU的7950X3D活动，对于这个u来说，这个促销无疑是超售了。卖家是Hetzner的经销商，没有自己机房，以低价和促销在low上有名。个人不推荐为了性能买这家，谨慎上车。

> ## 套餐
> 
> **_Provider :_ Hostbrr  
> _Type/Plan :_ **7950XD-6GBrr**  
> _Processor :_ AMD Ryzen 9 7950X3D (4.5 GHz++)  
> _Num of Core : 9 Cores_  
> _Memory : 6 GB_ DDR5 RAM  
> _Storage : 100 GB NVMe_(PCIe 4.0)  
> _Bandwidth : 15000 GB @ 1 Gbps IN | 1 Gbps OUT_  
> _Location :_ Falkenstein, Germany  
> _Price :_ $10.03 /month**

## 测评

速度没啥好测的，Hetzner的，测过无数次。

### Lscpu

```
root@catcat:~# lscpu
Architecture:            x86_64
  CPU op-mode(s):        32-bit, 64-bit
  Address sizes:         40 bits physical, 48 bits virtual
  Byte Order:            Little Endian
CPU(s):                  9
  On-line CPU(s) list:   0-8
Vendor ID:               AuthenticAMD
  BIOS Vendor ID:        QEMU
  Model name:            AMD Ryzen 9 7950X3D 16-Core Processor
    BIOS Model name:     pc-i440fx-5.2  CPU @ 2.0GHz
    BIOS CPU family:     1
    CPU family:          25
    Model:               97
    Thread(s) per core:  1
    Core(s) per socket:  1
    Socket(s):           9
    Stepping:            2
    BogoMIPS:            8384.28

Virtualization features: 
  Virtualization:        AMD-V
  Hypervisor vendor:     KVM
  Virtualization type:   full
Caches (sum of all):     
  L1d:                   288 KiB (9 instances)
  L1i:                   288 KiB (9 instances)
  L2:                    9 MiB (9 instances)
  L3:                    576 MiB (9 instances)
NUMA:                    
  NUMA node(s):          1
  NUMA node0 CPU(s):     0-8
Vulnerabilities:         
  Gather data sampling:  Not affected
  Itlb multihit:         Not affected
  L1tf:                  Not affected
  Mds:                   Not affected
  Meltdown:              Not affected
  Mmio stale data:       Not affected
  Retbleed:              Not affected
  Spec rstack overflow:  Mitigation; safe RET, no microcode
  Spec store bypass:     Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:            Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:            Mitigation; Retpolines, IBPB conditional, IBRS_FW, STIBP disabled, RSB filling,                          PBRSB-eIBRS Not affected
  Srbds:                 Not affected
  Tsx async abort:       Not affected
```

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 0 minutes
Processor  : AMD Ryzen 9 7950X3D 16-Core Processor
CPU cores  : 9 @ 4192.140 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 5.8 GiB
Swap       : 1024.0 MiB
Disk       : 99.9 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-12-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Hetzner Online GmbH
ASN        : AS24940 Hetzner Online GmbH
Location   : Falkenstein, Saxony (SN)
Country    : Germany

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 454.51 MB/s (113.6k) | 1.04 GB/s    (16.3k)
Write      | 455.71 MB/s (113.9k) | 1.05 GB/s    (16.4k)
Total      | 910.22 MB/s (227.5k) | 2.09 GB/s    (32.7k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.03 GB/s     (2.0k) | 949.72 MB/s    (927)
Write      | 1.08 GB/s     (2.1k) | 1.01 GB/s      (989)
Total      | 2.12 GB/s     (4.1k) | 1.96 GB/s     (1.9k)

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2510                          
Multi Core      | 10964                         
Full Test       | https://browser.geekbench.com/v6/cpu/2912840

YABS completed in 5 min 8 sec
```

### Bench

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU Cores          : 9 @ 4192.140 MHz
 CPU Cache          : 1024 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 99.9 GB (3.5 GB Used)
 Total Mem          : 5.8 GB (395.9 MB Used)
 Total Swap         : 1024.0 MB (0 Used)
 System uptime      : 0 days, 0 hour 8 min
 Load average       : 0.06, 0.42, 0.26
 OS                 : Debian GNU/Linux 12
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.1.0-12-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Region             : No ISP detected
----------------------------------------------------------------------
 I/O Speed(1st run) : 991 MB/s
 I/O Speed(2nd run) : 1.1 GB/s
 I/O Speed(3rd run) : 1.1 GB/s
 I/O Speed(average) : 1081.3 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    922.11 Mbps       923.01 Mbps         7.86 ms     
 Los Angeles, US  571.16 Mbps       745.52 Mbps         156.98 ms   
 Dallas, US       654.44 Mbps       877.95 Mbps         130.39 ms   
 Montreal, CA     13.50 Mbps        362.60 Mbps         112.06 ms   
 Paris, FR        921.02 Mbps       935.05 Mbps         16.01 ms    
 Amsterdam, NL    928.89 Mbps       932.88 Mbps         11.19 ms    
 Shanghai, CN     474.00 Mbps       567.54 Mbps         181.38 ms   
 Nanjing, CN      82.83 Mbps        682.83 Mbps         178.16 ms   
 Hongkong, CN     434.18 Mbps       552.58 Mbps         205.57 ms   
 Singapore, SG    349.51 Mbps       609.77 Mbps         158.98 ms   
 Tokyo, JP        369.05 Mbps       745.45 Mbps         225.20 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 15 sec
 Timestamp          : 2023-10-05 09:01:31 CST
----------------------------------------------------------------------
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU 核心数        : 9
 CPU 频率          : 4192.140 MHz
 CPU 缓存          : L1: 288.00 KB / L2: 9.00 MB / L3: 576.00 MB
 硬盘空间          : 3.50 GiB / 99.82 GiB
 启动盘路径        : /dev/vda3
 内存              : 264.96 MiB / 5.75 GiB
 Swap              : 0 KiB / 1024.00 MiB
 系统在线时间      : 0 days, 0 hour 15 min
 负载              : 0.03, 0.16, 0.18
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-12-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS24940 Hetzner Online GmbH
 IPV4 位置         : Gunzenhausen / DE-BY
 IPV6 ASN          : AS24940 Hetzner Online
 IPV6 位置         : Nuremberg / Bavaria
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           5641 Scores
 9 线程测试(多核)得分:          49091 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          68960.70 MB/s
 单线程写测试:          38874.39 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         53.3 MB/s (13.02 IOPS, 1.97s))          44.8 MB/s (10926 IOPS, 2.34s)
 1GB-1M Block           943 MB/s (899 IOPS, 1.11s)              2.4 GB/s (2268 IOPS, 0.44s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 492.21 MB/s (123.0k) | 1.10 GB/s    (17.1k)
Write      | 493.51 MB/s (123.3k) | 1.10 GB/s    (17.2k)
Total      | 985.73 MB/s (246.4k) | 2.20 GB/s    (34.4k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.06 GB/s     (2.0k) | 1.03 GB/s     (1.0k)
Write      | 1.12 GB/s     (2.1k) | 1.10 GB/s     (1.0k)
Total      | 2.19 GB/s     (4.2k) | 2.14 GB/s     (2.0k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA16S31)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA16S31)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：德国
[IPv6]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：德国
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：德国区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：德国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: DE)
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       No 
 Amazon Prime Video:                    Yes (Region: DE)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   DE
 Viu.com:                               No
 YouTube CDN:                           Frankfurt 
 Netflix Preferred CDN:                 Frankfurt  
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: DE)
 Netflix:                               Originals Only
 YouTube Premium:                       Failed
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Frankfurt 
 Netflix Preferred CDN:                 Frankfurt  
 Spotify Registration:                  No
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【DE】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 11②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):Data Center/Web Hosting/Transit⑤  hosting⑧  hosting⑨  
  公司类型(company_type):hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes② ⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No② ⑥ ⑦ ⑧ ⑨ ⑩ 
  VPN(vpn):  No② ⑦ ⑧ 
  TOR(tor):  No② ⑦ ⑧ ⑨ 
  TOR出口(tor_exit):  No⑧ 
  搜索引擎机器人(search_engine_robot):  No② 
  匿名代理(anonymous):  No⑦ ⑧ ⑨ 
  攻击方(attacker):  No⑧ ⑨ 
  滥用者(abuser):  No⑧ ⑨ 
  威胁(threat):  No⑧ ⑨ 
  iCloud中继(icloud_relay):  No⑧ ⑨ 
  未分配IP(bogon):  No⑧ ⑨ 
Google搜索可行性：YES
------以下为IPV6检测------
欺诈分数(越低越好): 11②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.12 ms         AS24940 德国 巴伐利亚州 贡岑豪森 hetzner.com
0.37 ms         * RFC6598
0.52 ms         AS24940 [DE-HETZNER] 德国 莱茵兰-普法尔茨州 法尔肯斯泰因 hetzner.com
2.90 ms         AS24940 [DE-HETZNER] 德国 巴伐利亚州 纽伦堡 hetzner.com
3.02 ms         AS1299 [ARELION-NET] 德国 巴伐利亚州 纽伦堡 arelion.com
6.44 ms         AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
6.08 ms         AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
7.59 ms         AS4134 [CHINANET-BB] 德国 黑森州 美因河畔法兰克福 CT-POP chinatelecom.com.cn 电信
302.64 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
* ms    AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
* ms    AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
202.69 ms       AS134774 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.cn 电信
201.92 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.07 ms         AS24940 德国 巴伐利亚州 贡岑豪森 hetzner.com
0.42 ms         * RFC6598
0.44 ms         AS24940 [DE-HETZNER] 德国 莱茵兰-普法尔茨州 法尔肯斯泰因 hetzner.com
2.87 ms         AS24940 [DE-HETZNER] 德国 拜仁 维尔茨堡 hetzner.com
2.90 ms         AS1299 [TELIANET] 德国 巴伐利亚州 纽伦堡 arelion.com
6.18 ms         AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
5.94 ms         AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
37.16 ms        AS4837 [CU169-BACKBONE] 德国 黑森州 美因河畔法兰克福 chinaunicom.cn 联通
174.09 ms       AS4837 [CU169-BACKBONE] 中国 香港 chinaunicom.cn 联通
219.44 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
172.98 ms       AS17816 [UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
215.74 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
195.70 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.12 ms         AS24940 德国 巴伐利亚州 贡岑豪森 hetzner.com
1.07 ms         * RFC6598
0.31 ms         AS24940 [DE-HETZNER] 德国 莱茵兰-普法尔茨州 法尔肯斯泰因 hetzner.com
4.92 ms         AS24940 [DE-HETZNER] 德国 黑森州 美因河畔法兰克福 hetzner.com
5.87 ms         AS58453 [DE-CIX] 德国 黑森州 美因河畔法兰克福 DE-CIX Frankfurt - China Mobile International - 100Gbps cmi.chinamobile.com
6.37 ms         AS58453 [CMI-INT] 德国 黑森州 美茵河畔法兰克福 cmi.chinamobile.com 移动
207.23 ms       AS58453 [CMI-INT] 德国 黑森州 美因河畔法兰克福 cmi.chinamobile.com 移动
208.95 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
209.06 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
411.95 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
210.89 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
213.68 ms       AS9808 [CMNET] 中国 海南省 海口市 chinamobile.com 移动
212.24 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    925.12 Mbps     924.90 Mbps     0.67     0.0%
法兰克福         928.73 Mbps     927.39 Mbps     5.35     0.0%
新加坡           379.20 Mbps     599.22 Mbps     165.33   0.0%
联通Fuzhou       536.90 Mbps     499.36 Mbps     245.16   0.0%
联通WuXi         489.15 Mbps     712.16 Mbps     185.27   0.0%
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD Ryzen 9 7950X3D 16-Core Processor (x86_64)
9 cores @ 0 MHz  |  5.8 GiB RAM
Number of Processes: 9  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          25770
  Integer Math                     67101 Million Operations/s
  Floating Point Math              53419 Million Operations/s
  Prime Numbers                    191 Million Primes/s
  Sorting                          37869 Thousand Strings/s
  Encryption                       14806 MB/s
  Compression                      259702 KB/s
  CPU Single Threaded              3650 Million Operations/s
  Physics                          2904 Frames/s
  Extended Instructions (SSE)      21980 Million Matrices/s

Memory Mark:                       2415
  Database Operations              6789 Thousand Operations/s
  Memory Read Cached               34035 MB/s
  Memory Read Uncached             27895 MB/s
  Memory Write                     15008 MB/s
  Available RAM                    5384 Megabytes
  Memory Latency                   67 Nanoseconds
  Memory Threaded                  36654 MB/s
--------------------------------------------------------------------------
```

### byte-unixbench 性能测试

```
------------------------------------------------------------------------
Benchmark Run: Thu Oct 05 2023 09:13:19 - 09:41:12
9 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       71137060.2 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    11511.4 MWIPS (9.8 s, 7 samples)
Execl Throughput                               5628.0 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1598823.9 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          387389.1 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       4236438.2 KBps  (30.0 s, 2 samples)
Pipe Throughput                             2594867.7 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 259308.0 lps   (10.0 s, 7 samples)
Process Creation                              11628.3 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  15425.7 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   6356.8 lpm   (60.0 s, 2 samples)
System Call Overhead                        2258717.8 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   71137060.2   6095.7
Double-Precision Whetstone                       55.0      11511.4   2093.0
Execl Throughput                                 43.0       5628.0   1308.8
File Copy 1024 bufsize 2000 maxblocks          3960.0    1598823.9   4037.4
File Copy 256 bufsize 500 maxblocks            1655.0     387389.1   2340.7
File Copy 4096 bufsize 8000 maxblocks          5800.0    4236438.2   7304.2
Pipe Throughput                               12440.0    2594867.7   2085.9
Pipe-based Context Switching                   4000.0     259308.0    648.3
Process Creation                                126.0      11628.3    922.9
Shell Scripts (1 concurrent)                     42.4      15425.7   3638.1
Shell Scripts (8 concurrent)                      6.0       6356.8  10594.7
System Call Overhead                          15000.0    2258717.8   1505.8
                                                                   ========
System Benchmarks Index Score                                        2571.2

------------------------------------------------------------------------
Benchmark Run: Thu Oct 05 2023 09:41:12 - 10:09:10
9 CPUs in system; running 9 parallel copies of tests

Dhrystone 2 using register variables      571646844.7 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    99427.5 MWIPS (9.6 s, 7 samples)
Execl Throughput                              27302.2 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1346828.2 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          341589.8 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       4269404.9 KBps  (30.0 s, 2 samples)
Pipe Throughput                            20441108.6 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                1918332.9 lps   (10.0 s, 7 samples)
Process Creation                              54443.7 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  71073.8 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   9727.6 lpm   (60.0 s, 2 samples)
System Call Overhead                        9243136.6 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0  571646844.7  48984.3
Double-Precision Whetstone                       55.0      99427.5  18077.7
Execl Throughput                                 43.0      27302.2   6349.4
File Copy 1024 bufsize 2000 maxblocks          3960.0    1346828.2   3401.1
File Copy 256 bufsize 500 maxblocks            1655.0     341589.8   2064.0
File Copy 4096 bufsize 8000 maxblocks          5800.0    4269404.9   7361.0
Pipe Throughput                               12440.0   20441108.6  16431.8
Pipe-based Context Switching                   4000.0    1918332.9   4795.8
Process Creation                                126.0      54443.7   4320.9
Shell Scripts (1 concurrent)                     42.4      71073.8  16762.7
Shell Scripts (8 concurrent)                      6.0       9727.6  16212.7
System Call Overhead                          15000.0    9243136.6   6162.1
                                                                   ========
System Benchmarks Index Score                                        8608.7
```
