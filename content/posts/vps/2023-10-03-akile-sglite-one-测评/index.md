---
title: "Akile SGLite-One 测评"
date: "2023-10-03"
categories: 
  - "vps"
  - "sg"
  - "special"
---

## 套餐配置

![](https://catcat.blog/wp-content/uploads/2023/10/image-2.png)

## 测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7402P 24-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 2794.746 MHz
 CPU 缓存          : L1: 64.00 KB / L2: 512.00 KB / L3: 16.00 MB
 硬盘空间          : 2.16 GiB / 4.88 GiB
 启动盘路径        : /dev/sda1
 内存              : 132.74 MiB / 957.89 MiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 7 min
 负载              : 0.76, 0.34, 0.18
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.4.11-x64v3-xanmod1
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 无法检测
 IPV4 ASN          : AS61112 AKILE LTD
 IPV4 位置         : Singapore / Singapore / SG
 IPV6 ASN          : AS61112 AKILE LTD
 IPV6 位置         : Singapore / SG-01
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		1180 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		30160.38 MB/s
 单线程写测试:		15904.45 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		47.9 MB/s (11.69 IOPS, 2.19s)		58.4 MB/s (14258 IOPS, 1.80s)
 1GB-1M Block		106 MB/s (101 IOPS, 9.90s)		106 MB/s (100 IOPS, 9.90s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 102.61 MB/s  (25.6k) | 102.37 MB/s   (1.5k)
Write      | 102.88 MB/s  (25.7k) | 102.91 MB/s   (1.6k)
Total      | 205.49 MB/s  (51.3k) | 205.29 MB/s   (3.2k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 97.68 MB/s     (190) | 96.49 MB/s      (94)
Write      | 102.87 MB/s    (200) | 102.92 MB/s    (100)
Total      | 200.55 MB/s    (390) | 199.42 MB/s    (194)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 新加坡 新加坡/樟宜  (SIN10S14)
Youtube识别地域: 新加坡(SG)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 新加坡 新加坡/樟宜  (SIN10S14)
Youtube识别地域: 新加坡(SG)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：新加坡
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：新加坡区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：新加坡区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					Yes (Region: SG)
 HotStar:				Yes (Region: SG)
 Disney+:				Yes (Region: SG)
 Netflix:				Yes (Region: SG)
 YouTube Premium:			Yes (Region: SG)
 Amazon Prime Video:			Yes (Region: SG)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			US
 Viu.com:				Yes (Region: SG)
 YouTube CDN:				Singapore 
 Netflix Preferred CDN:			Associated with [Nearoute Limited] in [Singapore ]
 Spotify Registration:			No
 Steam Currency:			SGD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				Failed (Network Connection)
 Disney+:				No
 Netflix:				Failed (Network Connection)
 YouTube Premium:			Failed (Network Connection)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube Region:			Check Failed (Network Connection)
 Netflix Preferred CDN:			Failed
 Spotify Registration:			Yes (Region: SG)
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【ES】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  isp⑧  business⑨  
  公司类型(company_type):hosting①  isp⑧  
  云服务提供商(cloud_provider):  No⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ② ⑥ ⑦ ⑧ ⑨ 
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
Google搜索可行性：NO
------以下为IPV6检测------
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: SG 城市: Singapore 服务商: AS61112 AKILE LTD
北京电信 219.141.136.12  测试超时
北京联通 202.106.50.1    联通4837[普通线路]           
北京移动 221.179.155.161 测试超时
上海电信 202.96.209.133  电信163 [普通线路]           
上海联通 210.22.97.1     联通4837[普通线路]           
上海移动 211.136.112.200 移动CMI [普通线路]           
广州电信 58.60.188.222   电信163 [普通线路]           
广州联通 210.21.196.6    联通4837[普通线路]           
广州移动 120.196.165.24  移动CMI [普通线路]           
成都电信 61.139.2.69     电信163 [普通线路]           
成都联通 119.6.6.6       联通4837[普通线路]           
成都移动 211.137.96.205  移动CMI [普通线路]           
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
4.60 ms 	AS61112 新加坡 akile.io
0.43 ms 	AS51847 [NEAROUTE3-HK] 新加坡 nearoute.io
1.48 ms 	AS174 [COGENT-BONE] 新加坡 cogentco.com
166.07 ms 	AS174 [COGENT-BONE] 法国 普罗旺斯-阿尔卑斯-蓝色海岸大区 马赛 cogentco.com
165.31 ms 	AS174 [COGENT-BONE] 法国 法兰西岛大区 巴黎 cogentco.com
165.29 ms 	AS174 [COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
166.14 ms 	AS174 [COGENT-BONE] 德国 黑森州 美因河畔法兰克福 cogentco.com
307.24 ms 	AS174 [COGENT-149] 德国 黑森州 美因河畔法兰克福 Cogent-CT-Peer cogentco.com
395.50 ms 	AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
* ms 	AS134774 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.cn 电信
508.06 ms 	AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
7.07 ms 	AS61112 新加坡 akile.io
0.53 ms 	AS51847 [NEAROUTE3-HK] 新加坡 nearoute.io
0.96 ms 	AS174 [COGENT-BONE] 新加坡 cogentco.com
174.72 ms 	AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
177.98 ms 	AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
178.01 ms 	AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
179.99 ms 	AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
185.44 ms 	AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
184.05 ms 	AS17816 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
183.05 ms 	AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
183.75 ms 	AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
24.18 ms 	AS61112 新加坡 akile.io
0.63 ms 	AS51847 [NEAROUTE3-HK] 新加坡 nearoute.io
0.98 ms 	AS174 [COGENT-BONE] 新加坡 cogentco.com
170.96 ms 	AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
166.42 ms 	AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
212.45 ms 	AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
238.05 ms 	AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
342.14 ms 	AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
212.59 ms 	AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
389.27 ms 	AS58453 [CMI-INT] 中国 广东省 广州市 cmi.chinamobile.com 移动
388.16 ms 	AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
388.44 ms 	AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
398.35 ms 	AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
395.11 ms 	AS9808 [CMNET] 中国 海南省 海口市 chinamobile.com 移动
350.15 ms 	AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 466.83 Mbps	 503.54 Mbps	 0.35	  0.0%
新加坡		 522.86 Mbps	 501.15 Mbps	 0.37	  0.0%
中国香港	 508.96 Mbps	 2.51 Mbps	 31.02	  NULL
联通Fuzhou	 202.75 Mbps	 501.25 Mbps	 49.87	  0.4%
联通湖南5G	 457.38 Mbps	 14.98 Mbps	 60.69	  NULL
电信Zhenjiang5G	 1.12 Mbps	 471.31 Mbps	 400.33	  NULL
------------------------------------------------------------------------
 总共花费      : 6 分 35 秒
 时间          : Tue Oct  3 06:05:13 EDT 2023
------------------------------------------------------------------------
```

### 回程测试

```
----------------------------------------------------------------------
北京电信
traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  5.253.36.1  108.17 ms  AS61112  Singapore, lvnet.lv
 2  103.181.12.128  6.30 ms  *  China, Hong Kong, nearoute.io
 3  te0-3-0-6-9.ccr31.sin01.atlas.cogentco.com (154.18.19.249)  0.94 ms  AS174  Singapore, cogentco.com
 4  be2914.ccr31.mrs02.atlas.cogentco.com (154.54.87.210)  155.56 ms  AS174  France, Provence-Alpes-Cote d'Azur, Marseille, cogentco.com
 5  be2779.ccr41.par01.atlas.cogentco.com (154.54.72.109)  155.85 ms  AS174  France, Ile-de-France, Paris, cogentco.com
 6  be2799.ccr41.fra03.atlas.cogentco.com (154.54.58.233)  156.04 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 7  be3186.agr41.fra03.atlas.cogentco.com (130.117.0.2)  155.91 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 8  chinatelecom.demarc.cogentco.com (149.14.159.114)  295.89 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 9  *
10  *
11  *
12  *
13  *
14  2.254.120.106.static.bjtelecom.net (106.120.254.2)  373.94 ms  AS4847  China, Beijing, ChinaTelecom
15  bj141-147-210.bjtelecom.net (219.141.147.210)  368.75 ms  AS4847  China, Beijing, ChinaTelecom

----------------------------------------------------------------------
上海电信
traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  5.253.36.1  7.81 ms  AS61112  Singapore, lvnet.lv
 2  103.181.12.128  0.45 ms  *  China, Hong Kong, nearoute.io
 3  te0-3-0-6-9.ccr31.sin01.atlas.cogentco.com (154.18.19.249)  0.89 ms  AS174  Singapore, cogentco.com
 4  be2914.ccr31.mrs02.atlas.cogentco.com (154.54.87.210)  155.90 ms  AS174  France, Provence-Alpes-Cote d'Azur, Marseille, cogentco.com
 5  be2779.ccr41.par01.atlas.cogentco.com (154.54.72.109)  156.01 ms  AS174  France, Ile-de-France, Paris, cogentco.com
 6  be2799.ccr41.fra03.atlas.cogentco.com (154.54.58.233)  155.87 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 7  be3186.agr41.fra03.atlas.cogentco.com (130.117.0.2)  155.80 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 8  chinatelecom.demarc.cogentco.com (149.14.159.114)  296.67 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 9  *
10  202.97.90.30  367.39 ms  AS4134  China, Shanghai, ChinaTelecom
11  *
12  *
13  *
14  ns-pd.online.sh.cn (202.96.209.133)  367.62 ms  AS4812  China, Shanghai, ChinaTelecom

----------------------------------------------------------------------
深圳电信
traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  5.253.36.1  8.66 ms  AS61112  Singapore, lvnet.lv
 2  103.181.12.128  0.37 ms  *  China, Hong Kong, nearoute.io
 3  te0-3-0-6-9.ccr31.sin01.atlas.cogentco.com (154.18.19.249)  0.67 ms  AS174  Singapore, cogentco.com
 4  be2914.ccr31.mrs02.atlas.cogentco.com (154.54.87.210)  164.49 ms  AS174  France, Provence-Alpes-Cote d'Azur, Marseille, cogentco.com
 5  be2779.ccr41.par01.atlas.cogentco.com (154.54.72.109)  164.83 ms  AS174  France, Ile-de-France, Paris, cogentco.com
 6  be2799.ccr41.fra03.atlas.cogentco.com (154.54.58.233)  164.81 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 7  be3186.agr41.fra03.atlas.cogentco.com (130.117.0.2)  164.76 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 8  chinatelecom.demarc.cogentco.com (149.14.159.114)  305.81 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 9  *
10  *
11  202.97.82.21  411.96 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
12  14.147.127.30  422.58 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
13  *
14  *
15  58.60.188.222  357.08 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom

----------------------------------------------------------------------
北京联通
traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  5.253.36.1  4.88 ms  AS61112  Singapore, lvnet.lv
 2  103.181.12.128  0.36 ms  *  China, Hong Kong, nearoute.io
 3  te0-3-0-6-9.ccr31.sin01.atlas.cogentco.com (154.18.19.249)  0.87 ms  AS174  Singapore, cogentco.com
 4  be2913.ccr41.lax04.atlas.cogentco.com (154.54.27.54)  170.90 ms  AS174  United States, California, Los Angeles, cogentco.com
 5  be3360.ccr42.lax01.atlas.cogentco.com (154.54.25.149)  166.37 ms  AS174  United States, California, Los Angeles, cogentco.com
 6  be3177.ccr22.sjc01.atlas.cogentco.com (154.54.40.146)  186.02 ms  AS174  United States, California, San Jose, cogentco.com
 7  be3144.ccr41.sjc03.atlas.cogentco.com (154.54.5.102)  186.36 ms  AS174  United States, California, San Jose, cogentco.com
 8  38.88.225.106  439.43 ms  AS174  United States, California, San Jose, cogentco.com
 9  219.158.96.41  467.64 ms  AS4837  China, Beijing, ChinaUnicom
10  219.158.3.133  462.48 ms  AS4837  China, Beijing, ChinaUnicom
11  *
12  *
13  202.106.50.1  451.21 ms  AS4808  China, Beijing, ChinaUnicom

----------------------------------------------------------------------
上海联通
traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  5.253.36.1  5.12 ms  AS61112  Singapore, lvnet.lv
 2  103.181.12.128  10.82 ms  *  China, Hong Kong, nearoute.io
 3  te0-3-0-6-9.ccr31.sin01.atlas.cogentco.com (154.18.19.249)  0.81 ms  AS174  Singapore, cogentco.com
 4  be2913.ccr41.lax04.atlas.cogentco.com (154.54.27.54)  170.89 ms  AS174  United States, California, Los Angeles, cogentco.com
 5  be3360.ccr42.lax01.atlas.cogentco.com (154.54.25.149)  166.43 ms  AS174  United States, California, Los Angeles, cogentco.com
 6  be3177.ccr22.sjc01.atlas.cogentco.com (154.54.40.146)  186.07 ms  AS174  United States, California, San Jose, cogentco.com
 7  be3144.ccr41.sjc03.atlas.cogentco.com (154.54.5.102)  186.30 ms  AS174  United States, California, San Jose, cogentco.com
 8  38.142.245.2  420.28 ms  AS174  United States, California, San Jose, cogentco.com
 9  219.158.97.181  423.55 ms  AS4837  China, Shanghai, ChinaUnicom
10  219.158.19.78  432.08 ms  AS4837  China, Shanghai, ChinaUnicom
11  *
12  *
13  112.64.250.202  439.38 ms  AS17621  China, Shanghai, ChinaUnicom
14  210.22.97.1  422.64 ms  AS17621  China, Shanghai, ChinaUnicom

----------------------------------------------------------------------
深圳联通
traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  5.253.36.1  1.14 ms  AS61112  Singapore, lvnet.lv
 2  103.181.12.128  0.33 ms  *  China, Hong Kong, nearoute.io
 3  te0-3-0-6-9.ccr31.sin01.atlas.cogentco.com (154.18.19.249)  0.93 ms  AS174  Singapore, cogentco.com
 4  be2913.ccr41.lax04.atlas.cogentco.com (154.54.27.54)  174.45 ms  AS174  United States, California, Los Angeles, cogentco.com
 5  be3252.rcr62.lax04.atlas.cogentco.com (154.54.91.22)  177.88 ms  AS174  United States, California, Los Angeles, cogentco.com
 6  38.142.32.34  421.19 ms  AS174  United States, California, Los Angeles, cogentco.com
 7  219.158.102.89  469.10 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
 8  219.158.103.33  480.99 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
 9  *
10  *
11  120.80.144.34  481.15 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
12  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  472.04 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom

----------------------------------------------------------------------
北京移动
traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  5.253.36.1  5.25 ms  AS61112  Singapore, lvnet.lv
 2  103.181.12.128  6.05 ms  *  China, Hong Kong, nearoute.io
 3  te0-3-0-6-9.ccr31.sin01.atlas.cogentco.com (154.18.19.249)  0.85 ms  AS174  Singapore, cogentco.com
 4  be2913.ccr41.lax04.atlas.cogentco.com (154.54.27.54)  177.38 ms  AS174  United States, California, Los Angeles, cogentco.com
 5  be3271.ccr41.lax01.atlas.cogentco.com (154.54.42.101)  168.99 ms  AS174  United States, California, Los Angeles, cogentco.com
 6  be3243.ccr41.lax05.atlas.cogentco.com (154.54.27.118)  177.96 ms  AS174  United States, California, Los Angeles, cogentco.com
 7  38.104.85.162  528.54 ms  AS174  United States, California, Los Angeles, cogentco.com
 8  *
 9  223.120.12.214  775.66 ms  AS58453  China, Shanghai, ChinaMobile
10  221.183.55.106  769.33 ms  AS9808  China, Beijing, ChinaMobile
11  221.183.46.250  767.55 ms  AS9808  China, Beijing, ChinaMobile
12  221.183.89.102  775.57 ms  AS9808  China, Beijing, ChinaMobile
13  221.183.46.178  763.20 ms  AS9808  China, Beijing, ChinaMobile
14  *
15  cachedns03.bj.chinamobile.com (221.179.155.161)  766.28 ms  AS56048  China, Beijing, ChinaMobile

----------------------------------------------------------------------
上海移动
traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  5.253.36.1  1.54 ms  AS61112  Singapore, lvnet.lv
 2  103.181.12.128  3.87 ms  *  China, Hong Kong, nearoute.io
 3  te0-3-0-6-9.ccr31.sin01.atlas.cogentco.com (154.18.19.249)  0.92 ms  AS174  Singapore, cogentco.com
 4  be2742.ccr41.fra03.atlas.cogentco.com (66.28.4.41)  158.36 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 5  be3374.rcr21.b019066-1.fra03.atlas.cogentco.com (154.54.37.249)  158.43 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 6  chinamobile.demarc.cogentco.com (149.29.9.162)  161.98 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 7  223.120.10.85  159.03 ms  AS58453  Germany, Hesse, Frankfurt, ChinaMobile
 8  *
 9  221.183.89.178  415.08 ms  AS9808  China, Shanghai, ChinaMobile
10  221.183.89.33  365.69 ms  AS9808  China, Shanghai, ChinaMobile
11  *
12  *
13  211.136.190.242  391.36 ms  AS24400  China, Shanghai, ChinaMobile
14  211.136.112.252  365.12 ms  AS24400  China, Shanghai, ChinaMobile
15  211.136.112.200  367.45 ms  AS24400  China, Shanghai, ChinaMobile

----------------------------------------------------------------------
深圳移动
traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  5.253.36.1  12.66 ms  AS61112  Singapore, lvnet.lv
 2  103.181.12.128  13.78 ms  *  China, Hong Kong, nearoute.io
 3  te0-3-0-6-9.ccr31.sin01.atlas.cogentco.com (154.18.19.249)  0.96 ms  AS174  Singapore, cogentco.com
 4  be2913.ccr41.lax04.atlas.cogentco.com (154.54.27.54)  170.96 ms  AS174  United States, California, Los Angeles, cogentco.com
 5  be3360.ccr42.lax01.atlas.cogentco.com (154.54.25.149)  166.24 ms  AS174  United States, California, Los Angeles, cogentco.com
 6  be3359.ccr41.lax05.atlas.cogentco.com (154.54.3.70)  212.55 ms  AS174  United States, California, Los Angeles, cogentco.com
 7  38.19.140.98  229.71 ms  AS174  United States, California, Los Angeles, cogentco.com
 8  223.118.10.85  231.77 ms  AS58453  United States, California, Los Angeles, ChinaMobile
 9  223.118.10.193  228.72 ms  AS58453  United States, California, Los Angeles, ChinaMobile
10  223.120.6.85  212.60 ms  AS58453  United States, California, Los Angeles, ChinaMobile
11  223.120.12.10  331.09 ms  AS58453  China, Guangdong, Guangzhou, ChinaMobile
12  221.183.55.82  328.85 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
13  221.183.92.21  376.64 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
14  *
15  221.183.71.82  383.89 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
16  221.183.110.170  383.56 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
17  ns6.gd.cnmobile.net (120.196.165.24)  338.26 ms  AS56040  China, Guangdong, Shenzhen, ChinaMobile

----------------------------------------------------------------------
成都教育网
traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  5.253.36.1  7.42 ms  AS61112  Singapore, lvnet.lv
 2  103.181.12.128  0.40 ms  *  China, Hong Kong, nearoute.io
 3  *
 4  *
 5  *
 6  *
 7  erx-cernet-bkb-as4538.e0-25.switch7.lax2.he.net (216.218.244.106)  167.39 ms  AS6939  United States, California, Los Angeles, he.net
 8  101.4.117.185  175.99 ms  AS4538  United States, California, Los Angeles, CHINAEDU
 9  101.4.117.213  322.64 ms  AS4538  China, Beijing, CHINAEDU
10  101.4.113.130  314.90 ms  AS4538  China, Beijing, CHINAEDU
11  101.4.114.193  319.06 ms  AS4538  China, Beijing, CHINAEDU
12  101.4.117.81  321.98 ms  AS4538  China, Beijing, CHINAEDU
13  101.4.116.106  345.10 ms  AS4538  China, Hubei, Wuhan, CHINAEDU
14  *
15  101.4.117.53  360.10 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
16  101.4.116.158  363.66 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
17  *
18  *
19  *
20  *
21  202.112.14.151  360.42 ms  AS24355  China, Sichuan, Chengdu, CHINAEDU

----------------------------------------------------------------------
```

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 1 days, 19 hours, 52 minutes
Processor  : AMD EPYC 7402P 24-Core Processor
CPU cores  : 1 @ 2794.746 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 957.9 MiB
Swap       : 0.0 KiB
Disk       : 4.9 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.4.11-x64v3-xanmod1
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Akile LTD
ASN        : AS61112 AKILE LTD
Host       : Akile
Location   : Singapore, North West (03)
Country    : Singapore

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 98.69 MB/s   (24.6k) | 102.40 MB/s   (1.6k)
Write      | 98.95 MB/s   (24.7k) | 102.94 MB/s   (1.6k)
Total      | 197.64 MB/s  (49.4k) | 205.35 MB/s   (3.2k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 97.72 MB/s     (190) | 96.48 MB/s      (94)
Write      | 102.91 MB/s    (201) | 102.91 MB/s    (100)
Total      | 200.64 MB/s    (391) | 199.39 MB/s    (194)

Geekbench test failed and low memory was detected. Add at least 1GB of SWAP or use GB4 instead (higher compatibility with low memory systems).

YABS completed in 2 min 1 sec
```
