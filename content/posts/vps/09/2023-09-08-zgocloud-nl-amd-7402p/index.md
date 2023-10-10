---
title: "Zgocloud 荷兰AMD 7402P测评"
date: "2023-09-08"
categories: 
  - "vps"
  - "eu"
  - "special"
---

总结：没啥性价比，流量过小，性能一般。欧洲荷兰只给2T流量真挺莫名其妙的。

> ## 套餐
> 
> 2 Core AMD EPYC 7402P  
> 2GB DDR4 ECC RAM  
> 25G SSD  
> 1 IPV4 & /64 IPV6  
> Netherlands  
> 2TB/Month/1000Mbps  
> 40 Gbit/s Anti-DDoS included  
> No refund/money back on this plan

## 测评

### 融合怪脚本

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7402P 24-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 2794.750 MHz
 CPU 缓存          : L1: 128.00 KB / L2: 1.00 MB / L3: 256.00 MB
 硬盘空间          : 1.22 GiB / 23.50 GiB
 启动盘路径        : /dev/sda1
 内存              : 213.62 MiB / 1.90 GiB
 Swap              : 0 KiB / 975.00 MiB
 系统在线时间      : 0 days, 0 hour 3 min
 负载              : 0.35, 0.09, 0.03
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-25-cloud-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS197767 ZgoShop, Inc.
 IPV4 位置         : Boulder / Colorado / US
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1647 Scores
 2 线程测试(多核)得分: 		3263 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		43894.58 MB/s
 单线程写测试:		18800.05 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		44.7 MB/s (10.85 IOPS, 2.36s)		50.6 MB/s (12269 IOPS, 2.09s)
 1GB-1M Block		283 MB/s (260 IOPS, 3.84s)		1.7 GB/s (1489 IOPS, 0.67s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 161.75 MB/s  (40.6k) | 1.31 GB/s    (21.0k)
Write      | 165.68 MB/s  (40.7k) | 1.33 GB/s    (21.1k)
Total      | 327.43 MB/s  (81.3k) | 2.64 GB/s    (42.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.21 GB/s     (2.1k) | 1.50 GB/s     (1.4k)
Write      | 1.16 GB/s     (2.2k) | 1.59 GB/s     (1.5k)
Total      | 2.37 GB/s     (4.4k) | 3.09 GB/s     (3.0k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS15S45)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS15S45)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
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
 Dazn:					Yes (Region: US)
 HotStar:				Yes (Region: US)
 Disney+:				Yes (Region: US)
 Netflix:				Yes (Region: US)
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				Amsterdam 
 Netflix Preferred CDN:			Dallas, TX  
 Spotify Registration:			No
 Steam Currency:			USD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				Yes (Region: US)
 Disney+:				Yes (Region: US)
 Netflix:				Yes (Region: US)
 YouTube Premium:			Yes
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Amsterdam 
 Netflix Preferred CDN:			Dallas, TX  
 Spotify Registration:			Yes (Region: US)
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		Failed
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):business①  Commercial⑤  business⑧  
  公司类型(company_type):business①  business⑧  
  云服务提供商(cloud_provider):  No⑧ 
  数据中心(datacenter):  No② ⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ② ⑥ ⑦ ⑧ ⑨ ⑩ 
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
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测87 ③
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
  qq邮箱: Yes
