---
title: "AkileCloud 日本bgp 测试"
date: "2023-07-24"
categories: 
  - "vps"
  - "jp"
---

## 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7402P 24-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 2794.748 MHz
 CPU 缓存          : L1: 128.00 KB / L2: 512.00 KB / L3: 16.00 MB
 硬盘空间          : 1.20 GiB / 7.71 GiB
 启动盘路径        : /dev/sda1
 内存              : 67.66 MiB / 224.14 MiB
 Swap              : 4.00 MiB / 256.00 MiB
 系统在线时间      : 0 days, 0 hour 3 min
 负载              : 0.27, 0.10, 0.03
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-22-cloud-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : Full Cone
 IPV4 ASN          : AS61112 AKILE LTD
 IPV4 位置         : Fuchū / Tokyo / JP
 IPV6 ASN          : AS51847 Nearoute Limited
 IPV6 位置         : Koganei / Tokyo
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1633 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		41255.87 MB/s
 单线程写测试:		18105.04 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		61.9 MB/s (15.11 IOPS, 1.69s)		112 MB/s (27241 IOPS, 0.94s)
 1GB-1M Block		1.8 GB/s (1763 IOPS, 0.57s)		5.2 GB/s (4931 IOPS, 0.20s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 238.86 MB/s  (59.7k) | 1.40 GB/s    (21.9k)
Write      | 239.49 MB/s  (59.8k) | 1.41 GB/s    (22.0k)
Total      | 478.36 MB/s (119.5k) | 2.81 GB/s    (44.0k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.57 GB/s     (3.0k) | 1.85 GB/s     (1.8k)
Write      | 1.65 GB/s     (3.2k) | 1.98 GB/s     (1.9k)
Total      | 3.22 GB/s     (6.3k) | 3.83 GB/s     (3.7k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 日本 东京(NRT12S24)
Youtube识别地域: 日本(JP)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 日本 东京(NRT12S24)
Youtube识别地域: 日本(JP)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：日本
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[提醒] 无法获取DisneyPlus权验接口信息，当前测试可能会不准确
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
 Dazn:					Yes (Region: JP)
 HotStar:				No
 Disney+:				Yes (Region: JP)
 Netflix:				Yes (Region: JP)
 YouTube Premium:			Yes (Region: JP)
 Amazon Prime Video:			Yes (Region: JP)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			JP
 Viu.com:				No
 YouTube CDN:				Tokyo 
 Netflix Preferred CDN:			Associated with [Nearoute Limited] in [Tokyo ]
 Spotify Registration:			No
 Steam Currency:			JPY
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				Failed (Network Connection)
 Disney+:				No
 Netflix:				Failed (Network Connection)
 YouTube Premium:			Failed (Network Connection)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube Region:			Check Failed (Network Connection)
 Netflix Preferred CDN:			Failed
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				No
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【JP】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：0
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
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱：No
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
2023/07/24 04:22:19 北京电信 219.141.136.12  电信163 [普通线路]           
2023/07/24 04:22:19 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/24 04:22:19 北京移动 221.179.155.161 测试超时
2023/07/24 04:22:19 上海电信 202.96.209.133  电信163 [普通线路]           
2023/07/24 04:22:19 上海联通 210.22.97.1     联通4837[普通线路]           
2023/07/24 04:22:19 上海移动 211.136.112.200 测试超时
2023/07/24 04:22:19 广州电信 58.60.188.222   电信163 [普通线路]           
2023/07/24 04:22:19 广州联通 210.21.196.6    联通4837[普通线路]           
2023/07/24 04:22:19 广州移动 120.196.165.24  测试超时
2023/07/24 04:22:19 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/24 04:22:19 成都联通 119.6.6.6       联通4837[普通线路]           
2023/07/24 04:22:19 成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
9.43 ms  AS61112  日本, 东京都, 东京, cogentco.com
0.66 ms  *  局域网
1.45 ms  AS2497  日本, 东京都, 东京, iij.ad.jp
1.54 ms  AS2497  日本, 东京都, 东京, iij.ad.jp
33.42 ms  AS4134  日本, 东京都, 东京, chinatelecom.com.cn, 电信
56.18 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
55.11 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
58.64 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
12.85 ms  AS61112  日本, 东京都, 东京, cogentco.com
16.16 ms  *  局域网
1.65 ms  AS2914  日本, 东京都, 东京, ntt.com
56.99 ms  AS2914  日本, 东京都, 东京, ntt.com
62.87 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
57.24 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
59.61 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
63.09 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
60.86 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
5.49 ms  AS61112  日本, 东京都, 东京, cogentco.com
0.73 ms  *  局域网
57.42 ms  AS9808  中国, 上海, chinamobile.com, 移动
57.67 ms  AS9808  中国, 上海, chinamobile.com, 移动
57.58 ms  AS9808  中国, 上海, chinamobile.com, 移动
75.06 ms  AS9808  中国, 北京, chinamobile.com, 移动
77.96 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 5330.38 Mbps	 3470.61 Mbps	 0.76	  NULL
日本东京	 1256.47 Mbps	 3258.23 Mbps	 3.73	  0.0%
中国香港	 644.93 Mbps	 196.91 Mbps	 50.59	  2.5%
联通WuXi	 46.22 Mbps	 49.90 Mbps	 40.22	  0.0%
联通郑州5G	 1139.51 Mbps	 1118.67 Mbps	 51.54	  NULL
电信Suzhou5G	 1158.40 Mbps	 885.95 Mbps	 36.53	  NULL
电信Zhenjiang5G	 824.60 Mbps	 634.05 Mbps	 95.82	  NULL
移动杭州5G	 919.58 Mbps	 1193.82 Mbps	 65.83	  0.0%
移动Zhengzhou5G	 990.95 Mbps	 892.21 Mbps	 80.52	  0.0%
------------------------------------------------------------------------
 总共花费      : 5 分 52 秒
 时间          : Mon Jul 24 04:27:00 UTC 2023
------------------------------------------------------------------------
```
