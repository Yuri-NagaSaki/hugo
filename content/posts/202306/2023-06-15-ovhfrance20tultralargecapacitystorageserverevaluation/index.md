---
title: "Spaceberg 法国20T 超大容量存储服务器测评"
date: "2023-06-15"
categories: 
  - "vps"
  - "eu"
---

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : Intel(R) Xeon(R) Gold 6226R CPU @ 2.90GHz
 CPU 核心数        : 5
 CPU 频率          : 2893.202 MHz
 CPU 缓存          : 22528 KB
 硬盘空间          : 20480.1 GB (147.0 GB 已用)
 内存              : 3883 MB (606 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 15 min
 负载              : 0.36, 0.08, 0.03
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 ASN组织           : AS16276 OVH SAS
 位置              : Lille / FR
 地区              : Hauts-de-France
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           1209 Scores
 5 线程测试(多核)得分:          5908 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          23386.91 MB/s
 单线程写测试:          16826.84 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         81.9 MB/s (0.05 IOPS, 1.28s))           114 MB/s (27857 IOPS, 0.92s)
 1GB-1M Block           2.0 GB/s (1863 IOPS, 0.54s)             3.6 GB/s (3468 IOPS, 0.29s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 376.35 MB/s  (94.0k) | 4.61 GB/s    (72.1k)
Write      | 377.34 MB/s  (94.3k) | 4.64 GB/s    (72.5k)
Total      | 753.69 MB/s (188.4k) | 9.25 GB/s   (144.6k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 6.02 GB/s    (11.7k) | 6.74 GB/s     (6.5k)
Write      | 6.34 GB/s    (12.3k) | 7.19 GB/s     (7.0k)
Total      | 12.37 GB/s   (24.1k) | 13.93 GB/s   (13.6k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA16S31)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: LILLIXFR
视频缓存节点地域: 法国 里尔(LIL1)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
Netflix在您的出口IP所在的国家不提供服务
[IPv6]
Netflix在您的出口IP所在的国家不提供服务
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：荷兰区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：法国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               No
 Netflix:                               No
 YouTube Premium:                       Yes (Region: FR)
 Amazon Prime Video:                    Yes (Region: NL)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   FR
 Viu.com:                               No
 YouTube CDN:                           Frankfurt 
 Netflix Preferred CDN:                 Failed
 Spotify Registration:                  No
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: FR)
 Netflix:                               No
 YouTube Premium:                       Yes (Region: FR)
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Associated with [LILLIXFR]
 Netflix Preferred CDN:                 Failed
 Spotify Registration:                  No
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【NL】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：43
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：34
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：42
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
2023/06/15 19:29:53 北京电信 219.141.136.12  电信163 [普通线路]           
2023/06/15 19:29:53 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/15 19:29:53 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/15 19:29:53 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/15 19:29:53 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/15 19:29:53 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/15 19:29:53 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/15 19:29:53 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/15 19:29:53 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/15 19:29:53 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/15 19:29:53 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/15 19:29:53 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS16276 OVH SAS
IPv6 ASN: AS16276 OVH SAS
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.80 ms  *  局域网
0.25 ms  *  局域网
0.21 ms  *  局域网
4.45 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
4.24 ms  *  局域网
7.95 ms  AS3356  英国, 伦敦, level3.com
10.33 ms  AS3356  英国, 伦敦, level3.com
254.47 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
261.18 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
256.52 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
259.45 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.15 ms  *  局域网
0.26 ms  *  局域网
0.28 ms  *  局域网
0.57 ms  *  局域网
4.30 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
4.21 ms  *  局域网
148.03 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
236.38 ms  AS3356  美国, 加利福尼亚州, 洛杉矶, level3.com
239.20 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
241.28 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
241.10 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
236.56 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.11 ms  *  局域网
0.22 ms  *  局域网
0.21 ms  *  局域网
2.14 ms  *  局域网
4.11 ms  AS16276  法国, 法兰西岛大区, 巴黎, ovh.com
3.97 ms  *  局域网
5.15 ms  AS16276  美国, 伊利诺伊州, 芝加哥, ovh.com
14.47 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
235.41 ms  AS58453  中国, 上海, chinamobile.com, 移动
231.43 ms  AS9808  中国, 上海, chinamobile.com, 移动
240.65 ms  AS9808  中国, 上海, chinamobile.com, 移动
228.39 ms  AS9808  中国, 上海, chinamobile.com, 移动
207.16 ms  AS9808  中国, 北京, chinamobile.com, 移动
201.70 ms  AS9808  中国, 北京, chinamobile.com, 移动
201.95 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    298.95 Mbps     5356.05 Mbps    4.61     0.0%
洛杉矶           296.76 Mbps     2123.94 Mbps    141.79   0.0%
日本东京         0.79 Mbps       2370.69 Mbps    234.75   23.7%
联通湖南5G       314.15 Mbps     430.37 Mbps     174.81   NULL
联通Fuzhou       323.24 Mbps     1708.30 Mbps    169.30   0.0%
电信上海         130.82 Mbps     2082.91 Mbps    232.40   NULL
电信天津5G       1.08 Mbps       987.51 Mbps     230.89   8.0%
移动Chengdu      298.51 Mbps     5127.20 Mbps    177.04   0.0%
移动Lanzhou      322.80 Mbps     4808.03 Mbps    220.13   NULL
------------------------------------------------------------------------
 总共花费      : 6 分 27 秒
 时间          : Thu Jun 15 19:35:18 CST 2023
------------------------------------------------------------------------
```

## Yabs

```

root@sayyiku:~# curl -sL yabs.sh | bash
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2023-04-23                    #
# https://github.com/masonr/yet-another-bench-script #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

Thu 15 Jun 2023 07:41:11 PM CST

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 27 minutes
Processor  : Intel(R) Xeon(R) Gold 6226R CPU @ 2.90GHz
CPU cores  : 5 @ 2893.202 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 3.8 GiB
Swap       : 0.0 KiB
Disk       : 20.0 TiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-23-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : OVH SAS
ASN        : AS16276 OVH SAS
Host       : OVH
Location   : Roubaix, Hauts-de-France (HDF)
Country    : France

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 391.84 MB/s  (97.9k) | 4.14 GB/s    (64.7k)
Write      | 392.87 MB/s  (98.2k) | 4.16 GB/s    (65.0k)
Total      | 784.71 MB/s (196.1k) | 8.30 GB/s   (129.7k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 6.56 GB/s    (12.8k) | 7.86 GB/s     (7.6k)
Write      | 6.91 GB/s    (13.5k) | 8.39 GB/s     (8.1k)
Total      | 13.48 GB/s   (26.3k) | 16.25 GB/s   (15.8k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 327 Mbits/sec   | 6.14 Gbits/sec  | 4.26 ms        
Scaleway        | Paris, FR (10G)           | 327 Mbits/sec   | 2.78 Gbits/sec  | 4.30 ms        
NovoServe       | North Holland, NL (40G)   | 327 Mbits/sec   | 4.63 Gbits/sec  | 10.8 ms        
Uztelecom       | Tashkent, UZ (10G)        | 313 Mbits/sec   | 1.66 Gbits/sec  | 96.5 ms        
Clouvider       | NYC, NY, US (10G)         | 312 Mbits/sec   | 99.2 Mbits/sec  | 82.4 ms        
Clouvider       | Dallas, TX, US (10G)      | 304 Mbits/sec   | 867 Mbits/sec   | 115 ms         
Clouvider       | Los Angeles, CA, US (10G) | 295 Mbits/sec   | 607 Mbits/sec   | 136 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 326 Mbits/sec   | 6.03 Gbits/sec  | 4.20 ms        
Scaleway        | Paris, FR (10G)           | 326 Mbits/sec   | busy            | 4.15 ms        
NovoServe       | North Holland, NL (40G)   | busy            | 4.28 Gbits/sec  | 10.7 ms        
Uztelecom       | Tashkent, UZ (10G)        | 311 Mbits/sec   | 1.31 Gbits/sec  | 96.2 ms        
Clouvider       | NYC, NY, US (10G)         | 311 Mbits/sec   | 104 Mbits/sec   | 80.8 ms        
Clouvider       | Dallas, TX, US (10G)      | 300 Mbits/sec   | 709 Mbits/sec   | 115 ms         
Clouvider       | Los Angeles, CA, US (10G) | 298 Mbits/sec   | 723 Mbits/sec   | 136 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1267                          
Multi Core      | 4788                          
Full Test       | https://browser.geekbench.com/v6/cpu/1605112

YABS completed in 11 min 16 sec
```

## SpeedTest

![](https://catcat.blog/wp-content/uploads/2023/06/image-6-1024x396.png)

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : Intel(R) Xeon(R) Gold 6226R CPU @ 2.90GHz
 CPU Cores          : 5 @ 2893.202 MHz
 CPU Cache          : 22528 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 20.0 TB (17.7 TB Used)
 Total Mem          : 3.8 GB (1.5 GB Used)
 Total Swap         : 4.0 GB (830.5 MB Used)
 System uptime      : 11 days, 19 hour 4 min
 Load average       : 0.83, 0.87, 0.77
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.1.0-0.deb11.7-amd64
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS16276 OVH SAS
 Location           : Lille / FR
 Region             : Hauts-de-France
----------------------------------------------------------------------
 I/O Speed(1st run) : 652 MB/s
 I/O Speed(2nd run) : 840 MB/s
 I/O Speed(3rd run) : 725 MB/s
 I/O Speed(average) : 739.0 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    268.22 Mbps       4302.12 Mbps        4.23 ms     
 Los Angeles, US  265.44 Mbps       1732.76 Mbps        137.93 ms   
 Dallas, US       193.14 Mbps       1657.25 Mbps        110.58 ms   
 Montreal, CA     157.53 Mbps       939.53 Mbps         86.57 ms    
 Paris, FR        246.80 Mbps       3309.95 Mbps        4.53 ms     
 Amsterdam, NL    246.23 Mbps       3530.80 Mbps        10.55 ms    
 Shanghai, CN     122.37 Mbps       1955.04 Mbps        258.48 ms   
 Nanjing, CN      264.65 Mbps       1887.54 Mbps        255.43 ms   
 Guangzhou, CN    1.13 Mbps         410.80 Mbps         263.42 ms   
 Hongkong, CN     196.94 Mbps       1075.26 Mbps        251.86 ms   
 Singapore, SG    104.57 Mbps       421.56 Mbps         230.41 ms   
 Tokyo, JP        303.24 Mbps       1655.42 Mbps        233.88 ms   
----------------------------------------------------------------------
 Finished in        : 6 min 30 sec
 Timestamp          : 2023-07-05 14:59:33 CST
----------------------------------------------------------------------
```
