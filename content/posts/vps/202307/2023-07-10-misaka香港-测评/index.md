---
title: "Misaka香港 测评"
date: "2023-07-10"
categories: 
  - "vps"
  - "hk"
---

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC-Milan Processor
 CPU 核心数        : 1
 CPU 频率          : 2645.030 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 1.24 GiB / 14.96 GiB
 启动盘路径        : /dev/vda1
 内存              : 152.71 MiB / 946.78 MiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 3 days, 20 hour 7 min
 负载              : 0.00, 0.00, 0.00
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS23961 Misaka Network, Inc.
 IPV4 位置         : Hong Kong / Central and Western / HK
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		3492 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		38729.95 MB/s
 单线程写测试:		14962.25 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		58.9 MB/s (14.38 IOPS, 1.78s)		84.5 MB/s (20627 IOPS, 1.24s)
 1GB-1M Block		1.6 GB/s (1573 IOPS, 0.64s)		2.1 GB/s (2032 IOPS, 0.49s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 251.57 MB/s  (62.8k) | 2.84 GB/s    (44.4k)
Write      | 252.24 MB/s  (63.0k) | 2.86 GB/s    (44.6k)
Total      | 503.82 MB/s (125.9k) | 5.70 GB/s    (89.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.95 GB/s     (7.7k) | 4.24 GB/s     (4.1k)
Write      | 4.16 GB/s     (8.1k) | 4.52 GB/s     (4.4k)
Total      | 8.11 GB/s    (15.8k) | 8.77 GB/s     (8.5k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 中国香港(HKG07S42)
Youtube识别地域: 香港(HK)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 中国香港(HKG33S01)
Youtube识别地域: 香港(HK)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：香港
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：香港
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：香港区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：香港区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: HK)
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
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				No
 Disney+:				Yes (Region: HK)
 Netflix:				Yes (Region: HK)
 YouTube Premium:			Yes (Region: HK)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Hong Kong 
 Netflix Preferred CDN:			Hong Kong  
 Spotify Registration:			No
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				No
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		Failed
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：31
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
  欺诈分数(越低越好)：49
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱：No
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：0
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
2023/07/10 09:22:48 北京电信 219.141.136.12  电信163 [普通线路]           
2023/07/10 09:22:48 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/10 09:22:48 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/10 09:22:48 上海电信 202.96.209.133  电信163 [普通线路]           
2023/07/10 09:22:48 上海联通 210.22.97.1     联通4837[普通线路]           
2023/07/10 09:22:48 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/10 09:22:48 广州电信 58.60.188.222   电信163 [普通线路]           
2023/07/10 09:22:48 广州联通 210.21.196.6    联通4837[普通线路]           
2023/07/10 09:22:48 广州移动 120.196.165.24  测试超时
2023/07/10 09:22:48 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/10 09:22:48 成都联通 119.6.6.6       联通4837[普通线路]           
2023/07/10 09:22:48 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.99 ms  AS57695  中国, 香港, misaka.io
0.24 ms  AS57695  中国, 香港, misaka.io
0.29 ms  *  中国, 香港, hostuj.to
1.20 ms  AS6453  中国, 香港, tatacommunications.com
56.47 ms  AS6453  日本, 千叶县, 千叶市, tatacommunications.com
167.30 ms  AS6453  美国, 加利福尼亚州, 圣何塞, tatacommunications.com
170.54 ms  AS4134  美国, 加利福尼亚州, 圣何塞, chinatelecom.com.cn, 电信
169.80 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
171.53 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
172.91 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
176.17 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
174.51 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.25 ms  AS57695  中国, 香港, misaka.io
0.26 ms  AS57695  中国, 香港, misaka.io
0.28 ms  *  中国, 香港, hostuj.to
1.30 ms  AS2914  中国, 香港, ntt.com
1.26 ms  AS2914  中国, 香港, ntt.com
51.70 ms  AS2914  日本, 东京都, 东京, ntt.com
49.67 ms  AS2914  日本, 东京都, 东京, ntt.com
85.65 ms  AS2914  日本, 东京都, 东京, ntt.com
95.46 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
93.90 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
93.81 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
92.90 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.15 ms  AS57695  中国, 香港, misaka.io
0.32 ms  AS57695  中国, 香港, misaka.io
0.31 ms  *  中国, 香港, hostuj.to
1.28 ms  AS2914  中国, 香港, ntt.com
29.10 ms  AS58453  中国, 上海, chinamobile.com, 移动
30.87 ms  AS9808  中国, 上海, chinamobile.com, 移动
30.93 ms  AS9808  中国, 上海, chinamobile.com, 移动
30.70 ms  AS9808  中国, 上海, chinamobile.com, 移动
55.56 ms  AS9808  中国, 北京, chinamobile.com, 移动
56.43 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 10205.99 Mbps	 12080.04 Mbps	 0.22	  0.0%
中国香港	 6784.97 Mbps	 5940.60 Mbps	 3.24	  0.0%
新加坡		 6390.33 Mbps	 2534.33 Mbps	 30.69	  0.0%
联通郑州5G	 317.09 Mbps	 231.00 Mbps	 0.30	  NULL
联通Fuzhou	 794.30 Mbps	 1165.67 Mbps	 76.89	  1.3%
电信Zhenjiang5G	 135.79 Mbps	 2002.00 Mbps	 160.47	  NULL
电信武汉	 116.55 Mbps	 405.61 Mbps	 165.77	  NULL
移动杭州5G	 350.99 Mbps	 16.48 Mbps	 37.50	  2.0%
移动Beijing	 806.39 Mbps	 1102.08 Mbps	 49.89	  1.3%
------------------------------------------------------------------------
 总共花费      : 5 分 59 秒
 时间          : Mon Jul 10 09:27:35 UTC 2023
------------------------------------------------------------------------
```

### 流媒体解锁

```
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: HK)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: HK)
 Amazon Prime Video:                    Yes (Region: HK)
 TVBAnywhere+:                          No
 iQyi Oversea Region:                   HK
 Viu.com:                               Yes (Region: HK)
 YouTube CDN:                           Hong Kong 
 Netflix Preferred CDN:                 Hong Kong  
 Spotify Registration:                  No
 Steam Currency:                        HKD
 ChatGPT:                               No
