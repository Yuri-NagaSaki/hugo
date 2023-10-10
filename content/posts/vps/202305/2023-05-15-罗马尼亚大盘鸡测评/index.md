---
title: "罗马尼亚6T超大盘鸡测评"
date: "2023-05-15"
categories: 
  - "vps"
  - "eu"
---

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : Intel(R) Xeon(R) CPU E5-2670 v2 @ 2.50GHz
 CPU 核心数        : 4
 CPU 频率          : 2499.998 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 5735.3 GB (1.5 GB 已用)
 内存              : 5884 MB (81 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 8 min
 负载              : 1.34, 0.78, 0.36
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS9050 ORANGE ROMANIA COMMUNICATION S.A
 位置              : Eindhoven / NL
 地区              : North Brabant
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		745 Scores
 4 线程测试(多核)得分: 		3203 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		16942.07 MB/s
 单线程写测试:		13449.31 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		17.9 MB/s (4366 IOPS, 5.86s)		19.1 MB/s (4654 IOPS, 5.50s)
 1GB-1M Block		652 MB/s (621 IOPS, 1.61s)		712 MB/s (679 IOPS, 1.47s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 1.54 MB/s      (385) | 26.62 MB/s     (415)
Write      | 1.57 MB/s      (393) | 27.06 MB/s     (422)
Total      | 3.11 MB/s      (778) | 53.69 MB/s     (837)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 101.94 MB/s    (199) | 654.06 MB/s    (638)
Write      | 107.35 MB/s    (209) | 697.62 MB/s    (681)
Total      | 209.29 MB/s    (408) | 1.35 GB/s     (1.3k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：罗马尼亚
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：罗马尼亚区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: US)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: RO)
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				Associated with [ROMTELE]
 Netflix Preferred CDN:			Associated with [Orange Romania Communications] in [Bucharest]
 Spotify Registration:			Yes (Region: US)
 Steam Currency:			USD
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【US】
---------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化---------
[IPv4]
Your IP supports access to OpenAI. Region: US
[IPv6]
IPv6 is not supported on the current host. Skip...
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：15
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：60
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/05/15 08:15:44 北京电信 219.141.136.12  电信163 [普通线路]           
2023/05/15 08:15:44 北京联通 202.106.50.1    联通4837[普通线路]           
2023/05/15 08:15:44 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/05/15 08:15:44 上海电信 202.96.209.133  电信163 [普通线路]           
2023/05/15 08:15:44 上海联通 210.22.97.1     联通4837[普通线路]           
2023/05/15 08:15:44 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/05/15 08:15:44 广州电信 58.60.188.222   电信163 [普通线路]           
2023/05/15 08:15:44 广州联通 210.21.196.6    联通4837[普通线路]           
2023/05/15 08:15:44 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/05/15 08:15:44 成都电信 61.139.2.69     电信163 [普通线路]           
2023/05/15 08:15:44 成都联通 119.6.6.6       联通4837[普通线路]           
2023/05/15 08:15:44 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS9050 Orange Romania Communications
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
40.26 ms  AS9050  罗马尼亚, 苏恰瓦县, legaconetworks.nl
2.62 ms  AS9050  罗马尼亚, 苏恰瓦县, telekom.ro
5.29 ms  *  局域网
23.19 ms  *  局域网
24.45 ms  *  局域网
24.38 ms  *  局域网
22.93 ms  AS6762  德国, 黑森州, 法兰克福, tisparkle.com
22.67 ms  AS6762  德国, 黑森州, 法兰克福, tisparkle.com
24.72 ms  AS6762  德国, 黑森州, 法兰克福, tisparkle.com
214.91 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
225.25 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
2.58 ms  AS9050  罗马尼亚, 苏恰瓦县, legaconetworks.nl
3.25 ms  AS9050  罗马尼亚, 苏恰瓦县, telekom.ro
6.19 ms  *  局域网
24.08 ms  *  局域网
25.05 ms  *  局域网
25.31 ms  *  局域网
26.96 ms  AS3257  德国, 黑森州, 法兰克福, gtt.net
26.79 ms  AS3257  德国, 黑森州, 法兰克福, gtt.net
25.12 ms  AS4837  德国, 黑森州, 法兰克福, chinaunicom.com, 联通
192.80 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
179.36 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
197.57 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
180.84 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
1.65 ms  AS9050  罗马尼亚, 苏恰瓦县, legaconetworks.nl
4.18 ms  AS9050  罗马尼亚, 苏恰瓦县, telekom.ro
6.07 ms  *  局域网
24.11 ms  *  局域网
25.52 ms  *  局域网
29.28 ms  *  局域网
24.65 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
27.16 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
26.58 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
26.78 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
43.70 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
292.93 ms  AS58453  中国, 上海, chinamobile.com, 移动
295.65 ms  AS9808  中国, 上海, chinamobile.com, 移动
293.54 ms  AS9808  中国, 上海, chinamobile.com, 移动
214.28 ms  AS9808  中国, 北京, chinamobile.com, 移动
306.06 ms  AS9808  中国, 北京, chinamobile.com, 移动
308.23 ms  AS9808  中国, 北京, chinamobile.com, 移动
308.26 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 266.05 Mbps	 551.91 Mbps	 108.14	  0.0%
联通上海5G	 196.60 Mbps	 545.48 Mbps	 206.13	  0.0%
联通郑州5G	 135.86 Mbps	 516.53 Mbps	 259.89	  NULL
电信天津5G	 4.06 Mbps	 162.98 Mbps	 227.87	  35.7%
电信天津	 3.75 Mbps	 542.35 Mbps	 174.40	  NULL
移动杭州5G	 200.29 Mbps	 340.95 Mbps	 315.96	  0.0%
移动Chengdu	 209.41 Mbps	 531.56 Mbps	 288.12	  0.0%
------------------------------------------------------------------------
 总共花费      : 8 分 27 秒
 时间          : Mon May 15 08:20:27 EDT 2023
```

## Yabs

```
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2023-04-23                    #
# https://github.com/masonr/yet-another-bench-script #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

Mon 05 Jun 2023 01:50:51 AM EDT

Basic System Information:
---------------------------------
Uptime     : 13 days, 21 hours, 22 minutes
Processor  : Intel(R) Xeon(R) CPU E5-2670 v2 @ 2.50GHz
CPU cores  : 4 @ 2499.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 5.7 GiB
Swap       : 6.0 GiB
Disk       : 5.5 TiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-23-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : Orange Romania Communication S.A
ASN        : AS9050 ORANGE ROMANIA COMMUNICATION S.A
Host       : Legaco Networks B.V
Location   : Orastie, Hunedoara (HD)
Country    : Romania

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.36 MB/s      (342) | 20.22 MB/s     (316)
Write      | 1.40 MB/s      (350) | 20.76 MB/s     (324)
Total      | 2.76 MB/s      (692) | 40.99 MB/s     (640)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 59.30 MB/s     (115) | 109.73 MB/s    (107)
Write      | 62.45 MB/s     (121) | 117.03 MB/s    (114)
Total      | 121.75 MB/s    (236) | 226.76 MB/s    (221)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 559 Mbits/sec   | 210 Mbits/sec   | 48.4 ms        
Scaleway        | Paris, FR (10G)           | busy            | busy            | 40.3 ms        
NovoServe       | North Holland, NL (40G)   | 562 Mbits/sec   | 704 Mbits/sec   | 44.7 ms        
Uztelecom       | Tashkent, UZ (10G)        | 550 Mbits/sec   | 247 Mbits/sec   | 108 ms         
Clouvider       | NYC, NY, US (10G)         | 450 Mbits/sec   | 340 Mbits/sec   | 110 ms         
Clouvider       | Dallas, TX, US (10G)      | 368 Mbits/sec   | 321 Mbits/sec   | 142 ms         
Clouvider       | Los Angeles, CA, US (10G) | 347 Mbits/sec   | 289 Mbits/sec   | 168 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 386                           
Multi Core      | 1231                          
Full Test       | https://browser.geekbench.com/v6/cpu/1485906

YABS completed in 24 min 25 sec
```
