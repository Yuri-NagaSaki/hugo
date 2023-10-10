---
title: "Aeza Amusitedan AMD 7950X3D 测评"
date: "2023-09-10"
categories: 
  - "vps"
  - "eu"
---

不测了，这家的鸡有问题，ssh会自动断联，非常的诡异，网络糟糕。

> ## 套餐
> 
> Provider : Aeza  
> Type/Plan : AMD Ryzen KVM VPS - Corporate Power  
> Processor : AMD Ryzen 9 7950X3D  
> Num of Core : 2 Cores  
> Memory : 4 GB  
> Storage : 60 GB NVMe  
> Bandwidth : Unlimited @ 1 Gbps IN | 1 Gbps OUT  
> Location : Amusitedan  
> Price : 94.22RMB

## 测评

### cpu

```
root@proper-trucks:~# lscpu
Architecture:                    x86_64
CPU op-mode(s):                  32-bit, 64-bit
Byte Order:                      Little Endian
Address sizes:                   48 bits physical, 48 bits virtual
CPU(s):                          2
On-line CPU(s) list:             0,1
Thread(s) per core:              1
Core(s) per socket:              2
Socket(s):                       1
NUMA node(s):                    1
Vendor ID:                       AuthenticAMD
CPU family:                      25
Model:                           97
Model name:                      AMD Ryzen 9 7950X3D 16-Core Processor
Stepping:                        2
CPU MHz:                         4192.120
BogoMIPS:                        8384.24
Hypervisor vendor:               KVM
Virtualization type:             full
L1d cache:                       128 KiB
L1i cache:                       128 KiB
L2 cache:                        1 MiB
L3 cache:                        16 MiB
NUMA node0 CPU(s):               0,1
Vulnerability Itlb multihit:     Not affected
Vulnerability L1tf:              Not affected
Vulnerability Mds:               Not affected
Vulnerability Meltdown:          Not affected
Vulnerability Mmio stale data:   Not affected
Vulnerability Retbleed:          Not affected
Vulnerability Spec store bypass: Mitigation; Speculative Store Bypass disabled via prctl and seccomp
Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
Vulnerability Spectre v2:        Mitigation; Retpolines, IBPB conditional, IBRS_FW, STIBP disabled, RSB filling, PBRS                                 B-eIBRS Not affected
Vulnerability Srbds:             Not affected
Vulnerability Tsx async abort:   Not affected
```

### 硬盘

