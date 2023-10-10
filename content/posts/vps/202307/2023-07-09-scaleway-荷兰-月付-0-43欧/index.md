---
title: "Scaleway 荷兰 年付30元"
date: "2023-07-09"
categories: 
  - "vps"
  - "eu"
---

## Yabs

```

Sun Jul  9 03:47:59 UTC 2023

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 24 minutes
Processor  : AMD EPYC 7281 16-Core Processor
CPU cores  : 1 @ 2096.062 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 975.8 MiB
Swap       : 0.0 KiB
Disk       : 9.1 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-23-cloud-amd64
VM Type    : KVM
IPv4/IPv6  : ❌ Offline / ✔ Online



fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 150.53 MB/s  (37.6k) | 1.08 GB/s    (16.9k)
Write      | 150.93 MB/s  (37.7k) | 1.09 GB/s    (17.0k)
Total      | 301.46 MB/s  (75.3k) | 2.17 GB/s    (33.9k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.36 GB/s     (2.6k) | 1.33 GB/s     (1.3k)
Write      | 1.44 GB/s     (2.8k) | 1.42 GB/s     (1.3k)
Total      | 2.80 GB/s     (5.4k) | 2.76 GB/s     (2.6k)

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 358 Mbits/sec   | 4.62 Gbits/sec  | 8.60 ms        
Scaleway        | Paris, FR (10G)           | busy            | busy            | 9.68 ms        
NovoServe       | North Holland, NL (40G)   | 359 Mbits/sec   | 4.86 Gbits/sec  | 2.04 ms        
Uztelecom       | Tashkent, UZ (10G)        | 232 Mbits/sec   | 1.96 Gbits/sec  | 88.6 ms        
Clouvider       | NYC, NY, US (10G)         | 253 Mbits/sec   | 1.89 Gbits/sec  | 83.8 ms        
Clouvider       | Dallas, TX, US (10G)      | 236 Mbits/sec   | 1.32 Gbits/sec  | 127 ms         
Clouvider       | Los Angeles, CA, US (10G) | busy            | 972 Mbits/sec   | 144 ms         

Geekbench releases can only be downloaded over IPv4. FTP the Geekbench files and run manually.

YABS completed in 7 min 52 sec
```

