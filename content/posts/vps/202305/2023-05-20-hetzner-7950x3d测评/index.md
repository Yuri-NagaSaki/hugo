---
title: "Hetzner 7950x3d测评"
date: "2023-05-20"
categories: 
  - "vps"
  - "eu"
---

```
眼馋7950x3d的性能，前几天管不住手终于下单了，研究了几天开小鸡
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 4192.140 MHz
 CPU 缓存          : 1024 KB
 硬盘空间          : 15.1 GB (2.7 GB 已用)
 内存              : 940 MB (170 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 2 min
 负载              : 0.07, 0.10, 0.04
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-20-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS24940 Hetzner Online GmbH
 位置              : Großbottwar / DE
 地区              : Baden-Wurttemberg
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		5963 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		69110.81 MB/s
 单线程写测试:		32458.76 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		64.0 MB/s (0.06 IOPS, 1.64s)		63.3 MB/s (15451 IOPS, 1.66s)
 1GB-1M Block		1.1 GB/s (1006 IOPS, 0.99s)		2.6 GB/s (2432 IOPS, 0.41s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 481.46 MB/s (120.3k) | 1.52 GB/s    (23.8k)
Write      | 482.73 MB/s (120.6k) | 1.53 GB/s    (23.9k)
Total      | 964.20 MB/s (241.0k) | 3.06 GB/s    (47.8k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.79 GB/s     (3.4k) | 1.84 GB/s     (1.7k)
Write      | 1.88 GB/s     (3.6k) | 1.96 GB/s     (1.9k)
Total      | 3.67 GB/s     (7.1k) | 3.80 GB/s     (3.7k)
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
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: DE)
 Amazon Prime Video:			Yes (Region: DE)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			DE
 Viu.com:				No
 YouTube CDN:				Frankfurt 
 Netflix Preferred CDN:			Frankfurt  
 Spotify Registration:			No
 Steam Currency:			EUR
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				No
 Disney+:				Yes (Region: US)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: DE)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Frankfurt 
 Netflix Preferred CDN:			Frankfurt  
 Spotify Registration:			No
 Steam Currency:			Failed (Network Connection)
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【DE】
---------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化---------
[IPv4]
Your IP supports access to OpenAI. Region: DE
[IPv6]
Your IP supports access to OpenAI. Region: DE
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：21
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：32
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：NO
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：29
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/05/20 19:56:54 北京电信 219.141.136.12  电信163 [普通线路]           
2023/05/20 19:56:54 北京联通 202.106.50.1    联通4837[普通线路]           
2023/05/20 19:56:54 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/05/20 19:56:54 上海电信 202.96.209.133  电信163 [普通线路]           
2023/05/20 19:56:54 上海联通 210.22.97.1     联通4837[普通线路]           
2023/05/20 19:56:54 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/05/20 19:56:54 广州电信 58.60.188.222   电信163 [普通线路]           
2023/05/20 19:56:54 广州联通 210.21.196.6    联通4837[普通线路]           
2023/05/20 19:56:54 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/05/20 19:56:54 成都电信 61.139.2.69     电信163 [普通线路]           
2023/05/20 19:56:54 成都联通 119.6.6.6       联通4837[普通线路]           
2023/05/20 19:56:54 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS24940 Hetzner Online
IPv6 ASN: AS24940 Hetzner Online
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.26 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
0.33 ms  *  共享地址
0.94 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
2.81 ms  AS24940  德国, 巴伐利亚州, 纽伦堡, hetzner.com
3.07 ms  AS1299  德国, 巴伐利亚州, 纽伦堡, telia.com
5.91 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
5.88 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
7.33 ms  AS4134  德国, 黑森州, 法兰克福, chinatelecom.com.cn, 电信
265.81 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
271.28 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
261.88 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.07 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
0.31 ms  *  共享地址
5.18 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
7.32 ms  AS24940  德国, 巴伐利亚州, 纽伦堡, hetzner.com
3.11 ms  AS1299  德国, 巴伐利亚州, 纽伦堡, telia.com
5.76 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
6.00 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
177.56 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
177.34 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
170.60 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
193.76 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
166.51 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.06 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
9.57 ms  *  共享地址
8.07 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
4.94 ms  AS24940  德国, 黑森州, 法兰克福, hetzner.com
6.72 ms  *  德国, 黑森州, 法兰克福, de-cix.net
7.78 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
230.51 ms  AS58453  中国, 上海, chinamobile.com, 移动
230.88 ms  AS9808  中国, 上海, chinamobile.com, 移动
199.90 ms  AS9808  中国, 北京, chinamobile.com, 移动
200.04 ms  AS9808  中国, 北京, chinamobile.com, 移动
201.48 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 92.84 Mbps	 57.94 Mbps	 4.09	  0.0%
中国香港	 246.78 Mbps	 408.75 Mbps	 269.05	  NULL
新加坡		 10.07 Mbps	 52.70 Mbps	 159.92	  0.3%
联通郑州5G	 467.46 Mbps	 620.14 Mbps	 159.82	  NULL
联通湖南5G	 531.57 Mbps	 449.96 Mbps	 182.78	  NULL
电信上海	 78.63 Mbps	 391.69 Mbps	 228.20	  NULL
电信天津	 1.26 Mbps	 516.92 Mbps	 246.90	  NULL
移动成都	 3.00 Mbps	 20.66 Mbps	 177.07	
移动福州	 4.00 Mbps	 19.07 Mbps	 204.65	
------------------------------------------------------------------------
 总共花费      : 6 分 34 秒
 时间          : Sat May 20 20:02:25 CST 2023
------------------------------------------------------------------------
```

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 6 minutes
Processor  : AMD Ryzen 9 7950X3D 16-Core Processor
CPU cores  : 2 @ 4192.120 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 1024.0 MiB
Disk       : 58.1 GiB
Distro     : Ubuntu 20.04.6 LTS
Kernel     : 5.4.0-148-generic
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
Read       | 645.61 MB/s (161.4k) | 2.05 GB/s    (32.0k)
Write      | 647.32 MB/s (161.8k) | 2.06 GB/s    (32.2k)
Total      | 1.29 GB/s   (323.2k) | 4.11 GB/s    (64.2k)
           |                      |
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ----
Read       | 2.53 GB/s     (4.9k) | 2.70 GB/s     (2.6k)
Write      | 2.66 GB/s     (5.2k) | 2.88 GB/s     (2.8k)
Total      | 5.20 GB/s    (10.1k) | 5.58 GB/s     (5.4k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 926 Mbits/sec   | 917 Mbits/sec   | 15.7 ms
Scaleway        | Paris, FR (10G)           | 929 Mbits/sec   | 934 Mbits/sec   | 24.7 ms
NovoServe       | North Holland, NL (40G)   | 935 Mbits/sec   | 936 Mbits/sec   | 11.7 ms
Uztelecom       | Tashkent, UZ (10G)        | 839 Mbits/sec   | 613 Mbits/sec   | 90.1 ms
Clouvider       | NYC, NY, US (10G)         | 596 Mbits/sec   | 378 Mbits/sec  | 85.2 ms
Clouvider       | Dallas, TX, US (10G)      | 634 Mbits/sec   | 363 Mbits/sec   | 127 ms
Clouvider       | Los Angeles, CA, US (10G) | 569 Mbits/sec   | 388 Mbits/sec  | 148 ms

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 919 Mbits/sec   | 922 Mbits/sec   | 15.6 ms
Scaleway        | Paris, FR (10G)           | 915 Mbits/sec   | 914 Mbits/sec   | 24.4 ms
NovoServe       | North Holland, NL (40G)   | 922 Mbits/sec   | 923 Mbits/sec   | 11.6 ms
Uztelecom       | Tashkent, UZ (10G)        | 840 Mbits/sec   | 616 Mbits/sec   | 89.8 ms
Clouvider       | NYC, NY, US (10G)         | 755 Mbits/sec   | 398 Mbits/sec   | 85.3 ms
Clouvider       | Dallas, TX, US (10G)      | 619 Mbits/sec   | 334 Mbits/sec   | 127 ms
Clouvider       | Los Angeles, CA, US (10G) | 576 Mbits/sec   | 382 Mbits/sec   | 148 ms

YABS completed in 6 min 22 sec
```
