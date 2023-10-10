---
title: "Little Creek  Epyc测试"
date: "2023-08-30"
categories: 
  - "vps"
  - "usa"
---

## 套餐

> Virtuozzo KVM  
> CPU Core: 4  
> RAM: 4096 MB  
> NVMe: 80GB  
> Bandwidth: 6000 GB/Month  
> $3.50/Month

## 测试

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 9 minutes
Processor  : AMD EPYC Processor (with IBPB)
CPU cores  : 4 @ 2799.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ❌ Disabled
RAM        : 3.8 GiB
Swap       : 4.0 GiB
Disk       : 75.8 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-8-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : Cogent Communications
ASN        : AS174 Cogent Communications
Host       : Little Creek Solutions
Location   : Morrisville, North Carolina (NC)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 23.79 MB/s    (5.9k) | 444.08 MB/s   (6.9k)
Write      | 23.81 MB/s    (5.9k) | 446.42 MB/s   (6.9k)
Total      | 47.61 MB/s   (11.9k) | 890.50 MB/s  (13.9k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.44 GB/s     (2.8k) | 2.03 GB/s     (1.9k)
Write      | 1.51 GB/s     (2.9k) | 2.17 GB/s     (2.1k)
Total      | 2.95 GB/s     (5.7k) | 4.21 GB/s     (4.1k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 35.2 Mbits/sec  | busy            | 86.7 ms        
Scaleway        | Paris, FR (10G)           | 207 Mbits/sec   | busy            | 90.9 ms        
NovoServe       | North Holland, NL (40G)   | 303 Mbits/sec   | 511 Mbits/sec   | 98.8 ms        
Uztelecom       | Tashkent, UZ (10G)        | 62.3 Mbits/sec  | 333 Mbits/sec   | 186 ms         
Clouvider       | NYC, NY, US (10G)         | 181 Mbits/sec   | 150 Mbits/sec   | 15.9 ms        
Clouvider       | Dallas, TX, US (10G)      | 62.0 Mbits/sec  | 234 Mbits/sec   | 38.4 ms        
Clouvider       | Los Angeles, CA, US (10G) | 53.8 Mbits/sec  | 175 Mbits/sec   | 64.3 ms        

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 797                           
Multi Core      | 1900                          
Full Test       | https://browser.geekbench.com/v6/cpu/2440475
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC Processor (with IBPB)
 CPU 核心数        : 4
 CPU 频率          : 2799.998 MHz
 CPU 缓存          : L1: 384.00 KB / L2: 2.00 MB / L3: 8.00 MB
 硬盘空间          : 2.19 GiB / 75.78 GiB
 启动盘路径        : /dev/vda1
 内存              : 117.11 MiB / 3.84 GiB
 Swap              : 0 KiB / 4.00 GiB
 系统在线时间      : 0 days, 0 hour 32 min
 负载              : 0.80, 0.42, 0.47
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-8-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS174 Cogent Communications
 IPV4 位置         : Wake Forest / North Carolina / US
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           1488 Scores
 4 线程测试(多核)得分:          5036 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          35989.84 MB/s
 单线程写测试:          14514.94 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         1.6 MB/s (400 IOPS, 64.06s)             8.6 MB/s (2088 IOPS, 12.26s)
 1GB-1M Block           171 MB/s (163 IOPS, 6.14s)              545 MB/s (519 IOPS, 1.93s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 26.94 MB/s    (6.7k) | 558.81 MB/s   (8.7k)
Write      | 26.97 MB/s    (6.7k) | 561.75 MB/s   (8.7k)
Total      | 53.92 MB/s   (13.4k) | 1.12 GB/s    (17.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.49 GB/s     (2.9k) | 1.04 GB/s     (1.0k)
Write      | 1.57 GB/s     (3.0k) | 1.10 GB/s     (1.0k)
Total      | 3.07 GB/s     (6.0k) | 2.14 GB/s     (2.0k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: IAD(IAD30S49)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: US)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Washington DC 
 Netflix Preferred CDN:                 Washington DC  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 100②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):isp①  Data Center/Web Hosting/Transit⑤  isp⑧  business⑨  
  公司类型(company_type):isp①  isp⑧  
  云服务提供商(cloud_provider):  No⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
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
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/08/30 09:38:15 北京电信 219.141.136.12  电信163 [普通线路]           
2023/08/30 09:38:15 北京联通 202.106.50.1    联通4837[普通线路]           
2023/08/30 09:38:15 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/08/30 09:38:15 上海电信 202.96.209.133  电信163 [普通线路]           
2023/08/30 09:38:15 上海联通 210.22.97.1     联通4837[普通线路]           
2023/08/30 09:38:15 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/08/30 09:38:15 广州电信 58.60.188.222   电信163 [普通线路]           
2023/08/30 09:38:15 广州联通 210.21.196.6    联通4837[普通线路]           
2023/08/30 09:38:15 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/08/30 09:38:15 成都电信 61.139.2.69     测试超时
2023/08/30 09:38:15 成都联通 119.6.6.6       联通4837[普通线路]           
2023/08/30 09:38:15 成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
5.96 ms         AS174 美国 华盛顿哥伦比亚特区 华盛顿 cogentco.com
1.95 ms         AS174 美国 华盛顿哥伦比亚特区 华盛顿 cogentco.com
2.54 ms         * [COGENT-BONE] 美国 北卡罗来纳州 德罕
2.37 ms         * [COGENT-BONE] 美国 北卡罗来纳州 德罕
5.92 ms         * [COGENT-BONE] 美国 北卡罗来纳州 Charlotte
11.04 ms        * [COGENT-BONE] 美国 佐治亚州 亚历山大
24.44 ms        AS174 [COGENT-BONE] 美国 德克萨斯州 休斯顿 cogentco.com
39.84 ms        AS174 [COGENT-BONE] 美国 得克萨斯州 埃尔帕索 cogentco.com
55.94 ms        AS174 [COGENT-BONE] 美国 亚利桑那州 凤凰城 cogentco.com
61.53 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
72.89 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 圣何塞 cogentco.com
72.44 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 圣何塞 cogentco.com
75.64 ms        AS174 美国 加利福尼亚州 圣克拉拉 cogentco.com
223.29 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 回国到达层 chinatelecom.com.cn 电信
327.72 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
330.31 ms       AS4134 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.com.cn 电信
240.72 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
1.30 ms         AS174 美国 华盛顿哥伦比亚特区 华盛顿 cogentco.com
1.63 ms         AS174 美国 华盛顿哥伦比亚特区 华盛顿 cogentco.com
2.02 ms         * [COGENT-BONE] 美国 北卡罗来纳州 德罕
2.30 ms         * [COGENT-BONE] 美国 北卡罗来纳州 德罕
6.09 ms         * [COGENT-BONE] 美国 北卡罗来纳州 Charlotte
21.90 ms        * [COGENT-BONE] 美国 佐治亚州 亚历山大
24.35 ms        AS174 [COGENT-BONE] 美国 德克萨斯州 休斯顿 cogentco.com
40.80 ms        AS174 [COGENT-BONE] 美国 得克萨斯州 埃尔帕索 cogentco.com
52.47 ms        AS174 [COGENT-BONE] 美国 亚利桑那州 凤凰城 cogentco.com
60.09 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
60.83 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
231.51 ms       AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
214.62 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
243.94 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
239.84 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
223.33 ms       AS17816 [UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
238.64 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
245.52 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
1.11 ms         AS174 美国 华盛顿哥伦比亚特区 华盛顿 cogentco.com
2.07 ms         AS174 美国 华盛顿哥伦比亚特区 华盛顿 cogentco.com
1.71 ms         AS174 [COGENT-BONE] 美国 北卡罗来纳州 德罕 cogentco.com
17.92 ms        * [COGENT-BONE] 美国 北卡罗来纳州 德罕
6.10 ms         * [COGENT-BONE] 美国 北卡罗来纳州 Charlotte
13.74 ms        * [COGENT-BONE] 美国 佐治亚州 亚历山大
24.09 ms        AS174 [COGENT-BONE] 美国 德克萨斯州 休斯顿 cogentco.com
41.07 ms        AS174 [COGENT-BONE] 美国 得克萨斯州 埃尔帕索 cogentco.com
50.87 ms        AS174 [COGENT-BONE] 美国 亚利桑那州 凤凰城 cogentco.com
59.96 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
60.28 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
70.94 ms        AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
71.00 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
72.48 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
70.42 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
217.69 ms       AS58453 [CMI-INT] 中国 广东省 广州市 cmi.chinamobile.com 移动
217.17 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
218.05 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
222.07 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
225.40 ms       AS9808 [CMNET] 中国 北京市 chinamobile.com 移动
229.91 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    530.76 Mbps     571.09 Mbps     13.19    0.0%
洛杉矶           239.72 Mbps     240.86 Mbps     59.67    0.3%
法兰克福         438.61 Mbps     442.03 Mbps     103.11   0.0%
联通Fuzhou       142.15 Mbps     412.65 Mbps     241.77   0.0%
联通郑州5G       4.66 Mbps       232.03 Mbps     357.86   NULL
电信Suzhou5G     300.56 Mbps     489.56 Mbps     202.85   NULL
电信Zhenjiang5G  1.17 Mbps       456.65 Mbps     213.82   NULL
移动Chengdu      108.23 Mbps     155.48 Mbps     286.75   0.0%
------------------------------------------------------------------------
 总共花费      : 9 分 11 秒
 时间          : Wed Aug 30 09:44:05 EDT 2023
------------------------------------------------------------------------
```

### 流媒体测试

```
============[ Multination ]============
 Dazn:                                  Yes (Region: US)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Washington DC 
 Netflix Preferred CDN:                 Washington DC  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
===========[ North America ]===========
 FOX:                                   Yes
 Hulu:                                  Failed
 NFL+:                                  Yes
 ESPN+:[Sponsored by Jam]               Yes
 Epix:                                  No
 Starz:                                 No
 Philo:                                 No
 FXNOW:                                 Yes
 TLC GO:                                Yes
 HBO Max:                               Yes
 Shudder:                               Yes
 BritBox:                               Yes
 Crackle:                               Yes
 CW TV:                                 Yes
 A&E TV:                                No
 NBA TV:                                Yes
 NBC TV:                                Yes
 Fubo TV:                               Yes
 Tubi TV:                               Yes
 Sling TV:                              Yes
 Pluto TV:                              Yes
 Acorn TV:                              Yes
 SHOWTIME:                              Yes
 encoreTVB:                             No
 Funimation:                            Yes (Region: US)
 Discovery+:                            No
 Paramount+:                            No
 Peacock TV:                            Yes
 Popcornflix:                           Yes
 Crunchyroll:                           Yes
 Directv Stream:                        No
 KBS American:                          No
 KOCOWA:                                Yes
 Maths Spot:                            Failed
 ---CA---
 CBC Gem:                               No
 Crave:                                 Yes
=======================================
```
