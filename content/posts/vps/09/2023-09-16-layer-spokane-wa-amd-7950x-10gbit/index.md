---
title: "Layer Spokane-WA AMD 7950X 10Gbit  测评"
date: "2023-09-16"
categories: 
  - "vps"
  - "performance"
  - "usa"
---

**来自迪拜的商家，据说从2012年就开始在OCF上提供服务，三年前更名为Layer(一家在迪拜注册的公司，贸易许可证号为 900809，并设有真正的办事处),目前拓展到扩展到华盛顿州斯波坎,硬件性能优秀，自带5个备份插槽，带DDOS防护，综合来说还是不错的。机器使用AMD 7950X+DDR5 内存+PCIE4.0 NVME固态，单核性能GB6接近3000分，在我使用的机器里仅次于Crunchbits的VDS，使用观察中ing.**

> ## 套餐
> 
> **_Provider :_ Layer  
> _Type/Plan : L2G_  
> _Processor :_ AMD Ryzen 9 7950X (4.5 GHz++)  
> _Num of Core : 1 Cores_  
> _Memory : 2 GB_ DDR5 RAM  
> _Storage : 50 GB NVMe_(PCIe 4.0)  
> _Bandwidth : 3000GB @ 10 Gbps IN | 10 Gbps OUT_  
> _Location :_ Spokane, WA (North West USA)  
> _Price :_ $9.9 /month**

## 测评

### CPU

