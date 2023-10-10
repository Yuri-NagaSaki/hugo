---
title: "Hostbbr 3T超大存储年付72刀翻倍款vps测评"
date: "2023-06-02"
categories: 
  - "vps"
  - "eu"
---

## 介绍

正在寻找具有海量存储容量和一流性能的可靠且价格合理的托管服务？HostBrr 就是您的最佳选择！凭借其令人印象深刻的平均 2.2$/1TB 存储空间和尖端的 7950X3d 服务器

### 官网

[**_地址_**](https://my.hostbrr.com/order/forms/a/MzQw)

![](https://catcat.blog/wp-content/uploads/wordpress/2023/06/image-1024x589.png)

The first weekend of the summer is officially starting, and HostBrr has finally provisioned a large storage server for all your storage needs! In celebration of that, we're having a large weekend/summer sale on these new VPS. Save 20% on our storage deals using coupon **20STORAGEBRR** and save a massive 40% using **40STORAGEBRR** when ordering quarterly. These discounts are of course **recurring!**. The storage VPS is provisioned with IPv4 NAT (20 ports) and IPv6/64.

## 优惠码

月付20%优惠：**20STORAGEBRR**

季付40%优惠：**40STORAGEBRR**

## 融合怪脚本测试

```
------------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : Intel(R) Xeon(R) W-2145 CPU @ 3.70GHz
 CPU 核心数        : 2
 CPU 频率          : 3695.994 MHz
 CPU 缓存          : 11264 KB
 硬盘空间          : 2993.7 GB (2.7 GB 已用)
 内存              : 5905 MB (198 MB 已用)
 Swap              : 1023 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 5 min
 负载              : 0.27, 0.11, 0.04
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-20-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 独立映射,独立过滤,不支持回环
 ASN组织           : AS24940 Hetzner Online GmbH
 位置              : Gunzenhausen / DE
 地区              : Bavaria
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1499 Scores
 2 线程测试(多核)得分: 		2948 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		29087.31 MB/s
 单线程写测试:		20893.21 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		58.6 MB/s (0.07 IOPS, 1.79s)		67.7 MB/s (16522 IOPS, 1.55s)
 1GB-1M Block		855 MB/s (815 IOPS, 1.23s)		1.1 GB/s (1044 IOPS, 0.96s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 220.18 MB/s  (55.0k) | 737.27 MB/s  (11.5k)
Write      | 220.76 MB/s  (55.1k) | 741.15 MB/s  (11.5k)
Total      | 440.94 MB/s (110.2k) | 1.47 GB/s    (23.0k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 978.39 MB/s   (1.9k) | 1.03 GB/s     (1.0k)
Write      | 1.03 GB/s     (2.0k) | 1.09 GB/s     (1.0k)
Total      | 2.00 GB/s     (3.9k) | 2.13 GB/s     (2.0k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA15S37)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA16S31)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：德国
[IPv6]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：德国
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
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: DE)
 Amazon Prime Video:			Yes (Region: DE)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			DE
 Viu.com:				No
 YouTube CDN:				Frankfurt 
 Netflix Preferred CDN:			Frankfurt  
 Spotify Registration:			No
 Steam Currency:			EUR
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				No
 Disney+:				Yes (Region: DE)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: DE)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Frankfurt 
 Netflix Preferred CDN:			Frankfurt  
 Spotify Registration:			No
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【DE】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：39
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
ip234数据库：
  欺诈分数(越低越好)：5
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：NO
------以下为IPV6检测------
scamalytics数据库:
  欺诈分数(越低越好)：39
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
2023/06/02 18:51:43 北京电信 219.141.136.12  测试超时
2023/06/02 18:51:43 北京联通 202.106.50.1    联通4837[普通线路]           
2023/06/02 18:51:43 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/06/02 18:51:43 上海电信 202.96.209.133  电信163 [普通线路]           
2023/06/02 18:51:43 上海联通 210.22.97.1     联通4837[普通线路]           
2023/06/02 18:51:43 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/06/02 18:51:43 广州电信 58.60.188.222   电信163 [普通线路]           
2023/06/02 18:51:43 广州联通 210.21.196.6    联通4837[普通线路]           
2023/06/02 18:51:43 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/06/02 18:51:43 成都电信 61.139.2.69     电信163 [普通线路]           
2023/06/02 18:51:43 成都联通 119.6.6.6       联通4837[普通线路]           
2023/06/02 18:51:43 成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
IPv4 ASN: AS24940 Hetzner Online
IPv6 ASN: AS24940 Hetzner Online
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.59 ms  *  局域网
1.14 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
0.67 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
3.19 ms  AS24940  德国, 巴伐利亚州, 纽伦堡, hetzner.com
3.48 ms  AS1299  德国, 巴伐利亚州, 纽伦堡, telia.com
6.36 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
6.36 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
8.83 ms  AS4134  德国, 黑森州, 法兰克福, chinatelecom.com.cn, 电信
335.67 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.31 ms  *  局域网
1.75 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
0.88 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
3.12 ms  AS24940  德国, 巴伐利亚州, 纽伦堡, hetzner.com
3.36 ms  AS1299  德国, 巴伐利亚州, 纽伦堡, telia.com
6.40 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
6.36 ms  AS1299  德国, 黑森州, 法兰克福, telia.com
189.30 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
177.19 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
196.31 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
177.93 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
0.29 ms  *  局域网
0.60 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
0.60 ms  AS24940  德国, 萨克森自由州, 法尔肯施泰因, hetzner.com
5.21 ms  AS24940  德国, 黑森州, 法兰克福, hetzner.com
6.66 ms  *  德国, 黑森州, 法兰克福, de-cix.net
6.73 ms  AS58453  德国, 黑森州, 法兰克福, chinamobile.com, 移动
242.62 ms  AS58453  中国, 上海, chinamobile.com, 移动
231.60 ms  AS9808  中国, 上海, chinamobile.com, 移动
243.42 ms  AS9808  中国, 上海, chinamobile.com, 移动
201.36 ms  AS9808  中国, 北京, chinamobile.com, 移动
201.15 ms  AS9808  中国, 北京, chinamobile.com, 移动
203.08 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 320.65 Mbps	 485.57 Mbps	 5.60	  0.0%
洛杉矶		 580.63 Mbps	 630.11 Mbps	 156.04	  0.0%
中国香港	 309.54 Mbps	 592.64 Mbps	 205.00	  0.0%
联通郑州5G	 903.50 Mbps	 705.98 Mbps	 172.37	  NULL
联通湖南5G	 481.38 Mbps	 291.17 Mbps	 184.63	  NULL
电信上海	 319.68 Mbps	 37.69 Mbps	 227.12	  NULL
电信重庆	 0.86 Mbps	 0.57 Mbps	 269.04	  3.7%
移动Chengdu	 13.96 Mbps	 1048.28 Mbps	 173.15	  0.3%
移动Lanzhou	 15.47 Mbps	 484.30 Mbps	 215.52	  NULL
------------------------------------------------------------------------
 总共花费      : 6 分 55 秒
 时间          : Fri Jun  2 18:57:13 CST 2023
------------------------------------------------------------------------
```

## 挂载hdd

```
mkdir  /mnt/hdd

mount /dev/vdb1 /mnt/hdd

echo "/dev/vdb1 /mnt/hdd ext4 defaults 0 0" >> /etc/fstab
```

## 一周观察

pt刷流非常强劲

![](https://catcat.blog/wp-content/uploads/2023/06/image-3.png)

![](https://catcat.blog/wp-content/uploads/2023/06/image-4-1024x254.png)

![](https://catcat.blog/wp-content/uploads/2023/06/image-5-905x1024.png)
