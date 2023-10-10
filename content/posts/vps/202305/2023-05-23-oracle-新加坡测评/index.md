---
title: "Oracle 测评"
date: "2023-05-23"
categories: 
  - "vps"
  - "sg"
  - "jp"
---

## 新加坡AMD

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD EPYC 7J13 64-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 2445.404 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 45.5 GB (1.2 GB 已用)
 内存              : 959 MB (98 MB 已用)
 Swap              : 975 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 8 min
 负载              : 0.13, 0.10, 0.08
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-22-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 独立映射,独立过滤,支持回环
 ASN组织           : AS31898 Oracle Corporation
 位置              : Singapore / SG
 地区              : Singapore
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1811 Scores
 2 线程测试(多核)得分: 		1822 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		22760.34 MB/s
 单线程写测试:		11553.09 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		11.7 MB/s (2860 IOPS, 8.95s)		13.1 MB/s (3197 IOPS, 8.01s)
 1GB-1M Block		55.2 MB/s (52 IOPS, 18.99s)		52.5 MB/s (50 IOPS, 19.99s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 6.32 MB/s     (1.5k) | 26.04 MB/s     (406)
Write      | 6.32 MB/s     (1.5k) | 26.49 MB/s     (413)
Total      | 12.64 MB/s    (3.1k) | 52.53 MB/s     (819)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 24.50 MB/s      (47) | 23.72 MB/s      (23)
Write      | 26.02 MB/s      (50) | 26.56 MB/s      (25)
Total      | 50.53 MB/s      (97) | 50.28 MB/s      (48)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 新加坡 新加坡/樟宜  (SIN11S18)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：新加坡
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：新加坡区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				Yes (Region: SG)
 Disney+:				Yes (Region: GB)
 Netflix:				Originals Only
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: SG)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			SG
 Viu.com:				Yes (Region: SG)
 YouTube CDN:				Singapore 
 Netflix Preferred CDN:			Singapore  
 Spotify Registration:			No
 Steam Currency:			SGD
 ChatGPT:				No
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【GB】
---------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化---------
[IPv4]
Your IP supports access to OpenAI. Region: SG
[IPv6]
IPv6 is not supported on the current host. Skip...
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：48
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：2
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/05/23 03:37:34 北京电信 219.141.136.12  电信163 [普通线路]           
2023/05/23 03:37:34 北京联通 202.106.50.1    联通4837[普通线路]           
2023/05/23 03:37:34 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/05/23 03:37:34 上海电信 202.96.209.133  电信163 [普通线路]           
2023/05/23 03:37:34 上海联通 210.22.97.1     联通4837[普通线路]           
2023/05/23 03:37:34 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/05/23 03:37:34 广州电信 58.60.188.222   电信163 [普通线路]           
2023/05/23 03:37:34 广州联通 210.21.196.6    联通4837[普通线路]           
2023/05/23 03:37:34 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/05/23 03:37:34 成都电信 61.139.2.69     电信163 [普通线路]           
2023/05/23 03:37:34 成都联通 119.6.6.6       联通4837[普通线路]           
2023/05/23 03:37:34 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS31898 Oracle Cloud
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.16 ms  AS31898  新加坡, oracle.com
2.36 ms  AS6453  新加坡, tatacommunications.com
0.97 ms  AS6453  新加坡, tatacommunications.com
188.12 ms  AS6453  新加坡, tatacommunications.com
166.78 ms  AS6453  日本, 东京都, 东京, tatacommunications.com
180.95 ms  AS6453  美国, 加利福尼亚州, 圣何塞, tatacommunications.com
179.39 ms  AS6453  美国, 加利福尼亚州, 圣何塞, tatacommunications.com
184.05 ms  AS4134  美国, 加利福尼亚州, 圣何塞, chinatelecom.com.cn, 电信
243.48 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
243.75 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
242.79 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.14 ms  AS31898  新加坡, oracle.com
0.97 ms  AS6453  新加坡, tatacommunications.com
0.98 ms  AS6453  新加坡, tatacommunications.com
189.91 ms  AS6453  新加坡, tatacommunications.com
76.71 ms  AS6453  日本, 千叶县, 千叶市, tatacommunications.com
180.35 ms  AS6453  美国, 加利福尼亚州, 洛杉矶, tatacommunications.com
197.40 ms  AS4837  美国, 加利福尼亚州, 洛杉矶, chinaunicom.com, 联通
342.53 ms  AS4837  中国, 北京, chinaunicom.com, 联通
227.09 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
224.63 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
224.82 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
208.14 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.17 ms  AS31898  新加坡, oracle.com
1.11 ms  AS7473  新加坡, singtel.com
2.50 ms  AS7473  新加坡, singtel.com
1.14 ms  AS7473  新加坡, singtel.com
3.36 ms  AS7473  新加坡, singtel.com
1.36 ms  AS7473  新加坡, singtel.com
1.81 ms  AS7473  新加坡, singtel.com
35.00 ms  AS7473  中国, 香港, singtel.com
35.83 ms  AS7473  中国, 香港, singtel.com
34.37 ms  AS7473  中国, 香港, singtel.com
36.00 ms  AS7473  中国, 香港, singtel.com
37.32 ms  AS58453  中国, 香港, chinamobile.com, 移动
63.76 ms  AS9808  中国, 上海, chinamobile.com, 移动
80.27 ms  AS9808  中国, 北京, chinamobile.com, 移动
81.98 ms  AS9808  中国, 北京, chinamobile.com, 移动
81.81 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 500.37 Mbps	 486.93 Mbps	 0.87	  NULL
新加坡		 500.63 Mbps	 487.55 Mbps	 2.96	  NULL
日本东京	 501.56 Mbps	 204.60 Mbps	 73.60	  0.0%
联通Fuzhou	 482.15 Mbps	 480.16 Mbps	 54.76	  0.0%
联通成都	 19.61 Mbps	 17.26 Mbps	 239.79	  NULL
电信上海	 129.45 Mbps	 499.41 Mbps	 211.36	  NULL
移动Chengdu	 501.76 Mbps	 305.91 Mbps	 90.03	  0.0%
------------------------------------------------------------------------
 总共花费      : 8 分 29 秒
 时间          : Tue May 23 03:41:22 EDT 2023