![](https://catcat.blog/wp-content/uploads/2023/09/image-91-1024x663.png)

### 硬盘

![](https://catcat.blog/wp-content/uploads/2023/09/image-92.png)

### 内存

![](https://catcat.blog/wp-content/uploads/2023/09/image-93-1024x126.png)

### Yabs

```

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 25 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 1 @ 4499.996 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 0.0 KiB
Disk       : 50.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-20-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Layer
ASN        : Unknown
Host       : Layer
Location   : Spokane, Washington (WA)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 460.71 MB/s (115.1k) | 2.83 GB/s    (44.3k)
Write      | 461.92 MB/s (115.4k) | 2.85 GB/s    (44.5k)
Total      | 922.63 MB/s (230.6k) | 5.69 GB/s    (88.9k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.34 GB/s     (6.5k) | 3.70 GB/s     (3.6k)
Write      | 3.52 GB/s     (6.8k) | 3.95 GB/s     (3.8k)
Total      | 6.87 GB/s    (13.4k) | 7.65 GB/s     (7.4k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 29.2 Mbits/sec  | 39.8 Mbits/sec  | 134 ms         
Scaleway        | Paris, FR (10G)           | 1.39 Gbits/sec  | 1.21 Gbits/sec  | 149 ms         
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 155 ms         
Uztelecom       | Tashkent, UZ (10G)        | 826 Mbits/sec   | 690 Mbits/sec   | 239 ms         
Clouvider       | NYC, NY, US (10G)         | 53.3 Mbits/sec  | 120 Mbits/sec   | 66.8 ms        
Clouvider       | Dallas, TX, US (10G)      | 60.5 Mbits/sec  | 89.0 Mbits/sec  | 72.2 ms        
Clouvider       | Los Angeles, CA, US (10G) | 100 Mbits/sec   | 210 Mbits/sec   | 39.2 ms        

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 28.8 Mbits/sec  | 44.6 Mbits/sec  | 134 ms         
Scaleway        | Paris, FR (10G)           | busy            | busy            | 143 ms         
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 153 ms         
Uztelecom       | Tashkent, UZ (10G)        | 775 Mbits/sec   | 691 Mbits/sec   | 239 ms         
Clouvider       | NYC, NY, US (10G)         | 58.9 Mbits/sec  | 95.9 Mbits/sec  | 66.9 ms        
Clouvider       | Dallas, TX, US (10G)      | 43.7 Mbits/sec  | 114 Mbits/sec   | 72.5 ms        
Clouvider       | Los Angeles, CA, US (10G) | 105 Mbits/sec   | busy            | 39.2 ms        

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2994                          
Multi Core      | 2965                          
Full Test       | https://browser.geekbench.com/v6/cpu/2622619

YABS completed in 12 min 37 sec
```

### GeekBench6

![](https://cdn.lirica.cn/wordpress/2023/09/image-94-1024x331.png)

### Benchy

```

Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Debian GNU/Linux 11 (bullseye)     Model       : AMD Ryzen 9 7950X 16-Core Processor
Location   : United States                      Core        : 1 @ 4499.996 MHz
Kernel     : 5.10.0-20-amd64                    AES-NI      : ✔ Enabled
Uptime     : 0 days, 0 hrs, 2 mins, 29 secs     VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 0.0 KiB   

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 49.9 GiB                           ASN         :           
Disk Usage : 1.9 GiB (4% Used)                  ISP         :           
Mem        : 1.9 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.2 GiB (10% Used)                 IPv6        : ✔ Enabled

Disk Performance Check (xfs on /dev/vda3) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 447.94 MB/s | 449.12 MB/s | 897.06 MB/s | 114.7k | 115.0k | 229.6k |
| 64k  | 2.88 GB/s   | 2.90 GB/s   | 5.78 GB/s   | 47.3k  | 47.5k  | 94.8k  |
| 512k | 3.35 GB/s   | 3.53 GB/s   | 6.89 GB/s   | 6.9k   | 7.2k   | 14.1k  |
| 1m   | 3.67 GB/s   | 3.91 GB/s   | 7.58 GB/s   | 3.8k   | 4.0k   | 7.8k   |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |    2.3 Gb/s  |    2.9 Gb/s  |   64.1 ms |
|       | Uztelecom   | Tashkent, UZ    |  847.5 Mb/s  |  773.8 Mb/s  |  242.3 ms |
|       | Novogara    | Amsterdam, NL   |    1.2 Gb/s  |  663.0 Mb/s  |  151.4 ms |
|       | FiberBy     | Copenhagen, DK  |    1.4 Gb/s  |  260.8 Mb/s  |  143.9 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |    2.4 Gb/s  |    3.0 Gb/s  |   64.4 ms |
|       | Uztelecom   | Tashkent, UZ    |  756.3 Mb/s  |  770.7 Mb/s  |  242.2 ms |
|       | Novogara    | Amsterdam, NL   |    1.1 Gb/s  |    1.2 Gb/s  |  154.8 ms |
|       | FiberBy     | Copenhagen, DK  |    1.4 Gb/s  |  277.8 Mb/s  |  143.9 ms |
+---------------------------------------------------------------------------------+

+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 2969                     |
| Multi Core         | 2962                     |
+-----------------------------------------------+
| https://browser.geekbench.com/v6/cpu/2622417  |
+-----------------------------------------------+
| Benchy time spent  | 10 Minutes 15 Seconds    |
+-----------------------------------------------+
| Benchy result      | http://sprunge.us/tQQDWY |
+-----------------------------------------------+
```

### Bench

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X 16-Core Processor
 CPU Cores          : 1 @ 4499.996 MHz
 CPU Cache          : 1024 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 50.0 GB (1.9 GB Used)
 Total Mem          : 1.9 GB (158.7 MB Used)
 System uptime      : 0 days, 0 hour 38 min
 Load average       : 0.24, 0.34, 0.21
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-20-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS216382 LAYER MARKETING SERVICES L.L.C
 Location           : Spokane / US
 Region             : Washington
----------------------------------------------------------------------
 I/O Speed(1st run) : 3.0 GB/s
 I/O Speed(2nd run) : 4.5 GB/s
 I/O Speed(3rd run) : 4.3 GB/s
 I/O Speed(average) : 4027.7 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    4904.67 Mbps      8957.11 Mbps        15.90 ms    
 Los Angeles, US  2303.63 Mbps      8690.42 Mbps        37.57 ms    
 Dallas, US       1273.01 Mbps      8554.41 Mbps        65.52 ms    
 Montreal, CA     179.84 Mbps       807.97 Mbps         72.73 ms    
 Paris, FR        509.73 Mbps       3930.74 Mbps        178.32 ms   
 Amsterdam, NL    587.99 Mbps       2427.00 Mbps        150.68 ms   
 Shanghai, CN     400.11 Mbps       3691.30 Mbps        181.39 ms   
 Nanjing, CN      3.08 Mbps         3838.31 Mbps        178.26 ms   
 Hongkong, CN     4.87 Mbps         0.25 Mbps           172.98 ms   
 Singapore, SG    530.38 Mbps       4268.14 Mbps        176.96 ms   
 Tokyo, JP        797.45 Mbps       7671.00 Mbps        100.27 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 30 sec
 Timestamp          : 2023-09-16 10:28:17 CST
----------------------------------------------------------------------
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 7950X 16-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 4499.996 MHz
 CPU 缓存          : L1: 64.00 KB / L2: 1.00 MB / L3: 64.00 MB
 硬盘空间          : 1.86 GiB / 49.87 GiB
 启动盘路径        : /dev/vda3
 内存              : 198.64 MiB / 1.90 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 14 min
 负载              : 0.12, 0.26, 0.16
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-20-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS216382 LAYER MARKETING SERVICES L.L.C
 IPV4 位置         : Spokane / Washington / US
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           6544 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          78276.88 MB/s
 单线程写测试:          38903.59 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         48.2 MB/s (11.77 IOPS, 2.18s))          61.4 MB/s (14992 IOPS, 1.71s)
 1GB-1M Block           1.4 GB/s (1342 IOPS, 0.75s)             2.9 GB/s (2796 IOPS, 0.36s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 472.88 MB/s (118.2k) | 2.76 GB/s    (43.2k)
Write      | 474.12 MB/s (118.5k) | 2.78 GB/s    (43.4k)
Total      | 947.00 MB/s (236.7k) | 5.54 GB/s    (86.6k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.33 GB/s     (6.5k) | 3.67 GB/s     (3.5k)
Write      | 3.50 GB/s     (6.8k) | 3.91 GB/s     (3.8k)
Total      | 6.84 GB/s    (13.3k) | 7.58 GB/s     (7.4k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA09S34)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA09S34)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：阿联酋
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：阿联酋
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口所在地区即将开通DisneyPlus，尽请期待哦！
[IPv6]
当前IPv6出口所在地区即将开通DisneyPlus，尽请期待哦！
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: US)
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Yes (Region: AE)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Yes (Region: AE)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Seattle, WA 
 Netflix Preferred CDN:                 Seattle, WA  
 Spotify Registration:                  No
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: AE)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Seattle, WA 
 Netflix Preferred CDN:                 Seattle, WA  
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
  使用类型(usage_type):business①  Commercial⑤  business⑧  
  公司类型(company_type):business①  business⑧  
  云服务提供商(cloud_provider):  No⑧ 
  数据中心(datacenter):  No② ⑥ ⑨ 
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
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测88 ③
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱：No
------以下为IPV6检测------
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: Commercial⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: US 城市: Spokane 服务商: AS216382 LAYER MARKETING SERVICES L.L.C
北京电信 219.141.136.12  电信163 [普通线路]           
北京联通 202.106.50.1    联通4837[普通线路]           
北京移动 221.179.155.161 移动CMI [普通线路]           
上海电信 202.96.209.133  电信163 [普通线路]           
上海联通 210.22.97.1     联通4837[普通线路]           
上海移动 211.136.112.200 移动CMI [普通线路]           
广州电信 58.60.188.222   电信163 [普通线路]           
广州联通 210.21.196.6    联通4837[普通线路]           
广州移动 120.196.165.24  移动CMI [普通线路]           
成都电信 61.139.2.69     电信163 [普通线路]           
成都联通 119.6.6.6       联通4837[普通线路]           
成都移动 211.137.96.205  移动CMI [普通线路]           
2023/09/16 10:00:30 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
4.14 ms         AS216382 美国 华盛顿州 斯波坎
0.44 ms         * RFC1918
19.21 ms        AS2914 美国 华盛顿州 西雅图 ntt.net
28.78 ms        AS2914 [NTT-BACKBONE] 美国 华盛顿州 西雅图 ntt.net
130.77 ms       AS2914 [NTT-BACKBONE] 美国 加利福尼亚州 圣何塞 ntt.net
29.03 ms        AS2914 [NTT-BACKBONE] 美国 加利福尼亚州 圣何塞 ntt.net
36.42 ms        AS4134 [CHINANET-US] 美国 加利福尼亚州 圣克拉拉 chinatelecom.com.cn 电信
189.41 ms       AS4134 [CHINANET-BB] 中国 chinatelecom.com.cn 电信
190.66 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
190.33 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
201.41 ms       AS4134 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.com.cn 电信
193.01 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
7.03 ms         AS216382 美国 华盛顿州 斯波坎
2.47 ms         * RFC1918
23.86 ms        AS2914 美国 华盛顿州 西雅图 ntt.net
33.00 ms        AS2914 [NTT-BACKBONE] 美国 华盛顿州 西雅图 ntt.net
11.42 ms        AS2914 [NTT-BACKBONE] 美国 华盛顿州 西雅图 ntt.net
12.26 ms        AS2914 [NTT-BACKBONE] 美国 华盛顿州 西雅图 ntt.net
36.30 ms        AS3356 美国 加利福尼亚州 洛杉矶 level3.com
193.30 ms       AS3356 美国 加利福尼亚州 洛杉矶 level3.com
190.24 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
189.90 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
190.40 ms       AS17816 [APNIC-AP] 中国 广东省 茂名市 chinaunicom.cn 联通
225.38 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
217.57 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
4.44 ms         AS216382 美国 华盛顿州 斯波坎
1.01 ms         * RFC1918
11.69 ms        AS2914 美国 华盛顿州 西雅图 ntt.net
14.11 ms        AS2914 [NTT-BACKBONE] 美国 华盛顿州 西雅图 ntt.net
107.50 ms       AS2914 [NTT-BACKBONE] 日本 东京都 东京 ntt.net
357.89 ms       AS2914 [NTT-BACKBONE] 中国 香港 ntt.net
153.81 ms       AS2914 [NTT-BACKBONE] 中国 香港 ntt.net
175.12 ms       AS2914 [NTT-GLOBAL] 中国 香港 ntt.net
177.35 ms       AS58453 [CMI-INT] 中国 香港 cmi.chinamobile.com 移动
252.49 ms       AS58453 [CMI-INT] 中国 广东省 广州市 X-I cmi.chinamobile.com 移动
178.08 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
178.58 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
180.34 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
257.19 ms       AS9808 [CMNET] 中国 北京市 chinamobile.com 移动
181.29 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    2331.40 Mbps    8938.77 Mbps    15.94    0.0%
洛杉矶           1283.38 Mbps    9079.91 Mbps    39.42    0.0%
日本东京         1264.38 Mbps    2202.04 Mbps    115.05   NULL
联通湖南5G       199.02 Mbps     19.83 Mbps      180.41   NULL
联通成都         87.26 Mbps      88.15 Mbps      222.23   NULL
电信Nanjing5G    2.12 Mbps       3308.09 Mbps    176.79   0.0%
电信Zhenjiang5G  4.25 Mbps       3117.33 Mbps    184.82   NULL
移动Chengdu      0.68 Mbps       5375.60 Mbps    214.15   8.0%
------------------------------------------------------------------------
 总共花费      : 6 分 12 秒
 时间          : Sat Sep 16 10:05:30 CST 2023
------------------------------------------------------------------------
```

### byte-unixbench 性能测试

```
------------------------------------------------------------------------
Benchmark Run: Sat Sep 16 2023 10:40:13 - 11:08:36
1 CPU in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       79494427.8 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    12958.7 MWIPS (10.0 s, 7 samples)
Execl Throughput                              12599.0 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       2720691.7 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          718028.6 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       8776956.2 KBps  (30.0 s, 2 samples)
Pipe Throughput                             4700807.7 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 487775.3 lps   (10.0 s, 7 samples)
Process Creation                              40456.6 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  23857.5 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   3130.9 lpm   (60.0 s, 2 samples)
System Call Overhead                        5628008.4 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   79494427.8   6811.9
Double-Precision Whetstone                       55.0      12958.7   2356.1
Execl Throughput                                 43.0      12599.0   2930.0
File Copy 1024 bufsize 2000 maxblocks          3960.0    2720691.7   6870.4
File Copy 256 bufsize 500 maxblocks            1655.0     718028.6   4338.5
File Copy 4096 bufsize 8000 maxblocks          5800.0    8776956.2  15132.7
Pipe Throughput                               12440.0    4700807.7   3778.8
Pipe-based Context Switching                   4000.0     487775.3   1219.4
Process Creation                                126.0      40456.6   3210.8
Shell Scripts (1 concurrent)                     42.4      23857.5   5626.8
Shell Scripts (8 concurrent)                      6.0       3130.9   5218.2
System Call Overhead                          15000.0    5628008.4   3752.0
                                                                   ========
System Benchmarks Index Score                                        4248.4
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD Ryzen 9 7950X 16-Core Processor (x86_64)
1 cores @ 4499 MHz  |  1.9 GiB RAM
Number of Processes: 1  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          4043
  Integer Math                     8872 Million Operations/s
  Floating Point Math              7991 Million Operations/s
  Prime Numbers                    32.0 Million Primes/s
  Sorting                          5611 Thousand Strings/s
  Encryption                       1972 MB/s
  Compression                      37732 KB/s
  CPU Single Threaded              4028 Million Operations/s
  Physics                          523 Frames/s
  Extended Instructions (SSE)      3282 Million Matrices/s

Memory Mark:                       1786
  Database Operations              1380 Thousand Operations/s
  Memory Read Cached               41032 MB/s
  Memory Read Uncached             39229 MB/s
  Memory Write                     21183 MB/s
  Available RAM                    1537 Megabytes
  Memory Latency                   64 Nanoseconds
  Memory Threaded                  39172 MB/s
--------------------------------------------------------------------------
```

### SpeedTest

```
Speedtest by Ookla

  Server: Vyve Broadband - Moses Lake, WA (id: 38364)
     ISP: 
Idle Latency: 16.04 ms (jitter: 0.15ms, low: 15.80ms, high: 16.20ms)
Download: 8954.76 Mbps (data used: 13.1 GB)
25.19 ms (jitter: 2.32ms, low: 15.48ms, high: 46.08ms)
Upload: 5020.55 Mbps (data used: 7.6 GB)
17.76 ms (jitter: 1.85ms, low: 15.45ms, high: 25.00ms)
Packet Loss: 0.0%
Result URL: https://www.speedtest.net/result/c/c4fbfc78-8692-4ccb-9b70-6720face5f97
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-90-1024x415.png)

### 2023.9.22

```
Basic System Information:
Uptime : 0 days, 0 hours, 1 minutes
Processor : AMD Ryzen 9 7950X 16-Core Processor
CPU cores : 1 @ 4499.996 MHz
AES-NI : Enabled
VM-x/AMD-V : Enabled
RAM : 1.9 GiB
Swap : 0.0 KiB
Disk : 49.9 GiB
Distro : Debian GNU/Linux 12 (bookworm)
Kernel : 6.1.0-9-amd64
VM Type : KVM
IPv4/IPv6 : Online / Online

IPv6 Network Information:
ISP : Layer
ASN : Unknown
Host : Layer
Location : Spokane, Washington (WA)
Country : United States

fio Disk Speed Tests (Mixed R/W 50/50):
Block Size	4k (IOPS)	64k (IOPS)
Read	462.13 MB/s (115.5k)	1.80 GB/s (28.1k)
Write	463.35 MB/s (115.8k)	1.81 GB/s (28.2k)
Total	925.48 MB/s (231.3k)	3.61 GB/s (56.4k)
Block Size	512k (IOPS)	1m (IOPS)
------	--- ----	---- ----
Read	2.78 GB/s (5.4k)	3.57 GB/s (3.4k)
Write	2.93 GB/s (5.7k)	3.81 GB/s (3.7k)
Total	5.71 GB/s (11.1k)	7.38 GB/s (7.2k)
Geekbench 6 Benchmark Test:
Test | Value
|
Single Core | 2886
Multi Core | 2904
Full Test | https://browser.geekbench.com/v6/cpu/2715734

YABS completed in 6 min 10 sec
```

### 国内延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-96-1024x452.png)

### 全球延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-95-1024x558.png)

### 2023年9.28日Yabs

```
Basic System Information:
---------------------------------
Uptime     : 1 days, 16 hours, 20 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 1 @ 4499.996 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 975.0 MiB
Disk       : 48.0 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-10-cloud-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Layer Marketing Services L.L.C
ASN        : AS216382 LAYER MARKETING SERVICES L.L.C
Host       : Layer
Location   : Spokane, Washington (WA)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 454.51 MB/s (113.6k) | 3.45 GB/s    (53.9k)
Write      | 455.71 MB/s (113.9k) | 3.46 GB/s    (54.2k)
Total      | 910.22 MB/s (227.5k) | 6.92 GB/s   (108.1k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.20 GB/s     (6.2k) | 3.73 GB/s     (3.6k)
Write      | 3.37 GB/s     (6.5k) | 3.98 GB/s     (3.8k)
Total      | 6.57 GB/s    (12.8k) | 7.72 GB/s     (7.5k)

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2794                          
Multi Core      | 2781                          
Full Test       | https://browser.geekbench.com/v6/cpu/2810263
```

### 2023年10.2日Yabs

```
Basic System Information:
---------------------------------
Uptime     : 5 days, 21 hours, 7 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 1 @ 4499.996 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 975.0 MiB
Disk       : 48.0 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-10-cloud-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Layer Marketing Services L.L.C
ASN        : AS216382 LAYER MARKETING SERVICES L.L.C
Host       : Layer
Location   : Spokane, Washington (WA)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 480.14 MB/s (120.0k) | 3.39 GB/s    (53.0k)
Write      | 481.41 MB/s (120.3k) | 3.41 GB/s    (53.3k)
Total      | 961.55 MB/s (240.3k) | 6.80 GB/s   (106.3k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.52 GB/s     (6.8k) | 3.90 GB/s     (3.8k)
Write      | 3.70 GB/s     (7.2k) | 4.16 GB/s     (4.0k)
Total      | 7.23 GB/s    (14.1k) | 8.06 GB/s     (7.8k)

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2780                          
Multi Core      | 2758                          
Full Test       | https://browser.geekbench.com/v6/cpu/2871629

YABS completed in 6 min 20 sec
```

### 2023年10月7日

```
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X 16-Core Processor
 CPU Cores          : 1 Core @ 4499.996 MHz
 CPU Cache          : 1024 KB
 AES-NI             : ✓ Enabled
 VM-x/AMD-V         : ✓ Enabled
 Total Disk         : 3.3 GB / 48.0 GB
 Total Mem          : 430.1 MB / 1.9 GB
 Total Swap         : 376.3 MB / 975.0 MB
 System uptime      : 10 days, 15 hour 17 min
 Load average       : 0.00, 0.01, 0.05
 OS                 : Debian GNU/Linux 12 x86_64 (64 Bit)
 Kernel             : 6.1.0-10-cloud-amd64
 TCP CC             : cubic
 Virtualization     : KVM
----------------------------------------------------------------------
 IP                 : *
 Organization       : AS216382 LAYER MARKETING SERVICES L.L.C
 Location           : Liberty Lake / US
 Region             : Washington
----------------------------------------------------------------------

 -> CPU Performance Test (Standard Mode, 3-Pass @ 30sec)

 1 Thread Test:                 6277 Scores

Geekbench 4 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 8889                          
Multi Core      | 8347                          
Full Test       | https://browser.geekbench.com/v4/cpu/16880424

Geekbench 5 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1986                          
Multi Core      | 2082                          
Full Test       | https://browser.geekbench.com/v5/cpu/21811249


 -> Memory Performance Test (Standard Mode, 3-Pass @ 30sec)

 1 Thread - Read Test :         74520.11 MB/s
 1 Thread - Write Test:         41534.28 MB/s

 -> Disk Speed Test (4K Block/1M Block, Direct-Write)

 Test Name              Write Speed                             Read Speed
 10MB-4K Block          30.4 MB/s (7414 IOPS, 0.35s)            64.4 MB/s (15730 IOPS, 0.16s)
 10MB-1M Block          2.1 GB/s (2014 IOPS, 0.00s)             1.9 GB/s (1803 IOPS, 0.01s)
 100MB-4K Block         47.5 MB/s (0.09 IOPS, 2.21s))           48.8 MB/s (11911 IOPS, 2.15s)
 100MB-1M Block         2.2 GB/s (2099 IOPS, 0.05s)             3.2 GB/s (3019 IOPS, 0.03s)
 1GB-4K Block           45.4 MB/s (0.09 IOPS, 23.10s))          56.5 MB/s (13784 IOPS, 18.57s)
 1GB-1M Block           1.9 GB/s (1852 IOPS, 0.54s)             3.0 GB/s (2860 IOPS, 0.35s)

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 454.01 MB/s (113.5k) | 3.40 GB/s    (53.1k)
Write      | 455.21 MB/s (113.8k) | 3.41 GB/s    (53.4k)
Total      | 909.23 MB/s (227.3k) | 6.82 GB/s   (106.5k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.68 GB/s     (7.1k) | 3.84 GB/s     (3.7k)
Write      | 3.87 GB/s     (7.5k) | 4.09 GB/s     (4.0k)
Total      | 7.55 GB/s    (14.7k) | 7.94 GB/s     (7.7k)

----------------------------------------------------------------------
**  TW, Hinet ( 168.95.1.1) **
 
traceroute to 168.95.1.1 (168.95.1.1), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  10.95 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.66 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  12.16 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  be3048.ccr21.sea02.atlas.cogentco.com (154.54.11.9)  11.96 ms  AS174  美国, 华盛顿州, 西雅图, cogentco.com
 5  be3717.ccr22.sfo01.atlas.cogentco.com (154.54.86.209)  30.54 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 6  be2430.ccr31.sjc04.atlas.cogentco.com (154.54.88.186)  33.24 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 7  38.32.64.42  30.75 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 8  pa-r31.us.hinet.net (202.39.84.29)  35.56 ms  AS9680  美国, 加利福尼亚州, 帕洛阿尔托, cht.com.tw
 9  r4001-s2.tp.hinet.net (202.39.91.78)  153.23 ms  AS9680  中国, 台湾, 台北市, cht.com.tw
10  61-221-53-30.hinet-ip.hinet.net (61.221.53.30)  177.35 ms  AS3462  中国, 台湾, 台北市, cht.com.tw
11  dns.hinet.net (168.95.1.1)  176.36 ms  AS3462  中国, 台湾, cht.com.tw

----------------------------------------------------------------------
**  TW, FETNet ( 139.175.1.254) **
 
traceroute to 139.175.1.254 (139.175.1.254), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  29.22 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.29 ms  *  局域网
 3  six.retn.net (206.81.80.150)  11.28 ms  *  美国, 华盛顿州, 西雅图, seattleix.net
 4  ae3-5.RT.CBQ.TPE.TW.retn.net (87.245.232.75)  135.24 ms  AS9002  中国, 台湾, 台北市, retn.net
 5  GW-Seednet.retn.net (87.245.251.195)  135.34 ms  AS9002  RETN.NET 骨干网, retn.net
 6  r58-4.seed.net.tw (139.175.58.4)  136.45 ms  AS4780  中国, 台湾, 台北市, fetnet.net
 7  r57-186.seed.net.tw (139.175.57.186)  134.10 ms  AS4780  中国, 台湾, 台北市, fetnet.net
 8  h98-192-72-49.seed.net.tw (192.72.49.98)  137.06 ms  AS4780  中国, 台湾, 台北市, fetnet.net
 9  ks1-254.dialup.seed.net.tw (139.175.1.254)  140.09 ms  AS4780  中国, 台湾, 台北市, fetnet.net

----------------------------------------------------------------------
**  TW, APTG ( 203.79.224.10) **
 
traceroute to 203.79.224.10 (203.79.224.10), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  11.36 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  2.24 ms  *  局域网
 3  seattleix.sg.gs (206.81.81.61)  63.22 ms  *  美国, 华盛顿州, 西雅图, seattleix.net
 4  124.6.32.74  179.20 ms  AS24482  中国, 香港, sg.gs
 5  *
 6  103.41.129.146  178.43 ms  AS133748  中国, 台湾, 台北市, coretelnet.com
 7  203-79-253-161.ebix.net.tw (203.79.253.161)  178.43 ms  AS17709  中国, 台湾, 台北市, aptg.com.tw
 8  IL203-79-251-46.static.apol.com.tw (203.79.251.46)  179.00 ms  AS17709  中国, 台湾, 台北市, aptg.com.tw
 9  192.168.125.1  178.82 ms  *  局域网
10  dns.octor.com (203.79.224.10)  178.81 ms  AS9311  中国, 台湾, 台北市, aptg.com.tw

----------------------------------------------------------------------
**  TW, SoNET ( 61.64.127.1) **
 
traceroute to 61.64.127.1 (61.64.127.1), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  7.31 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.29 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  11.29 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  sea-b1-link.ip.twelve99.net (213.248.70.12)  11.64 ms  AS1299  美国, 华盛顿州, 西雅图, telia.com
 5  sjo-b23-link.ip.twelve99.net (62.115.132.152)  31.25 ms  AS1299  美国, 加利福尼亚州, 圣何塞, telia.com
 6  lax-b23-link.ip.twelve99.net (62.115.116.41)  39.99 ms  AS1299  美国, 加利福尼亚州, 洛杉矶, telia.com
 7  chunghwa-ic-345200.ip.twelve99-cust.net (62.115.175.219)  41.16 ms  AS1299  美国, 加利福尼亚州, 洛杉矶, telia.com
 8  203-78-181-145.twgate-ip.twgate.net (203.78.181.145)  169.85 ms  AS9505  中国, 台湾, 台北市, twgate.net
 9  203-78-181-214.twgate-ip.twgate.net (203.78.181.214)  169.72 ms  AS9505  中国, 台湾, 台北市, twgate.net
10  175-41-63-86.twgate-ip.twgate.net (175.41.63.86)  169.72 ms  AS9505  中国, 台湾, 台北市, twgate.net
11  219.84.176.122  169.75 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw
12  219.84.176.142  198.92 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw
13  gw.so-net.net.tw (61.64.127.249)  169.74 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw
14  gw.so-net.net.tw (61.64.127.249)  170.42 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw
15  gw.so-net.net.tw (61.64.127.249)  169.80 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw
16  ns1.so-net.net.tw (61.64.127.1)  169.89 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw

----------------------------------------------------------------------
**  TW, TFN ( 219.87.66.1) **
 
traceroute to 219.87.66.1 (219.87.66.1), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  66.96 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.38 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  11.27 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r24.sttlwa01.us.bb.gin.ntt.net (129.250.2.72)  12.19 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  ae-9.r32.tokyjp05.jp.bb.gin.ntt.net (129.250.4.143)  111.03 ms  AS2914  日本, 东京都, 东京, ntt.com
 6  ae-1.r33.tokyjp05.jp.bb.gin.ntt.net (129.250.5.54)  107.76 ms  AS2914  日本, 东京都, 东京, ntt.com
 7  ae-2.r22.taiptw01.tw.bb.gin.ntt.net (129.250.7.6)  135.90 ms  AS2914  中国, 台湾, 台北市, ntt.com
 8  ae-6.r02.taiptw01.tw.bb.gin.ntt.net (129.250.7.41)  134.42 ms  AS2914  中国, 台湾, 台北市, ntt.com
 9  61.58.33.174  137.15 ms  AS2914  中国, 台湾, 台北市, ntt.com
10  60-199-14-246.static.tfn.net.tw (60.199.14.246)  135.78 ms  AS9924  中国, 台湾, 台北市, twmbroadband.com
11  219-87-66-1.static.tfn.net.tw (219.87.66.1)  137.10 ms  AS9924  中国, 台湾, 台北市, twmbroadband.com

----------------------------------------------------------------------
**  TW,TAIFO ( 103.31.196.1) **
 
traceroute to 103.31.196.1 (103.31.196.1), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  41.72 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.32 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  14.74 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  be3048.ccr21.sea02.atlas.cogentco.com (154.54.11.9)  12.76 ms  AS174  美国, 华盛顿州, 西雅图, cogentco.com
 5  be3717.ccr22.sfo01.atlas.cogentco.com (154.54.86.209)  30.12 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 6  be2430.ccr31.sjc04.atlas.cogentco.com (154.54.88.186)  33.36 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 7  38.32.64.42  62.41 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 8  pa-r31.us.hinet.net (202.39.84.29)  30.73 ms  AS9680  美国, 加利福尼亚州, 帕洛阿尔托, cht.com.tw
 9  r4001-s2.tp.hinet.net (211.72.108.22)  159.70 ms  AS3462  中国, 台湾, 台北市, cht.com.tw
10  r4101-s2.tp.hinet.net (220.128.11.130)  159.76 ms  *  中国, 台湾, 台北市, cht.com.tw
11  tpdb-3031.hinet.net (220.128.7.114)  183.23 ms  *  中国, 台湾, 台北市, cht.com.tw
12  hc-c12r1.router.hinet.net (220.128.1.129)  182.78 ms  *  中国, 台湾, 台北市, cht.com.tw
13  210-242-214-5.hinet-ip.hinet.net (210.242.214.5)  185.87 ms  AS3462  中国, 台湾, 台北市, cht.com.tw
14  *
15  103.31.197.66  186.55 ms  AS131584  中国, 台湾, 台北市, taifo.com.tw
16  103.31.196.1  187.12 ms  AS131584  中国, 台湾, 台北市, taifo.com.tw

----------------------------------------------------------------------
**  TW,Kbro ( 123.195.236.110) **
 
traceroute to 123.195.236.110 (123.195.236.110), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  12.05 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  3.69 ms  *  局域网
 3  six.retn.net (206.81.80.150)  11.20 ms  *  美国, 华盛顿州, 西雅图, seattleix.net
 4  ae5-10.RT.CLY.TPE.TW.retn.net (87.245.232.236)  133.54 ms  AS9002  中国, 台湾, 台北市, retn.net
 5  GW-TFN.retn.net (87.245.238.145)  133.58 ms  AS9002  中国, 台湾, 台北市, retn.net
 6  60-199-17-41.static.tfn.net.tw (60.199.17.41)  134.11 ms  AS9924  中国, 台湾, 台北市, twmbroadband.com
 7  60-199-47-106.static.tfn.net.tw (60.199.47.106)  140.17 ms  AS9924  中国, 台湾, 台北市, twmbroadband.com
 8  219-80-240-90.static.tfn.net.tw (219.80.240.90)  136.18 ms  AS9924  中国, 台湾, 桃园市, twmbroadband.com
 9  *
10  *
11  123-195-236-110.dynamic.kbronet.com.tw (123.195.236.110)  135.71 ms  AS38841  中国, 台湾, 台北市, kbro.com.tw

----------------------------------------------------------------------
**  北京电信 ( 219.141.147.210) **
 
traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  5.06 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.33 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  18.28 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r25.sttlwa01.us.bb.gin.ntt.net (129.250.2.94)  13.40 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  ae-3.r25.snjsca04.us.bb.gin.ntt.net (129.250.3.124)  29.41 ms  AS2914  美国, 加利福尼亚州, 圣何塞, ntt.com
 6  ae-1.a03.snjsca04.us.bb.gin.ntt.net (129.250.2.191)  30.27 ms  AS2914  美国, 加利福尼亚州, 圣何塞, ntt.com
 7  218.30.53.50  36.02 ms  AS4134  美国, 加利福尼亚州, 圣何塞, chinatelecom.com.cn, 电信
 8  *
 9  *
10  *
11  *
12  *
13  6.254.120.106.static.bjtelecom.net (106.120.254.6)  200.90 ms  AS4847  中国, 北京, chinatelecom.com.cn, 电信
14  bj141-147-210.bjtelecom.net (219.141.147.210)  201.34 ms  AS4847  中国, 北京, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
**  上海电信 ( 202.96.209.133) **
 
traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  40.26 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.39 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  11.44 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r25.sttlwa01.us.bb.gin.ntt.net (129.250.2.94)  11.87 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  ae-3.r25.snjsca04.us.bb.gin.ntt.net (129.250.3.124)  36.87 ms  AS2914  美国, 加利福尼亚州, 圣何塞, ntt.com
 6  ae-1.a03.snjsca04.us.bb.gin.ntt.net (129.250.2.191)  28.51 ms  AS2914  美国, 加利福尼亚州, 圣何塞, ntt.com
 7  218.30.53.50  35.99 ms  AS4134  美国, 加利福尼亚州, 圣何塞, chinatelecom.com.cn, 电信
 8  *
 9  202.97.50.194  235.73 ms  AS4134  中国, 上海, chinatelecom.com.cn, 电信
10  202.97.24.157  215.87 ms  AS4134  中国, 上海, chinatelecom.com.cn, 电信
11  *
12  101.95.89.162  221.42 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信
13  61.172.64.54  216.77 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信
14  ns-pd.online.sh.cn (202.96.209.133)  214.15 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
**  深圳电信 ( 58.60.188.222) **
 
traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  9.40 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.31 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  11.37 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r25.sttlwa01.us.bb.gin.ntt.net (129.250.2.94)  11.53 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  ae-3.r25.snjsca04.us.bb.gin.ntt.net (129.250.3.124)  29.15 ms  AS2914  美国, 加利福尼亚州, 圣何塞, ntt.com
 6  ae-1.a03.snjsca04.us.bb.gin.ntt.net (129.250.2.191)  28.56 ms  AS2914  美国, 加利福尼亚州, 圣何塞, ntt.com
 7  218.30.53.50  30.30 ms  AS4134  美国, 加利福尼亚州, 圣何塞, chinatelecom.com.cn, 电信
 8  202.97.63.29  188.08 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
 9  202.97.65.94  186.80 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
10  202.97.93.82  191.16 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
11  14.147.127.74  211.24 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
12  *
13  58.60.188.222  194.10 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
**  北京联通 ( 202.106.50.1) **
 
traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  142.56 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.24 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  11.32 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r24.sttlwa01.us.bb.gin.ntt.net (129.250.2.72)  11.79 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  ae-0.a03.sttlwa01.us.bb.gin.ntt.net (129.250.2.99)  11.42 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 6  *
 7  0.ae3.GW7.LAX1.ALTER.NET (140.222.3.47)  38.07 ms  *  美国, 加利福尼亚州, 洛杉矶, verizon.com
 8  157.130.247.190  286.21 ms  AS701  美国, 加利福尼亚州, 洛杉矶, verizon.com
 9  219.158.16.93  367.37 ms  AS4837  中国, 北京, chinaunicom.com, 联通
10  219.158.9.226  363.63 ms  AS4837  中国, 北京, chinaunicom.com, 联通
11  *
12  *
13  202.106.50.1  313.25 ms  AS4808  中国, 北京, chinaunicom.com, 联通

----------------------------------------------------------------------
**  上海联通 ( 210.22.97.1) **
 
traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  196.31 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.26 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  12.12 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r24.sttlwa01.us.bb.gin.ntt.net (129.250.2.72)  11.72 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  ae-0.a03.sttlwa01.us.bb.gin.ntt.net (129.250.2.99)  11.95 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 6  ae-0.lumen.sttlwa01.us.bb.gin.ntt.net (129.250.9.181)  11.53 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 7  4.69.209.169  28.85 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
 8  CHINA-UNICO.edge1.SanJose3.Level3.net (4.53.209.22)  45.03 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
 9  219.158.97.177  233.18 ms  AS4837  中国, 上海, chinaunicom.com, 联通
10  *
11  *
12  139.226.231.110  230.79 ms  AS17621  中国, 上海, chinaunicom.com, 联通
13  *
14  210.22.97.1  238.98 ms  AS17621  中国, 上海, chinaunicom.com, 联通

----------------------------------------------------------------------
**  深圳联通 ( 210.21.196.6) **
 
traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  53.38 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.24 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  16.34 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r24.sttlwa01.us.bb.gin.ntt.net (129.250.2.72)  15.63 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  ae-0.a03.sttlwa01.us.bb.gin.ntt.net (129.250.2.99)  14.20 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 6  0.peer-AS2914-1.PPR02.STTLWAWB.ALTER.NET (157.130.190.53)  11.32 ms  AS701  美国, 华盛顿州, 西雅图, verizon.com
 7  0.ae6.GW2.LAX1.ALTER.NET (140.222.223.17)  36.79 ms  *  美国, 加利福尼亚州, 洛杉矶, verizon.com
 8  157.130.230.58  333.82 ms  AS701  美国, 加利福尼亚州, 洛杉矶, verizon.com
 9  219.158.96.233  293.15 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
10  219.158.4.101  290.47 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
11  219.158.3.97  288.42 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
12  *
13  120.80.144.38  320.42 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
14  *
15  *
16  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  317.58 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通

----------------------------------------------------------------------
**  北京移动 ( 221.179.155.161) **
 
traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  14.35 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.25 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  11.32 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r24.sttlwa01.us.bb.gin.ntt.net (129.250.2.72)  11.33 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  ae-9.r32.tokyjp05.jp.bb.gin.ntt.net (129.250.4.143)  113.37 ms  AS2914  日本, 东京都, 东京, ntt.com
 6  ae-2.r26.tkokhk01.hk.bb.gin.ntt.net (129.250.2.51)  158.50 ms  AS2914  中国, 香港, ntt.com
 7  ae-0.a02.tkokhk01.hk.bb.gin.ntt.net (129.250.5.33)  159.51 ms  AS2914  中国, 香港, ntt.com
 8  *
 9  223.120.2.53  176.39 ms  AS58453  中国, 香港, chinamobile.com, 移动
10  *
11  223.120.22.142  234.22 ms  AS58453  中国, 北京, chinamobile.com, 移动
12  221.183.55.110  233.22 ms  AS9808  中国, 北京, chinamobile.com, 移动
13  221.183.25.201  233.05 ms  AS9808  中国, 北京, chinamobile.com, 移动
14  221.183.89.122  235.12 ms  AS9808  中国, 北京, chinamobile.com, 移动
15  221.183.46.178  207.84 ms  AS9808  中国, 北京, chinamobile.com, 移动
16  221.183.130.142  236.80 ms  AS9808  中国, 北京, chinamobile.com, 移动
17  cachedns03.bj.chinamobile.com (221.179.155.161)  236.28 ms  AS56048  中国, 北京, chinamobile.com, 移动

----------------------------------------------------------------------
**  上海移动 ( 211.136.112.200) **
 
traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  187.95 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.38 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  19.22 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r24.sttlwa01.us.bb.gin.ntt.net (129.250.2.72)  11.63 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  *
 6  *
 7  ae-1.r02.tkokhk01.hk.bb.gin.ntt.net (129.250.6.92)  155.23 ms  AS2914  中国, 香港, ntt.com
 8  ce-0-4-0-0.r02.tkokhk01.hk.ce.gin.ntt.net (203.131.241.82)  175.94 ms  AS2914  中国, 香港, ntt.com
 9  *
10  223.120.22.114  268.65 ms  AS58453  中国, 上海, chinamobile.com, 移动
11  221.183.89.178  199.86 ms  AS9808  中国, 上海, chinamobile.com, 移动
12  221.183.89.33  272.23 ms  AS9808  中国, 上海, chinamobile.com, 移动
13  221.183.89.10  271.43 ms  AS9808  中国, 上海, chinamobile.com, 移动
14  221.183.39.130  200.92 ms  AS9808  中国, 上海, chinamobile.com, 移动
15  221.181.125.138  273.46 ms  AS24400  中国, 上海, chinamobile.com, 移动
16  211.136.112.252  274.07 ms  AS24400  中国, 上海, chinamobile.com, 移动
17  211.136.112.200  276.58 ms  AS24400  中国, 上海, chinamobile.com, 移动

----------------------------------------------------------------------
**  深圳移动 ( 120.196.165.24) **
 
traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  56.50 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  0.29 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  12.64 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r24.sttlwa01.us.bb.gin.ntt.net (129.250.2.72)  11.90 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  ae-9.r32.tokyjp05.jp.bb.gin.ntt.net (129.250.4.143)  111.81 ms  AS2914  日本, 东京都, 东京, ntt.com
 6  *
 7  ae-1.r02.tkokhk01.hk.bb.gin.ntt.net (129.250.6.92)  153.21 ms  AS2914  中国, 香港, ntt.com
 8  ce-0-4-0-0.r02.tkokhk01.hk.ce.gin.ntt.net (203.131.241.82)  173.86 ms  AS2914  中国, 香港, ntt.com
 9  *
10  223.120.2.82  247.11 ms  AS58453  中国, 广东, 广州, chinamobile.com, 移动
11  221.183.55.82  248.47 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
12  221.183.92.21  177.67 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
13  *
14  221.183.71.78  175.66 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
15  221.183.110.166  180.76 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
16  ns6.gd.cnmobile.net (120.196.165.24)  251.16 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动

----------------------------------------------------------------------
**  成都教育网 ( 202.112.14.151) **
 
traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  1.138.119.199.hostedby.layer.ae (199.119.138.1)  4.83 ms  AS216382  美国, 华盛顿州, 利伯蒂湖, aia.us.com
 2  10.100.1.66  2.25 ms  *  局域网
 3  ce-3-0-1.a02.sttlwa01.us.bb.gin.ntt.net (157.238.227.230)  12.43 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 4  ae-2.r24.sttlwa01.us.bb.gin.ntt.net (129.250.2.72)  11.88 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
 5  *
 6  *
 7  ae-1.r02.tkokhk01.hk.bb.gin.ntt.net (129.250.6.92)  150.37 ms  AS2914  中国, 香港, ntt.com
 8  *
 9  223.120.2.117  172.03 ms  AS58453  中国, 香港, chinamobile.com, 移动
10  223.120.3.86  168.64 ms  AS58453  中国, 香港, chinamobile.com, 移动
11  223.119.81.94  152.25 ms  AS58453  中国, 香港, chinamobile.com, 移动
12  101.4.114.221  181.62 ms  AS4538  中国, 北京, edu.cn, 教育网
13  101.4.115.181  180.26 ms  AS4538  中国, 北京, edu.cn, 教育网
14  *
15  *
16  101.4.116.106  198.93 ms  AS4538  中国, 湖北, 武汉, edu.cn, 教育网
17  *
18  *
19  101.4.116.158  223.58 ms  AS4538  中国, 四川, 成都, edu.cn, 教育网
20  *
21  *
22  *
23  *
24  *
25  *
26  202.112.14.151  220.71 ms  AS24355  中国, 四川, 成都, 电子科技大学CERNET西南地区网络中心, edu.cn, 教育网

----------------------------------------------------------------------
 Node Name                  Upload Speed      Download Speed    Latency     Result      
 Speedtest.net              8717.35 Mbps      9202.17 Mbps      0.19 ms     https://www.speedtest.net/result/c/30921539-cdb9-425b-894e-2b6c1e20bc07
 TW, Chunghwa Mobile        466.79 Mbps       4353.99 Mbps      181.00 ms   https://www.speedtest.net/result/c/35bcb6ba-27a2-4f3f-8138-ffd07ea7c2ad
 TW, TAIFO                  19.05 Mbps        2854.11 Mbps      183.02 ms   https://www.speedtest.net/result/c/645
```
