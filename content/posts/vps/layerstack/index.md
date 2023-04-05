---
title: "香港主机 layerstack.com (ARM)"
date: "2023-03-22"
categories: 
  - "vps"
featuredImage: https://cdn.lirica.cn/webp/00002.webp
license: CC BY-NC-SA 4.0

hiddenFromHomePage: false
hiddenFromSearch: false
---

这次拿到了他的 ARM ，可以到他官网看看（[点我](https://www.layerstack.com/zh-tw/arm-based-cloud-server)），价格便宜很多。

**官方网站：[点我](https://www.layerstack.com/)**

**Looking Glass：**

- 新加坡：[https://sg01.layerstack.com/](https://sg01.layerstack.com/)

- 日本：[https://jp01.layerstack.com/](https://jp01.layerstack.com/)

- 香港：[https://hk03.layerstack.com/](https://hk03.layerstack.com/)

- 洛杉矶：[https://la01.layerstack.com/](https://la01.layerstack.com/)

## 测试规格

ARM008 香港，2 核 4G 搭配 50GB SSD ，一个月 8刀

[![](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fkangjw.me%2Fwp-content%2Fuploads%2F2023%2F03%2Fimage-16-2048x843.png)](https://kangjw.me/wp-content/uploads/2023/03/image-16.png)

## 服务器基本信息

```
 CPU Model          : CPU model not detected
 CPU Cores          : 2
 AES-NI             : ✓ Enabled
 VM-x/AMD-V         : ✘ Disabled
 Total Disk         : 2.4 GB / 47.1 GB
 Total Mem          : 137.2 MB / 3.8 GB
 Total Swap         : 0 / 2.0 GB
 System uptime      : 0 days, 0 hour 1 min
 Load average       : 0.08, 0.03, 0.00
 OS                 : Ubuntu 20.04.4 LTS aarch64 (64 Bit)
 Kernel             : 5.15.0-46-generic
 TCP CC             : cubic
 Virtualization     : KVM
```

## CPU性能

[![](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fkangjw.me%2Fwp-content%2Fuploads%2F2023%2F03%2Fimage-17.png)](https://kangjw.me/wp-content/uploads/2023/03/image-17.png)

**GeekBench5 测试：**[https://browser.geekbench.com/v5/cpu/20910246](https://browser.geekbench.com/v5/cpu/20910246)

**GeekBench4 测试：**ARM 不支援 GB4 测试

**CPU Events Per Second 跑分(基于sysbench)**

```
 1 Thread Test:                 3508 Scores
 2 Threads Test:                7020 Scores
```

```
 1 Thread - Read Test :         30915.43 MB/s
 1 Thread - Write Test:         14653.77 MB/s
```

## 硬盘性能

**DD 硬盘結果：**

```
 Test Name              Write Speed                             Read Speed
 10MB-4K Block          96.0 MB/s (0.04 IOPS, 0.11s))           116 MB/s (28243 IOPS, 0.09s)
 10MB-1M Block          3.1 GB/s (2972 IOPS, 0.00s)             2.5 GB/s (2358 IOPS, 0.00s)
 100MB-4K Block         99.4 MB/s (0.04 IOPS, 1.06s))           112 MB/s (27242 IOPS, 0.94s)
 100MB-1M Block         4.2 GB/s (4000 IOPS, 0.02s)             4.1 GB/s (3904 IOPS, 0.03s)
 1GB-4K Block           81.4 MB/s (0.05 IOPS, 12.89s))          112 MB/s (27437 IOPS, 9.33s)
 1GB-1M Block           1.6 GB/s (1495 IOPS, 0.67s)             4.2 GB/s (4008 IOPS, 0.25s)
```

**FIO 結果：**

```
fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 347.09 MB/s  (86.7k) | 2.66 GB/s    (41.6k)
Write      | 346.86 MB/s  (86.7k) | 2.74 GB/s    (42.8k)
Total      | 693.96 MB/s (173.4k) | 5.40 GB/s    (84.4k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.14 GB/s     (6.1k) | 3.41 GB/s     (3.3k)
Write      | 3.41 GB/s     (6.6k) | 3.81 GB/s     (3.7k)
Total      | 6.55 GB/s    (12.7k) | 7.23 GB/s     (7.0k)
```

## 网络

```
 IP                 : 103.231.254.200
 Organization       : AS133380 Layerstack Limited
 Location           : Hong Kong / HK
 Region             : Central and Western
```

### 全球延迟

![](https://cdn.lirica.cn/wordpress/2023/03/image-19-2048x2153.png)

### SpeedTest.net 测速

![](https://cdn.lirica.cn/wordpress/2023/03/82120.png)

### 台湾路由追踪

##### Hinet 168.95.1.1

```
traceroute to 168.95.1.1 (168.95.1.1), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.63 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  ve336.core2.hkg2.he.net (74.82.49.173)  0.64 ms  AS6939  China, Hong Kong, he.net
 3  *
 4  *
 5  *
 6  3462-sg1-ix.equinix.com (27.111.230.125)  35.44 ms  AS3491  Singapore, equinix.com
 7  220-128-6-194.hinet-ip.hinet.net (220.128.6.194)  75.01 ms  *  China, Taiwan, Taipei City, cht.com.tw
 8  tpdt-3032.hinet.net (220.128.2.14)  77.20 ms  *  China, Taiwan, Taipei City, cht.com.tw
 9  tpdb-3311.hinet.net (220.128.2.253)  75.31 ms  *  China, Taiwan, Taipei City, cht.com.tw
10  210-59-204-217.hinet-ip.hinet.net (210.59.204.217)  75.83 ms  AS3462  China, Taiwan, Taipei City, cht.com.tw
11  220-128-32-69.hinet-ip.hinet.net (220.128.32.69)  76.75 ms  AS3462  China, Taiwan, cht.com.tw
12  dns.hinet.net (168.95.1.1)  75.33 ms  AS3462  China, Taiwan, cht.com.tw
```

##### FENTNet 139.175.1.1

```
traceroute to 139.175.1.1 (139.175.1.1), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  2.78 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  10.40.40.204  0.39 ms  *  LAN Address
 3  172.29.29.21  0.60 ms  *  LAN Address
 4  27.111.196.245  0.45 ms  AS17819  China, Hong Kong, equinix.com
 5  xe-2-0-1-gw701.hk2.ap.equinix.com (36.255.38.170)  0.50 ms  *  China, Hong Kong, equinix.com
 6  unknown.telstraglobal.net (210.57.81.129)  1.67 ms  AS4637  China, Hong Kong, telstra.com
 7  *
 8  202.84.138.74  15.61 ms  AS4637  China, Taiwan, Taipei City, telstra.com
 9  i-92.tpei02.telstraglobal.net (202.84.137.250)  13.89 ms  AS4637  China, Taiwan, Taipei City, telstra.com
10  unknown.telstraglobal.net (210.176.136.111)  45.11 ms  AS4637  China, Taiwan, Taipei City, telstra.com
11  r56-142.seed.net.tw (139.175.56.142)  46.02 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
12  h90-192-72-49.seed.net.tw (192.72.49.90)  44.94 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
13  frd01.seed.net.tw (139.175.1.1)  45.70 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
```

##### APTG 203.79.224.10

```
traceroute to 203.79.224.10 (203.79.224.10), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.33 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  10.40.40.204  0.46 ms  *  LAN Address
 3  172.29.29.13  4.20 ms  *  LAN Address
 4  9505.hkg.equinix.com (36.255.56.66)  0.97 ms  AS9498  China, Hong Kong, equinix.com
 5  175-41-60-233.twgate-ip.twgate.net (175.41.60.233)  1.34 ms  AS9505  China, Hong Kong, twgate.net
 6  175-41-60-89.twgate-ip.twgate.net (175.41.60.89)  17.34 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 7  175-41-58-146.twgate-ip.twgate.net (175.41.58.146)  17.57 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 8  203-78-187-78.twgate-ip.twgate.net (203.78.187.78)  43.08 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 9  203-79-253-161.ebix.net.tw (203.79.253.161)  42.92 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
10  IL203-79-251-46.static.apol.com.tw (203.79.251.46)  43.47 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
11  *
12  dns.octor.com (203.79.224.10)  43.52 ms  AS9311  China, Taiwan, Taipei City, aptg.com.tw
```

##### SoNET 61.64.127.1

```
traceroute to 61.64.127.1 (61.64.127.1), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.68 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  10.40.40.204  0.80 ms  *  LAN Address
 3  172.29.29.13  0.35 ms  *  LAN Address
 4  9505.hkg.equinix.com (36.255.56.66)  1.34 ms  AS9498  China, Hong Kong, equinix.com
 5  175-41-60-217.twgate-ip.twgate.net (175.41.60.217)  14.54 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 6  203-78-181-214.twgate-ip.twgate.net (203.78.181.214)  14.59 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 7  175-41-63-86.twgate-ip.twgate.net (175.41.63.86)  14.20 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 8  219.84.176.122  14.50 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
 9  219.84.176.142  24.89 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
10  gw.so-net.net.tw (61.64.127.249)  14.20 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
11  gw.so-net.net.tw (61.64.127.249)  14.98 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
12  gw.so-net.net.tw (61.64.127.249)  14.32 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
13  ns1.so-net.net.tw (61.64.127.1)  14.45 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
```

##### TFN 219.87.66.1

```
traceroute to 219.87.66.1 (219.87.66.1), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.61 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  10.40.40.204  0.38 ms  *  LAN Address
 3  172.29.29.13  0.26 ms  *  LAN Address
 4  9505.hkg.equinix.com (36.255.56.66)  0.48 ms  AS9498  China, Hong Kong, equinix.com
 5  175-41-60-217.twgate-ip.twgate.net (175.41.60.217)  15.00 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 6  175-41-61-182.twgate-ip.twgate.net (175.41.61.182)  14.53 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 7  175-41-60-174.twgate-ip.twgate.net (175.41.60.174)  14.80 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 8  60-199-14-242.static.tfn.net.tw (60.199.14.242)  15.09 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
 9  219-87-66-1.static.tfn.net.tw (219.87.66.1)  16.90 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
```

##### TAIFO 103.31.196.1

```
traceroute to 103.31.196.1 (103.31.196.1), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.40 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  10.40.40.204  0.41 ms  *  LAN Address
 3  172.29.29.17  0.53 ms  *  LAN Address
 4  3005.r1.102.eq.hk.iptp.net (220.158.132.103)  0.81 ms  AS41095,AS140951  China, Hong Kong, iptp.net
 5  *
 6  210.173.176.96  43.53 ms  *  Japan, Tokyo, mfeed.ad.jp
 7  85.95.26.113  45.87 ms  AS15412  Japan, Tokyo, globalcloudxchange.com
 8  62.216.128.94  74.03 ms  AS15412  China, Taiwan, Taipei City, globalcloudxchange.com
 9  80.77.2.202  83.44 ms  AS15412  China, Taiwan, Taipei City, globalcloudxchange.com
10  13-252-123-103-static.chief.net.tw (103.123.252.13)  74.36 ms  *  China, Taiwan, Taipei City, chief.com.tw
11  209-84-21-113-static.chief.net.tw (113.21.84.209)  74.39 ms  *  China, Taiwan, Taipei City, chief.com.tw
12  210-84-21-113-static.chief.net.tw (113.21.84.210)  74.15 ms  *  China, Taiwan, Taipei City, chief.com.tw
13  103.31.197.122  74.35 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
14  *
15  103.31.197.70  74.22 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
16  103.31.196.1  74.77 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
```

##### Kbro 123.195.236.110

```
traceroute to 123.195.236.110 (123.195.236.110), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  8.58 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  10.40.40.204  0.35 ms  *  LAN Address
 3  172.29.29.13  0.36 ms  *  LAN Address
 4  9505.hkg.equinix.com (36.255.56.66)  0.50 ms  AS9498  China, Hong Kong, equinix.com
 5  175-41-60-217.twgate-ip.twgate.net (175.41.60.217)  14.75 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 6  175-41-60-221.twgate-ip.twgate.net (175.41.60.221)  14.72 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 7  175-41-60-170.twgate-ip.twgate.net (175.41.60.170)  15.27 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 8  60-199-14-242.static.tfn.net.tw (60.199.14.242)  15.13 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
 9  60-199-3-125.static.tfn.net.tw (60.199.3.125)  44.13 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
10  60-199-47-106.static.tfn.net.tw (60.199.47.106)  46.92 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
11  219-80-114-102.static.tfn.net.tw (219.80.114.102)  44.72 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
12  *
13  *
14  123-195-236-110.dynamic.kbronet.com.tw (123.195.236.110)  44.55 ms  AS9924  China, Taiwan, Taipei City, kbro.com.tw
```

### 大陆路由

##### 北京电信 219.141.147.210

```
traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.29 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  *
 3  *
 4  *
 5  port-channel4.core4.lax2.he.net (184.105.223.226)  138.71 ms  AS6939  United States, California, Los Angeles, he.net
 6  64.62.244.62  153.20 ms  AS6939  United States, California, Los Angeles, he.net
 7  202.97.52.165  165.75 ms  AS4134  China, Beijing, ChinaTelecom
 8  *
 9  *
10  *
11  6.254.120.106.static.bjtelecom.net (106.120.254.6)  170.34 ms  AS4847  China, Beijing, ChinaTelecom
12  bj141-147-210.bjtelecom.net (219.141.147.210)  168.14 ms  AS4847  China, Beijing, ChinaTelecom
```

##### 上海电信 202.96.209.133

```
traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.37 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  *
 3  *
 4  *
 5  *
 6  64.62.244.62  146.96 ms  AS6939  United States, California, Los Angeles, he.net
 7  *
 8  202.97.12.185  147.20 ms  AS4134  China, Shanghai, ChinaTelecom
 9  *
10  101.95.88.65  156.94 ms  AS4812  China, Shanghai, ChinaTelecom
11  *
12  180.169.255.122  149.44 ms  AS4812  China, Shanghai, ChinaTelecom
13  ns-pd.online.sh.cn (202.96.209.133)  155.36 ms  AS4812  China, Shanghai, ChinaTelecom
```

##### 深圳电信 58.60.188.222

```
traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.22 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  ve336.core2.hkg2.he.net (74.82.49.173)  0.63 ms  AS6939  China, Hong Kong, he.net
 3  *
 4  *
 5  port-channel8.core2.lax1.he.net (184.104.197.109)  153.80 ms  AS6939  United States, California, Los Angeles, he.net
 6  *
 7  *
 8  chinanet-backbone-as4134.10gigabitethernet13-14.core1.sjc2.he.net (64.62.151.102)  192.65 ms  AS6939  United States, California, San Jose, he.net
 9  *
10  *
11  *
12  202.105.158.49  184.43 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
13  *
14  58.60.188.222  191.34 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
```

##### 北京联通 202.106.50.1

```
traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.42 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  *
 3  *
 4  59.43.184.153  277.06 ms  *  China, Shanghai, ChinaTelecom
 5  *
 6  *
 7  *
 8  *
 9  *
10  *
11  219.158.5.5  308.87 ms  AS4837  China, Beijing, ChinaUnicom
12  *
13  202.106.50.1  327.71 ms  AS4808  China, Beijing, ChinaUnicom
```

##### 上海联通 210.22.97.1

```
traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.57 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  *
 3  *
 4  *
 5  *
 6  *
 7  219.158.38.241  246.57 ms  AS4837  China, Shanghai, ChinaUnicom
 8  *
 9  *
10  *
11  *
12  *
13  *
14  210.22.97.1  252.72 ms  AS17621  China, Shanghai, ChinaUnicom
```

##### 深圳联通 210.21.196.6

```
traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.39 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  *
 3  *
 4  *
 5  *
 6  59.43.130.149  215.78 ms  *  China, Guangdong, Guangzhou, ChinaTelecom
 7  219.158.38.245  208.94 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
 8  *
 9  *
10  120.80.144.34  222.88 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
11  *
12  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  214.13 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
```

##### 北京移动 221.179.155.161

```
traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.32 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  10.40.40.204  0.32 ms  *  LAN Address
 3  172.29.29.21  1.35 ms  *  LAN Address
 4  27.111.196.245  0.50 ms  AS17819  China, Hong Kong, equinix.com
 5  xe-2-0-1-gw701.hk2.ap.equinix.com (36.255.38.170)  0.45 ms  *  China, Hong Kong, equinix.com
 6  unknown.telstraglobal.net (210.57.81.129)  1.59 ms  AS4637  China, Hong Kong, telstra.com
 7  i-0-3-0-6.hkck-core01.telstraglobal.net (202.84.173.21)  4.74 ms  AS4637  China, Hong Kong, telstra.com
 8  202.84.157.37  2.42 ms  AS4637  China, Hong Kong, telstra.com
 9  134.159.128.214  53.33 ms  AS4637  China, Hong Kong, telstra.com
10  *
11  223.120.2.82  52.47 ms  AS58453  China, Guangdong, Guangzhou, ChinaMobile
12  223.120.22.29  134.51 ms  AS58453  China, Guangdong, Guangzhou, ChinaMobile
13  221.183.55.106  129.43 ms  AS9808  China, Beijing, ChinaMobile
14  221.183.46.250  130.42 ms  AS9808  China, Beijing, ChinaMobile
15  221.183.89.102  121.92 ms  AS9808  China, Beijing, ChinaMobile
16  221.183.46.178  113.67 ms  AS9808  China, Beijing, ChinaMobile
17  221.183.110.162  118.61 ms  AS9808  China, Beijing, ChinaMobile
18  cachedns03.bj.chinamobile.com (221.179.155.161)  123.16 ms  AS56048  China, Beijing, ChinaMobile
```

##### 上海移动 211.136.112.200

```
traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  21.08 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  10.40.40.204  0.53 ms  *  LAN Address
 3  172.29.29.21  0.40 ms  *  LAN Address
 4  27.111.196.245  0.45 ms  AS17819  China, Hong Kong, equinix.com
 5  xe-1-1-1.gw1501.hk1.ap.equinix.com (36.255.38.162)  0.59 ms  *  China, Hong Kong, equinix.com
 6  63-218-175-13.static.pccwglobal.net (63.218.175.13)  1.00 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 7  *
 8  223.121.2.49  37.82 ms  AS58453  Singapore, ChinaMobile
 9  223.120.22.133  33.68 ms  AS58453  China, Hong Kong, ChinaMobile
10  223.120.3.182  82.30 ms  AS58453  China, Shanghai, ChinaMobile
11  221.183.89.170  83.75 ms  AS9808  China, Shanghai, ChinaMobile
12  221.183.89.33  83.58 ms  AS9808  China, Shanghai, ChinaMobile
13  *
14  *
15  221.181.125.138  86.53 ms  AS24400  China, Shanghai, ChinaMobile
16  211.136.112.252  85.27 ms  AS24400  China, Shanghai, ChinaMobile
17  211.136.112.200  85.31 ms  AS24400  China, Shanghai, ChinaMobile
```

##### 深圳移动 120.196.165.24

```
traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  8.18 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  10.40.40.204  0.53 ms  *  LAN Address
 3  172.29.29.21  0.48 ms  *  LAN Address
 4  27.111.196.245  0.52 ms  AS17819  China, Hong Kong, equinix.com
 5  xe-1-1-1.gw1501.hk1.ap.equinix.com (36.255.38.162)  0.53 ms  *  China, Hong Kong, equinix.com
 6  63-218-175-13.static.pccwglobal.net (63.218.175.13)  1.09 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 7  223.119.48.5  186.54 ms  AS58453  China, Hong Kong, ChinaMobile
 8  *
 9  223.120.2.6  169.22 ms  AS58453  China, Guangdong, Guangzhou, ChinaMobile
10  221.183.68.125  169.73 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
11  221.183.25.122  168.99 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
12  221.183.68.138  168.87 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
13  *
14  221.183.71.70  173.12 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
15  221.183.110.166  176.02 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
16  *
17  *
18  ns6.gd.cnmobile.net (120.196.165.24)  175.75 ms  AS56040  China, Guangdong, Shenzhen, ChinaMobile
```

##### 成都教育网 202.112.14.151

```
traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  103.231.254.23.layerdns.cloud (103.231.254.23)  0.93 ms  AS133380  China, Hong Kong, easyinternethk.com
 2  *
 3  218.30.49.125  148.81 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
 4  59.43.184.153  145.77 ms  *  China, Shanghai, ChinaTelecom
 5  *
 6  59.43.138.49  152.86 ms  *  China, Shanghai, ChinaTelecom
 7  *
 8  *
 9  202.97.81.226  148.57 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
10  *
11  101.4.117.217  187.73 ms  AS4538  China, Shanghai, CHINAEDU
12  101.4.116.90  188.11 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
13  *
14  *
15  *
16  202.112.14.151  186.39 ms  AS24355  China, Sichuan, Chengdu, CHINAEDU
```

## 流媒体解锁

```
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               No
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: HK)
 Amazon Prime Video:                    Yes (Region: HK)
 TVBAnywhere+:                          No
 iQyi Oversea Region:                   HK
 Viu.com:                               Yes (Region: HK)
 YouTube CDN:                           Hong Kong 
 Netflix Preferred CDN:                 Hong Kong  
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
 DMM:                                   Unsupported
 DMM TV:                                No
 Abema.TV:                              No
 Niconico:                              No
 music.jp:                              No
 Telasa:                                Yes
 Paravi:                                No
 U-NEXT:                                No
 Hulu Japan:                            Yes
 TVer:                                  Yes
 GYAO!:                                 No
 WOWOW:                                 Failed
 VideoMarket:                           Failed (Unexpected Result: 404)
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
 Epix:                                  Failed
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
 DirecTV Go:                            Yes (Region: CO)
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
 Joyn:                                  Yes
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