=======================================
=============[ Hong Kong ]=============
 Now E:                                 Failed (Unexpected Result: )
 Viu.TV:                                Yes
 MyTVSuper:                             No
 HBO GO Asia:                           Yes (Region: HK)
 BiliBili Hongkong/Macau/Taiwan:        Yes
=======================================


 ** 正在测试IPv6解锁情况 
--------------------------------
 ** 您的网络为: Misaka Network (2407:b9c0:f001:*:*) 


============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: HK)
 Netflix:                               Yes (Region: HK)
 YouTube Premium:                       Yes (Region: HK)
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Hong Kong 
 Netflix Preferred CDN:                 Hong Kong  
 Spotify Registration:                  No
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               No
=======================================
=============[ Hong Kong ]=============
 Now E:                                 Failed (Unexpected Result: )
 Viu.TV:                                Failed (Network Connection)
 MyTVSuper:                             No
 HBO GO Asia:                           Failed (Network Connection)
 BiliBili Hongkong/Macau/Taiwan:        Failed (Network Connection)
=======================================
```

## 线路优化版套餐配置

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC-Milan Processor
 CPU 核心数        : 1
 CPU 频率          : 2645.030 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 1.05 GiB / 14.96 GiB
 启动盘路径        : /dev/vda1
 内存              : 202.86 MiB / 946.78 MiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 1 hour 23 min
 负载              : 0.07, 0.02, 0.00
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS23961 Misaka Network, Inc.
 IPV4 位置         : Hong Kong / Central and Western / HK
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		3795 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		39101.98 MB/s
 单线程写测试:		15950.02 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		47.3 MB/s (11.54 IOPS, 2.22s)		90.9 MB/s (22199 IOPS, 1.15s)
 1GB-1M Block		1.6 GB/s (1516 IOPS, 0.66s)		2.0 GB/s (1865 IOPS, 0.54s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 229.89 MB/s  (57.4k) | 2.33 GB/s    (36.4k)
Write      | 230.50 MB/s  (57.6k) | 2.34 GB/s    (36.6k)
Total      | 460.40 MB/s (115.1k) | 4.68 GB/s    (73.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.46 GB/s     (6.7k) | 3.62 GB/s     (3.5k)
Write      | 3.65 GB/s     (7.1k) | 3.86 GB/s     (3.7k)
Total      | 7.12 GB/s    (13.9k) | 7.48 GB/s     (7.3k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 中国香港(HKG07S42)
Youtube识别地域: 香港(HK)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 中国香港(HKG33S01)
Youtube识别地域: 香港(HK)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：香港
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：香港
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：香港区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：香港区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: HK)
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
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				No
 Disney+:				Yes (Region: HK)
 Netflix:				Yes (Region: HK)
 YouTube Premium:			Yes (Region: HK)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Hong Kong 
 Netflix Preferred CDN:			Hong Kong  
 Spotify Registration:			No
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				No
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		Failed
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：17
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
  欺诈分数(越低越好)：15
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱：No
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：0
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
2023/07/10 11:01:48 北京电信 219.141.136.12  移动CMI [普通线路]           
2023/07/10 11:01:48 北京联通 202.106.50.1    移动CMI [普通线路]           
2023/07/10 11:01:48 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/10 11:01:48 上海电信 202.96.209.133  移动CMI [普通线路] 
2023/07/10 11:01:48 上海联通 210.22.97.1     移动CMI [普通线路]           
2023/07/10 11:01:48 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/10 11:01:48 广州电信 58.60.188.222   移动CMI [普通线路]           
2023/07/10 11:01:48 广州联通 210.21.196.6    移动CMI [普通线路]           
2023/07/10 11:01:48 广州移动 120.196.165.24  移动CMI [普通线路] 
2023/07/10 11:01:48 成都电信 61.139.2.69     移动CMI [普通线路]           
2023/07/10 11:01:48 成都联通 119.6.6.6       移动CMI [普通线路]           
2023/07/10 11:01:48 成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.40 ms  AS57695  中国, 香港, misaka.io
0.37 ms  AS969  中国, 香港, misaka.io
29.23 ms  AS58453  中国, 上海, chinamobile.com, 移动
30.09 ms  AS9808  中国, 上海, chinamobile.com, 移动
30.67 ms  AS9808  中国, 上海, chinamobile.com, 移动
31.46 ms  AS9808  中国, 上海, chinamobile.com, 移动
37.39 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
39.34 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
38.86 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.15 ms  AS57695  中国, 香港, misaka.io
0.57 ms  AS969  中国, 香港, misaka.io
30.55 ms  AS9808  中国, 上海, chinamobile.com, 移动
33.91 ms  AS9808  中国, 上海, chinamobile.com, 移动
43.98 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
41.98 ms  AS17816  中国, 广东, 广州, chinaunicom.com, 联通
44.09 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
44.27 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.17 ms  AS57695  中国, 香港, misaka.io
0.56 ms  AS969  中国, 香港, misaka.io
56.38 ms  AS9808  中国, 北京, chinamobile.com, 移动
55.80 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 10287.48 Mbps	 12704.46 Mbps	 0.15	  0.0%
中国香港	 6931.67 Mbps	 6557.82 Mbps	 3.40	  0.0%
新加坡		 5745.68 Mbps	 1845.55 Mbps	 30.62	  0.0%
联通Fuzhou	 950.48 Mbps	 3256.66 Mbps	 49.36	  0.0%
电信合肥5G	 958.19 Mbps	 762.74 Mbps	 50.83	  0.0%
电信上海	 958.30 Mbps	 2350.79 Mbps	 30.42	  NULL
移动杭州5G	 959.52 Mbps	 1053.30 Mbps	 34.61	  0.0%
移动Beijing	 869.93 Mbps	 718.89 Mbps	 51.44	  1.7%
------------------------------------------------------------------------
 总共花费      : 5 分 12 秒
 时间          : Mon Jul 10 11:05:45 UTC 2023
------------------------------------------------------------------------
```

