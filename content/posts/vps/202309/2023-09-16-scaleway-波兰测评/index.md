---
title: "Scaleway 波兰测评"
date: "2023-09-16"
categories: 
  - "vps"
  - "eu"
---

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD EPYC 7282 16-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 2799.998 MHz
 CPU 缓存          : L1: 64.00 KB / L2: 512.00 KB / L3: 16.00 MB
 硬盘空间          : 1.13 GiB / 9.00 GiB
 启动盘路径        : /dev/vda1
 内存              : 179.45 MiB / 972.25 MiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 0 days, 0 hour 20 min
 负载              : 0.63, 0.41, 0.27
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.0-11-cloud-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 NAT类型           : 独立映射,独立过滤,不支持回环
 IPV4 ASN          : AS13335 Cloudflare, Inc.
 IPV4 位置         : Warsaw / Mazovia / PL
 IPV6 ASN          : AS12876 Scaleway
 IPV6 位置         : Warsaw / Mazovia
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           1584 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          42293.97 MB/s
 单线程写测试:          19160.22 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         55.0 MB/s (13.44 IOPS, 1.90s))          73.2 MB/s (17863 IOPS, 1.43s)
 1GB-1M Block           451 MB/s (430 IOPS, 2.33s)              2.4 GB/s (2320 IOPS, 0.43s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 122.71 MB/s  (30.6k) | 1.60 GB/s    (25.0k)
Write      | 123.03 MB/s  (30.7k) | 1.61 GB/s    (25.1k)
Total      | 245.75 MB/s  (61.4k) | 3.21 GB/s    (50.2k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.50 GB/s     (6.8k) | 3.49 GB/s     (3.4k)
Write      | 3.69 GB/s     (7.2k) | 3.72 GB/s     (3.6k)
Total      | 7.19 GB/s    (14.0k) | 7.21 GB/s     (7.0k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA16S31)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 波兰 华沙(WAW07S11)
Youtube识别地域: 无信息(null)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：波兰
[IPv6]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：波兰
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：波兰区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：波兰区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: US)
 HotStar:                               No
 Disney+:                               Yes (Region: PL)
 Netflix:                               Yes (Region: PL)
 YouTube Premium:                       Failed
 Amazon Prime Video:                    Yes (Region: PL)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Frankfurt 
 Netflix Preferred CDN:                 Warsaw  
 Spotify Registration:                  Yes (Region: PL)
 Steam Currency:                        PLN
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: PL)
 Netflix:                               Originals Only
 YouTube Premium:                       Failed
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Warsaw 
 Netflix Preferred CDN:                 Warsaw  
 Spotify Registration:                  No
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【PL】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 10②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Content Delivery Network⑤  hosting⑧  hosting⑨  
  公司类型(company_type):hosting①  hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ②   Yes⑥ ⑦ ⑧ ⑨ ⑩ 
  VPN(vpn):  No① ② ⑦ ⑧ 
  TOR(tor):  No① ② ⑦ ⑧ ⑨ 
  TOR出口(tor_exit):  No⑧ 
  搜索引擎机器人(search_engine_robot):  No② 
  匿名代理(anonymous):  No⑦ ⑧   Yes⑨ 
  攻击方(attacker):  No⑧ ⑨ 
  滥用者(abuser):  No⑧ ⑨ 
  威胁(threat):  No⑧ ⑨ 
  iCloud中继(icloud_relay):  No① ⑧ ⑨ 
  未分配IP(bogon):  No⑧ ⑨ 
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测88 ③
Google搜索可行性：NO
------以下为IPV6检测------
欺诈分数(越低越好): 15②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: PL 城市: Warsaw 服务商: AS13335 Cloudflare, Inc.
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
成都移动 211.137.96.205  测试超时
2023/09/16 11:23:42 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
2.55 ms         * United States of America Texas Dallas
34.22 ms        AS13335 [CLOUDFLARENET] 波兰 马佐夫舍省 华沙 cloudflare.com
2.90 ms         AS1299 [TELIANET] 波兰 马佐夫舍省 华沙 arelion.com
22.40 ms        AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
112.37 ms       AS4134 [CHINANET-BB] 德国 黑森州 美因河畔法兰克福 Telia-CTEuro-PoP chinatelecom.com.cn 电信
460.98 ms       AS4134 [CHINANET-BB] 中国 广州市 广州市 chinatelecom.com.cn 电信
266.72 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
* ms    AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
293.03 ms       AS134774 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.cn 电信
295.00 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
2.62 ms         * United States of America Texas Dallas
3.48 ms         AS13335 [CLOUDFLARENET] 波兰 马佐夫舍省 华沙 cloudflare.com
3.60 ms         AS1299 [TELIANET] 波兰 马佐夫舍省 华沙 arelion.com
125.11 ms       AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
273.70 ms       AS4837 [CU169-BACKBONE] 德国 黑森州 美茵河畔法兰克福 chinaunicom.cn 联通
307.44 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
294.42 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
302.79 ms       AS17816 [APNIC-AP] 中国 广东省 茂名市 chinaunicom.cn 联通
301.14 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
306.00 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
2.27 ms         * United States of America Texas Dallas
10.63 ms        AS13335 [CLOUDFLARENET] 波兰 马佐夫舍省 华沙 cloudflare.com
2.93 ms         AS1299 [TELIANET] 波兰 马佐夫舍省 华沙 arelion.com
22.99 ms        AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 arelion.com
26.34 ms        AS1299 [ARELION-NET] 德国 黑森州 美因河畔法兰克福 Telia-CM-Cust arelion.com
22.66 ms        AS58453 [CMI-INT] 德国 黑森州 美茵河畔法兰克福 cmi.chinamobile.com 移动
206.59 ms       AS58453 [CMI-INT] 德国 黑森州 美因河畔法兰克福 cmi.chinamobile.com 移动
206.98 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
207.22 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
209.02 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
208.99 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
212.33 ms       AS9808 [CMNET] 中国 海南省 海口市 chinamobile.com 移动
209.91 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    98.26 Mbps      5708.13 Mbps    1.05     0.0%
法兰克福         99.88 Mbps      5778.46 Mbps    22.59    0.0%
洛杉矶           168.07 Mbps     438.91 Mbps     163.87   0.5%
移动Chengdu      311.07 Mbps     1221.11 Mbps    306.43   0.0%
------------------------------------------------------------------------
 总共花费      : 4 分 50 秒
 时间          : Sat Sep 16 11:27:08 UTC 2023
------------------------------------------------------------------------
```
