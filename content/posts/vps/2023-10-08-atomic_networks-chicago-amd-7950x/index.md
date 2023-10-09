---
title: "Atomic_Networks 芝加哥 AMD 7950X 测评"
date: "2023-10-08"
categories: 
  - "vps"
  - "laboratory"
  - "performance"
  - "usa"
---

本次测评将全部采用xanmod Linux 6.1 LTS内核，开启BBRv3，顺便测测服务器。之前测评过他家的7900系列，因为不限流量，网络挺糟糕的，详情可见 [Atomic\_Networks 洛杉矶7900测评](https://catcat.blog/atomic_networks-%E6%B4%9B%E6%9D%89%E7%9F%B67900%E6%B5%8B%E8%AF%84.html)。今天这款芝加哥的7950X似乎同样性能不是很好，IP还被送中了，单核只有2200分，美区的解锁还不错。建议避坑。

> ## 套餐
> 
> **_Provider :_ Atomic\_Networks  
> _Type/Plan :_ 1GB CHI P-KVM Slice  
> _Processor :_ AMD Ryzen 9 7950X (4.5 GHz++)  
> _Num of Core : 1 Cores_  
> _Memory : 1 GB_ DDR5 RAM  
> _Storage : 30 GB NVMe_(PCIe 4.0)  
> _Bandwidth : Unmetered Bandwidth (_Fair Use_)  @ 1 Gbps IN | 1 Gbps OUT_  
> _Location :_ Chicago  
> _Price :_ $4.29 /month**

## 测评

### lscpu

```
root@catcat:~# lscpu
Architecture:            x86_64
  CPU op-mode(s):        32-bit, 64-bit
  Address sizes:         48 bits physical, 48 bits virtual
  Byte Order:            Little Endian
CPU(s):                  1
  On-line CPU(s) list:   0
Vendor ID:               AuthenticAMD
  BIOS Vendor ID:        QEMU
  Model name:            AMD Ryzen 9 7950X 16-Core Processor
    BIOS Model name:     pc-i440fx-7.2  CPU @ 2.0GHz
    BIOS CPU family:     1
    CPU family:          25
    Model:               97
    Thread(s) per core:  1
    Core(s) per socket:  1
    Socket(s):           1
    Stepping:            2
    BogoMIPS:            8999.96
Virtualization features: 
  Virtualization:        AMD-V
  Hypervisor vendor:     KVM
  Virtualization type:   full
Caches (sum of all):     
  L1d:                   32 KiB (1 instance)
  L1i:                   32 KiB (1 instance)
  L2:                    1 MiB (1 instance)
  L3:                    64 MiB (1 instance)
NUMA:                    
  NUMA node(s):          1
  NUMA node0 CPU(s):     0
Vulnerabilities:         
  Itlb multihit:         Not affected
  L1tf:                  Not affected
  Mds:                   Not affected
  Meltdown:              Not affected
  Mmio stale data:       Not affected
  Retbleed:              Not affected
  Spec store bypass:     Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:            Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:            Mitigation; Retpolines, IBPB conditional, IBRS_FW, STIBP disabled, RSB filling, PBRSB-eIB
                         RS Not affected
  Srbds:                 Not affected
  Tsx async abort:       Not affected
```

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 3 minutes
Processor  : AMD Ryzen 9 7950X 16-Core Processor
CPU cores  : 1 @ 4499.980 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 928.8 MiB
Swap       : 2.0 GiB
Disk       : 29.9 GiB
Distro     : Debian GNU/Linux 12 (bookworm)
Kernel     : 6.1.46-x64v4-xanmod1
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Atomic Networks LLC
ASN        : AS399820 Atomic Networks LLC
Host       : Atomic Networks LLC
Location   : Cheney, Kansas (KS)
Country    : United States

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 357.34 MB/s  (89.3k) | 4.20 GB/s    (65.6k)
Write      | 358.28 MB/s  (89.5k) | 4.22 GB/s    (65.9k)
Total      | 715.62 MB/s (178.9k) | 8.42 GB/s   (131.5k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.40 GB/s     (8.5k) | 4.65 GB/s     (4.5k)
Write      | 4.63 GB/s     (9.0k) | 4.96 GB/s     (4.8k)
Total      | 9.03 GB/s    (17.6k) | 9.61 GB/s     (9.3k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.05 Gbits/sec  | 300 Mbits/sec   | 88.2 ms        
Scaleway        | Paris, FR (10G)           | 1.05 Gbits/sec  | 141 Mbits/sec   | 91.9 ms        
NovoServe       | North Holland, NL (40G)   | 1.05 Gbits/sec  | 761 Mbits/sec   | 101 ms         
Uztelecom       | Tashkent, UZ (10G)        | 790 Mbits/sec   | 360 Mbits/sec   | -- 
Clouvider       | NYC, NY, US (10G)         | 1.11 Gbits/sec  | 960 Mbits/sec   | 20.2 ms        
Clouvider       | Dallas, TX, US (10G)      | 990 Mbits/sec   | 78.2 Mbits/sec  | 23.6 ms        
Clouvider       | Los Angeles, CA, US (10G) | 1.08 Gbits/sec  | 253 Mbits/sec   | 55.8 ms        

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 1.04 Gbits/sec  | 333 Mbits/sec   | 89.1 ms        
Scaleway        | Paris, FR (10G)           | 1.06 Gbits/sec  | 133 Mbits/sec   | 91.6 ms        
NovoServe       | North Holland, NL (40G)   | 1.05 Gbits/sec  | 749 Mbits/sec   | 101 ms         
Uztelecom       | Tashkent, UZ (10G)        | busy            | 1.24 Mbits/sec  | 241 ms         
Clouvider       | NYC, NY, US (10G)         | busy            | 958 Mbits/sec   | 20.2 ms        
Clouvider       | Dallas, TX, US (10G)      | 1.11 Gbits/sec  | 813 Mbits/sec   | 23.5 ms        
Clouvider       | Los Angeles, CA, US (10G) | 1.08 Gbits/sec  | 225 Mbits/sec   | 55.8 ms        

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2262                          
Multi Core      | 1617                          
Full Test       | https://browser.geekbench.com/v6/cpu/2977291

YABS completed in 15 min 44 sec
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 7950X 16-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 4499.980 MHz
 CPU 缓存          : L1: 32.00 KB / L2: 1.00 MB / L3: 64.00 MB
 硬盘空间          : 4.57 GiB / 29.82 GiB
 启动盘路径        : /dev/sda3
 内存              : 184.07 MiB / 928.79 MiB
 Swap              : 14.46 MiB / 2.00 GiB
 系统在线时间      : 0 days, 0 hour 20 min
 负载              : 0.18, 0.50, 0.30
 系统              : Debian GNU/Linux 12 (bookworm) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 6.1.46-x64v4-xanmod1
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS399820 Atomic Networks LLC
 IPV4 位置         : Chicago / Illinois / US
 IPV6 ASN          : AS399820 Atomic Networks LLC
 IPV6 位置         : Naperville / US-IL
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           6550 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          77016.53 MB/s
 单线程写测试:          43223.84 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         121 MB/s (29.63 IOPS, 0.86s))           152 MB/s (37177 IOPS, 0.69s)
 1GB-1M Block           1.7 GB/s (1661 IOPS, 0.60s)             6.1 GB/s (5777 IOPS, 0.17s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 370.36 MB/s  (92.5k) | 4.15 GB/s    (64.8k)
Write      | 371.33 MB/s  (92.8k) | 4.17 GB/s    (65.1k)
Total      | 741.69 MB/s (185.4k) | 8.32 GB/s   (130.0k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.75 GB/s     (9.2k) | 4.79 GB/s     (4.6k)
Write      | 5.00 GB/s     (9.7k) | 5.11 GB/s     (4.9k)
Total      | 9.75 GB/s    (19.0k) | 9.91 GB/s     (9.6k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: ORD(ORD38S25)
Youtube识别地域: 无信息(null)
[IPv6]
连接方式: Youtube Video Server
视频缓存节点地域: 美国  达拉斯(DFW28S09)
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
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: US)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       No  (Region: CN) 
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Chicago, IL 
 Netflix Preferred CDN:                 New York, NY  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Dallas, TX 
 Netflix Preferred CDN:                 New York, NY  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【US】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 84②
abuse得分(越低越好): 0④
IP类型: 
  使用类型(usage_type):hosting①  Data Center/Web Hosting/Transit⑤  hosting⑧  business⑨  
  公司类型(company_type):hosting①  hosting⑧  
  云服务提供商(cloud_provider):  Yes⑧ 
  数据中心(datacenter):  Yes②   No⑥ ⑨ 
  移动网络(mobile):  Yes⑥ 
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
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测88 ③
Google搜索可行性：YES
------以下为IPV6检测------
欺诈分数(越低越好): 84②
abuse得分(越低越好): 0④
IP类型: Data Center/Web Hosting/Transit⑤
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: US 城市: Chicago 服务商: AS399820 Atomic Networks LLC
北京电信 219.141.136.12  测试超时
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
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
0.22 ms         AS399820 美国 伊利诺伊州 芝加哥 Atomic Holdings LLC
0.92 ms         * 美国 伊利诺伊州 芝加哥 Cogent
2.42 ms         * [COGENT-BONE] 美国 伊利诺伊州 芝加哥 Cogent
63.63 ms        AS174 [COGENT-BONE] 美国 密苏里州 堪萨斯城 cogentco.com
25.28 ms        AS174 [COGENT-BONE] 美国 科罗拉多州 丹佛 cogentco.com
35.72 ms        AS174 [COGENT-BONE] 美国 犹他州 盐湖城 cogentco.com
50.35 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 旧金山 cogentco.com
50.98 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 圣何塞 cogentco.com
52.52 ms        AS174 美国 加利福尼亚州 圣克拉拉 cogentco.com
300.16 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
304.35 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
208.01 ms       AS4134 [CHINANET-BB] 中国 广东省 广州市 chinatelecom.com.cn 电信
209.94 ms       AS134774 [CHINANET-GD] 中国 广东省 深圳市 chinatelecom.cn 电信
210.40 ms       AS4134 中国 广东省 深圳市 福田区 chinatelecom.com.cn 电信
广州联通 210.21.196.6
0.20 ms         AS399820 美国 伊利诺伊州 芝加哥 Atomic Holdings LLC
0.99 ms         * 美国 伊利诺伊州 芝加哥 Cogent
2.14 ms         * [COGENT-BONE] 美国 伊利诺伊州 芝加哥 Cogent
13.88 ms        AS174 [COGENT-BONE] 美国 密苏里州 堪萨斯城 cogentco.com
25.18 ms        AS174 [COGENT-BONE] 美国 科罗拉多州 丹佛 cogentco.com
38.01 ms        AS174 [COGENT-BONE] 美国 得克萨斯州 埃尔帕索 cogentco.com
46.11 ms        AS174 [COGENT-BONE] 美国 亚利桑那州 凤凰城 cogentco.com
58.18 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
58.35 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
221.51 ms       AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
214.22 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
236.08 ms       AS4837 [CU169-BACKBONE] 中国 广东省 广州市 chinaunicom.cn 联通
241.75 ms       AS17816 [UNICOM-GD] 中国 广东省 深圳市 chinaunicom.cn 联通
219.74 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 chinaunicom.cn 联通
216.58 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.25 ms         AS399820 美国 伊利诺伊州 芝加哥 Atomic Holdings LLC
0.93 ms         * 美国 伊利诺伊州 芝加哥 Cogent
2.16 ms         * [COGENT-BONE] 美国 伊利诺伊州 芝加哥 Cogent
13.72 ms        AS174 [COGENT-BONE] 美国 密苏里州 堪萨斯城 cogentco.com
25.40 ms        AS174 [COGENT-BONE] 美国 科罗拉多州 丹佛 cogentco.com
37.99 ms        AS174 [COGENT-BONE] 美国 得克萨斯州 埃尔帕索 cogentco.com
46.09 ms        AS174 [COGENT-BONE] 美国 亚利桑那州 凤凰城 cogentco.com
57.95 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
58.11 ms        AS174 [COGENT-BONE] 美国 加利福尼亚州 洛杉矶 cogentco.com
58.23 ms        AS174 美国 加利福尼亚州 洛杉矶 cogentco.com
58.82 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
58.22 ms        AS58453 [CMI-INT] 美国 加利福尼亚州 洛杉矶 cmi.chinamobile.com 移动
217.00 ms       AS58453 [CMI-INT] 中国 广东省 广州市 cmi.chinamobile.com 移动
221.50 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
218.40 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
217.48 ms       AS9808 [CMNET] 中国 广东省 广州市 chinamobile.com 移动
219.46 ms       AS9808 [CMNET] 中国 北京市 chinamobile.com 移动
219.20 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    1029.86 Mbps    971.94 Mbps     23.68    2.2%
洛杉矶           1110.49 Mbps    985.45 Mbps     57.80    0.0%
法兰克福         858.36 Mbps     972.23 Mbps     104.00   0.0%
联通WuXi         419.40 Mbps     8.29 Mbps       256.15   0.0%
联通Fuzhou       420.38 Mbps     580.72 Mbps     229.80   0.0%
电信Zhenjiang5G  27.93 Mbps      614.98 Mbps     190.56   NULL
电信天津         12.48 Mbps      644.62 Mbps     340.58   NULL
移动Chengdu      32.86 Mbps      420.09 Mbps     301.05   1.7%
移动硬核通信     1.14 Mbps       12.29 Mbps      722.98   NULL
------------------------------------------------------------------------
 总共花费      : 6 分 41 秒
 时间          : Sun Oct  8 15:09:28 CST 2023
------------------------------------------------------------------------
```

### Bench

```
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X 16-Core Processor
 CPU Cores          : 1 @ 4499.980 MHz
 CPU Cache          : 1024 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 29.9 GB (4.6 GB Used)
 Total Mem          : 928.8 MB (267.3 MB Used)
 Total Swap         : 2.0 GB (14.2 MB Used)
 System uptime      : 0 days, 0 hour 28 min
 Load average       : 0.01, 0.16, 0.21
 OS                 : Debian GNU/Linux 12
 Arch               : x86_64 (64 Bit)
 Kernel             : 6.1.46-x64v4-xanmod1
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Online
 Organization       : AS399820 Atomic Networks LLC
 Location           : Chicago / US
 Region             : Illinois
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.3 GB/s
 I/O Speed(2nd run) : 1.3 GB/s
 I/O Speed(3rd run) : 1.3 GB/s
 I/O Speed(average) : 1331.2 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    1035.59 Mbps      965.99 Mbps         23.69 ms    
 Los Angeles, US  1096.20 Mbps      964.84 Mbps         58.17 ms    
 Dallas, US       1027.60 Mbps      966.78 Mbps         23.41 ms    
 Montreal, CA     888.35 Mbps       910.27 Mbps         23.12 ms    
 Paris, FR        858.24 Mbps       989.49 Mbps         93.53 ms    
 Amsterdam, NL    817.08 Mbps       931.75 Mbps         95.28 ms    
 Nanjing, CN      30.21 Mbps        847.21 Mbps         206.10 ms   
 Hongkong, CN     388.04 Mbps       621.51 Mbps         208.21 ms   
 Singapore, SG    346.19 Mbps       1.10 Mbps           218.69 ms   
 Tokyo, JP        461.35 Mbps       658.27 Mbps         156.27 ms   
----------------------------------------------------------------------
 Finished in        : 5 min 0 sec
 Timestamp          : 2023-10-08 15:15:26 CST
----------------------------------------------------------------------
```

### [PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
AMD Ryzen 9 7950X 16-Core Processor (x86_64)
1 cores @ 0 MHz  |  928 MiB RAM
Number of Processes: 1  |  Test Iterations: 1  |  Test Duration: Medium
--------------------------------------------------------------------------
CPU Mark:                          4000
  Integer Math                     8821 Million Operations/s
  Floating Point Math              7849 Million Operations/s
  Prime Numbers                    31.9 Million Primes/s
  Sorting                          5525 Thousand Strings/s
  Encryption                       1965 MB/s
  Compression                      37197 KB/s
  CPU Single Threaded              4053 Million Operations/s
  Physics                          524 Frames/s
  Extended Instructions (SSE)      3226 Million Matrices/s

Memory Mark:                       1098
  Database Operations              1257 Thousand Operations/s
  Memory Read Cached               40944 MB/s
  Memory Read Uncached             35117 MB/s
  Memory Write                     20590 MB/s
  Available RAM                    585 Megabytes
  Memory Latency                   64 Nanoseconds
  Memory Threaded                  36838 MB/s
--------------------------------------------------------------------------
```

### byte-unixbench 性能测试

```
========================================================================
   BYTE UNIX Benchmarks (Version 5.1.3)

   System: catcat.blog: GNU/Linux
   OS: GNU/Linux -- 6.1.46-x64v4-xanmod1 -- #0~20230816.g11dcd23 SMP PREEMPT_DYNAMIC Thu Aug 17 03:15:33 UTC
   Machine: x86_64 (unknown)
   Language: en_US.utf8 (charmap="UTF-8", collate="UTF-8")
   CPU 0: AMD Ryzen 9 7950X 16-Core Processor (9000.0 bogomips)
          x86-64, MMX, AMD MMX, Physical Address Ext, SYSENTER/SYSEXIT, AMD virtualization, SYSCALL/SYSRET
   15:22:44 up 41 min,  1 user,  load average: 0.49, 0.36, 0.26; runlevel 5

------------------------------------------------------------------------
Benchmark Run: Sun Oct 08 2023 15:22:44 - 15:51:04
1 CPU in system; running 1 parallel copy of tests

Dhrystone 2 using register variables       81089030.2 lps   (10.0 s, 7 samples)
Double-Precision Whetstone                    13139.7 MWIPS (10.0 s, 7 samples)
Execl Throughput                               4578.5 lps   (30.0 s, 2 samples)
File Copy 1024 bufsize 2000 maxblocks       1006701.7 KBps  (30.0 s, 2 samples)
File Copy 256 bufsize 500 maxblocks          256213.0 KBps  (30.0 s, 2 samples)
File Copy 4096 bufsize 8000 maxblocks       3587713.6 KBps  (30.0 s, 2 samples)
Pipe Throughput                             1706948.2 lps   (10.0 s, 7 samples)
Pipe-based Context Switching                 243974.2 lps   (10.0 s, 7 samples)
Process Creation                              13346.6 lps   (30.0 s, 2 samples)
Shell Scripts (1 concurrent)                  12936.2 lpm   (60.0 s, 2 samples)
Shell Scripts (8 concurrent)                   1719.3 lpm   (60.0 s, 2 samples)
System Call Overhead                        1544519.5 lps   (10.0 s, 7 samples)

System Benchmarks Index Values               BASELINE       RESULT    INDEX
Dhrystone 2 using register variables         116700.0   81089030.2   6948.5
Double-Precision Whetstone                       55.0      13139.7   2389.0
Execl Throughput                                 43.0       4578.5   1064.8
File Copy 1024 bufsize 2000 maxblocks          3960.0    1006701.7   2542.2
File Copy 256 bufsize 500 maxblocks            1655.0     256213.0   1548.1
File Copy 4096 bufsize 8000 maxblocks          5800.0    3587713.6   6185.7
Pipe Throughput                               12440.0    1706948.2   1372.1
Pipe-based Context Switching                   4000.0     243974.2    609.9
Process Creation                                126.0      13346.6   1059.3
Shell Scripts (1 concurrent)                     42.4      12936.2   3051.0
Shell Scripts (8 concurrent)                      6.0       1719.3   2865.5
System Call Overhead                          15000.0    1544519.5   1029.7
                                                                   ========
System Benchmarks Index Score                                        1970.8



======= Script description and score comparison completed! ======= 
```

### Speedtest

```
root@catcat:~# speedtest   Speedtest by Ookla      Server: Kansas Research and Education Network - Wichita, KS (id: 20531)         ISP: Atomic-networks-1Idle Latency:    23.68 ms   (jitter: 0.03ms, low: 23.65ms, high: 23.70ms)    Download:   966.52 Mbps (data used: 1.2 GB)                                                                    24.09 ms   (jitter: 0.11ms, low: 23.76ms, high: 24.36ms)      Upload:  1033.12 Mbps (data used: 1.5 GB)                                                                    23.80 ms   (jitter: 0.10ms, low: 23.68ms, high: 24.56ms) Packet Loss:     0.0%  Result URL: https://www.speedtest.net/result/c/9b905662-e8f5-4a9f-be59-466d08ab9278
```

![](https://catcat.blog/wp-content/uploads/2023/10/image-7-1024x372.png)

### 流媒体解锁测试

```
============[ Multination ]============
 Dazn:                                  Yes (Region: US)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       No  (Region: CN) 
 Amazon Prime Video:                    Yes (Region: US)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   US
 Viu.com:                               No
 YouTube CDN:                           Chicago, IL 
 Netflix Preferred CDN:                 New York, NY  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        USD
 ChatGPT:                               Yes
=======================================
===========[ North America ]===========
 FOX:                                   Yes
 Hulu:                                  Failed
 NFL+:                                  Yes
 ESPN+:[Sponsored by Jam]               Yes
 Epix:                                  Yes
 Starz:                                 Yes
 Philo:                                 Yes
 FXNOW:                                 Yes
 TLC GO:                                Yes
 HBO Max:                               Yes
 Shudder:                               Yes
 BritBox:                               Yes
 Crackle:                               Yes
 CW TV:                                 Yes
 A&E TV:                                No
 NBA TV:                                Yes
 NBC TV:                                Yes
 Fubo TV:                               No
 Tubi TV:                               Yes
 Sling TV:                              Yes
 Pluto TV:                              Yes
 Acorn TV:                              Yes
 SHOWTIME:                              Yes
 encoreTVB:                             Yes
 Funimation:                            Yes (Region: US)
 Discovery+:                            Yes
 Paramount+:                            Yes
 Peacock TV:                            Yes
 Popcornflix:                           Yes
 Crunchyroll:                           Yes
 KBS American:                          Failed (Network Connection)
 KOCOWA:                                Yes
 Maths Spot:                            Failed
 ---CA---
 CBC Gem:                               No
 Crave:                                 Yes
=======================================


 ** 正在测试IPv6解锁情况 
--------------------------------
 ** 您的网络为: Atomic-networks-1 (2602:fc2f:100:*:*) 


============[ Multination ]============
 Dazn:                                  Failed (Network Connection)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       Yes
 Amazon Prime Video:                    Unsupported
 TVBAnywhere+:                          Failed (Network Connection)
 iQyi Oversea Region:                   Failed
 Viu.com:                               Failed
 YouTube CDN:                           Dallas, TX 
 Netflix Preferred CDN:                 Washington DC  
 Spotify Registration:                  Yes (Region: US)
 Steam Currency:                        Failed (Network Connection)
 ChatGPT:                               Yes
=======================================
===========[ North America ]===========
 FOX:                                   Yes
 Hulu:                                  Failed
 NFL+:                                  IPv6 Not Support
 ESPN+:[Sponsored by Jam]               Yes
 Epix:                                  Failed (Network Connection)
 Epix:                                  Failed
 Starz:                                 Failed (Network Connection)
 Philo:                                 IPv6 Not Support
 FXNOW:                                 IPv6 Not Support
 TLC GO:                                IPv6 Not Support
 HBO Max:                               Failed (Network Connection)
 Shudder:                               Yes
 BritBox:                               Yes
 Crackle:                               Yes
 CW TV:                                 Yes
 A&E TV:                                IPv6 Not Support
 NBA TV:                                Yes
 NBC TV:                                Yes
 Fubo TV:                               IPv6 Not Support
 Tubi TV:                               Yes
 Sling TV:                              Yes
 Pluto TV:                              Yes
 Acorn TV:                              Failed (Network Connection)
 SHOWTIME:                              Failed (Network Connection)
 encoreTVB:                             Failed (Network Connection)
 Funimation:                            IPv6 Not Support
 Discovery+:                            IPv6 Not Support
 Paramount+:                            Yes
 Peacock TV:                            Yes
 Popcornflix:                           IPv6 Not Support
 Crunchyroll:                           IPv6 Not Support
 KBS American:                          IPv6 Not Support
 KOCOWA:                                IPv6 Not Support
 Maths Spot:                            IPv6 Not Support
 ---CA---
 CBC Gem:                               Failed (Network Connection)
 Crave:                                 Failed (Network Connection)
=======================================
```

### 国内延迟测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-8.png)

### 国际延迟测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-9.png)

### 综合测试

```
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X 16-Core Processor
 CPU Cores          : 1 Core @ 4499.980 MHz
 CPU Cache          : 1024 KB
 AES-NI             : ✓ Enabled
 VM-x/AMD-V         : ✓ Enabled
 Total Disk         : 5.0 GB / 29.9 GB
 Total Mem          : 353.7 MB / 928.8 MB
 Total Swap         : 14.2 MB / 2.0 GB
 System uptime      : 0 days, 1 hour 14 min
 Load average       : 0.09, 1.92, 1.77
 OS                 : Debian GNU/Linux 12 x86_64 (64 Bit)
 Kernel             : 6.1.46-x64v4-xanmod1
 TCP CC             : bbr
 Virtualization     : KVM
----------------------------------------------------------------------
 IP                 : *
 Organization       : AS399820 Atomic Networks LLC
 Location           : Chicago / US
 Region             : Illinois
----------------------------------------------------------------------

 -> CPU Performance Test (Standard Mode, 3-Pass @ 30sec)

 1 Thread Test:                 6311 Scores

Geekbench 4 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 10123                         
Multi Core      | 9017                          
Full Test       | https://browser.geekbench.com/v4/cpu/16881509

Geekbench 5 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2085                          
Multi Core      | 2016                          
Full Test       | https://browser.geekbench.com/v5/cpu/21815078


 -> Memory Performance Test (Standard Mode, 3-Pass @ 30sec)

 1 Thread - Read Test :         77636.05 MB/s
 1 Thread - Write Test:         43161.34 MB/s

 -> Disk Speed Test (4K Block/1M Block, Direct-Write)

 Test Name              Write Speed                             Read Speed
 10MB-4K Block          81.7 MB/s (0.05 IOPS, 0.13s))           110 MB/s (26856 IOPS, 0.10s)
 10MB-1M Block          1.6 GB/s (1487 IOPS, 0.01s)             2.4 GB/s (2334 IOPS, 0.00s)
 100MB-4K Block         115 MB/s (0.04 IOPS, 0.91s))            153 MB/s (37280 IOPS, 0.69s)
 100MB-1M Block         1.2 GB/s (1181 IOPS, 0.08s)             3.9 GB/s (3724 IOPS, 0.03s)
 1GB-4K Block           118 MB/s (0.03 IOPS, 8.91s))            175 MB/s (42817 IOPS, 5.98s)
 1GB-1M Block           2.4 GB/s (2308 IOPS, 0.43s)             6.2 GB/s (5873 IOPS, 0.17s)

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 358.44 MB/s  (89.6k) | 3.96 GB/s    (62.0k)
Write      | 359.39 MB/s  (89.8k) | 3.98 GB/s    (62.3k)
Total      | 717.83 MB/s (179.4k) | 7.95 GB/s   (124.3k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 4.40 GB/s     (8.5k) | 4.70 GB/s     (4.5k)
Write      | 4.63 GB/s     (9.0k) | 5.02 GB/s     (4.9k)
Total      | 9.03 GB/s    (17.6k) | 9.73 GB/s     (9.5k)

----------------------------------------------------------------------
**  TW, Hinet ( 168.95.1.1) **
 
traceroute to 168.95.1.1 (168.95.1.1), 30 hops max, 32 byte packets
 1  23.146.184.254  0.27 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.90 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  2.03 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2832.ccr22.mci01.atlas.cogentco.com (154.54.44.169)  13.82 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3036.ccr22.den01.atlas.cogentco.com (154.54.31.89)  25.16 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be3038.ccr32.slc01.atlas.cogentco.com (154.54.42.97)  35.16 ms  AS174  美国, 犹他州, 盐湖城, cogentco.com
 7  be3110.ccr22.sfo01.atlas.cogentco.com (154.54.44.141)  49.58 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 8  be2430.ccr31.sjc04.atlas.cogentco.com (154.54.88.186)  50.38 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 9  38.122.183.34  50.11 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
10  r4001-s2.tp.hinet.net (202.39.91.78)  172.57 ms  AS9680  中国, 台湾, 台北市, cht.com.tw
11  61-221-53-30.hinet-ip.hinet.net (61.221.53.30)  173.42 ms  AS3462  中国, 台湾, 台北市, cht.com.tw
12  dns.hinet.net (168.95.1.1)  172.38 ms  AS3462  中国, 台湾, cht.com.tw

----------------------------------------------------------------------
**  TW, FETNet ( 139.175.1.254) **
 
traceroute to 139.175.1.254 (139.175.1.254), 30 hops max, 32 byte packets
 1  23.146.184.254  0.24 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.69 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2509.ccr41.ord01.atlas.cogentco.com (154.54.43.233)  2.47 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2831.ccr21.mci01.atlas.cogentco.com (154.54.42.165)  14.02 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3035.ccr21.den01.atlas.cogentco.com (154.54.5.89)  25.47 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be2427.ccr21.elp02.atlas.cogentco.com (154.54.87.21)  37.88 ms  AS174  美国, 德克萨斯州, 埃尔帕索, cogentco.com
 7  be2979.ccr31.phx01.atlas.cogentco.com (154.54.5.217)  46.15 ms  AS174  美国, 亚利桑那州, 凤凰城, cogentco.com
 8  be2931.ccr41.lax01.atlas.cogentco.com (154.54.44.86)  57.97 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
 9  be3271.ccr41.lax04.atlas.cogentco.com (154.54.42.102)  58.13 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
10  38.142.238.218  57.96 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
11  ae2.0.pjr04.wad001.flagtel.com (62.216.129.206)  158.11 ms  AS15412  日本, 东京都, 东京, globalcloudxchange.com
12  ae2.0.eji01.tpe001.flagtel.com (85.95.27.102)  242.09 ms  AS15412  中国, 台湾, 台北市, globalcloudxchange.com
13  80.81.74.210  231.55 ms  AS15412  中国, 台湾, 台北市, globalcloudxchange.com
14  h237-192-72-124.seed.net.tw (192.72.124.237)  248.21 ms  AS4780  中国, 台湾, 台北市, fetnet.net
15  r58-146.seed.net.tw (139.175.58.146)  232.50 ms  AS4780  中国, 台湾, 台北市, fetnet.net
16  ks1-254.dialup.seed.net.tw (139.175.1.254)  230.89 ms  AS4780  中国, 台湾, 台北市, fetnet.net

----------------------------------------------------------------------
**  TW, APTG ( 203.79.224.10) **
 
traceroute to 203.79.224.10 (203.79.224.10), 30 hops max, 32 byte packets
 1  23.146.184.254  0.17 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.86 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  2.39 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2832.ccr22.mci01.atlas.cogentco.com (154.54.44.169)  14.51 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3036.ccr22.den01.atlas.cogentco.com (154.54.31.89)  25.22 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be3038.ccr32.slc01.atlas.cogentco.com (154.54.42.97)  35.38 ms  AS174  美国, 犹他州, 盐湖城, cogentco.com
 7  be3110.ccr22.sfo01.atlas.cogentco.com (154.54.44.141)  49.65 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 8  be2430.ccr31.sjc04.atlas.cogentco.com (154.54.88.186)  50.53 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 9  38.122.183.74  50.16 ms  AS174  美国, 加利福尼亚州, 帕洛阿尔托, cogentco.com
10  175-41-60-229.twgate-ip.twgate.net (175.41.60.229)  174.06 ms  AS9505  中国, 台湾, 台北市, twgate.net
11  203-78-181-134.twgate-ip.twgate.net (203.78.181.134)  190.82 ms  AS9505  中国, 台湾, 台北市, twgate.net
12  203-78-187-78.twgate-ip.twgate.net (203.78.187.78)  174.52 ms  AS9505  中国, 台湾, 台北市, twgate.net
13  203-79-253-161.ebix.net.tw (203.79.253.161)  174.50 ms  AS17709  中国, 台湾, 台北市, aptg.com.tw
14  IL203-79-251-42.static.apol.com.tw (203.79.251.42)  179.33 ms  AS17709  中国, 台湾, 台北市, aptg.com.tw
15  192.168.125.1  178.91 ms  *  局域网
16  dns.octor.com (203.79.224.10)  174.99 ms  AS9311  中国, 台湾, 台北市, aptg.com.tw

----------------------------------------------------------------------
**  TW, SoNET ( 61.64.127.1) **
 
traceroute to 61.64.127.1 (61.64.127.1), 30 hops max, 32 byte packets
 1  23.146.184.254  0.24 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.92 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  4.46 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2766.ccr41.ord03.atlas.cogentco.com (154.54.46.178)  2.12 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 5  telia.ord03.atlas.cogentco.com (154.54.12.38)  2.25 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 6  *
 7  *
 8  *
 9  lax-b22-link.ip.twelve99.net (62.115.118.247)  56.24 ms  AS1299  美国, 加利福尼亚州, 洛杉矶, telia.com
10  lax-b23-link.ip.twelve99.net (62.115.143.38)  56.37 ms  AS1299  美国, 加利福尼亚州, 洛杉矶, telia.com
11  chunghwa-ic-345200.ip.twelve99-cust.net (62.115.175.219)  58.47 ms  AS1299  美国, 加利福尼亚州, 洛杉矶, telia.com
12  203-78-181-145.twgate-ip.twgate.net (203.78.181.145)  176.26 ms  AS9505  中国, 台湾, 台北市, twgate.net
13  203-78-181-214.twgate-ip.twgate.net (203.78.181.214)  176.35 ms  AS9505  中国, 台湾, 台北市, twgate.net
14  175-41-63-86.twgate-ip.twgate.net (175.41.63.86)  176.24 ms  AS9505  中国, 台湾, 台北市, twgate.net
15  219.84.176.118  176.28 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw
16  219.84.176.138  207.87 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw
17  gw.so-net.net.tw (61.64.127.249)  180.13 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw
18  gw.so-net.net.tw (61.64.127.249)  180.94 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw
19  gw.so-net.net.tw (61.64.127.249)  180.36 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw
20  ns1.so-net.net.tw (61.64.127.1)  177.20 ms  AS18182  中国, 台湾, 台北市, so-net.net.tw

----------------------------------------------------------------------
**  TW, TFN ( 219.87.66.1) **
 
traceroute to 219.87.66.1 (219.87.66.1), 30 hops max, 32 byte packets
 1  23.146.184.254  0.19 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.80 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2509.ccr41.ord01.atlas.cogentco.com (154.54.43.233)  2.30 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2765.ccr41.ord03.atlas.cogentco.com (154.54.45.18)  2.35 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 5  *
 6  Bundle-Ether45.br02.tap04.pccwbtn.net (63.223.9.230)  186.31 ms  AS3491,AS31713  中国, 台湾, 台北市, pccw.com
 7  ncic.be6.br01.tap04.pccwbtn.net (63.222.40.102)  186.79 ms  AS3491,AS31713  中国, 台湾, 台北市, pccw.com
 8  60-199-14-246.static.tfn.net.tw (60.199.14.246)  186.39 ms  AS9924  中国, 台湾, 台北市, twmbroadband.com
 9  219-87-66-1.static.tfn.net.tw (219.87.66.1)  186.59 ms  AS9924  中国, 台湾, 台北市, twmbroadband.com

----------------------------------------------------------------------
**  TW,TAIFO ( 103.31.196.1) **
 
traceroute to 103.31.196.1 (103.31.196.1), 30 hops max, 32 byte packets
 1  23.146.184.254  0.19 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.75 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2509.ccr41.ord01.atlas.cogentco.com (154.54.43.233)  2.23 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2831.ccr21.mci01.atlas.cogentco.com (154.54.42.165)  13.81 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3035.ccr21.den01.atlas.cogentco.com (154.54.5.89)  25.09 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be3037.ccr21.slc01.atlas.cogentco.com (154.54.41.145)  35.45 ms  AS174  美国, 犹他州, 盐湖城, cogentco.com
 7  be3109.ccr21.sfo01.atlas.cogentco.com (154.54.44.137)  49.83 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 8  be2379.ccr31.sjc04.atlas.cogentco.com (154.54.42.158)  50.33 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 9  38.122.183.34  50.17 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
10  r4001-s2.tp.hinet.net (211.72.108.22)  185.03 ms  AS3462  中国, 台湾, 台北市, cht.com.tw
11  r4101-s2.tp.hinet.net (220.128.11.130)  180.05 ms  *  中国, 台湾, 台北市, cht.com.tw
12  tpdt-3032.hinet.net (220.128.7.118)  179.34 ms  *  中国, 台湾, 台北市, cht.com.tw
13  220-128-1-153.hinet-ip.hinet.net (220.128.1.153)  179.09 ms  *  中国, 台湾, 台北市, cht.com.tw
14  210-242-214-5.hinet-ip.hinet.net (210.242.214.5)  180.16 ms  AS3462  中国, 台湾, 台北市, cht.com.tw
15  *
16  103.31.197.66  179.65 ms  AS131584  中国, 台湾, 台北市, taifo.com.tw
17  103.31.196.1  180.51 ms  AS131584  中国, 台湾, 台北市, taifo.com.tw

----------------------------------------------------------------------
**  TW,Kbro ( 123.195.236.110) **
 
traceroute to 123.195.236.110 (123.195.236.110), 30 hops max, 32 byte packets
 1  23.146.184.254  0.20 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.85 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  1.88 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2832.ccr22.mci01.atlas.cogentco.com (154.54.44.169)  13.65 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3036.ccr22.den01.atlas.cogentco.com (154.54.31.89)  25.24 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be3038.ccr32.slc01.atlas.cogentco.com (154.54.42.97)  35.12 ms  AS174  美国, 犹他州, 盐湖城, cogentco.com
 7  be3110.ccr22.sfo01.atlas.cogentco.com (154.54.44.141)  49.57 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 8  be2430.ccr31.sjc04.atlas.cogentco.com (154.54.88.186)  50.37 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 9  omnicell-tech.demarc.cogentco.com (38.104.140.74)  49.94 ms  AS174  美国, 加利福尼亚州, 帕洛阿尔托, cogentco.com
10  60-199-22-81.static.tfn.net.tw (60.199.22.81)  201.21 ms  AS9924  中国, 台湾, 台北市, twmbroadband.com
11  60-199-14-246.static.tfn.net.tw (60.199.14.246)  201.16 ms  AS9924  中国, 台湾, 台北市, twmbroadband.com
12  60-199-3-141.static.tfn.net.tw (60.199.3.141)  201.35 ms  AS9924  中国, 台湾, 台北市, twmbroadband.com
13  60-199-47-206.static.tfn.net.tw (60.199.47.206)  209.08 ms  AS9924  中国, 台湾, 台北市, twmbroadband.com
14  219-80-240-90.static.tfn.net.tw (219.80.240.90)  201.73 ms  AS9924  中国, 台湾, 桃园市, twmbroadband.com
15  *
16  *
17  123-195-236-110.dynamic.kbronet.com.tw (123.195.236.110)  201.51 ms  AS38841  中国, 台湾, 台北市, kbro.com.tw

----------------------------------------------------------------------
**  北京电信 ( 219.141.147.210) **
 
traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  23.146.184.254  0.16 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.85 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  2.14 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2832.ccr22.mci01.atlas.cogentco.com (154.54.44.169)  13.71 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3036.ccr22.den01.atlas.cogentco.com (154.54.31.89)  25.50 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be3038.ccr32.slc01.atlas.cogentco.com (154.54.42.97)  35.70 ms  AS174  美国, 犹他州, 盐湖城, cogentco.com
 7  be3110.ccr22.sfo01.atlas.cogentco.com (154.54.44.141)  49.62 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 8  be3670.ccr41.sjc03.atlas.cogentco.com (154.54.43.14)  50.83 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 9  38.104.138.106  53.08 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
10  *
11  *
12  *
13  *
14  *
15  2.254.120.106.static.bjtelecom.net (106.120.254.2)  198.33 ms  AS4847  中国, 北京, chinatelecom.com.cn, 电信
16  bj141-147-210.bjtelecom.net (219.141.147.210)  194.56 ms  AS4847  中国, 北京, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
**  上海电信 ( 202.96.209.133) **
 
traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  23.146.184.254  0.15 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.99 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2509.ccr41.ord01.atlas.cogentco.com (154.54.43.233)  2.26 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2831.ccr21.mci01.atlas.cogentco.com (154.54.42.165)  14.21 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3035.ccr21.den01.atlas.cogentco.com (154.54.5.89)  25.50 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be3037.ccr21.slc01.atlas.cogentco.com (154.54.41.145)  35.61 ms  AS174  美国, 犹他州, 盐湖城, cogentco.com
 7  be3109.ccr21.sfo01.atlas.cogentco.com (154.54.44.137)  49.63 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 8  be3669.ccr41.sjc03.atlas.cogentco.com (154.54.43.10)  51.62 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 9  38.104.138.106  51.82 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
10  *
11  202.97.12.193  184.14 ms  AS4134  中国, 上海, chinatelecom.com.cn, 电信
12  202.97.50.177  199.81 ms  AS4134  中国, 上海, chinatelecom.com.cn, 电信
13  *
14  *
15  124.74.229.238  188.10 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信
16  ns-pd.online.sh.cn (202.96.209.133)  192.35 ms  AS4812  中国, 上海, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
**  深圳电信 ( 58.60.188.222) **
 
traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  23.146.184.254  0.12 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.96 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2509.ccr41.ord01.atlas.cogentco.com (154.54.43.233)  2.49 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2831.ccr21.mci01.atlas.cogentco.com (154.54.42.165)  14.41 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3035.ccr21.den01.atlas.cogentco.com (154.54.5.89)  25.23 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be3037.ccr21.slc01.atlas.cogentco.com (154.54.41.145)  35.59 ms  AS174  美国, 犹他州, 盐湖城, cogentco.com
 7  be3109.ccr21.sfo01.atlas.cogentco.com (154.54.44.137)  49.55 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 8  be3669.ccr41.sjc03.atlas.cogentco.com (154.54.43.10)  50.94 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 9  38.104.138.106  52.07 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
10  202.97.43.121  199.90 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
11  *
12  202.97.82.21  214.88 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
13  14.147.127.14  217.94 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
14  *
15  58.60.188.222  204.77 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信

----------------------------------------------------------------------
**  北京联通 ( 202.106.50.1) **
 
traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  23.146.184.254  0.20 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  1.13 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  2.12 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2832.ccr22.mci01.atlas.cogentco.com (154.54.44.169)  13.96 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3036.ccr22.den01.atlas.cogentco.com (154.54.31.89)  25.26 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be3038.ccr32.slc01.atlas.cogentco.com (154.54.42.97)  35.71 ms  AS174  美国, 犹他州, 盐湖城, cogentco.com
 7  be3110.ccr22.sfo01.atlas.cogentco.com (154.54.44.141)  49.75 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 8  be3670.ccr41.sjc03.atlas.cogentco.com (154.54.43.14)  50.94 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 9  38.88.224.14  75.44 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
10  219.158.117.1  276.22 ms  AS4837  中国, 北京, chinaunicom.com, 联通
11  219.158.16.77  264.13 ms  AS4837  中国, 北京, chinaunicom.com, 联通
12  219.158.5.145  260.40 ms  AS4837  中国, 北京, chinaunicom.com, 联通
13  125.33.186.118  269.90 ms  AS4808  中国, 北京, chinaunicom.com, 联通
14  202.106.50.1  233.35 ms  AS4808  中国, 北京, chinaunicom.com, 联通

----------------------------------------------------------------------
**  上海联通 ( 210.22.97.1) **
 
traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  23.146.184.254  0.29 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.97 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  2.15 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2832.ccr22.mci01.atlas.cogentco.com (154.54.44.169)  13.67 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3036.ccr22.den01.atlas.cogentco.com (154.54.31.89)  59.11 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be3038.ccr32.slc01.atlas.cogentco.com (154.54.42.97)  35.21 ms  AS174  美国, 犹他州, 盐湖城, cogentco.com
 7  be3110.ccr22.sfo01.atlas.cogentco.com (154.54.44.141)  50.50 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 8  be3670.ccr41.sjc03.atlas.cogentco.com (154.54.43.14)  50.75 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 9  38.142.244.250  51.98 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
10  219.158.6.5  210.38 ms  AS4837  中国, 上海, chinaunicom.com, 联通
11  219.158.6.209  186.49 ms  AS4837  中国, 上海, chinaunicom.com, 联通
12  *
13  *
14  112.64.250.202  208.55 ms  AS17621  中国, 上海, chinaunicom.com, 联通
15  210.22.97.1  186.76 ms  AS17621  中国, 上海, chinaunicom.com, 联通

----------------------------------------------------------------------
**  深圳联通 ( 210.21.196.6) **
 
traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  23.146.184.254  0.20 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  1.16 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  12.84 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2832.ccr22.mci01.atlas.cogentco.com (154.54.44.169)  13.85 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3036.ccr22.den01.atlas.cogentco.com (154.54.31.89)  25.11 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be2668.ccr22.elp02.atlas.cogentco.com (154.54.87.29)  37.96 ms  AS174  美国, 德克萨斯州, 埃尔帕索, cogentco.com
 7  be3872.ccr32.phx01.atlas.cogentco.com (154.54.26.53)  46.18 ms  AS174  美国, 亚利桑那州, 凤凰城, cogentco.com
 8  be2932.ccr42.lax01.atlas.cogentco.com (154.54.45.162)  57.87 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
 9  be3250.rcr62.lax04.atlas.cogentco.com (154.54.91.14)  58.28 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
10  38.142.238.66  222.43 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
11  219.158.17.85  216.14 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
12  219.158.4.129  236.11 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
13  *
14  221.4.0.130  240.84 ms  AS17816  中国, 广东, 深圳, chinaunicom.com, 联通
15  120.80.144.38  219.68 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
16  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  216.62 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通

----------------------------------------------------------------------
**  北京移动 ( 221.179.155.161) **
 
traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  23.146.184.254  0.25 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.80 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2509.ccr41.ord01.atlas.cogentco.com (154.54.43.233)  2.31 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2831.ccr21.mci01.atlas.cogentco.com (154.54.42.165)  13.92 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3035.ccr21.den01.atlas.cogentco.com (154.54.5.89)  25.39 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be2427.ccr21.elp02.atlas.cogentco.com (154.54.87.21)  37.92 ms  AS174  美国, 德克萨斯州, 埃尔帕索, cogentco.com
 7  be2979.ccr31.phx01.atlas.cogentco.com (154.54.5.217)  46.11 ms  AS174  美国, 亚利桑那州, 凤凰城, cogentco.com
 8  be2931.ccr41.lax01.atlas.cogentco.com (154.54.44.86)  57.94 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
 9  be3243.ccr41.lax05.atlas.cogentco.com (154.54.27.118)  58.02 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
10  38.104.85.162  401.27 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
11  223.120.6.217  393.83 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
12  223.120.12.214  593.19 ms  AS58453  中国, 上海, chinamobile.com, 移动
13  221.183.55.106  594.35 ms  AS9808  中国, 北京, chinamobile.com, 移动
14  221.183.46.250  597.98 ms  AS9808  中国, 北京, chinamobile.com, 移动
15  *
16  221.183.46.178  575.84 ms  AS9808  中国, 北京, chinamobile.com, 移动
17  *
18  cachedns03.bj.chinamobile.com (221.179.155.161)  559.62 ms  AS56048  中国, 北京, chinamobile.com, 移动

----------------------------------------------------------------------
**  上海移动 ( 211.136.112.200) **
 
traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  23.146.184.254  0.23 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  1.00 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  2.20 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2832.ccr22.mci01.atlas.cogentco.com (154.54.44.169)  13.71 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3036.ccr22.den01.atlas.cogentco.com (154.54.31.89)  81.71 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be3038.ccr32.slc01.atlas.cogentco.com (154.54.42.97)  35.17 ms  AS174  美国, 犹他州, 盐湖城, cogentco.com
 7  be3110.ccr22.sfo01.atlas.cogentco.com (154.54.44.141)  49.61 ms  AS174  美国, 加利福尼亚州, 旧金山, cogentco.com
 8  be3670.ccr41.sjc03.atlas.cogentco.com (154.54.43.14)  50.94 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
 9  38.88.224.162  50.89 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
10  223.120.6.69  51.04 ms  AS58453  美国, 加利福尼亚州, 圣何塞, chinamobile.com, 移动
11  *
12  221.183.89.170  232.24 ms  AS9808  中国, 上海, chinamobile.com, 移动
13  221.183.89.33  232.62 ms  AS9808  中国, 上海, chinamobile.com, 移动
14  221.183.89.10  234.47 ms  AS9808  中国, 上海, chinamobile.com, 移动
15  *
16  211.136.190.242  236.05 ms  AS24400  中国, 上海, chinamobile.com, 移动
17  211.136.112.252  236.64 ms  AS24400  中国, 上海, chinamobile.com, 移动
18  211.136.112.200  238.41 ms  AS24400  中国, 上海, chinamobile.com, 移动

----------------------------------------------------------------------
**  深圳移动 ( 120.196.165.24) **
 
traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  23.146.184.254  0.20 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.89 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  2.15 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2832.ccr22.mci01.atlas.cogentco.com (154.54.44.169)  14.00 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3036.ccr22.den01.atlas.cogentco.com (154.54.31.89)  25.20 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be2668.ccr22.elp02.atlas.cogentco.com (154.54.87.29)  37.99 ms  AS174  美国, 德克萨斯州, 埃尔帕索, cogentco.com
 7  be3872.ccr32.phx01.atlas.cogentco.com (154.54.26.53)  46.08 ms  AS174  美国, 亚利桑那州, 凤凰城, cogentco.com
 8  be2932.ccr42.lax01.atlas.cogentco.com (154.54.45.162)  57.93 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
 9  be3359.ccr41.lax05.atlas.cogentco.com (154.54.3.70)  58.12 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
10  38.19.140.98  58.11 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
11  223.118.10.81  59.46 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
12  223.120.6.97  58.14 ms  AS58453  美国, 加利福尼亚州, 洛杉矶, chinamobile.com, 移动
13  223.120.12.42  216.88 ms  AS58453  中国, 香港, chinamobile.com, 移动
14  221.183.55.58  221.46 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
15  221.183.92.21  218.17 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
16  *
17  221.183.71.78  217.36 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
18  221.183.110.166  219.32 ms  AS9808  中国, 广东, 广州, chinamobile.com, 移动
19  ns6.gd.cnmobile.net (120.196.165.24)  219.15 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动

----------------------------------------------------------------------
**  成都教育网 ( 202.112.14.151) **
 
traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  23.146.184.254  0.16 ms  AS399820  美国, 伊利诺伊州, 芝加哥, atomicnetworks.co
 2  te0-2-0-0.rcr51.b025243-2.ord01.atlas.cogentco.com (38.142.124.217)  0.72 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 3  be2513.ccr42.ord01.atlas.cogentco.com (154.54.43.237)  2.09 ms  AS174  美国, 伊利诺伊州, 芝加哥, cogentco.com
 4  be2832.ccr22.mci01.atlas.cogentco.com (154.54.44.169)  13.64 ms  AS174  美国, 密苏里州, 堪萨斯城, cogentco.com
 5  be3036.ccr22.den01.atlas.cogentco.com (154.54.31.89)  25.26 ms  AS174  美国, 科罗拉多州, 丹佛, cogentco.com
 6  be2668.ccr22.elp02.atlas.cogentco.com (154.54.87.29)  37.64 ms  AS174  美国, 德克萨斯州, 埃尔帕索, cogentco.com
 7  be3872.ccr32.phx01.atlas.cogentco.com (154.54.26.53)  46.05 ms  AS174  美国, 亚利桑那州, 凤凰城, cogentco.com
 8  be2932.ccr42.lax01.atlas.cogentco.com (154.54.45.162)  57.99 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
 9  be3360.ccr41.lax04.atlas.cogentco.com (154.54.25.150)  58.33 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
10  38.88.196.186  77.48 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
11  101.4.117.169  222.34 ms  AS4538  中国, 北京, edu.cn, 教育网
12  101.4.116.121  209.67 ms  AS4538  中国, 北京, edu.cn, 教育网
13  *
14  101.4.117.81  203.81 ms  AS4538  中国, 北京, edu.cn, 教育网
15  101.4.116.106  222.68 ms  AS4538  中国, 湖北, 武汉, edu.cn, 教育网
16  *
17  *
18  101.4.116.158  247.11 ms  AS4538  中国, 四川, 成都, edu.cn, 教育网
19  *
20  *
21  *
22  202.112.14.151  244.68 ms  AS24355  中国, 四川, 成都, 电子科技大学CERNET西南地区网络中心, edu.cn, 教育网

----------------------------------------------------------------------
```
