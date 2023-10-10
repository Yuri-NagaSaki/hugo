---
title: "Aeza Moscow AMD 7950X 测评"
date: "2023-09-12"
categories: 
  - "vps"
  - "俄罗斯"
  - "performance"
---

> ## 套餐
> 
> Provider : Aeza  
> Type/Plan : MSKs-2  
> Processor : AMD Ryzen 9 7950X  
> Num of Core : 2 Cores  
> Memory : 4 GB  
> Storage : 60 GB NVMe  
> Bandwidth : Unlimited @ 10 Gbps IN | 10 Gbps OUT  
> Location : Moscow  
> Price : 120RMB

## 测评

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 22 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 2 @ 4491.540 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ❌ Disabled
RAM        : 3.8 GiB
Swap       : 1024.0 MiB
Disk       : 59.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-21-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv4 Network Information:
---------------------------------
ISP        : AEZA GROUP Ltd
ASN        : AS210644 AEZA GROUP Ltd
Host       : Aeza Group LLC
Location   : Moscow, Moscow (MOW)
Country    : Russia

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 40.02 MB/s   (10.0k) | 656.30 MB/s  (10.2k)
Write      | 40.12 MB/s   (10.0k) | 659.76 MB/s  (10.3k)
Total      | 80.15 MB/s   (20.0k) | 1.31 GB/s    (20.5k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.86 GB/s     (9.5k) | 5.07 GB/s     (4.9k)
Write      | 5.12 GB/s    (10.0k) | 5.41 GB/s     (5.2k)
Total      | 9.98 GB/s    (19.5k) | 10.48 GB/s   (10.2k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 86.6 Mbits/sec  | 168 Mbits/sec   | 46.6 ms        
Scaleway        | Paris, FR (10G)           | 2.43 Gbits/sec  | 2.86 Gbits/sec  | 48.5 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 41.1 ms        
Uztelecom       | Tashkent, UZ (10G)        | 4.35 Gbits/sec  | 2.48 Gbits/sec  | 48.9 ms        
Clouvider       | NYC, NY, US (10G)         | 34.7 Mbits/sec  | 60.2 Mbits/sec  | 112 ms         
Clouvider       | Dallas, TX, US (10G)      | 27.1 Mbits/sec  | 66.3 Mbits/sec  | 144 ms         
Clouvider       | Los Angeles, CA, US (10G) | 22.4 Mbits/sec  | 34.8 Mbits/sec  | 174 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 83.4 Mbits/sec  | busy            | 46.8 ms        
Scaleway        | Paris, FR (10G)           | busy            | busy            | 50.6 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 41.1 ms        
Uztelecom       | Tashkent, UZ (10G)        | 2.23 Gbits/sec  | 1.69 Gbits/sec  | 48.9 ms        
Clouvider       | NYC, NY, US (10G)         | busy            | 55.7 Mbits/sec  | 112 ms         
Clouvider       | Dallas, TX, US (10G)      | 27.5 Mbits/sec  | 63.8 Mbits/sec  | 144 ms         
Clouvider       | Los Angeles, CA, US (10G) | 23.1 Mbits/sec  | 35.0 Mbits/sec  | 174 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2186                          
Multi Core      | 3839                          
Full Test       | https://browser.geekbench.com/v6/cpu/2572843

YABS completed in 12 min 11 sec
```

### Bench

```

Server Insight                                  Hardware Information
--------------------- ---------------------
OS         : Debian GNU/Linux 11 (bullseye)     Model       : AMD Ryzen 9 7950X 16-Core Processor
Location   : Russia                             Core        : 2 @ 4491.540 MHz
Kernel     : 5.10.0-21-amd64                    AES-NI      : ✔ Enabled
Uptime     : 0 days, 0 hrs, 1 mins, 15 secs     VM-x/AMD-V  : ❌ Disabled
Virt       : kvm                                Swap        : 1024.0 MiB

Disk & Memory Usage                             Network Information
--------------------- ---------------------
Disk (1)   : 59.0 GiB                           ASN         : AS210644  
Disk Usage : 2.2 GiB (4% Used)                  ISP         : AEZA GROUP Ltd
Mem        : 3.8 GiB                            IPv4        : ✔ Enabled
Mem Usage  : 0.1 GiB (1% Used)                  IPv6        : ✔ Enabled

Disk Performance Check (ext4 on /dev/vda1) (R: Read, W: Write, T: Total)
+---------------------------------------------------------------------------+
| Size | Read        | Write       | Total       |       IOPS (R,W,T)       |
+===========================================================================+
| 4k   | 39.06 MB/s  | 39.16 MB/s  | 78.23 MB/s  | 10.0k  | 10.0k  | 20.0k  |
| 64k  | 640.72 MB/s | 644.09 MB/s | 1.25 GB/s   | 10.2k  | 10.3k  | 20.6k  |
| 512k | 4.51 GB/s   | 4.75 GB/s   | 9.28 GB/s   | 9.2k   | 9.7k   | 19.0k  |
| 1m   | 4.75 GB/s   | 5.07 GB/s   | 9.82 GB/s   | 4.9k   | 5.2k   | 10.1k  |
+---------------------------------------------------------------------------+

Network Performance Test (Region: Mixed)
+---------------------------------------------------------------------------------+
| Prot. | Provider    | Location        | Send         | Receive      | Latency   |
+---------------------------------------------------------------------------------+
| IPv4  | Airstream   | Wisconsin, US   |        busy  |        busy  |  133.9 ms |
|       | Uztelecom   | Tashkent, UZ    |    4.4 Gb/s  |    2.5 Gb/s  |   49.0 ms |
|       | Novogara    | Amsterdam, NL   |    1.7 Gb/s  |    1.9 Gb/s  |   41.1 ms |
|       | FiberBy     | Copenhagen, DK  |    3.2 Gb/s  |        busy  |   52.7 ms |
+---------------------------------------------------------------------------------+
| IPv6  | Airstream   | Wisconsin, US   |  783.3 Mb/s  |    1.3 Gb/s  |  131.5 ms |
|       | Uztelecom   | Tashkent, UZ    |    2.2 Gb/s  |    2.0 Gb/s  |   84.8 ms |
|       | Novogara    | Amsterdam, NL   |    4.5 Gb/s  |        busy  |   41.2 ms |
|       | FiberBy     | Copenhagen, DK  |    2.1 Gb/s  |    2.2 Gb/s  |   40.6 ms |
+---------------------------------------------------------------------------------+

+-----------------------------------------------+
| Geekbench 6.1.0 for Linux AVX2                |
+===============================================+
| Single Core        | 2202                     |
| Multi Core         | 3860                     |
+-----------------------------------------------+
| https://browser.geekbench.com/v6/cpu/2572690  |
+-----------------------------------------------+
| Benchy time spent  | 10 Minutes 8 Seconds     |
+-----------------------------------------------+
| Benchy result      | http://sprunge.us/eMbiw2 |
+-----------------------------------------------+
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 7950X 16-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 4491.540 MHz
 CPU 缓存          : L1: 256.00 KB / L2: 1.00 MB / L3: 16.00 MB
 硬盘空间          : 2.40 GiB / 58.98 GiB
 启动盘路径        : /dev/vda1
 内存              : 101.20 MiB / 3.84 GiB
 Swap              : 0 KiB / 1024.00 MiB
 系统在线时间      : 0 days, 0 hour 12 min
 负载              : 0.49, 0.50, 0.25
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-21-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS210644 AEZA GROUP Ltd
 IPV4 位置         : Moscow / Moscow / RU
 IPV6 ASN          : AS210644 AEZA GROUP Ltd
 IPV6 位置         : Amsterdam / North Holland
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           5507 Scores
 2 线程测试(多核)得分:          10890 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          65893.64 MB/s
 单线程写测试:          31007.88 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         42.6 MB/s (10.40 IOPS, 2.46s))          42.5 MB/s (10368 IOPS, 2.47s)
 1GB-1M Block           3.2 GB/s (3049 IOPS, 0.33s)             3.7 GB/s (3547 IOPS, 0.28s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 40.02 MB/s   (10.0k) | 656.51 MB/s  (10.2k)
Write      | 40.12 MB/s   (10.0k) | 659.96 MB/s  (10.3k)
Total      | 80.15 MB/s   (20.0k) | 1.31 GB/s    (20.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.77 GB/s     (9.3k) | 5.02 GB/s     (4.9k)
Write      | 5.02 GB/s     (9.8k) | 5.35 GB/s     (5.2k)
Total      | 9.79 GB/s    (19.1k) | 10.38 GB/s   (10.1k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 俄罗斯 圣彼得堡(列宁格勒)(LED03S05)
Youtube识别地域: 俄罗斯联邦(RU)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: SVO(SVO04S27)
Youtube识别地域: 俄罗斯联邦(RU)
----------------Netflix----------------
[IPv4]
Netflix在您的出口IP所在的国家不提供服务
[IPv6]
Netflix在您的出口IP所在的国家不提供服务
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口所在地区即将开通DisneyPlus，尽请期待哦！
[IPv6]
当前IPv6出口所在地区即将开通DisneyPlus，尽请期待哦！
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               No
 Netflix:                               No
 YouTube Premium:                       No 
 Amazon Prime Video:                    Yes (Region: RU)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   INTL
 Viu.com:                               No
 YouTube CDN:                           St. Petersburg 
 Spotify Registration:                  No
 Steam Currency:                        RUB
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: NL)
 Netflix:                               No
 YouTube Premium:                       No 
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Moscow 
 Netflix Preferred CDN:                 Failed (CDN IP Not Found)
 Spotify Registration:                  No
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【RU】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 68②
abuse得分(越低越好): 49④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  business⑨  
  公司类型(company_type):hosting①  hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
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
黑名单记录统计(有多少个黑名单网站有记录): 无害62 恶意3 可疑1 未检测23 ③
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  yandex邮箱: Yes
  outlook邮箱: Yes
  qq邮箱：No
------以下为IPV6检测------
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: RU 城市: Moscow 服务商: AS210644 AEZA GROUP Ltd
北京电信 219.141.136.12  测试超时
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
2023/09/12 05:09:54 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.15 ms         * RFC1918
4.37 ms         * RFC1918
0.80 ms         * RFC1918
18.53 ms        * RFC6598
22.13 ms        AS174 [COGENT-BONE] 瑞典 斯德哥尔摩省 斯德哥尔摩 cogentco.com
32.22 ms        AS174 [COGENT-BONE] 丹麦 丹麦首都地区 哥本哈根 cogentco.com
37.44 ms        AS174 [COGENT-BONE] 德国 汉堡州 汉堡 cogentco.com
45.75 ms        AS174 [COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
45.86 ms        AS174 [COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
95.74 ms        AS174 [COGENT-149] 德国 黑森州 美因河畔法兰克福 Cogent-CT-Peer cogentco.com
288.05 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
296.83 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
282.18 ms       AS134774 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.cn 电信
292.49 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.09 ms         * RFC1918
9.38 ms         * RFC1918
0.89 ms         * RFC1918
1.12 ms         * RFC6598
39.94 ms        AS6939 德国 黑森州 美因河畔法兰克福 he.net
367.59 ms       AS6939 [HURRICANE-6] 德国 黑森州 美因河畔法兰克福 he.net
247.07 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
248.24 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
252.74 ms       AS17816 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
* ms    AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
255.60 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.10 ms         * RFC1918
4.96 ms         * RFC1918
0.80 ms         * RFC1918
1.96 ms         * RFC6598
49.39 ms        AS6939 [HURRICANE-11] 法国 法兰西岛大区 巴黎 he.net
50.22 ms        * 法国 法兰西岛大区 巴黎
55.38 ms        AS58453 [CMI-INT] 英国 英格兰 伦敦 cmi.chinamobile.com 移动
255.14 ms       AS58453 [CMI-INT] 英国 英格兰 伦敦 cmi.chinamobile.com 移动
300.67 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
256.45 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
300.95 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
260.79 ms       AS9808 [CMNET] 中国 海南省 海口市 chinamobile.com 移动
259.49 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    23.09 Mbps      55.05 Mbps      40.82    0.0%
法兰克福         1998.69 Mbps    4926.53 Mbps    43.02    0.0%
洛杉矶           512.97 Mbps     3782.56 Mbps    172.62   0.0%
联通Fuzhou       280.38 Mbps     1577.51 Mbps    268.75   0.0%
联通海南         68.02 Mbps      460.38 Mbps     270.81   NULL
移动Chengdu      880.86 Mbps     3957.95 Mbps    261.85   0.0%
移动Lanzhou      684.90 Mbps     699.74 Mbps     254.58   NULL
------------------------------------------------------------------------
 总共花费      : 7 分 21 秒
 时间          : Tue Sep 12 05:14:58 MSK 2023
------------------------------------------------------------------------
```

### SpeedTest

```

   Speedtest by Ookla

      Server: Odido - Amsterdam (id: 52365)
         ISP: AEZA GROUP Ltd
Idle Latency:    39.55 ms   (jitter: 0.05ms, low: 39.52ms, high: 39.63ms)
    Download:  6982.77 Mbps (data used: 9.4 GB)                                                   
                 50.07 ms   (jitter: 28.56ms, low: 39.21ms, high: 432.96ms)
      Upload:  2076.62 Mbps (data used: 2.6 GB)                                                   
                 39.51 ms   (jitter: 0.29ms, low: 39.19ms, high: 42.57ms)
 Packet Loss:     0.0%
  Result URL: https://www.speedtest.net/result/c/f6a01491-a602-4318-94a3-90aedc953355
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-73-1024x366.png)

### 国内延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-72-1024x596.png)

### 全球延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-71.png)
