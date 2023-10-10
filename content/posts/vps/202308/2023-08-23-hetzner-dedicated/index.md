---
title: "Hetzner Dedicated 测评"
date: "2023-08-23"
categories: 
  - "vps"
  - "eu"
---

## 套餐价格

Optimize your workload with AMD Milan Epyc™ 7003 and AMD Genoa Epyc™ 9654 processors.

![](https://catcat.blog/wp-content/uploads/2023/08/image-6-1024x485.png)

## Yabs

```
Wed Aug 23 08:38:40 AM UTC 2023

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 1 minutes
Processor  : AMD EPYC Processor
CPU cores  : 2 @ 2445.404 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ❌ Disabled
RAM        : 7.6 GiB
Swap       : 0.0 KiB
Disk       : 75.0 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-10-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Hetzner Online GmbH
ASN        : AS212317 Hetzner Online GmbH
Host       : Hetzner
Location   : Ashburn, Virginia (VA)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 196.56 MB/s  (49.1k) | 1.85 GB/s    (28.9k)
Write      | 197.08 MB/s  (49.2k) | 1.86 GB/s    (29.0k)
Total      | 393.64 MB/s  (98.4k) | 3.71 GB/s    (57.9k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.24 GB/s     (4.3k) | 2.39 GB/s     (2.3k)
Write      | 2.36 GB/s     (4.6k) | 2.55 GB/s     (2.4k)
Total      | 4.60 GB/s     (8.9k) | 4.95 GB/s     (4.8k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 25.0 Mbits/sec  | busy            | 160 ms         
Scaleway        | Paris, FR (10G)           | busy            | 1.22 Gbits/sec  | 160 ms         
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 162 ms         
Uztelecom       | Tashkent, UZ (10G)        | 836 Mbits/sec   | 693 Mbits/sec   | 231 ms         
Clouvider       | NYC, NY, US (10G)         | 1.92 Gbits/sec  | 104 Mbits/sec   | 87.5 ms        
Clouvider       | Dallas, TX, US (10G)      | 89.0 Mbits/sec  | 201 Mbits/sec   | 57.9 ms        
Clouvider       | Los Angeles, CA, US (10G) | 161 Mbits/sec   | 440 Mbits/sec   | 26.5 ms        

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 24.8 Mbits/sec  | 42.1 Mbits/sec  | 159 ms         
Scaleway        | Paris, FR (10G)           | 1.27 Gbits/sec  | 1.08 Gbits/sec  | 167 ms         
NovoServe       | North Holland, NL (40G)   | 1.05 Gbits/sec  | busy            | 162 ms         
Uztelecom       | Tashkent, UZ (10G)        | 605 Mbits/sec   | 585 Mbits/sec   | 231 ms         
Clouvider       | NYC, NY, US (10G)         | busy            | 119 Mbits/sec   | 87.6 ms        
Clouvider       | Dallas, TX, US (10G)      | 45.7 Mbits/sec  | 204 Mbits/sec   | 57.8 ms        
Clouvider       | Los Angeles, CA, US (10G) | 151 Mbits/sec   | 318 Mbits/sec   | 26.5 ms        

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1354                          
Multi Core      | 1756                          
Full Test       | https://browser.geekbench.com/v6/cpu/2359162
```

## lscpu

```
root@debian-8gb-hil-1:~# lscpu
Architecture:            x86_64
  CPU op-mode(s):        32-bit, 64-bit
  Address sizes:         40 bits physical, 48 bits virtual
  Byte Order:            Little Endian
CPU(s):                  2
  On-line CPU(s) list:   0,1
Vendor ID:               AuthenticAMD
  BIOS Vendor ID:        QEMU
  Model name:            AMD EPYC Processor
    BIOS Model name:     NotSpecified  CPU @ 2.0GHz
    BIOS CPU family:     1
    CPU family:          25
    Model:               1
    Thread(s) per core:  2
    Core(s) per socket:  1
    Socket(s):           1
    Stepping:            1
    BogoMIPS:            4890.80
Virtualization features: 
  Hypervisor vendor:     KVM
  Virtualization type:   full
Caches (sum of all):     
  L1d:                   32 KiB (1 instance)
  L1i:                   32 KiB (1 instance)
  L2:                    512 KiB (1 instance)
  L3:                    32 MiB (1 instance)
NUMA:                    
  NUMA node(s):          1
  NUMA node0 CPU(s):     0,1
Vulnerabilities:         
  Itlb multihit:         Not affected
  L1tf:                  Not affected
  Mds:                   Not affected
  Meltdown:              Not affected
  Mmio stale data:       Not affected
  Retbleed:              Not affected
  Spec store bypass:     Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:            Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:            Mitigation; Retpolines, IBPB conditional, IBRS_FW, STIBP conditional, RSB fi
                         lling, PBRSB-eIBRS Not affected
  Srbds:                 Not affected
  Tsx async abort:       Not affected
```

## LemonBench

```
-> System Information

 CPU Model Name:                AMD EPYC Processor
 CPU Cache Size:                L1: 32.00 KB / L2: 512.00 KB / L3: 32.00 MB
 CPU Specifications:            2 vCPU(s)
 Virtualization Ready:          No
 Virtualization Type:           KVM
 Memory Usage:                  159.14 MiB / 7.57 GiB
 Swap Usage:                    [ no swap partition or swap file detected ]
 Disk Usage:                    3.51 GiB / 74.81 GiB
 Boot Disk:                     /dev/sda1
 OS Release:                    Debian GNU/Linux 12 (bookworm) (x86_64)
 Kernel Version:                6.1.0-10-amd64

 -> Network Information

 IPv4-IP Address:               [US] 5.78.40.94
 IPv4-AS Information:           AS212317 - Hetzner Online GmbH
 IPv4-GeoIP Location:           United States Oregon Portland

 -> Streaming Service Unlock Test

 Netflix:                       Netflix Only
 HBO Now:                       Yes
 Youtube Premium:               Yes (GeoIP: DE)
 Tiktok Region:                 No
 BBC iPlayer:                   Yes
 NicoNico:                      No
 Princonne Re:dive Japan:       Yes
 Pretty Derby Japan:            Yes
 Kantai Collection Japan:       No
 Bahamut Anime:                 No
 Bilibili (China Mainland):     No
 Bilibili (China SAR&Taiwan):   No
 Bilibili (China Taiwan):       No
 Steam Price Currency:          USD

 -> CPU Performance Test (Fast mode, 1-Pass @ 5sec)

 1 Thread(s) Test:              3649.22 Scores (1.00x)
 2 Thread(s) Test:              4123.90 Scores (1.13x)

 -> Disk Performance Test (Using FIO, Direct mode, 32 IO-Depth)

 Write Test (4K-Block):         248.76 MB/s (63681 IOPS)
 Read  Test (4K-Block):         318.47 MB/s (81528 IOPS)
 Write Test (128K-Block):       2631.58 MB/s (21052 IOPS)
 Read  Test (128K-Block):       2380.95 MB/s (19047 IOPS)

 -> Network Speedtest Test (Using Ookla Speedtest, Fast Test Mode)

 Node Name                      Download Speed  Upload Speed    Ping Latency    Server Name
 Speedtest Default:             6399.24 Mbps    8480.52 Mbps    0.71 ms LS Networks, United States Portland, OR
```

## PassMark PerformanceTest

```
AMD EPYC Processor (x86_64)
1 cores @ 0 MHz  |  7.6 GiB RAM
Number of Processes: 2  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          3019
  Integer Math                     8359 Million Operations/s
  Floating Point Math              4620 Million Operations/s
  Prime Numbers                    19.0 Million Primes/s
  Sorting                          4624 Thousand Strings/s
  Encryption                       2171 MB/s
  Compression                      26767 KB/s
  CPU Single Threaded              2038 Million Operations/s
  Physics                          383 Frames/s
  Extended Instructions (SSE)      1759 Million Matrices/s

Memory Mark:                       1968
  Database Operations              776 Thousand Operations/s
  Memory Read Cached               24329 MB/s
  Memory Read Uncached             19200 MB/s
  Memory Write                     19668 MB/s
  Available RAM                    6834 Megabytes
  Memory Latency                   66 Nanoseconds
  Memory Threaded                  23089 MB/s
--------------------------------------------------------------------------
```

## 融合怪脚本测试

```
--------------------- A Bench Script By spiritlhl ----------------------
                   测评频道: https://t.me/vps_reviews                    
版本：2023.08.20
更新日志：VPS融合怪测试(集百家之长)                       
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC Processor
 CPU 核心数        : 2
 CPU 频率          : 2445.404 MHz
 CPU 缓存          : L1: 32.00 KB / L2: 512.00 KB / L3: 32.00 MB
 硬盘空间          : 3.81 GiB / 74.81 GiB
 启动盘路径        : /dev/sda1
 内存              : 202.34 MiB / 7.57 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 31 min
 负载              : 0.21, 0.38, 0.37
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-10-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS212317 Hetzner Online GmbH
 IPV4 位置         : Hillsboro / Oregon / US
 IPV6 ASN          : AS212317 Hetzner Online GmbH
 IPV6 位置         : Ashburn / Virginia
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           3646 Scores
 2 线程测试(多核)得分:          4119 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          41613.07 MB/s
 单线程写测试:          25815.35 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         69.7 MB/s (17.02 IOPS, 1.50s))          74.7 MB/s (18238 IOPS, 1.40s)
 1GB-1M Block           1.8 GB/s (1676 IOPS, 0.60s)             990 MB/s (944 IOPS, 1.06s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 189.55 MB/s  (47.3k) | 1.81 GB/s    (28.4k)
Write      | 190.05 MB/s  (47.5k) | 1.82 GB/s    (28.5k)
Total      | 379.60 MB/s  (94.9k) | 3.64 GB/s    (56.9k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.13 GB/s     (4.1k) | 2.33 GB/s     (2.2k)
Write      | 2.25 GB/s     (4.3k) | 2.49 GB/s     (2.4k)
Total      | 4.38 GB/s     (8.5k) | 4.83 GB/s     (4.7k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA30S12)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA09S34)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：美国
[IPv6]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
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
 YouTube Premium:                       Yes (Region: DE)
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Seattle, WA 
 Netflix Preferred CDN:                 Portland, OR  
 Spotify Registration:                  No
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: DE)
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Seattle, WA 
 Netflix Preferred CDN:                 Miami, FL  
 Spotify Registration:                  No
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
欺诈分数(越低越好): 60②
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
Google搜索可行性：NO
端口25检测:
  本地: No
  163邮箱：No
------以下为IPV6检测------
欺诈分数(越低越好): 32②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/08/23 09:11:03 北京电信 219.141.136.12  电信163 [普通线路]           
2023/08/23 09:11:03 北京联通 202.106.50.1    联通4837[普通线路]           
2023/08/23 09:11:03 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/08/23 09:11:03 上海电信 202.96.209.133  电信163 [普通线路]           
2023/08/23 09:11:03 上海联通 210.22.97.1     联通4837[普通线路]           
2023/08/23 09:11:03 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/08/23 09:11:03 广州电信 58.60.188.222   电信163 [普通线路]           
2023/08/23 09:11:03 广州联通 210.21.196.6    联通4837[普通线路]           
2023/08/23 09:11:03 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/08/23 09:11:03 成都电信 61.139.2.69     电信163 [普通线路]           
2023/08/23 09:11:03 成都联通 119.6.6.6       联通4837[普通线路]           
2023/08/23 09:11:03 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
2.20 ms         * [RFC1918] 局域网
0.21 ms         AS212317 美国 俄勒冈州 希尔斯伯勒 hetzner.com
1.04 ms         AS212317 美国 俄勒冈州 波特兰 hetzner.com
0.65 ms         AS212317 美国 俄勒冈州 波特兰 hetzner.com
1.58 ms         AS3356 美国 俄勒冈州 波特兰 level3.com
14.73 ms        AS3356 美国 加利福尼亚州 圣何塞 level3.com
16.61 ms        AS3356 美国 加利福尼亚州 圣何塞 level3.com
171.25 ms       AS4134 [CHINANET-BB] 中国 chinatelecom.com.cn 电信
380.43 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
270.63 ms       AS134774 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.cn 电信
274.68 ms       AS4134 中国 广东省 深圳市 chinatelecom.com.cn 电信
广州联通 210.21.196.6
2.73 ms         * [RFC1918] 局域网
0.75 ms         AS212317 美国 俄勒冈州 希尔斯伯勒 hetzner.com
1.47 ms         AS212317 美国 俄勒冈州 波特兰 hetzner.com
0.92 ms         AS212317 美国 俄勒冈州 波特兰 hetzner.com
1.12 ms         AS6453 美国 俄勒冈州 希尔斯伯勒 tatacommunications.com
34.75 ms        AS6453 美国 加利福尼亚州 圣何塞 tatacommunications.com
22.94 ms        AS6453 美国 加利福尼亚州 圣何塞 tatacommunications.com
160.38 ms       AS4837 [CU169-BACKBONE] 中国 北京市 chinaunicom.cn 联通
201.21 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
200.29 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
223.81 ms       AS4837 [CU169-BACKBONE] 中国 山西省 太原市 chinaunicom.cn 联通
221.87 ms       AS17816 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
220.64 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
194.51 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
广州移动 120.196.165.24
2.73 ms         * [RFC1918] 局域网
0.75 ms         AS212317 美国 俄勒冈州 希尔斯伯勒 hetzner.com
1.23 ms         AS212317 美国 俄勒冈州 波特兰 hetzner.com
0.82 ms         AS212317 美国 俄勒冈州 波特兰 hetzner.com
1.45 ms         AS212317 美国 俄勒冈州 波特兰 hetzner.com
1.23 ms         AS6453 美国 俄勒冈州 希尔斯伯勒 tatacommunications.com
15.60 ms        AS6453 美国 加利福尼亚州 圣何塞 tatacommunications.com
17.47 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 圣何塞 cogentco.com
16.50 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 圣何塞 cogentco.com
27.24 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
27.42 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
27.91 ms        AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
29.54 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
28.78 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
27.36 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
158.16 ms       AS58453 [CMI-INT] 中国 广东省 广州市 cmi.chinamobile.com 移动
160.07 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
203.01 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
188.80 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
203.18 ms       AS9808 [CMNET] 中国 海南省 海口市 chinamobile.com 移动
211.55 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    949.10 Mbps     949.59 Mbps     1.06     NULL
洛杉矶           3199.50 Mbps    8929.97 Mbps    25.82    0.0%
日本东京         635.07 Mbps     5180.43 Mbps    134.52   0.0%
联通Fuzhou       236.11 Mbps     639.46 Mbps     213.36   0.0%
电信Zhenjiang5G  1.55 Mbps       1474.00 Mbps    258.25   NULL
移动Chengdu      225.82 Mbps     212.78 Mbps     223.26   0.0%
移动陕西5G       2.17 Mbps       12337.66 Mbps   221.83   5.6%
------------------------------------------------------------------------
 总共花费      : 5 分 55 秒
 时间          : Arb Leq 23  9:15:25 saaku UTC 2023
------------------------------------------------------------------------
```

## 德国

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 1 minutes
Processor  : AMD EPYC-Milan Processor
CPU cores  : 2 @ 2396.398 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ❌ Disabled
RAM        : 7.6 GiB
Swap       : 0.0 KiB
Disk       : 75.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-25-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Hetzner Online GmbH
ASN        : AS24940 Hetzner Online GmbH
Host       : Hetzner
Location   : Gunzenhausen, Bavaria (BY)
Country    : Germany

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 244.24 MB/s  (61.0k) | 2.73 GB/s    (42.7k)
Write      | 244.88 MB/s  (61.2k) | 2.75 GB/s    (43.0k)
Total      | 489.13 MB/s (122.2k) | 5.48 GB/s    (85.7k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.11 GB/s     (8.0k) | 4.38 GB/s     (4.2k)
Write      | 4.32 GB/s     (8.4k) | 4.67 GB/s     (4.5k)
Total      | 8.43 GB/s    (16.4k) | 9.05 GB/s     (8.8k)

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1621                          
Multi Core      | 2124                          
Full Test       | https://browser.geekbench.com/v6/cpu/2794067
```
