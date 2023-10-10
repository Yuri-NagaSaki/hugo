---
title: "奥地利云服务商 Alwyzon测评"
date: "2023-05-28"
categories: 
  - "vps"
  - "eu"
---

奥地利云服务商 Alwyzon，Hohl IT e.U.旗下品牌，主要售卖 KVM 虚拟化的 VPS，大硬盘存储 VPS 和独立服务器，在奥地利最大互联网中心 Interxion 园区内运营所有服务器。欧洲对等互联优秀。

![](https://catcat.blog/wp-content/uploads/2023/05/image-7-1024x594.png)

## 脚本测试

### 存储机

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : Intel(R) Xeon(R) Silver 4210 CPU @ 2.20GHz
 CPU 核心数        : 2
 CPU 频率          : 2194.842 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 985.1 GB (1.6 GB 已用)
 内存              : 1982 MB (78 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 4 min
 负载              : 0.34, 0.24, 0.10
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-21-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS40994 Hohl IT e.U.
 位置              : Langenzersdorf / AT
 地区              : Lower Austria
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		902 Scores
 2 线程测试(多核)得分: 		1816 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		17934.64 MB/s
 单线程写测试:		12756.73 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		15.3 MB/s (3734 IOPS, 6.86s)		49.6 MB/s (12109 IOPS, 2.11s)
 1GB-1M Block		603 MB/s (574 IOPS, 1.74s)		1.8 GB/s (1693 IOPS, 0.59s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 76.24 MB/s   (19.0k) | 1.08 GB/s    (17.0k)
Write      | 76.44 MB/s   (19.1k) | 1.09 GB/s    (17.0k)
Total      | 152.69 MB/s  (38.1k) | 2.18 GB/s    (34.0k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.57 GB/s     (6.9k) | 2.55 GB/s     (2.4k)
Write      | 3.76 GB/s     (7.3k) | 2.72 GB/s     (2.6k)
Total      | 7.33 GB/s    (14.3k) | 5.27 GB/s     (5.1k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 捷克 布拉格(PRG03S09)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 匈牙利布达佩斯(BUD02S30)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：奥地利
[IPv6]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：奥地利
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：奥地利区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：奥地利区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: AT)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: AT)
 Amazon Prime Video:			Yes (Region: AT)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			INTL
 Viu.com:				No
 YouTube CDN:				Prague 
 Netflix Preferred CDN:			Associated with [RETN Limited] in [Budapest ]
 Spotify Registration:			Yes (Region: AT)
 Steam Currency:			EUR
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				No
 Disney+:				Yes (Region: AT)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: AT)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Budapest 
 Netflix Preferred CDN:			Associated with [RETN Limited] in [Budapest ]
 Spotify Registration:			Yes (Region: AT)
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【AT】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：67
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：28
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：67
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
2023/05/28 09:09:04 北京电信 219.141.136.12  测试超时
2023/05/28 09:09:04 北京联通 202.106.50.1    联通4837[普通线路]           
2023/05/28 09:09:04 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/05/28 09:09:04 上海电信 202.96.209.133  测试超时
2023/05/28 09:09:04 上海联通 210.22.97.1     联通4837[普通线路]           
2023/05/28 09:09:04 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/05/28 09:09:04 广州电信 58.60.188.222   测试超时
2023/05/28 09:09:04 广州联通 210.21.196.6    联通4837[普通线路]           
2023/05/28 09:09:04 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/05/28 09:09:04 成都电信 61.139.2.69     电信163 [普通线路]           
2023/05/28 09:09:04 成都联通 119.6.6.6       联通4837[普通线路]           
2023/05/28 09:09:04 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS40994 Alwyzon
IPv6 ASN: AS40994 Alwyzon
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
21.72 ms  AS40994  奥地利, 维也纳州, 维也纳, alwyzon.com
0.42 ms  AS40994  奥地利, 维也纳州, 维也纳, alwyzon.com
0.54 ms  AS9002  奥地利, 维也纳州, 维也纳, retn.net
12.71 ms  AS9002  德国, 黑森州, 法兰克福, retn.net
275.73 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
87.28 ms  AS40994  奥地利, 维也纳州, 维也纳, alwyzon.com
0.46 ms  AS40994  奥地利, 维也纳州, 维也纳, alwyzon.com
0.93 ms  AS1299  奥地利, 维也纳州, 维也纳, telia.com
11.74 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
11.97 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
173.16 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
169.28 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
174.86 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
191.59 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
31.01 ms  AS40994  奥地利, 维也纳州, 维也纳, alwyzon.com
0.43 ms  AS40994  奥地利, 维也纳州, 维也纳, alwyzon.com
0.50 ms  AS9002  奥地利, 维也纳州, 维也纳, retn.net
13.37 ms  AS9002  德国, 黑森州, 法兰克福, retn.net
25.09 ms  AS9002  德国, 黑森州, 法兰克福, retn.net
26.73 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
266.30 ms  AS58453  中国, 上海, chinamobile.com, 移动
258.41 ms  AS9808  中国, 上海, chinamobile.com, 移动
265.36 ms  AS9808  中国, 上海, chinamobile.com, 移动
249.64 ms  AS9808  中国, 上海, chinamobile.com, 移动
280.62 ms  AS9808  中国, 北京, chinamobile.com, 移动
274.24 ms  AS9808  中国, 北京, chinamobile.com, 移动
279.47 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 3323.98 Mbps	 3094.11 Mbps	 0.38	  0.0%
洛杉矶		 594.51 Mbps	 1108.80 Mbps	 154.01	  0.0%
中国香港	 317.74 Mbps	 3016.96 Mbps	 184.95	  0.0%
联通湖南5G	 516.28 Mbps	 872.57 Mbps	 169.15	  NULL
联通Fuzhou	 480.54 Mbps	 2774.43 Mbps	 199.21	  0.0%
移动Chengdu	 667.22 Mbps	 2177.49 Mbps	 241.95	  0.0%
移动Lanzhou	 555.99 Mbps	 1914.22 Mbps	 283.04	  NULL
------------------------------------------------------------------------
 总共花费      : 6 分 53 秒
 时间          : Sun May 28 09:14:15 UTC 2023
------------------------------------------------------------------------

```

![](https://catcat.blog/wp-content/uploads/2023/05/CleanShot-2023-05-31-at-10.29.24@2x-1024x553.jpg)

### VIRTUAL SERVERS

```
Wed May 24 12:49:24 UTC 2023

Basic System Information:
---------------------------------
Uptime     : 0 days, 6 hours, 1 minutes
Processor  : AMD EPYC 7543P 32-Core Processor
CPU cores  : 2 @ 2799.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 0.0 KiB
Disk       : 39.3 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-19-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Alwyzon
ASN        : AS40994 Hohl IT e.U.
Host       : Hohl IT e.U.
Location   : Vienna, Vienna (9)
Country    : Austria

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 259.07 MB/s  (64.7k) | 2.49 GB/s    (39.0k)
Write      | 259.76 MB/s  (64.9k) | 2.50 GB/s    (39.2k)
Total      | 518.83 MB/s (129.7k) | 5.00 GB/s    (78.2k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.35 GB/s     (8.5k) | 12.22 GB/s   (11.9k)
Write      | 4.58 GB/s     (8.9k) | 13.04 GB/s   (12.7k)
Total      | 8.94 GB/s    (17.4k) | 25.26 GB/s   (24.6k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 2.86 Gbits/sec  | 29.4 Mbits/sec  | 25.7 ms        
Scaleway        | Paris, FR (10G)           | busy            | 2.26 Gbits/sec  | 20.6 ms        
NovoServe       | North Holland, NL (40G)   | 3.25 Gbits/sec  | busy            | 18.4 ms        
Uztelecom       | Tashkent, UZ (10G)        | 2.15 Gbits/sec  | 1.52 Gbits/sec  | 74.9 ms        
Clouvider       | NYC, NY, US (10G)         | 1.73 Gbits/sec  | 1.51 Gbits/sec  | 99.8 ms        
Clouvider       | Dallas, TX, US (10G)      | 1.30 Gbits/sec  | 1.35 Gbits/sec  | 131 ms         
Clouvider       | Los Angeles, CA, US (10G) | 1.03 Gbits/sec  | 1.07 Gbits/sec  | 152 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 2.86 Gbits/sec  | 33.9 Mbits/sec  | 25.7 ms        
Scaleway        | Paris, FR (10G)           | busy            | busy            | 20.2 ms        
NovoServe       | North Holland, NL (40G)   | 3.24 Gbits/sec  | 3.07 Gbits/sec  | 18.7 ms        
Uztelecom       | Tashkent, UZ (10G)        | 2.25 Gbits/sec  | busy            | 75.0 ms        
Clouvider       | NYC, NY, US (10G)         | 1.77 Gbits/sec  | 972 Mbits/sec   | 99.7 ms        
Clouvider       | Dallas, TX, US (10G)      | 1.31 Gbits/sec  | 1.36 Gbits/sec  | 131 ms         
Clouvider       | Los Angeles, CA, US (10G) | 1.07 Gbits/sec  | busy            | 152 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1420                          
Multi Core      | 2492                          
```
