---
title: "op法国杜甫 测评"
date: "2023-06-18"
categories: 
  - "vps"
  - "eu"
---

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : Intel(R) Xeon(R) CPU E3-1240 V2 @ 3.40GHz
 CPU 核心数        : 8
 CPU 频率          : 3591.323 MHz
 CPU 缓存          : 8192 KB
 硬盘空间          : 1946.2 GB (5.6 GB 已用)
 内存              : 32080 MB (10594 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 123 days, 13 hour 29 min
 负载              : 0.13, 0.23, 0.84
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.0.0-0.deb11.6-amd64
 TCP加速方式       : bbrx
 虚拟化架构        : dedicated
 NAT类型           : 开放型
 ASN组织           : AS12876 SCALEWAY S.A.S.
 位置              : Paris / FR
 地区              : Île-de-France
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1056 Scores
 8 线程测试(多核)得分: 		6622 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		23206.47 MB/s
 单线程写测试:		17730.84 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		84.4 MB/s (0.05 IOPS, 1.24s)		87.0 MB/s (21240 IOPS, 1.21s)
 1GB-1M Block		372 MB/s (355 IOPS, 2.82s)		416 MB/s (396 IOPS, 2.52s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 106.48 MB/s  (26.6k) | 118.76 MB/s   (1.8k)
Write      | 106.76 MB/s  (26.6k) | 119.39 MB/s   (1.8k)
Total      | 213.24 MB/s  (53.3k) | 238.16 MB/s   (3.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 104.62 MB/s    (204) | 113.32 MB/s    (110)
Write      | 110.18 MB/s    (215) | 120.87 MB/s    (118)
Total      | 214.80 MB/s    (419) | 234.20 MB/s    (228)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: PAR(PAR21S25)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：法国
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：法国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: FR)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: FR)
 Amazon Prime Video:			Yes (Region: FR)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			FR
 Viu.com:				No
 YouTube CDN:				Paris 
 Netflix Preferred CDN:			Paris  
 Spotify Registration:			Yes (Region: FR)
 Steam Currency:			EUR
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【FR】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：34
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：39
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/06/18 14:42:04 北京电信 219.141.136.12  电信163 [普通线路]           
2023/06/18 14:42:04 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/18 14:42:04 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/18 14:42:04 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/18 14:42:04 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/18 14:42:04 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/18 14:42:04 广州电信 58.60.188.222   测试超时
2023/06/18 14:42:04 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/18 14:42:04 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/18 14:42:04 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/18 14:42:04 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/18 14:42:04 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS12876 Scaleway
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.72 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
0.67 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
0.45 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
1.48 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
15.18 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
16.47 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
213.59 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
207.86 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.68 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
0.59 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
0.51 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
1.20 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
1.54 ms  AS3356  法国, 法兰西岛大区, 巴黎, level3.com
140.75 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
253.08 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
269.84 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
283.11 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
287.10 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
331.25 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
296.32 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.60 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
0.89 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
0.46 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
1.27 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
1.70 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
1.75 ms  AS12876  法国, 法兰西岛大区, 巴黎, scaleway.com
9.49 ms  AS58453  英国, 伦敦, chinamobile.com, 移动
250.34 ms  AS58453  中国, 上海, chinamobile.com, 移动
283.52 ms  AS9808  中国, 上海, chinamobile.com, 移动
240.07 ms  AS9808  中国, 上海, chinamobile.com, 移动
284.94 ms  AS9808  中国, 上海, chinamobile.com, 移动
277.65 ms  AS9808  中国, 北京, chinamobile.com, 移动
279.14 ms  AS9808  中国, 北京, chinamobile.com, 移动
309.42 ms  AS9808  中国, 北京, chinamobile.com, 移动
320.73 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 949.07 Mbps	 934.75 Mbps	 1.07	  0.0%
洛杉矶		 648.82 Mbps	 14.82 Mbps	 136.44	  0.0%
新加坡		 492.80 Mbps	 11.72 Mbps	 156.11	  0.0%
联通海南	 481.51 Mbps	 8.60 Mbps	 196.21	  NULL
联通湖南5G	 495.34 Mbps	 6.73 Mbps	 202.61	  NULL
电信合肥5G	 145.70 Mbps	 9.59 Mbps	 192.45	  6.3%
移动Chengdu	 361.22 Mbps	 7.35 Mbps	 239.72	  0.0%
移动Zhengzhou5G	 274.27 Mbps	 4.42 Mbps	 257.06	  0.0%
------------------------------------------------------------------------
 总共花费      : 7 分 2 秒
 时间          : Sun Jun 18 14:46:41 CST 2023
------------------------------------------------------------------------
```

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : Intel(R) Xeon(R) CPU E3-1240 V2 @ 3.40GHz
 CPU Cores          : 8 @ 3648.482 MHz
 CPU Cache          : 8192 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 1.8 TB (13.5 GB Used)
 Total Mem          : 31.3 GB (10.4 GB Used)
 System uptime      : 123 days, 14 hour 28 min
 Load average       : 0.13, 0.16, 0.17
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.0.0-0.deb11.6-amd64
 TCP CC             : bbrx
 Virtualization     : Dedicated
 IPv4/IPv6          : Online / Online
 Organization       : AS12876 SCALEWAY S.A.S.
 Location           : Paris / FR
 Region             : Île-de-France
----------------------------------------------------------------------
 I/O Speed(1st run) : 371 MB/s
 I/O Speed(2nd run) : 186 MB/s
 I/O Speed(3rd run) : 153 MB/s
 I/O Speed(average) : 236.7 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    891.81 Mbps       902.67 Mbps         1.44 ms     
 Los Angeles, US  591.72 Mbps       912.54 Mbps         150.74 ms   
 Dallas, US       569.03 Mbps       909.23 Mbps         123.03 ms   
 Montreal, CA     774.07 Mbps       907.34 Mbps         92.86 ms    
 Paris, FR        926.51 Mbps       835.23 Mbps         1.39 ms     
 Amsterdam, NL    851.90 Mbps       876.90 Mbps         13.77 ms    
 Shanghai, CN     452.05 Mbps       629.72 Mbps         275.31 ms   
 Nanjing, CN      439.45 Mbps       852.80 Mbps         226.86 ms   
 Hongkong, CN     681.50 Mbps       830.52 Mbps         252.80 ms   
 Singapore, SG    275.68 Mbps       202.97 Mbps         238.84 ms   
 Tokyo, JP        354.98 Mbps       894.00 Mbps         228.99 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 33 sec
 Timestamp          : 2023-06-18 15:43:17 CST
----------------------------------------------------------------------
```
