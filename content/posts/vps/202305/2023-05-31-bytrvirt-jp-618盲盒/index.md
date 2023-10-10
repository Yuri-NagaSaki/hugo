---
title: "bytrvirt JP 618盲盒"
date: "2023-05-31"
categories: 
  - "vps"
  - "jp"
---

线路就是日本去程cn2 9929。跟鸡总家那款一样，目前可能还没优化好。  
盲盒是LXC 独立IPv4+V6(V6等配置)，16.88U抽一次，一共两款盲盒，概率不一样，可以选择自己想抽的。

他家跟A400家的盲盒不一样，内存/硬盘/流量三个指标都是独立随机

![](https://catcat.blog/wp-content/uploads/2023/05/image-8-1024x570.png)

```
-------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD EPYC 7402P 24-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 2794.748 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 5.9 GB (1.8 GB 已用)
 内存              : 512 MB (195 MB 已用)
 Swap              : 256 MB (7 MB 已用)
 系统在线时间      : 0 days, 0 hour 48 min
 负载              : 0.52, 0.12, 0.09
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.15.107-2-pve
 TCP加速方式       : cubic
 虚拟化架构        : LXC
 NAT类型           : 开放型
 ASN组织           : AS147293 Nearoute Limited.
 位置              : Motoyoyogichō / JP
 地区              : Tokyo
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1564 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		40850.11 MB/s
 单线程写测试:		17805.17 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		87.6 MB/s (0.05 IOPS, 1.20s)		136 MB/s (33082 IOPS, 0.77s)
 1GB-1M Block		647 MB/s (616 IOPS, 1.62s)		536 MB/s (511 IOPS, 1.96s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 23.99 MB/s    (5.9k) | 78.40 MB/s    (1.2k)
Write      | 24.01 MB/s    (6.0k) | 78.81 MB/s    (1.2k)
Total      | 48.00 MB/s   (12.0k) | 157.21 MB/s   (2.4k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 195.88 MB/s    (382) | 222.56 MB/s    (217)
Write      | 206.29 MB/s    (402) | 237.38 MB/s    (231)
Total      | 402.17 MB/s    (784) | 459.95 MB/s    (448)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 日本 东京(NRT20S05)
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
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Yes (Region: JP)
 YouTube Premium:			Yes (Region: JP)
 Amazon Prime Video:			Yes (Region: JP)
 TVBAnywhere+:				No
 iQyi Oversea Region:			JP
 Viu.com:				No
 YouTube CDN:				Tokyo 
 Netflix Preferred CDN:			Tokyo  
 Spotify Registration:			No
 Steam Currency:			CNY
 ChatGPT:				No
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【JP】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：14
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：12
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/05/31 09:10:05 北京电信 219.141.136.12  测试超时
2023/05/31 09:10:05 北京联通 202.106.50.1    联通4837[普通线路]           
2023/05/31 09:10:05 北京移动 221.179.155.161 测试超时
2023/05/31 09:10:05 上海电信 202.96.209.133  测试超时
2023/05/31 09:10:05 上海联通 210.22.97.1     联通4837[普通线路]           
2023/05/31 09:10:05 上海移动 211.136.112.200 测试超时
2023/05/31 09:10:05 广州电信 58.60.188.222   电信163 [普通线路]           
2023/05/31 09:10:05 广州联通 210.21.196.6    联通4837[普通线路]           
2023/05/31 09:10:05 广州移动 120.196.165.24  测试超时
2023/05/31 09:10:05 成都电信 61.139.2.69     电信163 [普通线路]           
2023/05/31 09:10:05 成都联通 119.6.6.6       联通4837[普通线路]           
2023/05/31 09:10:05 成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS147293 Nearoute Limited.
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
7.31 ms  AS147293  日本, 东京都, 东京, 1nextnet.com
0.50 ms  AS51847  日本, 东京都, 东京, cogentco.com
53.25 ms  AS17676  中国, 北京, bbtec.net
67.56 ms  AS4134  中国, 北京, chinatelecom.com.cn, 电信
88.04 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
83.53 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
5.14 ms  AS147293  日本, 东京都, 东京, 1nextnet.com
0.46 ms  AS51847  日本, 东京都, 东京, cogentco.com
1.17 ms  AS2914  日本, 东京都, 东京, ntt.com
63.28 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
63.11 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
65.03 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
66.37 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
63.99 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
7.21 ms  AS147293  日本, 东京都, 东京, 1nextnet.com
0.47 ms  AS51847  日本, 东京都, 东京, cogentco.com
56.22 ms  AS9808  中国, 北京, chinamobile.com, 移动
58.75 ms  AS9808  中国, 北京, chinamobile.com, 移动
59.10 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 50.30 Mbps	 100.46 Mbps	 36.93	  0.0%
日本东京	 103.56 Mbps	 100.84 Mbps	 3.26	  0.0%
中国香港	 101.08 Mbps	 100.68 Mbps	 47.11	  0.0%
联通WuXi	 48.52 Mbps	 54.49 Mbps	 36.91	  0.0%
联通Fuzhou	 97.13 Mbps	 100.70 Mbps	 56.48	  0.0%
电信Zhenjiang5G	 102.44 Mbps	 100.93 Mbps	 43.03	  NULL
电信湖南5G	 98.73 Mbps	 103.08 Mbps	 59.57	  0.0%
移动Lanzhou	 94.57 Mbps	 100.93 Mbps	 69.95	  NULL
移动Chengdu	 92.21 Mbps	 112.35 Mbps	 89.96	  0.0%
------------------------------------------------------------------------
 总共花费      : 6 分 13 秒
 时间          : Wed May 31 09:14:02 UTC 2023
```

不大行，不推荐
