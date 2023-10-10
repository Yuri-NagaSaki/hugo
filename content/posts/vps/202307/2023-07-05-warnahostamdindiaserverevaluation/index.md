---
title: "WarnaHost AMD 印度服务器测评"
date: "2023-07-05"
categories: 
  - "vps"
---

## **Bench**

```
 Version            : v2023-06-10
 Usage              : wget -qO- bench.sh | bash
----------------------------------------------------------------------
 CPU Model          : AMD Ryzen 9 5950X 16-Core Processor
 CPU Cores          : 2 @ 3399.998 MHz
 CPU Cache          : 512 KB
 AES-NI             : Enabled
 VM-x/AMD-V         : Enabled
 Total Disk         : 38.7 GB (2.9 GB Used)
 Total Mem          : 1.9 GB (162.9 MB Used)
 System uptime      : 0 days, 0 hour 50 min
 Load average       : 0.11, 0.30, 0.53
 OS                 : Ubuntu 22.04.2 LTS
 Arch               : x86_64 (64 Bit)
 Kernel             : 5.15.0-76-generic
 TCP CC             : bbr
 Virtualization     : KVM
 IPv4/IPv6          : Online / Offline
 Organization       : AS141120 PT Warna Data Multimedia
 Location           : Jakarta / ID
 Region             : Jakarta
----------------------------------------------------------------------
 I/O Speed(1st run) : 2.3 GB/s
 I/O Speed(2nd run) : 2.4 GB/s
 I/O Speed(3rd run) : 2.8 GB/s
 I/O Speed(average) : 2560.0 MB/s
----------------------------------------------------------------------
 Node Name        Upload Speed      Download Speed      Latency
 Speedtest.net    907.62 Mbps       930.75 Mbps         1.19 ms     
 Los Angeles, US  247.33 Mbps       691.44 Mbps         323.33 ms   
 Dallas, US       278.57 Mbps       619.85 Mbps         289.22 ms   
 Montreal, CA     274.60 Mbps       732.91 Mbps         261.49 ms   
 Paris, FR        310.04 Mbps       646.28 Mbps         253.52 ms   
 Amsterdam, NL    424.06 Mbps       579.91 Mbps         189.34 ms   
 Shanghai, CN     216.35 Mbps       11.78 Mbps          355.37 ms   
 Nanjing, CN      106.21 Mbps       614.60 Mbps         338.09 ms   
 Guangzhou, CN    141.16 Mbps       40.63 Mbps          333.15 ms   
 Hongkong, CN     403.43 Mbps       953.74 Mbps         194.86 ms   
 Singapore, SG    902.40 Mbps       531.00 Mbps         13.11 ms    
 Tokyo, JP        431.47 Mbps       610.05 Mbps         86.17 ms    
----------------------------------------------------------------------
```

## Yabs

```

Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 56 minutes
Processor  : AMD Ryzen 9 5950X 16-Core Processor
CPU cores  : 2 @ 3399.998 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 0.0 KiB
Disk       : 38.7 GiB
Distro     : Ubuntu 22.04.2 LTS
Kernel     : 5.15.0-76-generic
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ❌ Offline

IPv4 Network Information:
---------------------------------
ISP        : PT Warna Data Multimedia
ASN        : AS141120 PT Warna Data Multimedia
Host       : PT Warna Data Multimedia
Location   : Palu, Central Sulawesi (ST)
Country    : Indonesia

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 447.13 MB/s (111.7k) | 3.83 GB/s    (59.9k)
Write      | 448.31 MB/s (112.0k) | 3.85 GB/s    (60.2k)
Total      | 895.45 MB/s (223.8k) | 7.69 GB/s   (120.2k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.74 GB/s     (7.3k) | 3.67 GB/s     (3.5k)
Write      | 3.94 GB/s     (7.7k) | 3.92 GB/s     (3.8k)
Total      | 7.69 GB/s    (15.0k) | 7.59 GB/s     (7.4k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 524 Mbits/sec   | 411 Mbits/sec   | 166 ms
Scaleway        | Paris, FR (10G)           | 548 Mbits/sec   | 289 Mbits/sec   | 180 ms
NovoServe       | North Holland, NL (40G)   | 540 Mbits/sec   | 479 Mbits/sec   | 191 ms
Uztelecom       | Tashkent, UZ (10G)        | 446 Mbits/sec   | 251 Mbits/sec   | 282 ms
Clouvider       | NYC, NY, US (10G)         | 496 Mbits/sec   | 259 Mbits/sec  | 260 ms
Clouvider       | Dallas, TX, US (10G)      | 631 Mbits/sec   | 293 Mbits/sec   | 213 ms
Clouvider       | Los Angeles, CA, US (10G) | 524 Mbits/sec   | 254 Mbits/sec   | 179 ms

YABS completed in 3 min 59 sec
```