```

## 日本大阪ARM

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : Neoverse-N1
 CPU 核心数        : 4
 硬盘空间          : 97.5 GB (45.4 GB 已用)
 内存              : 23988 MB (3165 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 166 days, 23 hour 36 min
 负载              : 0.52, 0.15, 0.05
 系统              : Ubuntu 20.04.6 LTS
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : aarch64 (64 Bit)
 内核              : 5.15.0-1025-oracle
 TCP加速方式       : bbr
 虚拟化架构        : kvm
 NAT类型           : 独立映射,独立过滤,支持回环
 ASN组织           : AS31898 Oracle Corporation
 位置              : Osaka / JP
 地区              : Ōsaka
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           3497 Scores
 4 线程测试(多核)得分:          13894 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          29985.56 MB/s
 单线程写测试:          14580.98 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         9.1 MB/s (2228 IOPS, 11.49s)            9.1 MB/s (2230 IOPS, 11.48s)
 1GB-1M Block           53.4 MB/s (50 IOPS, 19.64s)             51.8 MB/s (49 IOPS, 20.26s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
ARM compatibility is considered *experimental*
  ------ | --- ---- | ---- ---- 
Read       | 12.63 MB/s    (3.1k) | 26.95 MB/s     (421)
Write      | 12.63 MB/s    (3.1k) | 27.76 MB/s     (433)
Total      | 25.27 MB/s    (6.3k) | 54.71 MB/s     (854)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 23.98 MB/s      (46) | 23.75 MB/s      (23)
Write      | 26.03 MB/s      (50) | 26.50 MB/s      (25)
Total      | 50.02 MB/s      (96) | 50.25 MB/s      (48)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
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
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: US)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: JP)
 Amazon Prime Video:                    Yes (Region: JP)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   JP
 Viu.com:                               No
 YouTube CDN:                           Osaka 
 Netflix Preferred CDN:                 Osaka  
 Spotify Registration:                  No
 Steam Currency:                        JPY
 ChatGPT:                               No
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【JP】
---------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化---------
[IPv4]
Your IP supports access to OpenAI. Region: JP
[IPv6]
IPv6 is not supported on the current host. Skip...
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：48
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：56
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/05/22 05:59:25 北京电信 219.141.136.12  测试超时
2023/05/22 05:59:25 北京联通 202.106.50.1    联通4837[普通线路]           
2023/05/22 05:59:25 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/05/22 05:59:25 上海电信 202.96.209.133  电信163 [普通线路]           
2023/05/22 05:59:25 上海联通 210.22.97.1     联通4837[普通线路]           
2023/05/22 05:59:25 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/05/22 05:59:25 广州电信 58.60.188.222   电信163 [普通线路]           
2023/05/22 05:59:25 广州联通 210.21.196.6    联通4837[普通线路]           
2023/05/22 05:59:25 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/05/22 05:59:25 成都电信 61.139.2.69     电信163 [普通线路]           
2023/05/22 05:59:25 成都联通 119.6.6.6       联通4837[普通线路]           
2023/05/22 05:59:25 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS31898 Oracle Cloud
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.30 ms  AS31898  日本, 大阪府, 大阪, oracle.com
0.94 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
1.57 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
109.02 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
110.54 ms  AS6453  日本, 东京都, 东京, tatacommunications.com
14.12 ms  AS6453  日本, 千叶县, 千叶市, tatacommunications.com
107.49 ms  AS6453  美国, 加利福尼亚州, 圣何塞, tatacommunications.com
114.15 ms  AS4134  美国, 加利福尼亚州, 圣何塞, chinatelecom.com.cn, 电信
172.40 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
181.48 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
180.72 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.41 ms  AS31898  日本, 大阪府, 大阪, oracle.com
0.82 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
1.49 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
120.29 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
121.23 ms  AS6453  日本, 东京都, 东京, tatacommunications.com
10.53 ms  AS6453  日本, 千叶县, 千叶市, tatacommunications.com
120.27 ms  AS6453  美国, 加利福尼亚州, 圣克拉拉, tatacommunications.com
121.34 ms  AS6453  美国, 加利福尼亚州, 洛杉矶, tatacommunications.com
127.81 ms  AS4837  美国, 加利福尼亚州, 洛杉矶, chinaunicom.com, 联通
330.60 ms  AS4837  中国, 北京, chinaunicom.com, 联通
204.45 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
200.79 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
232.56 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
216.22 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
219.80 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.30 ms  AS31898  日本, 大阪府, 大阪, oracle.com
1.43 ms  AS2914  日本, 大阪府, 大阪, ntt.com
1.40 ms  AS2914  日本, 大阪府, 大阪, ntt.com
2.46 ms  AS2914  日本, 大阪府, 大阪, ntt.com
55.95 ms  AS2914  中国, 香港, ntt.com
56.71 ms  AS58453  中国, 香港, chinamobile.com, 移动
83.32 ms  AS9808  中国, 上海, chinamobile.com, 移动
85.06 ms  AS9808  中国, 上海, chinamobile.com, 移动
101.10 ms  AS9808  中国, 北京, chinamobile.com, 移动
102.27 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    3723.87 Mbps    4084.66 Mbps    13.91    0.3%
新加坡           747.72 Mbps     938.19 Mbps     83.15    NULL
日本东京         375.40 Mbps     264.92 Mbps     111.17   0.0%
联通上海5G       305.39 Mbps     1831.35 Mbps    167.22   3.0%
联通湖南5G       451.50 Mbps     311.13 Mbps     177.89   NULL
电信Suzhou5G     513.59 Mbps     1944.03 Mbps    150.42   NULL
电信Zhenjiang5G  426.35 Mbps     3959.66 Mbps    152.24   NULL
移动Chengdu      570.96 Mbps     2211.38 Mbps    97.85    0.0%
------------------------------------------------------------------------
 总共花费      : 8 分 52 秒
 时间          : Mon May 22 06:04:24 UTC 2023
------------------------------------------------
```

