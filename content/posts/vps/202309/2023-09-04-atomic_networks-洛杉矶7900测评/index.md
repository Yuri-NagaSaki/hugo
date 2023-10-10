---
title: "Atomic_Networks 洛杉矶7900测评"
date: "2023-09-04"
categories: 
  - "vps"
  - "usa"
---

看上去是ReliableSite的下游，网络挺烂的，避坑

> ## 套餐
> 
> 1vCPU (Fair Share)  
> 1GB DDR5 RAM  
> 15GB NVMe Disk (Comment Your Invoice ID For Double Disk Space)  
> 1Gbit Unmetered  
> Los Angeles, USA

## 测评

### yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 4 minutes
Processor  : AMD Ryzen 9 7900 12-Core Processor
CPU cores  : 1 @ 3692.960 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 943.0 MiB
Swap       : 0.0 KiB
Disk       : 14.7 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-10-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : ReliableSite.Net LLC
ASN        : AS23470 ReliableSite.Net LLC
Host       : Atomic Networks LLC
Location   : Los Angeles, California (CA)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 295.06 MB/s  (73.7k) | 2.95 GB/s    (46.0k)
Write      | 295.84 MB/s  (73.9k) | 2.96 GB/s    (46.3k)
Total      | 590.91 MB/s (147.7k) | 5.91 GB/s    (92.4k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.57 GB/s     (6.9k) | 3.35 GB/s     (3.2k)
Write      | 3.76 GB/s     (7.3k) | 3.57 GB/s     (3.4k)
Total      | 7.34 GB/s    (14.3k) | 6.93 GB/s     (6.7k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 30.0 Mbits/sec  | 34.9 Mbits/sec  | 129 ms         
Scaleway        | Paris, FR (10G)           | 362 Mbits/sec   | 176 Mbits/sec   | 132 ms         
NovoServe       | North Holland, NL (40G)   | busy            | 780 Mbits/sec   | 136 ms         
Uztelecom       | Tashkent, UZ (10G)        | 351 Mbits/sec   | 94.0 Mbits/sec  | 220 ms         
Clouvider       | NYC, NY, US (10G)         | 70.0 Mbits/sec  | 79.3 Mbits/sec  | 63.1 ms        
Clouvider       | Dallas, TX, US (10G)      | 126 Mbits/sec   | 171 Mbits/sec   | 29.5 ms        
Clouvider       | Los Angeles, CA, US (10G) | 535 Mbits/sec   | 2.32 Gbits/sec  | 2.08 ms        
Biznet          | Jakarta, ID (10G)         | busy            | 36.3 Mbits/sec  | -- 

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | busy            | 37.4 Mbits/sec  | 129 ms         
Scaleway        | Paris, FR (10G)           | busy            | busy            | 136 ms         
NovoServe       | North Holland, NL (40G)   | 414 Mbits/sec   | busy            | 133 ms         
Uztelecom       | Tashkent, UZ (10G)        | 382 Mbits/sec   | 89.1 Mbits/sec  | 221 ms         
Clouvider       | NYC, NY, US (10G)         | 63.3 Mbits/sec  | 80.9 Mbits/sec  | 62.6 ms        
Clouvider       | Dallas, TX, US (10G)      | 115 Mbits/sec   | 184 Mbits/sec   | 29.6 ms        
Clouvider       | Los Angeles, CA, US (10G) | 593 Mbits/sec   | 2.28 Gbits/sec  | 0.379 ms       
Biznet          | Jakarta, ID (10G)         | busy            | busy            | -- 
```

### Geekbench6

![](https://cdn.lirica.cn/wordpress/2023/09/image-17-1024x302.png)

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 7900 12-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 3693.008 MHz
 CPU 缓存          : L1: 64.00 KB / L2: 1.00 MB / L3: 64.00 MB
 硬盘空间          : 8.68 GiB / 14.73 GiB
 启动盘路径        : /dev/sda1
 内存              : 129.72 MiB / 928.74 MiB
 Swap              : 15.95 MiB / 4.00 GiB
 系统在线时间      : 0 days, 0 hour 10 min
 负载              : 0.21, 0.44, 0.25
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-25-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS23470 ReliableSite.Net LLC
 IPV4 位置         : Los Angeles / California / US
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           6350 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          73896.26 MB/s
 单线程写测试:          35890.42 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         87.3 MB/s (21.32 IOPS, 1.20s))          115 MB/s (28027 IOPS, 0.91s)
 1GB-1M Block           1.5 GB/s (1471 IOPS, 0.68s)             3.5 GB/s (3329 IOPS, 0.30s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 316.89 MB/s  (79.2k) | 3.35 GB/s    (52.4k)
Write      | 317.73 MB/s  (79.4k) | 3.37 GB/s    (52.7k)
Total      | 634.63 MB/s (158.6k) | 6.73 GB/s   (105.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.87 GB/s     (9.5k) | 5.07 GB/s     (4.9k)
Write      | 5.13 GB/s    (10.0k) | 5.41 GB/s     (5.2k)
Total      | 10.01 GB/s   (19.5k) | 10.48 GB/s   (10.2k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX17S56)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX31S13)
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
 Dazn:                                  Yes (Region: US)
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       No  (Region: CN) 
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Los Angeles, CA 
 Netflix Preferred CDN:                 Los Angeles, CA  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: NL)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Los Angeles, CA 
 Netflix Preferred CDN:                 Los Angeles, CA  
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
  公司类型(company_type):hosting①  isp⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes② ⑥   No⑨ 
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
端口25检测:
  本地: No
  163邮箱：No
------以下为IPV6检测------
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: US 城市: Los Angeles 服务商: AS23470 ReliableSite.Net LLC
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
2023/09/04 22:23:22 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.32 ms         AS23470 美国 加利福尼亚州 洛杉矶 reliablesite.net
0.97 ms         AS3257 [GTT-GTT] 美国 加利福尼亚州 洛杉矶 gtt.net
15.87 ms        AS3257 [GTT-BACKBONE] 美国 加利福尼亚州 圣何塞 gtt.net
9.64 ms         AS4134 [CHINANET-US] 美国 加利福尼亚州 洛杉矶 CT-GTT-SJC-PoP chinatelecom.com.cn 电信
148.19 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 I-C chinatelecom.com.cn 电信
165.32 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
162.53 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
160.09 ms       AS4134 [APNIC-AP] 中国 广东省 深圳市 chinatelecom.com.cn 电信
184.46 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.22 ms         AS23470 美国 加利福尼亚州 洛杉矶 reliablesite.net
4.74 ms         AS3257 [GTT-GTT] 美国 加利福尼亚州 洛杉矶 gtt.net
7.97 ms         AS3257 [GTT-BACKBONE] 美国 加利福尼亚州 圣何塞 gtt.net
376.73 ms       AS3257 [TINET-TINET] 美国 加利福尼亚州 圣何塞 gtt.net
292.81 ms       AS4837 [CU169-BACKBONE] 中国 上海市 回国到达层 chinaunicom.cn 联通
234.48 ms       AS4837 [CU169-BACKBONE] 中国 上海市 chinaunicom.cn 联通
353.74 ms       AS17816 [UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
296.93 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
289.06 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.34 ms         AS23470 美国 加利福尼亚州 洛杉矶 reliablesite.net
0.90 ms         AS7922 美国 加利福尼亚州 洛杉矶 comcast.com
0.78 ms         AS7922 [CABLE-1] 美国 加利福尼亚州 洛杉矶 comcast.com
1.01 ms         AS701 [UUNETCUSTB40] 美国 加利福尼亚州 洛杉矶 verizon.com
1.13 ms         AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
0.85 ms         AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
148.71 ms       AS58453 [CMI-INT] 中国 广东省 广州市 cmi.chinamobile.com 移动
193.89 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
186.53 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
280.81 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
181.95 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
194.75 ms       AS9808 [CMNET] 中国 海南省 海口市 chinamobile.com 移动
182.40 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    112.03 Mbps     1169.61 Mbps    54.48    0.7%
洛杉矶           303.38 Mbps     1780.48 Mbps    0.60     0.0%
日本东京         7.33 Mbps       1186.91 Mbps    99.34    NULL
联通WuXi         17.13 Mbps      10.96 Mbps      185.34   6.4%
联通沈阳         0.75 Mbps       11.07 Mbps      195.09   19.1%
电信Suzhou5G     158.50 Mbps     372.05 Mbps     186.20   NULL
电信天津5G       2.39 Mbps       19.44 Mbps      183.11   11.0%
移动Chengdu      313.15 Mbps     667.87 Mbps     202.62   0.0%
------------------------------------------------------------------------
 总共花费      : 5 分 36 秒
 时间          : Mon Sep  4 22:27:54 CST 2023
------------------------------------------------------------------------
```

### speedtest

```
root@catcat:~/Geekbench-6.0.1-Linux# speedtest

   Speedtest by Ookla

      Server: All Points Broadband - Ashburn, VA (id: 41287)
         ISP: ReliableSite.Net LLC
Idle Latency:    54.27 ms   (jitter: 0.07ms, low: 54.21ms, high: 54.32ms)
    Download:  1220.60 Mbps (data used: 1.8 GB)                                                   
                 82.91 ms   (jitter: 9.50ms, low: 54.57ms, high: 172.47ms)
      Upload:   142.28 Mbps (data used: 258.2 MB)                                                   
                 81.01 ms   (jitter: 8.14ms, low: 54.41ms, high: 108.27ms)
 Packet Loss:     0.0%
  Result URL: https://www.speedtest.net/result/c/ab9ccdb7-efef-4543-b689-34c4031cd9c9
```

![](https://cdn.lirica.cn/wordpress/2023/09/image-18-1024x410.png)

### Bench

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7900 12-Core Processor
 CPU Cores          : 1 @ 3693.008 MHz
 CPU Cache          : 1024 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 14.7 GB (8.7 GB Used)
 Total Mem          : 928.7 MB (105.2 MB Used)
 Total Swap         : 4.0 GB (15.7 MB Used)
 System uptime      : 0 days, 0 hour 19 min
 Load average       : 0.06, 0.14, 0.18
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-25-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS23470 ReliableSite.Net LLC
 Location           : Los Angeles / US
 Region             : California
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.1 GB/s
 I/O Speed(2nd run) : 1.1 GB/s
 I/O Speed(3rd run) : 1.1 GB/s
 I/O Speed(average) : 1126.4 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    124.75 Mbps       1082.86 Mbps        54.35 ms    
 Los Angeles, US  311.76 Mbps       1909.84 Mbps        0.89 ms     
 Dallas, US       84.76 Mbps        1056.59 Mbps        28.90 ms    
 Montreal, CA     81.04 Mbps        919.09 Mbps         71.24 ms    
 Paris, FR        228.88 Mbps       862.59 Mbps         134.29 ms   
 Amsterdam, NL    295.79 Mbps       588.42 Mbps         154.84 ms   
 Nanjing, CN      221.93 Mbps       563.04 Mbps         164.01 ms   
 Singapore, SG    298.72 Mbps       383.66 Mbps         173.33 ms   
 Tokyo, JP        243.48 Mbps       415.04 Mbps         107.42 ms   
----------------------------------------------------------------------
```

### 流媒体解锁

```
============[ Multination ]============
 Dazn:                                  Yes (Region: US)
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       No  (Region: CN) 
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Los Angeles, CA 
 Netflix Preferred CDN:                 Los Angeles, CA  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
===========[ North America ]===========
 FOX:                                   Yes
 Hulu:                                  Failed
 NFL+:                                  Yes
 ESPN+:[Sponsored by Jam]               No
 Epix:                                  No
 Starz:                                 No
 Philo:                                 Yes
 FXNOW:                                 Yes
 TLC GO:                                Yes
 HBO Max:                               Yes
 Shudder:                               Yes
 BritBox:                               Yes
 Crackle:                               Yes
 CW TV:                                 Yes
 A&E TV:                                Yes
 NBA TV:                                Yes
 NBC TV:                                Yes
 Fubo TV:                               No
 Tubi TV:                               Yes
 Sling TV:                              Yes
 Pluto TV:                              Yes
 Acorn TV:                              Yes
 SHOWTIME:                              Yes
 encoreTVB:                             Yes
 Funimation:                            Yes (Region: US)
 Discovery+:                            Yes
 Paramount+:                            Yes
 Peacock TV:                            Yes
 Popcornflix:                           Yes
 Crunchyroll:                           Yes
 Directv Stream:                        No
 KBS American:                          Yes
 KOCOWA:                                Yes
 Maths Spot:                            Failed
 ---CA---
 CBC Gem:                               No
 Crave:                                 Yes
=======================================


 ** 正在测试IPv6解锁情况 
--------------------------------
 ** 您的网络为: ReliableSite.Net LLC (2602:fc2f:f01:*:*) 


============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: NL)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Los Angeles, CA 
 Netflix Preferred CDN:                 Los Angeles, CA  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
===========[ North America ]===========
 FOX:                                   Yes
 Hulu:                                  Failed
 NFL+:                                  IPv6 Not Support
 ESPN+:[Sponsored by Jam]               No
 Epix:                                  Failed (Network Connection)
 Epix:                                  Failed
 Starz:                                 Failed (Network Connection)
 Philo:                                 IPv6 Not Support
 FXNOW:                                 IPv6 Not Support
 TLC GO:                                IPv6 Not Support
 HBO Max:                               Failed (Network Connection)
 Shudder:                               Yes
 BritBox:                               Yes
 Crackle:                               Yes
 CW TV:                                 Yes
 A&E TV:                                IPv6 Not Support
 NBA TV:                                Yes
 NBC TV:                                Yes
 Fubo TV:                               IPv6 Not Support
 Tubi TV:                               Yes
 Sling TV:                              Yes
 Pluto TV:                              Yes
 Acorn TV:                              Failed (Network Connection)
 SHOWTIME:                              Failed (Network Connection)
 encoreTVB:                             Failed (Network Connection)
 Funimation:                            IPv6 Not Support
 Discovery+:                            IPv6 Not Support
 Paramount+:                            Yes
 Peacock TV:                            Yes
 Popcornflix:                           IPv6 Not Support
 Crunchyroll:                           IPv6 Not Support
 Directv Stream:                        No
 KBS American:                          IPv6 Not Support
 KOCOWA:                                IPv6 Not Support
 Maths Spot:                            IPv6 Not Support
 ---CA---
 CBC Gem:                               Failed (Network Connection)
 Crave:                                 Failed (Network Connection)
=======================================
```

### 全球延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-19-1024x531.png)
