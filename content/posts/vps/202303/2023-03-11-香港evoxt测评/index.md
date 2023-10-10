---
title: "香港evoxt测评（小众商家）"
date: "2023-03-11"
categories: 
  - "vps"
  - "hk"
tags: 
  - "hk"
---

> 香港vps evoxt.com，托管在 Mega2 机房中，共享 100Mbps 带宽。cpu有3.5 GHz 高频！

**官方网站：**[点我](https://console.evoxt.com/aff.php?aff=292) (优惠券 **AFF292-sayyiku** 可享 95 折)

**Looking Glass：**

- 美国： `103.179.142.254`

- 英国： `193.247.144.253`

- 马来西亚： `193.57.57.254`

- 香港：`154.91.202.254`

## 测试规格

香港 VM-3，每月 11.99 美金

![](https://catcat.blog/wp-content/uploads/2023/10/image-77.png)

## 基本配置

![](https://catcat.blog/wp-content/uploads/2023/10/image-79.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-80.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-81.png)

```
 CPU Model          : QEMU Virtual CPU version 2.5+
 CPU Cores          : 4 Core @ 3593.246 MHz
 CPU Cache          : 512 KB
 AES-NI             : ✘ Disabled
 VM-x/AMD-V         : ✘ Disabled
 Total Disk         : 1.5 GB / 29.8 GB
 Total Mem          : 71.2 MB / 3.8 GB
 System uptime      : 0 days, 0 hour 23 min
 Load average       : 0.00, 0.00, 0.00
 OS                 : Debian GNU/Linux 11 x86_64 (64 Bit)
 Kernel             : 5.10.0-8-amd64
 TCP CC             : cubic
 Virtualization     : KVM
```

## CPU 性能测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-82.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-83.png)

**CPU Events Per Second 跑分 (基于 sysbench)**

```
 -> CPU Performance Test (Standard Mode, 3-Pass @ 30sec)

 1 Thread Test:                 4040 Scores
 4 Threads Test:                16103 Scores
```

## 内存性能测试

```
 -> Memory Performance Test (Standard Mode, 3-Pass @ 30sec)

 1 Thread - Read Test :         48147.62 MB/s
 1 Thread - Write Test:         15673.12 MB/s
```

## 硬盘读写性能测试

**DD 硬盘测试：**

```
 Test Name              Write Speed                             Read Speed
 10MB-4K Block          65.0 MB/s (0.06 IOPS, 0.16s))           30.6 MB/s (7478 IOPS, 0.34s)
 10MB-1M Block          1.8 GB/s (1737 IOPS, 0.01s)             1.3 GB/s (1254 IOPS, 0.01s)
 100MB-4K Block         58.8 MB/s (0.07 IOPS, 1.78s))           25.3 MB/s (6185 IOPS, 4.14s)
 100MB-1M Block         2.1 GB/s (2036 IOPS, 0.05s)             2.0 GB/s (1902 IOPS, 0.05s)
 1GB-4K Block           59.6 MB/s (0.07 IOPS, 17.60s))          27.5 MB/s (6705 IOPS, 38.18s)
 1GB-1M Block           2.1 GB/s (2025 IOPS, 0.49s)             2.1 GB/s (1987 IOPS, 0.50s)
```

**FIO 硬盘测试：**

```
fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 464.49 MB/s (116.1k) | 1.68 GB/s    (26.2k)
Write      | 465.71 MB/s (116.4k) | 1.69 GB/s    (26.4k)
Total      | 930.20 MB/s (232.5k) | 3.37 GB/s    (52.6k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 2.08 GB/s     (4.0k) | 2.09 GB/s     (2.0k)
Write      | 2.19 GB/s     (4.2k) | 2.23 GB/s     (2.1k)
Total      | 4.28 GB/s     (8.3k) | 4.33 GB/s     (4.2k)
```

## 网络基本信息

```
 IP                 : 154.91.202.183
 Organization       : AS149440 Evoxt Enterprise
 Location           : Hong Kong / HK
 Region             : Central and Western
```

### 延迟测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-84.png)

### SpeedTest.net 测速

```
 Node Name                Upload Speed      Download Speed    Latency     Result      
 Speedtest.net            48.97 Mbps        20.89 Mbps        47.08 ms    https://www.speedtest.net/result/c/dd6191a6-5056-4ca7-b3da-e40fd10499de
 TW, Chunghwa Mobile      13.41 Mbps        60.00 Mbps        79.34 ms    https://www.speedtest.net/result/c/1ce3e803-3b38-4faa-97f2-f9dedd03ff97
 TW, Chief Telecom        16.19 Mbps        43.29 Mbps        59.42 ms    https://www.speedtest.net/result/c/3e8b0782-17d0-43be-bb45-771651760856
 TW, TAIFO                41.63 Mbps        39.87 Mbps        16.20 ms    https://www.speedtest.net/result/c/98c16bf4-4d21-4651-9c52-d14c74403ffe
 TW, DFT                  8.23 Mbps         11.58 Mbps        51.95 ms    https://www.speedtest.net/result/c/fbe69639-7e17-4a18-83d3-0cc1013d578c
 CN, Nanjing CT           0.46 Mbps         1.73 Mbps         46.51 ms    https://www.speedtest.net/result/c/b9ad8aea-0f56-463e-a58c-37f256163109
 CN, Hefei CT             0.43 Mbps         1.73 Mbps         40.69 ms    https://www.speedtest.net/result/c/0bf72c10-f8af-44ae-b5f2-082767a6545d
 CN, hanghai CU           3.16 Mbps         40.46 Mbps        318.56 ms   https://www.speedtest.net/result/c/ee92b1f0-0c35-4c2a-8ad6-d8ff6c0de651
 HK, HGC                  32.63 Mbps        40.88 Mbps        15.05 ms    https://www.speedtest.net/result/c/f0869565-a0ee-4e47-8f3a-f8bb2e0aa4c6
 HK, i3D.net              35.22 Mbps        82.44 Mbps        8.61 ms     https://www.speedtest.net/result/c/05184fa4-2b08-4fad-950b-0a2d909e9b64
 JP, i3D.net              38.58 Mbps        60.29 Mbps        43.17 ms    https://www.speedtest.net/result/c/736e5489-15a3-4a09-814b-5bc0fda651ad
 JP, fdcservers.net       14.53 Mbps        0.59 Mbps         183.36 ms   https://www.speedtest.net/result/c/454b6e06-942c-47c7-a3fd-eacd0627e880
 SG, i3D.net              17.16 Mbps        83.03 Mbps        39.44 ms    https://www.speedtest.net/result/c/b9f00b27-e48f-406b-90d4-fde115254359
 SG, NewMedia Express     53.61 Mbps        15.16 Mbps        39.00 ms    https://www.speedtest.net/result/c/15a72d5d-8384-4914-ba15-c03d80a42333
 SG, SuperInternet        24.40 Mbps        80.90 Mbps        38.72 ms    https://www.speedtest.net/result/c/07bf480e-a4c6-47a4-874e-f4e168cf8633
 MY, Telekom Malaysia     23.60 Mbps        10.04 Mbps        75.42 ms    https://www.speedtest.net/result/c/d8670fb5-d709-4788-96b9-3274c54e59b4
 MY, Celcom               6.76 Mbps         47.17 Mbps        65.51 ms    https://www.speedtest.net/result/c/ec541118-7b0d-4d6a-b5f1-a1b2a3f3cf83
 DE, GSL Networks         13.69 Mbps        42.55 Mbps        280.98 ms   https://www.speedtest.net/result/c/78a13125-9186-42c5-83b0-ba3bc8deab6e
 TR, Turkcell             15.41 Mbps        70.10 Mbps        211.26 ms   https://www.speedtest.net/result/c/cc567d9d-c5c1-4f16-963c-3c00a4071182
 TR, TurkNet              33.47 Mbps        28.31 Mbps        277.50 ms   https://www.speedtest.net/result/c/6c3f5056-31c4-496b-a432-520d5b884ab1
```

### iperf3

```
iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 35.9 Mbits/sec  | 22.2 Mbits/sec  | 204 ms         
Scaleway        | Paris, FR (10G)           | busy            | 2.10 Mbits/sec  | 235 ms         
NovoServe       | North Holland, NL (40G)   | 14.6 Mbits/sec  | 44.9 Mbits/sec  | 225 ms         
Uztelecom       | Tashkent, UZ (10G)        | busy            | 37.6 Mbits/sec  | 93.6 ms        
Clouvider       | NYC, NY, US (10G)         | 5.00 Mbits/sec  | 4.04 Mbits/sec  | 223 ms         
Clouvider       | Dallas, TX, US (10G)      | busy            | 7.30 Mbits/sec  | 251 ms         
Clouvider       | Los Angeles, CA, US (10G) | 3.34 Mbits/sec  | busy            | 150 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 26.5 Mbits/sec  | 31.0 Mbits/sec  | 203 ms         
Scaleway        | Paris, FR (10G)           | busy            | 605 Kbits/sec   |                
NovoServe       | North Holland, NL (40G)   | 28.5 Mbits/sec  | 73.1 Mbits/sec  | 219 ms         
Uztelecom       | Tashkent, UZ (10G)        | 31.4 Mbits/sec  | 45.9 Mbits/sec  | 91.0 ms        
Clouvider       | NYC, NY, US (10G)         | 28.3 Mbits/sec  | 3.86 Mbits/sec  | 220 ms         
Clouvider       | Dallas, TX, US (10G)      | 7.27 Mbits/sec  | 3.58 Mbits/sec  | 246 ms         
Clouvider       | Los Angeles, CA, US (10G) | 42.8 Mbits/sec  | 4.49 Mbits/sec  | 148 ms  
```

### 台湾路由跟踪

```
**  TW, Hinet ( 168.95.1.1) **

traceroute to 168.95.1.1 (168.95.1.1), 30 hops max, 32 byte packets
 1  154.91.202.1  6.70 ms  AS149440  China, Hong Kong, cloudinnovation.org
 2  45.204.17.251  25.85 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  63-216-83-161.static.pccwglobal.net (63.216.83.161)  11.53 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 6  HundredGE0-0-0-1.br06.hkg05.pccwbtn.net (63.223.31.218)  18.74 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 7  HundredGE0-0-0-1.br06.hkg05.pccwbtn.net (63.223.31.218)  11.13 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 8  63-218-56-102.static.pccwglobal.net (63.218.56.102)  61.53 ms  AS3491,AS31713  China, Taiwan, New Taipei City, pccw.com
 9  61-221-53-30.hinet-ip.hinet.net (61.221.53.30)  81.99 ms  AS3462  China, Taiwan, Taipei City, cht.com.tw
10  203-74-41-233.hinet-ip.hinet.net (203.74.41.233)  51.04 ms  AS3462  China, Taiwan, Taipei City, cht.com.tw
11  dns.hinet.net (168.95.1.1)  79.26 ms  AS3462  China, Taiwan, cht.com.tw

----------------------------------------------------------------------
**  TW, FETNet ( 139.175.1.1) **

traceroute to 139.175.1.1 (139.175.1.1), 30 hops max, 32 byte packets
 1  154.91.202.1  0.93 ms  AS149440  China, Hong Kong, cloudinnovation.org
 2  45.204.17.251  1.71 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  unknown.telstraglobal.net (210.176.141.93)  2.43 ms  AS4637  China, Hong Kong, telstra.com
 6  202.84.153.25  3.89 ms  AS4637  China, Hong Kong, telstra.com
 7  202.84.138.74  33.08 ms  AS4637  China, Taiwan, Taipei City, telstra.com
 8  i-92.tpei02.telstraglobal.net (202.84.137.250)  23.04 ms  AS4637  China, Taiwan, Taipei City, telstra.com
 9  unknown.telstraglobal.net (210.176.136.111)  15.24 ms  AS4637  China, Taiwan, Taipei City, telstra.com
10  r57-218.seed.net.tw (139.175.57.218)  15.50 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
11  *
12  frd01.seed.net.tw (139.175.1.1)  15.75 ms  AS4780  China, Taiwan, Taipei City, fetnet.net

----------------------------------------------------------------------
**  TW, APTG ( 203.79.224.10) **

traceroute to 203.79.224.10 (203.79.224.10), 30 hops max, 32 byte packets
 1  154.91.202.1  13.30 ms  AS149440  China, Hong Kong, cloudinnovation.org
 2  45.204.17.251  2.94 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  aptelecom1-10g.hkix.net (123.255.91.86)  2.49 ms  AS3491  China, Hong Kong, hkix.net
 6  43.240.106.24  18.33 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
 7  211.76.96.75  22.88 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
 8  IL203-79-251-46.static.apol.com.tw (203.79.251.46)  17.85 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
 9  192.168.125.1  18.32 ms  *  LAN Address
10  dns.octor.com (203.79.224.10)  17.42 ms  AS9311  China, Taiwan, Taipei City, aptg.com.tw

----------------------------------------------------------------------
**  TW, SoNET ( 61.64.127.1) **

traceroute to 61.64.127.1 (61.64.127.1), 30 hops max, 32 byte packets
 1  154.91.202.1  0.71 ms  AS149440  China, Hong Kong, cloudinnovation.org
 2  45.204.17.251  1.42 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  donghwa3-10g.hkix.net (123.255.91.131)  16.27 ms  AS3491  China, Hong Kong, hkix.net
 6  175-41-60-89.twgate-ip.twgate.net (175.41.60.89)  32.18 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 7  203-78-181-222.twgate-ip.twgate.net (203.78.181.222)  21.89 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 8  175-41-63-86.twgate-ip.twgate.net (175.41.63.86)  19.61 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 9  219.84.176.118  19.26 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
10  219.84.176.138  218.54 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
11  *
12  gw.so-net.net.tw (61.64.127.249)  19.99 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
13  gw.so-net.net.tw (61.64.127.249)  46.37 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
14  ns1.so-net.net.tw (61.64.127.1)  21.10 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw

----------------------------------------------------------------------
**  TW, TFN ( 219.87.66.1) **

traceroute to 219.87.66.1 (219.87.66.1), 30 hops max, 32 byte packets
 1  154.91.202.1  0.84 ms  AS149440  China, Hong Kong, cloudinnovation.org
 2  45.204.17.251  9.35 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  donghwa3-10g.hkix.net (123.255.91.131)  2.72 ms  AS3491  China, Hong Kong, hkix.net
 6  175-41-60-57.twgate-ip.twgate.net (175.41.60.57)  16.59 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 7  175-41-61-182.twgate-ip.twgate.net (175.41.61.182)  17.03 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 8  175-41-60-174.twgate-ip.twgate.net (175.41.60.174)  47.87 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 9  60-199-14-242.static.tfn.net.tw (60.199.14.242)  48.28 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
10  219-87-66-1.static.tfn.net.tw (219.87.66.1)  49.70 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com

----------------------------------------------------------------------
**  TW,TAIFO ( 103.31.196.1) **

traceroute to 103.31.196.1 (103.31.196.1), 30 hops max, 32 byte packets
 1  154.91.202.1  0.70 ms  AS149440  China, Hong Kong, cloudinnovation.org
 2  45.204.17.251  1.29 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  *
 6  133-253-123-103-static.chief.net.tw (103.123.253.133)  19.17 ms  *  China, Taiwan, Taipei City, chief.com.tw
 7  141-64-26-223-static.chief.net.tw (223.26.64.141)  52.74 ms  *  China, Taiwan, Taipei City, chief.com.tw
 8  209-84-21-113-static.chief.net.tw (113.21.84.209)  25.46 ms  *  China, Taiwan, Taipei City, chief.com.tw
 9  210-84-21-113-static.chief.net.tw (113.21.84.210)  15.79 ms  *  China, Taiwan, Taipei City, chief.com.tw
10  103.31.197.122  17.24 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
11  *
12  103.31.197.70  29.38 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
13  103.31.196.1  18.91 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
```

### 中国区域路由跟踪

```
**  北京电信 ( 219.141.147.210) **

traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  154.91.202.1  0.63 ms  AS149440  China, Hong Kong, cloudinnovation.org
 2  45.204.17.251  1.13 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  121.59.100.237  10.44 ms  AS23764  China, Hong Kong, ChinaTelecom
 6  *
 7  203.22.178.102  35.80 ms  *  China, Hong Kong, ChinaTelecom
 8  59.43.249.54  39.84 ms  *  China, Beijing, ChinaTelecom
 9  59.43.132.13  40.55 ms  *  China, Beijing, ChinaTelecom
10  *
11  *
12  6.254.120.106.static.bjtelecom.net (106.120.254.6)  39.35 ms  AS4847  China, Beijing, ChinaTelecom
13  *
14  bj141-147-210.bjtelecom.net (219.141.147.210)  50.44 ms  AS4847  China, Beijing, ChinaTelecom

----------------------------------------------------------------------
**  上海电信 ( 202.96.209.133) **

traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  *
 2  45.204.17.251  18.34 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  121.59.100.81  7.41 ms  AS23764  China, Hong Kong, ChinaTelecom
 6  69.194.186.217  6.58 ms  AS32505  United States, Louisiana, conterra.com
 7  203.22.178.86  26.13 ms  *  China, Hong Kong, ChinaTelecom
 8  59.43.38.169  26.23 ms  *  China, Shanghai, ChinaTelecom
 9  59.43.138.49  57.27 ms  *  China, Shanghai, ChinaTelecom
10  101.95.88.174  51.04 ms  AS4812  China, Shanghai, ChinaTelecom
11  *
12  ns-pd.online.sh.cn (202.96.209.133)  51.21 ms  AS4812  China, Shanghai, ChinaTelecom

----------------------------------------------------------------------
**  深圳电信 ( 58.60.188.222) **

traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  *
 2  45.204.17.251  10.29 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  121.59.100.237  13.55 ms  AS23764  China, Hong Kong, ChinaTelecom
 6  69.194.165.153  36.49 ms  AS23764  China, Hong Kong, ChinaTelecom
 7  *
 8  59.43.250.109  35.55 ms  *  China, Guangdong, Guangzhou, ChinaTelecom
 9  59.43.130.145  28.00 ms  *  China, Guangdong, Guangzhou, ChinaTelecom
10  59.43.132.126  32.94 ms  *  China, Guangdong, Guangzhou, ChinaTelecom
11  118.104.38.59.broad.fs.gd.dynamic.163data.com.cn (59.38.104.118)  37.03 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
12  *
13  58.60.188.222  17.76 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom

----------------------------------------------------------------------
**  北京联通 ( 202.106.50.1) **

traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  *
 2  45.204.17.251  16.09 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  202.77.19.169  4.87 ms  AS10099  China, Hong Kong, ChinaUnicom
 6  202.77.18.194  15.21 ms  AS10099  China, Hong Kong, ChinaUnicom
 7  202.77.23.25  19.80 ms  AS10099  China, Hong Kong, ChinaUnicom
 8  219.158.10.49  15.45 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
 9  219.158.4.33  35.26 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
10  219.158.3.125  12.91 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
11  *
12  *
13  202.106.50.1  47.97 ms  AS4808  China, Beijing, ChinaUnicom

----------------------------------------------------------------------
**  上海联通 ( 210.22.97.1) **

traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  154.91.202.1  12.21 ms  AS149440  China, Hong Kong, cloudinnovation.org
 2  45.204.17.251  19.69 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  202.77.19.169  11.25 ms  AS10099  China, Hong Kong, ChinaUnicom
 6  202.77.18.194  9.15 ms  AS10099  China, Hong Kong, ChinaUnicom
 7  43.252.86.129  9.42 ms  AS10099  China, Hong Kong, ChinaUnicom
 8  219.158.20.97  40.67 ms  AS4837  China, Hong Kong, ChinaUnicom
 9  219.158.24.133  23.05 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
10  *
11  219.158.7.41  57.90 ms  AS4837  China, Shanghai, ChinaUnicom
12  *
13  112.64.250.202  49.73 ms  AS17621  China, Shanghai, ChinaUnicom
14  210.22.97.1  53.29 ms  AS17621  China, Shanghai, ChinaUnicom

----------------------------------------------------------------------
**  深圳联通 ( 210.21.196.6) **

traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  *
 2  45.204.17.251  1.22 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  202.77.19.169  2.57 ms  AS10099  China, Hong Kong, ChinaUnicom
 6  202.77.18.194  8.82 ms  AS10099  China, Hong Kong, ChinaUnicom
 7  202.77.23.25  11.53 ms  AS10099  China, Hong Kong, ChinaUnicom
 8  219.158.10.53  10.93 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
 9  219.158.98.93  14.28 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
10  *
11  *
12  120.80.144.38  17.88 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
13  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  11.32 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom

----------------------------------------------------------------------
**  北京移动 ( 221.179.155.161) **

traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  *
 2  45.204.17.251  23.38 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  103.106.248.5  16.53 ms  *  Malaysia, 1maxhosting.com
 6  223.118.2.177  24.24 ms  AS58453  China, Hong Kong, ChinaMobile
 7  223.120.22.29  57.24 ms  AS58453  China, Guangdong, Guangzhou, ChinaMobile
 8  221.183.55.106  59.82 ms  AS9808  China, Beijing, ChinaMobile
 9  221.183.46.250  52.47 ms  AS9808  China, Beijing, ChinaMobile
10  221.183.89.102  76.70 ms  AS9808  China, Beijing, ChinaMobile
11  221.183.46.178  59.58 ms  AS9808  China, Beijing, ChinaMobile
12  *
13  cachedns03.bj.chinamobile.com (221.179.155.161)  50.79 ms  AS56048  China, Beijing, ChinaMobile

----------------------------------------------------------------------
**  深圳移动 ( 120.196.165.24) **

traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  154.91.202.1  0.86 ms  AS149440  China, Hong Kong, cloudinnovation.org
 2  45.204.17.251  2.00 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  103.106.248.5  21.67 ms  *  Malaysia, 1maxhosting.com
 6  223.118.2.177  14.25 ms  AS58453  China, Hong Kong, ChinaMobile
 7  *
 8  221.183.68.125  7.68 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
 9  221.183.52.85  13.41 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
10  221.176.24.5  23.33 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
11  111.24.5.165  16.88 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
12  221.183.71.74  13.11 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
13  221.183.110.170  23.36 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
14  ns6.gd.cnmobile.net (120.196.165.24)  16.34 ms  AS56040  China, Guangdong, Shenzhen, ChinaMobile

----------------------------------------------------------------------
**  成都教育网 ( 202.112.14.151) **

traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  *
 2  45.204.17.251  1.46 ms  AS55720  China, Hong Kong, cloudinnovation.org
 3  *
 4  *
 5  121.59.100.81  9.84 ms  AS23764  China, Hong Kong, ChinaTelecom
 6  69.194.165.153  15.98 ms  AS23764  China, Hong Kong, ChinaTelecom
 7  *
 8  59.43.181.93  17.50 ms  *  China, Guangdong, Guangzhou, ChinaTelecom
 9  59.43.16.165  12.77 ms  *  China, Guangdong, Guangzhou, ChinaTelecom
10  *
11  *
12  202.97.15.90  48.33 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
13  101.4.117.217  56.49 ms  AS4538  China, Shanghai, CHINAEDU
14  101.4.116.90  61.57 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
15  *
16  *
17  *
18  202.112.14.151  63.45 ms  AS24355  China, Sichuan, Chengdu, CHINAEDU
```

## 流媒体解锁

```
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: MY)
 Amazon Prime Video:                    Yes (Region: HK)
 TVBAnywhere+:                          No
 iQyi Oversea Region:                   HK
 Viu.com:                               Yes (Region: HK)
 YouTube CDN:                           Hong Kong 
 Netflix Preferred CDN:                 Singapore  
 Spotify Registration:                  No
 Steam Currency:                        HKD
=======================================
==============[ Taiwan ]===============
 KKTV:                                  No
 LiTV:                                  No
 MyVideo:                               No
 4GTV.TV:                               No
 LineTV.TW:                             No
 Hami Video:                            No
 CatchPlay+:                            No
 HBO GO Asia:                           Yes (Region: HK)
 Bahamut Anime:                         Failed (Network Connection)
 Bilibili Taiwan Only:                  No
=======================================
=============[ Hong Kong ]=============
 Now E:                                 Yes
 Viu.TV:                                Yes
 MyTVSuper:                             No
 HBO GO Asia:                           Yes (Region: HK)
 BiliBili Hongkong/Macau/Taiwan:        Yes
=======================================
===============[ Japan ]===============
 DMM:                                   No
 DMM TV:                                No
 Abema.TV:                              No
 Niconico:                              No
 music.jp:                              No
 Telasa:                                No
 Paravi:                                No
 U-NEXT:                                No
 Hulu Japan:                            Yes
 TVer:                                  Yes
 GYAO!:                                 No
 WOWOW:                                 Failed
 VideoMarket:                           No
 FOD(Fuji TV):                          No
 Radiko:                                No
 Karaoke@DAM:                           No
 J:com On Demand:                       No
 ---Game---
 Kancolle Japan:                        No
 Pretty Derby Japan:                    No
 Konosuba Fantastic Days:               No
 Princess Connect Re:Dive Japan:        No
 World Flipper Japan:                   No
 Project Sekai: Colorful Stage:         No
=======================================
===========[ North America ]===========
 FOX:                                   No
 Hulu:                                  Failed
 NFL+:                                  No
 ESPN+:[Sponsored by Jam]               No
 Epix:                                  No
 Starz:                                 No
 Philo:                                 No
 FXNOW:                                 No
 TLC GO:                                No
 HBO Max:                               No
 Shudder:                               No
 BritBox:                               Yes
 Crackle:                               No
 CW TV:                                 No
 A&E TV:                                No
 NBA TV:                                Yes
 NBC TV:                                No
 Fubo TV:                               No
 Tubi TV:                               No
 Sling TV:                              Yes
 Pluto TV:                              Yes
 Acorn TV:                              Yes
 SHOWTIME:                              Yes
 encoreTVB:                             No
 Funimation:                            No
 Discovery+:                            No
 Paramount+:                            No
 Peacock TV:                            No
 Popcornflix:                           No
 Crunchyroll:                           No
 Directv Stream:                        No
 KBS American:                          No
 KOCOWA:                                No
 Maths Spot:                            Failed
 ---CA---
 CBC Gem:                               No
 Crave:                                 Yes
=======================================
===========[ South America ]===========
 Star+:                                 No
 HBO Max:                               No
 DirecTV Go:                            Yes (Region: REGISTRARSE)
 Funimation:                            No
=======================================
===============[ Europe ]==============
 Rakuten TV:                            Yes
 Funimation:                            No
 SkyShowTime:                           No
 HBO Max:                               No
 Maths Spot:                            Failed
 ---GB---
 Sky Go:                                No
 BritBox:                               Yes
 ITV Hub:                               No
 Channel 4:                             No
 Channel 5:                             No
 BBC iPLAYER:                           No
 Discovery+ UK:                         No
 ---FR---
 Salto:                                 No
 Canal+:                                No
 Molotov:                               No
 ---DE---
 Joyn:                                  No
 Sky:                                   No
 ZDF:                                   No
 ---NL---
 NLZIET:                                Failed
 videoland:                             Failed (Network Connection)
 NPO Start Plus:                        No
 ---ES---
 PANTAYA:                               No
 ---IT---
 Rai Play:                              Yes
 ---RU---
 Amediateka:                            Yes
=======================================
==============[ Oceania ]==============
 NBA TV:                                Yes
 Acorn TV:                              Yes
 SHOWTIME:                              Yes
 BritBox:                               Yes
 Funimation:                            No
 Paramount+:                            No
 ---AU---
 Stan:                                  Yes
 Binge:                                 No
 Docplay:                               No
 7plus:                                 No
 Channel 9:                             No
 Channel 10:                            No
 ABC iView:                             No
 Kayo Sports:                           No
 Optus Sports:                          No
 SBS on Demand:                         No
 ---NZ---
 Neon TV:                               Yes
 SkyGo NZ:                              Failed (Unexpected Result: 401)
 ThreeNow:                              No
 Maori TV:                              Yes
=======================================
==============[ Korean ]===============
 Wavve:                                 No
 Tving:                                 No
 Coupang Play:                          No
 Naver TV:                              No
 Afreeca TV:                            Yes
 KBS Domestic:                          No
=======================================
```
