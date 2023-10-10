---
title: "Little Creek 评测"
date: "2023-03-02"
categories: 
  - "vps"
  - "usa"
tags: 
  - "usa"
---

## 1.官方网站

官网：[地址](https://www.littlecreekhosting.com/clients/index.php)

## 2.价格套餐

KVM-4 LET Special with DirectAdmin $4.50/Month [Order Here Now](https://www.littlecreekhosting.com/clients/cart.php?a=add&pid=382)

* * *

Standard DirectAdmin Control Panel  
Virtuozzo KVM  
CPU Core: 4  
RAM: 4096 MB  
NVMe: 80GB  
Bandwidth: 6000 GB/Month  
$4.50/Month  
[Order Here Now](https://www.littlecreekhosting.com/clients/cart.php?a=add&pid=382)

* * *

KVM-5 LET Special with DirectAdmin $8.00/Month [Order Here Now](https://www.littlecreekhosting.com/clients/cart.php?a=add&pid=383)

* * *

Standard DirectAdmin Control Panel  
Virtuozzo KVM  
CPU Core: 8  
RAM: 8192 MB  
NVMe: 160GB  
Bandwidth: 8000 GB/Month  
$8.00/Month  
[Order Here Now](https://www.littlecreekhosting.com/clients/cart.php?a=add&pid=383)

* * *

KVM-4 LET Special _No DirectAdmin_ $3.50/Month [Order Here Now](https://www.littlecreekhosting.com/clients/cart.php?a=add&pid=373)

* * *

Virtuozzo KVM  
CPU Core: 4  
RAM: 4096 MB  
NVMe: 80GB  
Bandwidth: 6000 GB/Month  
$3.50/Month  
[Order Here Now](https://www.littlecreekhosting.com/clients/cart.php?a=add&pid=373)

* * *

KVM-5 LET Special _No DirectAdmin_ $7.00/Month [Order Here Now](https://www.littlecreekhosting.com/clients/cart.php?a=add&pid=374)

* * *

Virtuozzo KVM  
CPU Core: 8  
RAM: 8192 MB  
NVMe: 160GB  
Bandwidth: 8000 GB/Month  
$7.00/Month  
[Order Here Now](https://www.littlecreekhosting.com/clients/cart.php?a=add&pid=374)

## 3.vps测试（7刀版本）

![](https://catcat.blog/wp-content/uploads/2023/10/image-101.png)

## 回程测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-102.png)

## 13刀版本融合怪测试

```
-----------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : Intel Xeon Processor (Cascadelake)
 CPU 核心数        : 1
 CPU 频率          : 2100.000 MHz
 CPU 缓存          : 4096 KB
 硬盘空间          : 19.0 GB (1.4 GB 已用)
 内存              : 976 MB (60 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 4 min
 负载              : 0.23, 0.09, 0.03
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-8-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 ASN组织           : AS174 Cogent Communications
 位置              : Durham / US
 地区              : North Carolina
-------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		2159 Scores
-------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		17763.83 MB/s
 单线程写测试:		12577.71 MB/s
----------------磁盘IO读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		->
 100MB-4K Block		23.1 MB/s (5642 IOPS, 4.54s)		->
 100MB-4K Block		23.1 MB/s (5642 IOPS, 4.54s)		15.7 MB/s (3824 IOPS, 6.69s)
 1GB-1M Block		->
 1GB-1M Block		431 MB/s (411 IOPS, 2.43s)		->
 1GB-1M Block		431 MB/s (411 IOPS, 2.43s)		1.4 GB/s (1377 IOPS, 0.73s)
-------------------磁盘IO读写测试--感谢yabs开源-----------------------
  ------ | --- ---- | ---- ---- 
Read       | 89.99 MB/s   (22.4k) | 409.72 MB/s   (6.4k)
Write      | 90.23 MB/s   (22.5k) | 411.88 MB/s   (6.4k)
Total      | 180.22 MB/s  (45.0k) | 821.60 MB/s  (12.8k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 912.40 MB/s   (1.7k) | 1.09 GB/s     (1.0k)
Write      | 960.88 MB/s   (1.8k) | 1.17 GB/s     (1.1k)
Total      | 1.87 GB/s     (3.6k) | 2.26 GB/s     (2.2k)
--------------------流媒体解锁--感谢sjlleo开源------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: IAD(IAD23S03)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: IAD(IAD23S03)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
---------------流媒体解锁--感谢RegionRestrictionCheck开源-------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				Yes (Region: US)
 Disney+:				Yes (Region: US)
 Netflix:				Yes (Region: US)
 YouTube Premium:			Yes
 Amazon Prime Video:			Yes (Region: US)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				No
 YouTube CDN:				Washington DC 
 Netflix Preferred CDN:			Seattle, WA  
 Spotify Registration:			No
 Steam Currency:			USD
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				Yes (Region: US)
 Disney+:				No
 Netflix:				Yes (Region: US)
 YouTube Premium:			Yes
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Washington DC 
 Netflix Preferred CDN:			Seattle, WA  
 Spotify Registration:			Yes (Region: US)
 Steam Currency:			Failed (Network Connection)
=======================================
-------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【US】
--------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化--------
[IPv4]
Your IP supports access to OpenAI. Region: US
[IPv6]
Your IP supports access to OpenAI. Region: US
-----------------欺诈分数以及IP质量检测--本频道原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：100
  匿名代理: No
  Tor出口节点: No
  服务器IP: No
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：20
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Commercial
Google搜索可行性：YES
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：100
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
-----------------三网回程--感谢zhanghanyun/backtrace开源--------------
2023/04/20 03:04:17 北京电信 219.141.136.12  电信163 [普通线路]           
2023/04/20 03:04:17 北京联通 202.106.50.1    联通4837[普通线路]           
2023/04/20 03:04:17 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/04/20 03:04:17 上海电信 202.96.209.133  测试超时
2023/04/20 03:04:17 上海联通 210.22.97.1     联通4837[普通线路]           
2023/04/20 03:04:17 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/04/20 03:04:17 广州电信 58.60.188.222   电信163 [普通线路]           
2023/04/20 03:04:17 广州联通 210.21.196.6    联通4837[普通线路]           
2023/04/20 03:04:17 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/04/20 03:04:17 成都电信 61.139.2.69     电信163 [普通线路]           
2023/04/20 03:04:17 成都联通 119.6.6.6       联通4837[普通线路]           
2023/04/20 03:04:17 成都移动 211.137.96.205  移动CMI [普通线路]           
------------------回程路由--感谢fscarmen开源及PR----------------------
IPv4 ASN: Cogent Communications
IPv6 ASN: Cogent Communications
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.59 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
1.95 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
2.29 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
2.12 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
6.15 ms  AS174  美国, 北卡罗来纳州, 夏洛特, cogentco.com
10.00 ms  AS174  美国, 乔治亚州, 亚特兰大, cogentco.com
24.97 ms  AS174  美国, 德克萨斯州, 休斯顿, cogentco.com
39.85 ms  AS174  美国, 德克萨斯州, 埃尔帕索, cogentco.com
48.20 ms  AS174  美国, 亚利桑那州, 凤凰城, cogentco.com
60.40 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
72.03 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
72.46 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
235.65 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
235.32 ms  AS134774  中国, 广东, 深圳, chinatelecom.com.cn, 电信
223.05 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.40 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
1.54 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
1.90 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
1.84 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
10.54 ms  AS174  美国, 北卡罗来纳州, 夏洛特, cogentco.com
9.77 ms  AS174  美国, 乔治亚州, 亚特兰大, cogentco.com
22.99 ms  AS174  美国, 德克萨斯州, 休斯顿, cogentco.com
46.53 ms  AS174  美国, 德克萨斯州, 埃尔帕索, cogentco.com
47.63 ms  AS174  美国, 亚利桑那州, 凤凰城, cogentco.com
59.59 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
59.49 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
229.50 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
225.85 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
219.64 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
222.96 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
244.25 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
221.10 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.2
0.30 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
6.72 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
1.73 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
2.67 ms  AS174  美国, 北卡罗来纳州, 罗利, cogentco.com
6.01 ms  AS174  美国, 北卡罗来纳州, 夏洛特, cogentco.com
10.58 ms  AS174  美国, 乔治亚州, 亚特兰大, cogentco.com
23.04 ms  AS174  美国, 德克萨斯州, 休斯顿, cogentco.com
39.57 ms  AS174  美国, 德克萨斯州, 埃尔帕索, cogentco.com
47.80 ms  AS174  美国, 亚利桑那州, 凤凰城, cogentco.com
59.98 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
59.39 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
70.65 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
69.82 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
70.01 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
251.73 ms  AS58453  中国, 上海, chinamobile.com, 移动
260.19 ms  AS9808  中国, 上海, chinamobile.com, 移动
244.77 ms  AS9808  中国, 上海, chinamobile.com, 移动
248.05 ms  AS9808  中国, 上海, chinamobile.com, 移动
287.32 ms  AS56040  中国, 广东, 广州, chinamobile.com, 移动
295.59 ms  AS56040  中国, 广东, 广州, chinamobile.com, 移动
284.15 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
------------------------ ecs-net--本频道独创 -------------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 705.22 Mbps	 730.10 Mbps	 81.70	  0.0%
洛杉矶		 713.35 Mbps	 707.47 Mbps	 59.64	  0.0%
新加坡		 362.66 Mbps	 467.91 Mbps	 551.20	  0.0%
联通Fuzhou	 396.28 Mbps	 724.85 Mbps	 225.15	  0.0%
联通上海5G	 325.81 Mbps	 684.42 Mbps	 253.32	  0.0%
电信天津	 2.57 Mbps	 578.65 Mbps	 222.72	  NULL
电信天津5G	 0.92 Mbps	 100.75 Mbps	 231.84	  9.7%
移动Chengdu	 276.02 Mbps	 548.03 Mbps	 273.96	  0.0%
----------------------------------------------------------------------
 总共花费      : 8 分 6 秒
 时间          : Thu 20 Apr 2023 03:10:27 AM EDT
```

## 4.测评

故事：  
LET上的一个商家，看官网说自己以前是个瓦工，建了网站发现托管在其他家不好用，于是自建，自己摸索，慢慢的规模起来了，就当这个故事是真的吧。大概就是几个人的小作坊。

推荐理由：  
· 稳定：用了几个月，还有LET几个用户反馈，很稳定。2020年百科君有推送，2021年有MJJ购买，没有什么问题；  
· DA授权：每个机器+1刀即可在自家的VPS上使用，如果你不需要可以少这1刀费用；  
· 硬件：GB6单核1000分，最低配置也给到了4核4G 80G NVMe，6T流量，1G带宽，如果去LET回帖可以双倍流量，做站绰绰有余；  
· 解锁IP：测试可以解锁NF和ChatGPT。

费用：最低3.5刀/月，需要DA授权+1刀。

槽点：机房托管在美东北卡罗来纳达勒姆，狗根网络+物理距离，建议中转加速，适合作落地鸡。
