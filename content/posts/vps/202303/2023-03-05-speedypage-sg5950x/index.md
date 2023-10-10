---
title: "SpeedyPage 新加坡5950x测评"
date: "2023-03-05"
categories: 
  - "vps"
  - "sg"
tags: 
  - "sg"
---

## 1.官方网站

官网：[地址](https://urls.catcat.blog/speedypage)

![](https://catcat.blog/wp-content/uploads/2023/10/image-93.png)

## 2.套餐价格

### 优惠码：**LET10OFF** 

![](https://catcat.blog/wp-content/uploads/2023/10/image-94.png)

<table><tbody><tr><td class="has-text-align-center" data-align="center"><strong>Ryzen 5950X CoresCPU</strong></td><td><strong>内存</strong></td><td>NVME</td><td><strong>Bandwidth @ 2.5Gbps</strong></td><td><strong>IPv4 | IPv6</strong></td><td>折前价格</td><td>购买</td></tr><tr><td class="has-text-align-center" data-align="center">1 5950X Cores</td><td>1g</td><td>15</td><td>1 TB @ 10 Gbps</td><td>1 IPv4 &amp; /64 IPv6</td><td><strong>£3.50/mo</strong></td><td><a href="https://my.speedypage.com/store/sg-vps&amp;aff=190" target="_blank" rel="noreferrer noopener">地址</a></td></tr><tr><td class="has-text-align-center" data-align="center">1 5950X Cores</td><td>2g</td><td>30</td><td>1 TB @ 10 Gbps</td><td>1 IPv4 &amp; /64 IPv6</td><td><strong>£4.99/mo</strong></td><td><a href="https://my.speedypage.com/store/sg-vps&amp;aff=190" target="_blank" rel="noreferrer noopener">地址</a></td></tr><tr><td class="has-text-align-center" data-align="center">2 5950X Cores</td><td>4g</td><td>60</td><td>2 TB @ 10 Gbps</td><td>1 IPv4 &amp; /64 IPv6</td><td><strong>£9.99/mo</strong></td><td><a href="https://my.speedypage.com/store/sg-vps&amp;aff=190" target="_blank" rel="noreferrer noopener">地址</a></td></tr><tr><td class="has-text-align-center" data-align="center">3 5950X Cores</td><td>6g</td><td>90</td><td>3 TB @ 10 Gbps</td><td>1 IPv4 &amp; /64 IPv6</td><td><strong><strong>£</strong>12.99/mo</strong></td><td><a href="https://my.speedypage.com/store/sg-vps&amp;aff=190" target="_blank" rel="noreferrer noopener">地址</a></td></tr><tr><td class="has-text-align-center" data-align="center">4 5950X Cores</td><td>8g</td><td>120</td><td>4 TB @ 10 Gbps</td><td>1 IPv4 &amp; /64 IPv6</td><td><strong>£14.99/mo</strong></td><td><a href="https://my.speedypage.com/store/sg-vps&amp;aff=190" target="_blank" rel="noreferrer noopener">地址</a></td></tr><tr><td class="has-text-align-center" data-align="center">4 5950X Cores</td><td>10g</td><td>150</td><td>5 TB @ 10 Gbps</td><td>1 IPv4 &amp; /64 IPv6</td><td><strong>£19.99/mo</strong></td><td><a href="https://my.speedypage.com/store/sg-vps&amp;aff=190" target="_blank" rel="noreferrer noopener">地址</a></td></tr></tbody></table>

## 3\. VPS 测试（1C1G）

![](https://catcat.blog/wp-content/uploads/2023/10/image-96.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-97.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-98.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-100.png)

## 4.Ping 值

#### TCP路由测试

去程: 电信/联通 绕日本(ntt), 移动经香港直连(telstra)  
回程: 电信绕美(cogent), 联通绕日本(ntt), 移动经香港直连(ntt)  
测试IP: 194.9.62.3

Looking Glass: [https://sg.lg.speedypage.com/](https://sg.lg.speedypage.com/)

![](https://catcat.blog/wp-content/uploads/2023/10/image-95.png)

## 5.融合怪脚本测试

```
-----------------感谢teddysun和superbench和yabs开源-------------------
 CPU 型号          : AMD Ryzen 9 5950X 16-Core Processor
 CPU 核心数        : 1
 CPU 频率          : 3393.622 MHz
 CPU 缓存          : 512 KB
 硬盘空间          : 15.0 GB (1.5 GB 已用)
 内存              : 943 MB (134 MB 已用)
 Swap              : 0 MB (0 MB 已用)
 系统在线时间      : 0 days, 0 hour 1 min
 负载              : 1.16, 0.58, 0.22
 系统              : Debian GNU/Linux 11 (bullseye)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-10-amd64
 TCP加速方式       : cubic
 虚拟化架构        : KVM
 ASN组织           : AS142594 SpeedyPage Ltd
 位置              : Singapore / SG
 地区              : Singapore
-------------------CPU测试--感谢lemonbench开源------------------------
 -> CPU 测试中 (Fast Mode, 1-Pass @ 5sec)
 1 线程测试(1核)得分: 		5313 Scores
-------------------内存测试--感谢lemonbench开源-----------------------
 -> 内存测试 Test (Fast Mode, 1-Pass @ 5sec)
 单线程读测试:		59898.46 MB/s
 单线程写测试:		30003.82 MB/s
----------------磁盘IO读写测试--感谢lemonbench开源--------------------
 -> 磁盘IO测试中 (4K Block/1M Block, Direct Mode)
 测试操作		写速度					读速度
 100MB-4K Block		->
 100MB-4K Block		104 MB/s (0.04K IOPS, 1.01s)		->
 100MB-4K Block		104 MB/s (0.04 IOPS, 1.01s)		143 MB/s (34900 IOPS, 0.73s)
 1GB-1M Block		->
 1GB-1M Block		844 MB/s (804 IOPS, 1.24s)		->
 1GB-1M Block		844 MB/s (804 IOPS, 1.24s)		4.6 GB/s (4402 IOPS, 0.23s)
-------------------磁盘IO读写测试--感谢yabs开源-----------------------
  ------ | --- ---- | ---- ---- 
Read       | 440.27 MB/s (110.0k) | 2.35 GB/s    (36.7k)
Write      | 441.43 MB/s (110.3k) | 2.36 GB/s    (36.9k)
Total      | 881.71 MB/s (220.4k) | 4.71 GB/s    (73.7k)           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.15 GB/s     (4.2k) | 2.12 GB/s     (2.0k)
Write      | 2.26 GB/s     (4.4k) | 2.26 GB/s     (2.2k)
Total      | 4.41 GB/s     (8.6k) | 4.39 GB/s     (4.2k)
--------------------流媒体解锁--感谢sjlleo开源------------------------
以下测试的解锁地区是准确的，但是不是完整解锁的判断可能有误，这方面仅作参考使用
----------------Youtube----------------
[IPv4]
连接方式: Youtube Video Server
视频缓存节点地域: 新加坡 新加坡/樟宜  (SIN11S18)
Youtube识别地域: 荷兰(NL)
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
解锁Youtube，Netflix，DisneyPlus上面和下面进行比较，不同之处自行判断
---------------流媒体解锁--感谢RegionRestrictionCheck开源-------------
 以下为IPV4网络测试，若无IPV4网络则无输出
============[ Multination ]============
 Dazn:					No
 HotStar:				Yes (Region: SG)
 Disney+:				No
 Netflix:				Yes (Region: SG)
 YouTube Premium:			Yes (Region: NL)
 Amazon Prime Video:			Yes (Region: SG)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			SG
 Viu.com:				Yes (Region: SG)
 YouTube CDN:				Singapore 
 Netflix Preferred CDN:			Singapore  
 Spotify Registration:			No
 Steam Currency:			SGD
=======================================
 以下为IPV6网络测试，若无IPV6网络则无输出
-------------TikTok解锁--感谢lmc999的源脚本及fscarmen PR--------------
 Tiktok Region:		【GB】
--------OpenAi解锁--感谢missuo的OpenAI-Checker项目本人修改优化--------
[IPv4]
Your IP supports access to OpenAI. Region: SG
[IPv6]
IPv6 is not supported on the current host. Skip...
-----------------欺诈分数以及IP质量检测--本频道原创-------------------
以下仅作参考，不代表100%准确，如果和实际情况不一致请手动查询多个数据库比对
scamalytics数据库:
  欺诈分数(越低越好)：82
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
  数据中心: No
abuseipdb数据库-abuse得分：0
IP类型:
  IP2Location数据库: Data Center/Web Hosting/Transit
Google搜索可行性：YES
-----------------三网回程--感谢zhanghanyun/backtrace开源--------------
2023/04/20 08:12:03 北京电信 219.141.136.12  电信163 [普通线路]           
2023/04/20 08:12:03 北京联通 202.106.50.1    联通4837[普通线路]           
2023/04/20 08:12:03 北京移动 221.179.155.161 移动CMI [普通线路]           
2023/04/20 08:12:03 上海电信 202.96.209.133  测试超时
2023/04/20 08:12:03 上海联通 210.22.97.1     联通4837[普通线路]           
2023/04/20 08:12:03 上海移动 211.136.112.200 移动CMI [普通线路]           
2023/04/20 08:12:03 广州电信 58.60.188.222   电信163 [普通线路]           
2023/04/20 08:12:03 广州联通 210.21.196.6    联通4837[普通线路]           
2023/04/20 08:12:03 广州移动 120.196.165.24  移动CMI [普通线路]           
2023/04/20 08:12:03 成都电信 61.139.2.69     电信163 [普通线路]           
2023/04/20 08:12:03 成都联通 119.6.6.6       联通4837[普通线路]           
2023/04/20 08:12:03 成都移动 211.137.96.205  移动CMI [普通线路]           
------------------回程路由--感谢fscarmen开源及PR----------------------
IPv4 ASN: SpeedyPage Ltd
依次测试电信，联通，移动经过的地区及线路，核心程序来由: ipip.net ，请知悉!
广州电信 58.60.188.222
0.22 ms  AS136557  新加坡, hostuniversal.com.au
0.99 ms  AS174  新加坡, cogentco.com
1.46 ms  AS174  新加坡, cogentco.com
1.65 ms  AS174  新加坡, cogentco.com
166.90 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
182.16 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
194.61 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
195.42 ms  AS174  美国, 加利福尼亚州, 圣何塞, cogentco.com
345.65 ms  AS4134  中国, 广东, 广州, chinatelecom.com.cn, 电信
350.11 ms  AS134774  中国, 广东, 深圳, chinatelecom.com.cn, 电信
350.37 ms  AS4134  中国, 广东, 深圳, chinatelecom.com.cn, 电信
广州联通 210.21.196.6
0.25 ms  AS136557  新加坡, hostuniversal.com.au
1.13 ms  AS174  新加坡, cogentco.com
1.29 ms  AS174  新加坡, cogentco.com
1.47 ms  AS174  新加坡, cogentco.com
166.87 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
167.43 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
173.75 ms  AS174  美国, 加利福尼亚州, 洛杉矶, cogentco.com
182.87 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
188.32 ms  AS4837  中国, 广东, 广州, chinaunicom.com, 联通
194.95 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
190.49 ms  AS17623  中国, 广东, 深圳, chinaunicom.com, 联通
广州移动 120.196.165.2
0.24 ms  AS136557  新加坡, hostuniversal.com.au
0.96 ms  AS136557  新加坡, hostuniversal.com.au
0.95 ms  AS60068  欧洲地区, datacamp.co.uk
1.50 ms  AS2914  新加坡, ntt.com
32.06 ms  AS2914  新加坡, ntt.com
31.70 ms  AS58453  中国, 香港, chinamobile.com, 移动
58.52 ms  AS58453  中国, 上海, chinamobile.com, 移动
57.33 ms  AS9808  中国, 上海, chinamobile.com, 移动
90.58 ms  AS56040  中国, 广东, 广州, chinamobile.com, 移动
91.44 ms  AS56040  中国, 广东, 广州, chinamobile.com, 移动
92.77 ms  AS56040  中国, 广东, 深圳, chinamobile.com, 移动
------------------------ ecs-net--本频道独创 -------------------------
位置		 上传速度	 下载速度	 延迟	  丢包率
Speedtest.net	 7667.02 Mbps	 6847.46 Mbps	 0.28	  0.0%
洛杉矶		 519.67 Mbps	 2191.66 Mbps	 194.50	  0.0%
新加坡		 6601.48 Mbps	 6932.77 Mbps	 1.98	  0.0%
联通Fuzhou	 409.34 Mbps	 4163.37 Mbps	 51.11	  0.0%
电信Suzhou5G	 308.98 Mbps	 1481.49 Mbps	 317.54	  NULL
电信合肥5G	 49.47 Mbps	 27.24 Mbps	 330.03	  0.0%
移动杭州5G	 810.04 Mbps	 3237.12 Mbps	 72.88	  0.0%
移动陕西5G	 584.00 Mbps	 2947.81 Mbps	 94.35	  0.0%
----------------------------------------------------------------------
 总共花费      : 5 分 37 秒
 时间          : Thu 20 Apr 2023 08:16:32 AM CST
----------------------------------------------------------------------
```

## 7.测评总结

配置/国际互联还算不错, G口带宽, 提供IPv4+IPv6, 新加坡上游为HostUniversal.  
国内tcp ping平均: 电信537ms,联通136ms,移动86ms.自带备份和ddos，适合建站  
适合移动用户直连, 或者 IPLC/香港机/新加机中转使用.  
除了不太适合直连外, 其他都感觉还不错.

自带备份和ddos，适合建站
