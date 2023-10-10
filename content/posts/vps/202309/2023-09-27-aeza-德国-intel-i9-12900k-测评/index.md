---
title: "Aeza DE Intel i9-12900K 测评"
date: "2023-09-27"
categories: 
  - "vps"
  - "eu"
---

> 套餐
> 
> Provider : Aeza  
> Type/Plan : IC9-2  
> Processor : ntel Core™ i9-12900k™  
> Num of Core : 2 Cores  
> Memory : 4 GB  
> Storage : 60 GB NVMe  
> Bandwidth : Unlimited @ 1 Gbps IN | 1 Gbps OUT  
> Location : Frankfurt  
> Price : 120RMB

### lscpu

```
12th Gen Intel Core i9-12900K (x86_64)
2 cores @ 3187 MHz  |  3.8 GiB RAM
Number of Processes: 2  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          5788
  Integer Math                     14050 Million Operations/s
  Floating Point Math              13956 Million Operations/s
  Prime Numbers                    21.0 Million Primes/s
  Sorting                          7439 Thousand Strings/s
  Encryption                       3406 MB/s
  Compression                      56792 KB/s
  CPU Single Threaded              3219 Million Operations/s
  Physics                          468 Frames/s
  Extended Instructions (SSE)      4417 Million Matrices/s

Memory Mark:                       1535
  Database Operations              2096 Thousand Operations/s
  Memory Read Cached               29948 MB/s
  Memory Read Uncached             6060 MB/s
  Memory Write                     10356 MB/s
  Available RAM                    3646 Megabytes
  Memory Latency                   65 Nanoseconds
  Memory Threaded                  11564 MB/s
--------------------------------------------------------------------------
```