------以下为IPV6检测------
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: Commercial⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: US 城市: Boulder 服务商: AS197767 ZgoShop, Inc.
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
2023/09/08 19:54:13 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.93 ms 	AS197767 美国 科罗拉多州州 博尔德
0.50 ms 	AS49981 [NL-WORLDSTREAM] 荷兰 北荷兰省 阿姆斯特丹 worldstream.com
13.10 ms 	AS174 [COGENT-BONE] 荷兰 北荷兰省 阿姆斯特丹 cogentco.com
9.03 ms 	AS174 [COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
9.44 ms 	AS174 [COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
143.73 ms 	AS174 [COGENT-149] 德国 黑森州 美因河畔法兰克福 Cogent-CT-Peer cogentco.com
363.38 ms 	AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
368.45 ms 	AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.41 ms 	AS197767 美国 科罗拉多州州 博尔德
0.53 ms 	AS49981 [NL-WORLDSTREAM] 荷兰 北荷兰省 阿姆斯特丹 worldstream.com
9.00 ms 	AS49981 [NL-WORLDSTREAM] 德国 黑森州 美因河畔法兰克福 worldstream.com
12.68 ms 	AS49981 [NL-WORLDSTREAM] 德国 黑森州 美因河畔法兰克福 worldstream.com
9.02 ms 	AS6830 [NL-CHELLO] 德国 黑森州 美因河畔法兰克福 libertyglobal.com
165.51 ms 	AS6830 德国 黑森州 美因河畔法兰克福 libertyglobal.com
119.92 ms 	AS6830 美国 佛罗里达州 迈阿密 libertyglobal.com
162.47 ms 	AS6830 美国 加利福尼亚州 圣何塞 libertyglobal.com
243.48 ms 	AS4837 [CU169-BACKBONE] 美国 加利福尼亚州 圣何塞 chinaunicom.cn 联通
264.89 ms 	AS4837 [CU169-BACKBONE] 中国 北京市 chinaunicom.cn 联通
277.62 ms 	AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
282.27 ms 	AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
386.57 ms 	AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
284.55 ms 	AS17816 [UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
292.21 ms 	AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
281.82 ms 	AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
1.29 ms 	AS197767 美国 科罗拉多州州 博尔德
0.56 ms 	AS49981 [NL-WORLDSTREAM] 荷兰 北荷兰省 阿姆斯特丹 worldstream.com
1.50 ms 	AS49981 [NL-WORLDSTREAM] 荷兰 北荷兰省 阿姆斯特丹 worldstream.com
2.27 ms 	AS201011 荷兰 北荷兰省 阿姆斯特丹 core-backbone.com
8.55 ms 	AS201011 英国 英格兰 伦敦 core-backbone.com
76.40 ms 	AS25577 [LINX-PEER] 英国 英格兰 伦敦 cloudcoco.co.uk
261.21 ms 	AS58453 [CMI-INT] 英国 英格兰 伦敦 cmi.chinamobile.com 移动
356.64 ms 	AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
283.20 ms 	AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
293.63 ms 	AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
328.14 ms 	AS9808 [CMNET] 中国 北京市 chinamobile.com 移动
318.40 ms 	AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 781.89 Mbps	 983.35 Mbps	 36.63	  0.0%
法兰克福	 934.39 Mbps	 978.16 Mbps	 12.81	  0.0%
洛杉矶		 675.64 Mbps	 982.25 Mbps	 153.52	  0.0%
联通沈阳	 243.52 Mbps	 200.92 Mbps	 147.56	  0.0%
联通湖南5G	 369.05 Mbps	 1.69 Mbps	 263.75	  NULL
电信天津	 33.97 Mbps	 36.66 Mbps	 269.91	  NULL
```

### Yabs

```
---------------------------------
Uptime     : 0 days, 0 hours, 32 minutes
Processor  : AMD EPYC 7402P 24-Core Processor
CPU cores  : 2 @ 2794.750 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 935.0 MiB
Disk       : 23.7 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-25-cloud-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

##IPv6 Network Information:
---------------------------------
ISP        : Ayaka Tech LLC
ASN        : Unknown
Host       : Ayaka Tech LLC
Location   : London, England (ENG)
Country    : United Kingdom

##fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Read       | 161.75 MB/s  (40.6k) | 1.31 GB/s    (21.0k)
Write      | 165.68 MB/s  (40.7k) | 1.33 GB/s    (21.1k)
Total      | 327.43 MB/s  (81.3k) | 2.64 GB/s    (42.1k)                                                 
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.21 GB/s     (2.1k) | 1.50 GB/s     (1.4k)
Write      | 1.16 GB/s     (2.2k) | 1.59 GB/s     (1.5k)
Total      | 2.37 GB/s     (4.4k) | 3.09 GB/s     (3.0k)

##iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 894 Mbits/sec   | 945 Mbits/sec   | 7.61 ms        
Scaleway        | Paris, FR (10G)           | 956 Mbits/sec   | 939 Mbits/sec   | 9.90 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 2.67 ms        
Uztelecom       | Tashkent, UZ (10G)        | 813 Mbits/sec   | 892 Mbits/sec   | 97.9 ms        
Clouvider       | NYC, NY, US (10G)         | busy            | 101.6 Mbits/sec | 77.6 ms        
Clouvider       | Dallas, TX, US (10G)      | 13.8 Mbits/sec  | 24.6 Mbits/sec  | 165 ms         
Clouvider       | Los Angeles, CA, US (10G) | 21.1 Mbits/sec  | 31.2 Mbits/sec  | 181 ms         

##iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 503 Mbits/sec   | 773 Mbits/sec   | 7.68 ms        
Scaleway        | Paris, FR (10G)           | 963 Mbits/sec   | 927 Mbits/sec   | 10.1 ms        
NovoServe       | North Holland, NL (40G)   | 967 Mbits/sec   | 989 Mbits/sec   | 2.22 ms        
Uztelecom       | Tashkent, UZ (10G)        | 769 Mbits/sec   | 834 Mbits/sec   | 97.8 ms        
Clouvider       | NYC, NY, US (10G)         | 13.6 Mbits/sec  | 46.7 Mbits/sec  | 78.6 ms        
Clouvider       | Dallas, TX, US (10G)      | 32.8 Mbits/sec  | 88.8 Mbits/sec  | 194 ms         
Clouvider       | Los Angeles, CA, US (10G) | 29.6 Mbits/sec  | 43.6 Mbits/sec  | 173 ms 

Geekbench 6 Benchmark Test:
--------------------------------- 
Test            | Value                         
                |                               
Single Core     | 1336                         
Multi Core      | 2689          
```
