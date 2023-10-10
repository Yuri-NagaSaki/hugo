---
title: "cloudsigma 日本VPS 测评"
date: "2023-07-10"
categories: 
  - "vps"
  - "jp"
---

## 流媒体解锁测试

```
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: JP)
 Netflix:                               Yes (Region: JP)
 YouTube Premium:                       Yes (Region: JP)
 Amazon Prime Video:                    Yes (Region: JP)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   JP
 Viu.com:                               No
 YouTube CDN:                           Associated with [IPS]
 Netflix Preferred CDN:                 Tokyo  
 Spotify Registration:                  No
 Steam Currency:                        JPY
 ChatGPT:                               Yes
=======================================
===============[ Japan ]===============
 DMM:                                   Yes
 DMM TV:                                No
 Abema.TV:                              No
 Niconico:                              Yes
 music.jp:                              Yes
 Telasa:                                No
 U-NEXT:                                Yes
 Hulu Japan:                            No
 TVer:                                  Yes
 GYAO!:                                 Yes
 WOWOW:                                 Failed
 VideoMarket:                           Failed (Unexpected Result: 404)
 FOD(Fuji TV):                          Yes
 Radiko:                                Yes (City: TOKYO)
 Karaoke@DAM:                           Yes
 J:com On Demand:                       Yes
 ---Game---
 Kancolle Japan:                        Yes
 Pretty Derby Japan:                    Yes
 Konosuba Fantastic Days:               Yes
 Princess Connect Re:Dive Japan:        Yes
 World Flipper Japan:                   Yes
 Project Sekai: Colorful Stage:         Yes
=======================================
```

## 融合怪测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : Intel(R) Xeon(R) Gold 6148 CPU @ 2.40GHz
 CPU 核心数        : 1
 CPU 频率          : 2394.374 MHz
 CPU 缓存          : 16384 KB
 硬盘空间          : 4.99 GiB / 49.10 GiB
 启动盘路径        : /dev/vda1
 内存              : 141.60 MiB / 1.92 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 10 min
 负载              : 0.40, 0.17, 0.07
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 无法检测
 IPV4 ASN          : AS131939 IPS INC
 IPV4 位置         : Urayasu / Tokyo / JP
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           821 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          15885.45 MB/s
 单线程写测试:          10149.98 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         25.2 MB/s (6147 IOPS, 4.16s)            54.0 MB/s (13185 IOPS, 1.94s)
 1GB-1M Block           1.2 GB/s (1161 IOPS, 0.86s)             1.3 GB/s (1240 IOPS, 0.81s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 178.38 MB/s  (44.5k) | 897.70 MB/s  (14.0k)
Write      | 178.85 MB/s  (44.7k) | 902.42 MB/s  (14.1k)
Total      | 357.23 MB/s  (89.3k) | 1.80 GB/s    (28.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 886.28 MB/s   (1.7k) | 791.87 MB/s    (773)
Write      | 933.37 MB/s   (1.8k) | 844.61 MB/s    (824)
Total      | 1.81 GB/s     (3.5k) | 1.63 GB/s     (1.5k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: IPS
视频缓存节点地域: 菲律宾马尼拉(MNL2)
Youtube识别地域: 日本(JP)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：日本
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：日本区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: JP)
 Netflix:                               Yes (Region: JP)
 YouTube Premium:                       Yes (Region: JP)
 Amazon Prime Video:                    Yes (Region: JP)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   JP
 Viu.com:                               No
 YouTube CDN:                           Associated with [IPS]
 Netflix Preferred CDN:                 Tokyo  
 Spotify Registration:                  No
 Steam Currency:                        JPY
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【JP】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：50
  匿名代理: No
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：47
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Fixed Line ISP
Google搜索可行性：NO
端口25检测:
  本地: No
  163邮箱：No
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/07/10 08:25:30 北京电信 219.141.136.12  电信163 [普通线路]           
2023/07/10 08:25:30 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/10 08:25:30 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/10 08:25:30 上海电信 202.96.209.133  电信163 [普通线路]           
2023/07/10 08:25:30 上海联通 210.22.97.1     联通4837[普通线路]           
2023/07/10 08:25:30 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/10 08:25:30 广州电信 58.60.188.222   电信163 [普通线路]           
2023/07/10 08:25:30 广州联通 210.21.196.6    联通4837[普通线路]           
2023/07/10 08:25:30 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/07/10 08:25:30 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/10 08:25:30 成都联通 119.6.6.6       联通4837[普通线路]           
2023/07/10 08:25:30 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.59 ms  AS131939  日本, 东京都, 东京, ipsism.co.jp
0.13 ms  AS131939  日本, 东京都, 东京, ipsism.co.jp
0.22 ms  AS131939  日本, 东京都, 东京, ipsism.co.jp
1.23 ms  AS10010  日本, 东京都, tokai-com.co.jp
1.11 ms  AS10010  日本, 东京都, tokai-com.co.jp
0.58 ms  AS2497  日本, 东京都, 东京, iij.ad.jp
0.61 ms  AS2497  日本, 东京都, 东京, iij.ad.jp
2.02 ms  AS2497  日本, 东京都, 东京, iij.ad.jp
1.62 ms  AS4134  日本, 东京都, 东京, chinatelecom.com.cn, 电信
49.56 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
50.17 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
55.13 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
53.98 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.35 ms  AS131939  日本, 东京都, 东京, ipsism.co.jp
0.17 ms  AS131939  日本, 东京都, 东京, ipsism.co.jp
0.23 ms  AS131939  日本, 东京都, 东京, ipsism.co.jp
1.17 ms  AS10010  日本, 东京都, tokai-com.co.jp
0.86 ms  AS10010  日本, 东京都, tokai-com.co.jp
2.11 ms  AS2497  日本, 东京都, 东京, iij.ad.jp
0.58 ms  AS2497  日本, 东京都, 东京, iij.ad.jp
1.11 ms  AS2497  日本, 东京都, 东京, iij.ad.jp
1.12 ms  AS2497  日本, 东京都, 东京, iij.ad.jp
34.65 ms  AS2497  日本, 东京都, 东京, iij.ad.jp
64.34 ms  AS4837  中国, 上海, chinaunicom.com, 联通
96.54 ms  AS4837  中国, 上海, chinaunicom.com, 联通
94.20 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
106.77 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
118.49 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.38 ms  AS131939  日本, 东京都, 东京, ipsism.co.jp
0.14 ms  AS131939  日本, 东京都, 东京, ipsism.co.jp
0.25 ms  AS131939  日本, 东京都, 东京, ipsism.co.jp
1.19 ms  AS10010  日本, 东京都, tokai-com.co.jp
1.05 ms  AS10010  日本, 东京都, tokai-com.co.jp
1.40 ms  AS3491,AS31713  日本, 东京都, 东京, pccw.com
54.03 ms  AS3491,AS31713  中国, 香港, pccw.com
53.49 ms  AS58453  中国, 香港, chinamobile.com, 移动
182.49 ms  AS58453  中国, 上海, chinamobile.com, 移动
59.90 ms  AS9808  中国, 上海, chinamobile.com, 移动
98.71 ms  AS9808  中国, 北京, chinamobile.com, 移动
197.17 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
```
