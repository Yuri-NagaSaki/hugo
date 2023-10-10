---
title: "advinservers东京测评"
date: "2023-04-09"
categories: 
  - "vps"
  - "jp"
tags: 
  - "东京"
---

- 性价比不错，延迟优秀

- 日本地区 DDoS 清洗采用 TeraSwitch In House Mitigation

**官方网站：[点我](https://clients.advinservers.com/aff.php?aff=190)**

**日本vps：**[**点**](https://clients.advinservers.com/aff.php?aff=190&gid=26)[**我**](https://clients.advinservers.com/aff.php?aff=336&gid=26)

**Looking Glass：**

> **Tokyo, JP:** 194.87.169.7  
> **Amsterdam, NL:** 45.61.161.93 (LG: [http://45.61.161.93/](http://45.61.161.93/))  
> **Coventry, UK:** 78.157.214.36 (LG: [http://78.157.214.36](http://78.157.214.36/))  
> **Dallas, TX:** 172.99.233.46 (LG: [http://172.99.233.46](http://172.99.233.46/))  
> **Los Angeles, CA:** 45.8.22.11 (LG: [http://45.8.22.11](http://45.8.22.11/))  
> **Miami, FL:** 23.137.104.80 (LG: [http://23.137.104.80](http://23.137.104.80/))  
> **New York, NY:** 45.61.162.146 (LG: [http://45.61.162.146](http://45.61.162.146/))

## 规格

![](https://catcat.blog/wp-content/uploads/2023/04/image-18.png)

![](https://catcat.blog/wp-content/uploads/2023/04/image-19.png)

## YABS

```
 CPU Model          : Intel(R) Xeon(R) E-2388G CPU @ 3.20GHz
 CPU Cores          : 4 Core @ 3192.000 MHz
 CPU Cache          : 16384 KB
 AES-NI             : ✓ Enabled
 VM-x/AMD-V         : ✓ Enabled
 Total Disk         : 1.9 GB / 107.5 GB
 Total Mem          : 187.7 MB / 31.4 GB
 System uptime      : 0 days, 0 hour 35 min
 Load average       : 0.53, 0.19, 0.06
 OS                 : Ubuntu 20.04.5 LTS x86_64 (64 Bit)
 Kernel             : 5.4.0-135-generic
 TCP CC             : cubic
 Virtualization     : KVM
```

## CPU 测试

![](https://catcat.blog/wp-content/uploads/2023/04/image-20.png)

```
 -> CPU Performance Test (Standard Mode, 3-Pass @ 30sec)

 1 Thread Test:                 2843 Scores
 4 Threads Test:                9961 Scores
```

## 内存测试

```
 -> Memory Performance Test (Standard Mode, 3-Pass @ 30sec)

 1 Thread - Read Test :         26247.68 MB/s
 1 Thread - Write Test:         13654.43 MB/s
```

## 硬盘测试

```
fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
------ | --- ---- | ---- ----
Read       | 38.67 MB/s    (9.6k) | 535.49 MB/s   (8.3k)
Write      | 38.76 MB/s    (9.6k) | 538.31 MB/s   (8.4k)
Total      | 77.43 MB/s   (19.3k) | 1.07 GB/s    (16.7k)
|                      |
Block Size | 512k          (IOPS) | 1m            (IOPS)
------ | --- ---- | ---- ----
Read       | 1.15 GB/s     (2.2k) | 1.15 GB/s     (1.1k)
Write      | 1.21 GB/s     (2.3k) | 1.22 GB/s     (1.1k)
Total      | 2.36 GB/s     (4.6k) | 2.37 GB/s     (2.3k)
```

## 全球延迟

![](https://catcat.blog/wp-content/uploads/2023/04/image-21.png)

## Speedtest测试

```
 Node Name                Upload Speed      Download Speed    Latency     Result
Speedtest.net            8204.84 Mbps      5134.43 Mbps      0.70 ms     https://www.speedtest.net/result/c/d114a012-a167-4ac4-8ab0-27d82eb47065
TW, Chunghwa Mobile      852.71 Mbps       1054.80 Mbps      99.49 ms    https://www.speedtest.net/result/c/69fb2feb-ad85-4b71-a775-336996f4df92
TW, Chief Telecom        876.98 Mbps       5225.54 Mbps      69.88 ms    https://www.speedtest.net/result/c/b057bcdb-afb0-446f-9a66-74845fb33d1f
TW, TAIFO                475.23 Mbps       390.29 Mbps       32.79 ms    https://www.speedtest.net/result/c/31960c9e-c3e4-4c72-870c-22e95f27b661
TW, DFT                  1076.98 Mbps      4377.19 Mbps      47.96 ms    https://www.speedtest.net/result/c/9329dbcd-f8fc-4f88-95e9-8fba557de93f
TW, FET                  1470.53 Mbps      5003.27 Mbps      33.07 ms    https://www.speedtest.net/result/c/37fbd541-e5df-4c6d-952b-d8ac5ce15025
CN, hanghai CU           485.81 Mbps       2306.79 Mbps      140.89 ms   https://www.speedtest.net/result/c/7215aa0e-3aee-456b-bef8-89a5afd1a1f6
CN, Chengdu CM           715.48 Mbps       6530.10 Mbps      131.51 ms   https://www.speedtest.net/result/c/4406864e-48f1-4da1-a7ee-22266ccc0a67
HK, HKIX                 1473.22 Mbps      921.89 Mbps       47.90 ms    https://www.speedtest.net/result/c/136e9ec4-36f5-4eed-89d9-ab8296cd2c64
HK, HGC                  1332.98 Mbps      5178.86 Mbps      53.48 ms    https://www.speedtest.net/result/c/b4a04aac-dc37-4e3f-b46e-01ee2f8ec974
HK, i3D.net              1104.02 Mbps      5368.06 Mbps      50.27 ms    https://www.speedtest.net/result/c/d2d00953-f3cb-4d8f-bb12-a9acd97b00e0
JP, i3D.net              6850.57 Mbps      5348.91 Mbps      1.44 ms     https://www.speedtest.net/result/c/2db87507-5401-4cc3-8d48-f451fae6fb22
JP, GSL Networks         654.67 Mbps       7886.89 Mbps      0.70 ms     https://www.speedtest.net/result/c/0082baa1-7ab4-42b5-9b86-4a588c5115f9
JP, fdcservers.net       8336.80 Mbps      4728.28 Mbps      0.68 ms     https://www.speedtest.net/result/c/d2fb1e8a-74de-4a2b-998e-e142adc62d02
SG, i3D.net              1209.77 Mbps      4782.61 Mbps      67.95 ms    https://www.speedtest.net/result/c/0787c2e0-bb61-425d-9522-112c6039c78c
SG, NewMedia Express     1270.99 Mbps      3946.69 Mbps      67.43 ms    https://www.speedtest.net/result/c/e7c59e43-01b8-4db6-9849-90a0a2725245
SG, SuperInternet        841.87 Mbps       2382.51 Mbps      68.00 ms    https://www.speedtest.net/result/c/527414c6-81e1-43ec-a8e4-c04cc2360db1
MY, Telekom Malaysia     742.86 Mbps       4431.58 Mbps      101.64 ms   https://www.speedtest.net/result/c/e8a8b174-e41b-46e8-9b25-4f33e47c547d
MY, Celcom               721.59 Mbps       1709.17 Mbps      106.40 ms   https://www.speedtest.net/result/c/c5fb37e0-8c44-4d7a-8068-eb593af4d0b1
DE, GSL Networks         252.55 Mbps       2676.23 Mbps      217.14 ms   https://www.speedtest.net/result/c/ad73f0df-59ae-4658-8ac9-6a1ad2df39e7
DE, wirsNET              74.10 Mbps        932.78 Mbps       218.54 ms   https://www.speedtest.net/result/c/e5153167-591b-4f5e-94a3-1125092f1130
TR, Turkcell             291.95 Mbps       2424.84 Mbps      337.02 ms   https://www.speedtest.net/result/c/0336abfe-1e53-4ede-a57c-6898ec03b99d
TR, TurkNet              296.91 Mbps       1531.64 Mbps      269.38 ms   https://www.speedtest.net/result/c/1189a167-ef05-47cd-bcf0-c8af813322b4
```

## 流媒体解锁

```
============[ Multination ]============
Dazn:                                  No
HotStar:                               No
Disney+:                               Yes (Region: JP)
Netflix:                               Originals Only
YouTube Premium:                       Yes (Region: JP)
Amazon Prime Video:                    Yes (Region: JP)
TVBAnywhere+:                          Yes
iQyi Oversea Region:                   JP
Viu.com:                               No
YouTube CDN:                           Atlanta, GA
Netflix Preferred CDN:                 Associated with [TPG Internet] in [Sydney, N.S.W. ]
Spotify Registration:                  No
Steam Currency:                        JPY
=======================================
==============[ Taiwan ]===============
KKTV:                                  No
LiTV:                                  No
MyVideo:                               No
4GTV.TV:                               No
LineTV.TW:                             No
Hami Video:                            No
CatchPlay+:                            No
HBO GO Asia:                           No
Bahamut Anime:                         Failed (Network Connection)
Bilibili Taiwan Only:                  No
=======================================
=============[ Hong Kong ]=============
Now E:                                 No
Viu.TV:                                No
MyTVSuper:                             No
HBO GO Asia:                           No
BiliBili Hongkong/Macau/Taiwan:        No
=======================================
===============[ Japan ]===============
DMM:                                   No
Abema.TV:                              No
Niconico:                              No
music.jp:                              No
Telasa:                                No
Paravi:                                No
U-NEXT:                                Yes
Hulu Japan:                            Yes
TVer:                                  Yes
GYAO!:                                 Yes
WOWOW:                                 Failed
VideoMarket:                           No
FOD(Fuji TV):                          No
Radiko:                                No
Karaoke@DAM:                           No
J:com On Demand:                       Failed (Unexpected Result: 502)
---Game---
Kancolle Japan:                        No
Pretty Derby Japan:                    Yes
Konosuba Fantastic Days:               No
Princess Connect Re:Dive Japan:        Yes
World Flipper Japan:                   Yes
Project Sekai: Colorful Stage:         No
=======================================
===========[ North America ]===========
FOX:                                   No
Hulu:                                  Failed
NFL+:                                  Yes
ESPN+:[Sponsored by Jam]               No
Epix:                                  No
Starz:                                 No
Philo:                                 Yes
FXNOW:                                 No
TLC GO:                                No
HBO Max:                               No
Shudder:                               Yes
BritBox:                               Yes
Crackle:                               No
CW TV:                                 No
A&E TV:                                No
NBA TV:                                Yes
NBC TV:                                No
Fubo TV:                               Yes
Tubi TV:                               No
Sling TV:                              Yes
Pluto TV:                              Yes
Acorn TV:                              Yes
SHOWTIME:                              Yes
encoreTVB:                             Yes
Funimation:                            No
Discovery+:                            No
Paramount+:                            Yes
Peacock TV:                            No
Popcornflix:                           No
Crunchyroll:                           No
Directv Stream:                        No
KBS American:                          No
KOCOWA:                                No
---CA---
CBC Gem:                               No
Crave:                                 No
=======================================
===========[ South America ]===========
Star+:                                 No
HBO Max:                               No
DirecTV Go:                            Yes (Region: REGISTRARSE)
Funimation:                            No
=======================================
===============[ Europe ]==============
Rakuten TV:                            Yes
Funimation:                            No
SkyShowTime:                           No
HBO Max:                               No
---GB---
Sky Go:                                No
BritBox:                               Yes
ITV Hub:                               No
Channel 4:                             No
Channel 5:                             No
BBC iPLAYER:                           No
Discovery+ UK:                         No
---FR---
Salto:                                 No
Canal+:                                No
Molotov:                               No
---DE---
Joyn:                                  No
Sky:                                   No
ZDF:                                   No
---NL---
NLZIET:                                Failed
videoland:                             No
NPO Start Plus:                        No
---ES---
PANTAYA:                               No
---IT---
Rai Play:                              Yes
---RU---
Amediateka:                            Yes
=======================================
==============[ Oceania ]==============
NBA TV:                                Yes
Acorn TV:                              Yes
SHOWTIME:                              Yes
BritBox:                               Yes
Funimation:                            No
Paramount+:                            Yes
---AU---
Stan:                                  Yes
Binge:                                 No
Docplay:                               No
Channel 7:                             Failed (Network Connection)
Channel 9:                             No
Channel 10:                            No
ABC iView:                             No
Kayo Sports:                           No
Optus Sports:                          No
SBS on Demand:                         No
---NZ---
Neon TV:                               Yes
SkyGo NZ:                              No
ThreeNow:                              No
Maori TV:                              Yes
=======================================
==============[ Korean ]===============
Wavve:                                 No
Tving:                                 No
Coupang Play:                          No
Naver TV:                              No
Afreeca TV:                            No
KBS Domestic:                          No
KOCOWA:                                No
=======================================
```

## TCP大陆路由

去程: 电信直连(ntt), 联通直连(ntt), 移动部分直连(pccw)  
回程: 电信部分直连(软银), 联通直连(软银), 移动部分直连

## 融合怪脚本测试

```
-----------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD EPYC Processor
 CPU 核心数        : 4
 CPU 频率          : 3792.874 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 120.0 GB (2.2 GB 已用)
 内存              : 15884 MB (223 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 8 min
 负载              : 0.04, 0.27, 0.21
 系统              : CentOS Linux 7 (Core)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 3.10.0-1127.el7.x86_64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 ASN组织           : AS206216 Advin Services LLC
 位置              : Nishi-Tokyo-shi / JP
 地区              : Tokyo
-------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1962 Scores
 4 线程测试(多核)得分: 		7591 Scores
-------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		50187.64 MB/s
 单线程写测试:		21382.19 MB/s
----------------磁盘IO读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		->
 100MB-4K Block		58.9 MB/s (0.07K IOPS, 1.78s)		->
 100MB-4K Block		58.9 MB/s (0.07 IOPS, 1.78s)		69.7 MB/s (17015 IOPS, 1.50s)
 1GB-1M Block		->
 1GB-1M Block		2.4 GB/s (2281 IOPS, 0.44s)		->
 1GB-1M Block		2.4 GB/s (2281 IOPS, 0.44s)		3.0 GB/s (2840 IOPS, 0.35s)
-------------------磁盘IO读写测试--感谢yabs开源-----------------------
dd Sequential Disk Speed Tests:
---------------------------------
       | Test 1      | Test 2      | Test 3      | Avg        
       |             |             |             |            
Write  | 881 MB/s    | 817 MB/s    | 811 MB/s    | 836.33 MB/s
Read   | 616 MB/s    | 2.0 GB/s    | 1.8 GB/s    | 1.47   GB/s
--------------------流媒体解锁--感谢sjlleo开源------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  达拉斯(DFW25S40)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：美国
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
---------------流媒体解锁--感谢RegionRestrictionCheck开源-------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: US)
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				Dallas, TX 
 Netflix Preferred CDN:			Tokyo  
 Spotify Registration:			Yes (Region: JP)
 Steam Currency:			JPY
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
-------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【LT】
--------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化--------
[IPv4]
Your IP supports access to OpenAI. Region: JP
[IPv6]
IPv6 is not supported on the current host. Skip...
-----------------欺诈分数以及IP质量检测--本频道原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
------以下为IPV4检测------
scamalytics数据库:
  欺诈分数(越低越好)：100
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：11
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分： 0
IP类型:
  IP2Location数据库:  Data Center/Web Hosting/Transit
Google搜索可行性：未知
-----------------三网回程--感谢zhanghanyun/backtrace开源--------------
2023/04/13 01:30:25 北京电信 219.141.136.12  测试超时
2023/04/13 01:30:25 北京联通 202.106.50.1    联通4837[普通线路]           
2023/04/13 01:30:25 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/04/13 01:30:25 上海电信 202.96.209.133  电信163 [普通线路]           
2023/04/13 01:30:25 上海联通 210.22.97.1     联通4837[普通线路]           
2023/04/13 01:30:25 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/04/13 01:30:25 广州电信 58.60.188.222   电信163 [普通线路]           
2023/04/13 01:30:25 广州联通 210.21.196.6    联通4837[普通线路]           
2023/04/13 01:30:25 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/04/13 01:30:25 成都电信 61.139.2.69     电信163 [普通线路]           
2023/04/13 01:30:25 成都联通 119.6.6.6       联通4837[普通线路]           
2023/04/13 01:30:25 成都移动 211.137.96.205  移动CMI [普通线路]           
------------------回程路由--感谢fscarmen开源及PR----------------------
IPv4 ASN: Advin Services LLC
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.25 ms  AS206216  日本, 东京都, 东京
0.22 ms  *  日本, 东京都, 东京, datacamp.co.uk
0.57 ms  AS2914  日本, 东京都, 东京, ntt.com
1.00 ms  AS2914  日本, 东京都, 东京, ntt.com
1.25 ms  AS2914  日本, 东京都, 东京, ntt.com
93.72 ms  AS2914  韩国, 首尔, ntt.com
96.19 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
97.07 ms  AS134774  中国, 广东, 深圳, chinatelecom.com.cn, 电信
97.14 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.31 ms  AS206216  日本, 东京都, 东京
0.24 ms  *  日本, 东京都, 东京, datacamp.co.uk
0.43 ms  AS2914  日本, 东京都, 东京, ntt.com
0.85 ms  AS2914  日本, 东京都, 东京, ntt.com
1.18 ms  AS2914  日本, 东京都, 东京, ntt.com
65.13 ms  AS2914  日本, 东京都, 东京, ntt.com
62.75 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
58.55 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.2
0.29 ms  AS206216  日本, 东京都, 东京
0.32 ms  *  日本, 东京都, 东京, datacamp.co.uk
0.38 ms  AS2914  日本, 东京都, 东京, ntt.com
6.57 ms  AS2914  日本, 东京都, 东京, ntt.com
46.57 ms  AS2914  中国, 香港, ntt.com
43.59 ms  AS2914  中国, 香港, ntt.com
49.22 ms  AS2914  中国, 香港, ntt.com
75.50 ms  AS9808  中国, 上海, chinamobile.com, 移动
75.65 ms  AS9808  中国, 上海, chinamobile.com, 移动
106.31 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
89.10 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------网络测速--由teddysun和superspeed开源及spiritlhls整理----------
测速点位置	 上传速度	 下载速度	 延迟
Speedtest.net	 938.93 Mbps	 943.66 Mbps	 0.19 ms
洛杉矶		 690.28 Mbps	 947.06 Mbps	 112.39 ms
新加坡		 892.64 Mbps	 845.58 Mbps	 88.31 ms
电信上海	 1.03 Mbps	 847.05 Mbps	 63.82 ms
电信广东广州5G	 228.82 Mbps	 744.97 Mbps	 171.46 ms
联通湖南长沙	 932.39 Mbps	 755.36 Mbps	 47.61 ms
---------------------------------------------------------------------
```

## 总结

```

国内tcp ping平均: 电信102ms,联通58ms,移动69ms.
给的配置高/内存大, 带免费的DDoS防护;
跑分还行, 面板还可安装Windows镜像(用户名为administrator).
更适合联通直连, 或者沪日IPLC等中转.
跑占用资源高的项目可考虑，比如远程桌面/docker项目之类.
如果要性能更好的，可尝试SpeedyPage
稳定性待观察, 之前东京的网络出了问题, 商家回复解决了.
```
