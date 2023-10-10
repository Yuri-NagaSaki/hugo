---
title: "Oblivus 芝加哥 纽约 拉斯维加斯测评"
date: "2023-08-05"
categories: 
  - "vps"
  - "usa"
---

## 机器配置

> ```
> CPU: AMD EPYC Milan
> RAM: 4G
> SSD: 40GB
> Bandwidth: 10Gbps
> IPV4: 1 
> 不提供ipv6
> ```

![](https://catcat.blog/wp-content/uploads/2023/08/image-432x1024.png)

## 官网价格

![](https://catcat.blog/wp-content/uploads/2023/08/image-2-1024x395.png)

![](https://catcat.blog/wp-content/uploads/2023/08/image-3-1024x296.png)

### 后台面板

![](https://catcat.blog/wp-content/uploads/2023/08/image-4-1024x556.png)

![](https://catcat.blog/wp-content/uploads/2023/08/image-5-1024x563.png)

**不提供Debian的系统镜像**

## 纽约测评

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7443P 24-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 2849.998 MHz
 CPU 缓存          : L1: 64.00 KB / L2: 512.00 KB / L3: 16.00 MB
 硬盘空间          : 4.88 GiB / 38.58 GiB
 启动盘路径        : /dev/vda1
 内存              : 288.07 MiB / 3.82 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 2 min
 负载              : 0.49, 0.16, 0.05
 系统              : Ubuntu 22.04.2 LTS (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.19.0-45-generic
 TCP加速方式       : cubic
 虚拟化架构        : Dedicated
 NAT类型           : 开放型
 IPV4 ASN          : AS33425 CoreWeave, Inc
 IPV4 位置         : New York City / New York / US
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		4477 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		50799.53 MB/s
 单线程写测试:		30436.26 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		170 MB/s (41.58 IOPS, 0.62s)		248 MB/s (60614 IOPS, 0.42s)
 1GB-1M Block		1.7 GB/s (1648 IOPS, 0.61s)		5.9 GB/s (5595 IOPS, 0.18s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 36.22 MB/s    (9.0k) | 332.00 KB/s      (5)
Write      | 36.29 MB/s    (9.0k) | 345.00 KB/s      (5)
Total      | 72.52 MB/s   (18.1k) | 677.00 KB/s     (10)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 696.00 KB/s      (1) | 3.97 MB/s        (3)
Write      | 804.00 KB/s      (1) | 4.00 MB/s        (3)
Total      | 1.50 MB/s        (2) | 7.98 MB/s        (6)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: YYZ(YYZ10S23)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				Yes (Region: US)
 Disney+:				Yes (Region: US)
 Netflix:				Yes (Region: US)
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				Toronto, ON 
 Netflix Preferred CDN:			Washington DC  
 Spotify Registration:			No
 Steam Currency:			USD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ip234数据库       ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 0②  7⑦
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):isp①  Data Center/Web Hosting/Transit⑤  isp⑧  business⑨  
  公司类型(company_type):isp①  isp⑧  
  云服务提供商(cloud_provider):  No⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ② ⑥ ⑧ ⑨ 
  VPN(vpn):  No① ② ⑧ 
  TOR(tor):  No① ② ⑧ ⑨ 
  TOR出口(tor_exit):  No⑧ 
  搜索引擎机器人(search_engine_robot):  No② 
  匿名代理(anonymous):  No⑧ ⑨ 
  攻击方(attacker):  No⑧ ⑨ 
  滥用者(abuser):  No⑧ ⑨ 
  威胁(threat):  No⑧ ⑨ 
  iCloud中继(icloud_relay):  No① ⑧ ⑨ 
  未分配IP(bogon):  No⑧ ⑨ 
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  qq邮箱: Yes
  yandex邮箱: Yes
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/08/05 06:20:52 北京电信 219.141.136.12  测试超时
2023/08/05 06:20:52 北京联通 202.106.50.1    联通4837[普通线路]           
2023/08/05 06:20:52 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/08/05 06:20:52 上海电信 202.96.209.133  电信163 [普通线路]           
2023/08/05 06:20:52 上海联通 210.22.97.1     联通4837[普通线路]           
2023/08/05 06:20:52 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/08/05 06:20:52 广州电信 58.60.188.222   电信163 [普通线路]           
2023/08/05 06:20:52 广州联通 210.21.196.6    联通4837[普通线路]           
2023/08/05 06:20:52 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/08/05 06:20:52 成都电信 61.139.2.69     电信163 [普通线路]           
2023/08/05 06:20:52 成都联通 119.6.6.6       联通4837[普通线路]           
2023/08/05 06:20:52 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.28 ms  *  局域网
0.30 ms  *  局域网
0.21 ms  *  局域网
0.25 ms  *  局域网
0.25 ms  *  局域网
0.21 ms  *  局域网
1.90 ms  AS33425  美国, 纽约州, 纽约, coreweave.com
1.18 ms  AS3356  美国, 纽约州, 纽约, level3.com
69.96 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
222.12 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
227.75 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
235.36 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
239.95 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
240.14 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.09 ms  *  局域网
0.24 ms  *  局域网
0.20 ms  *  局域网
0.19 ms  *  局域网
0.28 ms  *  局域网
0.18 ms  *  局域网
0.89 ms  AS33425  美国, 纽约州, 纽约, coreweave.com
1.79 ms  AS33425  美国, 纽约州, 纽约, coreweave.com
0.60 ms  AS3356  美国, 纽约州, 纽约, level3.com
63.78 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
216.62 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
234.44 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
228.33 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
234.55 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
233.10 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
232.59 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.11 ms  *  局域网
0.21 ms  *  局域网
0.21 ms  *  局域网
0.23 ms  *  局域网
0.21 ms  *  局域网
0.28 ms  *  局域网
2.47 ms  AS33425  美国, 纽约州, 纽约, coreweave.com
0.68 ms  AS3356  美国, 纽约州, 纽约, level3.com
65.16 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
64.08 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
64.23 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
237.20 ms  AS9808  中国, 上海, chinamobile.com, 移动
242.03 ms  AS9808  中国, 上海, chinamobile.com, 移动
253.71 ms  AS9808  中国, 北京, chinamobile.com, 移动
255.29 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 66.17 Mbps	 2707.80 Mbps	 0.52	  0.0%
洛杉矶		 2145.12 Mbps	 4957.39 Mbps	 63.23	  0.0%
日本东京	 470.32 Mbps	 5167.10 Mbps	 173.64	  0.0%
联通WuXi	 1376.08 Mbps	 7149.70 Mbps	 231.40	  0.0%
联通郑州5G	 519.63 Mbps	 635.79 Mbps	 223.98	  NULL
电信Zhenjiang5G	 1.84 Mbps	 3965.47 Mbps	 199.27	  NULL
电信天津	 1.31 Mbps	 4115.85 Mbps	 384.97	  NULL
移动杭州5G	 225.80 Mbps	 696.96 Mbps	 260.41	  0.0%
移动Chengdu	 775.52 Mbps	 1967.30 Mbps	 253.46	  0.0%
------------------------------------------------------------------------
 总共花费      : 9 分 55 秒
 时间          : Sat Aug  5 06:26:37 UTC 2023
------------------------------------------------------------------------
```

### 流媒体解锁

> \============\[ Multination \]============  
> Dazn: No  
> HotStar: Yes (Region: US)  
> Disney+: Yes (Region: US)  
> Netflix: Yes (Region: US)  
> YouTube Premium: Yes  
> Amazon Prime Video: Yes (Region: US)  
> TVBAnywhere+: Yes  
> iQyi Oversea Region: US  
> Viu.com: No  
> YouTube CDN: Toronto, ON  
> Netflix Preferred CDN: Washington DC  
> Spotify Registration: No  
> Steam Currency: USD  
> ChatGPT: Yes  
> \===========\[ North America \]===========  
> FOX: Yes  
> Hulu: Failed  
> NFL+: Yes  
> ESPN+:\[Sponsored by Jam\] Yes  
> Epix: Yes  
> Starz: Yes  
> Philo: Yes  
> FXNOW: Yes  
> TLC GO: Yes  
> HBO Max: Yes  
> Shudder: Yes  
> BritBox: Yes  
> Crackle: Yes  
> CW TV: Yes  
> A&E TV: No  
> NBA TV: Yes  
> NBC TV: Yes  
> Fubo TV: Yes  
> Tubi TV: Yes  
> Sling TV: Yes  
> Pluto TV: Yes  
> Acorn TV: Yes  
> SHOWTIME: Yes  
> encoreTVB: Yes  
> Funimation: Yes (Region: US)  
> Discovery+: Yes  
> Paramount+: Yes  
> Peacock TV: Yes  
> Popcornflix: Yes  
> Crunchyroll: Yes  
> Directv Stream: No  
> KBS American: Failed (Network Connection)  
> KOCOWA: Yes  
> Maths Spot: Failed  
> \---CA--- 
> CBC Gem: No  
> Crave: Yes

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 15 minutes
Processor  : AMD EPYC 7443P 24-Core Processor
CPU cores  : 1 @ 2849.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 0.0 KiB
Disk       : 38.7 GiB
Distro     : Ubuntu 22.04.2 LTS
Kernel     : 5.19.0-45-generic
VM Type    : VM-OTHER
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : CoreWeave, Inc
ASN        : AS33425 CoreWeave, Inc
Location   : New York, New York (NY)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 34.36 MB/s    (8.5k) | 161.00 KB/s      (2)
Write      | 34.46 MB/s    (8.6k) | 171.00 KB/s      (2)
Total      | 68.82 MB/s   (17.2k) | 332.00 KB/s      (4)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.37 MB/s        (4) | 4.04 MB/s        (3)
Write      | 2.41 MB/s        (4) | 4.13 MB/s        (4)
Total      | 4.78 MB/s        (8) | 8.17 MB/s        (7)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 2.47 Gbits/sec  | 1.11 Gbits/sec  | 69.8 ms        
Scaleway        | Paris, FR (10G)           | busy            | busy            | 83.0 ms        
NovoServe       | North Holland, NL (40G)   | busy            | 2.79 Gbits/sec  | 76.7 ms        
Uztelecom       | Tashkent, UZ (10G)        | 2.06 Gbits/sec  | 3.00 Gbits/sec  | 171 ms         
Clouvider       | NYC, NY, US (10G)         | busy            | 7.61 Gbits/sec  | 1.43 ms        
Clouvider       | Dallas, TX, US (10G)      | 5.64 Gbits/sec  | 7.19 Gbits/sec  | 33.1 ms        
Clouvider       | Los Angeles, CA, US (10G) | 2.94 Gbits/sec  | 1.53 Gbits/sec  | 63.3 ms        

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1573                          
Multi Core      | 1552                          
Full Test       | https://browser.geekbench.com/v6/cpu/2154536
```

## 拉斯维加斯

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7413 24-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 2650.002 MHz
 CPU 缓存          : L1: 128.00 KB / L2: 1.00 MB / L3: 16.00 MB
 硬盘空间          : 7.73 GiB / 38.58 GiB
 启动盘路径        : /dev/vda1
 内存              : 615.01 MiB / 7.75 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 12 min
 负载              : 0.44, 1.43, 1.02
 系统              : Ubuntu 22.04.3 LTS (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.19.0-45-generic
 TCP加速方式       : cubic
 虚拟化架构        : Dedicated
 NAT类型           : 开放型
 IPV4 ASN          : AS33425 CoreWeave, Inc
 IPV4 位置         : Las Vegas / Nevada / US
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		4111 Scores
 2 线程测试(多核)得分: 		8169 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		48891.38 MB/s
 单线程写测试:		27666.74 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		177 MB/s (43.20 IOPS, 0.59s)		254 MB/s (62079 IOPS, 0.41s)
 1GB-1M Block		1.3 GB/s (1284 IOPS, 0.78s)		4.5 GB/s (4333 IOPS, 0.23s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 34.26 MB/s    (8.5k) | 7.47 MB/s      (116)
Write      | 34.36 MB/s    (8.5k) | 7.84 MB/s      (122)
Total      | 68.63 MB/s   (17.1k) | 15.31 MB/s     (238)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 11.27 MB/s      (22) | 15.08 MB/s      (14)
Write      | 12.45 MB/s      (24) | 16.83 MB/s      (16)
Total      | 23.73 MB/s      (46) | 31.92 MB/s      (30)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX17S56)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					Yes (Region: US)
 HotStar:				Yes (Region: US)
 Disney+:				Yes (Region: US)
 Netflix:				Yes (Region: US)
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				Los Angeles, CA 
 Netflix Preferred CDN:			Los Angeles, CA  
 Spotify Registration:			No
 Steam Currency:			USD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ip234数据库       ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 0②  9⑦
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):isp①  Data Center/Web Hosting/Transit⑤  isp⑧  business⑨  
  公司类型(company_type):isp①  isp⑧  
  云服务提供商(cloud_provider):  No⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ② ⑥ ⑧ ⑨ ⑩ 
  VPN(vpn):  No① ② ⑧ 
  TOR(tor):  No① ② ⑧ ⑨ 
  TOR出口(tor_exit):  No⑧ 
  搜索引擎机器人(search_engine_robot):  No② 
  匿名代理(anonymous):  No⑧ ⑨ 
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
  qq邮箱：No
  yandex邮箱: Yes
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/08/05 07:03:49 北京电信 219.141.136.12  电信163 [普通线路]           
2023/08/05 07:03:49 北京联通 202.106.50.1    联通4837[普通线路]           
2023/08/05 07:03:49 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/08/05 07:03:49 上海电信 202.96.209.133  电信163 [普通线路]           
2023/08/05 07:03:49 上海联通 210.22.97.1     联通4837[普通线路]           
2023/08/05 07:03:49 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/08/05 07:03:49 广州电信 58.60.188.222   电信163 [普通线路]           
2023/08/05 07:03:49 广州联通 210.21.196.6    联通4837[普通线路]           
2023/08/05 07:03:49 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/08/05 07:03:49 成都电信 61.139.2.69     电信163 [普通线路]           
2023/08/05 07:03:49 成都联通 119.6.6.6       联通4837[普通线路]           
2023/08/05 07:03:49 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.13 ms  *  局域网
0.19 ms  *  局域网
0.29 ms  *  局域网
0.18 ms  *  局域网
0.39 ms  *  局域网
0.25 ms  *  局域网
1.97 ms  AS33425  美国, 内华达州, 拉斯维加斯, coreweave.com
2.58 ms  AS33425  美国, 内华达州, 拉斯维加斯, coreweave.com
0.69 ms  AS3356  美国, 内华达州, 拉斯维加斯, level3.com
16.51 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
15.84 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
166.13 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
175.75 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
178.95 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.23 ms  *  局域网
0.29 ms  *  局域网
0.24 ms  *  局域网
0.23 ms  *  局域网
0.23 ms  *  局域网
0.22 ms  *  局域网
2.45 ms  AS33425  美国, 内华达州, 拉斯维加斯, coreweave.com
1.14 ms  AS33425  美国, 内华达州, 拉斯维加斯, coreweave.com
0.76 ms  AS3356  美国, 内华达州, 拉斯维加斯, level3.com
5.70 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
10.10 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
167.58 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
171.09 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
171.71 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
177.29 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
170.26 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.19 ms  *  局域网
0.29 ms  *  局域网
0.27 ms  *  局域网
0.39 ms  *  局域网
0.24 ms  *  局域网
0.20 ms  *  局域网
2.02 ms  AS33425  美国, 内华达州, 拉斯维加斯, coreweave.com
10.16 ms  AS33425  美国, 内华达州, 拉斯维加斯, coreweave.com
0.70 ms  AS3356  美国, 内华达州, 拉斯维加斯, level3.com
6.37 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
6.22 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
6.05 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
192.22 ms  AS58453  中国, 上海, chinamobile.com, 移动
190.12 ms  AS9808  中国, 上海, chinamobile.com, 移动
192.23 ms  AS9808  中国, 上海, chinamobile.com, 移动
217.63 ms  AS9808  中国, 北京, chinamobile.com, 移动
217.79 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 6198.26 Mbps	 5695.18 Mbps	 0.92	  0.0%
洛杉矶		 7104.50 Mbps	 7519.67 Mbps	 7.54	  0.0%
日本东京	 743.26 Mbps	 7064.14 Mbps	 115.04	  0.0%
联通郑州5G	 563.90 Mbps	 656.05 Mbps	 202.86	  NULL
联通海南	 496.58 Mbps	 2207.44 Mbps	 177.41	  NULL
电信Suzhou5G	 684.79 Mbps	 2583.27 Mbps	 211.59	  NULL
电信天津	 1.00 Mbps	 2137.84 Mbps	 163.02	  NULL
移动Chengdu	 686.08 Mbps	 1717.81 Mbps	 196.65	  0.0%
移动Zhengzhou5G	 351.52 Mbps	 1032.81 Mbps	 207.16	  0.0%
------------------------------------------------------------------------
 总共花费      : 8 分 27 秒
 时间          : Sat Aug  5 07:09:01 UTC 2023
------------------------------------------------------------------------
```

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 25 minutes
Processor  : AMD EPYC 7413 24-Core Processor
CPU cores  : 2 @ 2650.002 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 7.8 GiB
Swap       : 0.0 KiB
Disk       : 38.7 GiB
Distro     : Ubuntu 22.04.3 LTS
Kernel     : 5.19.0-45-generic
VM Type    : VM-OTHER
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : CoreWeave, Inc
ASN        : AS33425 CoreWeave, Inc
Location   : Las Vegas, Nevada (NV)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 34.62 MB/s    (8.6k) | 3.40 MB/s       (53)
Write      | 34.71 MB/s    (8.6k) | 3.59 MB/s       (56)
Total      | 69.34 MB/s   (17.3k) | 7.00 MB/s      (109)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 11.93 MB/s      (23) | 19.46 MB/s      (19)
Write      | 13.00 MB/s      (25) | 21.35 MB/s      (20)
Total      | 24.93 MB/s      (48) | 40.82 MB/s      (39)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 670 Mbits/sec   | 1.17 Gbits/sec  | 134 ms         
Scaleway        | Paris, FR (10G)           | busy            | busy            | 142 ms         
NovoServe       | North Holland, NL (40G)   | 1.12 Gbits/sec  | 1.45 Gbits/sec  | 141 ms         
Uztelecom       | Tashkent, UZ (10G)        | 778 Mbits/sec   | 2.22 Gbits/sec  | 235 ms         
Clouvider       | NYC, NY, US (10G)         | 1.81 Gbits/sec  | 501 Mbits/sec   | 65.8 ms        
Clouvider       | Dallas, TX, US (10G)      | 4.58 Gbits/sec  | 7.20 Gbits/sec  | 32.8 ms        
Clouvider       | Los Angeles, CA, US (10G) | 8.39 Gbits/sec  | 8.84 Gbits/sec  | 5.73 ms        

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1717                          
Multi Core      | 3129                          
Full Test       | https://browser.geekbench.com/v6/cpu/2154871
```

### 流媒体解锁

```
============[ Multination ]============
 Dazn:                                  Yes (Region: US)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Los Angeles, CA 
 Netflix Preferred CDN:                 Los Angeles, CA  
 Spotify Registration:                  No
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
===========[ North America ]===========
 FOX:                                   Yes
 Hulu:                                  Failed
 NFL+:                                  Yes
 ESPN+:[Sponsored by Jam]               Yes
 Epix:                                  Yes
 Starz:                                 Yes
 Philo:                                 Yes
 FXNOW:                                 Yes
 TLC GO:                                Yes
 HBO Max:                               Yes
 Shudder:                               Yes
 BritBox:                               Yes
 Crackle:                               Yes
 CW TV:                                 Yes
 A&E TV:                                No
 NBA TV:                                Yes
 NBC TV:                                Yes
 Fubo TV:                               Yes
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
 KBS American:                          Failed (Network Connection)
 KOCOWA:                                Yes
 Maths Spot:                            Failed
 ---CA---
 CBC Gem:                               No
 Crave:                                 Yes
=======================================
```

## 芝加哥

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7413 24-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 2649.998 MHz
 CPU 缓存          : L1: 128.00 KB / L2: 1.00 MB / L3: 16.00 MB
 硬盘空间          : 4.88 GiB / 38.58 GiB
 启动盘路径        : /dev/vda1
 内存              : 363.70 MiB / 7.75 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 2 min
 负载              : 1.19, 0.31, 0.10
 系统              : Ubuntu 22.04.2 LTS (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.19.0-45-generic
 TCP加速方式       : cubic
 虚拟化架构        : Dedicated
 NAT类型           : 开放型
 IPV4 ASN          : AS33425 CoreWeave, Inc
 IPV4 位置         : Chicago / Illinois / US
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		4062 Scores
 2 线程测试(多核)得分: 		8039 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		41674.85 MB/s
 单线程写测试:		22053.17 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		184 MB/s (44.95 IOPS, 0.57s)		291 MB/s (71161 IOPS, 0.36s)
 1GB-1M Block		785 MB/s (749 IOPS, 1.34s)		6.9 GB/s (6566 IOPS, 0.15s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 33.31 MB/s    (8.3k) | 17.07 MB/s     (266)
Write      | 33.39 MB/s    (8.3k) | 17.58 MB/s     (274)
Total      | 66.70 MB/s   (16.6k) | 34.65 MB/s     (540)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 369.35 MB/s    (721) | 1.13 GB/s     (1.1k)
Write      | 388.97 MB/s    (759) | 1.20 GB/s     (1.1k)
Total      | 758.32 MB/s   (1.4k) | 2.34 GB/s     (2.2k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  达拉斯(DFW28S09)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					Yes (Region: US)
 HotStar:				Yes (Region: US)
 Disney+:				Yes (Region: US)
 Netflix:				Yes (Region: US)
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				Dallas, TX 
 Netflix Preferred CDN:			Chicago, IL  
 Spotify Registration:			No
 Steam Currency:			USD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ip234数据库       ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 0②  33⑦
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):isp①  Data Center/Web Hosting/Transit⑤  business⑨  
  公司类型(company_type):isp①  hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ② ⑥ ⑧ ⑨ ⑩ 
  VPN(vpn):  No① ② ⑧ 
  TOR(tor):  No① ② ⑧ ⑨ 
  TOR出口(tor_exit):  No⑧ 
  搜索引擎机器人(search_engine_robot):  No② 
  匿名代理(anonymous):  No⑧ ⑨ 
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
  qq邮箱：No
  yandex邮箱: Yes
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/08/05 07:35:43 北京电信 219.141.136.12  测试超时
2023/08/05 07:35:43 北京联通 202.106.50.1    联通4837[普通线路]           
2023/08/05 07:35:43 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/08/05 07:35:43 上海电信 202.96.209.133  电信163 [普通线路]           
2023/08/05 07:35:43 上海联通 210.22.97.1     联通4837[普通线路]           
2023/08/05 07:35:43 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/08/05 07:35:43 广州电信 58.60.188.222   电信163 [普通线路]           
2023/08/05 07:35:43 广州联通 210.21.196.6    联通4837[普通线路]           
2023/08/05 07:35:43 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/08/05 07:35:43 成都电信 61.139.2.69     电信163 [普通线路]           
2023/08/05 07:35:43 成都联通 119.6.6.6       联通4837[普通线路]           
2023/08/05 07:35:43 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.13 ms  *  局域网
0.51 ms  *  局域网
0.50 ms  *  局域网
0.42 ms  *  局域网
2.65 ms  AS3356  美国, 伊利诺伊州, 芝加哥, level3.com
60.95 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
107.49 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
277.26 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
305.32 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.12 ms  *  局域网
0.52 ms  *  局域网
0.50 ms  *  局域网
0.38 ms  *  局域网
1.91 ms  AS3356  美国, 伊利诺伊州, 芝加哥, level3.com
58.27 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
210.32 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
202.98 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
229.52 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
207.90 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
208.95 ms  AS17816  中国, 广东, 广州, chinaunicom.com, 联通
215.44 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
208.03 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.13 ms  *  局域网
0.59 ms  *  局域网
0.55 ms  *  局域网
0.43 ms  *  局域网
9.46 ms  AS3356  美国, 伊利诺伊州, 芝加哥, level3.com
51.73 ms  AS3356  美国, 华盛顿州, 西雅图, level3.com
51.19 ms  AS3356  美国, 华盛顿州, 西雅图, level3.com
51.43 ms  AS58453  美国, 华盛顿州, 西雅图, chinamobile.com, 移动
55.45 ms  AS58453  美国, 华盛顿州, 西雅图, chinamobile.com, 移动
230.14 ms  AS58453  中国, 上海, chinamobile.com, 移动
228.48 ms  AS9808  中国, 上海, chinamobile.com, 移动
229.13 ms  AS9808  中国, 上海, chinamobile.com, 移动
239.63 ms  AS9808  中国, 北京, chinamobile.com, 移动
241.71 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 9425.92 Mbps	 5772.86 Mbps	 1.63	  0.0%
洛杉矶		 2598.00 Mbps	 6706.13 Mbps	 54.44	  0.0%
日本东京	 512.12 Mbps	 5644.18 Mbps	 166.68	  0.0%
联通上海5G	 391.67 Mbps	 1926.91 Mbps	 226.18	  0.0%
联通WuXi	 9.69 Mbps	 3121.31 Mbps	 193.40	  0.0%
电信合肥5G	 34.96 Mbps	 178.86 Mbps	 235.51	  NULL
电信Zhenjiang5G	 1.38 Mbps	 2085.47 Mbps	 240.62	  NULL
移动Chengdu	 28.50 Mbps	 2331.47 Mbps	 229.23	  0.7%
移动Zhengzhou5G	 337.03 Mbps	 7.61 Mbps	 245.27	  0.0%
------------------------------------------------------------------------
 总共花费      : 7 分 22 秒
 时间          : Sat Aug  5 07:41:00 UTC 2023
------------------------------------------------------------------------
```

```
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2023-04-23                    #
# https://github.com/masonr/yet-another-bench-script #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

Sat Aug  5 07:41:57 UTC 2023

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 11 minutes
Processor  : AMD EPYC 7413 24-Core Processor
CPU cores  : 2 @ 2649.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 7.8 GiB
Swap       : 0.0 KiB
Disk       : 38.7 GiB
Distro     : Ubuntu 22.04.2 LTS
Kernel     : 5.19.0-45-generic
VM Type    : VM-OTHER
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : CoreWeave, Inc
ASN        : AS33425 CoreWeave, Inc
Host       : RELX inc
Location   : Chicago, Illinois (IL)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 31.25 MB/s    (7.8k) | 21.47 MB/s     (335)
Write      | 31.28 MB/s    (7.8k) | 21.97 MB/s     (343)
Total      | 62.53 MB/s   (15.6k) | 43.44 MB/s     (678)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 495.24 MB/s    (967) | 1.21 GB/s     (1.1k)
Write      | 521.55 MB/s   (1.0k) | 1.29 GB/s     (1.2k)
Total      | 1.01 GB/s     (1.9k) | 2.51 GB/s     (2.4k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.99 Gbits/sec  | 2.31 Gbits/sec  | 92.2 ms        
Scaleway        | Paris, FR (10G)           | busy            | busy            | 98.1 ms        
NovoServe       | North Holland, NL (40G)   | 1.81 Gbits/sec  | 2.13 Gbits/sec  | 99.2 ms        
Uztelecom       | Tashkent, UZ (10G)        | 2.14 Gbits/sec  | 1.77 Gbits/sec  | 193 ms         
Clouvider       | NYC, NY, US (10G)         | 6.43 Gbits/sec  | busy            | 23.9 ms        
Clouvider       | Dallas, TX, US (10G)      | busy            | 8.83 Gbits/sec  | 21.2 ms        
Clouvider       | Los Angeles, CA, US (10G) | 2.55 Gbits/sec  | 3.86 Gbits/sec  | 59.4 ms        

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1419                          
Multi Core      | 2495                          
Full Test       | https://browser.geekbench.com/v6/cpu/2155122
```

```
============[ Multination ]============
 Dazn:                                  Yes (Region: US)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Dallas, TX 
 Netflix Preferred CDN:                 Chicago, IL  
 Spotify Registration:                  No
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
===========[ North America ]===========
 FOX:                                   Yes
 Hulu:                                  Failed
 NFL+:                                  Yes
 ESPN+:[Sponsored by Jam]               Yes
 Epix:                                  Yes
 Starz:                                 Yes
 Philo:                                 Yes
 FXNOW:                                 Yes
 TLC GO:                                Yes
 HBO Max:                               Yes
 Shudder:                               Yes
 BritBox:                               Yes
 Crackle:                               Yes
 CW TV:                                 Yes
 A&E TV:                                No
 NBA TV:                                Yes
 NBC TV:                                Yes
 Fubo TV:                               Yes
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
 KBS American:                          Failed (Network Connection)
 KOCOWA:                                Yes
 Maths Spot:                            Failed
 ---CA---
 CBC Gem:                               No
 Crave:                                 Yes
=======================================
```
