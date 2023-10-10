---
title: "Hostaris 德国 AMD 5950X 测试"
date: "2023-09-13"
categories: 
  - "vps"
  - "performance"
  - "eu"
---

> ## 套餐
> 
> **_Provider :_ Hostaris  
> _Type/Plan :_ KVM-RYZEN-2GB  
> _Processor : AMD Ryzen 9 5950X_  
> _Num of Core : 1 Cores_  
> _Memory : 2 GB_  
> _Storage : 20 GB NVMe_  
> _Bandwidth : 4T @ 1 Gbps IN | 1 Gbps OUT_  
> _Location :_ DE  
> _Price :_ £4/month / £10.20/quarter / £36/year**

## 测评

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 2 hours, 1 minutes
Processor  : AMD Ryzen 9 5950X 16-Core Processor
CPU cores  : 1 @ 3393.624 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 0.0 KiB
Disk       : 19.3 GiB
Distro     : Ubuntu 22.04.3 LTS
Kernel     : 5.15.0-71-generic
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Hostaris Limited
ASN        : AS199765 Hostaris Limited
Host       : Hostaris Limited
Location   : Frankfurt am Main, Hesse (HE)
Country    : Germany

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 347.38 MB/s  (86.8k) | 2.91 GB/s    (45.5k)
Write      | 348.30 MB/s  (87.0k) | 2.92 GB/s    (45.7k)
Total      | 695.68 MB/s (173.9k) | 5.84 GB/s    (91.2k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.05 GB/s     (5.9k) | 3.36 GB/s     (3.2k)
Write      | 3.21 GB/s     (6.2k) | 3.58 GB/s     (3.5k)
Total      | 6.26 GB/s    (12.2k) | 6.94 GB/s     (6.7k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 164 Mbits/sec   | 301 Mbits/sec   | 15.8 ms        
Scaleway        | Paris, FR (10G)           | 683 Mbits/sec   | busy            | 20.8 ms        
NovoServe       | North Holland, NL (40G)   | busy            | 892 Mbits/sec   | 12.9 ms        
Uztelecom       | Tashkent, UZ (10G)        | 773 Mbits/sec   | 484 Mbits/sec   | 101 ms         
Clouvider       | NYC, NY, US (10G)         | 42.8 Mbits/sec  | 41.7 Mbits/sec  | 91.7 ms        
Clouvider       | Dallas, TX, US (10G)      | 17.0 Mbits/sec  | 82.5 Mbits/sec  | 123 ms         
Clouvider       | Los Angeles, CA, US (10G) | 17.1 Mbits/sec  | 30.2 Mbits/sec  | 149 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 250 Mbits/sec   | 350 Mbits/sec   | 15.7 ms        
Scaleway        | Paris, FR (10G)           | 885 Mbits/sec   | busy            | 17.1 ms        
NovoServe       | North Holland, NL (40G)   | 892 Mbits/sec   | 891 Mbits/sec   | 12.9 ms        
Uztelecom       | Tashkent, UZ (10G)        | 818 Mbits/sec   | busy            | 100 ms         
Clouvider       | NYC, NY, US (10G)         | 41.7 Mbits/sec  | 31.8 Mbits/sec  | 94.8 ms        
Clouvider       | Dallas, TX, US (10G)      | 31.4 Mbits/sec  | 40.3 Mbits/sec  | 123 ms         
Clouvider       | Los Angeles, CA, US (10G) | 25.6 Mbits/sec  | busy            | 149 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1730                          
Multi Core      | 1706                          
Full Test       | https://browser.geekbench.com/v6/cpu/2583393
```

### benchy

```
Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Ubuntu 22.04.3 LTS                 Model       : AMD Ryzen 9 5950X 16-Core Processor
Location   : Germany                            Core        : 1 @ 3393.624 MHz
Kernel     : 5.15.0-71-generic                  AES-NI      : ✔ Enabled
Uptime     : 0 days, 0 hrs, 31 mins, 53 secs    VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 0.0 KiB   

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 19.2 GiB                           ASN         : AS199765  
Disk Usage : 2.1 GiB (11% Used)                 ISP         : Hostaris Limited
Mem        : 1.9 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.3 GiB (13% Used)                 IPv6        : ✔ Enabled

Disk Performance Check (ext4 on /dev/vda1) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 284.97 MB/s | 285.73 MB/s | 570.71 MB/s | 73.0k  | 73.1k  | 146.1k |
| 64k  | 2.80 GB/s   | 2.82 GB/s   | 5.62 GB/s   | 46.0k  | 46.2k  | 92.2k  |
| 512k | 2.89 GB/s   | 3.04 GB/s   | 5.94 GB/s   | 5.9k   | 6.2k   | 12.2k  |
| 1m   | 3.24 GB/s   | 3.45 GB/s   | 6.69 GB/s   | 3.3k   | 3.5k   | 6.9k   |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |  823.1 Mb/s  |  404.4 Mb/s  |  111.4 ms |
|       | Uztelecom   | Tashkent, UZ    |        busy  |  544.2 Mb/s  |   96.9 ms |
|       | Novogara    | Amsterdam, NL   |  919.7 Mb/s  |  871.5 Mb/s  |   12.2 ms |
|       | FiberBy     | Copenhagen, DK  |  889.8 Mb/s  |  567.7 Mb/s  |   18.4 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |  805.2 Mb/s  |        busy  |  111.3 ms |
|       | Uztelecom   | Tashkent, UZ    |  830.8 Mb/s  |  621.8 Mb/s  |   93.2 ms |
|       | Novogara    | Amsterdam, NL   |  908.6 Mb/s  |  908.9 Mb/s  |   12.3 ms |
|       | FiberBy     | Copenhagen, DK  |  885.9 Mb/s  |  612.0 Mb/s  |   18.3 ms |
+---------------------------------------------------------------------------------+

+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 1715                     |
| Multi Core         | 1701                     |
+-----------------------------------------------+
| https://browser.geekbench.com/v6/cpu/2582809  |
+-----------------------------------------------+
| Benchy time spent  | 11 Minutes 52 Seconds    |
+-----------------------------------------------+
```

### 融合怪脚本

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 5950X 16-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 3393.624 MHz
 CPU 缓存          : L1: 32.00 KB / L2: 512.00 KB / L3: 64.00 MB
 硬盘空间          : 2.07 GiB / 19.20 GiB
 启动盘路径        : /dev/vda1
 内存              : 352.45 MiB / 1.90 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 46 min
 负载              : 0.88, 0.50, 0.30
 系统              : Ubuntu 22.04.3 LTS (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.15.0-71-generic
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 无法检测
 IPV4 ASN          : AS199765 Hostaris Limited
 IPV4 位置         : Frankfurt am Main / Hesse / DE
 IPV6 ASN          : AS199765 Hostaris Limited
 IPV6 位置         : Frankfurt am Main / Hesse
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           5086 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          57556.97 MB/s
 单线程写测试:          34751.35 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         82.1 MB/s (20.04 IOPS, 1.28s))          58.7 MB/s (14324 IOPS, 1.79s)
 1GB-1M Block           2.8 GB/s (2716 IOPS, 0.37s)             2.8 GB/s (2690 IOPS, 0.37s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 339.88 MB/s  (84.9k) | 2.95 GB/s    (46.2k)
Write      | 340.78 MB/s  (85.1k) | 2.97 GB/s    (46.4k)
Total      | 680.67 MB/s (170.1k) | 5.93 GB/s    (92.6k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.02 GB/s     (5.9k) | 3.37 GB/s     (3.2k)
Write      | 3.18 GB/s     (6.2k) | 3.60 GB/s     (3.5k)
Total      | 6.20 GB/s    (12.1k) | 6.97 GB/s     (6.8k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 捷克 布拉格(PRG03S08)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS15S45)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
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
 Dazn:                                  Yes (Region: DE)
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       Failed
 Amazon Prime Video:                    Yes (Region: DE)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   DE
 Viu.com:                               No
 YouTube CDN:                           Prague 
 Netflix Preferred CDN:                 Frankfurt  
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: DE)
 Netflix:                               Yes (Region: DE)
 YouTube Premium:                       No  (Region: CN) 
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Amsterdam 
 Netflix Preferred CDN:                 Frankfurt  
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
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Commercial⑤  hosting⑧  business⑨  
  公司类型(company_type):hosting①  business⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  No② ⑥ ⑨ 
  移动网络(mobile):  Yes⑥ 
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
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测88 ③
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
国家: DE 城市: Frankfurt am Main 服务商: AS199765 Hostaris Limited
北京电信 219.141.136.12  电信163 [普通线路]           
北京联通 202.106.50.1    联通4837[普通线路]           
北京移动 221.179.155.161 移动CMI [普通线路]           
上海电信 202.96.209.133  测试超时
上海联通 210.22.97.1     联通4837[普通线路]           
上海移动 211.136.112.200 移动CMI [普通线路]           
广州电信 58.60.188.222   电信163 [普通线路]           
广州联通 210.21.196.6    测试超时
广州移动 120.196.165.24  移动CMI [普通线路]           
成都电信 61.139.2.69     电信163 [普通线路]           
成都联通 119.6.6.6       联通4837[普通线路]           
成都移动 211.137.96.205  移动CMI [普通线路]           
2023/09/13 00:10:26 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.32 ms         AS199765 德国 黑森州 美因河畔法兰克福 Hostaris Limited
5.11 ms         AS212508 德国 黑森州 美因河畔法兰克福 lowhosting.com
5.35 ms         AS60068 [CDN77-c0r3] 德国 黑森州 美因河畔法兰克福 cdn77.com
7.46 ms         AS3356 [FRANKFURT-SERIAL] 德国 黑森州 美因河畔法兰克福 Level3-CT-Peer level3.com
217.18 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
209.10 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
200.38 ms       AS134774 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.cn 电信
213.48 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.17 ms         AS199765 德国 黑森州 美因河畔法兰克福 Hostaris Limited
5.08 ms         AS212508 德国 黑森州 美因河畔法兰克福 lowhosting.com
5.38 ms         AS60068 [CDN77-c0r3] 德国 黑森州 美因河畔法兰克福 cdn77.com
15.40 ms        AS174 [COGENT-BONE] 法国 法兰西岛大区 巴黎 cogentco.com
97.16 ms        AS174 [COGENT-BONE] 美国 华盛顿哥伦比亚特区 华盛顿 cogentco.com
114.46 ms       AS174 [COGENT-BONE] 美国 佐治亚州 亚历山大 cogentco.com
127.62 ms       AS174 [COGENT-BONE] 美国 德克萨斯州 休斯顿 cogentco.com
142.93 ms       AS174 [COGENT-BONE] 美国 得克萨斯州 埃尔帕索 cogentco.com
161.14 ms       AS174 [COGENT-BONE] 美国 亚利桑那州 凤凰城 cogentco.com
163.99 ms       AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
164.57 ms       AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
230.68 ms       AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
261.33 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
261.64 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
258.93 ms       AS4837 [CU169-BACKBONE] 中国 山西省 太原市 chinaunicom.cn 联通
262.86 ms       AS17816 [UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
263.95 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
262.74 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.10 ms         AS199765 德国 黑森州 美因河畔法兰克福 Hostaris Limited
5.05 ms         AS212508 德国 黑森州 美因河畔法兰克福 lowhosting.com
5.32 ms         AS60068 [CDN77-c0r3] 德国 黑森州 美因河畔法兰克福 cdn77.com
5.43 ms         AS201011 德国 黑森州 美因河畔法兰克福 core-backbone.com
5.58 ms         AS201011 德国 黑森州 美因河畔法兰克福 core-backbone.com
19.02 ms        AS58453 [DE-CIX] 德国 黑森州 美因河畔法兰克福 DE-CIX Frankfurt - China Mobile International - 100Gbps cmi.chinamobile.com
19.68 ms        AS58453 [CMI-INT] 德国 黑森州 美茵河畔法兰克福 cmi.chinamobile.com 移动
267.38 ms       AS58453 [CMI-INT] 德国 黑森州 美因河畔法兰克福 cmi.chinamobile.com 移动
297.15 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
* ms    AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
395.88 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
298.67 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
297.26 ms       AS9808 [CMNET] 中国 海南省 海口市 chinamobile.com 移动
293.97 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    921.49 Mbps     921.26 Mbps     5.25     NULL
法兰克福         909.74 Mbps     909.35 Mbps     5.96     0.0%
新加坡           347.30 Mbps     616.01 Mbps     160.35   1.7%
联通WuXi         697.07 Mbps     632.49 Mbps     179.59   0.0%
联通湖南5G       557.16 Mbps     26.23 Mbps      161.49   NULL
电信天津5G       486.91 Mbps     258.90 Mbps     208.81   0.0%
电信天津         140.95 Mbps     665.62 Mbps     165.46   NULL
移动Chengdu      571.77 Mbps     472.86 Mbps     280.75   0.0%
移动Lanzhou      51.55 Mbps      525.48 Mbps     316.71   NULL
------------------------------------------------------------------------
 总共花费      : 6 分 12 秒
 时间          : Wed Sep 13 00:15:30 BST 2023
------------------------------------------------------------------------
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD Ryzen 9 5950X 16-Core Processor (x86_64)
1 cores @ 0 MHz  |  1.9 GiB RAM
Number of Processes: 1  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          2943
  Integer Math                     7329 Million Operations/s
  Floating Point Math              5937 Million Operations/s
  Prime Numbers                    21.7 Million Primes/s
  Sorting                          4283 Thousand Strings/s
  Encryption                       1592 MB/s
  Compression                      22408 KB/s
  CPU Single Threaded              2755 Million Operations/s
  Physics                          389 Frames/s
  Extended Instructions (SSE)      2409 Million Matrices/s

Memory Mark:                       1337
  Database Operations              937 Thousand Operations/s
  Memory Read Cached               34799 MB/s
  Memory Read Uncached             15043 MB/s
  Memory Write                     11626 MB/s
  Available RAM                    1135 Megabytes
  Memory Latency                   63 Nanoseconds
  Memory Threaded                  17387 MB/s
--------------------------------------------------------------------------
```

### byte-unixbench 性能测试

```
------------------------------------------------------------------------
Benchmark Run: Wed Sep 13 2023 01:52:29 - 02:20:25
1 CPU in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       57403106.1 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    10798.3 MWIPS (10.0 s, 7 samples)
Execl Throughput                               5224.9 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1788151.8 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          480698.8 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       4908230.2 KBps  (30.0 s, 2 samples)
Pipe Throughput                             2832729.5 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 284672.3 lps   (10.0 s, 7 samples)
Process Creation                              17061.5 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  12809.2 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   1714.4 lpm   (60.0 s, 2 samples)
System Call Overhead                        2710202.5 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   57403106.1   4918.9
Double-Precision Whetstone                       55.0      10798.3   1963.3
Execl Throughput                                 43.0       5224.9   1215.1
File Copy 1024 bufsize 2000 maxblocks          3960.0    1788151.8   4515.5
File Copy 256 bufsize 500 maxblocks            1655.0     480698.8   2904.5
File Copy 4096 bufsize 8000 maxblocks          5800.0    4908230.2   8462.5
Pipe Throughput                               12440.0    2832729.5   2277.1
Pipe-based Context Switching                   4000.0     284672.3    711.7
Process Creation                                126.0      17061.5   1354.1
Shell Scripts (1 concurrent)                     42.4      12809.2   3021.0
Shell Scripts (8 concurrent)                      6.0       1714.4   2857.4
System Call Overhead                          15000.0    2710202.5   1806.8
                                                                   ========
System Benchmarks Index Score                                        2440.2



======= Script description and score comparison completed! ======= 
```

### Network-Speed

```
---------------------------- network-speed.xyz ----------------------------
      A simple script to test network performance using speedtest-cli      
---------------------------------------------------------------------------
 Version            : v2023.09.04
 Global Speedtest   : wget -qO- network-speed.xyz | bash
 Region Speedtest   : wget -qO- network-speed.xyz | bash -s -- -r <region>
---------------------------------------------------------------------------
 Basic System Info
---------------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 5950X 16-Core Processor
 CPU Cores          : 1 @ 3393.624 MHz
 CPU Cache          : 512 KB
 AES-NI             : ✔ Enabled
 VM-x/AMD-V         : ✔ Enabled
 Total Disk         : 19.3 GB (2.4 GB Used)
 Total RAM          : 1.9 GB (306.1 MB Used)
 System uptime      : 0 days, 3 hour 23 min
 Load average       : 0.00, 0.05, 0.46
 OS                 : Ubuntu 22.04.3 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.15.0-71-generic
 Virtualization     : KVM
---------------------------------------------------------------------------
 Basic Network Info
---------------------------------------------------------------------------
 Primary Network    : IPv6
 ISP                : Hostaris Limited
 ASN                : AS199765 Hostaris Limited
 Host               : Hostaris Limited
 Location           : Frankfurt am Main, Hesse-HE, Germany
---------------------------------------------------------------------------
 Speedtest.net (Region: GLOBAL)
---------------------------------------------------------------------------
 Location         Latency     Loss    DL Speed       UP Speed       Server      

 ISP: Hostaris Limited 

 Nearest          5.26 ms     N/A     919.24 Mbps    916.72 Mbps    Netprotect - Frankfurt 

 Kochi, IN        195.23 ms   0.0%    629.24 Mbps    443.62 Mbps    Asianet Broadband - Cochin 
 Bangalore, IN    182.53 ms   0.3%    754.00 Mbps    359.38 Mbps    Bharti Airtel Ltd - Bangalore 
 Chennai, IN      166.98 ms   N/A     661.59 Mbps    530.87 Mbps    Jio - Chennai 
 Mumbai, IN       110.87 ms   0.0%    829.85 Mbps    720.40 Mbps    i3D.net - Mumbai 
 Delhi, IN        132.94 ms   0.0%    745.72 Mbps    645.69 Mbps    Tata Teleservices Ltd - New Delhi 

 Seattle, US      157.53 ms   0.0%    786.02 Mbps    556.84 Mbps    Ziply Fiber - Seattle, WA 
 Los Angeles, US  151.90 ms   0.0%    829.36 Mbps    593.77 Mbps    ReliableSite Hosting - Los Angeles, CA 
 Dallas, US       126.47 ms   0.0%    653.85 Mbps    673.84 Mbps    Hivelocity - Dallas, TX 
 Miami, US        173.79 ms   13.2%   540.86 Mbps    0.75 Mbps      AT&T - Miami, FL 
 New York, US     FAILED                                                        
 Toronto, CA      99.34 ms    0.0%    743.26 Mbps    826.00 Mbps    Rogers - Toronto, ON 

 London, UK       16.70 ms    0.0%    900.84 Mbps    889.81 Mbps    VeloxServ Communications - London 
 Amsterdam, NL    FAILED                                                        
 Paris, FR        16.57 ms    N/A     6.45 Mbps      74.63 Mbps     Axione - Paris 
 Frankfurt, DE    5.67 ms     0.0%    890.23 Mbps    893.21 Mbps    23M GmbH - Frankfurt am Main 
 Warsaw, PL       25.26 ms    0.0%    887.07 Mbps    882.24 Mbps    UPC Polska - Warszawa 
 Bucharest, RO    FAILED                                                        

 Jeddah, SA       82.17 ms    0.0%    866.16 Mbps    803.58 Mbps    Saudi Telecom Company 
 Dubai, AE        FAILED                                                        
 Fujairah, AE     FAILED                                                        

 Tokyo, JP        FAILED                                                        
 Shanghai, CU-CN  FAILED                                                        
 Nanjing, CT-CN   FAILED                                                        
 Hong Kong, CN    160.01 ms   N/A     6.08 Mbps      63.96 Mbps     STC - Hong Kong 
 Singapore, SG    160.09 ms   0.0%    682.17 Mbps    560.13 Mbps    i3D.net - Singapore 
 Jakarta, ID      187.11 ms   0.0%    578.14 Mbps    465.54 Mbps    PT. Telekomunikasi Indonesia - Jakarta 
---------------------------------------------------------------------------
 Avg DL Speed       : 679.48 Mbps
 Avg UL Speed       : 573.73 Mbps

 Total DL Data      : 17.22 GB
 Total UL Data      : 13.69 GB
 Total Data         : 30.91 GB
---------------------------------------------------------------------------
 Duration           : 9 min 36 sec
 System Time        : 13/09/2023 - 02:54:54 BST
 Total Script Runs  : 23079
---------------------------------------------------------------------------
 Result             : https://result.network-speed.xyz/r/1694570095_DTLG5B_GLOBAL.txt
---------------------------------------------------------------------------
```

### 国内延迟

![](https://catcat.blog/wp-content/uploads/2023/09/image-74-1024x460.png)

### 全球延迟

![](https://catcat.blog/wp-content/uploads/2023/09/image-75-1024x548.png)
