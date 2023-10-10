---
title: "BuyVM 卢森堡 5900x 不限流量"
date: "2023-04-23"
categories: 
  - "vps"
  - "eu"
tags: 
  - "eu"
---

## 融合怪脚本测试

```
----------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD Ryzen 9 5900X 12-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 3693.062 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 20.0 GB (4.6 GB 已用)
 内存              : 976 MB (359 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 25 days, 20 hour 44 min
 负载              : 0.12, 0.04, 0.01
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-19-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 ASN组织           : AS53667 FranTech Solutions
 位置              : Luxembourg / LU
 地区              : Luxembourg
-------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           4474 Scores
-------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          47227.45 MB/s
 单线程写测试:          23861.89 MB/s
----------------磁盘IO读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         ->
 100MB-4K Block         71.3 MB/s (0.06K IOPS, 1.47s)           ->
 100MB-4K Block         71.3 MB/s (0.06 IOPS, 1.47s)            83.7 MB/s (20431 IOPS, 1.25s)
 1GB-1M Block           ->
 1GB-1M Block           1.6 GB/s (1570 IOPS, 0.64s)             ->
 1GB-1M Block           1.6 GB/s (1570 IOPS, 0.64s)             1.9 GB/s (1773 IOPS, 0.56s)
-------------------磁盘IO读写测试--感谢yabs开源-----------------------
  ------ | --- ---- | ---- ---- 
Read       | 309.27 MB/s  (77.3k) | 1.04 GB/s    (16.3k)
Write      | 310.08 MB/s  (77.5k) | 1.05 GB/s    (16.4k)
Total      | 619.35 MB/s (154.8k) | 2.10 GB/s    (32.8k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.21 GB/s     (2.3k) | 1.45 GB/s     (1.4k)
Write      | 1.28 GB/s     (2.5k) | 1.55 GB/s     (1.5k)
Total      | 2.50 GB/s     (4.8k) | 3.01 GB/s     (2.9k)
--------------------流媒体解锁--感谢sjlleo开源------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 捷克 布拉格(PRG03S04)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：卢森堡
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：卢森堡区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
---------------流媒体解锁--感谢RegionRestrictionCheck开源-------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: LU)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: LU)
 Amazon Prime Video:                    Yes (Region: LU)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   INTL
 Viu.com:                               No
 YouTube CDN:                           Prague 
 Netflix Preferred CDN:                 Washington DC  
 Spotify Registration:                  No
 Steam Currency:                        EUR
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
-------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【LU】
--------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化--------
[IPv4]
Your IP supports access to OpenAI. Region: LU
[IPv6]
IPv6 is not supported on the current host. Skip...
-----------------欺诈分数以及IP质量检测--本频道原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：74
  匿名代理: Yes
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：19
ip-api数据库:
  手机流量: No
  代理服务: Yes
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：NO
-----------------三网回程--感谢zhanghanyun/backtrace开源--------------
2023/04/22 19:44:38 北京电信 219.141.136.12  测试超时
2023/04/22 19:44:38 北京联通 202.106.50.1    联通4837[普通线路]           
2023/04/22 19:44:38 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/04/22 19:44:38 上海电信 202.96.209.133  测试超时
2023/04/22 19:44:38 上海联通 210.22.97.1     联通4837[普通线路]           
2023/04/22 19:44:38 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/04/22 19:44:38 广州电信 58.60.188.222   测试超时
2023/04/22 19:44:38 广州联通 210.21.196.6    联通4837[普通线路]           
2023/04/22 19:44:38 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/04/22 19:44:38 成都电信 61.139.2.69     测试超时
2023/04/22 19:44:38 成都联通 119.6.6.6       联通4837[普通线路]           
2023/04/22 19:44:38 成都移动 211.137.96.205  移动CMI [普通线路]           
------------------回程路由--感谢fscarmen开源及PR----------------------
IPv4 ASN: FranTech Solutions
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.41 ms  AS53667  卢森堡, buyvm.net
2.02 ms  *  局域网
5.76 ms  AS6939  比利时, 布鲁塞尔－首都大区, 布鲁塞尔, he.net
14.51 ms  AS6939  英国, 伦敦, he.net
203.16 ms  AS4134  英国, 伦敦, chinatelecom.com.cn, 电信
563.14 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
571.65 ms  AS134774  中国, 广东, 深圳, chinatelecom.com.cn, 电信
705.73 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
89.25 ms  AS53667  卢森堡, buyvm.net
2.06 ms  *  局域网
12.67 ms  AS6939  德国, 黑森州, 法兰克福, he.net
5.83 ms  AS6939  德国, 黑森州, 法兰克福, he.net
223.41 ms  AS6939  德国, 黑森州, 法兰克福, he.net
237.11 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
244.15 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
226.40 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
229.67 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
236.68 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
229.12 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.2
4.43 ms  AS53667  卢森堡, buyvm.net
1.83 ms  *  局域网
6.74 ms  AS6939  比利时, 布鲁塞尔－首都大区, 布鲁塞尔, he.net
12.48 ms  AS6939  法国, 法兰西岛大区, 巴黎, he.net
19.39 ms  AS9009  法国, 法兰西岛大区, 巴黎, equinix.com
13.95 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
14.29 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
234.65 ms  AS58453  中国, 上海, chinamobile.com, 移动
250.81 ms  AS9808  中国, 上海, chinamobile.com, 移动
241.33 ms  AS9808  中国, 上海, chinamobile.com, 移动
245.46 ms  AS9808  中国, 上海, chinamobile.com, 移动
276.18 ms  AS56040  中国, 广东, 广州, chinamobile.com, 移动
280.87 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
------------------------ ecs-net--本频道独创 -------------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    1028.89 Mbps    931.09 Mbps     1.14     0.0%
洛杉矶           237.04 Mbps     376.48 Mbps     142.88   0.0%
新加坡           43.83 Mbps      621.20 Mbps     220.77   0.3%
联通WuXi         224.72 Mbps     220.80 Mbps     249.80   0.3%
联通上海5G       141.73 Mbps     370.04 Mbps     229.56   0.0%
电信天津         3.09 Mbps       9.80 Mbps       630.55   NULL
电信湖南5G       0.75 Mbps       16.76 Mbps      549.02   9.7%
移动Chengdu      243.72 Mbps     515.15 Mbps     224.51   0.3%
移动陕西5G       16.70 Mbps      462.19 Mbps     274.54   0.0%
----------------------------------------------------------------------
 总共花费      : 7 分 12 秒
 时间          : Sat 22 Apr 2023 07:50:48 PM PDT
```
