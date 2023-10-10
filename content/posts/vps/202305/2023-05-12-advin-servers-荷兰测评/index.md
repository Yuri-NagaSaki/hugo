---
title: "Advin Servers 荷兰测评"
date: "2023-05-12"
categories: 
  - "vps"
  - "eu"
---

## 官网

**官方网站：[点我](https://clients.advinservers.com/aff.php?aff=336)**

**Looking Glass：**

> **Tokyo, JP:** 194.87.169.7  
> **Amsterdam, NL:** 45.61.161.93 (LG: [http://45.61.161.93/](http://45.61.161.93/))  
> **Coventry, UK:** 78.157.214.36 (LG: [http://78.157.214.36](http://78.157.214.36/))  
> **Dallas, TX:** 172.99.233.46 (LG: [http://172.99.233.46](http://172.99.233.46/))  
> **Los Angeles, CA:** 45.8.22.11 (LG: [http://45.8.22.11](http://45.8.22.11/))  
> **Miami, FL:** 23.137.104.80 (LG: [http://23.137.104.80](http://23.137.104.80/))  
> **New York, NY:** 45.61.162.146 (LG: [http://45.61.162.146](http://45.61.162.146/))

## 规格

![](https://catcat.blog/wp-content/uploads/2023/05/image-1024x494.png)

## 融合怪脚本测试

```
-----------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD EPYC Processor
 CPU 核心数        : 4
 CPU 频率          : 3393.624 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 110.0 GB (1.9 GB 已用)
 内存              : 16008 MB (102 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 1 min
 负载              : 0.51, 0.19, 0.07
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-21-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 ASN组织           : AS206216 Advin Services LLC
 位置              : Amsterdam / NL
 地区              : North Holland
-------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           5101 Scores
 4 线程测试(多核)得分:          18764 Scores
-------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          53951.75 MB/s
 单线程写测试:          26637.20 MB/s
----------------磁盘IO读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         60.6 MB/s (0.07 IOPS, 1.73s)            68.7 MB/s (16779 IOPS, 1.53s)
 1GB-1M Block           1.2 GB/s (1109 IOPS, 0.90s)             1.2 GB/s (1109 IOPS, 0.90s)
-------------------磁盘IO读写测试--感谢yabs开源-----------------------
  ------ | --- ---- | ---- ---- 
Read       | 69.06 MB/s   (17.2k) | 948.59 MB/s  (14.8k)
Write      | 69.25 MB/s   (17.3k) | 953.58 MB/s  (14.8k)
Total      | 138.32 MB/s  (34.5k) | 1.90 GB/s    (29.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.01 GB/s     (1.9k) | 986.18 MB/s    (963)
Write      | 1.06 GB/s     (2.0k) | 1.05 GB/s     (1.0k)
Total      | 2.08 GB/s     (4.0k) | 2.03 GB/s     (1.9k)
--------------------流媒体解锁--感谢sjlleo开源------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 荷兰阿姆斯特丹(AMS17S06)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：荷兰
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：荷兰区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
---------------流媒体解锁--感谢RegionRestrictionCheck开源-------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: NL)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: BE)
 Amazon Prime Video:                    Yes (Region: NL)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   INTL
 Viu.com:                               No
 YouTube CDN:                           Amsterdam 
 Netflix Preferred CDN:                 Associated with [RETN Limited] in [Budapest ]
 Spotify Registration:                  Yes (Region: NL)
 Steam Currency:                        EUR
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
-------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【NL】
--------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化--------
[IPv4]
Your IP supports access to OpenAI. Region: NL
[IPv6]
IPv6 is not supported on the current host. Skip...
-----------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：0
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：50
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
-----------------三网回程--感谢zhanghanyun/backtrace开源--------------
2023/05/12 06:44:16 北京电信 219.141.136.12  测试超时
2023/05/12 06:44:16 北京联通 202.106.50.1    联通4837[普通线路]           
2023/05/12 06:44:16 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/05/12 06:44:16 上海电信 202.96.209.133  测试超时
2023/05/12 06:44:16 上海联通 210.22.97.1     联通4837[普通线路]           
2023/05/12 06:44:16 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/05/12 06:44:16 广州电信 58.60.188.222   测试超时
2023/05/12 06:44:16 广州联通 210.21.196.6    联通4837[普通线路]           
2023/05/12 06:44:16 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/05/12 06:44:16 成都电信 61.139.2.69     电信163 [普通线路]           
2023/05/12 06:44:16 成都联通 119.6.6.6       联通4837[普通线路]           
2023/05/12 06:44:16 成都移动 211.137.96.205  移动CMI [普通线路]           
------------------回程路由--感谢fscarmen开源及PR----------------------
IPv4 ASN: AS206216 Advin Services LLC
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
21.47 ms  AS206216  荷兰, 林堡省, 艾赫尔斯霍芬, buyvm.net
161.92 ms  *  局域网
0.32 ms  AS49581  荷兰, 林堡省, 艾赫尔斯霍芬, tube-hosting.de
6.98 ms  *  局域网
6.34 ms  AS3356  荷兰, 北荷兰省, 阿姆斯特丹, level3.com
15.37 ms  AS3356  德国, 黑森州, 法兰克福, level3.com
260.15 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
268.36 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
13.70 ms  AS206216  荷兰, 林堡省, 艾赫尔斯霍芬, buyvm.net
22.92 ms  *  局域网
1.11 ms  AS49581  荷兰, 林堡省, 艾赫尔斯霍芬, tube-hosting.de
4.99 ms  *  局域网
13.20 ms  *  局域网
23.58 ms  AS9002  奥地利, 维也纳州, 维也纳, retn.net
28.08 ms  AS5511  ORANGE.COM 骨干网, orange.com
31.25 ms  AS5511  德国, 黑森州, 法兰克福, orange.com
144.79 ms  AS4837  中国, 北京, chinaunicom.com, 联通
178.05 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
180.49 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
193.80 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
183.78 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
202.95 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
179.22 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.2
12.57 ms  AS206216  荷兰, 林堡省, 艾赫尔斯霍芬, buyvm.net
20.09 ms  *  局域网
28.17 ms  AS49581  荷兰, 林堡省, 艾赫尔斯霍芬, tube-hosting.de
4.91 ms  *  局域网
14.29 ms  AS1299  英国, 伦敦, telia.com
14.19 ms  AS1299  英国, 伦敦, telia.com
16.54 ms  AS1299  英国, 伦敦, telia.com
462.53 ms  AS58453  中国, 上海, chinamobile.com, 移动
462.41 ms  AS9808  中国, 上海, chinamobile.com, 移动
465.03 ms  AS9808  中国, 上海, chinamobile.com, 移动
480.02 ms  AS9808  中国, 上海, chinamobile.com, 移动
508.59 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
-------------------自动更新测速节点列表--本脚本原创-------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    7909.70 Mbps    8483.83 Mbps    6.03     0.0%
洛杉矶           607.84 Mbps     2799.81 Mbps    149.56   0.0%
新加坡           115.35 Mbps     3690.45 Mbps    187.54   0.0%
联通沈阳         117.41 Mbps     331.62 Mbps     337.36   1.7%
联通郑州5G       572.58 Mbps     1412.48 Mbps    259.71   NULL
----------------------------------------------------------------------
 总共花费      : 5 分 37 秒
 时间          : Fri May 12 06:48:08 UTC 2023
----------------------------------------------------------------------
```
