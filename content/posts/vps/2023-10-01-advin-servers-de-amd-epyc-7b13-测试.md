---
title: Advin Servers DE AMD EPYC 7B13 测试
author: 猫猫博客
type: post
date: 2023-09-30T16:10:52+00:00
url: /advin-servers-de-amd-epyc-7b13-测试.html
ai_summon_excerpt:
  - Advin Servers进行了一项关于AMD EPYC 7B13服务器的测试。根据测试结果显示，该服务器具备2个核心和8GB DDR4 RAM，以及60GB的NVMe存储空间。网络带宽方面，它提供每秒10Gbps的无限下载和上传速度。据YABS和Benchy的测试结果显示，AMD EPYC 7B13处理器在性能上表现出色。它在fio磁盘速度测试中达到了高速的读写速度，并且在Geekbench 6的基准测试中也表现良好。通过Speedtest.net的测速，该服务器在多个节点的上传和下载速度也表现出色。总体而言，Advin Servers的AMD EPYC 7B13服务器在性能方面表现出色。
views:
  - 82
categories:
  - vps
  - 欧洲
  - 特价促销鸡

---
**<mark style="background-color:rgba(0, 0, 0, 0)" class="has-inline-color has-vivid-red-color">注意：灵车，带宽非无限，每个套餐都有固定的使用量，无限流量只是商家的推辞。谨慎购买</mark>**

商家的回复：We have measured almost 100TB+ of outbound bandwidth usages within the past month which is well above our fair use policy outlined in our TOS on a $24/month service. You are free to no longer renew.

<blockquote class="wp-block-quote">
  <h2 class="wp-block-heading">
    套餐
  </h2>
  
  <cite><strong><em>Provider :&nbsp;Advin Servers<br />Type/Plan :&nbsp;KVM Standard XS<br />Processor :&nbsp;AMD EPYC 7B13<br />Num of Core : 2 Cores<br />Memory : 8 GB&nbsp;DDR4 RAM<br />Storage : 60 GB NVMe(PCIe 4.0)<br />Bandwidth : Unlimited @ 10 Gbps IN | 10 Gbps OUT<br />Location :&nbsp;Nuremberg, DE<br />Price :&nbsp;$4.00 /month</em></strong></cite>
</blockquote>

## 测试 {.wp-block-heading}

### Yabs {.wp-block-heading}

<pre class="wp-block-code"><code>Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 1 minutes
Processor  : AMD EPYC 7B13 64-Core Processor
CPU cores  : 2 @ 2249.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 7.8 GiB
Swap       : 0.0 KiB
Disk       : 59.0 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.0-12-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ❌ Offline

 Network Information:
