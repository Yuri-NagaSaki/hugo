---
title: "搬瓦工The Plan 机房系列测评"
date: "2023-06-30"
categories: 
  - "vps"
  - "hk"
---

![](https://catcat.blog/wp-content/uploads/2023/06/image-13-1024x427.png)

## 香港HK 三网CMI

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2699.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 40.5 GB (5.4 GB 已用)
 内存              : 1998 MB (628 MB 已用)
 Swap              : 1023 MB (79 MB 已用)
 系统在线时间      : 87 days, 0 hour 39 min
 负载              : 0.24, 0.06, 0.02
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-8-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Hong Kong / HK
 地区              : Central and Western
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		661 Scores
 2 线程测试(多核)得分: 		1324 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		13596.79 MB/s
 单线程写测试:		11401.06 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		14.0 MB/s (3428 IOPS, 7.47s)		17.7 MB/s (4328 IOPS, 5.91s)
 1GB-1M Block		306 MB/s (292 IOPS, 3.42s)		1.1 GB/s (1018 IOPS, 0.98s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 40.45 MB/s   (10.1k) | 497.30 MB/s   (7.7k)
Write      | 40.53 MB/s   (10.1k) | 499.91 MB/s   (7.8k)
Total      | 80.98 MB/s   (20.2k) | 997.21 MB/s  (15.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.00 GB/s     (1.9k) | 1.16 GB/s     (1.1k)
Write      | 1.05 GB/s     (2.0k) | 1.24 GB/s     (1.2k)
Total      | 2.05 GB/s     (4.0k) | 2.41 GB/s     (2.3k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 中国香港(HKG07S42)
Youtube识别地域: 香港(HK)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：香港
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：香港区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: HK)
 Amazon Prime Video:			Yes (Region: HK)
 TVBAnywhere+:				No
 iQyi Oversea Region:			HK
 Viu.com:				Yes (Region: HK)
 YouTube CDN:				Hong Kong 
 Netflix Preferred CDN:			Hong Kong  
 Spotify Registration:			No
 Steam Currency:			HKD
 ChatGPT:				No
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		Failed
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：56
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：42
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/30 09:09:57 北京电信 219.141.136.12  移动CMI [普通线路]           
2023/06/30 09:09:57 北京联通 202.106.50.1    移动CMI [普通线路]           
2023/06/30 09:09:57 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/30 09:09:57 上海电信 202.96.209.133  移动CMI [普通线路]           
2023/06/30 09:09:57 上海联通 210.22.97.1     移动CMI [普通线路]           
2023/06/30 09:09:57 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/30 09:09:57 广州电信 58.60.188.222   移动CMI [普通线路]           
2023/06/30 09:09:57 广州联通 210.21.196.6    移动CMI [普通线路]           
2023/06/30 09:09:57 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/30 09:09:57 成都电信 61.139.2.69     移动CMI [普通线路]           
2023/06/30 09:09:57 成都联通 119.6.6.6       移动CMI [普通线路]           
2023/06/30 09:09:57 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
12.53 ms  *  局域网
716.13 ms  AS9312  中国, 香港, xtom.com
0.39 ms  AS9312  中国, 香港, xtom.com
0.75 ms  AS9312  中国, 香港, xtom.com
0.53 ms  AS58453  中国, 香港, chinamobile.com, 移动
0.53 ms  AS58453  中国, 香港, chinamobile.com, 移动
28.56 ms  AS58453  中国, 上海, chinamobile.com, 移动
29.42 ms  AS9808  中国, 上海, chinamobile.com, 移动
29.49 ms  AS9808  中国, 上海, chinamobile.com, 移动
50.18 ms  AS9808  中国, 上海, chinamobile.com, 移动
90.06 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
12.40 ms  *  局域网
7.08 ms  AS9312  中国, 香港, xtom.com
0.72 ms  AS9312  中国, 香港, xtom.com
0.83 ms  AS9312  中国, 香港, xtom.com
0.37 ms  AS58453  中国, 香港, chinamobile.com, 移动
2.38 ms  AS58453  中国, 香港, chinamobile.com, 移动
28.66 ms  AS58453  中国, 上海, chinamobile.com, 移动
29.89 ms  AS9808  中国, 上海, chinamobile.com, 移动
29.90 ms  AS9808  中国, 上海, chinamobile.com, 移动
68.21 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
83.06 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
90.25 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
89.55 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
95.48 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
87.28 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
12.77 ms  *  局域网
3.21 ms  AS9312  中国, 香港, xtom.com
0.38 ms  AS9312  中国, 香港, xtom.com
0.83 ms  AS9312  中国, 香港, xtom.com
0.60 ms  AS58453  中国, 香港, chinamobile.com, 移动
174.83 ms  AS58453  中国, 香港, chinamobile.com, 移动
2.19 ms  AS58453  中国, 香港, chinamobile.com, 移动
28.38 ms  AS58453  中国, 上海, chinamobile.com, 移动
29.17 ms  AS9808  中国, 上海, chinamobile.com, 移动
29.58 ms  AS9808  中国, 上海, chinamobile.com, 移动
49.26 ms  AS9808  中国, 上海, chinamobile.com, 移动
46.19 ms  AS9808  中国, 北京, chinamobile.com, 移动
50.02 ms  AS9808  中国, 北京, chinamobile.com, 移动
48.00 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 7227.95 Mbps	 4069.21 Mbps	 0.29	  NULL
中国香港	 1964.22 Mbps	 876.08 Mbps	 4.08	  NULL
新加坡		 2521.26 Mbps	 852.05 Mbps	 35.47	  0.0%
联通上海5G	 2249.69 Mbps	 1446.87 Mbps	 61.78	  0.0%
联通WuXi	 2016.78 Mbps	 30.63 Mbps	 67.28	  0.0%
电信上海	 312.12 Mbps	 69.96 Mbps	 57.54	  NULL
电信Zhenjiang5G	 1120.72 Mbps	 1766.57 Mbps	 83.49	  NULL
移动Beijing	 3863.96 Mbps	 2300.05 Mbps	 41.42	  NULL
移动杭州5G	 1099.21 Mbps	 25.10 Mbps	 52.88	  0.0%
------------------------------------------------------------------------
```

## 日本软银

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2699.990 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.5 GB (8.7 GB 已用)
 内存              : 1986 MB (1097 MB 已用)
 Swap              : 1023 MB (252 MB 已用)
 系统在线时间      : 0 days, 0 hour 8 min
 负载              : 0.31, 0.22, 0.19
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Osaka / JP
 地区              : Ōsaka
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		738 Scores
 2 线程测试(多核)得分: 		1534 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		16913.83 MB/s
 单线程写测试:		13994.32 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		17.5 MB/s (4274 IOPS, 5.99s)		21.3 MB/s (5189 IOPS, 4.93s)
 1GB-1M Block		334 MB/s (319 IOPS, 3.14s)		1.2 GB/s (1171 IOPS, 0.85s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 39.64 MB/s    (9.9k) | 368.18 MB/s   (5.7k)
Write      | 39.73 MB/s    (9.9k) | 370.12 MB/s   (5.7k)
Total      | 79.38 MB/s   (19.8k) | 738.30 MB/s  (11.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 895.21 MB/s   (1.7k) | 1.03 GB/s     (1.0k)
Write      | 942.78 MB/s   (1.8k) | 1.10 GB/s     (1.0k)
Total      | 1.83 GB/s     (3.5k) | 2.14 GB/s     (2.0k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 日本 大阪(KIX07S05)
Youtube识别地域: 日本(JP)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 日本 大阪(KIX06S16)
Youtube识别地域: 日本(JP)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：日本
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
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
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: JP)
 Amazon Prime Video:			Yes (Region: JP)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			JP
 Viu.com:				No
 YouTube CDN:				Osaka 
 Netflix Preferred CDN:			Osaka  
 Spotify Registration:			No
 Steam Currency:			JPY
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【JP】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：55
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：4
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/26 23:54:05 北京电信 219.141.136.12  电信163 [普通线路]
2023/06/26 23:54:05 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/26 23:54:05 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/26 23:54:05 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/26 23:54:05 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/26 23:54:05 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/26 23:54:05 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/26 23:54:05 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/26 23:54:05 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/26 23:54:05 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/26 23:54:05 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/26 23:54:05 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
20.14 ms  *  局域网
17.50 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.52 ms  AS4785  日本, 大阪府, 大阪, xtom.com
7.78 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.92 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.50 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
1.55 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
27.37 ms  AS17676  中国, 上海, bbtec.net
33.26 ms  AS4134  中国, 上海, chinatelecom.com.cn, 电信
33.87 ms  AS4134  中国, 上海, chinatelecom.com.cn, 电信
59.69 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
60.65 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
13.75 ms  *  局域网
12.85 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.76 ms  AS4785  日本, 大阪府, 大阪, xtom.com
10.31 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.58 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.61 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
1.50 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
52.87 ms  AS17676  中国, 北京, bbtec.net
81.30 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
75.66 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
74.71 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
80.08 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
81.38 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
15.87 ms  *  局域网
17.60 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.94 ms  AS4785  日本, 大阪府, 大阪, xtom.com
5.51 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.83 ms  AS4785  日本, 大阪府, 大阪, xtom.com
0.45 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
1.56 ms  AS17676  日本, 大阪府, 大阪, bbtec.net
7.62 ms  AS17676  日本, 东京都, 东京, bbtec.net
61.07 ms  AS58453  中国, 上海, chinamobile.com, 移动
61.45 ms  AS9808  中国, 上海, chinamobile.com, 移动
60.78 ms  AS9808  中国, 上海, chinamobile.com, 移动
79.19 ms  AS9808  中国, 上海, chinamobile.com, 移动
86.92 ms  AS9808  中国, 北京, chinamobile.com, 移动
83.24 ms  AS9808  中国, 北京, chinamobile.com, 移动
85.28 ms  AS9808  中国, 北京, chinamobile.com, 移动
82.30 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 464.71 Mbps	 1961.98 Mbps	 7.43	  71.0%
日本东京	 3914.06 Mbps	 2477.31 Mbps	 11.32	  0.0%
新加坡		 2387.24 Mbps	 840.69 Mbps	 83.57	  0.0%
联通湖南5G	 1782.90 Mbps	 536.20 Mbps	 50.48	  NULL
联通WuXi	 42.19 Mbps	 43.03 Mbps	 47.45	  0.0%
电信上海	 363.16 Mbps	 117.82 Mbps	 44.88	  NULL
电信合肥5G	 1451.45 Mbps	 165.93 Mbps	 47.78	  0.0%
移动Zhengzhou5G	 1035.50 Mbps	 1158.76 Mbps	 85.78	  0.0%
移动杭州5G	 729.57 Mbps	 2606.44 Mbps	 83.91	  0.0%
------------------------------------------------------------------------
```

## 悉尼9929

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2399.996 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1984 MB (292 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 1 min
 负载              : 0.00, 0.00, 0.00
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS8888 xTom Pty Ltd
 位置              : Sydney / AU
 地区              : New South Wales
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		894 Scores
 2 线程测试(多核)得分: 		1765 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		19730.28 MB/s
 单线程写测试:		14682.46 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		24.2 MB/s (5905 IOPS, 4.34s)		27.2 MB/s (6642 IOPS, 3.85s)
 1GB-1M Block		495 MB/s (472 IOPS, 2.12s)		1.7 GB/s (1588 IOPS, 0.63s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 58.12 MB/s   (14.0k) | 668.04 MB/s  (10.4k)
Write      | 58.21 MB/s   (14.0k) | 671.56 MB/s  (10.4k)
Total      | 112.33 MB/s  (28.0k) | 1.33 GB/s    (20.9k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.32 GB/s     (2.6k) | 1.76 GB/s     (1.7k)
Write      | 1.44 GB/s     (2.8k) | 1.88 GB/s     (1.8k)
Total      | 2.81 GB/s     (5.4k) | 3.65 GB/s     (3.5k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 澳大利亚 悉尼(SYD15S07)
Youtube识别地域: 澳大利亚(AU)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 澳大利亚 悉尼(SYD15S07)
Youtube识别地域: 澳大利亚(AU)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：澳大利亚
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：澳大利亚区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：澳大利亚区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: AU)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: AU)
 Amazon Prime Video:			Yes (Region: AU)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			AU
 Viu.com:				No
 YouTube CDN:				Sydney, N.S.W. 
 Netflix Preferred CDN:			Sydney, N.S.W.  
 Spotify Registration:			No
 Steam Currency:			AUD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【AU】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：50
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：17
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 01:27:24 北京电信 219.141.136.12  联通9929[优质线路]           
2023/06/27 01:27:24 北京联通 202.106.50.1    联通9929[优质线路]           
2023/06/27 01:27:24 北京移动 221.179.155.161 联通9929[优质线路]           
2023/06/27 01:27:24 上海电信 202.96.209.133  联通9929[优质线路]           
2023/06/27 01:27:24 上海联通 210.22.97.1     联通9929[优质线路]           
2023/06/27 01:27:24 上海移动 211.136.112.200 联通9929[优质线路]           
2023/06/27 01:27:24 广州电信 58.60.188.222   联通9929[优质线路]           
2023/06/27 01:27:24 广州联通 210.21.196.6    联通9929[优质线路]           
2023/06/27 01:27:24 广州移动 120.196.165.24  联通9929[优质线路]           
2023/06/27 01:27:24 成都电信 61.139.2.69     联通9929[优质线路]           
2023/06/27 01:27:24 成都联通 119.6.6.6       联通9929[优质线路]           
2023/06/27 01:27:24 成都移动 211.137.96.205  联通9929[优质线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS8888 xTom
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
4.07 ms  AS8888  澳大利亚, 新南威尔士州, 悉尼, xtom.com
0.61 ms  AS8888  澳大利亚, 新南威尔士州, 悉尼, xtom.com
2.00 ms  AS10099  中国, 香港, chinaunicom.com, 联通
137.46 ms  *  中国, 香港, chinaunicom.com, 联通
129.29 ms  AS10099  中国, 香港, chinaunicom.com, 联通
132.43 ms  AS9929  中国, 广东, 广州, chinaunicom.com, 联通
135.17 ms  AS9929  中国, 广东, 广州, chinaunicom.com, 联通
142.52 ms  *  中国, 广东, 广州, chinaunicom.com, 联通
146.44 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
148.40 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
141.10 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
2.69 ms  AS8888  澳大利亚, 新南威尔士州, 悉尼, xtom.com
0.26 ms  AS8888  澳大利亚, 新南威尔士州, 悉尼, xtom.com
1.96 ms  AS10099  中国, 香港, chinaunicom.com, 联通
133.82 ms  *  中国, 香港, chinaunicom.com, 联通
129.20 ms  AS10099  中国, 香港, chinaunicom.com, 联通
135.68 ms  AS9929  中国, 广东, 广州, chinaunicom.com, 联通
138.26 ms  AS9929  中国, 广东, 广州, chinaunicom.com, 联通
142.61 ms  *  中国, 广东, 广州, chinaunicom.com, 联通
146.15 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
149.12 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
142.50 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
31.71 ms  AS8888  澳大利亚, 新南威尔士州, 悉尼, xtom.com
0.24 ms  AS8888  澳大利亚, 新南威尔士州, 悉尼, xtom.com
1.88 ms  AS10099  中国, 香港, chinaunicom.com, 联通
134.80 ms  *  中国, 香港, chinaunicom.com, 联通
128.89 ms  AS10099  中国, 香港, chinaunicom.com, 联通
131.27 ms  AS9929  中国, 广东, 广州, chinaunicom.com, 联通
136.39 ms  *  中国, 广东, 广州, chinaunicom.com, 联通
137.63 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
159.75 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
159.37 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
163.61 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
158.96 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 2176.40 Mbps	 8716.08 Mbps	 0.15	  0.0%
新加坡		 2092.72 Mbps	 1509.47 Mbps	 95.62	  0.0%
日本东京	 2119.19 Mbps	 5192.22 Mbps	 101.68	  0.0%
联通湖南5G	 641.02 Mbps	 426.90 Mbps	 145.88	  NULL
联通海南	 601.86 Mbps	 700.90 Mbps	 151.95	  NULL
电信上海	 384.66 Mbps	 308.49 Mbps	 144.31	  NULL
电信合肥5G	 535.22 Mbps	 16.68 Mbps	 155.17	  0.0%
移动Beijing	 1146.49 Mbps	 1614.98 Mbps	 162.98	  NULL
移动Chengdu	 1061.10 Mbps	 1314.56 Mbps	 180.62	  0.0%
------------------------------------------------------------------------
```

## 纽约

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2599.986 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (299 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 1 min
 负载              : 0.09, 0.03, 0.00
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : New York City / US
 地区              : New York
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		738 Scores
 2 线程测试(多核)得分: 		1466 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		15177.68 MB/s
 单线程写测试:		11870.90 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		15.3 MB/s (3744 IOPS, 6.84s)		20.1 MB/s (4912 IOPS, 5.21s)
 1GB-1M Block		712 MB/s (679 IOPS, 1.47s)		1.5 GB/s (1400 IOPS, 0.71s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 48.35 MB/s   (12.0k) | 649.17 MB/s  (10.1k)
Write      | 48.40 MB/s   (12.1k) | 652.59 MB/s  (10.1k)
Total      | 96.75 MB/s   (24.1k) | 1.30 GB/s    (20.3k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.49 GB/s     (2.9k) | 1.73 GB/s     (1.6k)
Write      | 1.57 GB/s     (3.0k) | 1.84 GB/s     (1.8k)
Total      | 3.07 GB/s     (6.0k) | 3.58 GB/s     (3.4k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: LGA(LGA25S82)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: LGA(LGA25S82)
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
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				New York, NY 
 Netflix Preferred CDN:			New York, NY  
 Spotify Registration:			No
 Steam Currency:			USD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：56
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：3
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 03:54:33 北京电信 219.141.136.12  测试超时
2023/06/27 03:54:33 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 03:54:33 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/27 03:54:33 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/27 03:54:33 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/27 03:54:33 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/27 03:54:33 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/27 03:54:33 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/27 03:54:33 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/27 03:54:33 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/27 03:54:33 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 03:54:33 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
7.84 ms  *  局域网
1.75 ms  AS46407  美国, 新泽西州, 皮斯卡特维, choopa.com
1.22 ms  *  局域网
1.45 ms  *  局域网
2.24 ms  AS3356  美国, 纽约州, 纽约, level3.com
70.25 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
166.90 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
310.90 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
251.77 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
61.47 ms  *  局域网
3.84 ms  AS46407  美国, 新泽西州, 皮斯卡特维, choopa.com
1.16 ms  *  局域网
0.94 ms  *  局域网
1.00 ms  *  局域网
2.25 ms  AS3356  美国, 纽约州, 纽约, level3.com
65.17 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
73.19 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
221.72 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
235.65 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
229.26 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
228.02 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
231.01 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
18.82 ms  *  局域网
6.63 ms  AS46407  美国, 新泽西州, 皮斯卡特维, choopa.com
6.66 ms  *  局域网
1.04 ms  *  局域网
1.18 ms  *  局域网
1.98 ms  *  美国, 纽约州, 纽约, telehouse.com
3.02 ms  AS58453  美国, 纽约州, 纽约, chinamobile.com, 移动
57.37 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
234.35 ms  AS9808  中国, 上海, chinamobile.com, 移动
233.88 ms  AS9808  中国, 上海, chinamobile.com, 移动
248.15 ms  AS9808  中国, 上海, chinamobile.com, 移动
248.95 ms  AS9808  中国, 北京, chinamobile.com, 移动
251.70 ms  AS9808  中国, 北京, chinamobile.com, 移动
250.50 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 1283.65 Mbps	 6685.22 Mbps	 1.66	  0.0%
洛杉矶		 1537.01 Mbps	 4115.14 Mbps	 58.74	  0.0%
日本东京	 1429.80 Mbps	 3450.80 Mbps	 150.05	  0.0%
联通郑州5G	 720.99 Mbps	 635.45 Mbps	 226.93	  NULL
联通WuXi	 6.23 Mbps	 163.85 Mbps	 266.03	  0.0%
电信上海	 60.37 Mbps	 8.77 Mbps	 408.96	  NULL
电信Suzhou5G	 742.50 Mbps	 0.52 Mbps	 980.42	  NULL
移动Beijing	 808.33 Mbps	 1478.94 Mbps	 234.37	  NULL
------------------------------------------------------------------------
```

## 新泽西

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2599.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (299 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 2 min
 负载              : 0.01, 0.00, 0.00
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : New York City / US
 地区              : New York
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		640 Scores
 2 线程测试(多核)得分: 		1276 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		13415.08 MB/s
 单线程写测试:		11890.46 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		14.7 MB/s (3587 IOPS, 7.14s)		17.2 MB/s (4191 IOPS, 6.11s)
 1GB-1M Block		361 MB/s (344 IOPS, 2.91s)		1.1 GB/s (1066 IOPS, 0.94s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 38.45 MB/s    (9.6k) | 377.89 MB/s   (5.9k)
Write      | 38.52 MB/s    (9.6k) | 379.88 MB/s   (5.9k)
Total      | 76.98 MB/s   (19.2k) | 757.77 MB/s  (11.8k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 479.66 MB/s    (936) | 708.89 MB/s    (692)
Write      | 505.14 MB/s    (986) | 756.10 MB/s    (738)
Total      | 984.80 MB/s   (1.9k) | 1.46 GB/s     (1.4k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: LGA(LGA34S42)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: LGA(LGA34S42)
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
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				New York, NY 
 Netflix Preferred CDN:			Newark, NJ  
 Spotify Registration:			No
 Steam Currency:			USD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：46
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 55
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 34
ip234数据库：
  欺诈分数(越低越好)：8
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 06:04:42 北京电信 219.141.136.12  电信163 [普通线路]           
2023/06/27 06:04:42 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 06:04:42 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/27 06:04:42 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/27 06:04:42 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/27 06:04:42 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/27 06:04:42 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/27 06:04:42 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/27 06:04:42 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/27 06:04:42 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/27 06:04:42 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 06:04:42 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
1.66 ms  AS32748  美国, 新泽西州, 爱迪生, steadfast.net
0.43 ms  AS32748  美国, 新泽西州, 爱迪生, steadfast.net
4.45 ms  AS2914  美国, 纽约州, 纽约, ntt.com
2.25 ms  AS2914  美国, 新泽西州, 纽瓦克, ntt.com
5.05 ms  AS2914  美国, 纽约州, 纽约, ntt.com
5.57 ms  AS2914  美国, 纽约州, 纽约, ntt.com
73.70 ms  AS4134  美国, 加利福尼亚州, 洛杉矶, chinatelecom.com.cn, 电信
243.69 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
244.03 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.43 ms  AS32748  美国, 新泽西州, 爱迪生, steadfast.net
0.37 ms  AS32748  美国, 新泽西州, 爱迪生, steadfast.net
1.42 ms  AS1299  美国, 新泽西州, 纽瓦克, telia.com
2.03 ms  AS1299  美国, 纽约州, 纽约, telia.com
6.45 ms  AS1299  美国, 弗吉尼亚州, 阿什本, telia.com
60.19 ms  AS1299  美国, 加利福尼亚州, 洛杉矶, telia.com
93.11 ms  AS4837  美国, 加利福尼亚州, 洛杉矶, chinaunicom.com, 联通
219.69 ms  AS4837  中国, 北京, chinaunicom.com, 联通
252.03 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
250.65 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
231.63 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
238.52 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
242.18 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.35 ms  AS32748  美国, 新泽西州, 爱迪生, steadfast.net
0.40 ms  AS32748  美国, 新泽西州, 爱迪生, steadfast.net
1.92 ms  AS2914  美国, 纽约州, 纽约, ntt.com
5.11 ms  AS2914  美国, 新泽西州, 纽瓦克, ntt.com
62.64 ms  AS2914  美国, 华盛顿州, 西雅图, ntt.com
158.98 ms  AS2914  日本, 东京都, 东京, ntt.com
207.66 ms  AS2914  中国, 香港, ntt.com
202.77 ms  AS2914  中国, 香港, ntt.com
243.54 ms  AS9808  中国, 上海, chinamobile.com, 移动
257.01 ms  AS9808  中国, 北京, chinamobile.com, 移动
259.38 ms  AS9808  中国, 北京, chinamobile.com, 移动
258.14 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 913.27 Mbps	 746.53 Mbps	 1.59	  NULL
洛杉矶		 887.26 Mbps	 946.66 Mbps	 61.94	  0.0%
日本东京	 780.67 Mbps	 788.56 Mbps	 155.19	  0.0%
联通WuXi	 298.64 Mbps	 606.95 Mbps	 241.93	  0.0%
电信上海	 55.89 Mbps	 471.00 Mbps	 238.09	  NULL
电信Suzhou5G	 639.20 Mbps	 607.20 Mbps	 210.87	  NULL
移动Chengdu	 581.79 Mbps	 13.83 Mbps	 265.90	  0.0%
移动Beijing	 493.59 Mbps	 510.61 Mbps	 243.85	  NULL
------------------------------------------------------------------------
```

## 荷兰EUNL\_3

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2599.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (289 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 1 min
 负载              : 0.11, 0.06, 0.02
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Rotterdam / NL
 地区              : South Holland
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		700 Scores
 2 线程测试(多核)得分: 		1325 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		14830.25 MB/s
 单线程写测试:		12807.23 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		10.7 MB/s (2600 IOPS, 9.84s)		13.4 MB/s (3268 IOPS, 7.83s)
 1GB-1M Block		260 MB/s (248 IOPS, 4.03s)		941 MB/s (897 IOPS, 1.11s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 34.73 MB/s    (8.6k) | 376.12 MB/s   (5.8k)
Write      | 34.84 MB/s    (8.7k) | 378.10 MB/s   (5.9k)
Total      | 69.58 MB/s   (17.3k) | 754.23 MB/s  (11.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 871.90 MB/s   (1.7k) | 1.07 GB/s     (1.0k)
Write      | 918.23 MB/s   (1.7k) | 1.14 GB/s     (1.1k)
Total      | 1.79 GB/s     (3.4k) | 2.21 GB/s     (2.1k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: DTELIX
视频缓存节点地域: KBP(KBP3)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: DTELIX
视频缓存节点地域: KBP(KBP3)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：荷兰
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：荷兰区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：荷兰区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: NL)
 Amazon Prime Video:			Yes (Region: NL)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			INTL
 Viu.com:				No
 YouTube CDN:				Associated with [DTELIX]
 Netflix Preferred CDN:			Amsterdam  
 Spotify Registration:			No
 Steam Currency:			EUR
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【NL】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：46
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：46
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 03:43:13 北京电信 219.141.136.12  测试超时
2023/06/27 03:43:13 北京联通 202.106.50.1    测试超时
2023/06/27 03:43:13 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/27 03:43:13 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/27 03:43:13 上海联通 210.22.97.1     测试超时
2023/06/27 03:43:13 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/27 03:43:13 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/27 03:43:13 广州联通 210.21.196.6    测试超时
2023/06/27 03:43:13 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/27 03:43:13 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/27 03:43:13 成都联通 119.6.6.6       测试超时
2023/06/27 03:43:13 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
64.27 ms  AS49544  荷兰, 南荷兰省, 鹿特丹, i3d.net
0.54 ms  AS49544  荷兰, 南荷兰省, 鹿特丹, i3d.net
8.52 ms  AS2914  荷兰, 北荷兰省, 阿姆斯特丹, ntt.com
2.49 ms  AS2914  荷兰, 北荷兰省, 阿姆斯特丹, ntt.com
8.61 ms  AS2914  英国, 伦敦, ntt.com
7.90 ms  AS2914  英国, 伦敦, ntt.com
9.20 ms  AS4134  英国, 伦敦, chinatelecom.com.cn, 电信
206.87 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
202.84 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
215.05 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
214.91 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.61 ms  AS49544  荷兰, 南荷兰省, 鹿特丹, i3d.net
0.76 ms  AS49544  荷兰, 南荷兰省, 鹿特丹, i3d.net
1.66 ms  AS49544  荷兰, 北荷兰省, 阿姆斯特丹, i3d.net
2.45 ms  *  荷兰, 北荷兰省, 阿姆斯特丹, ams-ix.net
2.69 ms  AS1239  荷兰, 北荷兰省, 阿姆斯特丹, sprint.com
9.03 ms  AS1239  英国, 伦敦, sprint.com
84.06 ms  AS1239  英国, 伦敦, sprint.com
81.97 ms  AS1239  美国, 纽约州, 纽约, sprint.com
83.49 ms  AS1239  美国, 马里兰州, 阿比特斯, sprint.com
82.13 ms  AS1239  美国, 华盛顿, sprint.com
95.83 ms  AS1239  美国, 南卡罗来纳州, 费尔法克斯, sprint.com
101.08 ms  AS1239  美国, 乔治亚州, 亚特兰大, sprint.com
114.30 ms  AS1239  美国, 德克萨斯州, 沃思堡, sprint.com
142.42 ms  AS1239  美国, 加利福尼亚州, 里亚托, sprint.com
139.45 ms  AS1239  美国, 加利福尼亚州, 洛杉矶, sprint.com
234.31 ms  AS1239  美国, 加利福尼亚州, 洛杉矶, sprint.com
226.05 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
282.89 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
244.49 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
260.19 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
264.72 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.64 ms  AS49544  荷兰, 南荷兰省, 鹿特丹, i3d.net
1.41 ms  AS49544  荷兰, 南荷兰省, 鹿特丹, i3d.net
40.32 ms  AS49544  英国, 伦敦, i3d.net
9.23 ms  AS34984  英国, 伦敦, linx.net
251.57 ms  AS58453  中国, 上海, chinamobile.com, 移动
242.54 ms  AS9808  中国, 上海, chinamobile.com, 移动
252.88 ms  AS9808  中国, 上海, chinamobile.com, 移动
265.64 ms  AS9808  中国, 上海, chinamobile.com, 移动
266.15 ms  AS9808  中国, 北京, chinamobile.com, 移动
266.61 ms  AS9808  中国, 北京, chinamobile.com, 移动
271.43 ms  AS9808  中国, 北京, chinamobile.com, 移动
268.76 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 765.91 Mbps	 893.16 Mbps	 0.57	  0.0%
洛杉矶		 633.44 Mbps	 663.54 Mbps	 137.26	  0.0%
新加坡		 630.51 Mbps	 244.53 Mbps	 175.19	  0.0%
联通WuXi	 9.10 Mbps	 278.81 Mbps	 222.63	  0.0%
联通湖南5G	 348.80 Mbps	 9.66 Mbps	 262.51	  NULL
电信天津5G	 287.60 Mbps	 318.19 Mbps	 167.02	  6.5%
移动Beijing	 512.36 Mbps	 459.08 Mbps	 255.73	  NULL
移动Zhengzhou5G	 284.79 Mbps	 69.58 Mbps	 259.35	  0.0%
------------------------------------------------------------------------
```

## 荷兰联通9929

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 1999.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (313 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 1 hour 50 min
 负载              : 0.12, 0.03, 0.01
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS3214 xTom GmbH
 位置              : Amsterdam / NL
 地区              : North Holland
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		716 Scores
 2 线程测试(多核)得分: 		1444 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		16369.40 MB/s
 单线程写测试:		12568.47 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		22.4 MB/s (5470 IOPS, 4.68s)		25.3 MB/s (6169 IOPS, 4.15s)
 1GB-1M Block		529 MB/s (505 IOPS, 1.98s)		1.8 GB/s (1700 IOPS, 0.59s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 52.95 MB/s   (13.2k) | 690.99 MB/s  (10.7k)
Write      | 53.02 MB/s   (13.2k) | 694.63 MB/s  (10.8k)
Total      | 105.97 MB/s  (26.4k) | 1.38 GB/s    (21.6k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.51 GB/s     (2.9k) | 1.78 GB/s     (1.7k)
Write      | 1.59 GB/s     (3.1k) | 1.90 GB/s     (1.8k)
Total      | 3.11 GB/s     (6.0k) | 3.68 GB/s     (3.6k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS17S06)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS17S06)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：加拿大
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：加拿大区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：加拿大区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				Yes (Region: CA)
 Disney+:				Yes (Region: NL)
 Netflix:				Yes (Region: CA)
 YouTube Premium:			Yes (Region: NL)
 Amazon Prime Video:			Yes (Region: NL)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			CA
 Viu.com:				No
 YouTube CDN:				Amsterdam 
 Netflix Preferred CDN:			London  
 Spotify Registration:			No
 Steam Currency:			EUR
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【NL】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：33
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：49
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 03:30:47 北京电信 219.141.136.12  电信163 [普通线路]           
2023/06/27 03:30:47 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 03:30:47 北京移动 221.179.155.161 联通4837[普通线路]           
2023/06/27 03:30:47 上海电信 202.96.209.133  联通9929[优质线路]           
2023/06/27 03:30:47 上海联通 210.22.97.1     联通9929[优质线路]           
2023/06/27 03:30:47 上海移动 211.136.112.200 联通9929[优质线路]           
2023/06/27 03:30:47 广州电信 58.60.188.222   联通9929[优质线路]           
2023/06/27 03:30:47 广州联通 210.21.196.6    联通9929[优质线路]           
2023/06/27 03:30:47 广州移动 120.196.165.24  联通9929[优质线路]           
2023/06/27 03:30:47 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/27 03:30:47 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 03:30:47 成都移动 211.137.96.205  联通4837[普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS3214 xTom GmbH
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
4.96 ms  *  局域网
0.95 ms  *  荷兰, 北荷兰省, 阿姆斯特丹, xtom.com
6.45 ms  *  英国, 伦敦, xtom.com
7.80 ms  AS10099  英国, 伦敦, chinaunicom.com, 联通
20.03 ms  AS10099  英国, 伦敦, chinaunicom.com, 联通
170.82 ms  AS10099  英国, 伦敦, chinaunicom.com, 联通
161.06 ms  *  中国, 北京, chinaunicom.com, 联通
181.33 ms  AS9929  中国, 广东, 广州, chinaunicom.com, 联通
183.52 ms  *  中国, 广东, 广州, chinaunicom.com, 联通
184.09 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
186.91 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
185.28 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
4.94 ms  *  局域网
0.96 ms  *  荷兰, 北荷兰省, 阿姆斯特丹, xtom.com
6.43 ms  *  英国, 伦敦, xtom.com
8.98 ms  AS10099  英国, 伦敦, chinaunicom.com, 联通
19.77 ms  AS10099  英国, 伦敦, chinaunicom.com, 联通
169.59 ms  AS10099  英国, 伦敦, chinaunicom.com, 联通
159.81 ms  *  中国, 北京, chinaunicom.com, 联通
179.98 ms  AS9929  中国, 广东, 广州, chinaunicom.com, 联通
182.07 ms  *  中国, 广东, 广州, chinaunicom.com, 联通
184.35 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
186.80 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
195.23 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.97 ms  *  局域网
1.24 ms  *  荷兰, 北荷兰省, 阿姆斯特丹, xtom.com
6.93 ms  *  英国, 伦敦, xtom.com
9.11 ms  AS10099  英国, 伦敦, chinaunicom.com, 联通
24.05 ms  AS10099  英国, 伦敦, chinaunicom.com, 联通
171.80 ms  AS10099  英国, 伦敦, chinaunicom.com, 联通
151.55 ms  *  中国, 北京, chinaunicom.com, 联通
183.03 ms  AS9929  中国, 广东, 广州, chinaunicom.com, 联通
194.12 ms  *  中国, 广东, 广州, chinaunicom.com, 联通
184.52 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
288.17 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
238.22 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
234.69 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 1600.87 Mbps	 5478.80 Mbps	 1.72	  0.0%
新加坡		 1145.20 Mbps	 582.11 Mbps	 187.69	  0.0%
洛杉矶		 1479.25 Mbps	 1792.74 Mbps	 221.56	  0.0%
联通湖南5G	 517.74 Mbps	 38.44 Mbps	 188.49	  NULL
联通郑州5G	 1130.59 Mbps	 2861.66 Mbps	 174.15	  NULL
电信天津5G	 1431.36 Mbps	 682.37 Mbps	 163.26	  0.0%
电信合肥5G	 467.73 Mbps	 338.01 Mbps	 184.96	  0.0%
移动Beijing	 784.38 Mbps	 1595.74 Mbps	 250.93	  NULL
移动Lanzhou	 682.62 Mbps	 775.83 Mbps	 190.40	  NULL
------------------------------------------------------------------------
```

## 美国洛杉矶DC2

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2399.988 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (304 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 23 min
 负载              : 0.07, 0.02, 0.00
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Los Angeles / US
 地区              : California
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		790 Scores
 2 线程测试(多核)得分: 		1611 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		17003.57 MB/s
 单线程写测试:		12580.96 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		21.7 MB/s (5307 IOPS, 4.82s)		23.7 MB/s (5789 IOPS, 4.42s)
 1GB-1M Block		492 MB/s (469 IOPS, 2.13s)		1.6 GB/s (1499 IOPS, 0.67s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 34.03 MB/s    (8.5k) | 465.22 MB/s   (7.2k)
Write      | 34.13 MB/s    (8.5k) | 467.67 MB/s   (7.3k)
Total      | 68.16 MB/s   (17.0k) | 932.89 MB/s  (14.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.30 GB/s     (2.5k) | 1.29 GB/s     (1.2k)
Write      | 1.37 GB/s     (2.6k) | 1.38 GB/s     (1.3k)
Total      | 2.67 GB/s     (5.2k) | 2.68 GB/s     (2.6k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX31S13)
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
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
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
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
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
scamalytics数据库:
  欺诈分数(越低越好)：56
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：27
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 07:25:13 北京电信 219.141.136.12  电信CN2 [优质线路]           
2023/06/27 07:25:13 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 07:25:13 北京移动 221.179.155.161 电信CN2 [优质线路]           
2023/06/27 07:25:13 上海电信 202.96.209.133  电信CN2 [优质线路]           
2023/06/27 07:25:13 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/27 07:25:13 上海移动 211.136.112.200 电信CN2 [优质线路]           
2023/06/27 07:25:13 广州电信 58.60.188.222   电信CN2 [优质线路]           
2023/06/27 07:25:13 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/27 07:25:13 广州移动 120.196.165.24  电信CN2 [优质线路]           
2023/06/27 07:25:13 成都电信 61.139.2.69     电信CN2 [优质线路]           
2023/06/27 07:25:13 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 07:25:13 成都移动 211.137.96.205  电信CN2 [优质线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks Inc
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.73 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
0.28 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
0.41 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
26.72 ms  AS4134  美国, 加利福尼亚州, 洛杉矶, chinatelecom.com.cn, 电信
210.62 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
187.93 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
212.91 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
210.28 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.78 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
0.46 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
18.87 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
0.90 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
7.83 ms  AS19174  美国, 加利福尼亚州, 洛杉矶, chinaunicom.com, 联通
200.24 ms  AS4837  中国, 北京, chinaunicom.com, 联通
206.58 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
185.92 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
193.03 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
205.73 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
202.90 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.87 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
0.59 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
52.89 ms  AS4134  美国, 加利福尼亚州, 洛杉矶, chinatelecom.com.cn, 电信
185.48 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
179.86 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
202.26 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
234.45 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
233.04 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
256.31 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
260.48 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 849.14 Mbps	 932.68 Mbps	 0.43	  0.0%
洛杉矶		 885.19 Mbps	 892.24 Mbps	 1.09	  0.0%
日本东京	 793.95 Mbps	 661.24 Mbps	 236.72	  0.0%
联通WuXi	 374.10 Mbps	 630.01 Mbps	 181.08	  0.0%
联通Fuzhou	 394.81 Mbps	 490.52 Mbps	 179.45	  0.0%
电信上海	 70.83 Mbps	 35.07 Mbps	 133.12	  NULL
电信武汉	 39.33 Mbps	 430.54 Mbps	 172.11	  NULL
移动Beijing	 555.13 Mbps	 533.75 Mbps	 186.63	  NULL
移动杭州5G	 69.17 Mbps	 870.61 Mbps	 257.99	  7.1%
------------------------------------------------------------------------
```

## 美国洛杉矶DC3

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2599.994 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (311 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 5 min
 负载              : 0.21, 0.05, 0.02
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Los Angeles / US
 地区              : California
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		615 Scores
 2 线程测试(多核)得分: 		1262 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		13331.34 MB/s
 单线程写测试:		11517.99 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		14.9 MB/s (3635 IOPS, 7.04s)		18.7 MB/s (4566 IOPS, 5.61s)
 1GB-1M Block		339 MB/s (324 IOPS, 3.09s)		1.2 GB/s (1117 IOPS, 0.90s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 40.96 MB/s   (10.2k) | 471.51 MB/s   (7.3k)
Write      | 41.04 MB/s   (10.2k) | 473.99 MB/s   (7.4k)
Total      | 82.00 MB/s   (20.5k) | 945.51 MB/s  (14.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.03 GB/s     (2.0k) | 1.15 GB/s     (1.1k)
Write      | 1.08 GB/s     (2.1k) | 1.22 GB/s     (1.2k)
Total      | 2.12 GB/s     (4.1k) | 2.38 GB/s     (2.3k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX31S13)
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
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
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
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
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
scamalytics数据库:
  欺诈分数(越低越好)：56
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：0
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 06:50:36 北京电信 219.141.136.12  电信CN2 [优质线路]           
2023/06/27 06:50:36 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 06:50:36 北京移动 221.179.155.161 联通4837[普通线路]           
2023/06/27 06:50:36 上海电信 202.96.209.133  电信CN2 [优质线路]           
2023/06/27 06:50:36 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/27 06:50:36 上海移动 211.136.112.200 联通4837[普通线路]           
2023/06/27 06:50:36 广州电信 58.60.188.222   电信CN2 [优质线路]           
2023/06/27 06:50:36 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/27 06:50:36 广州移动 120.196.165.24  联通4837[普通线路]           
2023/06/27 06:50:36 成都电信 61.139.2.69     电信CN2 [优质线路]           
2023/06/27 06:50:36 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 06:50:36 成都移动 211.137.96.205  联通4837[普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
1.24 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
1.16 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
12.64 ms  AS4134  美国, 加利福尼亚州, 洛杉矶, chinatelecom.com.cn, 电信
167.75 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
179.53 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
201.58 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.87 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
0.48 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
1.45 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
3.88 ms  AS19174  美国, 加利福尼亚州, 洛杉矶, chinaunicom.com, 联通
154.54 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
164.10 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
159.55 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
157.39 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
166.79 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
2.20 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
6.79 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
0.93 ms  AS8100  美国, 加利福尼亚州, 洛杉矶, quadranet.com
1.75 ms  AS19174  美国, 加利福尼亚州, 洛杉矶, chinaunicom.com, 联通
179.18 ms  AS4837  中国, 北京, chinaunicom.com, 联通
156.88 ms  AS4837  中国, 北京, chinaunicom.com, 联通
176.05 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
209.78 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
208.74 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
208.75 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
206.58 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 737.54 Mbps	 664.96 Mbps	 0.45	  0.0%
洛杉矶		 711.99 Mbps	 610.22 Mbps	 1.46	  0.0%
日本东京	 627.51 Mbps	 51.38 Mbps	 231.68	  0.0%
联通湖南5G	 496.59 Mbps	 9.80 Mbps	 181.62	  NULL
联通郑州5G	 551.44 Mbps	 517.05 Mbps	 189.54	  NULL
电信上海	 67.66 Mbps	 11.49 Mbps	 179.68	  NULL
电信合肥5G	 170.95 Mbps	 16.70 Mbps	 200.67	  7.4%
移动Zhengzhou5G	 120.79 Mbps	 5.70 Mbps	 194.78	  0.0%
移动Beijing	 511.93 Mbps	 576.28 Mbps	 196.36	  NULL
------------------------------------------------------------------------
```

## 美国洛杉矶DC4

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2399.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (300 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 3 min
 负载              : 0.00, 0.00, 0.00
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Los Angeles / US
 地区              : California
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		756 Scores
 2 线程测试(多核)得分: 		1537 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		16788.16 MB/s
 单线程写测试:		12155.59 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		17.0 MB/s (4160 IOPS, 6.15s)		19.3 MB/s (4712 IOPS, 5.43s)
 1GB-1M Block		267 MB/s (255 IOPS, 3.92s)		871 MB/s (830 IOPS, 1.20s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 37.07 MB/s    (9.2k) | 269.95 MB/s   (4.2k)
Write      | 37.17 MB/s    (9.2k) | 271.38 MB/s   (4.2k)
Total      | 74.24 MB/s   (18.5k) | 541.33 MB/s   (8.4k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 143.29 MB/s    (279) | 170.15 MB/s    (166)
Write      | 150.91 MB/s    (294) | 181.48 MB/s    (177)
Total      | 294.21 MB/s    (573) | 351.63 MB/s    (343)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX31S13)
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
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
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
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
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
scamalytics数据库:
  欺诈分数(越低越好)：56
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：6
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 07:39:59 北京电信 219.141.136.12  电信163 [普通线路]           
2023/06/27 07:39:59 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 07:39:59 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/27 07:39:59 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/27 07:39:59 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/27 07:39:59 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/27 07:39:59 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/27 07:39:59 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/27 07:39:59 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/27 07:39:59 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/27 07:39:59 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 07:39:59 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 Cluster Logic Inc
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.98 ms  *  局域网
0.61 ms  AS35916  美国, 加利福尼亚州, 洛杉矶, multacom.com
0.80 ms  AS35916  美国, 加利福尼亚州, 洛杉矶, multacom.com
0.53 ms  AS209  美国, 加利福尼亚州, 洛杉矶, centurylink.com
0.59 ms  AS209  美国, 加利福尼亚州, 洛杉矶, centurylink.com
10.48 ms  AS3356  美国, 加利福尼亚州, 圣何塞, level3.com
154.01 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
155.70 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
167.67 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
180.53 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
169.34 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
1.57 ms  *  局域网
0.71 ms  AS35916  美国, 加利福尼亚州, 洛杉矶, multacom.com
0.88 ms  AS35916  美国, 加利福尼亚州, 洛杉矶, multacom.com
1.10 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
1.40 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
2.06 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
157.52 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
162.71 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
157.02 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
163.40 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
166.47 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.89 ms  *  局域网
0.38 ms  AS35916  美国, 加利福尼亚州, 洛杉矶, multacom.com
2.94 ms  AS35916  美国, 加利福尼亚州, 洛杉矶, multacom.com
1.20 ms  AS9009  美国, 加利福尼亚州, 洛杉矶, coresite.com
1.23 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
189.76 ms  AS58453  中国, 上海, chinamobile.com, 移动
196.88 ms  AS9808  中国, 上海, chinamobile.com, 移动
208.23 ms  AS9808  中国, 上海, chinamobile.com, 移动
209.04 ms  AS9808  中国, 北京, chinamobile.com, 移动
208.06 ms  AS9808  中国, 北京, chinamobile.com, 移动
209.82 ms  AS9808  中国, 北京, chinamobile.com, 移动
209.57 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 919.97 Mbps	 918.53 Mbps	 0.47	  0.0%
洛杉矶		 924.70 Mbps	 934.82 Mbps	 0.83	  0.0%
日本东京	 844.52 Mbps	 808.51 Mbps	 105.41	  0.0%
联通湖南5G	 543.40 Mbps	 236.59 Mbps	 172.06	  NULL
联通沈阳	 149.88 Mbps	 364.20 Mbps	 175.04	  0.0%
电信上海	 8.12 Mbps	 442.19 Mbps	 165.24	  NULL
电信Suzhou5G	 647.17 Mbps	 600.65 Mbps	 147.83	  NULL
移动Chengdu	 607.93 Mbps	 808.48 Mbps	 194.31	  0.0%
移动杭州5G	 285.94 Mbps	 683.40 Mbps	 215.58	  0.0%
------------------------------------------------------------------------
```

## 美国洛杉矶DC6 CN2GIA-E

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2599.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (279 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 1 min
 负载              : 0.31, 0.10, 0.03
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Los Angeles / US
 地区              : California
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		629 Scores
 2 线程测试(多核)得分: 		1255 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		13017.15 MB/s
 单线程写测试:		11450.24 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		11.3 MB/s (2762 IOPS, 9.27s)		13.1 MB/s (3186 IOPS, 8.03s)
 1GB-1M Block		206 MB/s (196 IOPS, 5.10s)		696 MB/s (663 IOPS, 1.51s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 32.67 MB/s    (8.1k) | 312.27 MB/s   (4.8k)
Write      | 32.73 MB/s    (8.1k) | 313.92 MB/s   (4.9k)
Total      | 65.41 MB/s   (16.3k) | 626.20 MB/s   (9.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 609.81 MB/s   (1.1k) | 722.52 MB/s    (705)
Write      | 642.21 MB/s   (1.2k) | 770.64 MB/s    (752)
Total      | 1.25 GB/s     (2.4k) | 1.49 GB/s     (1.4k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX31S13)
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
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
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
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
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
scamalytics数据库:
  欺诈分数(越低越好)：46
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：32
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 04:25:17 北京电信 219.141.136.12  电信CN2 [优质线路]           
2023/06/27 04:25:17 北京联通 202.106.50.1    电信CN2 [优质线路]           
2023/06/27 04:25:17 北京移动 221.179.155.161 电信CN2 [优质线路]           
2023/06/27 04:25:17 上海电信 202.96.209.133  电信CN2 [优质线路]           
2023/06/27 04:25:17 上海联通 210.22.97.1     电信CN2 [优质线路]           
2023/06/27 04:25:17 上海移动 211.136.112.200 电信CN2 [优质线路]           
2023/06/27 04:25:17 广州电信 58.60.188.222   电信CN2 [优质线路]           
2023/06/27 04:25:17 广州联通 210.21.196.6    电信CN2 [优质线路]           
2023/06/27 04:25:17 广州移动 120.196.165.24  电信CN2 [优质线路]           
2023/06/27 04:25:17 成都电信 61.139.2.69     电信CN2 [优质线路]           
2023/06/27 04:25:17 成都联通 119.6.6.6       电信CN2 [优质线路]           
2023/06/27 04:25:17 成都移动 211.137.96.205  电信CN2 [优质线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS21887 IT7 Networks Inc
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
22.86 ms  *  局域网
0.99 ms  AS4134  美国, chinatelecom.com.cn, 电信
151.50 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
153.09 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
155.00 ms  *  中国, 广东, 深圳, chinatelecom.com.cn, 电信
157.53 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
154.40 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
974.84 ms  *  局域网
61.41 ms  *  局域网
0.73 ms  AS4134  美国, chinatelecom.com.cn, 电信
144.96 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
152.32 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
153.66 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
163.20 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
156.19 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
58.53 ms  *  局域网
0.49 ms  AS906  美国, 加利福尼亚州, 洛杉矶, dmit.io
0.81 ms  AS906  美国, 加利福尼亚州, 洛杉矶, dmit.io
151.70 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
153.00 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
154.26 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
197.52 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
187.82 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
192.67 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
192.42 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
193.15 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 703.77 Mbps	 3962.24 Mbps	 0.46	  NULL
洛杉矶		 875.06 Mbps	 4019.35 Mbps	 0.88	  0.0%
日本东京	 660.69 Mbps	 3536.21 Mbps	 118.70	  0.0%
联通WuXi	 14.97 Mbps	 343.87 Mbps	 132.77	  0.0%
联通上海5G	 674.95 Mbps	 1879.62 Mbps	 130.64	  0.0%
电信上海	 398.87 Mbps	 86.96 Mbps	 128.55	  NULL
电信Zhenjiang5G	 532.84 Mbps	 1438.97 Mbps	 133.92	  NULL
移动Beijing	 529.53 Mbps	 958.76 Mbps	 173.20	  NULL
移动Zhengzhou5G	 422.09 Mbps	 75.84 Mbps	 184.15	  0.0%
------------------------------------------------------------------------
```

## 美国洛杉矶DC8

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2599.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (285 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 0 min
 负载              : 0.73, 0.17, 0.06
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Los Angeles / US
 地区              : California
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		621 Scores
 2 线程测试(多核)得分: 		1228 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		13060.11 MB/s
 单线程写测试:		11254.79 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		12.6 MB/s (3079 IOPS, 8.31s)		15.0 MB/s (3651 IOPS, 7.01s)
 1GB-1M Block		297 MB/s (284 IOPS, 3.53s)		852 MB/s (812 IOPS, 1.23s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 32.49 MB/s    (8.1k) | 306.10 MB/s   (4.7k)
Write      | 32.55 MB/s    (8.1k) | 307.72 MB/s   (4.8k)
Total      | 65.04 MB/s   (16.2k) | 613.82 MB/s   (9.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 488.14 MB/s    (953) | 676.07 MB/s    (660)
Write      | 514.07 MB/s   (1.0k) | 721.09 MB/s    (704)
Total      | 1.00 GB/s     (1.9k) | 1.39 GB/s     (1.3k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX31S13)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX17S56)
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
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
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
scamalytics数据库:
  欺诈分数(越低越好)：46
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：15
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 07:50:02 北京电信 219.141.136.12  测试超时
2023/06/27 07:50:02 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 07:50:02 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/27 07:50:02 上海电信 202.96.209.133  测试超时
2023/06/27 07:50:02 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/27 07:50:02 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/27 07:50:02 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/27 07:50:02 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/27 07:50:02 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/27 07:50:02 成都电信 61.139.2.69     测试超时
2023/06/27 07:50:02 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 07:50:02 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks Inc
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
3.94 ms  AS21859  美国, 加利福尼亚州, 洛杉矶, zenlayer.com
0.47 ms  AS21859  美国, 加利福尼亚州, 洛杉矶, zenlayer.com
4.64 ms  AS4134  美国, 加利福尼亚州, 洛杉矶, chinatelecom.com.cn, 电信
164.67 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
178.98 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
161.53 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
177.80 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
6.22 ms  AS21859  美国, 加利福尼亚州, 洛杉矶, zenlayer.com
0.61 ms  AS21859  美国, 加利福尼亚州, 洛杉矶, zenlayer.com
0.81 ms  AS21859  美国, 加利福尼亚州, 洛杉矶, zenlayer.com
2.55 ms  AS4837  美国, 加利福尼亚州, 洛杉矶, chinaunicom.com, 联通
151.57 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
162.91 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
160.82 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
157.41 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
8.81 ms  AS21859  美国, 加利福尼亚州, 洛杉矶, zenlayer.com
0.69 ms  AS21859  美国, 加利福尼亚州, 洛杉矶, zenlayer.com
0.55 ms  AS4229,AS21859  美国, 加利福尼亚州, 洛杉矶, zenlayer.com
0.71 ms  AS4229,AS21859  美国, 加利福尼亚州, 洛杉矶, zenlayer.com
1.40 ms  AS4229,AS21859  美国, 加利福尼亚州, 洛杉矶, zenlayer.com
1.37 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
1.68 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
182.36 ms  AS9808  中国, 上海, chinamobile.com, 移动
202.89 ms  AS9808  中国, 北京, chinamobile.com, 移动
195.83 ms  AS9808  中国, 北京, chinamobile.com, 移动
205.60 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 696.73 Mbps	 939.86 Mbps	 0.41	  NULL
洛杉矶		 726.49 Mbps	 911.02 Mbps	 1.38	  0.0%
日本东京	 686.59 Mbps	 706.30 Mbps	 122.79	  0.0%
联通湖南5G	 473.95 Mbps	 367.66 Mbps	 176.10	  NULL
联通Fuzhou	 505.38 Mbps	 672.55 Mbps	 181.29	  0.0%
电信Suzhou5G	 644.75 Mbps	 588.40 Mbps	 137.56	  NULL
移动Beijing	 620.81 Mbps	 603.86 Mbps	 185.02	  NULL
移动Chengdu	 631.22 Mbps	 899.55 Mbps	 208.52	  0.0%
------------------------------------------------------------------------
```

## 美国洛杉矶DC9(CN2-GIA)

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2599.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (290 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 0 min
 负载              : 0.07, 0.02, 0.00
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Los Angeles / US
 地区              : California
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		713 Scores
 2 线程测试(多核)得分: 		1406 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		15240.27 MB/s
 单线程写测试:		13252.59 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		16.2 MB/s (3964 IOPS, 6.46s)		19.5 MB/s (4759 IOPS, 5.38s)
 1GB-1M Block		316 MB/s (302 IOPS, 3.32s)		1.0 GB/s (1000 IOPS, 1.00s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 37.44 MB/s    (9.3k) | 333.48 MB/s   (5.2k)
Write      | 37.54 MB/s    (9.3k) | 335.24 MB/s   (5.2k)
Total      | 74.98 MB/s   (18.7k) | 668.73 MB/s  (10.4k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 757.46 MB/s   (1.4k) | 792.18 MB/s    (773)
Write      | 797.71 MB/s   (1.5k) | 844.93 MB/s    (825)
Total      | 1.55 GB/s     (3.0k) | 1.63 GB/s     (1.5k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  洛杉机(LAX31S13)
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
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
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
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
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
 Tiktok Region:		Failed
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：46
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：51
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 04:13:31 北京电信 219.141.136.12  电信CN2 [优质线路]           
2023/06/27 04:13:31 北京联通 202.106.50.1    电信CN2 [优质线路]           
2023/06/27 04:13:31 北京移动 221.179.155.161 电信CN2 [优质线路]           
2023/06/27 04:13:31 上海电信 202.96.209.133  电信CN2 [优质线路]           
2023/06/27 04:13:31 上海联通 210.22.97.1     电信CN2 [优质线路]           
2023/06/27 04:13:31 上海移动 211.136.112.200 电信CN2 [优质线路]           
2023/06/27 04:13:31 广州电信 58.60.188.222   电信CN2 [优质线路]           
2023/06/27 04:13:31 广州联通 210.21.196.6    电信CN2 [优质线路]           
2023/06/27 04:13:31 广州移动 120.196.165.24  电信CN2 [优质线路]           
2023/06/27 04:13:31 成都电信 61.139.2.69     电信CN2 [优质线路]           
2023/06/27 04:13:31 成都联通 119.6.6.6       电信CN2 [优质线路]           
2023/06/27 04:13:31 成都移动 211.137.96.205  电信CN2 [优质线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.65 ms  AS4134  美国, 加利福尼亚州, 洛杉矶, chinatelecom.com.cn, 电信
144.93 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
146.44 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
148.31 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
156.53 ms  *  中国, 广东, 深圳, chinatelecom.com.cn, 电信
156.58 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
154.89 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
1.44 ms  AS4134  美国, chinatelecom.com.cn, 电信
145.12 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
149.94 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
158.93 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
157.37 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
1.11 ms  AS4134  美国, 加利福尼亚州, 洛杉矶, chinatelecom.com.cn, 电信
150.28 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
157.89 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
196.45 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
199.67 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
198.16 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 776.91 Mbps	 1693.93 Mbps	 0.51	  0.0%
洛杉矶		 794.00 Mbps	 861.64 Mbps	 1.37	  0.0%
中国香港	 695.98 Mbps	 711.82 Mbps	 149.58	  NULL
联通上海5G	 674.95 Mbps	 810.81 Mbps	 128.20	  0.0%
电信上海	 468.21 Mbps	 747.64 Mbps	 128.15	  NULL
电信Zhenjiang5G	 630.82 Mbps	 621.58 Mbps	 133.19	  NULL
移动Beijing	 664.38 Mbps	 661.33 Mbps	 172.82	  NULL
移动杭州5G	 338.99 Mbps	 933.81 Mbps	 184.60	  0.0%
------------------------------------------------------------------------
```

## 加拿大温哥华

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2599.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (302 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 0 min
 负载              : 0.12, 0.03, 0.01
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Vancouver / CA
 地区              : British Columbia
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		717 Scores
 2 线程测试(多核)得分: 		1441 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		15245.90 MB/s
 单线程写测试:		13299.40 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		17.8 MB/s (4338 IOPS, 5.90s)		21.3 MB/s (5196 IOPS, 4.93s)
 1GB-1M Block		408 MB/s (389 IOPS, 2.57s)		1.4 GB/s (1292 IOPS, 0.77s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 41.84 MB/s   (10.4k) | 489.84 MB/s   (7.6k)
Write      | 41.93 MB/s   (10.4k) | 492.42 MB/s   (7.6k)
Total      | 83.77 MB/s   (20.9k) | 982.27 MB/s  (15.3k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.00 GB/s     (1.9k) | 1.22 GB/s     (1.1k)
Write      | 1.05 GB/s     (2.0k) | 1.30 GB/s     (1.2k)
Total      | 2.06 GB/s     (4.0k) | 2.52 GB/s     (2.4k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA30S12)
Youtube识别地域: 加拿大(CA)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  西雅图(SEA30S12)
Youtube识别地域: 加拿大(CA)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：加拿大
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：加拿大区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：加拿大区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: CA)
 Amazon Prime Video:			Yes (Region: CA)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			CA
 Viu.com:				No
 YouTube CDN:				Seattle, WA 
 Netflix Preferred CDN:			Seattle, WA  
 Spotify Registration:			No
 Steam Currency:			CAD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【CA】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：46
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：28
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 01:15:29 北京电信 219.141.136.12  电信163 [普通线路]           
2023/06/27 01:15:29 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 01:15:29 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/27 01:15:29 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/27 01:15:29 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/27 01:15:29 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/27 01:15:29 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/27 01:15:29 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/27 01:15:29 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/27 01:15:29 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/27 01:15:29 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 01:15:29 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks Inc
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
17.85 ms  *  局域网
24.80 ms  AS54527  加拿大, 不列颠哥伦比亚省, 温哥华, astuteinternet.com
0.51 ms  AS54527  加拿大, 不列颠哥伦比亚省, 温哥华, astuteinternet.com
0.56 ms  AS54527  加拿大, 不列颠哥伦比亚省, 温哥华, astuteinternet.com
2.76 ms  AS6327  加拿大, 不列颠哥伦比亚省, 温哥华, shaw.ca
6.21 ms  AS6327  美国, 华盛顿州, 西雅图, shaw.ca
41.63 ms  AS6327  美国, 加利福尼亚州, 圣何塞, shaw.ca
46.06 ms  AS4134  美国, 加利福尼亚州, 圣何塞, chinatelecom.com.cn, 电信
192.67 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
205.99 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
208.92 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
212.28 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
18.11 ms  *  局域网
17.01 ms  AS54527  加拿大, 不列颠哥伦比亚省, 温哥华, astuteinternet.com
0.50 ms  AS54527  加拿大, 不列颠哥伦比亚省, 温哥华, astuteinternet.com
0.53 ms  AS54527  加拿大, 不列颠哥伦比亚省, 温哥华, astuteinternet.com
1.63 ms  AS6327  加拿大, 不列颠哥伦比亚省, 温哥华, shaw.ca
6.40 ms  AS6327  美国, 华盛顿州, 西雅图, shaw.ca
41.78 ms  AS6327  美国, 加利福尼亚州, 圣何塞, shaw.ca
217.97 ms  AS4837  美国, 加利福尼亚州, 圣何塞, chinaunicom.com, 联通
214.00 ms  AS4837  中国, 北京, chinaunicom.com, 联通
210.21 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
212.27 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
222.63 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
223.10 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
19.72 ms  *  局域网
12.92 ms  AS54527  加拿大, 不列颠哥伦比亚省, 温哥华, astuteinternet.com
0.49 ms  AS54527  加拿大, 不列颠哥伦比亚省, 温哥华, astuteinternet.com
0.54 ms  AS54527  加拿大, 不列颠哥伦比亚省, 温哥华, astuteinternet.com
1.46 ms  AS6327  加拿大, 不列颠哥伦比亚省, 温哥华, shaw.ca
6.72 ms  AS6327  美国, 华盛顿州, 西雅图, shaw.ca
5.75 ms  AS6327  美国, 华盛顿州, 西雅图, shaw.ca
5.22 ms  AS58453  美国, 华盛顿州, 西雅图, chinamobile.com, 移动
9.07 ms  AS58453  美国, chinamobile.com, 移动
192.61 ms  AS9808  中国, 上海, chinamobile.com, 移动
197.87 ms  AS9808  中国, 上海, chinamobile.com, 移动
191.27 ms  AS9808  中国, 上海, chinamobile.com, 移动
191.95 ms  AS9808  中国, 北京, chinamobile.com, 移动
205.98 ms  AS9808  中国, 北京, chinamobile.com, 移动
209.13 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 1743.69 Mbps	 7133.59 Mbps	 0.57	  0.0%
洛杉矶		 1860.56 Mbps	 5364.67 Mbps	 29.49	  0.0%
日本东京	 1879.88 Mbps	 4266.86 Mbps	 88.52	  0.0%
联通湖南5G	 429.95 Mbps	 359.91 Mbps	 219.75	  NULL
联通Fuzhou	 426.93 Mbps	 2758.99 Mbps	 223.81	  0.0%
电信Suzhou5G	 947.08 Mbps	 786.80 Mbps	 181.54	  NULL
移动Beijing	 1008.89 Mbps	 1704.42 Mbps	 180.20	  NULL
移动Chengdu	 912.44 Mbps	 2142.02 Mbps	 215.87	  0.0%
------------------------------------------------------------------------
```

## 加拿大温哥华（CN2GIA）

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2399.988 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (311 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 3 min
 负载              : 0.16, 0.06, 0.02
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS6233 xTom
 位置              : Vancouver / CA
 地区              : British Columbia
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		823 Scores
 2 线程测试(多核)得分: 		1642 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		18031.82 MB/s
 单线程写测试:		13935.62 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		23.2 MB/s (5655 IOPS, 4.53s)		25.2 MB/s (6160 IOPS, 4.16s)
 1GB-1M Block		520 MB/s (496 IOPS, 2.02s)		1.4 GB/s (1342 IOPS, 0.74s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 28.01 MB/s    (7.0k) | 348.60 MB/s   (5.4k)
Write      | 28.03 MB/s    (7.0k) | 350.44 MB/s   (5.4k)
Total      | 56.05 MB/s   (14.0k) | 699.05 MB/s  (10.9k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 909.96 MB/s   (1.7k) | 940.05 MB/s    (918)
Write      | 958.31 MB/s   (1.8k) | 1.00 GB/s      (979)
Total      | 1.86 GB/s     (3.6k) | 1.94 GB/s     (1.8k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  旧金山(SFO03S20)
Youtube识别地域: 加拿大(CA)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  旧金山(SFO03S20)
Youtube识别地域: 加拿大(CA)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：加拿大
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：加拿大区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：加拿大区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: CA)
 Amazon Prime Video:			Yes (Region: CA)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			CA
 Viu.com:				No
 YouTube CDN:				San Francisco, CA 
 Netflix Preferred CDN:			San Jose, CA  
 Spotify Registration:			No
 Steam Currency:			CAD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【CA】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：56
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：47
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 01:05:01 北京电信 219.141.136.12  电信CN2 [优质线路]           
2023/06/27 01:05:01 北京联通 202.106.50.1    联通9929[优质线路]           
2023/06/27 01:05:01 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/27 01:05:01 上海电信 202.96.209.133  电信CN2 [优质线路]           
2023/06/27 01:05:01 上海联通 210.22.97.1     联通9929[优质线路]           
2023/06/27 01:05:01 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/27 01:05:01 广州电信 58.60.188.222   电信CN2 [优质线路]           
2023/06/27 01:05:01 广州联通 210.21.196.6    联通9929[优质线路]           
2023/06/27 01:05:01 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/27 01:05:01 成都电信 61.139.2.69     电信CN2 [优质线路]           
2023/06/27 01:05:01 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 01:05:01 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS6233 Cluster Logic Inc
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
15.53 ms  *  局域网
35.92 ms  *  局域网
20.80 ms  AS6233  美国, 加利福尼亚州, 圣何塞, xtom.com
21.04 ms  AS4134  美国, 加利福尼亚州, 圣何塞, chinatelecom.com.cn, 电信
178.00 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
179.57 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
185.50 ms  *  中国, 广东, 广州, chinatelecom.com.cn, 电信
184.15 ms  *  中国, 广东, 深圳, chinatelecom.com.cn, 电信
183.65 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
182.13 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
11.45 ms  *  局域网
31.87 ms  *  局域网
28.30 ms  AS6233  美国, 加利福尼亚州, 圣何塞, xtom.com
21.40 ms  AS10099  美国, 加利福尼亚州, 圣何塞, chinaunicom.com, 联通
150.44 ms  AS10099  美国, chinaunicom.com, 联通
153.03 ms  *  中国, 上海, chinaunicom.com, 联通
179.44 ms  AS9929  中国, 广东, 广州, chinaunicom.com, 联通
179.51 ms  *  中国, 广东, 广州, chinaunicom.com, 联通
183.44 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
179.74 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
187.53 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
7.30 ms  *  局域网
37.23 ms  *  局域网
20.82 ms  AS6233  美国, 加利福尼亚州, 圣何塞, xtom.com
21.34 ms  AS58453  美国, 加利福尼亚州, 圣何塞, chinamobile.com, 移动
21.06 ms  AS58453  美国, 加利福尼亚州, 圣何塞, chinamobile.com, 移动
203.66 ms  AS58453  中国, 上海, chinamobile.com, 移动
214.63 ms  AS9808  中国, 上海, chinamobile.com, 移动
217.48 ms  AS9808  中国, 北京, chinamobile.com, 移动
218.22 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 7790.03 Mbps	 8511.31 Mbps	 0.69	  NULL
洛杉矶		 6222.02 Mbps	 4296.87 Mbps	 29.62	  0.0%
日本东京	 2926.89 Mbps	 7458.35 Mbps	 89.53	  0.0%
联通湖南5G	 17.43 Mbps	 505.91 Mbps	 173.75	  NULL
电信上海	 26.70 Mbps	 983.40 Mbps	 152.62	  NULL
电信Suzhou5G	 28.12 Mbps	 1394.64 Mbps	 148.89	  NULL
移动Chengdu	 54.84 Mbps	 2353.13 Mbps	 221.75	  1.7%
移动杭州5G	 24.20 Mbps	 3306.77 Mbps	 212.70	  2.3%
------------------------------------------------------------------------
```

## 美国加弗里蒙特 \[USCA\_FMT\]

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2599.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (317 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 1 hour 4 min
 负载              : 0.14, 0.04, 0.01
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Fremont / US
 地区              : California
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		568 Scores
 2 线程测试(多核)得分: 		1133 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		11963.29 MB/s
 单线程写测试:		10035.08 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		9.5 MB/s (2310 IOPS, 11.08s)		9.6 MB/s (2336 IOPS, 10.95s)
 1GB-1M Block		245 MB/s (233 IOPS, 4.29s)		734 MB/s (699 IOPS, 1.43s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 26.09 MB/s    (6.5k) | 303.79 MB/s   (4.7k)
Write      | 26.12 MB/s    (6.5k) | 305.39 MB/s   (4.7k)
Total      | 52.21 MB/s   (13.0k) | 609.19 MB/s   (9.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 776.46 MB/s   (1.5k) | 943.54 MB/s    (921)
Write      | 817.72 MB/s   (1.5k) | 1.00 GB/s      (982)
Total      | 1.59 GB/s     (3.1k) | 1.94 GB/s     (1.9k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: NUQ(NUQ04S38)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: NUQ(NUQ04S38)
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
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				San Jose, CA 
 Netflix Preferred CDN:			San Jose, CA  
 Spotify Registration:			No
 Steam Currency:			USD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：46
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：36
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 05:51:22 北京电信 219.141.136.12  电信163 [普通线路]           
2023/06/27 05:51:22 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 05:51:22 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/27 05:51:22 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/27 05:51:22 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/27 05:51:22 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/27 05:51:22 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/27 05:51:22 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/27 05:51:22 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/27 05:51:22 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/27 05:51:22 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 05:51:22 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks Inc
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
1.09 ms  *  局域网
0.72 ms  AS6939  美国, 加利福尼亚州, 费利蒙, he.net
3.59 ms  AS6939  美国, 加利福尼亚州, 圣何塞, he.net
172.22 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
163.40 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
1.45 ms  *  局域网
3.40 ms  AS6939  美国, 加利福尼亚州, 费利蒙, he.net
198.35 ms  AS6939  美国, 加利福尼亚州, 洛杉矶, he.net
184.86 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
191.28 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
195.33 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
203.53 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
168.33 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
13.19 ms  *  局域网
2.01 ms  AS6939  美国, 加利福尼亚州, 费利蒙, he.net
1.46 ms  AS6939  美国, 加利福尼亚州, 圣何塞, he.net
1.52 ms  AS58453  美国, 加利福尼亚州, 圣何塞, chinamobile.com, 移动
184.70 ms  AS58453  中国, 上海, chinamobile.com, 移动
183.78 ms  AS9808  中国, 上海, chinamobile.com, 移动
182.79 ms  AS9808  中国, 上海, chinamobile.com, 移动
196.91 ms  AS9808  中国, 北京, chinamobile.com, 移动
198.33 ms  AS9808  中国, 北京, chinamobile.com, 移动
197.58 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 475.26 Mbps	 493.17 Mbps	 1.43	  0.0%
洛杉矶		 453.59 Mbps	 268.03 Mbps	 10.21	  0.0%
日本东京	 472.25 Mbps	 263.21 Mbps	 108.77	  0.0%
联通郑州5G	 449.86 Mbps	 519.82 Mbps	 165.18	  NULL
联通湖南5G	 274.70 Mbps	 21.50 Mbps	 207.70	  NULL
电信上海	 153.86 Mbps	 215.43 Mbps	 149.16	  NULL
电信Suzhou5G	 406.61 Mbps	 241.85 Mbps	 154.15	  NULL
移动Beijing	 420.05 Mbps	 454.09 Mbps	 187.71	  NULL
------------------------------------------------------------------------
```

## 美国弗里蒙特（三网直连，已经取消4837）

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2599.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (285 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 0 min
 负载              : 0.15, 0.03, 0.01
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS25820 IT7 Networks Inc
 位置              : Fremont / US
 地区              : California
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		641 Scores
 2 线程测试(多核)得分: 		1280 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		13546.78 MB/s
 单线程写测试:		11921.39 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		16.5 MB/s (4028 IOPS, 6.36s)		21.7 MB/s (5309 IOPS, 4.82s)
 1GB-1M Block		351 MB/s (334 IOPS, 2.99s)		860 MB/s (820 IOPS, 1.22s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 40.82 MB/s   (10.2k) | 425.99 MB/s   (6.6k)
Write      | 40.90 MB/s   (10.2k) | 428.23 MB/s   (6.6k)
Total      | 81.72 MB/s   (20.4k) | 854.23 MB/s  (13.3k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 770.02 MB/s   (1.5k) | 933.99 MB/s    (912)
Write      | 810.94 MB/s   (1.5k) | 996.19 MB/s    (972)
Total      | 1.58 GB/s     (3.0k) | 1.93 GB/s     (1.8k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  旧金山(SFO03S20)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  旧金山(SFO03S20)
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
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				San Jose, CA 
 Netflix Preferred CDN:			San Jose, CA  
 Spotify Registration:			No
 Steam Currency:			USD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：56
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：28
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 04:36:38 北京电信 219.141.136.12  电信163 [普通线路]           
2023/06/27 04:36:38 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 04:36:38 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/27 04:36:38 上海电信 202.96.209.133  测试超时
2023/06/27 04:36:38 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/27 04:36:38 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/27 04:36:38 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/27 04:36:38 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/27 04:36:38 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/27 04:36:38 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/27 04:36:38 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 04:36:38 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS25820 IT7 Networks
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
18.81 ms  *  局域网
0.99 ms  *  局域网
0.51 ms  AS6939  美国, 加利福尼亚州, 费利蒙, he.net
2.41 ms  AS6939  美国, 加利福尼亚州, 圣何塞, he.net
161.16 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
157.24 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
173.84 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
13.77 ms  *  局域网
1.76 ms  *  局域网
0.48 ms  AS6939  美国, 加利福尼亚州, 费利蒙, he.net
168.78 ms  AS6939  美国, 加利福尼亚州, 洛杉矶, he.net
169.78 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
168.94 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
178.65 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
165.19 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
166.61 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
15.71 ms  *  局域网
1.99 ms  *  局域网
35.54 ms  AS6939  美国, 加利福尼亚州, 费利蒙, he.net
156.01 ms  AS6939  美国, 加利福尼亚州, 圣何塞, he.net
155.87 ms  AS58453  美国, 加利福尼亚州, 圣何塞, chinamobile.com, 移动
215.90 ms  AS58453  中国, 上海, chinamobile.com, 移动
213.56 ms  AS9808  中国, 上海, chinamobile.com, 移动
215.84 ms  AS9808  中国, 上海, chinamobile.com, 移动
240.47 ms  AS9808  中国, 北京, chinamobile.com, 移动
241.82 ms  AS9808  中国, 北京, chinamobile.com, 移动
241.40 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 947.55 Mbps	 915.68 Mbps	 0.48	  0.0%
洛杉矶		 1956.24 Mbps	 5341.32 Mbps	 8.66	  0.0%
日本东京	 1970.05 Mbps	 3828.27 Mbps	 107.39	  0.0%
联通湖南5G	 529.47 Mbps	 3.04 Mbps	 164.61	  NULL
联通Fuzhou	 616.97 Mbps	 3556.68 Mbps	 151.05	  0.0%
电信Suzhou5G	 1161.72 Mbps	 1791.58 Mbps	 148.59	  NULL
电信武汉	 383.33 Mbps	 1532.66 Mbps	 158.42	  NULL
移动Beijing	 803.87 Mbps	 1446.80 Mbps	 230.34	  NULL
移动Chengdu	 813.44 Mbps	 1981.17 Mbps	 235.97	  0.0%
------------------------------------------------------------------------
```

## 迪拜

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : QEMU Virtual CPU version (cpu64-rhel6)
 CPU 核心数        : 2
 CPU 频率          : 2699.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 39.4 GB (2.9 GB 已用)
 内存              : 1983 MB (313 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 4 min
 负载              : 0.00, 0.00, 0.00
 系统              : Debian GNU/Linux 12 (bookworm)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-9-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS21887 Fiber Logic Inc.
 位置              : Dubai / AE
 地区              : Dubai
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		670 Scores
 2 线程测试(多核)得分: 		1337 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		13773.20 MB/s
 单线程写测试:		12402.37 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		15.3 MB/s (3734 IOPS, 6.86s)		19.2 MB/s (4699 IOPS, 5.45s)
 1GB-1M Block		330 MB/s (315 IOPS, 3.18s)		1.2 GB/s (1143 IOPS, 0.87s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 40.81 MB/s   (10.2k) | 452.44 MB/s   (7.0k)
Write      | 40.89 MB/s   (10.2k) | 454.82 MB/s   (7.1k)
Total      | 81.70 MB/s   (20.4k) | 907.26 MB/s  (14.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 947.53 MB/s   (1.8k) | 1.17 GB/s     (1.1k)
Write      | 997.87 MB/s   (1.9k) | 1.24 GB/s     (1.2k)
Total      | 1.94 GB/s     (3.7k) | 2.42 GB/s     (2.3k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: INTERLAN
视频缓存节点地域: OTP(OTP2)
Youtube识别地域: 阿联酋(AE)
[IPv6]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: INTERLAN
视频缓存节点地域: OTP(OTP2)
Youtube识别地域: 阿联酋(AE)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：阿联酋
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口所在地区即将开通DisneyPlus，尽请期待哦！
[IPv6]
当前IPv6出口所在地区即将开通DisneyPlus，尽请期待哦！
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Available For [Disney+ AE] Soon
 Netflix:				Yes (Region: AE)
 YouTube Premium:			Yes (Region: AE)
 Amazon Prime Video:			Yes (Region: AE)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			AE
 Viu.com:				Yes (Region: AE)
 YouTube CDN:				Associated with [INTERLAN]
 Netflix Preferred CDN:			Milan  
 Spotify Registration:			No
 Steam Currency:			AED
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		Failed
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：50
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：6
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/27 00:46:48 北京电信 219.141.136.12  测试超时
2023/06/27 00:46:48 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/27 00:46:48 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/27 00:46:48 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/27 00:46:48 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/27 00:46:48 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/27 00:46:48 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/27 00:46:48 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/27 00:46:48 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/27 00:46:48 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/27 00:46:48 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/27 00:46:48 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS21887 Fiber-logic
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
19.35 ms  *  局域网
0.28 ms  AS200851  阿联酋, 迪拜酋长国, 迪拜, bamboozle.me
0.50 ms  AS6939  阿联酋, 迪拜酋长国, 迪拜, he.net
40.56 ms  AS6939  吉布提, 吉布提市, he.net
153.97 ms  AS6939  肯尼亚, 内罗毕县, 内罗毕, he.net
185.32 ms  AS6939  南非, 豪登省, 约翰内斯堡, he.net
236.30 ms  *  南非, 豪登省, 约翰内斯堡, inx.net.za
313.52 ms  AS4134  新加坡, chinatelecom.com.cn, 电信
354.07 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
371.41 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
370.12 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
368.41 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
11.97 ms  *  局域网
27.02 ms  AS200851  阿联酋, 迪拜酋长国, 迪拜, bamboozle.me
12.42 ms  AS6939  阿联酋, 迪拜酋长国, 迪拜, he.net
99.04 ms  AS6939  法国, 普罗旺斯－阿尔卑斯－蓝色海岸大区, 马赛, he.net
332.73 ms  AS6939  德国, 黑森州, 法兰克福, he.net
336.68 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
332.65 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
325.92 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
327.39 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
12.16 ms  *  局域网
0.30 ms  AS200851  阿联酋, 迪拜酋长国, 迪拜, bamboozle.me
26.14 ms  AS6939  阿联酋, 迪拜酋长国, 迪拜, he.net
120.37 ms  AS6939  新加坡, he.net
77.20 ms  AS3491  新加坡, equinix.com
108.24 ms  AS58453  中国, 香港, chinamobile.com, 移动
277.68 ms  AS58453  中国, 上海, chinamobile.com, 移动
278.97 ms  AS9808  中国, 上海, chinamobile.com, 移动
280.88 ms  AS9808  中国, 上海, chinamobile.com, 移动
298.48 ms  AS9808  中国, 北京, chinamobile.com, 移动
306.71 ms  AS9808  中国, 北京, chinamobile.com, 移动
305.42 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 1282.35 Mbps	 881.27 Mbps	 0.51	  NULL
中国香港	 723.75 Mbps	 920.13 Mbps	 109.86	  NULL
日本东京	 606.38 Mbps	 946.36 Mbps	 150.90	  0.0%
联通湖南5G	 216.93 Mbps	 117.48 Mbps	 345.76	  NULL
电信天津	 0.84 Mbps	 268.91 Mbps	 269.23	  NULL
电信上海	 1.96 Mbps	 7.25 Mbps	 307.46	  NULL
移动Beijing	 578.03 Mbps	 631.34 Mbps	 348.30	  NULL
移动杭州5G	 130.69 Mbps	 787.27 Mbps	 377.57	  0.0%
------------------------------------------------------------------------
```
