---
title: "Google Cloud 台湾"
date: "2023-07-10"
categories: 
  - "vps"
  - "台湾"
---

## 流媒体测试

```
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: TW)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: TW)
 Amazon Prime Video:                    Yes (Region: TW)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   TW
 Viu.com:                               No
 YouTube CDN:                           Associated with [TSA01S15]
 Netflix Preferred CDN:                 Hong Kong  
 Spotify Registration:                  No
 Steam Currency:                        TWD
 ChatGPT:                               Yes
=======================================
==============[ Taiwan ]===============
 KKTV:                                  Yes
 LiTV:                                  Yes
 MyVideo:                               No
 4GTV.TV:                               Failed
 LineTV.TW:                             Yes
 Hami Video:                            Yes
 CatchPlay+:                            Yes
 HBO GO Asia:                           Yes (Region: TW)
 Bahamut Anime:                         Yes
 Bilibili Taiwan Only:                  Yes
=======================================
当前主机不支持IPv6,跳过...
```

## 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : Intel(R) Xeon(R) CPU @ 2.20GHz
 CPU 核心数        : 1
 CPU 频率          : 2199.998 MHz
 CPU 缓存          : 56320 KB
 硬盘空间          : 2.74 GiB / 9.62 GiB
 启动盘路径        : /dev/sda1
 内存              : 246.73 MiB / 571.88 MiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 20 min
 负载              : 0.09, 0.06, 0.02
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-cloud-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 独立映射,独立过滤,支持回环
 IPV4 ASN          : AS396982 Google LLC
 IPV4 位置         : Taipei / Taiwan / TW
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		940 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		19123.04 MB/s
 单线程写测试:		13372.23 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		10.1 MB/s (2462 IOPS, 10.40s)		14.1 MB/s (3439 IOPS, 7.44s)
 1GB-1M Block		37.7 MB/s (36 IOPS, 27.81s)		153 MB/s (145 IOPS, 6.86s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
  ------ | --- ---- | ---- ---- 
Read       | 6.45 MB/s     (1.6k) | 36.89 MB/s     (576)
Write      | 6.45 MB/s     (1.6k) | 37.19 MB/s     (581)
Total      | 12.90 MB/s    (3.2k) | 74.09 MB/s    (1.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 38.87 MB/s      (75) | 37.26 MB/s      (36)
Write      | 40.61 MB/s      (79) | 39.93 MB/s      (39)
Total      | 79.49 MB/s     (154) | 77.20 MB/s      (75)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: TSA(TSA01S15)
Youtube识别地域: 台湾(TW)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：台湾
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：台湾区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				Yes (Region: TW)
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: TW)
 Amazon Prime Video:			Yes (Region: TW)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			TW
 Viu.com:				No
 YouTube CDN:				Associated with [TSA01S15]
 Netflix Preferred CDN:			Hong Kong  
 Spotify Registration:			No
 Steam Currency:			TWD
 ChatGPT:				Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【TW】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：54
  匿名代理: No
  Tor出口节点: No
  服务器IP: Yes
  公共代理: No
  网络代理: No
  搜索引擎机器人: No
黑名单记录统计:(有多少黑名单网站有记录)
  无害记录： 0
  恶意记录： 0
  可疑记录： 0
  未检测到记录： 87
ip234数据库：
  欺诈分数(越低越好)：15
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
端口25检测:
  本地: Yes
  163邮箱：No
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/07/10 12:36:23 北京电信 219.141.136.12  电信163 [普通线路]           
2023/07/10 12:36:23 北京联通 202.106.50.1    联通4837[普通线路]           
2023/07/10 12:36:23 北京移动 221.179.155.161 测试超时
2023/07/10 12:36:23 上海电信 202.96.209.133  测试超时
2023/07/10 12:36:23 上海联通 210.22.97.1     联通4837[普通线路]           
2023/07/10 12:36:23 上海移动 211.136.112.200 测试超时
2023/07/10 12:36:23 广州电信 58.60.188.222   电信163 [普通线路]           
2023/07/10 12:36:23 广州联通 210.21.196.6    联通4837[普通线路]           
2023/07/10 12:36:23 广州移动 120.196.165.24  测试超时
2023/07/10 12:36:23 成都电信 61.139.2.69     电信163 [普通线路]           
2023/07/10 12:36:23 成都联通 119.6.6.6       联通4837[普通线路]           
2023/07/10 12:36:23 成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
16.40 ms  AS15169  中国, 香港, google.com
17.88 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
23.12 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
24.30 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
26.05 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
28.56 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
28.10 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
275.21 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 979.85 Mbps	 7501.93 Mbps	 3.69	  NULL
中国香港	 980.47 Mbps	 5853.00 Mbps	 14.51	  0.0%
日本东京	 951.94 Mbps	 6887.00 Mbps	 39.19	  0.0%
联通Fuzhou	 981.03 Mbps	 4495.35 Mbps	 37.83	  0.0%
联通WuXi	 891.89 Mbps	 2986.14 Mbps	 42.96	  0.0%
电信合肥5G	 270.56 Mbps	 372.36 Mbps	 88.90	  6.3%
电信天津	 232.59 Mbps	 3932.39 Mbps	 55.29	  NULL
移动杭州5G	 410.02 Mbps	 3942.40 Mbps	 187.47	  0.0%
移动Beijing	 430.30 Mbps	 2117.74 Mbps	 186.76	  NULL
------------------------------------------------------------------------
 总共花费      : 8 分 51 秒
 时间          : Mon Jul 10 12:40:48 UTC 2023
------------------------------------------------------------------------
```

## bench测试

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : Intel(R) Xeon(R) CPU @ 2.20GHz
 CPU Cores          : 1 @ 2199.998 MHz
 CPU Cache          : 56320 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Disabled
 Total Disk         : 9.7 GB (2.7 GB Used)
 Total Mem          : 571.9 MB (227.5 MB Used)
 System uptime      : 0 days, 0 hour 35 min
 Load average       : 0.04, 0.39, 0.46
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-23-cloud-amd64
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Offline
 Organization       : AS396982 Google LLC
 Location           : Taipei / TW
 Region             : Taiwan
----------------------------------------------------------------------
 I/O Speed(1st run) : 53.1 MB/s
 I/O Speed(2nd run) : 52.3 MB/s
 I/O Speed(3rd run) : 54.2 MB/s
 I/O Speed(average) : 53.2 MB/s
----------------------------------------------------------------------
```