## SpeedTest

![](https://2023/07/image-3.png)

## 流媒体检测

```
============[ Multination ]============
 Dazn: Yes (Region: ID)
 HotStar: Yes (Region: ID)
 Disney+: No
 Netflix: Yes (Region: ID)
 YouTube Premium: Yes (Region: ID)
 Amazon Prime Video: Yes (Region: ID)
 TVBAnywhere+: Yes
 iQyi Oversea Region: ID
 Viu.com: Yes (Region: ID)
 YouTube CDN: Associated with [BIZNET]
 Netflix Preferred CDN: Seattle, WA  
 Spotify Registration: Yes (Region: ID)
 Steam Currency: IDR
 ChatGPT: Yes
=======================================
===============[ Sport ]===============
 Dazn: Yes (Region: ID)
 Star+: No
 ESPN+:[Sponsored by Jam] No
 NBA TV: Yes
 Fubo TV: Yes
 Mola TV: Yes
 Setanta Sports: No
 Optus Sports: No
 Bein Sports Connect: No
 Eurosport RO: Yes
===================================================[ Multination ]============
 Dazn:					Yes (Region: ID)
 HotStar:				Yes (Region: ID)
 Disney+:				No
 Netflix:				Yes (Region: ID)
 YouTube Premium:			Yes (Region: ID)
 Amazon Prime Video:			Yes (Region: ID)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			ID
 Viu.com:				Yes (Region: ID)
 YouTube CDN:				Associated with [BIZNET]
 Netflix Preferred CDN:		        Seattle, WA  
 Spotify Registration:			Yes (Region: ID)
 Steam Currency:			IDR
 ChatGPT:				Yes
=======================================
===============[ Sport ]===============
 Dazn:					Yes (Region: ID)
 Star+:					No
 ESPN+:[Sponsored by Jam]		No
 NBA TV:				Yes
 Fubo TV:				Yes
 Mola TV:				Yes
 Setanta Sports:			No
 Optus Sports:				No
 Bein Sports Connect:			No
 Eurosport RO:				Yes
=======================================
 Spotify Registration:			Yes (Region: ID)
 Steam Currency:			IDR
 ChatGPT:				Yes
=======================================
===============[ Sport ]===============
 Dazn:					Yes (Region: ID)
 Star+:					No
 ESPN+:[Sponsored by Jam]		No
 NBA TV:				Yes
 Fubo TV:				Yes
 Mola TV:				Yes
 Setanta Sports:			No
 Optus Sports:				No
 Bein Sports Connect:			No
 Eurosport RO:				Yes
=======================================
```

## [](https://www.speedtest.net/result/c/3faecc9b-5a6a-4467-b886-744654fe10fa)

## OpenAi检测

```
[IPv4]
Your IPv4: 103.189.*.* - PT Warna Data Multimedia
Your IP supports access to OpenAI. Region: ID
-------------------------------------
```

## Geekbench 5

![](https://catcat.blog/wp-content/uploads/2023/07/image-4-1024x295.png)
