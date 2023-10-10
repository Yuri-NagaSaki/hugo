---
title: "usercloud.host 香港VPS"
date: "2023-07-04"
categories: 
  - "vps"
  - "hk"
---

- 新开的香港主机，自有 AS 151188，上游对接 enos

> 官网：[https://www.usercloud.host/](https://www.usercloud.host/)  
> 购买：[https://billing.usercloud.host/index.php/store/hk-kvm](https://billing.usercloud.host/index.php/store/hk-kvm)

## Test Plan

下单连结：[https://billing.usercloud.host/index.php/store/hk-kvm/starter-vps](https://billing.usercloud.host/index.php/store/hk-kvm/starter-vps)

方案：1h2g 30GB

## Info

```
 CPU Model          : Intel(R) Xeon(R) CPU E5-2660 v4 @ 2.00GHz
 CPU Cores          : 1 Core @ 1995.373 MHz
 CPU Cache          : 35840 KB
 AES-NI             : ✓ Enabled
 VM-x/AMD-V         : ✓ Enabled
 Total Disk         : 1.7 GB / 30.0 GB
 Total Mem          : 147.8 MB / 1.9 GB
 System uptime      : 0 days, 0 hour 28 min
 Load average       : 0.18, 0.05, 0.01
 OS                 : Debian GNU/Linux 11 x86_64 (64 Bit)
 Kernel             : 5.10.0-20-amd64
 TCP CC             : cubic
 Virtualization     : KVM
```

## CPU

据商家自称使用 CPU 为 **Intel Xeon E5-2660 v4**

### GeekBench 4

测试结果：[https://browser.geekbench.com/v4/cpu/16787874](https://browser.geekbench.com/v4/cpu/16787874)

![](https://catcat.blog/wp-content/uploads/2023/07/image-1-1024x219.png)

### GeekBench 5

测试结果：[https://browser.geekbench.com/v5/cpu/21321561](https://browser.geekbench.com/v5/cpu/21321561)

![](https://catcat.blog/wp-content/uploads/2023/10/image-166.png)

## Disk

### IO

```
 Test Name              Write Speed                             Read Speed
 10MB-4K Block          13.2 MB/s (3218 IOPS, 0.80s)            12.8 MB/s (3127 IOPS, 0.82s)
 10MB-1M Block          555 MB/s (529 IOPS, 0.02s)              866 MB/s (825 IOPS, 0.01s)
 100MB-4K Block         14.4 MB/s (3507 IOPS, 7.30s)            15.9 MB/s (3889 IOPS, 6.58s)
 100MB-1M Block         563 MB/s (536 IOPS, 0.19s)              519 MB/s (494 IOPS, 0.20s)
 1GB-4K Block           14.2 MB/s (3458 IOPS, 74.03s)           18.1 MB/s (4411 IOPS, 58.03s)
 1GB-1M Block           390 MB/s (372 IOPS, 2.69s)              152 MB/s (145 IOPS, 6.88s)
```

### FIO

```
fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.40 MB/s      (851) | 28.29 MB/s     (442)
Write      | 3.43 MB/s      (859) | 28.65 MB/s     (447)
Total      | 6.84 MB/s     (1.7k) | 56.95 MB/s     (889)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 71.57 MB/s     (139) | 91.40 MB/s      (89)
Write      | 75.38 MB/s     (147) | 97.49 MB/s      (95)
Total      | 146.96 MB/s    (286) | 188.89 MB/s    (184)
```

## Network

### SpeedTest

```
Node Name                  Upload Speed      Download Speed    Latency     Result      
 Speedtest.net              153.78 Mbps       128.08 Mbps       195.85 ms   https://www.speedtest.net/result/c/8dc7c39c-02e2-433b-ad39-9e48c5a4e44a
 CN, Hefei, Anhui CT        0.53 Mbps         3.90 Mbps         328.50 ms   https://www.speedtest.net/result/c/7d1a8db3-b599-4c10-8c8a-b19e331de1df
 CN, Jiangsu Zhenjiang CT   0.56 Mbps         0.98 Mbps         353.74 ms   https://www.speedtest.net/result/c/f96bcd58-fe77-45a0-82e1-0d52810d29fc
 CN, Chengdu, Sichuan CT    0.91 Mbps         1.36 Mbps         509.86 ms   https://www.speedtest.net/result/c/2307dc1e-2aa6-482b-844a-8cb559d0f896
 CN, Shanghai CU            82.70 Mbps        138.27 Mbps       251.24 ms   https://www.speedtest.net/result/c/4db34865-c188-4d91-b364-90a6b36f877b
 CN, Wuxi, Jiangsu CU       161.38 Mbps       143.79 Mbps       98.20 ms    https://www.speedtest.net/result/c/771859ae-b79f-45c4-9884-7bfd876a2a82
 CN, Zhengzhou, Henan CU    160.35 Mbps       147.00 Mbps       98.50 ms    https://www.speedtest.net/result/c/2ef85172-17b3-4ad7-931f-47f74d6dd021
 CN, Shenyang, Liaoning CU  3.92 Mbps         133.09 Mbps       114.11 ms   https://www.speedtest.net/result/c/c56b65ff-4f9a-4853-b74d-4cd8a9e8b88a
 CN, Beijing CM             128.43 Mbps       151.13 Mbps       114.09 ms   https://www.speedtest.net/result/c/f1685195-5b89-48cd-ac59-c70e081274ad
 CN, Chengdu, Sichuan CM    152.75 Mbps       153.56 Mbps       121.85 ms   https://www.speedtest.net/result/c/49f14617-e868-4913-833b-db57400f6719
 CN, Zhengzhou, Henan CM    0.19 Mbps         142.00 Mbps       292.51 ms   https://www.speedtest.net/result/c/7a9aace7-cfe3-4119-b13f-500c824ae8a2
 CN, Hangzhou, Zhejiang CM  159.03 Mbps       156.55 Mbps       346.16 ms   https://www.speedtest.net/result/c/c95b24c6-535b-4f6c-81e5-8dc8ee9b7f03
 CN, Lanzhou, Gansu CM      2.31 Mbps         155.33 Mbps       172.11 ms   https://www.speedtest.net/result/c/ba1d9d3d-60e0-47dd-8f56-363d8a927b3f

 CN, Jiangsu Kunshan EDU    23.50 Mbps        1.55 Mbps         87.00 ms    https://www.speedtest.net/result/c/c35882ca-75f0-4f38-a4aa-93275a453b9b
 CN, Sichuan Chengdu BN     1.47 Mbps         84.40 Mbps        341.53 ms   https://www.speedtest.net/result/c/01ddcced-5063-4657-8165-d604846348b4
 HK, HKIX                   148.65 Mbps       142.19 Mbps       1.74 ms     https://www.speedtest.net/result/c/d90ea438-be7e-4625-9f43-dba79112fd94
 HK, i3D.net                148.29 Mbps       142.54 Mbps       2.42 ms     https://www.speedtest.net/result/c/508b799b-2d5f-4504-b47b-8d1647ed11db
 JP, i3D.net                152.05 Mbps       144.65 Mbps       43.49 ms    https://www.speedtest.net/result/c/ea20df97-673e-4bf9-bcf3-ad38990138a0
 SG, i3D.net                150.20 Mbps       142.63 Mbps       36.77 ms    https://www.speedtest.net/result/c/8d8c9cfb-4b8d-4e82-9688-d95723fc85e2
 SG, NewMedia Express       151.03 Mbps       142.74 Mbps       35.66 ms    https://www.speedtest.net/result/c/67cace64-a565-4770-af8e-ca321bd666af
 MY, Telekom Malaysia       150.06 Mbps       145.27 Mbps       67.18 ms    https://www.speedtest.net/result/c/5c046101-5d31-4202-be98-f6b72c4c7b79
 MY, Celcom                 150.29 Mbps       144.94 Mbps       66.28 ms    https://www.speedtest.net/result/c/f5ef2ed3-9553-4925-832e-a52155093736
 DE, GSL Networks           156.77 Mbps       149.57 Mbps       187.61 ms   https://www.speedtest.net/result/c/a171f626-341f-4322-9d1e-33f0aa58a189
 DE, wirsNET                109.93 Mbps       47.17 Mbps        181.10 ms   https://www.speedtest.net/result/c/2ab96f8e-2343-4199-a892-5d8acd072c70
 TR, Turkcell               160.33 Mbps       144.54 Mbps       225.57 ms   https://www.speedtest.net/result/c/973684a6-9e51-4a9d-8e80-8161a0aa5bd9
 TR, TurkNet                161.34 Mbps       144.62 Mbps       229.40 ms   https://www.speedtest.net/result/c/605ebfe7-4b09-4761-9dbc-ded2c10e5028
```

### TraceRoute

#### CN, 北京电信

```
traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  hkg1-edge.as151188.simple.taipei (103.244.163.1)  0.27 ms  AS151188  China, Hong Kong
 2  103.180.28.33  13.43 ms  AS138997  China, Hong Kong, metroponet.com
 3  ae-0-0.cr1.hkg1.eons.cloud (103.138.72.1)  0.56 ms  AS138997  China, Hong Kong, eons.cloud
 4  63.222.112.41  0.91 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 5  *
 6  TenGE0-2-0-1.br03.lax05.pccwbtn.net (63.218.72.166)  249.87 ms  AS3491,AS31713  United States, California, Los Angeles, pccw.com
 7  218.30.53.86  328.37 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
 8  *
 9  *
10  *
11  *
12  *
13  6.254.120.106.static.bjtelecom.net (106.120.254.6)  367.09 ms  AS4847  China, Beijing, ChinaTelecom
14  bj141-147-210.bjtelecom.net (219.141.147.210)  316.93 ms  AS4847  China, Beijing, ChinaTelecom
```

#### CN, 上海电信

```
traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  hkg1-edge.as151188.simple.taipei (103.244.163.1)  0.27 ms  AS151188  China, Hong Kong
 2  103.180.28.33  11.51 ms  AS138997  China, Hong Kong, metroponet.com
 3  ae-0-0.cr1.hkg1.eons.cloud (103.138.72.1)  1.03 ms  AS138997  China, Hong Kong, eons.cloud
 4  63.222.112.41  1.25 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 5  *
 6  HundredGE0-5-0-0.br03.lax05.pccwbtn.net (63.218.72.230)  254.20 ms  AS3491,AS31713  United States, California, Los Angeles, pccw.com
 7  218.30.53.86  320.17 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
 8  202.97.89.141  487.67 ms  AS4134  China, Shanghai, ChinaTelecom
 9  *
10  *
11  *
12  124.74.229.234  480.57 ms  AS4812  China, Shanghai, ChinaTelecom
13  *
14  ns-pd.online.sh.cn (202.96.209.133)  434.30 ms  AS4812  China, Shanghai, ChinaTelecom
```

#### CN, 深圳电信

```
traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  hkg1-edge.as151188.simple.taipei (103.244.163.1)  0.29 ms  AS151188  China, Hong Kong
 2  103.180.28.33  14.03 ms  AS138997  China, Hong Kong, metroponet.com
 3  ae-0-0.cr1.hkg1.eons.cloud (103.138.72.1)  0.62 ms  AS138997  China, Hong Kong, eons.cloud
 4  63.222.112.41  1.07 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 5  *
 6  218.30.53.86  322.92 ms  AS4134  United States, California, Los Angeles, ChinaTelecom
 7  *
 8  202.97.91.193  470.40 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
 9  202.97.91.157  368.09 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
10  202.105.158.49  360.62 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
11  *
12  58.60.188.222  446.34 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
```

#### CN, 北京联通

```
traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  hkg1-edge.as151188.simple.taipei (103.244.163.1)  0.37 ms  AS151188  China, Hong Kong
 2  103.180.28.33  22.36 ms  AS138997  China, Hong Kong, metroponet.com
 3  ae-0-0.cr2.hkg1.eons.cloud (103.138.72.2)  0.54 ms  AS138997  China, Hong Kong, eons.cloud
 4  ae-0-0.cr1.hkg1.eons.cloud (103.138.72.1)  0.96 ms  AS138997  China, Hong Kong, eons.cloud
 5  63.222.112.41  1.31 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 6  *
 7  Bundle-Ether40.br06.sjo01.pccwbtn.net (63.223.60.126)  246.58 ms  AS3491,AS31713  United States, California, San Jose, pccw.com
 8  63-217-21-70.static.pccwglobal.net (63.217.21.70)  240.71 ms  AS3491,AS31713  United States, California, San Jose, pccw.com
 9  *
10  CHINA-NETCO.ear1.LosAngeles6.Level3.net (4.26.2.162)  201.22 ms  AS3356  United States, California, Los Angeles, level3.com
11  219.158.4.9  208.89 ms  AS4837  China, Beijing, ChinaUnicom
12  219.158.9.218  221.60 ms  AS4837  China, Beijing, ChinaUnicom
13  *
14  *
15  202.106.50.1  245.69 ms  AS4808  China, Beijing, ChinaUnicom
```

#### CN, 上海联通

```
 traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  hkg1-edge.as151188.simple.taipei (103.244.163.1)  0.35 ms  AS151188  China, Hong Kong
 2  103.180.28.33  6.66 ms  AS138997  China, Hong Kong, metroponet.com
 3  ae-0-0.cr2.hkg1.eons.cloud (103.138.72.2)  0.61 ms  AS138997  China, Hong Kong, eons.cloud
 4  ae-0-0.cr1.hkg1.eons.cloud (103.138.72.1)  1.42 ms  AS138997  China, Hong Kong, eons.cloud
 5  63.222.112.41  1.48 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 6  *
 7  *
 8  63-217-21-70.static.pccwglobal.net (63.217.21.70)  240.93 ms  AS3491,AS31713  United States, California, San Jose, pccw.com
 9  4.69.209.169  241.49 ms  AS3356  United States, California, San Jose, level3.com
10  CHINA-UNICO.edge1.SanJose3.Level3.net (4.53.209.78)  254.38 ms  AS3356  United States, California, San Jose, level3.com
11  219.158.6.5  234.78 ms  AS4837  China, Shanghai, ChinaUnicom
12  219.158.6.209  239.92 ms  AS4837  China, Shanghai, ChinaUnicom
13  *
14  *
15  *
16  210.22.97.1  230.63 ms  AS17621  China, Shanghai, ChinaUnicom
```

#### CN, 深圳联通

```
traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  hkg1-edge.as151188.simple.taipei (103.244.163.1)  0.25 ms  AS151188  China, Hong Kong
 2  103.180.28.33  3.08 ms  AS138997  China, Hong Kong, metroponet.com
 3  ae-0-0.cr2.hkg1.eons.cloud (103.138.72.2)  0.45 ms  AS138997  China, Hong Kong, eons.cloud
 4  ae-0-0.cr1.hkg1.eons.cloud (103.138.72.1)  0.53 ms  AS138997  China, Hong Kong, eons.cloud
 5  63.222.112.41  1.01 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 6  *
 7  *
 8  63-217-21-70.static.pccwglobal.net (63.217.21.70)  240.47 ms  AS3491,AS31713  United States, California, San Jose, pccw.com
 9  ae1.17.edge1.LosAngeles6.level3.net (4.69.209.249)  229.82 ms  AS3356  United States, California, Los Angeles, level3.com
10  CHINA-NETCO.edge1.LosAngeles6.Level3.net (4.26.0.66)  193.29 ms  AS3356  United States, California, Los Angeles, level3.com
11  219.158.98.49  195.80 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
12  219.158.4.29  204.81 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
13  219.158.3.97  204.24 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
14  *
15  120.80.144.34  213.63 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
16  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  206.29 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
```

#### CN, 北京移动

```
traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  hkg1-edge.as151188.simple.taipei (103.244.163.1)  0.29 ms  AS151188  China, Hong Kong
 2  103.180.28.33  12.38 ms  AS138997  China, Hong Kong, metroponet.com
 3  ae-0-0.cr1.hkg1.eons.cloud (103.138.72.1)  0.91 ms  AS138997  China, Hong Kong, eons.cloud
 4  hu-0-0-1-0.br1.hkg2.eons.cloud (103.138.72.9)  0.86 ms  AS138997  China, Hong Kong, eons.cloud
 5  gsl-be-2-4.br1.hkg2.eons.cloud (103.138.72.19)  5.97 ms  AS138997  China, Hong Kong, eons.cloud
 6  31.217.251.226  1.38 ms  AS7578  China, Hong Kong, globalsecurelayer.com
 7  31.217.251.120  1.71 ms  AS7578  China, Hong Kong, globalsecurelayer.com
 8  unknown.telstraglobal.net (210.176.141.138)  1.98 ms  AS4637  China, Hong Kong, telstra.com
 9  202.84.157.226  3.50 ms  AS4637  China, Hong Kong, telstra.com
10  202.84.157.37  2.29 ms  AS4637  China, Hong Kong, telstra.com
11  134.159.128.214  88.04 ms  AS4637  China, Hong Kong, telstra.com
12  *
13  223.120.22.142  138.92 ms  AS58453  China, Beijing, ChinaMobile
14  221.183.55.110  147.39 ms  AS9808  China, Beijing, ChinaMobile
15  221.183.25.201  140.34 ms  AS9808  China, Beijing, ChinaMobile
16  221.183.89.122  137.25 ms  AS9808  China, Beijing, ChinaMobile
17  221.183.46.178  142.29 ms  AS9808  China, Beijing, ChinaMobile
18  221.183.110.162  152.58 ms  AS9808  China, Beijing, ChinaMobile
19  *
20  cachedns03.bj.chinamobile.com (221.179.155.161)  138.89 ms  AS56048  China, Beijing, ChinaMobile
```

#### CN, 上海移动

```
traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  hkg1-edge.as151188.simple.taipei (103.244.163.1)  0.36 ms  AS151188  China, Hong Kong
 2  103.180.28.33  40.19 ms  AS138997  China, Hong Kong, metroponet.com
 3  ae-0-0.cr2.hkg1.eons.cloud (103.138.72.2)  0.67 ms  AS138997  China, Hong Kong, eons.cloud
 4  ae-0-0.cr1.hkg1.eons.cloud (103.138.72.1)  0.50 ms  AS138997  China, Hong Kong, eons.cloud
 5  63.222.112.41  1.34 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 6  *
 7  223.121.2.49  36.21 ms  AS58453  Singapore, ChinaMobile
 8  223.120.2.45  68.50 ms  AS58453  China, Hong Kong, ChinaMobile
 9  *
10  221.183.89.174  100.97 ms  AS9808  China, Shanghai, ChinaMobile
11  221.183.89.69  100.24 ms  AS9808  China, Shanghai, ChinaMobile
12  221.183.89.50  102.06 ms  AS9808  China, Shanghai, ChinaMobile
13  *
14  211.136.190.234  87.45 ms  AS24400  China, Shanghai, ChinaMobile
15  211.136.112.252  88.64 ms  AS24400  China, Shanghai, ChinaMobile
16  211.136.112.200  90.93 ms  AS24400  China, Shanghai, ChinaMobile
```

#### CN, 深圳移动

```
traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  hkg1-edge.as151188.simple.taipei (103.244.163.1)  0.27 ms  AS151188  China, Hong Kong
 2  103.180.28.33  31.99 ms  AS138997  China, Hong Kong, metroponet.com
 3  ae-0-0.cr1.hkg1.eons.cloud (103.138.72.1)  0.59 ms  AS138997  China, Hong Kong, eons.cloud
 4  63.222.112.41  0.92 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 5  HundredGE0-3-0-1.br03.hkg12.pccwbtn.net (63.218.174.201)  1.97 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 6  HundredGE0-3-0-1.br03.hkg12.pccwbtn.net (63.218.174.201)  1.43 ms  AS3491,AS31713  China, Hong Kong, pccw.com
 7  223.119.48.5  35.94 ms  AS58453  China, Hong Kong, ChinaMobile
 8  223.120.2.49  35.31 ms  AS58453  China, Hong Kong, ChinaMobile
 9  223.120.3.174  68.54 ms  AS58453  China, Shanghai, ChinaMobile
10  221.183.89.174  70.05 ms  AS9808  China, Shanghai, ChinaMobile
11  221.183.89.69  69.28 ms  AS9808  China, Shanghai, ChinaMobile
12  221.183.89.50  71.17 ms  AS9808  China, Shanghai, ChinaMobile
13  *
14  221.183.46.178  98.42 ms  AS9808  China, Beijing, ChinaMobile
15  *
16  ns6.gd.cnmobile.net (120.196.165.24)  98.16 ms  AS56040  China, Guangdong, Shenzhen, ChinaMobile
```

## Media

```
 ** 正在测试IPv4解锁情况 
--------------------------------
 ** 您的网络为: 404 Network Information Co. (103.244.*.*) 


============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: TW)
 Netflix:                               Yes (Region: TW)
 YouTube Premium:                       Yes (Region: TW)
 Amazon Prime Video:                    Yes (Region: TW)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   TW
 Viu.com:                               Failed
 YouTube CDN:                           Taipei 
 Netflix Preferred CDN:                 Hong Kong  
 Spotify Registration:                  No
 Steam Currency:                        HKD
 ChatGPT:                               Yes
=======================================
==============[ Taiwan ]===============
 KKTV:                                  No
 LiTV:                                  Yes
 MyVideo:                               Yes
 4GTV.TV:                               Yes
 LineTV.TW:                             Yes
 Hami Video:                            No
 CatchPlay+:                            Failed
 HBO GO Asia:                           No
 Bahamut Anime:                         Failed (Network Connection)
 Bilibili Taiwan Only:                  No
=======================================
=============[ Hong Kong ]=============
 Now E:                                 Failed (Unexpected Result: )
 Viu.TV:                                No
 MyTVSuper:                             No
 HBO GO Asia:                           No
 BiliBili Hongkong/Macau/Taiwan:        Yes
=======================================
===============[ Japan ]===============
 DMM:                                   Unsupported
 DMM TV:                                Yes
 Abema.TV:                              No
 Niconico:                              No
 music.jp:                              No
 Telasa:                                Yes
 Paravi:                                Yes
 U-NEXT:                                No
 Hulu Japan:                            Yes
 TVer:                                  Yes
 GYAO!:                                 Yes
 WOWOW:                                 Yes
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
 Project Sekai: Colorful Stage:         Yes
=======================================
===========[ North America ]===========
 FOX:                                   No
 Hulu:                                  Failed
 NFL+:                                  No
 ESPN+:[Sponsored by Jam]               No
 Epix:                                  Yes
 Starz:                                 No
 Philo:                                 No
 FXNOW:                                 No
 TLC GO:                                No
 HBO Max:                               No
 Shudder:                               No
 BritBox:                               Yes
 Crackle:                               No
 CW TV:                                 No
 A&E TV:                                Yes
 NBA TV:                                Yes
 NBC TV:                                No
 Fubo TV:                               Yes
 Tubi TV:                               Yes
 Sling TV:                              Yes
 Pluto TV:                              Yes
 Acorn TV:                              Yes
 SHOWTIME:                              Yes
 encoreTVB:                             No
 Funimation:                            Yes (Region: 00)
 Discovery+:                            No
 Paramount+:                            No
 Peacock TV:                            No
 Popcornflix:                           Yes
 Crunchyroll:                           No
 Directv Stream:                        No
 KBS American:                          No
 KOCOWA:                                Yes
 Maths Spot:                            Failed
 ---CA---
 CBC Gem:                               No
 Crave:                                 Yes
=======================================
===========[ South America ]===========
 Star+:                                 No
 HBO Max:                               No
 DirecTV Go:                            Yes (Region: CO)
 Funimation:                            Yes (Region: 00)
=======================================
===============[ Europe ]==============
 Rakuten TV:                            Yes
 Funimation:                            Yes (Region: 00)
 SkyShowTime:                           No
 HBO Max:                               No
 Maths Spot:                            Failed
 ---GB---
 Sky Go:                                Yes
 BritBox:                               Yes
 ITV Hub:                               No
 Channel 4:                             No
 Channel 5:                             No
 BBC iPLAYER:                           No
 Discovery+ UK:                         No
 ---FR---
 Salto:                                 Failed (Network Connection)
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
 PANTAYA:                               Failed (Network Connection)
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
 Funimation:                            Yes (Region: 00)
 Paramount+:                            No
 ---AU---
 Stan:                                  Yes
 Binge:                                 No
 Docplay:                               Yes
 7plus:                                 No
 Channel 9:                             No
 Channel 10:                            No
 ABC iView:                             No
 Kayo Sports:                           Yes
 Optus Sports:                          No
 SBS on Demand:                         No
 ---NZ---
 Neon TV:                               Yes
 SkyGo NZ:                              No
 ThreeNow:                              Yes
 Maori TV:                              Yes
=======================================
==============[ Korean ]===============
 Wavve:                                 Yes
 Tving:                                 No
 Coupang Play:                          No
 Naver TV:                              No
 Afreeca TV:                            Yes
 KBS Domestic:                          No
=======================================
```
