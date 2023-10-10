---
title: "Aeza USA AMD 7950X3D 测评"
date: "2023-09-11"
categories: 
  - "vps"
  - "performance"
  - "usa"
---

> ## 套餐
> 
> _Provider :_ Aeza  
> _Type/Plan : AMD Ryzen KVM VPS - Corporate Power_  
> _Processor : AMD Ryzen 9 7950X3D_  
> _Num of Core : 2 Cores_  
> _Memory : 4 GB_  
> _Storage : 60 GB NVMe_  
> _Bandwidth : Unlimited @ 1 Gbps IN | 1 Gbps OUT_  
> _Location :_ USA  
> _Price : 120RMB_

## 测评

### Yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 15 minutes
Processor  : AMD Ryzen 9 7950X3D 16-Core Processor
CPU cores  : 2 @ 4199.924 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ❌ Disabled
RAM        : 3.8 GiB
Swap       : 1024.0 MiB
Disk       : 59.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-21-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : FAST
ASN        : AS210644 AEZA GROUP Ltd
Location   : Warsaw, Mazovia (14)
Country    : Poland

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 40.02 MB/s   (10.0k) | 656.51 MB/s  (10.2k)
Write      | 40.12 MB/s   (10.0k) | 659.96 MB/s  (10.3k)
Total      | 80.15 MB/s   (20.0k) | 1.31 GB/s    (20.5k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.86 GB/s     (3.6k) | 1.75 GB/s     (1.7k)
Write      | 1.96 GB/s     (3.8k) | 1.86 GB/s     (1.8k)
Total      | 3.82 GB/s     (7.4k) | 3.61 GB/s     (3.5k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 25.7 Mbits/sec  | 31.5 Mbits/sec  | 144 ms         
Scaleway        | Paris, FR (10G)           | 684 Mbits/sec   | 696 Mbits/sec   | 156 ms         
NovoServe       | North Holland, NL (40G)   | 699 Mbits/sec   | busy            | 151 ms         
Uztelecom       | Tashkent, UZ (10G)        | busy            | 431 Mbits/sec   | 249 ms         
Clouvider       | NYC, NY, US (10G)         | 42.4 Mbits/sec  | 37.9 Mbits/sec  | 93.6 ms        
Clouvider       | Dallas, TX, US (10G)      | 65.8 Mbits/sec  | 145 Mbits/sec   | 58.9 ms        
Clouvider       | Los Angeles, CA, US (10G) | 137 Mbits/sec   | 225 Mbits/sec   | 28.2 ms        

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 2279                          
Multi Core      | 3945                          
Full Test       | https://browser.geekbench.com/v6/cpu/2566741
```

### Bench

```
-------------------- A Bench.sh Script By Teddysun -------------------
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU Cores          : 2 @ 4199.924 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Disabled
 Total Disk         : 59.0 GB (2.2 GB Used)
 Total Mem          : 3.8 GB (56.4 MB Used)
 Total Swap         : 1024.0 MB (0 Used)
 System uptime      : 0 days, 0 hour 2 min
 Load average       : 0.04, 0.03, 0.01
 OS                 : Debian GNU/Linux 11
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.10.0-21-amd64
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Offline
 Organization       : AS210644 AEZA GROUP Ltd
 Location           : Bergen / NO
 Region             : Vestland
----------------------------------------------------------------------
 I/O Speed(1st run) : 1.7 GB/s
 I/O Speed(2nd run) : 2.0 GB/s
 I/O Speed(3rd run) : 2.0 GB/s
 I/O Speed(average) : 1945.6 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency     
 Speedtest.net    500.05 Mbps       834.68 Mbps         161.56 ms   
 Los Angeles, US  811.77 Mbps       825.28 Mbps         28.88 ms    
 Dallas, US       742.68 Mbps       794.32 Mbps         63.40 ms    
 Montreal, CA     459.37 Mbps       414.32 Mbps         108.63 ms   
 Paris, FR        521.55 Mbps       895.64 Mbps         156.70 ms   
 Amsterdam, NL    534.88 Mbps       800.02 Mbps         148.44 ms   
 Shanghai, CN     310.39 Mbps       823.21 Mbps         186.18 ms   
 Nanjing, CN      278.11 Mbps       758.98 Mbps         257.18 ms   
 Hongkong, CN     338.98 Mbps       792.51 Mbps         240.57 ms   
 Singapore, SG    388.00 Mbps       800.40 Mbps         218.72 ms   
 Tokyo, JP        582.64 Mbps       807.29 Mbps         132.80 ms   
----------------------------------------------------------------------
 Finished in        : 6 min 25 sec
 Timestamp          : 2023-09-11 05:39:35 PDT
----------------------------------------------------------------------
```

### 融合怪脚本测试

```
---------------------基础信息查询--感谢所有开源项目---------------------
 CPU 型号          : AMD Ryzen 9 7950X3D 16-Core Processor
 CPU 核心数        : 2
 CPU 频率          : 4199.924 MHz
 CPU 缓存          : L1: 256.00 KB / L2: 1.00 MB / L3: 16.00 MB
 硬盘空间          : 2.42 GiB / 58.98 GiB
 启动盘路径        : /dev/vda1
 内存              : 103.65 MiB / 3.84 GiB
 Swap              : 0 KiB / 1024.00 MiB
 系统在线时间      : 0 days, 0 hour 27 min
 负载              : 0.30, 0.40, 0.20
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ❌ Disabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-21-amd64
 TCP加速方式       : bbr
 虚拟化架构        : KVM
 NAT类型           : 开放型
 IPV4 ASN          : AS210644 AEZA GROUP Ltd
 IPV4 位置         : Bergen / Vestland / NO
---------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分:           5374 Scores
 2 线程测试(多核)得分:          10676 Scores
---------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:          64011.41 MB/s
 单线程写测试:          30782.38 MB/s
------------------磁盘dd读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作               写速度                                  读速度
 100MB-4K Block         42.6 MB/s (10.40 IOPS, 2.46s))          41.5 MB/s (10128 IOPS, 2.53s)
 1GB-1M Block           2.3 GB/s (2168 IOPS, 0.46s)             958 MB/s (913 IOPS, 1.09s)
---------------------磁盘fio读写测试--感谢yabs开源----------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 40.01 MB/s   (10.0k) | 656.51 MB/s  (10.2k)
Write      | 40.11 MB/s   (10.0k) | 659.96 MB/s  (10.3k)
Total      | 80.12 MB/s   (20.0k) | 1.31 GB/s    (20.5k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 1.84 GB/s     (3.5k) | 1.81 GB/s     (1.7k)
Write      | 1.93 GB/s     (3.7k) | 1.93 GB/s     (1.8k)
Total      | 3.77 GB/s     (7.3k) | 3.75 GB/s     (3.6k)
---------------------流媒体解锁--感谢sjlleo开源-------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Google Global CacheCDN (ISP Cooperation)
ISP运营商: GIGANET
视频缓存节点地域: KBP(KBP9)
Youtube识别地域: 俄罗斯联邦(RU)
----------------Netflix----------------
[IPv4]
您的出口IP完整解锁Netflix，支持非自制剧的观看
NF所识别的IP地域信息：美国
[IPv6]
您的网络可能没有正常配置IPv6，或者没有IPv6网络接入
---------------DisneyPlus---------------
[IPv4]
当前IPv4出口解锁DisneyPlus
区域：美国区
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
----------------流媒体解锁--感谢RegionRestrictionCheck开源--------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:                                  Yes (Region: PL)
 HotStar:                               Yes (Region: US)
 Disney+:                               Yes (Region: US)
 Netflix:                               Yes (Region: US)
 YouTube Premium:                       No 
 Amazon Prime Video:                    Yes (Region: RU)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   INTL
 Viu.com:                               No
 YouTube CDN:                           GIGANET in Kiev 
 Netflix Preferred CDN:                 Stockholm  
 Spotify Registration:                  No
 Steam Currency:                        PLN
 ChatGPT:                               Yes
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
---------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:         【RU】
-------------------欺诈分数以及IP质量检测--本脚本原创-------------------
数据仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
以下为各数据库编号，输出结果后将自带数据库来源对应的编号
ipinfo数据库 ①  | scamalytics数据库 ②  | virustotal数据库 ③  | abuseipdb数据库 ④  | ip2location数据库   ⑤
ip-api数据库 ⑥  | ipwhois数据库     ⑦  | ipregistry数据库 ⑧  | ipdata数据库    ⑨  | ipgeolocation数据库 ⑩
欺诈分数(越低越好): 0②
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
黑名单记录统计(有多少个黑名单网站有记录): 无害0 恶意0 可疑0 未检测88 ③
Google搜索可行性：YES
端口25检测:
  本地: No
  163邮箱: Yes
  gmail邮箱: Yes
  yandex邮箱: Yes
  outlook邮箱: Yes
  qq邮箱: Yes
----------------三网回程--感谢zhanghanyun/backtrace开源-----------------
国家: NO 城市: Bergen 服务商: AS210644 AEZA GROUP Ltd
北京电信 219.141.136.12  测试超时
北京联通 202.106.50.1    测试超时
北京移动 221.179.155.161 测试超时
上海电信 202.96.209.133  测试超时
上海联通 210.22.97.1     测试超时
上海移动 211.136.112.200 测试超时
广州电信 58.60.188.222   测试超时
广州联通 210.21.196.6    测试超时
广州移动 120.196.165.24  测试超时
成都电信 61.139.2.69     测试超时
成都联通 119.6.6.6       测试超时
成都移动 211.137.96.205  测试超时
2023/09/11 06:01:05 测试完成!
---------------------回程路由--感谢fscarmen开源及PR---------------------
依次测试电信/联通/移动经过的地区及线路，核心程序来自ipip.net或nexttrace，请知悉!
广州电信 58.60.188.222
 
广州联通 210.21.196.6
0.10 ms         * RFC1918
27.71 ms        AS60068 美国 加利福尼亚州 洛杉矶 cdn77.com
28.34 ms        AS60068 美国 加利福尼亚州 洛杉矶 cdn77.com
207.93 ms       AS17623 [APNIC-AP] 中国 广东省 深圳市 宝安区 chinaunicom.cn 联通
广州移动 120.196.165.24
0.11 ms         * RFC1918
27.90 ms        AS60068 美国 加利福尼亚州 洛杉矶 cdn77.com
28.55 ms        AS60068 美国 加利福尼亚州 洛杉矶 cdn77.com
221.21 ms       AS56040 [APNIC-AP] 中国 广东省 深圳市 chinamobile.com 移动
--------------------自动更新测速节点列表--本脚本原创--------------------
位置             上传速度        下载速度        延迟     丢包率
Speedtest.net    775.09 Mbps     911.45 Mbps     163.98   0.0%
日本东京         777.22 Mbps     725.66 Mbps     126.92   NULL
法兰克福         592.85 Mbps     818.06 Mbps     147.50   0.0%
联通Fuzhou       429.55 Mbps     788.01 Mbps     215.09   0.0%
联通WuXi         368.06 Mbps     712.48 Mbps     214.66   0.7%
电信Suzhou5G     598.53 Mbps     820.30 Mbps     255.47   NULL
电信Nanjing5G    202.97 Mbps     669.07 Mbps     258.63   0.0%
移动Lanzhou      43.07 Mbps      3.79 Mbps       462.34   NULL
------------------------------------------------------------------------
 总共花费      : 7 分 7 秒
 时间          : Mon Sep 11 06:06:06 PDT 2023
------------------------------------------------------------------------
```

### SpeedTest

```

   Speedtest by Ookla

      Server: RETN - Warsaw (id: 32927)
         ISP: AEZA GROUP Ltd
Idle Latency:   160.20 ms   (jitter: 0.07ms, low: 160.06ms, high: 160.24ms)
    Download:   817.14 Mbps (data used: 1.3 GB)                                                   
                294.71 ms   (jitter: 75.76ms, low: 162.44ms, high: 907.63ms)
      Upload:   506.56 Mbps (data used: 690.7 MB)                                                   
                244.77 ms   (jitter: 69.34ms, low: 162.52ms, high: 326.71ms)
 Packet Loss:     0.0%
  Result URL: https://www.speedtest.net/result/c/97b6979e-b96f-4fc6-9d6b-1206c2ca7a8b
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-70-1024x395.png)

### 国内延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-69-1024x458.png)

### 全球延迟测试

![](https://catcat.blog/wp-content/uploads/2023/09/image-68-1024x615.png)
