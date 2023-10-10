---
title: "荷兰 liteserver 测评"
date: "2023-03-11"
categories: 
  - "vps"
  - "eu"
tags: 
  - "eu"
---

> 2007年的佬商家，自有ASN AS60404，主机托管于荷兰Serverius DC1资料中心，有NVMe及HDD可选，均提供1Gbps网络线路，流量会使用完成后会限速10Mbps

- 2007 年创建商家，自有 ASN AS60404

- 托管于荷兰 Serverius DC1 数据中心

- 有 NVMe 及 HDD 可选，均提供 1Gbps 端口，流量使用完后限速 10Mbps

- 可单独加核心（5 €/ 月）跟内存（2 €/ 月）以及 NVMe （2 €/ 月每 50GB）

- 根据 AUP 来理解，如果常被 DDoS 攻击，会导致停机！

- 新用户可以在两天内完成 VPS 的退款（但別滥用 ><）

**官方网站：[点我](https://clients.liteserver.nl/aff.php?aff=621)**

**Looking Glass：[点我](https://lg-drn.liteserver.nl/)** (185.31.172.235)

## 测试规格

![](https://catcat.blog/wp-content/uploads/2023/10/image-85.png)

## 基本配置

```
 CPU Model          : AMD EPYC 7763 64-Core Processor
 CPU Cores          : 2 Core @ 2449.998 MHz
 CPU Cache          : 512 KB
 AES-NI             : ✓ Enabled
 VM-x/AMD-V         : ✓ Enabled
 Total Disk         : 2.4 GB / 39.1 GB
 Total Mem          : 77.6 MB / 1.9 GB
 Total Swap         : 12.0 KB / 255.0 MB
 System uptime      : 0 days, 12 hour 49 min
 Load average       : 0.08, 0.02, 0.01
 OS                 : Debian GNU/Linux 11 x86_64 (64 Bit)
 Kernel             : 5.10.0-16-amd64
 TCP CC             : cubic
 Virtualization     : KVM
```

## CPU 性能测试

![](https://catcat.blog/wp-content/uploads/2023/10/image-86.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-87.png)

**CPU Events Per Second 跑分 (基于 sysbench)**

```
 -> CPU Performance Test (Standard Mode, 3-Pass @ 30sec)

 1 Thread Test:                 3501 Scores
 2 Threads Test:                6999 Scores
```

## 内存性能测试

```
 -> Memory Performance Test (Standard Mode, 3-Pass @ 30sec)

 1 Thread - Read Test :         41902.19 MB/s
 1 Thread - Write Test:         21429.07 MB/s
```

## 硬盘读写性能测试

**DD 硬盘测试：**

```
  Test Name              Write Speed                             Read Speed
 10MB-4K Block          69.8 MB/s (0.06 IOPS, 0.15s))           81.4 MB/s (19864 IOPS, 0.13s)
 10MB-1M Block          2.3 GB/s (2218 IOPS, 0.00s)             961 MB/s (916 IOPS, 0.01s)
 100MB-4K Block         64.7 MB/s (0.06 IOPS, 1.62s))           73.9 MB/s (18047 IOPS, 1.42s)
 100MB-1M Block         2.6 GB/s (2462 IOPS, 0.04s)             2.6 GB/s (2437 IOPS, 0.04s)
 1GB-4K Block           57.0 MB/s (0.07 IOPS, 18.40s))          92.1 MB/s (22482 IOPS, 11.39s)
 1GB-1M Block           973 MB/s (928 IOPS, 1.08s)              3.5 GB/s (3327 IOPS, 0.30s)
```

**FIO 硬盘测试：**

```
fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 373.79 MB/s  (93.4k) | 5.08 GB/s    (79.5k)
Write      | 374.78 MB/s  (93.6k) | 5.11 GB/s    (79.9k)
Total      | 748.58 MB/s (187.1k) | 10.20 GB/s  (159.4k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 8.04 GB/s    (15.7k) | 8.35 GB/s     (8.1k)
Write      | 8.47 GB/s    (16.5k) | 8.90 GB/s     (8.6k)
Total      | 16.51 GB/s   (32.2k) | 17.26 GB/s   (16.8k)
```

## 网络基本信息

```
 IP                 : 5.255.107.155
 Organization       : AS60404 Liteserver
 Location           : Alkmaar / NL
 Region             : North Holland
```

### 全球延迟

![](https://catcat.blog/wp-content/uploads/2023/10/image-88.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-89.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-90.png)

### SpeedTest.net

```
 Node Name                Upload Speed      Download Speed    Latency     Result      
 Speedtest.net            347.77 Mbps       941.79 Mbps       90.85 ms    https://www.speedtest.net/result/c/8b4d3935-fdf6-412a-9908-5db63e2b05d3
 TW, Chunghwa Mobile      244.71 Mbps       703.53 Mbps       138.44 ms   https://www.speedtest.net/result/c/24a18272-06bb-4c6f-894c-7927afd7c016
 TW, Chief Telecom        215.05 Mbps       939.38 Mbps       203.08 ms   https://www.speedtest.net/result/c/fc852ae6-9990-4cb6-b486-f945a4ed8604
 TW, TAIFO                132.17 Mbps       352.53 Mbps       233.97 ms   https://www.speedtest.net/result/c/284d2d0c-753d-49f4-ab6d-3d0d68976e45
 TW, DFT                  187.01 Mbps       152.34 Mbps       240.48 ms   https://www.speedtest.net/result/c/b824e213-8e03-45e2-9f09-1be26e2165cc
 TW, FET                  194.48 Mbps       801.41 Mbps       247.17 ms   https://www.speedtest.net/result/c/09d09f8f-40ac-4b7e-acc5-97a7c4fef02b
 CN, Nanjing CT           69.81 Mbps        238.81 Mbps       215.53 ms   https://www.speedtest.net/result/c/6eaa7d2c-358e-45a0-8b3b-e91162bdb66d
 CN, Hefei CT             22.13 Mbps        431.29 Mbps       180.13 ms   https://www.speedtest.net/result/c/0dcb3d62-9534-4401-8509-dd65ff0450ec
 CN, Guangzhou CT         1.65 Mbps         31.91 Mbps        229.36 ms   https://www.speedtest.net/result/c/79e225ab-ba05-449f-8322-bb0a4e222407
 CN, hanghai CU           218.16 Mbps       472.99 Mbps       185.42 ms   https://www.speedtest.net/result/c/272f81e3-ee8a-4264-8b1e-2ea7185fa9d0
 HK, HKIX                 212.49 Mbps       718.48 Mbps       248.40 ms   https://www.speedtest.net/result/c/6558dc2b-3b56-4ac7-bba1-e14827be89de
 HK, HGC                  185.47 Mbps       9.07 Mbps         245.85 ms   https://www.speedtest.net/result/c/08e4272e-1215-42b5-8d73-649f80543ef5
 HK, i3D.net              187.59 Mbps       547.10 Mbps       172.76 ms   https://www.speedtest.net/result/c/41b47783-48c6-440c-86d9-fbb00c176cbb
 JP, i3D.net              220.19 Mbps       443.12 Mbps       239.32 ms   https://www.speedtest.net/result/c/b905184b-6a99-4ca0-8819-a05634f74295
 JP, GSL Networks         164.90 Mbps       635.98 Mbps       222.13 ms   https://www.speedtest.net/result/c/acefa6e5-adfa-4629-bdb2-a51450ab2895
 JP, fdcservers.net       204.57 Mbps       488.30 Mbps       247.28 ms   https://www.speedtest.net/result/c/d9b516dd-1f21-427d-93cb-72b109fd798f
 SG, i3D.net              224.15 Mbps       693.32 Mbps       152.53 ms   https://www.speedtest.net/result/c/30857d89-bc84-4548-893e-b95e515d87a2
 SG, NewMedia Express     97.00 Mbps        617.37 Mbps       162.15 ms   https://www.speedtest.net/result/c/12193e97-46ab-48e6-8591-fbd164020c08
 SG, SuperInternet        70.64 Mbps        611.09 Mbps       159.91 ms   https://www.speedtest.net/result/c/0138abff-6cf3-457f-ab7e-78fb6d4e8cb6
 MY, Telekom Malaysia     218.09 Mbps       491.57 Mbps       208.88 ms   https://www.speedtest.net/result/c/df132b62-6abd-4d9e-8915-7454fd80b121
 MY, Celcom               189.27 Mbps       1.47 Mbps         202.26 ms   https://www.speedtest.net/result/c/ac0f4e0c-018c-4fdb-9304-6344a1cbde12
 DE, GSL Networks         936.33 Mbps       896.04 Mbps       7.37 ms     https://www.speedtest.net/result/c/4f6ec8f0-bbe9-411f-b411-3694eecbb9bd
 DE, wirsNET              937.62 Mbps       890.58 Mbps       8.62 ms     https://www.speedtest.net/result/c/5f287895-6734-4ca9-bd90-577c830006bf
 TR, Turkcell             576.95 Mbps       928.14 Mbps       45.05 ms    https://www.speedtest.net/result/c/8de764e7-878f-4940-8183-1d86a9fab9bb
 TR, TurkNet              531.99 Mbps       914.32 Mbps       46.45 ms    https://www.speedtest.net/result/c/8420e940-8465-4b9d-ae3a-bea974385bab
```

### iperf3

```
 Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | busy            | 834 Mbits/sec   | 8.30 ms        
Scaleway        | Paris, FR (10G)           | 924 Mbits/sec   | 778 Mbits/sec   | 11.1 ms        
NovoServe       | North Holland, NL (40G)   | 933 Mbits/sec   | 937 Mbits/sec   | 2.13 ms        
Uztelecom       | Tashkent, UZ (10G)        | 530 Mbits/sec   | 360 Mbits/sec   | 82.2 ms        
Clouvider       | NYC, NY, US (10G)         | 599 Mbits/sec   | 335 Mbits/sec   | 80.3 ms        
Clouvider       | Dallas, TX, US (10G)      | 298 Mbits/sec   | 178 Mbits/sec   | 124 ms         
Clouvider       | Los Angeles, CA, US (10G) | 452 Mbits/sec   | 228 Mbits/sec   | 153 ms 
```

### Traceroute

```
**  TW, Hinet ( 168.95.1.1) **

traceroute to 168.95.1.1 (168.95.1.1), 30 hops max, 32 byte packets
 1  5.255.107.2  0.37 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.43 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.31 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  0.67 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.64 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.67 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  0.71 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  0.68 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  0.69 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  80.249.215.17  161.77 ms  *  Netherlands, North Holland, Amsterdam, ams-ix.net
    80.249.215.17  161.86 ms  *  Netherlands, North Holland, Amsterdam, ams-ix.net
    80.249.215.17  161.81 ms  *  Netherlands, North Holland, Amsterdam, ams-ix.net
 5  220-128-6-194.hinet-ip.hinet.net (220.128.6.194)  205.70 ms  *  China, Taiwan, Taipei City, cht.com.tw
    220-128-6-194.hinet-ip.hinet.net (220.128.6.194)  205.70 ms  *  China, Taiwan, Taipei City, cht.com.tw
    220-128-6-194.hinet-ip.hinet.net (220.128.6.194)  205.73 ms  *  China, Taiwan, Taipei City, cht.com.tw
 6  tpdb-3031.hinet.net (220.128.3.162)  208.66 ms  *  China, Taiwan, Taipei City, cht.com.tw
    tpdb-3031.hinet.net (220.128.3.162)  208.37 ms  *  China, Taiwan, Taipei City, cht.com.tw
    tpdb-3031.hinet.net (220.128.3.162)  208.76 ms  *  China, Taiwan, Taipei City, cht.com.tw
 7  tpdb-3311.hinet.net (220.128.3.189)  205.90 ms  *  China, Taiwan, Taipei City, cht.com.tw
    tpdb-3311.hinet.net (220.128.3.189)  205.89 ms  *  China, Taiwan, Taipei City, cht.com.tw
    tpdb-3311.hinet.net (220.128.3.189)  205.88 ms  *  China, Taiwan, Taipei City, cht.com.tw
 8  210-59-204-217.hinet-ip.hinet.net (210.59.204.217)  205.93 ms  AS3462  China, Taiwan, Taipei City, cht.com.tw
    210-59-204-217.hinet-ip.hinet.net (210.59.204.217)  205.88 ms  AS3462  China, Taiwan, Taipei City, cht.com.tw
    210-59-204-217.hinet-ip.hinet.net (210.59.204.217)  205.91 ms  AS3462  China, Taiwan, Taipei City, cht.com.tw
 9  220-128-32-69.hinet-ip.hinet.net (220.128.32.69)  210.20 ms  AS3462  China, Taiwan, cht.com.tw
    220-128-32-69.hinet-ip.hinet.net (220.128.32.69)  206.70 ms  AS3462  China, Taiwan, cht.com.tw
    220-128-32-69.hinet-ip.hinet.net (220.128.32.69)  207.71 ms  AS3462  China, Taiwan, cht.com.tw
10  dns.hinet.net (168.95.1.1)  205.88 ms  AS3462  China, Taiwan, cht.com.tw
    dns.hinet.net (168.95.1.1)  205.90 ms  AS3462  China, Taiwan, cht.com.tw
    dns.hinet.net (168.95.1.1)  205.90 ms  AS3462  China, Taiwan, cht.com.tw
```

```
**  TW, FETNet ( 139.175.1.1) **

traceroute to 139.175.1.1 (139.175.1.1), 30 hops max, 32 byte packets
 1  5.255.107.2  0.30 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.33 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.24 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  0.51 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.59 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.77 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  1.26 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.35 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.56 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  ix-et-9-1-2-0.tcore1.ad1-amsterdam.as6453.net (80.231.80.65)  2.03 ms  AS6453  Netherlands, North Holland, Amsterdam, tatacommunications.com
    ix-et-9-1-2-0.tcore1.ad1-amsterdam.as6453.net (80.231.80.65)  2.10 ms  AS6453  Netherlands, North Holland, Amsterdam, tatacommunications.com
    ix-et-9-1-2-0.tcore1.ad1-amsterdam.as6453.net (80.231.80.65)  2.25 ms  AS6453  Netherlands, North Holland, Amsterdam, tatacommunications.com
 5  *
    *
    *
 6  if-ae-2-2.tcore2.av2-amsterdam.as6453.net (195.219.194.6)  137.76 ms  AS6453  Netherlands, North Holland, Amsterdam, tatacommunications.com
    *
    *
 7  *
    if-ae-14-2.tcore2.l78-london.as6453.net (80.231.131.160)  148.82 ms  AS6453  United Kingdom, London, tatacommunications.com
    *
 8  *
    if-ae-18-2.tcore1.nto-newyork.as6453.net (80.231.131.73)  130.91 ms  AS6453  United States, New York, New York City, tatacommunications.com
    *
 9  *
    if-ae-12-2.tcore1.sqn-sanjose.as6453.net (63.243.128.29)  139.13 ms  AS6453  United States, California, San Jose, tatacommunications.com
    if-ae-12-2.tcore1.sqn-sanjose.as6453.net (63.243.128.29)  139.74 ms  AS6453  United States, California, San Jose, tatacommunications.com
10  i-91.tpei02.telstraglobal.net (202.84.137.253)  284.20 ms  AS4637  China, Taiwan, Taipei City, telstra.com
    i-91.tpei02.telstraglobal.net (202.84.137.253)  283.11 ms  AS4637  China, Taiwan, Taipei City, telstra.com
    i-91.tpei02.telstraglobal.net (202.84.137.253)  283.68 ms  AS4637  China, Taiwan, Taipei City, telstra.com
11  unknown.telstraglobal.net (210.176.136.111)  227.56 ms  AS4637  China, Taiwan, Taipei City, telstra.com
    unknown.telstraglobal.net (210.176.136.111)  221.02 ms  AS4637  China, Taiwan, Taipei City, telstra.com
    unknown.telstraglobal.net (210.176.136.111)  223.01 ms  AS4637  China, Taiwan, Taipei City, telstra.com
12  r56-142.seed.net.tw (139.175.56.142)  220.94 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
    r56-142.seed.net.tw (139.175.56.142)  224.55 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
    r56-142.seed.net.tw (139.175.56.142)  222.96 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
13  h90-192-72-49.seed.net.tw (192.72.49.90)  225.06 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
    h90-192-72-49.seed.net.tw (192.72.49.90)  224.29 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
    h90-192-72-49.seed.net.tw (192.72.49.90)  224.41 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
14  frd01.seed.net.tw (139.175.1.1)  224.15 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
    frd01.seed.net.tw (139.175.1.1)  228.98 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
    frd01.seed.net.tw (139.175.1.1)  226.33 ms  AS4780  China, Taiwan, Taipei City, fetnet.net
```

```
**  TW, APTG ( 203.79.224.10) **

traceroute to 203.79.224.10 (203.79.224.10), 30 hops max, 32 byte packets
 1  5.255.107.2  0.34 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.26 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.33 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  45.83.173.3  1.34 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
    45.83.173.3  1.46 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
    45.83.173.3  1.27 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
 3  shadow-router.ams.seabone.net (195.22.213.198)  1.31 ms  AS6762  Netherlands, North Holland, Amsterdam, tisparkle.com
    shadow-router.ams.seabone.net (195.22.213.198)  1.40 ms  AS6762  Netherlands, North Holland, Amsterdam, tisparkle.com
    shadow-router.ams.seabone.net (195.22.213.198)  1.34 ms  AS6762  Netherlands, North Holland, Amsterdam, tisparkle.com
 4  ae29.londra32.lon.seabone.net (195.22.209.198)  15.92 ms  AS6762  United Kingdom, London, tisparkle.com
    ae29.londra32.lon.seabone.net (195.22.209.198)  15.87 ms  AS6762  United Kingdom, London, tisparkle.com
    ae29.londra32.lon.seabone.net (195.22.209.198)  15.98 ms  AS6762  United Kingdom, London, tisparkle.com
 5  i-2-peer.ulco01.pr.telstraglobal.net (134.159.95.229)  17.68 ms  AS4637  United Kingdom, London, telstra.com
    i-2-peer.ulco01.pr.telstraglobal.net (134.159.95.229)  16.77 ms  AS4637  United Kingdom, London, telstra.com
    i-2-peer.ulco01.pr.telstraglobal.net (134.159.95.229)  16.63 ms  AS4637  United Kingdom, London, telstra.com
 6  i-1001.ulhc-core02.telstraglobal.net (202.84.178.70)  16.79 ms  AS4637  United Kingdom, London, telstra.com
    i-1001.ulhc-core02.telstraglobal.net (202.84.178.70)  16.76 ms  AS4637  United Kingdom, London, telstra.com
    i-1001.ulhc-core02.telstraglobal.net (202.84.178.70)  16.78 ms  AS4637  United Kingdom, London, telstra.com
 7  202.84.249.1  152.90 ms  AS4637  United States, California, Los Angeles, telstra.com
    202.84.249.1  153.80 ms  AS4637  United States, California, Los Angeles, telstra.com
    202.84.249.1  154.58 ms  AS4637  United States, California, Los Angeles, telstra.com
 8  202.84.249.1  308.66 ms  AS4637  United States, California, Los Angeles, telstra.com
    202.84.249.1  308.17 ms  AS4637  United States, California, Los Angeles, telstra.com
    202.84.249.1  307.69 ms  AS4637  United States, California, Los Angeles, telstra.com
 9  i-14205.jtha-core02.telstraglobal.net (202.84.141.201)  305.56 ms  AS4637  Japan, Tokyo, telstra.com
    i-14205.jtha-core02.telstraglobal.net (202.84.141.201)  307.09 ms  AS4637  Japan, Tokyo, telstra.com
    i-14205.jtha-core02.telstraglobal.net (202.84.141.201)  307.06 ms  AS4637  Japan, Tokyo, telstra.com
10  i-14205.jtha-core02.telstraglobal.net (202.84.141.201)  305.16 ms  AS4637  Japan, Tokyo, telstra.com
    i-14205.jtha-core02.telstraglobal.net (202.84.141.201)  304.42 ms  AS4637  Japan, Tokyo, telstra.com
    i-14205.jtha-core02.telstraglobal.net (202.84.141.201)  302.98 ms  AS4637  Japan, Tokyo, telstra.com
11  i-13642.tpei-core01.telstraglobal.net (202.84.140.202)  306.42 ms  AS4637  China, Taiwan, Taipei City, telstra.com
    i-13642.tpei-core01.telstraglobal.net (202.84.140.202)  307.86 ms  AS4637  China, Taiwan, Taipei City, telstra.com
    i-13642.tpei-core01.telstraglobal.net (202.84.140.202)  305.15 ms  AS4637  China, Taiwan, Taipei City, telstra.com
12  i-92.tpei02.telstraglobal.net (202.84.137.250)  302.78 ms  AS4637  China, Taiwan, Taipei City, telstra.com
    i-92.tpei02.telstraglobal.net (202.84.137.250)  302.75 ms  AS4637  China, Taiwan, Taipei City, telstra.com
    i-92.tpei02.telstraglobal.net (202.84.137.250)  302.73 ms  AS4637  China, Taiwan, Taipei City, telstra.com
13  unknown.telstraglobal.net (210.176.44.14)  308.33 ms  AS4637  China, Taiwan, Taipei City, telstra.com
    unknown.telstraglobal.net (210.176.44.14)  309.66 ms  AS4637  China, Taiwan, Taipei City, telstra.com
    unknown.telstraglobal.net (210.176.44.14)  309.12 ms  AS4637  China, Taiwan, Taipei City, telstra.com
14  203-79-253-161.ebix.net.tw (203.79.253.161)  302.60 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
    203-79-253-161.ebix.net.tw (203.79.253.161)  302.66 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
    203-79-253-161.ebix.net.tw (203.79.253.161)  302.80 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
15  IL203-79-251-46.static.apol.com.tw (203.79.251.46)  299.76 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
    IL203-79-251-46.static.apol.com.tw (203.79.251.46)  299.87 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
    IL203-79-251-46.static.apol.com.tw (203.79.251.46)  299.69 ms  AS17709  China, Taiwan, Taipei City, aptg.com.tw
16  *
    *
    *
17  dns.octor.com (203.79.224.10)  298.61 ms  AS9311  China, Taiwan, Taipei City, aptg.com.tw
    dns.octor.com (203.79.224.10)  298.39 ms  AS9311  China, Taiwan, Taipei City, aptg.com.tw
    dns.octor.com (203.79.224.10)  298.43 ms  AS9311  China, Taiwan, Taipei City, aptg.com.tw
```

```
**  TW, SoNET ( 61.64.127.1) **

traceroute to 61.64.127.1 (61.64.127.1), 30 hops max, 32 byte packets
 1  5.255.107.2  0.26 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.42 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.64 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  0.66 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.61 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.53 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  1.14 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  5.43 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.17 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  ae1-499.RT.SRV.DRO.NL.retn.net (87.245.246.50)  0.52 ms  AS9002  Netherlands, Flevoland, Dronten, retn.net
    ae1-499.RT.SRV.DRO.NL.retn.net (87.245.246.50)  0.64 ms  AS9002  Netherlands, Flevoland, Dronten, retn.net
    ae1-499.RT.SRV.DRO.NL.retn.net (87.245.246.50)  0.58 ms  AS9002  Netherlands, Flevoland, Dronten, retn.net
 5  ae2-2.RT.EQX.SIN.SG.retn.net (87.245.234.83)  163.37 ms  AS9002  Singapore, retn.net
    ae2-2.RT.EQX.SIN.SG.retn.net (87.245.234.83)  204.37 ms  AS9002  Singapore, retn.net
    ae2-2.RT.EQX.SIN.SG.retn.net (87.245.234.83)  168.60 ms  AS9002  Singapore, retn.net
 6  9505.sgw.equinix.com (27.111.228.63)  151.44 ms  AS3491  Singapore, equinix.com
    9505.sgw.equinix.com (27.111.228.63)  171.73 ms  AS3491  Singapore, equinix.com
    9505.sgw.equinix.com (27.111.228.63)  151.56 ms  AS3491  Singapore, equinix.com
 7  203-78-181-173.twgate-ip.twgate.net (203.78.181.173)  198.69 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    203-78-181-173.twgate-ip.twgate.net (203.78.181.173)  198.83 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    203-78-181-173.twgate-ip.twgate.net (203.78.181.173)  200.29 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 8  175-41-60-221.twgate-ip.twgate.net (175.41.60.221)  199.06 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    175-41-60-221.twgate-ip.twgate.net (175.41.60.221)  198.87 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    175-41-60-221.twgate-ip.twgate.net (175.41.60.221)  198.95 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 9  175-41-63-86.twgate-ip.twgate.net (175.41.63.86)  197.67 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    175-41-63-86.twgate-ip.twgate.net (175.41.63.86)  199.08 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    175-41-63-86.twgate-ip.twgate.net (175.41.63.86)  200.89 ms  AS9505  China, Taiwan, Taipei City, twgate.net
10  219.84.176.122  198.16 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    219.84.176.122  198.35 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    219.84.176.122  200.05 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
11  219.84.176.142  214.01 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    219.84.176.142  211.36 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    219.84.176.142  214.36 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
12  gw.so-net.net.tw (61.64.127.249)  198.62 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    *
    *
13  gw.so-net.net.tw (61.64.127.249)  199.34 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    gw.so-net.net.tw (61.64.127.249)  199.86 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    gw.so-net.net.tw (61.64.127.249)  200.52 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
14  gw.so-net.net.tw (61.64.127.249)  198.80 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    gw.so-net.net.tw (61.64.127.249)  199.33 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    gw.so-net.net.tw (61.64.127.249)  200.98 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
15  ns1.so-net.net.tw (61.64.127.1)  202.30 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    ns1.so-net.net.tw (61.64.127.1)  199.36 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
    ns1.so-net.net.tw (61.64.127.1)  199.42 ms  AS18182  China, Taiwan, Taipei City, so-net.net.tw
```

```
**  TW, TFN ( 219.87.66.1) **

traceroute to 219.87.66.1 (219.87.66.1), 30 hops max, 32 byte packets
 1  5.255.107.2  0.60 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.31 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.55 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  45.83.173.3  1.48 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
    45.83.173.3  1.29 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
    45.83.173.3  1.48 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
 3  45.83.172.5  18.59 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
    45.83.172.5  1.40 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
    45.83.172.5  5.81 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
 4  87.245.215.180  2.25 ms  AS9002  Europe Regions, retn.net
    87.245.215.180  11.86 ms  AS9002  Europe Regions, retn.net
    87.245.215.180  1.52 ms  AS9002  Europe Regions, retn.net
 5  ae3-5.RT.EQX.SIN.SG.retn.net (87.245.232.113)  155.50 ms  AS9002  Singapore, retn.net
    ae3-5.RT.EQX.SIN.SG.retn.net (87.245.232.113)  155.43 ms  AS9002  Singapore, retn.net
    ae3-5.RT.EQX.SIN.SG.retn.net (87.245.232.113)  155.46 ms  AS9002  Singapore, retn.net
 6  9505.sgw.equinix.com (27.111.228.63)  156.21 ms  AS3491  Singapore, equinix.com
    9505.sgw.equinix.com (27.111.228.63)  155.83 ms  AS3491  Singapore, equinix.com
    9505.sgw.equinix.com (27.111.228.63)  164.41 ms  AS3491  Singapore, equinix.com
 7  203-78-181-37.twgate-ip.twgate.net (203.78.181.37)  208.88 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    203-78-181-37.twgate-ip.twgate.net (203.78.181.37)  204.63 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    203-78-181-37.twgate-ip.twgate.net (203.78.181.37)  203.46 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 8  175-41-61-174.twgate-ip.twgate.net (175.41.61.174)  204.07 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    175-41-61-174.twgate-ip.twgate.net (175.41.61.174)  204.02 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    175-41-61-174.twgate-ip.twgate.net (175.41.61.174)  204.00 ms  AS9505  China, Taiwan, Taipei City, twgate.net
 9  175-41-60-174.twgate-ip.twgate.net (175.41.60.174)  218.17 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    175-41-60-174.twgate-ip.twgate.net (175.41.60.174)  217.16 ms  AS9505  China, Taiwan, Taipei City, twgate.net
    175-41-60-174.twgate-ip.twgate.net (175.41.60.174)  217.22 ms  AS9505  China, Taiwan, Taipei City, twgate.net
10  60-199-14-242.static.tfn.net.tw (60.199.14.242)  217.39 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
    60-199-14-242.static.tfn.net.tw (60.199.14.242)  217.35 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
    60-199-14-242.static.tfn.net.tw (60.199.14.242)  217.22 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
11  219-87-66-1.static.tfn.net.tw (219.87.66.1)  218.25 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
    219-87-66-1.static.tfn.net.tw (219.87.66.1)  216.93 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
    219-87-66-1.static.tfn.net.tw (219.87.66.1)  217.06 ms  AS9924  China, Taiwan, Taipei City, twmbroadband.com
```

```
**  TW,TAIFO ( 103.31.196.1) **

traceroute to 103.31.196.1 (103.31.196.1), 30 hops max, 32 byte packets
 1  5.255.107.2  0.34 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.52 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  3.61 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  45.83.173.3  1.50 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
    45.83.173.3  1.36 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
    45.83.173.3  1.24 ms  AS42156  Netherlands, North Holland, Amsterdam, netnova.nl
 3  shadow-router.ams.seabone.net (195.22.213.198)  1.33 ms  AS6762  Netherlands, North Holland, Amsterdam, tisparkle.com
    shadow-router.ams.seabone.net (195.22.213.198)  1.92 ms  AS6762  Netherlands, North Holland, Amsterdam, tisparkle.com
    shadow-router.ams.seabone.net (195.22.213.198)  1.33 ms  AS6762  Netherlands, North Holland, Amsterdam, tisparkle.com
 4  ae10.paloalto2.pao.seabone.net (195.22.206.148)  260.69 ms  AS6762  United States, California, Palo Alto, tisparkle.com
    ae10.paloalto2.pao.seabone.net (195.22.206.148)  255.62 ms  AS6762  United States, California, Palo Alto, tisparkle.com
    ae10.paloalto2.pao.seabone.net (195.22.206.148)  250.73 ms  AS6762  United States, California, Palo Alto, tisparkle.com
 5  pa-r32.us.hinet.net (202.39.82.54)  256.03 ms  AS9680  United States, California, Palo Alto, cht.com.tw
    pa-r32.us.hinet.net (202.39.82.54)  245.10 ms  AS9680  United States, California, Palo Alto, cht.com.tw
    pa-r32.us.hinet.net (202.39.82.54)  238.35 ms  AS9680  United States, California, Palo Alto, cht.com.tw
 6  pa-r31.us.hinet.net (202.39.84.29)  261.98 ms  AS9680  United States, California, Palo Alto, cht.com.tw
    pa-r31.us.hinet.net (202.39.84.29)  245.70 ms  AS9680  United States, California, Palo Alto, cht.com.tw
    pa-r31.us.hinet.net (202.39.84.29)  222.06 ms  AS9680  United States, California, Palo Alto, cht.com.tw
 7  r4001-s2.tp.hinet.net (202.39.91.58)  367.95 ms  AS9680  China, Taiwan, Taipei City, cht.com.tw
    r4001-s2.tp.hinet.net (202.39.91.58)  380.27 ms  AS9680  China, Taiwan, Taipei City, cht.com.tw
    r4001-s2.tp.hinet.net (202.39.91.58)  378.79 ms  AS9680  China, Taiwan, Taipei City, cht.com.tw
 8  *
    *
    *
 9  tpdt-3032.hinet.net (220.128.7.118)  244.33 ms  *  China, Taiwan, Taipei City, cht.com.tw
    tpdt-3032.hinet.net (220.128.7.118)  244.44 ms  *  China, Taiwan, Taipei City, cht.com.tw
    tpdt-3032.hinet.net (220.128.7.118)  244.25 ms  *  China, Taiwan, Taipei City, cht.com.tw
10  220-128-1-153.hinet-ip.hinet.net (220.128.1.153)  241.31 ms  *  China, Taiwan, Taipei City, cht.com.tw
    220-128-1-153.hinet-ip.hinet.net (220.128.1.153)  241.35 ms  *  China, Taiwan, Taipei City, cht.com.tw
    220-128-1-153.hinet-ip.hinet.net (220.128.1.153)  241.31 ms  *  China, Taiwan, Taipei City, cht.com.tw
11  210-242-214-5.hinet-ip.hinet.net (210.242.214.5)  227.79 ms  AS3462  China, Taiwan, Taipei City, cht.com.tw
    210-242-214-5.hinet-ip.hinet.net (210.242.214.5)  227.75 ms  AS3462  China, Taiwan, Taipei City, cht.com.tw
    210-242-214-5.hinet-ip.hinet.net (210.242.214.5)  228.62 ms  AS3462  China, Taiwan, Taipei City, cht.com.tw
12  *
    *
    *
13  103.31.197.66  224.79 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
    103.31.197.66  224.80 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
    103.31.197.66  224.88 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
14  103.31.196.1  228.91 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
    103.31.196.1  228.70 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
    103.31.196.1  228.14 ms  AS131584  China, Taiwan, Taipei City, taifo.com.tw
```

```
**  北京电信 ( 219.141.147.210) **

traceroute to 219.141.147.210 (219.141.147.210), 30 hops max, 32 byte packets
 1  5.255.107.2  0.43 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.52 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.27 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  0.71 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.72 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.72 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  1.26 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.52 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.42 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  *
    *
    *
 5  be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  184.37 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.92 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.60 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 6  be3198.rcr21.b031955-0.ams03.atlas.cogentco.com (154.54.57.78)  3.70 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3198.rcr21.b031955-0.ams03.atlas.cogentco.com (154.54.57.78)  3.79 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3198.rcr21.b031955-0.ams03.atlas.cogentco.com (154.54.57.78)  3.63 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 7  chinatelecom.demarc.cogentco.com (149.29.1.130)  56.76 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    chinatelecom.demarc.cogentco.com (149.29.1.130)  61.90 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    chinatelecom.demarc.cogentco.com (149.29.1.130)  59.20 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 8  *
    *
    202.97.36.29  261.11 ms  AS4134  China, Beijing, ChinaTelecom
 9  *
    *
    *
10  *
    *
    *
11  *
    *
    *
12  6.254.120.106.static.bjtelecom.net (106.120.254.6)  254.02 ms  AS4847  China, Beijing, ChinaTelecom
    6.254.120.106.static.bjtelecom.net (106.120.254.6)  245.89 ms  AS4847  China, Beijing, ChinaTelecom
    6.254.120.106.static.bjtelecom.net (106.120.254.6)  234.12 ms  AS4847  China, Beijing, ChinaTelecom
13  bj141-147-210.bjtelecom.net (219.141.147.210)  210.41 ms  AS4847  China, Beijing, ChinaTelecom
    bj141-147-210.bjtelecom.net (219.141.147.210)  207.17 ms  AS4847  China, Beijing, ChinaTelecom
    bj141-147-210.bjtelecom.net (219.141.147.210)  218.78 ms  AS4847  China, Beijing, ChinaTelecom
```

```
**  上海电信 ( 202.96.209.133) **

traceroute to 202.96.209.133 (202.96.209.133), 30 hops max, 32 byte packets
 1  5.255.107.2  0.33 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.52 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.33 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  0.67 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.63 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.68 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  1.29 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.39 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.30 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  *
    *
    *
 5  be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.71 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.76 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.78 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 6  be3198.rcr21.b031955-0.ams03.atlas.cogentco.com (154.54.57.78)  3.48 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3198.rcr21.b031955-0.ams03.atlas.cogentco.com (154.54.57.78)  3.72 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3198.rcr21.b031955-0.ams03.atlas.cogentco.com (154.54.57.78)  3.47 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 7  chinatelecom.demarc.cogentco.com (149.29.1.130)  41.78 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    chinatelecom.demarc.cogentco.com (149.29.1.130)  54.82 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    chinatelecom.demarc.cogentco.com (149.29.1.130)  44.72 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 8  *
    *
    *
 9  202.97.33.133  190.63 ms  AS4134  China, Shanghai, ChinaTelecom
    202.97.33.133  203.40 ms  AS4134  China, Shanghai, ChinaTelecom
    202.97.33.133  224.30 ms  AS4134  China, Shanghai, ChinaTelecom
10  *
    *
    202.97.57.26  227.83 ms  AS4134  China, Shanghai, ChinaTelecom
11  61.152.25.17  249.81 ms  AS4812  China, Shanghai, ChinaTelecom
    61.152.25.17  250.88 ms  AS4812  China, Shanghai, ChinaTelecom
    61.152.25.17  242.94 ms  AS4812  China, Shanghai, ChinaTelecom
12  180.169.255.122  244.89 ms  AS4812  China, Shanghai, ChinaTelecom
    180.169.255.122  250.48 ms  AS4812  China, Shanghai, ChinaTelecom
    *
13  ns-pd.online.sh.cn (202.96.209.133)  244.08 ms  AS4812  China, Shanghai, ChinaTelecom
    ns-pd.online.sh.cn (202.96.209.133)  236.29 ms  AS4812  China, Shanghai, ChinaTelecom
    ns-pd.online.sh.cn (202.96.209.133)  223.55 ms  AS4812  China, Shanghai, ChinaTelecom
```

```
**  深圳电信 ( 58.60.188.222) **

traceroute to 58.60.188.222 (58.60.188.222), 30 hops max, 32 byte packets
 1  5.255.107.2  8.66 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.30 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.36 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  0.71 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.63 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.68 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  1.65 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.39 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.51 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  *
    *
    *
 5  be3457.ccr41.ams03.atlas.cogentco.com (130.117.1.9)  2.51 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3457.ccr41.ams03.atlas.cogentco.com (130.117.1.9)  67.77 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3457.ccr41.ams03.atlas.cogentco.com (130.117.1.9)  2.39 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 6  be3197.rcr21.b031955-0.ams03.atlas.cogentco.com (154.54.56.154)  3.93 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3197.rcr21.b031955-0.ams03.atlas.cogentco.com (154.54.56.154)  3.71 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3197.rcr21.b031955-0.ams03.atlas.cogentco.com (154.54.56.154)  3.88 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 7  chinatelecom.demarc.cogentco.com (149.29.1.130)  38.12 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    chinatelecom.demarc.cogentco.com (149.29.1.130)  35.03 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    chinatelecom.demarc.cogentco.com (149.29.1.130)  32.22 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 8  202.97.13.25  230.08 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
    202.97.13.25  199.62 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
    202.97.13.25  205.78 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
 9  *
    *
    *
10  202.97.66.169  248.09 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
    202.97.66.169  240.39 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
    202.97.66.169  253.37 ms  AS4134  China, Guangdong, Guangzhou, ChinaTelecom
11  202.105.158.41  253.97 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
    202.105.158.41  236.54 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
    *
12  *
    *
    *
13  58.60.188.222  241.09 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
    58.60.188.222  230.24 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
    58.60.188.222  234.70 ms  AS4134  China, Guangdong, Shenzhen, ChinaTelecom
```

```
**  北京联通 ( 202.106.50.1) **

traceroute to 202.106.50.1 (202.106.50.1), 30 hops max, 32 byte packets
 1  5.255.107.2  0.40 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.46 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.34 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  0.55 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  1.53 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.64 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  1.48 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.41 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.19 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  *
    *
    *
 5  be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.70 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.49 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.52 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 6  be2814.ccr42.fra03.atlas.cogentco.com (130.117.0.142)  9.95 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2814.ccr42.fra03.atlas.cogentco.com (130.117.0.142)  9.94 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2814.ccr42.fra03.atlas.cogentco.com (130.117.0.142)  9.93 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 7  be3187.agr41.fra03.atlas.cogentco.com (130.117.1.117)  9.95 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be3187.agr41.fra03.atlas.cogentco.com (130.117.1.117)  10.05 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be3187.agr41.fra03.atlas.cogentco.com (130.117.1.117)  11.65 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 8  *
    *
    149.11.181.26  9.78 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 9  219.158.15.157  140.36 ms  AS4837  China, Beijing, ChinaUnicom
    219.158.15.157  137.61 ms  AS4837  China, Beijing, ChinaUnicom
    219.158.15.157  142.91 ms  AS4837  China, Beijing, ChinaUnicom
10  219.158.3.49  136.60 ms  AS4837  China, Beijing, ChinaUnicom
    219.158.3.49  134.08 ms  AS4837  China, Beijing, ChinaUnicom
    219.158.3.49  130.73 ms  AS4837  China, Beijing, ChinaUnicom
11  *
    *
    *
12  *
    124.65.194.26  135.55 ms  AS4808  China, Beijing, ChinaUnicom
    124.65.194.26  139.35 ms  AS4808  China, Beijing, ChinaUnicom
13  202.106.50.1  149.83 ms  AS4808  China, Beijing, ChinaUnicom
    202.106.50.1  149.87 ms  AS4808  China, Beijing, ChinaUnicom
    202.106.50.1  149.87 ms  AS4808  China, Beijing, ChinaUnicom
```

```
**  上海联通 ( 210.22.97.1) **

traceroute to 210.22.97.1 (210.22.97.1), 30 hops max, 32 byte packets
 1  5.255.107.2  0.33 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.58 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.34 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  0.60 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.57 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.81 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  0.89 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  0.81 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  0.75 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  *
    *
    *
 5  be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  3.72 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.56 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.70 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 6  be2814.ccr42.fra03.atlas.cogentco.com (130.117.0.142)  10.01 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2814.ccr42.fra03.atlas.cogentco.com (130.117.0.142)  10.67 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2814.ccr42.fra03.atlas.cogentco.com (130.117.0.142)  11.72 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 7  be2846.rcr22.fra06.atlas.cogentco.com (154.54.37.30)  10.19 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2846.rcr22.fra06.atlas.cogentco.com (154.54.37.30)  9.98 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2846.rcr22.fra06.atlas.cogentco.com (154.54.37.30)  31.57 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 8  be2844.agr21.fra06.atlas.cogentco.com (130.117.0.30)  9.40 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2844.agr21.fra06.atlas.cogentco.com (130.117.0.30)  9.56 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2844.agr21.fra06.atlas.cogentco.com (130.117.0.30)  9.53 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 9  be3167.nr51.b037206-0.fra06.atlas.cogentco.com (154.25.14.78)  10.11 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be3167.nr51.b037206-0.fra06.atlas.cogentco.com (154.25.14.78)  10.02 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be3167.nr51.b037206-0.fra06.atlas.cogentco.com (154.25.14.78)  10.04 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
10  149.11.84.210  10.38 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    149.11.84.210  10.29 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    149.11.84.210  10.28 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
11  219.158.14.189  166.91 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
    219.158.14.189  168.67 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
    219.158.14.189  170.00 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
12  219.158.24.133  165.15 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
    219.158.24.133  162.76 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
    219.158.24.133  167.65 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
13  219.158.97.1  167.48 ms  AS4837  China, Guangdong, Guangzhou, ChinaUnicom
    *
    *
14  *
    *
    *
15  *
    139.226.225.154  175.65 ms  AS17621  China, Shanghai, ChinaUnicom
    *
16  112.64.250.202  188.09 ms  AS17621  China, Shanghai, ChinaUnicom
    112.64.250.202  187.85 ms  AS17621  China, Shanghai, ChinaUnicom
    112.64.250.202  200.13 ms  AS17621  China, Shanghai, ChinaUnicom
17  210.22.97.1  176.94 ms  AS17621  China, Shanghai, ChinaUnicom
    210.22.97.1  177.82 ms  AS17621  China, Shanghai, ChinaUnicom
    210.22.97.1  176.91 ms  AS17621  China, Shanghai, ChinaUnicom
```

```
**  深圳联通 ( 210.21.196.6) **

traceroute to 210.21.196.6 (210.21.196.6), 30 hops max, 32 byte packets
 1  5.255.107.2  0.33 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.24 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.49 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  1.54 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.70 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.60 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  1.54 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.52 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.38 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  ix-et-9-1-2-0.tcore1.ad1-amsterdam.as6453.net (80.231.80.65)  2.14 ms  AS6453  Netherlands, North Holland, Amsterdam, tatacommunications.com
    ix-et-9-1-2-0.tcore1.ad1-amsterdam.as6453.net (80.231.80.65)  2.17 ms  AS6453  Netherlands, North Holland, Amsterdam, tatacommunications.com
    ix-et-9-1-2-0.tcore1.ad1-amsterdam.as6453.net (80.231.80.65)  2.14 ms  AS6453  Netherlands, North Holland, Amsterdam, tatacommunications.com
 5  *
    if-ae-7-3.tcore1.av2-amsterdam.as6453.net (80.231.80.57)  8.13 ms  AS6453  Netherlands, North Holland, Amsterdam, tatacommunications.com
    *
 6  *
    if-ae-6-2.tcore1.fnm-frankfurt.as6453.net (195.219.194.150)  8.85 ms  AS6453  Germany, Hesse, Frankfurt, tatacommunications.com
    if-ae-6-2.tcore1.fnm-frankfurt.as6453.net (195.219.194.150)  9.88 ms  AS6453  Germany, Hesse, Frankfurt, tatacommunications.com
 7  *
    *
    *
 8  *
    *
    *
 9  *
    *
    *
10  *
    *
    *
11  *
    *
    *
12  120.80.144.34  226.20 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
    120.80.144.34  219.11 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
    120.80.144.34  210.29 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
13  dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  189.48 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
    dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  186.58 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
    dns2-ftcg.gdsz.cncnet.net (210.21.196.6)  190.39 ms  AS17623  China, Guangdong, Shenzhen, ChinaUnicom
```

```
**  北京移动 ( 221.179.155.161) **

traceroute to 221.179.155.161 (221.179.155.161), 30 hops max, 32 byte packets
 1  5.255.107.2  0.31 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.28 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.37 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  0.61 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.60 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.65 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  1.17 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.51 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.45 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  ae22-404.ams10.core-backbone.com (5.56.20.169)  2.27 ms  AS201011  Netherlands, North Holland, Amsterdam, core-backbone.com
    ae22-404.ams10.core-backbone.com (5.56.20.169)  2.25 ms  AS201011  Netherlands, North Holland, Amsterdam, core-backbone.com
    ae22-404.ams10.core-backbone.com (5.56.20.169)  2.15 ms  AS201011  Netherlands, North Holland, Amsterdam, core-backbone.com
 5  *
    *
    *
 6  *
    *
    *
 7  *
    *
    *
 8  221.183.89.178  327.43 ms  AS9808  China, Shanghai, ChinaMobile
    221.183.89.178  310.84 ms  AS9808  China, Shanghai, ChinaMobile
    *
 9  *
    *
    *
10  *
    221.183.89.14  336.14 ms  AS9808  China, Shanghai, ChinaMobile
    *
11  *
    *
    *
12  *
    *
    *
13  *
    *
    221.183.110.162  364.45 ms  AS9808  China, Beijing, ChinaMobile
14  *
    *
    *
15  *
    cachedns03.bj.chinamobile.com (221.179.155.161)  393.42 ms  AS56048  China, Beijing, ChinaMobile
    *
```

```
**  上海移动 ( 211.136.112.200) **

traceroute to 211.136.112.200 (211.136.112.200), 30 hops max, 32 byte packets
 1  5.255.107.2  0.42 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  1.13 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  10.70 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  0.66 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.73 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.59 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  1.58 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.52 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.34 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  *
    *
    *
 5  be3457.ccr41.ams03.atlas.cogentco.com (130.117.1.9)  2.62 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3457.ccr41.ams03.atlas.cogentco.com (130.117.1.9)  2.61 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3457.ccr41.ams03.atlas.cogentco.com (130.117.1.9)  2.75 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 6  be2813.ccr41.fra03.atlas.cogentco.com (130.117.0.122)  10.04 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2813.ccr41.fra03.atlas.cogentco.com (130.117.0.122)  10.03 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2813.ccr41.fra03.atlas.cogentco.com (130.117.0.122)  9.94 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 7  be2533.agr22.fra03.atlas.cogentco.com (130.117.48.157)  10.00 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2533.agr22.fra03.atlas.cogentco.com (130.117.48.157)  10.21 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be2533.agr22.fra03.atlas.cogentco.com (130.117.48.157)  10.07 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 8  be3395.nr21.b019066-1.fra03.atlas.cogentco.com (154.25.12.65)  9.98 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be3395.nr21.b019066-1.fra03.atlas.cogentco.com (154.25.12.65)  10.06 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    be3395.nr21.b019066-1.fra03.atlas.cogentco.com (154.25.12.65)  10.08 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
 9  chinamobile.demarc.cogentco.com (149.29.9.162)  15.01 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    chinamobile.demarc.cogentco.com (149.29.9.162)  9.26 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
    chinamobile.demarc.cogentco.com (149.29.9.162)  8.96 ms  AS174  Germany, Hesse, Frankfurt, cogentco.com
10  223.120.10.14  10.11 ms  AS58453  Germany, Hesse, Frankfurt, ChinaMobile
    223.120.10.14  10.10 ms  AS58453  Germany, Hesse, Frankfurt, ChinaMobile
    223.120.10.14  10.12 ms  AS58453  Germany, Hesse, Frankfurt, ChinaMobile
11  223.120.16.142  238.67 ms  AS58453  China, Shanghai, ChinaMobile
    223.120.16.142  238.73 ms  AS58453  China, Shanghai, ChinaMobile
    223.120.16.142  238.67 ms  AS58453  China, Shanghai, ChinaMobile
12  221.183.89.170  230.14 ms  AS9808  China, Shanghai, ChinaMobile
    221.183.89.170  230.45 ms  AS9808  China, Shanghai, ChinaMobile
    221.183.89.170  230.19 ms  AS9808  China, Shanghai, ChinaMobile
13  221.183.89.33  236.74 ms  AS9808  China, Shanghai, ChinaMobile
    221.183.89.33  236.74 ms  AS9808  China, Shanghai, ChinaMobile
    221.183.89.33  236.76 ms  AS9808  China, Shanghai, ChinaMobile
14  221.183.89.10  240.15 ms  AS9808  China, Shanghai, ChinaMobile
    *
    221.183.89.10  240.15 ms  AS9808  China, Shanghai, ChinaMobile
15  *
    *
    *
16  221.181.125.138  238.21 ms  AS24400  China, Shanghai, ChinaMobile
    221.181.125.138  238.26 ms  AS24400  China, Shanghai, ChinaMobile
    221.181.125.138  238.16 ms  AS24400  China, Shanghai, ChinaMobile
17  211.136.112.252  231.77 ms  AS24400  China, Shanghai, ChinaMobile
    211.136.112.252  231.63 ms  AS24400  China, Shanghai, ChinaMobile
    211.136.112.252  231.85 ms  AS24400  China, Shanghai, ChinaMobile
18  211.136.112.200  243.94 ms  AS24400  China, Shanghai, ChinaMobile
    211.136.112.200  243.76 ms  AS24400  China, Shanghai, ChinaMobile
    211.136.112.200  244.13 ms  AS24400  China, Shanghai, ChinaMobile
```

```
**  深圳移动 ( 120.196.165.24) **

traceroute to 120.196.165.24 (120.196.165.24), 30 hops max, 32 byte packets
 1  5.255.107.2  0.33 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.31 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.35 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  4.48 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.55 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.67 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  1.41 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.65 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  1.36 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  *
    *
    *
 5  be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.37 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.47 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3458.ccr42.ams03.atlas.cogentco.com (154.54.39.185)  2.57 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 6  be12266.ccr42.par01.atlas.cogentco.com (154.54.56.174)  86.23 ms  AS174  France, Ile-de-France, Paris, cogentco.com
    be12266.ccr42.par01.atlas.cogentco.com (154.54.56.174)  86.38 ms  AS174  France, Ile-de-France, Paris, cogentco.com
    be12266.ccr42.par01.atlas.cogentco.com (154.54.56.174)  86.19 ms  AS174  France, Ile-de-France, Paris, cogentco.com
 7  be3628.ccr42.jfk02.atlas.cogentco.com (154.54.27.169)  86.68 ms  AS174  United States, New York, New York City, cogentco.com
    be3628.ccr42.jfk02.atlas.cogentco.com (154.54.27.169)  86.60 ms  AS174  United States, New York, New York City, cogentco.com
    be3628.ccr42.jfk02.atlas.cogentco.com (154.54.27.169)  86.83 ms  AS174  United States, New York, New York City, cogentco.com
 8  be2807.ccr42.dca01.atlas.cogentco.com (154.54.40.110)  85.84 ms  AS174  United States, Virginia, Arlington, cogentco.com
    be2807.ccr42.dca01.atlas.cogentco.com (154.54.40.110)  87.73 ms  AS174  United States, Virginia, Arlington, cogentco.com
    be2807.ccr42.dca01.atlas.cogentco.com (154.54.40.110)  85.88 ms  AS174  United States, Virginia, Arlington, cogentco.com
 9  be2113.ccr42.atl01.atlas.cogentco.com (154.54.24.222)  103.06 ms  AS174  United States, Georgia, Atlanta, cogentco.com
    be2113.ccr42.atl01.atlas.cogentco.com (154.54.24.222)  102.66 ms  AS174  United States, Georgia, Atlanta, cogentco.com
    be2113.ccr42.atl01.atlas.cogentco.com (154.54.24.222)  102.68 ms  AS174  United States, Georgia, Atlanta, cogentco.com
10  be2690.ccr42.iah01.atlas.cogentco.com (154.54.28.130)  116.45 ms  AS174  United States, Texas, Houston, cogentco.com
    be2690.ccr42.iah01.atlas.cogentco.com (154.54.28.130)  116.99 ms  AS174  United States, Texas, Houston, cogentco.com
    be2690.ccr42.iah01.atlas.cogentco.com (154.54.28.130)  116.20 ms  AS174  United States, Texas, Houston, cogentco.com
11  be2928.ccr21.elp01.atlas.cogentco.com (154.54.30.162)  131.67 ms  AS174  United States, Texas, El Paso, cogentco.com
    be2928.ccr21.elp01.atlas.cogentco.com (154.54.30.162)  168.06 ms  AS174  United States, Texas, El Paso, cogentco.com
    be2928.ccr21.elp01.atlas.cogentco.com (154.54.30.162)  132.01 ms  AS174  United States, Texas, El Paso, cogentco.com
12  be2929.ccr31.phx01.atlas.cogentco.com (154.54.42.65)  464.96 ms  AS174  United States, Arizona, Phoenix, cogentco.com
    be2929.ccr31.phx01.atlas.cogentco.com (154.54.42.65)  481.50 ms  AS174  United States, Arizona, Phoenix, cogentco.com
    be2929.ccr31.phx01.atlas.cogentco.com (154.54.42.65)  488.61 ms  AS174  United States, Arizona, Phoenix, cogentco.com
13  be2931.ccr41.lax01.atlas.cogentco.com (154.54.44.86)  151.66 ms  AS174  United States, California, Los Angeles, cogentco.com
    be2931.ccr41.lax01.atlas.cogentco.com (154.54.44.86)  151.64 ms  AS174  United States, California, Los Angeles, cogentco.com
    be2931.ccr41.lax01.atlas.cogentco.com (154.54.44.86)  152.03 ms  AS174  United States, California, Los Angeles, cogentco.com
14  be3243.ccr41.lax05.atlas.cogentco.com (154.54.27.118)  152.25 ms  AS174  United States, California, Los Angeles, cogentco.com
    be3243.ccr41.lax05.atlas.cogentco.com (154.54.27.118)  151.32 ms  AS174  United States, California, Los Angeles, cogentco.com
    be3243.ccr41.lax05.atlas.cogentco.com (154.54.27.118)  151.88 ms  AS174  United States, California, Los Angeles, cogentco.com
15  38.19.140.98  151.90 ms  AS174  United States, California, Los Angeles, cogentco.com
    38.19.140.98  151.91 ms  AS174  United States, California, Los Angeles, cogentco.com
    38.19.140.98  152.14 ms  AS174  United States, California, Los Angeles, cogentco.com
16  223.118.10.85  153.99 ms  AS58453  United States, California, Los Angeles, ChinaMobile
    223.118.10.85  155.45 ms  AS58453  United States, California, Los Angeles, ChinaMobile
    223.118.10.85  152.79 ms  AS58453  United States, California, Los Angeles, ChinaMobile
17  221.183.30.205  257.82 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    221.183.30.205  274.32 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    221.183.30.205  257.25 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
18  221.183.25.122  256.01 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    221.183.25.122  255.99 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    221.183.25.122  256.10 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
19  221.176.22.157  259.37 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    221.176.22.157  258.87 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    221.176.22.157  258.93 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
20  111.24.14.149  269.66 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    111.24.5.185  267.46 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    111.24.5.193  261.15 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
21  221.183.71.74  299.34 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    221.183.71.74  297.99 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    221.183.71.74  297.70 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
22  221.183.110.170  297.48 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    221.183.110.170  297.92 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
    221.183.110.170  298.96 ms  AS9808  China, Guangdong, Guangzhou, ChinaMobile
23  ns6.gd.cnmobile.net (120.196.165.24)  301.91 ms  AS56040  China, Guangdong, Shenzhen, ChinaMobile
    ns6.gd.cnmobile.net (120.196.165.24)  300.55 ms  AS56040  China, Guangdong, Shenzhen, ChinaMobile
    ns6.gd.cnmobile.net (120.196.165.24)  300.72 ms  AS56040  China, Guangdong, Shenzhen, ChinaMobile
```

```
**  成都教育网 ( 202.112.14.151) **

traceroute to 202.112.14.151 (202.112.14.151), 30 hops max, 32 byte packets
 1  5.255.107.2  2.46 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.27 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
    5.255.107.2  0.51 ms  AS60404  Netherlands, Flevoland, Dronten, theinfrastructure.group
 2  5.255.66.194  1.00 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.73 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
    5.255.66.194  0.58 ms  AS50673  Netherlands, Flevoland, Dronten, serverius.net
 3  185.8.179.33  0.73 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  0.64 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
    185.8.179.33  0.67 ms  AS50673  Netherlands, Drenthe, Meppel, serverius.net
 4  *
    *
    *
 5  be3457.ccr41.ams03.atlas.cogentco.com (130.117.1.9)  2.44 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3457.ccr41.ams03.atlas.cogentco.com (130.117.1.9)  2.54 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
    be3457.ccr41.ams03.atlas.cogentco.com (130.117.1.9)  2.50 ms  AS174  Netherlands, North Holland, Amsterdam, cogentco.com
 6  be12265.ccr41.par01.atlas.cogentco.com (130.117.2.142)  88.32 ms  AS174  France, Ile-de-France, Paris, cogentco.com
    be12265.ccr41.par01.atlas.cogentco.com (130.117.2.142)  86.62 ms  AS174  France, Ile-de-France, Paris, cogentco.com
    be12265.ccr41.par01.atlas.cogentco.com (130.117.2.142)  86.20 ms  AS174  France, Ile-de-France, Paris, cogentco.com
 7  *
    be3095.ccr41.dca01.atlas.cogentco.com (154.54.89.221)  86.28 ms  AS174  United States, Virginia, Arlington, cogentco.com
    be3095.ccr41.dca01.atlas.cogentco.com (154.54.89.221)  86.28 ms  AS174  United States, Virginia, Arlington, cogentco.com
 8  be2112.ccr41.atl01.atlas.cogentco.com (154.54.7.158)  102.26 ms  AS174  United States, Georgia, Atlanta, cogentco.com
    be2112.ccr41.atl01.atlas.cogentco.com (154.54.7.158)  102.38 ms  AS174  United States, Georgia, Atlanta, cogentco.com
    be2112.ccr41.atl01.atlas.cogentco.com (154.54.7.158)  102.77 ms  AS174  United States, Georgia, Atlanta, cogentco.com
 9  be2687.ccr41.iah01.atlas.cogentco.com (154.54.28.70)  115.99 ms  AS174  United States, Texas, Houston, cogentco.com
    be2687.ccr41.iah01.atlas.cogentco.com (154.54.28.70)  116.12 ms  AS174  United States, Texas, Houston, cogentco.com
    be2687.ccr41.iah01.atlas.cogentco.com (154.54.28.70)  115.98 ms  AS174  United States, Texas, Houston, cogentco.com
10  be2927.ccr21.elp01.atlas.cogentco.com (154.54.29.222)  132.69 ms  AS174  United States, Texas, El Paso, cogentco.com
    be2927.ccr21.elp01.atlas.cogentco.com (154.54.29.222)  132.33 ms  AS174  United States, Texas, El Paso, cogentco.com
    be2927.ccr21.elp01.atlas.cogentco.com (154.54.29.222)  132.29 ms  AS174  United States, Texas, El Paso, cogentco.com
11  be2930.ccr32.phx01.atlas.cogentco.com (154.54.42.77)  139.78 ms  AS174  United States, Arizona, Phoenix, cogentco.com
    be2930.ccr32.phx01.atlas.cogentco.com (154.54.42.77)  139.84 ms  AS174  United States, Arizona, Phoenix, cogentco.com
    be2930.ccr32.phx01.atlas.cogentco.com (154.54.42.77)  140.02 ms  AS174  United States, Arizona, Phoenix, cogentco.com
12  be2932.ccr42.lax01.atlas.cogentco.com (154.54.45.162)  155.03 ms  AS174  United States, California, Los Angeles, cogentco.com
    be2932.ccr42.lax01.atlas.cogentco.com (154.54.45.162)  151.59 ms  AS174  United States, California, Los Angeles, cogentco.com
    be2932.ccr42.lax01.atlas.cogentco.com (154.54.45.162)  151.44 ms  AS174  United States, California, Los Angeles, cogentco.com
13  be3360.ccr41.lax04.atlas.cogentco.com (154.54.25.150)  151.49 ms  AS174  United States, California, Los Angeles, cogentco.com
    be3360.ccr41.lax04.atlas.cogentco.com (154.54.25.150)  151.57 ms  AS174  United States, California, Los Angeles, cogentco.com
    be3360.ccr41.lax04.atlas.cogentco.com (154.54.25.150)  152.20 ms  AS174  United States, California, Los Angeles, cogentco.com
14  38.88.196.186  153.83 ms  AS174  United States, California, Los Angeles, cogentco.com
    38.88.196.186  155.58 ms  AS174  United States, California, Los Angeles, cogentco.com
    38.88.196.186  152.61 ms  AS174  United States, California, Los Angeles, cogentco.com
15  101.4.117.169  301.63 ms  AS4538  China, Beijing, CHINAEDU
    101.4.117.169  299.62 ms  AS4538  China, Beijing, CHINAEDU
    101.4.117.169  300.86 ms  AS4538  China, Beijing, CHINAEDU
16  *
    *
    *
17  101.4.118.213  302.94 ms  AS4538  China, Beijing, CHINAEDU
    101.4.118.213  301.55 ms  AS4538  China, Beijing, CHINAEDU
    101.4.118.213  301.91 ms  AS4538  China, Beijing, CHINAEDU
18  101.4.112.14  313.96 ms  AS4538  China, Shaanxi, Xi'an, CHINAEDU
    101.4.112.14  314.13 ms  AS4538  China, Shaanxi, Xi'an, CHINAEDU
    101.4.112.14  325.35 ms  AS4538  China, Shaanxi, Xi'an, CHINAEDU
19  101.4.112.18  340.14 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
    101.4.112.18  328.51 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
    101.4.112.18  342.27 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
20  101.4.116.158  326.42 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
    101.4.116.158  327.13 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
    101.4.116.158  326.69 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
21  *
    202.115.255.2  787.47 ms  AS4538  China, Sichuan, Chengdu, CHINAEDU
    *
22  *
    *
    *
23  *
    *
    *
24  *
    *
    *
25  202.112.14.151  330.30 ms  AS24355  China, Sichuan, Chengdu, CHINAEDU
    202.112.14.151  330.72 ms  AS24355  China, Sichuan, Chengdu, CHINAEDU
    202.112.14.151  330.30 ms  AS24355  China, Sichuan, Chengdu, CHINAEDU
```

## 流媒体解锁

```
============[ Multination ]============
 Dazn:                                  No
 HotStar:                               No
 Disney+:                               Yes (Region: NL)
 Netflix:                               Originals Only
 YouTube Premium:                       Yes (Region: NL)
 Amazon Prime Video:                    Yes (Region: NL)
 TVBAnywhere+:                          Yes
 iQyi Oversea Region:                   INTL
 Viu.com:                               No
 YouTube CDN:                           Amsterdam 
 Netflix Preferred CDN:                 Associated with [RETN Limited] in [Warsaw ]
 Spotify Registration:                  No
 Steam Currency:                        USD
=======================================
==============[ Taiwan ]===============
 KKTV:                                  No
 LiTV:                                  No
 MyVideo:                               No
 4GTV.TV:                               No
 LineTV.TW:                             No
 Hami Video:                            No
 CatchPlay+:                            No
 HBO GO Asia:                           No
 Bahamut Anime:                         Failed (Network Connection)
 Bilibili Taiwan Only:                  No
=======================================
=============[ Hong Kong ]=============
 Now E:                                 No
 Viu.TV:                                No
 MyTVSuper:                             No
 HBO GO Asia:                           No
 BiliBili Hongkong/Macau/Taiwan:        No
=======================================
===============[ Japan ]===============
 DMM:                                   No
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
 VideoMarket:                           No
 FOD(Fuji TV):                          No
 Radiko:                                No
 Karaoke@DAM:                           No
 J:com On Demand:                       No
 ---Game---
 Kancolle Japan:                        No
 Pretty Derby Japan:                    Yes
 Konosuba Fantastic Days:               No
 Princess Connect Re:Dive Japan:        Yes
 World Flipper Japan:                   Yes
 Project Sekai: Colorful Stage:         No
=======================================
===========[ North America ]===========
 FOX:                                   Yes
 Hulu:                                  Failed
 ESPN+:[Sponsored by Jam]               No
 Epix:                                  No
 Starz:                                 No
 Philo:                                 No
 FXNOW:                                 No
 TLC GO:                                Yes
 HBO Max:                               Yes (Region: NL)
 Shudder:                               No
 BritBox:                               Yes
 CW TV:                                 Yes
 NBA TV:                                Yes
 Fubo TV:                               Yes
 Tubi TV:                               No
 Sling TV:                              Yes
 Pluto TV:                              Yes
 Acorn TV:                              Yes
 SHOWTIME:                              Yes
 encoreTVB:                             No
 Funimation:                            Yes (Region: US)
 Discovery+:                            Yes
 Paramount+:                            No
 Peacock TV:                            No
 Popcornflix:                           No
 Crunchyroll:                           No
 Directv Stream:                        No
 KBS American:                          No
 KOCOWA:                                No
 ---CA---
 CBC Gem:                               No
 Crave:                                 No
=======================================
===========[ South America ]===========
 Star+:                                 No
 HBO Max:                               Yes (Region: NL)
 DirecTV Go:                            Yes (Region: REGISTRARSE)
 Funimation:                            Yes (Region: US)
=======================================
===============[ Europe ]==============
 Rakuten TV:                            Yes
 Funimation:                            Yes (Region: US)
 HBO Nordic:                            Failed (Network Connection)
 HBO GO Europe:                         Failed (Network Connection)
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
 videoland:                             No
 NPO Start Plus:                        No
 ---ES---
 HBO Spain:                             Failed (Network Connection)
 PANTAYA:                               No
 ---IT---
 Rai Play:                              Yes
 ---RU---
 Amediateka:                            Yes
 ---PT---
 HBO Portugal:                          Failed (Network Connection)
=======================================
==============[ Oceania ]==============
 NBA TV:                                Yes
 Acorn TV:                              Yes
 SHOWTIME:                              Yes
 BritBox:                               Yes
 Funimation:                            Yes (Region: US)
 Paramount+:                            No
 ---AU---
 Stan:                                  Yes
 Binge:                                 No
 Docplay:                               No
 Channel 7:                             Failed (Network Connection)
 Channel 9:                             No
 Channel 10:                            No
 ABC iView:                             No
 Kayo Sports:                           No
 Optus Sports:                          No
 SBS on Demand:                         No
 ---NZ---
 Neon TV:                               Yes
 SkyGo NZ:                              No
 ThreeNow:                              No
 Maori TV:                              Yes
=======================================
```
