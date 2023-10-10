---
title: "Aeza Stockholm AMD 7950X3D 测评"
date: "2023-09-09"
categories: 
  - "vps"
  - "performance"
  - "eu"
---

很容易开出被墙IP,不是很推荐购买

> ## 套餐

![](https://catcat.blog/wp-content/uploads/2023/09/image-55-1024x444.png)

## 测评

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 28 minutes
Processor  : AMD Ryzen 9 7950X3D 16-Core Processor
CPU cores  : 1 @ 4192.100 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ❌ Disabled
RAM        : 1.9 GiB
Swap       : 1024.0 MiB
Disk       : 29.4 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-10-amd64
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
Read       | 40.02 MB/s   (10.0k) | 657.13 MB/s  (10.2k)
Write      | 40.12 MB/s   (10.0k) | 660.58 MB/s  (10.3k)
Total      | 80.15 MB/s   (20.0k) | 1.31 GB/s    (20.5k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.05 GB/s     (5.9k) | 3.34 GB/s     (3.2k)
Write      | 3.22 GB/s     (6.2k) | 3.57 GB/s     (3.4k)
Total      | 6.27 GB/s    (12.2k) | 6.92 GB/s     (6.7k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 113 Mbits/sec   | busy            | 32.4 ms        
Scaleway        | Paris, FR (10G)           | 872 Mbits/sec   | 770 Mbits/sec   | 38.1 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 27.1 ms        
Uztelecom       | Tashkent, UZ (10G)        | 831 Mbits/sec   | 531 Mbits/sec   | 122 ms         
Clouvider       | NYC, NY, US (10G)         | 13.9 Mbits/sec  | 16.6 Mbits/sec  | 110 ms         
Clouvider       | Dallas, TX, US (10G)      | 21.7 Mbits/sec  | 27.8 Mbits/sec  | 140 ms         
Clouvider       | Los Angeles, CA, US (10G) | 22.0 Mbits/sec  | 30.4 Mbits/sec  | 166 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 117 Mbits/sec   | 126 Mbits/sec   | 32.5 ms        
Scaleway        | Paris, FR (10G)           | busy            | 472 Mbits/sec   | 44.9 ms        
NovoServe       | North Holland, NL (40G)   | 853 Mbits/sec   | busy            | 26.8 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | 218 Mbits/sec   | 123 ms         
Clouvider       | NYC, NY, US (10G)         | 28.7 Mbits/sec  | 24.1 Mbits/sec  | 103 ms         
Clouvider       | Dallas, TX, US (10G)      | 26.0 Mbits/sec  | 31.0 Mbits/sec  | 140 ms         
Clouvider       | Los Angeles, CA, US (10G) | 22.2 Mbits/sec  | 8.55 Mbits/sec  | 166 ms 

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2628                          
Multi Core      | 2647                          
Full Test       | https://browser.geekbench.com/v6/cpu/2547625

YABS completed in 14 min 1 sec        
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 4192.100 MHz
 CPU 缓存          : L1: 64.00 KB / L2: 512.00 KB / L3: 16.00 MB
 硬盘空间          : 7.59 GiB / 29.45 GiB
 启动盘路径        : /dev/vda1
 内存              : 136.24 MiB / 1.92 GiB
 Swap              : 1.90 MiB / 1024.00 MiB
 系统在线时间      : 0 days, 0 hour 43 min
 负载              : 0.32, 0.38, 0.23
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-10-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS210644 AEZA GROUP Ltd
 IPV4 位置         : Herräng / Stockholm / SE
 IPV6 ASN          : AS210644 AEZA GROUP Ltd
 IPV6 位置         : Stockholm / Stockholm County
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		5687 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		68862.52 MB/s
 单线程写测试:		39253.34 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		42.6 MB/s (10.40 IOPS, 2.46s)		42.6 MB/s (10401 IOPS, 2.46s)
 1GB-1M Block		4.9 GB/s (4638 IOPS, 0.22s)		4.4 GB/s (4226 IOPS, 0.24s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 40.03 MB/s   (10.0k) | 657.13 MB/s  (10.2k)
Write      | 40.12 MB/s   (10.0k) | 660.58 MB/s  (10.3k)
Total      | 80.16 MB/s   (20.0k) | 1.31 GB/s    (20.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.13 GB/s     (6.1k) | 3.41 GB/s     (3.3k)
Write      | 3.30 GB/s     (6.4k) | 3.63 GB/s     (3.5k)
Total      | 6.44 GB/s    (12.5k) | 7.04 GB/s     (6.8k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: GIGANET
视频缓存节点地域: KBP(KBP9)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 德国汉堡(HAM11S06)
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
 Dazn:					Yes (Region: SE)
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Failed
 Amazon Prime Video:			Yes (Region: SE)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			INTL
 Viu.com:				No
 YouTube CDN:				GIGANET in Kiev 
 Netflix Preferred CDN:			Stockholm  
 Spotify Registration:			Yes (Region: SE)
 Steam Currency:			EUR
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
 YouTube CDN:				Hamburg 
 Netflix Preferred CDN:			Stockholm  
 Spotify Registration:			Yes (Region: SE)
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【RU】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 72②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Fixed Line ISP⑤  hosting⑧  business⑨  
  公司类型(company_type):hosting①  isp⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  No② ⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ② ⑥ ⑦ ⑧ ⑨ 
  VPN(vpn):  No① ② ⑦ ⑧ 
  TOR(tor):  No① ② ⑦ ⑧ ⑨ 
  TOR出口(tor_exit):  No⑧ 
  搜索引擎机器人(search_engine_robot):  No② 
  匿名代理(anonymous):  No⑦ ⑧ ⑨ 
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
  yandex邮箱: Yes
  qq邮箱：No
------以下为IPV6检测------
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: SE 城市: Herräng 服务商: AS210644 AEZA GROUP Ltd
北京电信 219.141.136.12  电信163 [普通线路]           
北京联通 202.106.50.1    联通4837[普通线路]           
北京移动 221.179.155.161 移动CMI [普通线路]           
上海电信 202.96.209.133  电信163 [普通线路]           
上海联通 210.22.97.1     联通4837[普通线路]           
上海移动 211.136.112.200 移动CMI [普通线路]           
广州电信 58.60.188.222   电信163 [普通线路]           
广州联通 210.21.196.6    联通4837[普通线路]           
广州移动 120.196.165.24  移动CMI [普通线路]           
成都电信 61.139.2.69     电信163 [普通线路]           
成都联通 119.6.6.6       联通4837[普通线路]           
成都移动 211.137.96.205  移动CMI [普通线路]           
2023/09/09 19:04:34 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.16 ms 	* RFC1918
6.21 ms 	AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
6.42 ms 	AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
6.35 ms 	* [CDN77-PEERLINKS] 瑞典 斯德哥尔摩省 斯德哥尔摩
6.89 ms 	AS1299 [ARELION-NET] 瑞典 斯德哥尔摩省 斯德哥尔摩 arelion.com
7.28 ms 	AS1299 [ARELION-NET] 瑞典 斯德哥尔摩省 斯德哥尔摩 arelion.com
25.73 ms 	AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
25.71 ms 	AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
87.45 ms 	AS4134 [CHINANET-BB] 德国 黑森州 美因河畔法兰克福 CT-POP chinatelecom.com.cn 电信
* ms 	AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.12 ms 	* RFC1918
6.17 ms 	AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
6.31 ms 	AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
6.37 ms 	* [CDN77-PEERLINKS] 瑞典 斯德哥尔摩省 斯德哥尔摩
7.08 ms 	AS1299 [ARELION-NET] 瑞典 斯德哥尔摩省 斯德哥尔摩 arelion.com
23.69 ms 	AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
24.02 ms 	AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
427.69 ms 	AS4837 [CU169-BACKBONE] 德国 黑森州 美茵河畔法兰克福 chinaunicom.cn 联通
广州移动 120.196.165.24
0.10 ms 	* RFC1918
6.30 ms 	AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
6.16 ms 	AS60068 瑞典 斯德哥尔摩省 斯德哥尔摩 cdn77.com
6.43 ms 	* [CDN77-PEERLINKS] 瑞典 斯德哥尔摩省 斯德哥尔摩
6.69 ms 	AS201011 瑞典 斯德哥尔摩省 斯德哥尔摩 core-backbone.com
22.84 ms 	AS201011 德国 黑森州 美因河畔法兰克福 core-backbone.com
45.58 ms 	AS58453 [DE-CIX] 德国 黑森州 美因河畔法兰克福 DE-CIX Frankfurt - China Mobile International - 100Gbps cmi.chinamobile.com
44.92 ms 	AS58453 [CMI-INT] 德国 黑森州 美茵河畔法兰克福 cmi.chinamobile.com 移动
297.78 ms 	AS58453 [CMI-INT] 德国 黑森州 美因河畔法兰克福 cmi.chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 905.65 Mbps	 906.47 Mbps	 7.81	  NULL
法兰克福	 877.87 Mbps	 836.11 Mbps	 27.36	  1.3%
洛杉矶		 457.71 Mbps	 644.64 Mbps	 190.14	  0.0%
------------------------------------------------------------------------
 总共花费      : 4 分 36 秒
 时间          : Sat Sep  9 19:07:29 MSK 2023
------------------------------------------------------------------------
```

### Bench

```
Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Debian GNU/Linux 12 (bookworm)     Model       : AMD Ryzen 9 7950X3D 16-Core Processor
Location   : Sweden                             Core        : 1 @ 4192.100 MHz
Kernel     : 6.1.0-10-amd64                     AES-NI      : ✔ Enabled
Uptime     : 0 days, 0 hrs, 49 mins, 7 secs     VM-x/AMD-V  : ❌ Disabled
Virt       : kvm                                Swap        : 1024.0 MiB

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 29.4 GiB                           ASN         : AS210644  
Disk Usage : 7.6 GiB (26% Used)                 ISP         : AEZA GROUP Ltd
Mem        : 1.9 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.2 GiB (11% Used)                 IPv6        : ❌ Disabled

Disk Performance Check (ext4 on /dev/vda1) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 39.09 MB/s  | 39.18 MB/s  | 78.28 MB/s  | 10.0k  | 10.0k  | 20.0k  |
| 64k  | 641.32 MB/s | 644.70 MB/s | 1.25 GB/s   | 10.3k  | 10.3k  | 20.6k  |
| 512k | 2.92 GB/s   | 3.08 GB/s   | 6.00 GB/s   | 6.0k   | 6.3k   | 12.3k  |
| 1m   | 3.28 GB/s   | 3.49 GB/s   | 6.77 GB/s   | 3.4k   | 3.6k   | 6.9k   |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |  731.2 Mb/s  |  151.2 Mb/s  |  130.8 ms |
|       | Uztelecom   | Tashkent, UZ    |        busy  |        busy  |  124.0 ms |
|       | Novogara    | Amsterdam, NL   |  896.9 Mb/s  |  895.8 Mb/s  |   28.9 ms |
|       | FiberBy     | Copenhagen, DK  |  728.1 Mb/s  |  607.4 Mb/s  |   16.9 ms |
+---------------------------------------------------------------------------------+

+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 2642                     |
| Multi Core         | 2632                     |
+-----------------------------------------------+
| https://browser.geekbench.com/v6/cpu/2547883  |
+-----------------------------------------------+
| Benchy time spent  | 8 Minutes 43 Seconds     |
+-----------------------------------------------+
| Benchy result      | http://sprunge.us/m4dgTV |
+-----------------------------------------------+
```

### 全球延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-56.png)
