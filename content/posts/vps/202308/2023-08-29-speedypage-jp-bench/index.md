---
title: "SpeedyPage 日本东京测试"
date: "2023-08-29"
categories: 
  - "vps"
  - "jp"
---

## 套餐

> **Tokyo** Location  
> **2** CPU Cores  
> **4GB** DDR4 Memory  
> **60GB** NVMe Disk Space  
> **2TB** Bandwidth  
> **1Gbps** Network Uplink

## 测试

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 3 minutes
Processor  : AMD Ryzen 9 3900X 12-Core Processor
CPU cores  : 2 @ 3792.872 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 0.0 KiB
Disk       : 59.9 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-9-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Mario
ASN        : AS212294 Mario Gomez Canadas
Host       : Mario
Location   : Pyongyang, Pyongyang (01)
Country    : North Korea

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 277.21 MB/s  (69.3k) | 996.97 MB/s  (15.5k)
Write      | 277.95 MB/s  (69.4k) | 1.00 GB/s    (15.6k)
Total      | 555.16 MB/s (138.7k) | 1.99 GB/s    (31.2k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.12 GB/s     (2.2k) | 1.10 GB/s     (1.0k)
Write      | 1.18 GB/s     (2.3k) | 1.18 GB/s     (1.1k)
Total      | 2.31 GB/s     (4.5k) | 2.28 GB/s     (2.2k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | busy            | busy            | 235 ms         
Scaleway        | Paris, FR (10G)           | busy            | busy            | 257 ms         
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 238 ms         
Uztelecom       | Tashkent, UZ (10G)        | busy            | 678 Mbits/sec   | 246 ms         
Clouvider       | NYC, NY, US (10G)         | 22.3 Mbits/sec  | 29.8 Mbits/sec  | 160 ms         
Clouvider       | Dallas, TX, US (10G)      | busy            | busy            | 189 ms         
Clouvider       | Los Angeles, CA, US (10G) | 35.8 Mbits/sec  | 46.2 Mbits/sec  | 160 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 15.8 Mbits/sec  | 20.5 Mbits/sec  | 235 ms         
Scaleway        | Paris, FR (10G)           | 690 Mbits/sec   | 566 Mbits/sec   | 243 ms         
NovoServe       | North Holland, NL (40G)   | 651 Mbits/sec   | 644 Mbits/sec   | 238 ms         
Uztelecom       | Tashkent, UZ (10G)        | 552 Mbits/sec   | 561 Mbits/sec   | 246 ms         
Clouvider       | NYC, NY, US (10G)         | 25.0 Mbits/sec  | 30.7 Mbits/sec  | 160 ms         
Clouvider       | Dallas, TX, US (10G)      | 20.3 Mbits/sec  | 29.5 Mbits/sec  | 188 ms         
Clouvider       | Los Angeles, CA, US (10G) | 24.7 Mbits/sec  | 30.6 Mbits/sec  | 160 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1537                          
Multi Core      | 2689                          
Full Test       | https://browser.geekbench.com/v6/cpu/2423169

YABS completed in 14 min 34 sec
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 3900X 12-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 3792.872 MHz
 CPU 缓存          : L1: 64.00 KB / L2: 1.00 MB / L3: 128.00 MB
 硬盘空间          : 2.22 GiB / 59.82 GiB
 启动盘路径        : /dev/vda3
 内存              : 281.36 MiB / 3.79 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 21 min
 负载              : 0.03, 0.34, 0.27
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS142594 SpeedyPage Ltd
 IPV4 位置         : Motoyoyogichō / Tokyo / JP
 IPV6 ASN          : AS142594 Mario
 IPV6 位置         : Tokyo / Tokyo
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           2001 Scores
 2 线程测试(多核)得分:          3943 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          53839.26 MB/s
 单线程写测试:          23586.41 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         71.1 MB/s (17.36 IOPS, 1.47s))          91.4 MB/s (22304 IOPS, 1.15s)
 1GB-1M Block           1.1 GB/s (1030 IOPS, 0.97s)             3.5 GB/s (3318 IOPS, 0.30s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 274.56 MB/s  (68.6k) | 1.19 GB/s    (18.7k)
Write      | 275.29 MB/s  (68.8k) | 1.20 GB/s    (18.8k)
Total      | 549.85 MB/s (137.4k) | 2.40 GB/s    (37.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.12 GB/s     (2.2k) | 1.13 GB/s     (1.1k)
Write      | 1.18 GB/s     (2.3k) | 1.20 GB/s     (1.1k)
Total      | 2.31 GB/s     (4.5k) | 2.33 GB/s     (2.2k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 日本 东京(NRT20S05)
Youtube识别地域: 日本(JP)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: TSA(TSA03S10)
Youtube识别地域: 澳大利亚(AU)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：日本
[IPv6]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：日本
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：日本区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：日本区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: JP)
 Netflix:                               Yes (Region: JP)
 YouTube Premium:                       Yes (Region: JP)
 Amazon Prime Video:                    Yes (Region: JP)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   JP
 Viu.com:                               No
 YouTube CDN:                           Tokyo 
 Netflix Preferred CDN:                 Tokyo  
 Spotify Registration:                  Yes (Region: JP)
 Steam Currency:                        JPY
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: JP)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: AU)
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Taipei 
 Netflix Preferred CDN:                 Hong Kong  
 Spotify Registration:                  Yes (Region: JP)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【JP】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 50②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Commercial⑤  hosting⑧  business⑨  
  公司类型(company_type):hosting①  hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ② ⑥ ⑦ ⑧ ⑨ 
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
------以下为IPV6检测------
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/08/29 11:57:49 北京电信 219.141.136.12  测试超时
2023/08/29 11:57:49 北京联通 202.106.50.1    联通4837[普通线路]           
2023/08/29 11:57:49 北京移动 221.179.155.161 测试超时
2023/08/29 11:57:49 上海电信 202.96.209.133  电信163 [普通线路]           
2023/08/29 11:57:49 上海联通 210.22.97.1     联通4837[普通线路]           
2023/08/29 11:57:49 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/08/29 11:57:49 广州电信 58.60.188.222   电信163 [普通线路]           
2023/08/29 11:57:49 广州联通 210.21.196.6    联通4837[普通线路]           
2023/08/29 11:57:49 广州移动 120.196.165.24  测试超时
2023/08/29 11:57:49 成都电信 61.139.2.69     电信163 [普通线路]           
2023/08/29 11:57:49 成都联通 119.6.6.6       联通4837[普通线路]           
2023/08/29 11:57:49 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.34 ms         AS136557 [HOST-AU] 日本 东京都 东京 hostuniversal.com.au
0.37 ms         AS136557 [HOST-AU] 日本 东京都 东京 hostuniversal.com.au
0.34 ms         AS136557 [Ransom_IT_Infrastructure] 日本 东京都 东京 hostuniversal.com.au
0.32 ms         * [CDN77-Int] 日本 东京都 东京
0.40 ms         AS2914 [NTTGIN] 日本 东京都 东京 ntt.net
1.31 ms         AS2914 [NTT-BACKBONE] 日本 东京都 东京 ntt.net
92.79 ms        AS2914 [NTT-BACKBONE] 日本 东京都 东京 ntt.net
92.70 ms        AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
94.57 ms        AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
103.79 ms       AS4134 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.com.cn 电信
97.11 ms        AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.34 ms         AS136557 [HOST-AU] 日本 东京都 东京 hostuniversal.com.au
0.31 ms         AS136557 [HOST-AU] 日本 东京都 东京 hostuniversal.com.au
0.24 ms         AS136557 [Ransom_IT_Infrastructure] 日本 东京都 东京 hostuniversal.com.au
0.26 ms         * [CDN77-Int] 日本 东京都 东京
0.42 ms         AS2914 [NTTGIN] 日本 东京都 东京 ntt.net
1.30 ms         AS2914 [NTT-BACKBONE] 日本 东京都 东京 ntt.net
60.77 ms        AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
67.08 ms        AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
64.10 ms        AS17816 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
65.60 ms        AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
64.27 ms        AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.41 ms         AS136557 [HOST-AU] 日本 东京都 东京 hostuniversal.com.au
0.41 ms         AS136557 [HOST-AU] 日本 东京都 东京 hostuniversal.com.au
0.33 ms         AS136557 [Ransom_IT_Infrastructure] 日本 东京都 东京 hostuniversal.com.au
0.34 ms         * [CDN77-Int] 日本 东京都 东京
0.43 ms         AS2914 [NTTGIN] 日本 东京都 东京 ntt.net
204.61 ms       AS2914 [NTT-BACKBONE] 日本 东京都 东京 ntt.net
52.21 ms        AS2914 [NTT-BACKBONE] 中国 香港 ntt.net
52.36 ms        AS2914 [NTT-GLOBAL] 中国 香港 ntt.net
52.41 ms        AS58453 [CMI-INT] 中国 香港 cmi.chinamobile.com 移动
160.32 ms       AS58453 [CMI-INT] 中国 广东省 广州市 cmi.chinamobile.com 移动
178.32 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
189.82 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
286.13 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
187.30 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
282.16 ms       AS9808 [CMNET] 中国 海南省 海口市 chinamobile.com 移动
184.90 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    946.47 Mbps     889.53 Mbps     0.25     NULL
日本东京         454.46 Mbps     833.65 Mbps     140.74   6.6%
新加坡           318.09 Mbps     888.31 Mbps     88.15    0.0%
联通WuXi         17.42 Mbps      52.80 Mbps      39.40    5.5%
联通湖南5G       284.68 Mbps     10.29 Mbps      52.14    NULL
电信Zhenjiang5G  39.93 Mbps      851.88 Mbps     93.33    NULL
移动Chengdu      843.15 Mbps     831.65 Mbps     208.76   0.0%
移动硬核通信     85.10 Mbps      14.89 Mbps      190.33   NULL
------------------------------------------------------------------------
 总共花费      : 5 分 36 秒
 时间          : Tue Aug 29 12:02:08 CST 2023
------------------------------------------------------------------------
```

### Bench

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 3900X 12-Core Processor
 CPU Cores          : 2 @ 3792.872 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 59.9 GB (2.2 GB Used)
 Total Mem          : 3.8 GB (359.3 MB Used)
 System uptime      : 0 days, 0 hour 38 min
 Load average       : 0.00, 0.01, 0.09
 OS                 : Debian GNU/Linux 12
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.1.0-9-amd64
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS142594 SpeedyPage Ltd
 Location           : Motoyoyogichō / JP
 Region             : Tokyo
----------------------------------------------------------------------
 I/O Speed(1st run) : 581 MB/s
 I/O Speed(2nd run) : 778 MB/s
 I/O Speed(3rd run) : 748 MB/s
 I/O Speed(average) : 702.3 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    932.12 Mbps       878.01 Mbps         0.36 ms     
 Los Angeles, US  706.62 Mbps       818.92 Mbps         109.18 ms   
 Dallas, US       583.10 Mbps       847.28 Mbps         137.10 ms   
 Montreal, CA     308.57 Mbps       263.96 Mbps         181.94 ms   
 Paris, FR        299.92 Mbps       851.24 Mbps         255.86 ms   
 Amsterdam, NL    333.07 Mbps       785.15 Mbps         241.16 ms   
 Nanjing, CN      91.38 Mbps        1.53 Mbps           115.88 ms   
 Hongkong, CN     4.83 Mbps         4.79 Mbps           50.58 ms    
 Singapore, SG    850.74 Mbps       825.92 Mbps         93.34 ms    
 Tokyo, JP        475.10 Mbps       854.26 Mbps         137.85 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 0 sec
 Timestamp          : 2023-08-29 12:18:50 CST
----------------------------------------------------------------------
```

### Benchmark

```
------------------------------------------------------------------------
Benchmark Run: Tue Aug 29 2023 12:25:19 - 12:53:15
2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       48984971.2 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     8749.5 MWIPS (9.9 s, 7 samples)
Execl Throughput                               3638.5 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        940949.8 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          250290.9 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       2772459.5 KBps  (30.0 s, 2 samples)
Pipe Throughput                             1749067.7 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 109172.1 lps   (10.0 s, 7 samples)
Process Creation                               8396.6 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  11655.3 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   2136.2 lpm   (60.0 s, 2 samples)
System Call Overhead                        1963697.9 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   48984971.2   4197.5
Double-Precision Whetstone                       55.0       8749.5   1590.8
Execl Throughput                                 43.0       3638.5    846.2
File Copy 1024 bufsize 2000 maxblocks          3960.0     940949.8   2376.1
File Copy 256 bufsize 500 maxblocks            1655.0     250290.9   1512.3
File Copy 4096 bufsize 8000 maxblocks          5800.0    2772459.5   4780.1
Pipe Throughput                               12440.0    1749067.7   1406.0
Pipe-based Context Switching                   4000.0     109172.1    272.9
Process Creation                                126.0       8396.6    666.4
Shell Scripts (1 concurrent)                     42.4      11655.3   2748.9
Shell Scripts (8 concurrent)                      6.0       2136.2   3560.4
System Call Overhead                          15000.0    1963697.9   1309.1
                                                                   ========
System Benchmarks Index Score                                        1616.4

------------------------------------------------------------------------
Benchmark Run: Tue Aug 29 2023 12:53:15 - 13:21:12
2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables       96252850.8 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    17526.8 MWIPS (10.0 s, 7 samples)
Execl Throughput                               6375.3 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1261542.0 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          324945.5 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       3604976.4 KBps  (30.0 s, 2 samples)
Pipe Throughput                             3474312.9 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 401321.6 lps   (10.0 s, 7 samples)
Process Creation                              17995.0 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  15955.8 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   2152.5 lpm   (60.0 s, 2 samples)
System Call Overhead                        3149910.0 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   96252850.8   8247.9
Double-Precision Whetstone                       55.0      17526.8   3186.7
Execl Throughput                                 43.0       6375.3   1482.6
File Copy 1024 bufsize 2000 maxblocks          3960.0    1261542.0   3185.7
File Copy 256 bufsize 500 maxblocks            1655.0     324945.5   1963.4
File Copy 4096 bufsize 8000 maxblocks          5800.0    3604976.4   6215.5
Pipe Throughput                               12440.0    3474312.9   2792.9
Pipe-based Context Switching                   4000.0     401321.6   1003.3
Process Creation                                126.0      17995.0   1428.2
Shell Scripts (1 concurrent)                     42.4      15955.8   3763.2
Shell Scripts (8 concurrent)                      6.0       2152.5   3587.6
System Call Overhead                          15000.0    3149910.0   2099.9
                                                                   ========
System Benchmarks Index Score                                        2730.7



======= Script description and score comparison completed! ======= 
```

### PassMark

```
AMD Ryzen 9 3900X 12-Core Processor (x86_64)
2 cores @ 0 MHz  |  3.8 GiB RAM
Number of Processes: 2  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          4907
  Integer Math                     11292 Million Operations/s
  Floating Point Math              8277 Million Operations/s
  Prime Numbers                    34.8 Million Primes/s
  Sorting                          6884 Thousand Strings/s
  Encryption                       2771 MB/s
  Compression                      48852 KB/s
  CPU Single Threaded              2557 Million Operations/s
  Physics                          583 Frames/s
  Extended Instructions (SSE)      3806 Million Matrices/s

Memory Mark:                       1889
  Database Operations              1567 Thousand Operations/s
  Memory Read Cached               28868 MB/s
  Memory Read Uncached             12644 MB/s
  Memory Write                     10220 MB/s
  Available RAM                    2816 Megabytes
  Memory Latency                   51 Nanoseconds
  Memory Threaded                  22589 MB/s
--------------------------------------------------------------------------
```

### 流媒体解锁测试

```
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: JP)
 Netflix:                               Yes (Region: JP)
 YouTube Premium:                       Yes (Region: JP)
 Amazon Prime Video:                    Yes (Region: JP)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   JP
 Viu.com:                               No
 YouTube CDN:                           Tokyo 
 Netflix Preferred CDN:                 Tokyo  
 Spotify Registration:                  Yes (Region: JP)
 Steam Currency:                        JPY
 ChatGPT:                               Yes
=======================================
===============[ Japan ]===============
 DMM:                                   Yes
 DMM TV:                                No
 Abema.TV:                              No
 Niconico:                              No
 music.jp:                              No
 Telasa:                                No
 U-NEXT:                                Failed (Network Connection)
 Hulu Japan:                            No
 TVer:                                  Failed (Network Connection)
 GYAO!:                                 Yes
 WOWOW:                                 Failed
 VideoMarket:                           Failed (Unexpected Result: 404)
 FOD(Fuji TV):                          No
 Radiko:                                No
 Karaoke@DAM:                           Yes
 J:com On Demand:                       Yes
 ---Game---
 Kancolle Japan:                        No
 Pretty Derby Japan:                    No
 Konosuba Fantastic Days:               Yes
 Princess Connect Re:Dive Japan:        Yes
 World Flipper Japan:                   Yes
 Project Sekai: Colorful Stage:         Yes
=======================================


 ** 正在测试IPv6解锁情况 
--------------------------------
 ** 您的网络为: Mario (2a06:a005:19e0:*:*) 


============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: JP)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: AU)
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Taipei 
 Netflix Preferred CDN:                 Hong Kong  
 Spotify Registration:                  Yes (Region: JP)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
===============[ Japan ]===============
 DMM:                                   Unsupported
 DMM TV:                                Yes
 Abema.TV:                              Failed (Network Connection)
 Niconico:                              Failed (Network Connection)
 music.jp:                              No
 Telasa:                                Failed (Network Connection)
 Paravi:                                Failed (Network Connection)
 U-NEXT:                                Failed (Network Connection)
 Hulu Japan:                            Yes
 TVer:                                  Failed (Network Connection)
 GYAO!:                                 IPv6 Not Supported
 WOWOW:                                 Failed
 VideoMarket:                           IPv6 Not Supported
 FOD(Fuji TV):                          No
 Radiko:                                Unsupported
 Karaoke@DAM:                           Failed (Network Connection)
 J:com On Demand:                       Yes
 ---Game---
 Kancolle Japan:                        Failed (Network Connection)
 Pretty Derby Japan:                    No
 Konosuba Fantastic Days:               Failed (Network Connection)
 Princess Connect Re:Dive Japan:        Failed (Network Connection)
 World Flipper Japan:                   Yes
 Project Sekai: Colorful Stage:         Failed (Network Connection)
=======================================
```

### 全球PING

![](https://cdn.lirica.cn/wordpress/2023/08/image-7-1024x559.png)

### Network

```
---------------------------- network-speed.xyz ----------------------------
      A simple script to test network performance using speedtest-cli      
---------------------------------------------------------------------------
 Version            : v2023.08.28
 Global Speedtest   : wget -qO- network-speed.xyz | bash
 Region Speedtest   : wget -qO- network-speed.xyz | bash -s -- -r <region>
---------------------------------------------------------------------------
 Basic System Info
---------------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 3900X 12-Core Processor
 CPU Cores          : 2 @ 3792.872 MHz
 CPU Cache          : 512 KB
 AES-NI             : ✔ Enabled
 VM-x/AMD-V         : ✔ Enabled
 Total Disk         : 59.9 GB (2.6 GB Used)
 Total RAM          : 3.8 GB (531.7 MB Used)
 System uptime      : 0 days, 2 hour 1 min
 Load average       : 0.00, 0.49, 1.68
 OS                 : Debian GNU/Linux 12
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.1.0-9-amd64
 Virtualization     : KVM
---------------------------------------------------------------------------
 Basic Network Info
---------------------------------------------------------------------------
 Primary Network    : IPv6
 ISP                : Mario
 ASN                : AS212294 Mario Gomez Canadas
 ASN (IPv4)         : AS142594 SpeedyPage Ltd
 Host               : Mario
 Location           : Pyongyang, Pyongyang-01, North Korea
 Location (IPv4)    : Motoyoyogichō, Tokyo, JP
---------------------------------------------------------------------------
 Speedtest.net (Region: ASIA)
---------------------------------------------------------------------------
 Location         Latency     Loss    DL Speed       UP Speed       Server      

 ISP: SpeedyPage Ltd 

 Nearest          0.22 ms     N/A     878.62 Mbps    931.03 Mbps    fdcservers.net - Tokyo 

 Mumbai, IN       234.70 ms   0.0%    821.87 Mbps    333.38 Mbps    i3D.net - Mumbai 
 Chennai, IN      111.80 ms   N/A     865.25 Mbps    667.37 Mbps    Jio - Chennai 
 Bangalore, IN    256.56 ms   0.0%    833.68 Mbps    315.92 Mbps    Bharti Airtel Ltd - Bangalore 
 Singapore, SG    80.86 ms    0.0%    868.83 Mbps    877.53 Mbps    MyRepublic Singapore - Singapore 
 Singapore, SG    83.08 ms    N/A     871.17 Mbps    862.63 Mbps    StarHub Ltd - Singapore 
```
