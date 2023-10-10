---
title: "Casbay马来服务器测评"
date: "2023-08-30"
categories: 
  - "vps"
  - "马来西亚"
---

## 商家介绍

Casbay: 马来西亚VPS/云服务器, 100Mbps带宽，不限流量，月付 $11.59

Casbay(AS132841)自2010年成立起，现如今已有十多年历史的服务器商家，有自己的网络和服数据中心。主打马来西亚和新加坡数据中心的业务，其中包括VPS业务，独立服务器，云服务器等等。其中马来西亚的VPS/云服务器采用KVM虚拟，默认100M带宽，不限制流量，自带一个IPv4。

付款支持：加密货币，PayPal，信用卡，微信支付，支付宝都可付款

![](https://cdn.lirica.cn/wordpress/2023/08/image-9-1024x600.png)

## 测试

## Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 1 hours, 4 minutes
Processor  : Intel Xeon E3-12xx v2 (Ivy Bridge, IBRS)
CPU cores  : 8 @ 2599.990 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 11.7 GiB
Swap       : 6.0 GiB
Disk       : 43.8 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-8-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : Gigabit Hosting Sdn Bhd
ASN        : AS55720 Gigabit Hosting Sdn Bhd
Host       : Casbay Sdn. Bhd
Location   : George Town, Penang (07)
Country    : Malaysia

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 10.29 MB/s    (2.5k) | 142.07 MB/s   (2.2k)
Write      | 10.31 MB/s    (2.5k) | 142.82 MB/s   (2.2k)
Total      | 20.60 MB/s    (5.1k) | 284.90 MB/s   (4.4k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 195.43 MB/s    (381) | 215.91 MB/s    (210)
Write      | 205.81 MB/s    (401) | 230.29 MB/s    (224)
Total      | 401.25 MB/s    (782) | 446.20 MB/s    (434)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 16.6 Mbits/sec  | 6.59 Mbits/sec  | 223 ms         
Scaleway        | Paris, FR (10G)           | 75.7 Mbits/sec  | busy            | 155 ms         
NovoServe       | North Holland, NL (40G)   | 71.5 Mbits/sec  | busy            | 150 ms         
Uztelecom       | Tashkent, UZ (10G)        | busy            | 8.30 Mbits/sec  | 180 ms         
Clouvider       | NYC, NY, US (10G)         | 15.1 Mbits/sec  | 5.71 Mbits/sec  | 257 ms         
Clouvider       | Dallas, TX, US (10G)      | 8.17 Mbits/sec  | 3.79 Mbits/sec  | 253 ms         
Clouvider       | Los Angeles, CA, US (10G) | busy            | 2.08 Mbits/sec  | 263 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 310                           
Multi Core      | 1438                          
Full Test       | https://browser.geekbench.com/v6/cpu/2434602

YABS completed in 34 min 44 sec
```

### 融合怪脚本

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : Intel Xeon E3-12xx v2 (Ivy Bridge, IBRS)
 CPU 核心数        : 8
 CPU 频率          : 2599.990 MHz
 CPU 缓存          : L1: 512.00 KB / L2: 32.00 MB / L3: 128.00 MB
 硬盘空间          : 2.05 GiB / 43.78 GiB
 启动盘路径        : /dev/vda1
 内存              : 208.75 MiB / 11.70 GiB
 Swap              : 0 KiB / 6.00 GiB
 系统在线时间      : 0 days, 2 hour 2 min
 负载              : 0.10, 0.05, 0.38
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-8-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS55720 Gigabit Hosting Sdn Bhd
 IPV4 位置         : Shah Alam / Selangor / MY
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           575 Scores
 8 线程测试(多核)得分:          4155 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          11875.64 MB/s
 单线程写测试:          8119.54 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         16.5 MB/s (4019 IOPS, 6.37s)            14.2 MB/s (3455 IOPS, 7.41s)
 1GB-1M Block           463 MB/s (442 IOPS, 2.26s)              1.0 GB/s (959 IOPS, 1.04s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 10.13 MB/s    (2.5k) | 133.93 MB/s   (2.0k)
Write      | 10.17 MB/s    (2.5k) | 134.63 MB/s   (2.1k)
Total      | 20.30 MB/s    (5.0k) | 268.57 MB/s   (4.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 179.29 MB/s    (350) | 225.80 MB/s    (220)
Write      | 188.82 MB/s    (368) | 240.84 MB/s    (235)
Total      | 368.11 MB/s    (718) | 466.65 MB/s    (455)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 马来西亚吉隆坡(KUL09S19)
Youtube识别地域: 马来西亚(MY)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：马来西亚
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口所在地区即将开通DisneyPlus，尽请期待哦！
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: MY)
 HotStar:                               Yes (Region: MY)
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: MY)
 Amazon Prime Video:                    Yes (Region: MY)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   MY
 Viu.com:                               Yes (Region: MY)
 YouTube CDN:                           Kuala Lumpur 
 Netflix Preferred CDN:                 Singapore  
 Spotify Registration:                  Yes (Region: MY)
 Steam Currency:                        MYR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【MY】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  business⑨  
  公司类型(company_type):hosting①  business⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  No②   Yes⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ②   Yes⑥ ⑦ ⑧ ⑨ ⑩ 
  VPN(vpn):  Yes① ②   No⑦ ⑧ 
  TOR(tor):  No① ② ⑦ ⑧ ⑨ 
  TOR出口(tor_exit):  No⑧ 
  搜索引擎机器人(search_engine_robot):  No② 
  匿名代理(anonymous):  Yes⑦ ⑧   No⑨ 
  攻击方(attacker):  No⑧ ⑨ 
  滥用者(abuser):  No⑧ ⑨ 
  威胁(threat):  No⑧ ⑨ 
  iCloud中继(icloud_relay):  No① ⑧ ⑨ 
  未分配IP(bogon):  No⑧ ⑨ 
黑名单记录统计(有多少个黑名单网站有记录): 无害64 恶意2 可疑0 未检测22 ③
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
  qq邮箱: Yes
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/08/29 22:16:43 北京电信 219.141.136.12  测试超时
2023/08/29 22:16:43 北京联通 202.106.50.1    联通4837[普通线路]           
2023/08/29 22:16:43 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/08/29 22:16:43 上海电信 202.96.209.133  电信163 [普通线路]           
2023/08/29 22:16:43 上海联通 210.22.97.1     联通4837[普通线路]           
2023/08/29 22:16:43 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/08/29 22:16:43 广州电信 58.60.188.222   电信163 [普通线路]           
2023/08/29 22:16:43 广州联通 210.21.196.6    联通4837[普通线路]           
2023/08/29 22:16:43 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/08/29 22:16:43 成都电信 61.139.2.69     电信163 [普通线路]           
2023/08/29 22:16:43 成都联通 119.6.6.6       联通4837[普通线路]           
2023/08/29 22:16:43 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
1.02 ms         AS55720 [YTE-MY] 马来西亚 吉隆坡联邦直辖区 吉隆坡 thegigabit.com
84.82 ms        AS4637 新加坡 telstraglobal.com
12.97 ms        AS4637 [TELSTRAGLOBAL-AP] 新加坡 telstraglobal.com
43.82 ms        AS4637 [TELSTRAGLOBAL-AP] 新加坡 telstraglobal.com
143.06 ms       AS4637 [TELSTRAGLOBAL-AP] 中国 香港 telstraglobal.com
42.80 ms        AS4637 [TELSTRAGLOBAL-AP] 中国 香港 telstraglobal.com
192.54 ms       AS4134 [CHINANET-FJ] 中国 香港 chinatelecom.com.cn 电信
192.44 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
* ms    AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
402.56 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
205.70 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.72 ms         AS55720 [YTE-MY] 马来西亚 吉隆坡联邦直辖区 吉隆坡 thegigabit.com
17.17 ms        AS4637 新加坡 telstraglobal.com
119.40 ms       AS4637 [TELSTRAGLOBAL-AP] 新加坡 telstraglobal.com
* ms    AS4637 [TELSTRAGLOBAL-AP] 中国 香港 telstraglobal.com
51.43 ms        AS4637 [TELSTRAGLOBAL-AP] 中国 香港 telstraglobal.com
103.98 ms       AS4837 [CU169-BACKBONE] 中国 香港 chinaunicom.cn 联通
108.46 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
110.11 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
115.63 ms       AS17816 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
113.37 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
112.06 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.77 ms         AS55720 [YTE-MY] 马来西亚 吉隆坡联邦直辖区 吉隆坡 thegigabit.com
2.89 ms         AS2914 [NTTGIN-JP] 马来西亚 吉隆坡联邦直辖区 吉隆坡 ntt.net
2.96 ms         AS2914 [NTT-BACKBONE] 马来西亚 吉隆坡联邦直辖区 吉隆坡 ntt.net
* ms    AS2914 [NTT-BACKBONE] 新加坡 ntt.net
7.91 ms         AS2914 [NTT-BACKBONE] 新加坡 ntt.net
9.66 ms         AS2914 [NTT-GIN] 新加坡 ntt.net
* ms    AS58453 [CMI-INT] 中国 香港 cmi.chinamobile.com 移动
49.38 ms        AS58453 [CMI-INT] 中国 广东省 广州市 cmi.chinamobile.com 移动
48.60 ms        AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
50.39 ms        AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
149.65 ms       AS9808 [CMNET] 中国 上海市 chinamobile.com 移动
50.50 ms        AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
53.71 ms        AS9808 [CMNET] 中国 北京市 chinamobile.com 移动
51.58 ms        AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    79.85 Mbps      39.67 Mbps      1.56     0.0%
新加坡           80.46 Mbps      20.59 Mbps      25.96    0.0%
中国香港         79.13 Mbps      13.95 Mbps      44.02    0.0%
联通WuXi         77.12 Mbps      14.17 Mbps      92.13    0.0%
联通Fuzhou       79.74 Mbps      10.93 Mbps      95.27    0.0%
电信Suzhou5G     82.33 Mbps      3.92 Mbps       195.30   NULL
移动Chengdu      80.77 Mbps      36.98 Mbps      110.56   0.0%
移动硬核通信     82.89 Mbps      8.84 Mbps       61.43    NULL
------------------------------------------------------------------------
 总共花费      : 6 分 45 秒
 时间          : Tue Aug 29 22:20:48 EDT 2023
------------------------------------------------------------------------
```

### bench

```
----------------------------------------------------------------------
 CPU Model          : Intel Xeon E3-12xx v2 (Ivy Bridge, IBRS)
 CPU Cores          : 8 @ 2599.990 MHz
 CPU Cache          : 16384 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 43.8 GB (2.1 GB Used)
 Total Mem          : 11.7 GB (117.7 MB Used)
 Total Swap         : 6.0 GB (0 Used)
 System uptime      : 0 days, 2 hour 13 min
 Load average       : 0.00, 0.05, 0.24
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-8-amd64
 TCP CC             : cubic
 Virtualization     : KVM
 IPv4/IPv6          : Online / Offline
 Organization       : AS55720 Gigabit Hosting Sdn Bhd
 Location           : Shah Alam / MY
 Region             : Selangor
----------------------------------------------------------------------
 I/O Speed(1st run) : 193 MB/s
 I/O Speed(2nd run) : 419 MB/s
 I/O Speed(3rd run) : 497 MB/s
 I/O Speed(average) : 369.7 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    81.24 Mbps        37.20 Mbps          1.46 ms     
 Los Angeles, US  75.16 Mbps        3.39 Mbps           315.10 ms   
 Dallas, US       78.33 Mbps        5.39 Mbps           286.43 ms   
 Montreal, CA     80.26 Mbps        6.83 Mbps           253.12 ms   
 Paris, FR        77.65 Mbps        46.38 Mbps          166.31 ms   
 Amsterdam, NL    83.44 Mbps        6.37 Mbps           159.19 ms   
 Nanjing, CN      80.30 Mbps        8.38 Mbps           216.65 ms   
 Hongkong, CN     82.30 Mbps        42.39 Mbps          43.61 ms    
 Singapore, SG    83.90 Mbps        26.33 Mbps          8.30 ms     
 Tokyo, JP        83.16 Mbps        8.30 Mbps           74.04 ms    
----------------------------------------------------------------------
 Finished in        : 4 min 44 sec
 Timestamp          : 2023-08-29 22:30:16 EDT
----------------------------------------------------------------------
```

### 多线路回程测评

```
----------------------------------------------------------------------
北京电信
traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  103.212.69.194  0.69 ms  http: 403  http: 403
 2  *
 3  unknown.telstraglobal.net (202.127.73.209)  10.34 ms  http: 403  http: 403
 4  *
 5  *
 6  202.84.153.38  43.15 ms  http: 403  http: 403
 7  203.215.232.185  189.74 ms  http: 403  http: 403
 8  *
 9  202.97.12.145  238.23 ms  http: 403  http: 403
10  202.97.94.185  236.12 ms  http: 403  http: 403
11  *
12  *
13  2.254.120.106.static.bjtelecom.net (106.120.254.2)  239.70 ms  http: 403  http: 403
14  bj141-147-210.bjtelecom.net (219.141.147.210)  214.96 ms  http: 403  http: 403

----------------------------------------------------------------------
上海电信
traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  103.212.69.194  0.85 ms  http: 403  http: 403
 2  *
 3  unknown.telstraglobal.net (202.127.73.209)  9.44 ms  http: 403  http: 403
 4  *
 5  202.84.249.161  43.49 ms  http: 403  http: 403
 6  202.84.157.37  48.17 ms  http: 403  http: 403
 7  218.30.56.149  186.66 ms  http: 403  http: 403
 8  202.97.6.49  189.48 ms  http: 403  http: 403
 9  *
10  202.97.83.2  198.10 ms  http: 403  http: 403
11  *
12  101.95.89.162  195.05 ms  http: 403  http: 403
13  180.169.255.114  201.84 ms  http: 403  http: 403
14  ns-pd.online.sh.cn (202.96.209.133)  188.46 ms  http: 403  http: 403

----------------------------------------------------------------------
深圳电信
traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  103.212.69.194  0.86 ms  http: 403  http: 403
 2  *
 3  unknown.telstraglobal.net (202.127.73.209)  15.00 ms  http: 403  http: 403
 4  i-91.sgcn-core01.telstraglobal.net (202.84.224.198)  12.41 ms  http: 403  http: 403
 5  i-91.sgcn-core01.telstraglobal.net (202.84.224.198)  43.80 ms  http: 403  http: 403
 6  i-15251.hkth-core03.telstraglobal.net (202.84.141.110)  42.29 ms  http: 403  http: 403
 7  202.84.153.38  42.55 ms  http: 403  http: 403
 8  203.215.232.185  190.46 ms  http: 403  http: 403
 9  202.97.95.173  191.91 ms  http: 403  http: 403
10  *
11  *
12  14.147.127.2  200.15 ms  http: 403  http: 403
13  *
14  58.60.188.222  199.25 ms  http: 403  http: 403

----------------------------------------------------------------------
北京联通
traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  103.212.69.194  0.95 ms  http: 403  http: 403
 2  *
 3  unknown.telstraglobal.net (202.127.73.209)  164.67 ms  http: 403  http: 403
 4  i-91.sgcn-core01.telstraglobal.net (202.84.224.198)  11.97 ms  http: 403  http: 403
 5  i-91.sgcn-core01.telstraglobal.net (202.84.224.198)  43.65 ms  http: 403  http: 403
 6  i-15251.hkth-core03.telstraglobal.net (202.84.141.110)  43.52 ms  http: 403  http: 403
 7  202.84.153.54  43.91 ms  http: 403  http: 403
 8  219.158.40.233  98.11 ms  http: 403  http: 403
 9  219.158.20.93  96.43 ms  http: 403  http: 403
10  219.158.4.49  97.34 ms  http: 403  http: 403
11  219.158.3.93  95.08 ms  http: 403  http: 403
12  219.158.19.225  106.41 ms  http: 403  http: 403
13  *
14  202.106.50.1  109.80 ms  http: 403  http: 403

----------------------------------------------------------------------
上海联通
traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  103.212.69.194  0.79 ms  http: 403  http: 403
 2  *
 3  unknown.telstraglobal.net (202.127.73.209)  10.65 ms  http: 403  http: 403
 4  i-93.sgpl-core03.telstraglobal.net (202.84.224.189)  10.51 ms  http: 403  http: 403
 5  *
 6  202.84.153.54  51.17 ms  http: 403  http: 403
 7  219.158.40.233  101.67 ms  http: 403  http: 403
 8  *
 9  219.158.4.105  106.29 ms  http: 403  http: 403
10  219.158.3.93  102.81 ms  http: 403  http: 403
11  *
12  *
13  *
14  210.22.97.1  107.21 ms  http: 403  http: 403

----------------------------------------------------------------------
深圳联通
traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  103.212.69.194  0.74 ms  http: 403  http: 403
 2  *
 3  unknown.telstraglobal.net (202.127.73.209)  27.70 ms  http: 403  http: 403
 4  *
 5  202.84.249.249  52.88 ms  http: 403  http: 403
 6  202.84.153.54  51.18 ms  http: 403  http: 403
 7  219.158.40.233  103.46 ms  http: 403  http: 403
 8  219.158.10.29  113.09 ms  http: 403  http: 403
 9  219.158.103.29  113.78 ms  http: 403  http: 403
10  219.158.8.121  104.60 ms  http: 403  http: 403
11  120.82.0.162  110.29 ms  http: 403  http: 403
12  120.80.144.34  116.93 ms  http: 403  http: 403
13  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  111.13 ms  http: 403  http: 403

----------------------------------------------------------------------
北京移动
traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  103.212.69.194  0.72 ms  http: 403  http: 403
 2  *
 3  xe-0-1-0-3-5-100.r00.kslrml02.my.bb.gin.ntt.net (203.78.193.165)  2.95 ms  http: 403  http: 403
 4  ae-1.r22.kslrml02.my.bb.gin.ntt.net (129.250.3.196)  10.61 ms  http: 403  http: 403
 5  ae-5.r27.tkokhk01.hk.bb.gin.ntt.net (129.250.2.195)  33.44 ms  http: 403  http: 403
 6  ae-1.a02.tkokhk01.hk.bb.gin.ntt.net (129.250.5.39)  37.44 ms  http: 403  http: 403
 7  *
 8  223.120.2.53  41.22 ms  http: 403  http: 403
 9  *
10  223.120.22.142  75.29 ms  http: 403  http: 403
11  221.183.55.110  75.57 ms  http: 403  http: 403
12  221.183.25.201  83.42 ms  http: 403  http: 403
13  *
14  *
15  *
16  cachedns03.bj.chinamobile.com (221.179.155.161)  89.46 ms  http: 403  http: 403

----------------------------------------------------------------------
上海移动
traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  103.212.69.194  0.85 ms  http: 403  http: 403
 2  *
 3  xe-0-1-0-3-5-100.r00.kslrml02.my.bb.gin.ntt.net (203.78.193.165)  2.59 ms  http: 403  http: 403
 4  *
 5  *
 6  ae-1.r01.sngpsi07.sg.bb.gin.ntt.net (129.250.4.94)  7.62 ms  http: 403  http: 403
 7  ce-0-11-0-1.r01.sngpsi07.sg.ce.gin.ntt.net (116.51.17.238)  9.71 ms  http: 403  http: 403
 8  223.120.2.45  41.61 ms  http: 403  http: 403
 9  223.120.3.182  65.90 ms  http: 403  http: 403
10  221.183.89.170  68.05 ms  http: 403  http: 403
11  221.183.89.33  67.33 ms  http: 403  http: 403
12  *
13  *
14  221.181.125.138  71.84 ms  http: 403  http: 403
15  211.136.112.252  69.87 ms  http: 403  http: 403
16  211.136.112.200  69.22 ms  http: 403  http: 403

----------------------------------------------------------------------
深圳移动
traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  103.212.69.194  0.74 ms  http: 403  http: 403
 2  *
 3  xe-0-1-0-3-5-100.r00.kslrml02.my.bb.gin.ntt.net (203.78.193.165)  2.64 ms  http: 403  http: 403
 4  ae-5.r23.kslrml02.my.bb.gin.ntt.net (129.250.3.231)  4.43 ms  http: 403  http: 403
 5  ae-8.r23.sngpsi07.sg.bb.gin.ntt.net (129.250.2.168)  7.74 ms  http: 403  http: 403
 6  ae-1.r01.sngpsi07.sg.bb.gin.ntt.net (129.250.4.94)  7.81 ms  http: 403  http: 403
 7  ce-0-11-0-1.r01.sngpsi07.sg.ce.gin.ntt.net (116.51.17.238)  259.58 ms  http: 403  http: 403
 8  223.120.2.109  45.37 ms  http: 403  http: 403
 9  223.120.2.14  57.24 ms  http: 403  http: 403
10  221.183.55.58  48.48 ms  http: 403  http: 403
11  221.183.92.21  49.81 ms  http: 403  http: 403
12  *
13  221.183.71.78  50.18 ms  http: 403  http: 403
14  221.183.110.166  52.02 ms  http: 403  http: 403
15  ns6.gd.cnmobile.net (120.196.165.24)  51.14 ms  http: 403  http: 403

----------------------------------------------------------------------
成都教育网
traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  103.212.69.194  0.77 ms  http: 403  http: 403
 2  *
 3  unknown.telstraglobal.net (202.127.73.209)  11.10 ms  http: 403  http: 403
 4  *
 5  *
 6  *
 7  erx-cernet-bkb-as4538.e0-25.switch7.lax2.he.net (216.218.244.106)  183.43 ms  http: 403  http: 403
 8  101.4.117.185  208.31 ms  http: 403  http: 403
 9  101.4.117.213  201.96 ms  http: 403  http: 403
10  101.4.118.214  200.33 ms  http: 403  http: 403
11  *
12  101.4.117.81  208.61 ms  http: 403  http: 403
13  101.4.112.14  227.02 ms  http: 403  http: 403
14  *
15  101.4.116.158  229.62 ms  http: 403  http: 403
16  *
17  *
18  *
19  202.112.14.151  233.23 ms  http: 403  http: 403

----------------------------------------------------------------------
```
