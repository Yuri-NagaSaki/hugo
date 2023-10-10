---
title: "AWS Lightsail 新加坡 东京升级款"
date: "2023-07-03"
categories: 
  - "vps"
  - "sg"
---

![](https://catcat.blog/wp-content/uploads/2023/07/image-1024x435.png)

## 新加坡

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
 CPU Cores          : 2 @ 2499.998 MHz
 CPU Cache          : 36608 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Disabled
 Total Disk         : 39.3 GB (1.1 GB Used)
 Total Mem          : 950.8 MB (67.1 MB Used)
 System uptime      : 0 days, 0 hour 3 min
 Load average       : 0.80, 0.40, 0.16
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-17-cloud-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS16509 Amazon.com, Inc.
 Location           : Singapore / SG
 Region             : Singapore
----------------------------------------------------------------------
 I/O Speed(1st run) : 56.5 MB/s
 I/O Speed(2nd run) : 56.3 MB/s
 I/O Speed(3rd run) : 49.4 MB/s
 I/O Speed(average) : 54.1 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    4496.93 Mbps      4446.08 Mbps        0.90 ms     
 Los Angeles, US  508.91 Mbps       1664.60 Mbps        177.24 ms   
 Dallas, US       434.83 Mbps       1439.37 Mbps        203.95 ms   
 Montreal, CA     122.15 Mbps       599.27 Mbps         249.74 ms   
 Paris, FR        745.40 Mbps       2359.28 Mbps        151.50 ms   
 Amsterdam, NL    493.76 Mbps       1443.75 Mbps        186.16 ms   
 Shanghai, CN     1115.62 Mbps      3852.72 Mbps        65.80 ms    
 Nanjing, CN      880.18 Mbps       1884.71 Mbps        66.15 ms    
 Hongkong, CN     1153.76 Mbps      3630.48 Mbps        34.55 ms    
 Singapore, SG    4046.21 Mbps      4508.58 Mbps        1.48 ms     
 Tokyo, JP        449.56 Mbps       2800.17 Mbps        66.17 ms    
----------------------------------------------------------------------
 Finished in        : 6 min 28 sec
 Timestamp          : 2023-07-03 06:18:38 UTC
----------------------------------------------------------------------
```

## 东京

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
 CPU 核心数        : 2
 CPU 频率          : 2499.998 MHz
 CPU 缓存          : 36608 KB
 硬盘空间          : 40.1 GB (1.1 GB 已用)
 内存              : 950 MB (73 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 11 min
 负载              : 0.33, 0.46, 0.31
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-17-cloud-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 独立映射,独立过滤,支持回环
 ASN组织           : AS16509 Amazon.com, Inc.
 位置              : Singapore / SG
 地区              : Singapore
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		998 Scores
 2 线程测试(多核)得分: 		1684 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		19643.11 MB/s
 单线程写测试:		14649.93 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		4.9 MB/s (1196 IOPS, 21.41s)		13.9 MB/s (3397 IOPS, 7.53s)
 1GB-1M Block		15.4 MB/s (15 IOPS, 67.90s)		154 MB/s (146 IOPS, 6.81s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 6.18 MB/s     (1.5k) | 67.63 MB/s    (1.0k)
Write      | 6.18 MB/s     (1.5k) | 67.93 MB/s    (1.0k)
Total      | 12.36 MB/s    (3.0k) | 135.57 MB/s   (2.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 64.84 MB/s     (126) | 63.97 MB/s      (62)
Write      | 67.95 MB/s     (132) | 68.66 MB/s      (67)
Total      | 132.79 MB/s    (258) | 132.64 MB/s    (129)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 新加坡 新加坡/樟宜  (SIN10S14)
Youtube识别地域: 新加坡(SG)
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
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: SG)
 Amazon Prime Video:			Yes (Region: SG)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			SG
 Viu.com:				Yes (Region: SG)
 YouTube CDN:				Singapore 
 Netflix Preferred CDN:			Mumbai (Bombay)  
 Spotify Registration:			No
 Steam Currency:			SGD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【SG】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：28
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
  欺诈分数(越低越好)：40
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/07/03 06:25:45 北京电信 219.141.136.12  电信163 [普通线路]           
2023/07/03 06:25:45 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/03 06:25:45 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/03 06:25:45 上海电信 202.96.209.133  电信163 [普通线路]           
2023/07/03 06:25:45 上海联通 210.22.97.1     联通4837[普通线路]           
2023/07/03 06:25:45 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/03 06:25:45 广州电信 58.60.188.222   测试超时
2023/07/03 06:25:45 广州联通 210.21.196.6    联通4837[普通线路]           
2023/07/03 06:25:45 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/07/03 06:25:45 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/03 06:25:45 成都联通 119.6.6.6       联通4837[普通线路]           
2023/07/03 06:25:45 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS16509 Amazon.com
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
8.35 ms  AS16509  新加坡, amazon.com
0.37 ms  *  共享地址
1.45 ms  *  新加坡, amazon.com
1.62 ms  *  新加坡, amazon.com
0.85 ms  *  新加坡, amazon.com
1.26 ms  AS174  新加坡, cogentco.com
2.85 ms  AS174  新加坡, cogentco.com
171.60 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
174.07 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
195.92 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
182.28 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
200.99 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
202.77 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
200.40 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
212.98 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
210.10 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
10.91 ms  *  保留地址
0.99 ms  *  共享地址
0.52 ms  *  新加坡, amazon.com
1.42 ms  *  新加坡, amazon.com
0.94 ms  *  新加坡, amazon.com
1.22 ms  *  新加坡, amazon.com
46.07 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
52.78 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
49.22 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
48.69 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
1.58 ms  *  共享地址
6.74 ms  *  新加坡, amazon.com
8.04 ms  *  新加坡, amazon.com
1.78 ms  *  新加坡, amazon.com
1.62 ms  AS58453  新加坡, chinamobile.com, 移动
31.20 ms  AS58453  中国, 香港, chinamobile.com, 移动
61.34 ms  AS9808  中国, 上海, chinamobile.com, 移动
60.79 ms  AS9808  中国, 上海, chinamobile.com, 移动
59.79 ms  AS9808  中国, 上海, chinamobile.com, 移动
78.24 ms  AS9808  中国, 北京, chinamobile.com, 移动
77.98 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 4496.52 Mbps	 4212.04 Mbps	 0.82	  0.0%
新加坡		 4452.36 Mbps	 4385.47 Mbps	 1.89	  0.0%
中国香港	 766.04 Mbps	 202.56 Mbps	 39.20	  NULL
联通湖南5G	 1097.91 Mbps	 652.17 Mbps	 47.78	  NULL
联通海南	 1380.55 Mbps	 2036.37 Mbps	 58.18	  NULL
电信上海	 1.99 Mbps	 2276.33 Mbps	 66.94	  NULL
电信Suzhou5G	 820.24 Mbps	 1463.08 Mbps	 66.07	  NULL
移动杭州5G	 595.09 Mbps	 536.03 Mbps	 65.55	  0.0%
移动Beijing	 702.12 Mbps	 426.33 Mbps	 71.76	  NULL
------------------------------------------------------------------------
 总共花费      : 10 分 11 秒
 时间          : Mon Jul  3 06:30:44 UTC 2023
------------------------------------------------------------------------



```

```

-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : Intel(R) Xeon(R) Platinum 8175M CPU @ 2.50GHz
 CPU Cores          : 2 @ 2499.996 MHz
 CPU Cache          : 33792 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Disabled
 Total Disk         : 19.6 GB (5.3 GB Used)
 Total Mem          : 453.6 MB (319.4 MB Used)
 Total Swap         : 1024.0 MB (35.0 MB Used)
 System uptime      : 0 days, 0 hour 13 min
 Load average       : 0.06, 0.10, 0.04
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-23-cloud-amd64
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS16509 Amazon.com, Inc.
 Location           : Tokyo / JP
 Region             : Tokyo
----------------------------------------------------------------------
 I/O Speed(1st run) : 151 MB/s
 I/O Speed(2nd run) : 133 MB/s
 I/O Speed(3rd run) : 134 MB/s
 I/O Speed(average) : 139.3 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    4541.19 Mbps      2499.56 Mbps        1.29 ms     
 Los Angeles, US  649.04 Mbps       1575.36 Mbps        100.07 ms   
 Dallas, US       487.88 Mbps       1453.39 Mbps        142.28 ms   
 Montreal, CA     377.62 Mbps       802.37 Mbps         181.02 ms   
 Paris, FR        315.39 Mbps       1020.15 Mbps        217.17 ms   
 Amsterdam, NL    308.41 Mbps       1012.92 Mbps        228.18 ms   
 Shanghai, CN     1605.55 Mbps      3365.05 Mbps        33.65 ms    
 Nanjing, CN      1665.72 Mbps      2194.31 Mbps        33.89 ms    
 Guangzhou, CN    2.36 Mbps         473.51 Mbps         170.95 ms   
 Hongkong, CN     644.31 Mbps       2164.92 Mbps        101.07 ms   
 Singapore, SG    985.24 Mbps       2112.16 Mbps        70.64 ms    
 Tokyo, JP        425.37 Mbps       4395.44 Mbps        2.36 ms     
----------------------------------------------------------------------
 Finished in        : 6 min 22 sec
 Timestamp          : 2023-07-03 07:21:00 UTC
----------------------------------------------------------------------
```

```
--------------------- A Bench Script By spiritlhl ----------------------
                   测评频道: https://t.me/vps_reviews                    
版本：2023.06.27
更新日志：融合怪十代目(集合百家之长)(专为测评频道小鸡而生)
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : Intel(R) Xeon(R) Platinum 8175M CPU @ 2.50GHz
 CPU 核心数        : 2
 CPU 频率          : 2499.996 MHz
 CPU 缓存          : 33792 KB
 硬盘空间          : 20.1 GB (5.3 GB 已用)
 内存              : 453 MB (229 MB 已用)
 Swap              : 1023 MB (145 MB 已用)
 系统在线时间      : 0 days, 0 hour 21 min
 负载              : 0.52, 0.30, 0.15
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-cloud-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 独立映射,独立过滤,支持回环
 ASN组织           : AS16509 Amazon.com, Inc.
 位置              : Tokyo / JP
 地区              : Tokyo
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           148 Scores
 2 线程测试(多核)得分:          94 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          2125.70 MB/s
 单线程写测试:          1402.49 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         7.0 MB/s (1699 IOPS, 15.07s)            13.5 MB/s (3307 IOPS, 7.74s)
 1GB-1M Block           153 MB/s (146 IOPS, 6.86s)              144 MB/s (137 IOPS, 7.28s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 6.18 MB/s     (1.5k) | 67.52 MB/s    (1.0k)
Write      | 6.17 MB/s     (1.5k) | 67.96 MB/s    (1.0k)
Total      | 12.36 MB/s    (3.0k) | 135.48 MB/s   (2.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 64.66 MB/s     (126) | 64.27 MB/s      (62)
Write      | 67.93 MB/s     (132) | 68.49 MB/s      (66)
Total      | 132.59 MB/s    (258) | 132.76 MB/s    (128)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 日本 东京(NRT20S05)
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
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: JP)
 Amazon Prime Video:                    Yes (Region: JP)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   JP
 Viu.com:                               No
 YouTube CDN:                           Tokyo 
 Netflix Preferred CDN:                 Mumbai (Bombay)  
 Spotify Registration:                  No
 Steam Currency:                        JPY
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【JP】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：33
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
  欺诈分数(越低越好)：16
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/07/03 07:26:51 北京电信 219.141.136.12  测试超时
2023/07/03 07:26:51 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/03 07:26:51 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/03 07:26:51 上海电信 202.96.209.133  电信163 [普通线路]           
2023/07/03 07:26:51 上海联通 210.22.97.1     联通4837[普通线路]           
2023/07/03 07:26:51 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/03 07:26:51 广州电信 58.60.188.222   测试超时
2023/07/03 07:26:51 广州联通 210.21.196.6    联通4837[普通线路]           
2023/07/03 07:26:51 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/07/03 07:26:51 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/03 07:26:51 成都联通 119.6.6.6       联通4837[普通线路]           
2023/07/03 07:26:51 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS16509 Amazon.com
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
3.11 ms  AS16509  日本, 东京都, 东京, amazon.com
0.23 ms  *  保留地址
0.26 ms  *  保留地址
0.26 ms  *  保留地址
2.20 ms  *  共享地址
2.93 ms  *  日本, 大阪府, 大阪, amazon.com
2.52 ms  AS2914  日本, 东京都, 东京, ntt.com
4.09 ms  AS2914  日本, 东京都, 东京, ntt.com
3.11 ms  AS2914  日本, 东京都, 东京, ntt.com
91.62 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
96.09 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
95.99 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
7.90 ms  AS16509  日本, 东京都, 东京, amazon.com
0.24 ms  *  保留地址
0.26 ms  *  保留地址
1.30 ms  *  保留地址
2.24 ms  *  保留地址
1.13 ms  *  保留地址
1.54 ms  *  日本, 东京都, 东京, amazon.com
2.47 ms  *  日本, 东京都, 东京, amazon.com
83.33 ms  AS4837  中国, 上海, chinaunicom.com, 联通
61.16 ms  AS4837  中国, 上海, chinaunicom.com, 联通
94.70 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
103.58 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
97.22 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
6.44 ms  AS16509  日本, 东京都, 东京, amazon.com
0.26 ms  *  保留地址
0.26 ms  *  保留地址
0.96 ms  *  保留地址
2.28 ms  *  共享地址
1.47 ms  *  日本, 东京都, 东京, amazon.com
3.24 ms  *  美国, 弗吉尼亚州, 阿什本, amazon.com
2.21 ms  AS58453  日本, 东京都, 东京, chinamobile.com, 移动
32.56 ms  AS58453  中国, 上海, chinamobile.com, 移动
34.82 ms  AS9808  中国, 上海, chinamobile.com, 移动
33.92 ms  AS9808  中国, 上海, chinamobile.com, 移动
70.63 ms  AS9808  中国, 北京, chinamobile.com, 移动
76.88 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    1288.12 Mbps    4628.10 Mbps    3.12     NULL
日本东京         392.23 Mbps     365.82 Mbps     2.84     0.0%
中国香港         149.02 Mbps     62.78 Mbps      52.32    NULL
联通上海5G       251.07 Mbps     265.44 Mbps     60.10    0.0%
联通WuXi         42.69 Mbps      102.10 Mbps     34.85    0.0%
电信上海         81.89 Mbps      241.48 Mbps     43.97    NULL
电信Suzhou5G     228.91 Mbps     253.69 Mbps     54.16    NULL
移动杭州5G       217.86 Mbps     76.44 Mbps      39.71    0.0%
移动Chengdu      125.05 Mbps     222.76 Mbps     108.83   0.0%
------------------------------------------------------------------------
 总共花费      : 8 分 33 秒
 时间          : Mon Jul  3 07:31:36 UTC 2023
------------------------------------------------------------------------
```
