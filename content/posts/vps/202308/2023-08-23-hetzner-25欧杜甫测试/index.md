---
title: "Hetzner 25欧杜甫测试"
date: "2023-08-23"
categories: 
  - "vps"
  - "eu"
---

## SSD 测试

```

  CPU 型号              Intel(R) Core(TM) i7-7700 CPU @ 3.60GHz
  CPU 核心              合计 4 核心，8 线程
  CPU 状态              当前主频 1600.012 MHz
  内存大小              64091 MB (275 MB 已用)

  第 1 块硬盘           通电 10743 小时，型号 SAMSUNG MZVLB512HAJQ-00000
  第 2 块硬盘           通电 6522 小时，型号 SAMSUNG MZVLB512HAJQ-00000

  硬盘大小              937.5 GB

  服务器时间            2023-08-23 21:24:01
  运行时间              0 days 0 hour 14 min
  系统负载              0.06, 0.05, 0.05
  虚拟化技术            No Virtualization Detected

  IPv4 地址             178.63.xxx.xxx
  IPv6 地址             2a01:4f8:xxxx:xxxx
  运营商                AS24940 Hetzner Online GmbH
  地理位置              DE, Berlin, Berlin

  操作系统              Debian 11.7 bullseye (x86_64)
  系统内核              5.10.0-23-amd64
  TCP 加速              bbr

  当前脚本版本          1.4.1.1

  顺序写入 (1st)        1200 MB/s
  顺序写入 (2nd)        1300 MB/s
  顺序写入 (3rd)        1300 MB/s
  顺序写入 (4th)        1200 MB/s
  顺序写入 (5th)        1300 MB/s
  顺序写入 (avg)        1266.7 MB/s
```

## Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 1 hours, 1 minutes
Processor  : Intel(R) Core(TM) i7-7700 CPU @ 3.60GHz
CPU cores  : 8 @ 1600.056 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 62.6 GiB
Swap       : 0.0 KiB
Disk       : 937.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-23-amd64
VM Type    : NONE
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Hetzner Online GmbH
ASN        : AS24940 Hetzner Online GmbH
Host       : Hetzner
Location   : Falkenstein, Saxony (SN)
Country    : Germany

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 735.38 MB/s (183.8k) | 1.74 GB/s    (27.3k)
Write      | 737.33 MB/s (184.3k) | 1.75 GB/s    (27.4k)
Total      | 1.47 GB/s   (368.1k) | 3.50 GB/s    (54.7k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.69 GB/s     (3.3k) | 1.72 GB/s     (1.6k)
Write      | 1.78 GB/s     (3.4k) | 1.83 GB/s     (1.7k)
Total      | 3.47 GB/s     (6.7k) | 3.56 GB/s     (3.4k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 172 Mbits/sec   | 369 Mbits/sec   | 23.9 ms        
Scaleway        | Paris, FR (10G)           | 832 Mbits/sec   | 931 Mbits/sec   | 21.2 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 11.7 ms        
Uztelecom       | Tashkent, UZ (10G)        | 786 Mbits/sec   | 701 Mbits/sec   | 89.7 ms        
Clouvider       | NYC, NY, US (10G)         | 630 Mbits/sec   | 121 Mbits/sec   | 85.3 ms        
Clouvider       | Dallas, TX, US (10G)      | 31.3 Mbits/sec  | 48.6 Mbits/sec  | 127 ms         
Clouvider       | Los Angeles, CA, US (10G) | 25.5 Mbits/sec  | 35.7 Mbits/sec  | 156 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 174 Mbits/sec   | 387 Mbits/sec   | 23.8 ms        
Scaleway        | Paris, FR (10G)           | 808 Mbits/sec   | 854 Mbits/sec   | 21.7 ms        
NovoServe       | North Holland, NL (40G)   | 841 Mbits/sec   | busy            | 11.7 ms        
Uztelecom       | Tashkent, UZ (10G)        | busy            | 697 Mbits/sec   | 89.5 ms        
Clouvider       | NYC, NY, US (10G)         | 655 Mbits/sec   | busy            | 89.0 ms        
Clouvider       | Dallas, TX, US (10G)      | 30.3 Mbits/sec  | 47.1 Mbits/sec  | 126 ms         
Clouvider       | Los Angeles, CA, US (10G) | 22.4 Mbits/sec  | 38.6 Mbits/sec  | 156 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 1557                          
Multi Core      | 5187                          
Full Test       | https://browser.geekbench.com/v6/cpu/2362188

YABS completed in 11 min 42 sec
```

## 融合怪

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : Intel(R) Core(TM) i7-7700 CPU @ 3.60GHz
 CPU 核心数        : 1 物理核心, 4 总核心, 8 总线程数
 CPU 频率          : 4089.603 MHz
 CPU 缓存          : L1: 256.00 KB / L2: 1.00 MB / L3: 8.00 MB
 硬盘空间          : 678.17 GiB / 936.60 GiB
 启动盘路径        : /dev/md1
 内存              : 24.31 GiB / 62.59 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 14 days, 19 hour 25 min
 负载              : 1.42, 1.76, 2.01
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-amd64
 TCP加速方式       : bbr
 虚拟化架构        : Dedicated
 NAT类型           : 开放型
 IPV4 ASN          : AS24940 Hetzner Online GmbH
 IPV4 位置         : Berlin / Berlin / DE
 IPV6 ASN          : AS24940 Hetzner Online GmbH
 IPV6 位置         : Nuremberg / DE-BY
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           1231 Scores
 8 线程测试(多核)得分:          7917 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          25162.12 MB/s
 单线程写测试:          17245.78 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         145 MB/s (35.44 IOPS, 0.72s))           228 MB/s (55724 IOPS, 0.46s)
 1GB-1M Block           1.5 GB/s (1439 IOPS, 0.69s)             2.6 GB/s (2483 IOPS, 0.40s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 594.48 MB/s (148.6k) | 358.22 MB/s   (5.5k)
Write      | 596.05 MB/s (149.0k) | 360.10 MB/s   (5.6k)
Total      | 1.19 GB/s   (297.6k) | 718.32 MB/s  (11.2k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 125.34 MB/s    (244) | 154.14 MB/s    (150)
Write      | 132.00 MB/s    (257) | 164.40 MB/s    (160)
Total      | 257.35 MB/s    (501) | 318.54 MB/s    (310)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA15S37)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA15S37)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
Netflix在您的出口IP所在的国家不提供服务
[IPv6]
Netflix在您的出口IP所在的国家不提供服务
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：德国区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：德国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: DE)
 HotStar:                               No
 Disney+:                               No
 YouTube Premium:                       Failed
 Amazon Prime Video:                    Yes (Region: DE)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   DE
 Viu.com:                               No
 YouTube CDN:                           Frankfurt 
 Netflix Preferred CDN:                 Frankfurt  
 Spotify Registration:                  Yes (Region: DE)
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: DE)
 YouTube Premium:                       Failed
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Frankfurt 
 Netflix Preferred CDN:                 Frankfurt  
 Spotify Registration:                  Yes (Region: DE)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【DE】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 28②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  hosting⑨  
  公司类型(company_type):hosting①  hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes② ⑥ ⑨ 
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
Google搜索可行性：NO
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
  qq邮箱：No
------以下为IPV6检测------
欺诈分数(越低越好): 19②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: DE 城市: Berlin 服务商: AS24940 Hetzner Online GmbH
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
2023/09/07 16:37:46 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
1.03 ms         AS24940 德国 柏林 hetzner.com
0.49 ms         AS24940 [DE-HETZNER] 德国 莱茵兰-普法尔茨州 法尔肯斯泰因 hetzner.com
2.85 ms         AS24940 [DE-HETZNER] 德国 巴伐利亚州 纽伦堡 hetzner.com
5.60 ms         AS1299 [ARELION-NET] 德国 巴伐利亚州 纽伦堡 arelion.com
5.87 ms         AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
6.60 ms         AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
7.41 ms         AS4134 [CHINANET-BB] 德国 黑森州 美因河畔法兰克福 CT-POP chinatelecom.com.cn 电信
206.72 ms       AS4134 [CHINANET-BB] 中国 香港 chinatelecom.com.cn 电信
205.13 ms       AS4134 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.com.cn 电信
204.60 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.26 ms         AS24940 德国 柏林 hetzner.com
0.48 ms         AS24940 [DE-HETZNER] 德国 莱茵兰-普法尔茨州 法尔肯斯泰因 hetzner.com
2.98 ms         AS24940 [DE-HETZNER] 澳大利亚 西澳大利亚州 珀斯 hetzner.com
2.87 ms         * France Ile-de-France Paris
6.09 ms         AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
55.35 ms        AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
303.60 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
205.40 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
205.72 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
202.01 ms       AS17816 [UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
207.99 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
215.10 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
1.44 ms         AS24940 德国 柏林 hetzner.com
0.58 ms         AS24940 [DE-HETZNER] 德国 莱茵兰-普法尔茨州 法尔肯斯泰因 hetzner.com
4.93 ms         AS24940 [DE-HETZNER] 德国 黑森州 美因河畔法兰克福 hetzner.com
5.93 ms         AS58453 [DE-CIX] 德国 黑森州 美因河畔法兰克福 DE-CIX Frankfurt - China Mobile International - 100Gbps cmi.chinamobile.com
5.97 ms         AS58453 [CMI-INT] 德国 黑森州 美茵河畔法兰克福 cmi.chinamobile.com 移动
202.42 ms       AS58453 [CMI-INT] 德国 黑森州 美因河畔法兰克福 cmi.chinamobile.com 移动
204.12 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
203.94 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
304.64 ms       AS9808 [CMNET] 中国 上海市 chinamobile.com 移动
207.27 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
208.74 ms       AS9808 [CMNET] 中国 北京市 chinamobile.com 移动
208.42 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
```