### 流媒体解锁

```
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: HK)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: HK)
 Amazon Prime Video:                    Yes (Region: HK)
 TVBAnywhere+:                          No
 iQyi Oversea Region:                   HK
 Viu.com:                               Yes (Region: HK)
 YouTube CDN:                           Hong Kong 
 Netflix Preferred CDN:                 Hong Kong  
 Spotify Registration:                  No
 Steam Currency:                        HKD
 ChatGPT:                               No
=======================================
=============[ Hong Kong ]=============
 Now E:                                 Failed (Unexpected Result: )
 Viu.TV:                                Yes
 MyTVSuper:                             No
 HBO GO Asia:                           Yes (Region: HK)
 BiliBili Hongkong/Macau/Taiwan:        Yes
=======================================


 ** 正在测试IPv6解锁情况 
--------------------------------
 ** 您的网络为: Misaka Network (2407:b9c0:f001:*:*) 


============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: HK)
 Netflix:                               Yes (Region: HK)
 YouTube Premium:                       Yes (Region: HK)
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Hong Kong 
 Netflix Preferred CDN:                 Hong Kong  
 Spotify Registration:                  No
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               No
=======================================
=============[ Hong Kong ]=============
 Now E:                                 Failed (Unexpected Result: )
 Viu.TV:                                Failed (Network Connection)
 MyTVSuper:                             No
 HBO GO Asia:                           Failed (Network Connection)
 BiliBili Hongkong/Macau/Taiwan:        Failed (Network Connection)
=======================================
```

### ping.ie测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-170.png)