## 融合怪脚本测试

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD EPYC 7281 16-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 2096.062 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 9.2 GB (1.1 GB 已用)
 内存              : 975 MB (94 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 56 min
 负载              : 0.11, 0.19, 0.09
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-cloud-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 独立映射,独立过滤,不支持回环
 IPV4 ASN          : AS13335 Cloudflare, Inc.
 IPV4 位置         : Amsterdam / North Holland / NL
 IPV6 ASN          : AS12876 Scaleway
 IPV6 位置         : Amsterdam / North Holland
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1285 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		33289.82 MB/s
 单线程写测试:		12946.49 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		33.9 MB/s (8287 IOPS, 3.09s)		41.4 MB/s (10107 IOPS, 2.53s)
 1GB-1M Block		287 MB/s (274 IOPS, 3.65s)		1.8 GB/s (1694 IOPS, 0.59s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 142.77 MB/s  (35.6k) | 963.89 MB/s  (15.0k)
Write      | 143.15 MB/s  (35.7k) | 968.96 MB/s  (15.1k)
Total      | 285.92 MB/s  (71.4k) | 1.93 GB/s    (30.2k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.19 GB/s     (2.3k) | 1.29 GB/s     (1.2k)
Write      | 1.26 GB/s     (2.4k) | 1.38 GB/s     (1.3k)
Total      | 2.46 GB/s     (4.8k) | 2.67 GB/s     (2.6k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 新加坡 新加坡/樟宜  (SIN10S14)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS15S46)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：荷兰
[IPv6]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：荷兰
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
 Dazn:					Yes (Region: NL)
 HotStar:				No
 Disney+:				Yes (Region: NL)
 Netflix:				Yes (Region: NL)
 YouTube Premium:			Yes (Region: NL)
 Amazon Prime Video:			Yes (Region: NL)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				Singapore 
 Netflix Preferred CDN:			Amsterdam  
 Spotify Registration:			No
 Steam Currency:			EUR
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				No
 Disney+:				Yes (Region: NL)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: NL)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Amsterdam 
 Netflix Preferred CDN:			Amsterdam  
 Spotify Registration:			No
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【NL】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：7
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
  欺诈分数(越低越好)：6
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Content Delivery Network
Google搜索可行性：NO
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：13
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
2023/07/09 04:23:53 北京电信 219.141.136.12  电信163 [普通线路]           
2023/07/09 04:23:53 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/09 04:23:53 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/09 04:23:53 上海电信 202.96.209.133  电信163 [普通线路]           
2023/07/09 04:23:53 上海联通 210.22.97.1     测试超时
2023/07/09 04:23:53 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/09 04:23:53 广州电信 58.60.188.222   电信163 [普通线路]           
2023/07/09 04:23:53 广州联通 210.21.196.6    测试超时
2023/07/09 04:23:53 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/07/09 04:23:53 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/09 04:23:53 成都联通 119.6.6.6       测试超时
2023/07/09 04:23:53 成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
3.17 ms  AS13335  中国, 香港, cloudflare.com
3.11 ms  AS13335  荷兰, 北荷兰省, 阿姆斯特丹, level3.com
5.29 ms  AS13335  荷兰, 北荷兰省, 阿姆斯特丹, cloudflare.com
4.39 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
3.92 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
10.22 ms  AS1299  英国, 伦敦, telia.com
10.35 ms  AS1299  英国, 伦敦, telia.com
90.37 ms  AS1299  英国, 伦敦, telia.com
283.06 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
264.97 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
266.00 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
271.60 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
275.01 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
3.05 ms  AS13335  中国, 香港, cloudflare.com
2.92 ms  AS13335  荷兰, 北荷兰省, 阿姆斯特丹, level3.com
3.63 ms  AS13335  荷兰, 北荷兰省, 阿姆斯特丹, cloudflare.com
4.56 ms  *  荷兰, 北荷兰省, 阿姆斯特丹, ams-ix.net
3.90 ms  AS1239  荷兰, 北荷兰省, 阿姆斯特丹, sprint.com
11.93 ms  AS1239  英国, 伦敦, sprint.com
85.29 ms  AS1239  英国, 伦敦, sprint.com
103.65 ms  AS1239  美国, 纽约州, 纽约, sprint.com
106.32 ms  AS1239  美国, 马里兰州, 阿比特斯, sprint.com
87.83 ms  AS1239  美国, 华盛顿, sprint.com
121.84 ms  AS1239  美国, 南卡罗来纳州, 费尔法克斯, sprint.com
125.25 ms  AS1239  美国, 乔治亚州, 亚特兰大, sprint.com
119.21 ms  AS1239  美国, 德克萨斯州, 沃思堡, sprint.com
155.04 ms  AS1239  美国, 加利福尼亚州, 里亚托, sprint.com
144.76 ms  AS1239  美国, 加利福尼亚州, 洛杉矶, sprint.com
298.10 ms  AS1239  美国, 加利福尼亚州, 洛杉矶, sprint.com
309.18 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
310.23 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
305.49 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
317.54 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
318.83 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
309.24 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
2.93 ms  AS13335  中国, 香港, cloudflare.com
2.69 ms  AS13335  荷兰, 北荷兰省, 阿姆斯特丹, level3.com
31.69 ms  AS13335  荷兰, 北荷兰省, 阿姆斯特丹, cloudflare.com
3.92 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
4.00 ms  AS1299  荷兰, 北荷兰省, 阿姆斯特丹, telia.com
10.33 ms  AS1299  英国, 伦敦, telia.com
11.50 ms  AS1299  英国, 伦敦, telia.com
22.93 ms  AS1299  英国, 伦敦, telia.com
228.09 ms  AS58453  中国, 上海, chinamobile.com, 移动
291.51 ms  AS9808  中国, 上海, chinamobile.com, 移动
229.69 ms  AS9808  中国, 上海, chinamobile.com, 移动
290.07 ms  AS9808  中国, 上海, chinamobile.com, 移动
303.18 ms  AS9808  中国, 北京, chinamobile.com, 移动
309.37 ms  AS9808  中国, 北京, chinamobile.com, 移动
307.59 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟
Speedtest.net	 54.50Mbps	 152.56Mbps	 4.89ms	
洛杉矶		 107.15Mbps	 155.72Mbps	 3.58ms	
新加坡		 111.14Mbps	 1.62Mbps	 3.77ms	
联通WuXi	 113.21Mbps	 40.04Mbps	 3.64ms	
联通上海5G	 112.18Mbps	 0.11Mbps	 3.62ms	
电信上海	 113.54Mbps	 119.91Mbps	 3.73ms	
电信Zhenjiang5G	 114.30Mbps	 0.25Mbps	 3.55ms	
移动Chengdu	 113.70Mbps	 77.07Mbps	 3.57ms	
移动杭州5G	 113.70Mbps	 1.58Mbps	 3.60ms	
------------------------------------------------------------------------
 总共花费      : 7 分 22 秒
 时间          : Sun Jul  9 04:28:41 UTC 2023
------------------------------------------------------------------------
```