![](https://catcat.blog/wp-content/uploads/2023/09/image-64.png)

### 内存

![](https://catcat.blog/wp-content/uploads/2023/09/image-65-1024x166.png)

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 6 minutes
Processor  : AMD Ryzen 9 7950X3D 16-Core Processor
CPU cores  : 2 @ 4192.120 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ❌ Disabled
RAM        : 3.8 GiB
Swap       : 1024.0 MiB
Disk       : 59.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-21-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv4 Network Information:
---------------------------------
ISP        : AEZA GROUP Ltd
ASN        : AS210644 AEZA GROUP Ltd
Host       : Aeza Group LLC
Location   : Amsterdam, North Holland (NH)
Country    : Netherlands

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 40.00 MB/s   (10.0k) | 656.51 MB/s  (10.2k)
Write      | 40.10 MB/s   (10.0k) | 659.96 MB/s  (10.3k)
Total      | 80.11 MB/s   (20.0k) | 1.31 GB/s    (20.5k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.23 GB/s     (6.3k) | 3.33 GB/s     (3.2k)
Write      | 3.40 GB/s     (6.6k) | 3.56 GB/s     (3.4k)
Total      | 6.63 GB/s    (12.9k) | 6.89 GB/s     (6.7k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 216 Mbits/sec   | 205 Mbits/sec   | 17.6 ms        
Scaleway        | Paris, FR (10G)           | 875 Mbits/sec   | 649 Mbits/sec   | 17.9 ms        
NovoServe       | North Holland, NL (40G)   | busy            | 869 Mbits/sec   | 12.4 ms        
Uztelecom       | Tashkent, UZ (10G)        | 811 Mbits/sec   | 232 Mbits/sec   | 97.2 ms        
Clouvider       | NYC, NY, US (10G)         | busy            | 19.1 Mbits/sec  | 89.9 ms        
Clouvider       | Dallas, TX, US (10G)      | 29.1 Mbits/sec  | 31.9 Mbits/sec  | 129 ms         
Clouvider       | Los Angeles, CA, US (10G) | 23.1 Mbits/sec  | 20.6 Mbits/sec  | 158 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 226 Mbits/sec   | 368 Mbits/sec   | 16.4 ms        
Scaleway        | Paris, FR (10G)           | 757 Mbits/sec   | 437 Mbits/sec   | 17.1 ms        
NovoServe       | North Holland, NL (40G)   | busy            | busy            | 12.5 ms        
Uztelecom       | Tashkent, UZ (10G)        | 597 Mbits/sec   | 48.6 Mbits/sec  | 97.1 ms        
Clouvider       | NYC, NY, US (10G)         | 30.6 Mbits/sec  | 21.3 Mbits/sec  | 95.4 ms        
Clouvider       | Dallas, TX, US (10G)      | 22.0 Mbits/sec  | 24.3 Mbits/sec  | 129 ms         
Clouvider       | Los Angeles, CA, US (10G) | 15.4 Mbits/sec  | 23.4 Mbits/sec  | 158 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2610                          
Multi Core      | 4679                          
Full Test       | https://browser.geekbench.com/v6/cpu/2555602

YABS completed in 12 min 54 sec
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 4192.120 MHz
 CPU 缓存          : L1: 256.00 KB / L2: 1.00 MB / L3: 16.00 MB
 硬盘空间          : 2.76 GiB / 58.98 GiB
 启动盘路径        : /dev/vda1
 内存              : 168.76 MiB / 3.84 GiB
 Swap              : 0 KiB / 1024.00 MiB
 系统在线时间      : 0 days, 0 hour 24 min
 负载              : 0.00, 0.15, 0.13
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-21-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS210644 AEZA GROUP Ltd
 IPV4 位置         : Amsterdam / North Holland / NL
 IPV6 ASN          : AS210644 AEZA GROUP Ltd
 IPV6 位置         : Amsterdam / North Holland
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           5780 Scores
 2 线程测试(多核)得分:          11339 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          67447.20 MB/s
 单线程写测试:          34124.46 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         42.5 MB/s (10.39 IOPS, 2.46s))          42.6 MB/s (10403 IOPS, 2.46s)
 1GB-1M Block           4.3 GB/s (4091 IOPS, 0.24s)             4.8 GB/s (4540 IOPS, 0.22s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 40.02 MB/s   (10.0k) | 656.30 MB/s  (10.2k)
Write      | 40.12 MB/s   (10.0k) | 659.76 MB/s  (10.3k)
Total      | 80.15 MB/s   (20.0k) | 1.31 GB/s    (20.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.98 GB/s     (5.8k) | 3.32 GB/s     (3.2k)
Write      | 3.14 GB/s     (6.1k) | 3.54 GB/s     (3.4k)
Total      | 6.12 GB/s    (11.9k) | 6.87 GB/s     (6.7k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 德国法兰克福(FRA15S37)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  迈阿密(MIA07S69)
Youtube识别地域: 俄罗斯联邦(RU)
----------------Netflix----------------
[IPv4]
您的出口IP可以使用Netflix，但仅可看Netflix自制剧
NF所识别的IP地域信息：荷兰
[IPv6]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：荷兰
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：荷兰区
[IPv6]
当前IPv6出口解锁DisneyPlus
区域：荷兰区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: NL)
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       Failed
 Amazon Prime Video:                    Yes (Region: NL)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   INTL
 Viu.com:                               No
 YouTube CDN:                           Frankfurt 
 Netflix Preferred CDN:                 Stockholm  
 Spotify Registration:                  No
 Steam Currency:                        EUR
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               No
 Disney+:                               Yes (Region: NL)
 Netflix:                               Yes (Region: NL)
 YouTube Premium:                       No 
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Miami, FL 
 Netflix Preferred CDN:                 Frankfurt  
 Spotify Registration:                  No
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【NL】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 72②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  business⑨  
  公司类型(company_type):hosting①  hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
  移动网络(mobile):  No⑥ 
  代理(proxy):  No① ② ⑥ ⑦ ⑧ ⑨ ⑩ 
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
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测87 ③
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  outlook邮箱: Yes
  yandex邮箱: Yes
  qq邮箱：No
------以下为IPV6检测------
欺诈分数(越低越好): 0②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: NL 城市: Amsterdam 服务商: AS210644 AEZA GROUP Ltd
北京电信 219.141.136.12  电信163 [普通线路]           
北京联通 202.106.50.1    联通4837[普通线路]           
北京移动 221.179.155.161 移动CMI [普通线路]           
上海电信 202.96.209.133  测试超时
上海联通 210.22.97.1     联通4837[普通线路]           
上海移动 211.136.112.200 移动CMI [普通线路]           
广州电信 58.60.188.222   电信163 [普通线路]           
广州联通 210.21.196.6    联通4837[普通线路]           
广州移动 120.196.165.24  移动CMI [普通线路]           
成都电信 61.139.2.69     电信163 [普通线路]           
成都联通 119.6.6.6       联通4837[普通线路]           
成都移动 211.137.96.205  移动CMI [普通线路]           
2023/09/10 13:57:47 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.17 ms         * RFC1918
5.29 ms         AS60068 德国 黑森州 美因河畔法兰克福 cdn77.com
13.18 ms        AS60068 德国 黑森州 美因河畔法兰克福 cdn77.com
12.18 ms        AS60068 [CDN77-c0r3] 德国 黑森州 美因河畔法兰克福 cdn77.com
13.66 ms        AS60068 [CDN77-c0r3] 德国 黑森州 美因河畔法兰克福 cdn77.com
15.39 ms        AS3356 [FRANKFURT-SERIAL] 德国 黑森州 美因河畔法兰克福 Level3-CT-Peer level3.com
210.91 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
* ms    AS4134 [CHINANET-BB] 中国 香港 chinatelecom.com.cn 电信
314.92 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.12 ms         * RFC1918
5.34 ms         AS60068 德国 黑森州 美因河畔法兰克福 cdn77.com
12.20 ms        AS60068 德国 黑森州 美因河畔法兰克福 cdn77.com
12.28 ms        AS60068 [CDN77-c0r3] 德国 黑森州 美因河畔法兰克福 cdn77.com
18.27 ms        AS174 [COGENT-BONE] 法国 法兰西岛大区 巴黎 cogentco.com
97.90 ms        AS174 [COGENT-BONE] 美国 华盛顿哥伦比亚特区 华盛顿 cogentco.com
111.60 ms       AS174 [COGENT-BONE] 美国 佐治亚州 亚历山大 cogentco.com
126.57 ms       AS174 [COGENT-BONE] 美国 德克萨斯州 休斯顿 cogentco.com
* ms    AS174 [COGENT-BONE] 美国 得克萨斯州 埃尔帕索 cogentco.com
152.51 ms       AS174 [COGENT-BONE] 美国 亚利桑那州 凤凰城 cogentco.com
164.84 ms       AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
164.99 ms       AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
349.57 ms       AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
345.30 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
328.67 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
* ms    AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
322.33 ms       AS17816 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
354.35 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
328.22 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
 
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    726.18 Mbps     774.90 Mbps     10.80    6.3%
法兰克福         768.22 Mbps     555.41 Mbps     6.07     7.0%
洛杉矶           541.91 Mbps     5.66 Mbps       163.99   0.0%
联通沈阳         331.49 Mbps     1.42 Mbps       240.43   0.0%
联通湖南5G       355.49 Mbps     47.83 Mbps      258.30   NULL
```

### 国内延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-66-1024x457.png)

### 全球延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-67-1024x588.png)