## 日本大阪AMD

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD EPYC 7551 32-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 1996.246 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 45.5 GB (1.2 GB 已用)
 内存              : 959 MB (92 MB 已用)
 Swap              : 975 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 4 min
 负载              : 0.59, 0.27, 0.10
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-22-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 独立映射,独立过滤,支持回环
 ASN组织           : AS31898 Oracle Corporation
 位置              : Osaka / JP
 地区              : Ōsaka
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		616 Scores
 2 线程测试(多核)得分: 		608 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		16272.13 MB/s
 单线程写测试:		7347.01 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		7.4 MB/s (1794 IOPS, 14.26s)		7.5 MB/s (1820 IOPS, 14.07s)
 1GB-1M Block		55.1 MB/s (52 IOPS, 19.03s)		52.5 MB/s (50 IOPS, 19.97s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 6.37 MB/s     (1.5k) | 25.91 MB/s     (404)
Write      | 6.37 MB/s     (1.5k) | 26.37 MB/s     (412)
Total      | 12.75 MB/s    (3.1k) | 52.28 MB/s     (816)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 24.62 MB/s      (48) | 23.99 MB/s      (23)
Write      | 25.98 MB/s      (50) | 26.48 MB/s      (25)
Total      | 50.60 MB/s      (98) | 50.48 MB/s      (48)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 日本 大阪(KIX07S05)
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
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: AU)
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
 ChatGPT:				No
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【JP】
---------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化---------
[IPv4]
Your IP supports access to OpenAI. Region: JP
[IPv6]
IPv6 is not supported on the current host. Skip...
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：48
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：31
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/05/23 03:59:09 北京电信 219.141.136.12  电信163 [普通线路]           
2023/05/23 03:59:09 北京联通 202.106.50.1    联通4837[普通线路]           
2023/05/23 03:59:09 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/05/23 03:59:09 上海电信 202.96.209.133  电信163 [普通线路]           
2023/05/23 03:59:09 上海联通 210.22.97.1     联通4837[普通线路]           
2023/05/23 03:59:09 上海移动 211.136.112.200 测试超时
2023/05/23 03:59:09 广州电信 58.60.188.222   电信163 [普通线路]           
2023/05/23 03:59:09 广州联通 210.21.196.6    联通4837[普通线路]           
2023/05/23 03:59:09 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/05/23 03:59:09 成都电信 61.139.2.69     电信163 [普通线路]           
2023/05/23 03:59:09 成都联通 119.6.6.6       联通4837[普通线路]           
2023/05/23 03:59:09 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS31898 Oracle Cloud
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.23 ms  AS31898  日本, 大阪府, 大阪, oracle.com
0.93 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
1.31 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
107.86 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
107.86 ms  AS6453  日本, 东京都, 东京, tatacommunications.com
9.84 ms  AS6453  日本, 千叶县, 千叶市, tatacommunications.com
107.64 ms  AS6453  美国, 加利福尼亚州, 圣何塞, tatacommunications.com
113.83 ms  AS4134  美国, 加利福尼亚州, 圣何塞, chinatelecom.com.cn, 电信
173.29 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
182.47 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
183.08 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
179.98 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.31 ms  AS31898  日本, 大阪府, 大阪, oracle.com
1.03 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
1.24 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
119.04 ms  AS6453  日本, 大阪府, 大阪, tatacommunications.com
10.37 ms  AS6453  日本, 千叶县, 千叶市, tatacommunications.com
122.62 ms  AS6453  美国, 加利福尼亚州, 圣克拉拉, tatacommunications.com
121.38 ms  AS6453  美国, 加利福尼亚州, 圣克拉拉, tatacommunications.com
119.01 ms  AS6453  美国, 加利福尼亚州, 洛杉矶, tatacommunications.com
129.78 ms  AS4837  美国, 加利福尼亚州, 洛杉矶, chinaunicom.com, 联通
283.97 ms  AS4837  中国, 北京, chinaunicom.com, 联通
201.64 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
190.30 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
195.26 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
199.64 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
208.10 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.28 ms  AS31898  日本, 大阪府, 大阪, oracle.com
0.92 ms  AS2914  日本, 大阪府, 大阪, ntt.com
1.26 ms  AS2914  日本, 大阪府, 大阪, ntt.com
1.31 ms  AS2914  日本, 大阪府, 大阪, ntt.com
56.03 ms  AS2914  中国, 香港, ntt.com
56.07 ms  AS2914  中国, 香港, ntt.com
58.74 ms  AS58453  中国, 香港, chinamobile.com, 移动
82.49 ms  AS58453  中国, 上海, chinamobile.com, 移动
84.22 ms  AS9808  中国, 上海, chinamobile.com, 移动
99.46 ms  AS9808  中国, 北京, chinamobile.com, 移动
104.18 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		         上传速度	         下载速度	         延迟	          丢包率
Speedtest.net	 415.09 Mbps	 439.72 Mbps	 8.75	          84.6%
日本东京	         484.94 Mbps	 287.74 Mbps	 105.40	  0.8%
新加坡		 483.72 Mbps	 259.51 Mbps	 76.83	  NULL
联通湖南5G	 437.28 Mbps	 327.36 Mbps	 178.06	  NULL
联通WuXi	         9.77 Mbps	 352.68 Mbps	 175.75	  0.0%
电信Zhenjiang5G 312.89 Mbps	 477.50 Mbps	 150.47	  NULL
电信Suzhou5G	 480.65 Mbps	 386.26 Mbps	 148.66	  NULL
移动Chengdu	 483.47 Mbps	 286.11 Mbps	 112.14	  0.0%
------------------------------------------------------------------------
 总共花费      : 9 分 50 秒
 时间          : Tue May 23 04:03:52 EDT 2023
------------------------------------------------------------------------
```