---------------------------------
ISP        : Advin Services LLC
ASN        : AS206216 Advin Services LLC
Host       : MB \Lirutis\
Location   : Kerkrade, Limburg (LI)
Country    : Netherlands

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------   | ---            ----  | ----           ---- 
Read       | 181.19 MB/s  (45.2k) | 1.92 GB/s    (30.0k)
Write      | 181.66 MB/s  (45.4k) | 1.93 GB/s    (30.2k)
Total      | 362.86 MB/s  (90.7k) | 3.85 GB/s    (60.2k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------   | ---            ----  | ----           ---- 
Read       | 3.74 GB/s     (7.3k) | 3.95 GB/s     (3.8k)
Write      | 3.94 GB/s     (7.6k) | 4.21 GB/s     (4.1k)
Total      | 7.68 GB/s    (15.0k) | 8.17 GB/s     (7.9k)

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1317                          
Multi Core      | 2355                          
Full Test       | https://browser.geekbench.com/v6/cpu/2843868

YABS completed in 8 min 45 sec</code></pre>

### Benchy {.wp-block-heading}

<pre class="wp-block-code"><code>----------------------------------------------------------------------
 CPU Model          : AMD EPYC 7B13 64-Core Processor
 CPU Cores          : 2 @ 2249.998 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 59.0 GB (1.8 GB Used)
 Total Mem          : 7.8 GB (325.1 MB Used)
 System uptime      : 0 days, 0 hour 15 min
 Load average       : 0.00, 0.29, 0.26
 OS                 : Debian GNU/Linux 12
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.1.0-12-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Offline
 Organization       : AS206216 Advin Services LLC
 Location           : Kerkrade / NL
 Region             : Limburg
----------------------------------------------------------------------
 I/O Speed(1st run) : 940 MB/s
 I/O Speed(2nd run) : 1.2 GB/s
 I/O Speed(3rd run) : 1.2 GB/s
 I/O Speed(average) : 1132.5 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    7328.28 Mbps      6029.43 Mbps        11.30 ms    
 Los Angeles, US  571.37 Mbps       4905.19 Mbps        160.87 ms   
 Dallas, US       669.70 Mbps       5853.78 Mbps        131.40 ms   
 Montreal, CA     149.77 Mbps       864.39 Mbps         94.39 ms    
 Paris, FR        3135.82 Mbps      4576.64 Mbps        18.56 ms    
 Amsterdam, NL    4437.17 Mbps      5032.25 Mbps        15.11 ms    
 Shanghai, CN     369.72 Mbps       3204.88 Mbps        241.02 ms   
 Nanjing, CN      0.27 Mbps         2129.87 Mbps        325.50 ms   
 Hongkong, CN     5.13 Mbps         0.83 Mbps           238.57 ms   
 Singapore, SG    4.80 Mbps         3167.96 Mbps        246.76 ms   
 Tokyo, JP        0.74 Mbps         2996.30 Mbps        259.52 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 44 sec
 Timestamp          : 2023-09-30 14:37:50 UTC
----------------------------------------------------------------------</code></pre>

### Benchy {.wp-block-heading}

<pre class="wp-block-code"><code>Server Insight                                  Hardware Information
---------------------                           ---------------------
OS         : Debian GNU/Linux 12 (bookworm)     Model       : AMD EPYC 7B13 64-Core Processor
Location   : Netherlands                        Core        : 2 @ 2249.998 MHz
Kernel     : 6.1.0-12-amd64                     AES-NI      : ✔ Enabled
Uptime     : 0 days, 0 hrs, 21 mins, 53 secs    VM-x/AMD-V  : ✔ Enabled
Virt       : kvm                                Swap        : 0.0 KiB   

Disk & Memory Usage                             Network Information
---------------------                           ---------------------
Disk (1)   : 59.0 GiB                           ASN         : AS206216  
Disk Usage : 1.8 GiB (3% Used)                  ISP         : Advin Services LLC
Mem        : 7.8 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.3 GiB (4% Used)                  IPv6        : ❌ Disabled

Disk Performance Check (ext4 on /dev/sda1) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 183.31 MB/s | 183.80 MB/s | 367.12 MB/s | 46.9k  | 47.0k  | 94.0k  |
| 64k  | 1.88 GB/s   | 1.89 GB/s   | 3.78 GB/s   | 30.9k  | 31.1k  | 62.0k  |
| 512k | 3.46 GB/s   | 3.65 GB/s   | 7.11 GB/s   | 7.1k   | 7.5k   | 14.6k  |
| 1m   | 3.78 GB/s   | 4.03 GB/s   | 7.82 GB/s   | 3.9k   | 4.1k   | 8.0k   |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |    1.4 Gb/s  |    1.5 Gb/s  |  119.6 ms |
|       | Uztelecom   | Tashkent, UZ    |        busy  |        busy  |   93.4 ms |
|       | Novogara    | Amsterdam, NL   |    2.6 Gb/s  |    2.2 Gb/s  |   15.6 ms |
|       | FiberBy     | Copenhagen, DK  |    1.7 Gb/s  |    7.2 Gb/s  |   21.6 ms |
+---------------------------------------------------------------------------------+

+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 1123                     |
| Multi Core         | 2237                     |
+-----------------------------------------------+
| https://browser.geekbench.com/v6/cpu/2844166  |
+-----------------------------------------------+
| Benchy time spent  | 11 Minutes 15 Seconds    |
+-----------------------------------------------+
| Benchy result      | http://sprunge.us/sIQGpf |
+-----------------------------------------------+</code></pre>

### 融合怪脚本测试 {.wp-block-heading}

<pre class="wp-block-code"><code>---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7B13 64-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 2249.998 MHz
 CPU 缓存          : L1: 128.00 KB / L2: 1.00 MB / L3: 32.00 MB
 硬盘空间          : 1.76 GiB / 59.04 GiB
 启动盘路径        : /dev/sda1
 内存              : 148.42 MiB / 7.76 GiB
 Swap              : &#91; no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 34 min
 负载              : 0.44, 0.68, 0.49
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-12-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS206216 Advin Services LLC
 IPV4 位置         : Kerkrade / Limburg / NL
---------------------CPU测试--感谢lemonbench开源------------------------
 -&gt; CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           3501 Scores
 2 线程测试(多核)得分:          6983 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -&gt; 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          39600.76 MB/s
 单线程写测试:          22488.13 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -&gt; 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         40.3 MB/s (9839 IOPS, 2.60s)            75.9 MB/s (18518 IOPS, 1.38s)
 1GB-1M Block           3.4 GB/s (3225 IOPS, 0.31s)             6.7 GB/s (6389 IOPS, 0.16s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------   | ---            ----  | ----           ---- 
Read       | 191.79 MB/s  (47.9k) | 1.75 GB/s    (27.4k)
Write      | 192.30 MB/s  (48.0k) | 1.76 GB/s    (27.5k)
Total      | 384.09 MB/s  (96.0k) | 3.52 GB/s    (55.0k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------   | ---            ----  | ----           ---- 
Read       | 3.86 GB/s     (7.5k) | 4.10 GB/s     (4.0k)
Write      | 4.07 GB/s     (7.9k) | 4.37 GB/s     (4.2k)
Total      | 7.94 GB/s    (15.5k) | 8.47 GB/s     (8.2k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
&#91;IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA16S31)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
&#91;IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：美国
&#91;IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
&#91;IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============&#91; Multination ]============
 Dazn:                                  Yes (Region: NL)
 HotStar:                               Yes (Region: US)
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Yes (Region: NL)
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   DE
 Viu.com:                               No
 YouTube CDN:                           Frankfurt 
 Netflix Preferred CDN:                 Washington DC  
 Spotify Registration:                  No
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【NL】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 100②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  business⑨  
  公司类型(company_type):hosting①  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
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
黑名单记录统计(有多少个黑名单网站有记录): 无害63 恶意1 可疑0 未检测25 ③
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: NL 城市: Kerkrade 服务商: AS206216 Advin Services LLC
北京电信 219.141.136.12  电信163 &#91;普通线路]           
北京联通 202.106.50.1    联通4837&#91;普通线路]           
北京移动 221.179.155.161 测试超时
上海电信 202.96.209.133  测试超时
上海联通 210.22.97.1     联通4837&#91;普通线路]           
上海移动 211.136.112.200 移动CMI &#91;普通线路]           
广州电信 58.60.188.222   电信163 &#91;普通线路]           
广州联通 210.21.196.6    联通4837&#91;普通线路]           
广州移动 120.196.165.24  移动CMI &#91;普通线路]           
成都电信 61.139.2.69     电信163 &#91;普通线路]           
成都联通 119.6.6.6       联通4837&#91;普通线路]           
成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.46 ms         AS206216 德国 巴伐利亚州 纽伦堡 advinservers.com
0.88 ms         AS174 &#91;COGENT-BONE] 德国 巴伐利亚州 纽伦堡 cogentco.com
3.07 ms         AS174 &#91;COGENT-BONE] 德国 巴伐利亚州 慕尼黑 cogentco.com
8.37 ms         AS174 &#91;COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
8.59 ms         AS174 &#91;COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
61.98 ms        AS174 &#91;COGENT-149] 德国 黑森州 美因河畔法兰克福 Cogent-CT-Peer cogentco.com
307.34 ms       AS4134 &#91;CHINANET-BB] 中国 广州市 广州市 chinatelecom.com.cn 电信
311.42 ms       AS4134 &#91;CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
514.65 ms       AS4134 &#91;CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
* ms    AS4134 &#91;CHINANET-GD] 中国 广东省 深圳市 chinatelecom.com.cn 电信
424.09 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
2.12 ms         AS206216 德国 巴伐利亚州 纽伦堡 advinservers.com
0.89 ms         AS174 &#91;COGENT-BONE] 德国 巴伐利亚州 纽伦堡 cogentco.com
2.95 ms         AS174 &#91;COGENT-BONE] 德国 巴伐利亚州 慕尼黑 cogentco.com
8.32 ms         AS174 &#91;COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
17.79 ms        AS174 &#91;COGENT-BONE] 法国 法兰西岛大区 巴黎 cogentco.com
94.70 ms        AS174 &#91;COGENT-BONE] 美国 华盛顿哥伦比亚特区 华盛顿 cogentco.com
111.13 ms       AS174 &#91;COGENT-BONE] 美国 佐治亚州 亚历山大 cogentco.com
130.30 ms       AS174 &#91;COGENT-BONE] 美国 德克萨斯州 休斯顿 cogentco.com
140.59 ms       AS174 &#91;COGENT-BONE] 美国 得克萨斯州 埃尔帕索 cogentco.com
148.85 ms       AS174 &#91;COGENT-BONE] 美国 亚利桑那州 凤凰城 cogentco.com
161.58 ms       AS174 &#91;COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
160.98 ms       AS174 &#91;COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
320.43 ms       AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
343.59 ms       AS4837 &#91;CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
327.57 ms       AS4837 &#91;CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
521.80 ms       AS4837 &#91;CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
326.50 ms       AS17816 &#91;UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
328.72 ms       AS17623 &#91;APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
349.84 ms       AS17623 &#91;APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.42 ms         AS206216 德国 巴伐利亚州 纽伦堡 advinservers.com
0.89 ms         AS174 &#91;COGENT-BONE] 德国 巴伐利亚州 纽伦堡 cogentco.com
2.89 ms         AS174 &#91;COGENT-BONE] 德国 巴伐利亚州 慕尼黑 cogentco.com
8.24 ms         AS174 &#91;COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
8.83 ms         AS174 &#91;COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
47.76 ms        AS174 &#91;COGENT-149] 德国 黑森州 美因河畔法兰克福 cogentco.com
23.62 ms        AS58453 &#91;CMI-INT] 德国 黑森州 美茵河畔法兰克福 cmi.chinamobile.com 移动
221.07 ms       AS58453 &#91;CMI-INT] 德国 黑森州 美因河畔法兰克福 cmi.chinamobile.com 移动
222.58 ms       AS9808 &#91;CMNET] 中国 广东省 广州市 chinamobile.com 移动
225.25 ms       AS9808 &#91;CMNET] 中国 广东省 广州市 chinamobile.com 移动
226.23 ms       AS9808 &#91;CMNET] 中国 广东省 广州市 chinamobile.com 移动
232.31 ms       AS9808 &#91;CMNET] 中国 海南省 海口市 chinamobile.com 移动
227.58 ms       AS56040 &#91;APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    6717.63 Mbps    5905.11 Mbps    11.25    0.0%
法兰克福         8175.85 Mbps    7873.47 Mbps    8.35     0.0%
洛杉矶           557.44 Mbps     4491.40 Mbps    159.57   0.0%
联通湖南5G       212.93 Mbps     2.75 Mbps       342.62   NULL
联通沈阳         79.36 Mbps      2.74 Mbps       255.33   0.0%
电信Suzhou5G     0.94 Mbps       4374.49 Mbps    330.03   NULL
移动Chengdu      784.77 Mbps     4778.96 Mbps    233.46   0.0%
------------------------------------------------------------------------
 总共花费      : 5 分 27 秒
 时间          : Sat Sep 30 14:56:57 UTC 2023
------------------------------------------------------------------------</code></pre>

### byte-unixbench 性能测试 {.wp-block-heading}

<pre class="wp-block-code"><code>------------------------------------------------------------------------
Benchmark Run: Sat Sep 30 2023 15:01:04 - 15:29:03
2 CPUs in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       40436139.5 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                     7380.5 MWIPS (9.9 s, 7 samples)
Execl Throughput                               2762.0 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks        929165.5 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          247917.2 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       2489939.2 KBps  (30.0 s, 2 samples)
Pipe Throughput                             1373865.3 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                  38226.3 lps   (10.0 s, 7 samples)
Process Creation                               6235.6 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                   9095.6 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   1757.5 lpm   (60.0 s, 2 samples)
System Call Overhead                        1353747.8 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   40436139.5   3465.0
Double-Precision Whetstone                       55.0       7380.5   1341.9
Execl Throughput                                 43.0       2762.0    642.3
File Copy 1024 bufsize 2000 maxblocks          3960.0     929165.5   2346.4
File Copy 256 bufsize 500 maxblocks            1655.0     247917.2   1498.0
File Copy 4096 bufsize 8000 maxblocks          5800.0    2489939.2   4293.0
Pipe Throughput                               12440.0    1373865.3   1104.4
Pipe-based Context Switching                   4000.0      38226.3     95.6
Process Creation                                126.0       6235.6    494.9
Shell Scripts (1 concurrent)                     42.4       9095.6   2145.2
Shell Scripts (8 concurrent)                      6.0       1757.5   2929.2
System Call Overhead                          15000.0    1353747.8    902.5
                                                                   ========
System Benchmarks Index Score                                        1241.0

------------------------------------------------------------------------
Benchmark Run: Sat Sep 30 2023 15:29:03 - 15:57:03
2 CPUs in system; running 2 parallel copies of tests

Dhrystone 2 using register variables       81128417.5 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    14829.8 MWIPS (9.9 s, 7 samples)
Execl Throughput                               5223.1 lps   (29.8 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1676977.3 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          416968.9 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       3610998.4 KBps  (30.0 s, 2 samples)
Pipe Throughput                             2738083.7 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 362703.1 lps   (10.0 s, 7 samples)
Process Creation                              16674.3 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  13709.8 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   1834.8 lpm   (60.0 s, 2 samples)
System Call Overhead                        2529640.3 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   81128417.5   6951.9
Double-Precision Whetstone                       55.0      14829.8   2696.3
Execl Throughput                                 43.0       5223.1   1214.7
File Copy 1024 bufsize 2000 maxblocks          3960.0    1676977.3   4234.8
File Copy 256 bufsize 500 maxblocks            1655.0     416968.9   2519.4
File Copy 4096 bufsize 8000 maxblocks          5800.0    3610998.4   6225.9
Pipe Throughput                               12440.0    2738083.7   2201.0
Pipe-based Context Switching                   4000.0     362703.1    906.8
Process Creation                                126.0      16674.3   1323.4
Shell Scripts (1 concurrent)                     42.4      13709.8   3233.5
Shell Scripts (8 concurrent)                      6.0       1834.8   3058.0
System Call Overhead                          15000.0    2529640.3   1686.4
                                                                   ========
System Benchmarks Index Score                                        2523.3



======= Script description and score comparison completed! ======= </code></pre>

### <a href="https://www.passmark.com/products/pt_linux/download.php" target="_blank" rel="noreferrer noopener" rel="nofollow" >PerformanceTest Linux</a>&nbsp;测试 {.wp-block-heading}

<pre class="wp-block-code"><code>AMD EPYC 7B13 64-Core Processor (x86_64)
2 cores @ 0 MHz  |  7.8 GiB RAM
Number of Processes: 2  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          4101
  Integer Math                     10202 Million Operations/s
  Floating Point Math              7788 Million Operations/s
  Prime Numbers                    27.0 Million Primes/s
  Sorting                          5593 Thousand Strings/s
  Encryption                       2190 MB/s
  Compression                      39043 KB/s
  CPU Single Threaded              2096 Million Operations/s
  Physics                          473 Frames/s
  Extended Instructions (SSE)      2996 Million Matrices/s

Memory Mark:                       1700
  Database Operations              1383 Thousand Operations/s
  Memory Read Cached               18383 MB/s
  Memory Read Uncached             12318 MB/s
  Memory Write                     12951 MB/s
  Available RAM                    7077 Megabytes
  Memory Latency                   83 Nanoseconds
  Memory Threaded                  23011 MB/s
--------------------------------------------------------------------------</code></pre>

### SpeedTest {.wp-block-heading}

<pre class="wp-block-code"><code>root@s9286:~# speedtest

   Speedtest by Ookla

      Server: Händle & Korte GmbH - Dusseldorf (id: 28624)
         ISP: Advin Services LLC
Idle Latency:    11.30 ms   (jitter: 0.02ms, low: 11.22ms, high: 11.31ms)
    Download:  5549.05 Mbps (data used: 4.5 GB)                                                   
                 12.92 ms   (jitter: 1.28ms, low: 11.24ms, high: 20.73ms)
      Upload:  6384.01 Mbps (data used: 5.0 GB)                                                   
                 11.53 ms   (jitter: 0.56ms, low: 11.17ms, high: 14.09ms)
 Packet Loss:     0.0%
  Result URL: https://www.speedtest.net/result/c/50057e64-e11a-4d47-b7f5-600d285608d9</code></pre><figure class="wp-block-image size-large">

<img decoding="async" loading="lazy" width="1024" height="384" src="https://cdn.lirica.cn/wordpress/2023/10/image-1024x384.png" alt="" class="wp-image-2262" srcset="https://catcat.blog/wp-content/uploads/2023/10/image-1024x384.png 1024w, https://catcat.blog/wp-content/uploads/2023/10/image-300x112.png 300w, https://catcat.blog/wp-content/uploads/2023/10/image-768x288.png 768w, https://catcat.blog/wp-content/uploads/2023/10/image.png 1465w" sizes="(max-width: 1024px) 100vw, 1024px" /> </figure>