## 测评

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 3 minutes
Processor  : 12th Gen Intel(R) Core(TM) i9-12900K
CPU cores  : 2 @ 3187.200 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 1024.0 MiB
Disk       : 59.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-21-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv4 Network Information:
---------------------------------
ISP        : AEZA GROUP Ltd
ASN        : AS210644 AEZA INTERNATIONAL LTD
Host       : Aeza Group LLC
Location   : Frankfurt am Main, Hesse (HE)
Country    : Germany

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 120.38 MB/s  (30.0k) | 2.10 GB/s    (32.8k)
Write      | 120.70 MB/s  (30.1k) | 2.11 GB/s    (33.0k)
Total      | 241.09 MB/s  (60.2k) | 4.21 GB/s    (65.8k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.69 GB/s     (5.2k) | 2.81 GB/s     (2.7k)
Write      | 2.83 GB/s     (5.5k) | 2.99 GB/s     (2.9k)
Total      | 5.52 GB/s    (10.7k) | 5.80 GB/s     (5.6k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 842 Mbits/sec   | 377 Mbits/sec   | 18.5 ms        
Scaleway        | Paris, FR (10G)           | 848 Mbits/sec   | 410 Mbits/sec   | 15.9 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 17.2 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | 125 Mbits/sec   | 111 ms         
Clouvider       | NYC, NY, US (10G)         | 649 Mbits/sec   | 179 Mbits/sec   | 156 ms         
Clouvider       | Dallas, TX, US (10G)      | 665 Mbits/sec   | 180 Mbits/sec   | 156 ms         
Clouvider       | Los Angeles, CA, US (10G) | 696 Mbits/sec   | busy            | 149 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 795 Mbits/sec   | 288 Mbits/sec   | 18.5 ms        
Scaleway        | Paris, FR (10G)           | 824 Mbits/sec   | 180 Mbits/sec   | 16.9 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 16.9 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | 95.3 Mbits/sec  | 114 ms         
Clouvider       | NYC, NY, US (10G)         | 699 Mbits/sec   | 79.1 Mbits/sec  | 157 ms         
Clouvider       | Dallas, TX, US (10G)      | 648 Mbits/sec   | 61.0 Mbits/sec  | 156 ms         
Clouvider       | Los Angeles, CA, US (10G) | 585 Mbits/sec   | 101 Mbits/sec   | 149 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1435                          
Multi Core      | 2562                          
Full Test       | https://browser.geekbench.com/v6/cpu/2790396
```

### Bench

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : 12th Gen Intel(R) Core(TM) i9-12900K
 CPU Cores          : 2 @ 3187.200 MHz
 CPU Cache          : 16384 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 59.0 GB (2.8 GB Used)
 Total Mem          : 3.8 GB (81.7 MB Used)
 Total Swap         : 1024.0 MB (0 Used)
 System uptime      : 0 days, 0 hour 19 min
 Load average       : 0.13, 0.52, 0.35
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-21-amd64
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS210644 AEZA INTERNATIONAL LTD
 Location           : Frankfurt am Main / DE
 Region             : Hesse
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.7 GB/s
 I/O Speed(2nd run) : 1.4 GB/s
 I/O Speed(3rd run) : 1.7 GB/s
 I/O Speed(average) : 1638.4 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    785.29 Mbps       782.83 Mbps         11.20 ms    
 Los Angeles, US  428.79 Mbps       57.99 Mbps          175.08 ms   
 Dallas, US       471.18 Mbps       110.40 Mbps         147.17 ms   
```

### 融合怪脚本

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : 12th Gen Intel(R) Core(TM) i9-12900K
 CPU 核心数        : 2
 CPU 频率          : 3187.200 MHz
 CPU 缓存          : L1: 128.00 KB / L2: 8.00 MB / L3: 16.00 MB
 硬盘空间          : 2.82 GiB / 58.98 GiB
 启动盘路径        : /dev/vda1
 内存              : 166.43 MiB / 3.84 GiB
 Swap              : 0 KiB / 1024.00 MiB
 系统在线时间      : 0 days, 0 hour 22 min
 负载              : 0.15, 0.38, 0.32
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-21-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS210644 AEZA INTERNATIONAL LTD
 IPV4 位置         : Frankfurt am Main / Hesse / DE
 IPV6 ASN          : AS210644 AEZA GROUP Ltd
 IPV6 位置         : Amsterdam / North Holland
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           3961 Scores
 2 线程测试(多核)得分:          7295 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          43865.48 MB/s
 单线程写测试:          26144.24 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         60.2 MB/s (14.69 IOPS, 1.74s))          48.3 MB/s (11780 IOPS, 2.17s)
 1GB-1M Block           1.7 GB/s (1661 IOPS, 0.60s)             2.9 GB/s (2741 IOPS, 0.36s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 120.38 MB/s  (30.0k) | 2.10 GB/s    (32.8k)
Write      | 120.69 MB/s  (30.1k) | 2.11 GB/s    (33.0k)
Total      | 241.07 MB/s  (60.2k) | 4.21 GB/s    (65.8k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.77 GB/s     (5.4k) | 2.93 GB/s     (2.8k)
Write      | 2.91 GB/s     (5.7k) | 3.12 GB/s     (3.0k)
Total      | 5.69 GB/s    (11.1k) | 6.06 GB/s     (5.9k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: GIGANET
视频缓存节点地域: KBP(KBP9)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: ARN(ARN09S18)
Youtube识别地域: 俄罗斯联邦(RU)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：德国
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
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
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: DE)
 Netflix:                               Yes (Region: DE)
 YouTube Premium:                       Failed
 Amazon Prime Video:                    Yes (Region: DE)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   DE
 Viu.com:                               No
 YouTube CDN:                           GIGANET in Kiev 
 Netflix Preferred CDN:                 Stockholm  
 Spotify Registration:                  No
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Yes (Region: DE)
 YouTube Premium:                       No 
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Stockholm 
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
欺诈分数(越低越好): 60②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  business
general⑨  
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
  攻击方(attacker):  No⑧   Yes⑨ 
  滥用者(abuser):  No⑧   Yes⑨ 
  威胁(threat):  No⑧   Yes⑨ 
  iCloud中继(icloud_relay):  No① ⑧ ⑨ 
  未分配IP(bogon):  No⑧ ⑨ 
黑名单记录统计(有多少个黑名单网站有记录): 无害54 恶意12 可疑0 未检测23 ③
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
  qq邮箱: Yes
------以下为IPV6检测------
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: DE 城市: Frankfurt am Main 服务商: AS210644 AEZA INTERNATIONAL LTD
北京电信 219.141.136.12  测试超时
北京联通 202.106.50.1    测试超时
北京移动 221.179.155.161 测试超时
上海电信 202.96.209.133  测试超时
上海联通 210.22.97.1     测试超时
上海移动 211.136.112.200 测试超时
广州电信 58.60.188.222   测试超时
广州联通 210.21.196.6    测试超时
广州移动 120.196.165.24  测试超时
成都电信 61.139.2.69     测试超时
成都联通 119.6.6.6       测试超时
成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.20 ms         * RFC1918
5.71 ms         AS210644 德国 黑森州 美因河畔法兰克福 aeza.net
6.13 ms         AS60068 德国 黑森州 美因河畔法兰克福 cdn77.com
206.40 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.11 ms         * RFC1918
5.44 ms         AS60068 德国 黑森州 美因河畔法兰克福 cdn77.com
5.66 ms         AS60068 德国 黑森州 美因河畔法兰克福 cdn77.com
337.26 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.21 ms         * RFC1918
5.67 ms         AS210644 德国 黑森州 美因河畔法兰克福 aeza.net
5.65 ms         AS60068 德国 黑森州 美因河畔法兰克福 cdn77.com
281.84 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    781.46 Mbps     683.37 Mbps     11.57    4.5%
法兰克福         778.79 Mbps     343.20 Mbps     6.27     0.0%
洛杉矶           443.83 Mbps     315.19 Mbps     173.67   0.0%
联通郑州5G       662.41 Mbps     335.51 Mbps     244.26   NULL
联通湖南5G       332.97 Mbps     2.63 Mbps       238.95   NULL
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
12th Gen Intel Core i9-12900K (x86_64)
2 cores @ 3187 MHz  |  3.8 GiB RAM
Number of Processes: 2  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          5788
  Integer Math                     14050 Million Operations/s
  Floating Point Math              13956 Million Operations/s
  Prime Numbers                    21.0 Million Primes/s
  Sorting                          7439 Thousand Strings/s
  Encryption                       3406 MB/s
  Compression                      56792 KB/s
  CPU Single Threaded              3219 Million Operations/s
  Physics                          468 Frames/s
  Extended Instructions (SSE)      4417 Million Matrices/s

Memory Mark:                       1535
  Database Operations              2096 Thousand Operations/s
  Memory Read Cached               29948 MB/s
  Memory Read Uncached             6060 MB/s
  Memory Write                     10356 MB/s
  Available RAM                    3646 Megabytes
  Memory Latency                   65 Nanoseconds
  Memory Threaded                  11564 MB/s
--------------------------------------------------------------------------
```
