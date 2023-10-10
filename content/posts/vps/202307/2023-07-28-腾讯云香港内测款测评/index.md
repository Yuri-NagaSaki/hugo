---
title: "腾讯云香港内测款测评"
date: "2023-07-28"
categories: 
  - "vps"
  - "hk"
---

## 套餐

- CPU - 2核 内存 - 2GB

- 系统盘 - SSD云硬盘 40GB管理快照

- 流量包 - 512GB/月（峰值带宽：20Mbps）

## 服务器测试

### 融合怪脚本

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : Intel(R) Xeon(R) CPU E5-26xx v4
 CPU 核心数        : 2
 CPU 频率          : 2399.988 MHz
 CPU 缓存          : L1: 128.00 KB / L2: 8.00 MB / L3: 0.00 KB
 硬盘空间          : 1.97 GiB / 39.26 GiB
 启动盘路径        : /dev/vda1
 内存              : 188.46 MiB / 1.94 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 3 min
 负载              : 0.28, 0.11, 0.04
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-19-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 独立映射,独立过滤,支持回环
 IPV4 ASN          : AS132203 Tencent Building, Kejizhongyi Avenue
 IPV4 位置         : Hong Kong / Central and Western / HK
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           929 Scores
 2 线程测试(多核)得分:          1832 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          18532.02 MB/s
 单线程写测试:          13506.30 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         7.8 MB/s (1897 IOPS, 13.49s)            9.6 MB/s (2351 IOPS, 10.89s)
 1GB-1M Block           184 MB/s (176 IOPS, 5.69s)              277 MB/s (264 IOPS, 3.79s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 58.80 MB/s   (14.7k) | 197.08 MB/s   (3.0k)
Write      | 58.90 MB/s   (14.7k) | 198.12 MB/s   (3.0k)
Total      | 117.70 MB/s  (29.4k) | 395.20 MB/s   (6.1k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 267.70 MB/s    (522) | 259.00 MB/s    (252)
Write      | 281.93 MB/s    (550) | 276.25 MB/s    (269)
Total      | 549.64 MB/s   (1.0k) | 535.26 MB/s    (521)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 中国香港(HKG07S42)
Youtube识别地域: 香港(HK)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：香港
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：香港区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: HK)
 Netflix:                               Originals Only
 YouTube Premium:                       Failed
 Amazon Prime Video:                    Yes (Region: HK)
 TVBAnywhere+:                          No
 iQyi Oversea Region:                   HK
 Viu.com:                               Yes (Region: HK)
 YouTube CDN:                           Hong Kong 
 Netflix Preferred CDN:                 Hong Kong  
 Spotify Registration:                  No
 Steam Currency:                        HKD
 ChatGPT:                               No
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         Failed
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：57
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
  欺诈分数(越低越好)：40
ip-api数据库:
  手机流量: No
  代理服务: No
  数据中心: Yes
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  qq邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
2023/07/28 17:21:55 北京电信 219.141.136.12  移动CMI [普通线路]           
2023/07/28 17:21:55 北京联通 202.106.50.1    移动CMI [普通线路]           
2023/07/28 17:21:55 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/07/28 17:21:55 上海电信 202.96.209.133  测试超时
2023/07/28 17:21:55 上海联通 210.22.97.1     移动CMI [普通线路]           
2023/07/28 17:21:55 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/07/28 17:21:55 广州电信 58.60.188.222   测试超时
2023/07/28 17:21:55 广州联通 210.21.196.6    移动CMI [普通线路]           
2023/07/28 17:21:55 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/07/28 17:21:55 成都电信 61.139.2.69     移动CMI [普通线路]           
2023/07/28 17:21:55 成都联通 119.6.6.6       移动CMI [普通线路]           
2023/07/28 17:21:55 成都移动 211.137.96.205  测试超时
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
2.91 ms  *  局域网
36.49 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
1.23 ms  AS749  美国, defense.gov
1.38 ms  *  局域网
7.35 ms  *  局域网
1.87 ms  AS749  美国, defense.gov
1.40 ms  AS749  美国, defense.gov
19.64 ms  AS58453  中国, 香港, chinamobile.com, 移动
3.66 ms  AS58453  中国, 香港, chinamobile.com, 移动
31.55 ms  AS9808  中国, 上海, chinamobile.com, 移动
32.73 ms  AS9808  中国, 上海, chinamobile.com, 移动
38.99 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
42.49 ms  AS17816  中国, 广东, 广州, chinaunicom.com, 联通
39.64 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
36.06 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.24
4.32 ms  *  局域网
1.81 ms  AS749  美国, defense.gov
1.45 ms  AS749  美国, defense.gov
2.61 ms  AS58453  中国, 香港, chinamobile.com, 移动
3.41 ms  AS58453  中国, 香港, chinamobile.com, 移动
30.63 ms  AS9808  中国, 上海, chinamobile.com, 移动
30.48 ms  AS9808  中国, 上海, chinamobile.com, 移动
31.49 ms  AS9808  中国, 上海, chinamobile.com, 移动
53.88 ms  AS9808  中国, 北京, chinamobile.com, 移动
55.61 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    19.44 Mbps      119.94 Mbps     3.20     NULL
```

### 回程多地区测试脚本

```
----------------------------------------------------------------------
北京电信
traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  11.84.200.193  1.14 ms  AS749  美国, defense.gov
 2  11.84.247.64  1.02 ms  AS749  美国, defense.gov
 3  *
 4  10.196.94.149  1.72 ms  *  局域网
 5  11.48.233.60  1.79 ms  AS749  美国, defense.gov
 6  11.48.233.60  1.31 ms  AS749  美国, defense.gov
 7  223.119.80.113  5.12 ms  AS58453  中国, 香港, chinamobile.com, 移动
 8  223.120.22.69  3.23 ms  AS58453  中国, 香港, chinamobile.com, 移动
 9  *
10  221.183.89.170  486.43 ms  AS9808  中国, 上海, chinamobile.com, 移动
11  *
12  221.183.89.10  61.20 ms  AS9808  中国, 上海, chinamobile.com, 移动
13  *
14  221.183.94.22  55.13 ms  AS9808  中国, 北京, chinamobile.com, 移动
15  221.183.95.170  48.25 ms  AS9808  中国, 北京, chinamobile.com, 移动
16  202.97.17.89  48.09 ms  AS4134  中国, 北京, chinatelecom.com.cn, 电信
17  bj141-152-74.bjtelecom.net (219.141.152.74)  49.02 ms  AS4847  中国, 北京, chinatelecom.com.cn, 电信
18  *
19  6.254.120.106.static.bjtelecom.net (106.120.254.6)  60.06 ms  AS4847  中国, 北京, chinatelecom.com.cn, 电信
20  bj141-147-210.bjtelecom.net (219.141.147.210)  49.24 ms  AS4847  中国, 北京, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
上海电信
traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  *
 2  *
 3  10.162.74.157  1.46 ms  *  局域网
 4  10.196.94.149  1.59 ms  *  局域网
 5  11.48.233.63  1.89 ms  AS749  美国, defense.gov
 6  11.48.233.63  1.37 ms  AS749  美国, defense.gov
 7  223.119.80.113  1361.84 ms  AS58453  中国, 香港, chinamobile.com, 移动
 8  223.120.22.69  1115.20 ms  AS58453  中国, 香港, chinamobile.com, 移动
 9  223.120.3.182  2180.43 ms  AS58453  中国, 上海, chinamobile.com, 移动
10  *
11  *
12  *
13  *
14  *
15  *
16  *
17  *
18  *
19  *
20  *
21  *
22  *
23  *
24  *
25  *
26  *
27  *
28  *
29  *
30  *

----------------------------------------------------------------------
深圳电信
traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  *
 2  *
 3  *
 4  10.200.59.157  1.84 ms  *  局域网
 5  58.60.188.222  36.44 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
北京联通
traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  *
 2  *
 3  10.162.74.137  1.37 ms  *  局域网
 4  10.196.94.153  1.66 ms  *  局域网
 5  11.48.233.51  1.84 ms  AS749  美国, defense.gov
 6  11.48.233.53  1.40 ms  AS749  美国, defense.gov
 7  223.119.80.113  2.53 ms  AS58453  中国, 香港, chinamobile.com, 移动
 8  223.120.22.69  2.74 ms  AS58453  中国, 香港, chinamobile.com, 移动
 9  *
10  221.183.89.170  29.98 ms  AS9808  中国, 上海, chinamobile.com, 移动
11  221.183.89.33  30.17 ms  AS9808  中国, 上海, chinamobile.com, 移动
12  *
13  *
14  *
15  221.183.95.54  52.08 ms  AS9808  中国, 北京, chinamobile.com, 移动
16  219.158.120.117  47.38 ms  AS4837  中国, 北京, chinaunicom.com, 联通
17  *
18  202.106.50.1  47.48 ms  AS4808  中国, 北京, chinaunicom.com, 联通

----------------------------------------------------------------------
上海联通
traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  *
 2  11.84.247.70  0.97 ms  AS749  美国, defense.gov
 3  *
 4  10.196.94.149  1.24 ms  *  局域网
 5  11.50.201.51  2.01 ms  AS749  美国, defense.gov
 6  11.50.201.53  0.91 ms  AS749  美国, defense.gov
 7  223.119.21.209  8.76 ms  AS58453  中国, 香港, chinamobile.com, 移动
 8  *
 9  *
10  221.183.89.170  37.01 ms  AS9808  中国, 上海, chinamobile.com, 移动
11  221.183.89.33  30.88 ms  AS9808  中国, 上海, chinamobile.com, 移动
12  *
13  *
14  221.183.123.110  38.22 ms  AS9808  中国, 上海, chinamobile.com, 移动
15  *
16  *
17  112.64.250.202  32.41 ms  AS17621  中国, 上海, chinaunicom.com, 联通
18  210.22.97.1  38.34 ms  AS17621  中国, 上海, chinaunicom.com, 联通

----------------------------------------------------------------------
深圳联通
traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  *
 2  *
 3  *
 4  10.196.94.157  1.32 ms  *  局域网
 5  11.50.201.54  1.78 ms  AS749  美国, defense.gov
 6  11.50.201.54  1.38 ms  AS749  美国, defense.gov
 7  223.119.21.209  3.42 ms  AS58453  中国, 香港, chinamobile.com, 移动
 8  223.120.2.53  3.77 ms  AS58453  中国, 香港, chinamobile.com, 移动
 9  *
10  221.183.89.170  31.08 ms  AS9808  中国, 上海, chinamobile.com, 移动
11  221.183.89.33  31.49 ms  AS9808  中国, 上海, chinamobile.com, 移动
12  *
13  *
14  221.183.94.174  34.68 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
15  221.183.123.2  42.87 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
16  *
17  157.148.0.58  40.36 ms  AS17816  中国, 广东, 广州, chinaunicom.com, 联通
18  120.80.144.34  40.45 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
19  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  36.07 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通

----------------------------------------------------------------------
北京移动
traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  *
 2  11.84.247.70  0.99 ms  AS749  美国, defense.gov
 3  *
 4  10.196.94.149  1.13 ms  *  局域网
 5  11.50.201.50  1.51 ms  AS749  美国, defense.gov
 6  11.50.201.50  0.90 ms  AS749  美国, defense.gov
 7  223.119.21.209  1079.84 ms  AS58453  中国, 香港, chinamobile.com, 移动
 8  223.120.2.53  878.66 ms  AS58453  中国, 香港, chinamobile.com, 移动
 9  223.120.2.42  757.68 ms  AS58453  中国, 香港, chinamobile.com, 移动
10  223.120.22.142  561.18 ms  AS58453  中国, 北京, chinamobile.com, 移动
11  221.183.55.106  399.92 ms  AS9808  中国, 北京, chinamobile.com, 移动
12  221.183.46.250  174.75 ms  AS9808  中国, 北京, chinamobile.com, 移动
13  221.183.89.102  62.12 ms  AS9808  中国, 北京, chinamobile.com, 移动
14  221.183.46.178  47.17 ms  AS9808  中国, 北京, chinamobile.com, 移动
15  *
16  cachedns03.bj.chinamobile.com (221.179.155.161)  635.20 ms  AS56048  中国, 北京, chinamobile.com, 移动

----------------------------------------------------------------------
上海移动
traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  *
 2  *
 3  *
 4  10.196.94.149  1.12 ms  *  局域网
 5  11.50.201.50  1.38 ms  AS749  美国, defense.gov
 6  11.50.201.54  1.42 ms  AS749  美国, defense.gov
 7  223.119.21.209  6.52 ms  AS58453  中国, 香港, chinamobile.com, 移动
 8  223.120.2.53  4.49 ms  AS58453  中国, 香港, chinamobile.com, 移动
 9  223.120.3.186  30.22 ms  AS58453  中国, 上海, chinamobile.com, 移动
10  *
11  221.183.89.69  32.43 ms  AS9808  中国, 上海, chinamobile.com, 移动
12  *
13  *
14  221.181.125.178  33.20 ms  AS24400  中国, 上海, chinamobile.com, 移动
15  211.136.112.252  33.48 ms  AS24400  中国, 上海, chinamobile.com, 移动
16  211.136.112.200  37.89 ms  AS24400  中国, 上海, chinamobile.com, 移动

----------------------------------------------------------------------
深圳移动
traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  *
 2  *
 3  *
 4  10.196.94.145  2.07 ms  *  局域网
 5  11.48.233.51  1.91 ms  AS749  美国, defense.gov
 6  11.48.233.53  1.50 ms  AS749  美国, defense.gov
 7  223.119.80.113  2.67 ms  AS58453  中国, 香港, chinamobile.com, 移动
 8  223.120.22.69  3.24 ms  AS58453  中国, 香港, chinamobile.com, 移动
 9  *
10  221.183.89.174  30.54 ms  AS9808  中国, 上海, chinamobile.com, 移动
11  221.183.89.69  30.48 ms  AS9808  中国, 上海, chinamobile.com, 移动
12  221.183.89.50  31.55 ms  AS9808  中国, 上海, chinamobile.com, 移动
13  *
14  221.183.46.178  53.82 ms  AS9808  中国, 北京, chinamobile.com, 移动
15  *
16  ns6.gd.cnmobile.net (120.196.165.24)  55.52 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动

----------------------------------------------------------------------
成都教育网
traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  11.84.200.225  1.12 ms  AS749  美国, defense.gov
 2  *
 3  *
 4  10.196.94.133  1.57 ms  *  局域网
 5  10.196.95.182  1.82 ms  *  局域网
 6  10.200.59.194  2.26 ms  *  局域网
 7  10.196.95.206  1.22 ms  *  局域网
 8  cernetedu1-100g.hkix.net (123.255.91.118)  2.42 ms  AS3491  中国, 香港, hkix.net
 9  101.4.114.181  37.33 ms  AS4538  中国, 北京, edu.cn, 教育网
10  *
11  101.4.117.81  38.33 ms  AS4538  中国, 北京, edu.cn, 教育网
12  101.4.112.14  62.47 ms  AS4538  中国, 陕西, 西安, edu.cn, 教育网
13  101.4.112.18  58.06 ms  AS4538  中国, 四川, 成都, edu.cn, 教育网
14  *
15  *
16  *
17  *
18  *
19  202.112.14.151  54.20 ms  AS24355  中国, 四川, 成都, 电子科技大学CERNET西南地区网络中心, edu.cn, 教育网

----------------------------------------------------------------------
```
