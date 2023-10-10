---
title: "Aeza瑞典 测评"
date: "2023-07-13"
categories: 
  - "vps"
  - "eu"
---

## 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 5 3600 6-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 3599.998 MHz
 CPU 缓存          : L1: 128.00 KB / L2: 512.00 KB / L3: 16.00 MB
 硬盘空间          : 2.40 GiB / 9.77 GiB
 启动盘路径        : /dev/vda1
 内存              : 99.88 MiB / 3.84 GiB
 Swap              : 0 KiB / 1024.00 MiB
 系统在线时间      : 0 days, 0 hour 9 min
 负载              : 0.56, 0.21, 0.12
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-21-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS210644 AEZA GROUP Ltd
 IPV4 位置         : Herräng /  / SE
 IPV6 ASN          : AS210644 AEZA GROUP Ltd
 IPV6 位置         : Stockholm / Stockholm County
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1927 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		44585.70 MB/s
 单线程写测试:		18491.44 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		4.1 MB/s (1003 IOPS, 25.51s)		4.1 MB/s (1003 IOPS, 25.51s)
 1GB-1M Block		476 MB/s (454 IOPS, 2.20s)		1.1 GB/s (1095 IOPS, 0.91s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 3.98 MB/s      (995) | 63.76 MB/s     (996)
Write      | 4.00 MB/s     (1.0k) | 64.18 MB/s    (1.0k)
Total      | 7.99 MB/s     (1.9k) | 127.94 MB/s   (1.9k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 498.26 MB/s    (973) | 997.33 MB/s    (973)
Write      | 524.73 MB/s   (1.0k) | 1.06 GB/s     (1.0k)
Total      | 1.02 GB/s     (1.9k) | 2.06 GB/s     (2.0k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: GIGANET
视频缓存节点地域: KBP(KBP9)
Youtube识别地域: 瑞典(SE)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA15S37)
Youtube识别地域: 俄罗斯联邦(RU)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：瑞典
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：瑞典
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：瑞典区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：瑞典区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Available For [Disney+ RU] Soon
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: SE)
 Amazon Prime Video:			Yes (Region: SE)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			INTL
 Viu.com:				No
 YouTube CDN:				Associated with [GIGANET]
 Netflix Preferred CDN:			Stockholm  
 Spotify Registration:			No
 Steam Currency:			RUB
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				No
 Disney+:				Yes (Region: SE)
 Netflix:				Yes (Region: SE)
 YouTube Premium:			No 
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Frankfurt 
 Netflix Preferred CDN:			Stockholm  
 Spotify Registration:			No
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【RU】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：70
  匿名代理: No
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：41
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Fixed Line ISP
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
  qq邮箱：No
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：73
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
2023/07/13 15:02:56 北京电信 219.141.136.12  测试超时
2023/07/13 15:02:56 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/13 15:02:56 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/13 15:02:56 上海电信 202.96.209.133  测试超时
2023/07/13 15:02:56 上海联通 210.22.97.1     联通4837[普通线路]           
2023/07/13 15:02:56 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/13 15:02:56 广州电信 58.60.188.222   电信163 [普通线路]           
2023/07/13 15:02:56 广州联通 210.21.196.6    测试超时
2023/07/13 15:02:56 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/07/13 15:02:56 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/13 15:02:56 成都联通 119.6.6.6       测试超时
2023/07/13 15:02:56 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.43 ms  *  局域网
6.52 ms  AS60068  瑞典, 斯德哥尔摩省, 斯德哥尔摩, datacamp.co.uk
6.68 ms  AS60068  瑞典, 斯德哥尔摩省, 斯德哥尔摩, datacamp.co.uk
6.64 ms  *  瑞典, 斯德哥尔摩省, 斯德哥尔摩, datacamp.co.uk
7.84 ms  AS1299  瑞典, 斯德哥尔摩省, 斯德哥尔摩, telia.com
24.29 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
24.26 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
229.02 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
232.86 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.38 ms  *  局域网
6.75 ms  AS60068  瑞典, 斯德哥尔摩省, 斯德哥尔摩, datacamp.co.uk
7.43 ms  AS60068  瑞典, 斯德哥尔摩省, 斯德哥尔摩, datacamp.co.uk
7.64 ms  *  瑞典, 斯德哥尔摩省, 斯德哥尔摩, datacamp.co.uk
广州移动 120.196.165.24
0.11 ms  *  局域网
6.61 ms  AS60068  瑞典, 斯德哥尔摩省, 斯德哥尔摩, datacamp.co.uk
6.22 ms  AS60068  瑞典, 斯德哥尔摩省, 斯德哥尔摩, datacamp.co.uk
6.37 ms  *  瑞典, 斯德哥尔摩省, 斯德哥尔摩, datacamp.co.uk
7.05 ms  AS201011  瑞典, 斯德哥尔摩省, 斯德哥尔摩, core-backbone.com
22.99 ms  AS201011  德国, 黑森州, 法兰克福, core-backbone.com
37.65 ms  *  德国, 黑森州, 法兰克福, de-cix.net
38.78 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
300.35 ms  AS58453  中国, 上海, chinamobile.com, 移动
294.17 ms  AS9808  中国, 上海, chinamobile.com, 移动
306.91 ms  AS9808  中国, 上海, chinamobile.com, 移动
303.02 ms  AS9808  中国, 上海, chinamobile.com, 移动
327.91 ms  AS9808  中国, 北京, chinamobile.com, 移动
330.73 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 537.05 Mbps	 411.16 Mbps	 6.31	  5.6%
洛杉矶		 504.01 Mbps	 335.83 Mbps	 174.89	  0.0%
电信天津5G	 7.13 Mbps	 96.81 Mbps	 195.43	  13.9%
电信合肥5G	 14.81 Mbps	 9.59 Mbps	 474.31	  12.4%
移动Beijing	 479.70 Mbps	 398.54 Mbps	 222.96	  7.0%
------------------------------------------------------------------------
 总共花费      : 7 分 47 秒
 时间          : Thu Jul 13 15:07:40 CEST 2023
------------------------------------------------------------------------
```

## Yabs

```
root@sa:~# curl -sL yabs.sh | bash
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2023-04-23                    #
# https://github.com/masonr/yet-another-bench-script #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

Thu 13 Jul 2023 03:14:44 PM CEST

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 24 minutes
Processor  : AMD Ryzen 5 3600 6-Core Processor
CPU cores  : 1 @ 3599.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 1024.0 MiB
Disk       : 9.8 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-21-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : AEZA GROUP Ltd
ASN        : AS210644 AEZA GROUP Ltd
Host       : Aeza Network Stockholm
Location   : Stockholm, Stockholm County (AB)
Country    : Sweden

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.98 MB/s      (996) | 63.74 MB/s     (996)
Write      | 4.01 MB/s     (1.0k) | 64.15 MB/s    (1.0k)
Total      | 7.99 MB/s     (1.9k) | 127.90 MB/s   (1.9k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 498.75 MB/s    (974) | 996.84 MB/s    (973)
Write      | 525.25 MB/s   (1.0k) | 1.06 GB/s     (1.0k)
Total      | 1.02 GB/s     (1.9k) | 2.06 GB/s     (2.0k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 547 Mbits/sec   | 328 Mbits/sec   | 32.0 ms        
Scaleway        | Paris, FR (10G)           | 547 Mbits/sec   | 332 Mbits/sec   | 34.3 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 26.1 ms        
Uztelecom       | Tashkent, UZ (10G)        | 512 Mbits/sec   | 297 Mbits/sec   | 115 ms         
Clouvider       | NYC, NY, US (10G)         | busy            | 33.9 Mbits/sec  | 102 ms         
Clouvider       | Dallas, TX, US (10G)      | 508 Mbits/sec   | 131 Mbits/sec   | 139 ms         
Clouvider       | Los Angeles, CA, US (10G) | 484 Mbits/sec   | 212 Mbits/sec   | 163 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 501 Mbits/sec   | 60.5 Mbits/sec  | 32.0 ms        
Scaleway        | Paris, FR (10G)           | 510 Mbits/sec   | 39.0 Mbits/sec  | -- 
NovoServe       | North Holland, NL (40G)   | 515 Mbits/sec   | 320 Mbits/sec   | 81.4 ms        
Uztelecom       | Tashkent, UZ (10G)        | 470 Mbits/sec   | 55.8 Mbits/sec  | 114 ms         
Clouvider       | NYC, NY, US (10G)         | 456 Mbits/sec   | 4.07 Mbits/sec  | 104 ms         
Clouvider       | Dallas, TX, US (10G)      | 451 Mbits/sec   | 12.2 Mbits/sec  | 139 ms         
Clouvider       | Los Angeles, CA, US (10G) | 441 Mbits/sec   | 26.8 Mbits/sec  | 163 ms         

Geekbench 6 test failed. Run manually to determine cause.

YABS completed in 10 min 42 sec
```
