---
title: "v6Node 4 核 AMD 8GB RAM 10g口测评"
date: "2023-06-07"
categories: 
  - "vps"
  - "eu"
---

## 套餐价格

年付69欧元

![](https://catcat.blog/wp-content/uploads/2023/06/image-1-1024x547.png)

## Yabs

```
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #
#              Yet-Another-Bench-Script              #
#                     v2023-04-23                    #
# https://github.com/masonr/yet-another-bench-script #
# ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## ## #

Mon Jun  6 1:01:23 UTC 2023

Basic System Information:
---------------------------------
Uptime     : 0 days, 24 hours, 45 minutes
Processor  : AMD EPYC 7542 32-Core Processor
CPU cores  : 4 @ 2900.000 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 7.8 GiB
Swap       : 0.0 KiB
Disk       : 68.8 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-23-cloud-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Ian David Klemm
ASN        : AS200461 Ian David Klemm
Host       : Ian David Klemm
Location   : Rotterdam, South Holland (ZH)
Country    : Netherlands

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ----
Read       | 278.13 MB/s  (69.5k) | 3.16 GB/s    (49.5k)
Write      | 278.87 MB/s  (69.7k) | 3.18 GB/s    (49.7k)
Total      | 557.01 MB/s (139.2k) | 6.35 GB/s    (99.2k)
           |                      |
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ----
Read       | 4.71 GB/s     (9.2k) | 8.28 GB/s     (8.0k)
Write      | 4.96 GB/s     (9.7k) | 8.83 GB/s     (8.6k)
Total      | 9.68 GB/s    (18.9k) | 17.11 GB/s   (16.7k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 6.63 Gbits/sec  | 4.38 Gbits/sec  | 12.7 ms
Scaleway        | Paris, FR (10G)           | 6.18 Gbits/sec  | 5.57 Gbits/sec  | 9.73 ms
NovoServe       | North Holland, NL (40G)   | 7.51 Gbits/sec  | 4.11 Gbits/sec  | 7.32 ms
Uztelecom       | Tashkent, UZ (10G)        | 2.24 Gbits/sec  | 899 Mbits/sec   | 76.8 ms
Clouvider       | NYC, NY, US (10G)         | 2.18 Gbits/sec  | busy            | 80.8 ms
Clouvider       | Dallas, TX, US (10G)      | 1.52 Gbits/sec  | 1.37 Gbits/sec  | 115 ms
Clouvider       | Los Angeles, CA, US (10G) | 1.24 Gbits/sec  | 1.31 Gbits/sec  | 145 ms

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 4.88 Gbits/sec  | 6.72 Gbits/sec  | 12.5 ms
Scaleway        | Paris, FR (10G)           | 5.14 Gbits/sec  | 5.96 Gbits/sec  | 11.2 ms
NovoServe       | North Holland, NL (40G)   | 6.93 Gbits/sec  | 6.29 Gbits/sec  | 6.72 ms
Uztelecom       | Tashkent, UZ (10G)        | 2.44 Gbits/sec  | 993 Mbits/sec   | 76.9 ms
Clouvider       | NYC, NY, US (10G)         | 2.10 Gbits/sec  | busy            | 80.3 ms
Clouvider       | Dallas, TX, US (10G)      | 1.13 Gbits/sec  | 1.47 Gbits/sec  | 115 ms
Clouvider       | Los Angeles, CA, US (10G) | 1.35 Gbits/sec  | 1.24 Gbits/sec  | 143 ms

YABS completed in 7 min 34 sec
```

## SpeedTest测试

![](https://cdn.lirica.cn/wordpress/2023/06/image-2-1024x426.png)

## 流媒体解锁测试

```
 ** Checking Results Under IPv4
--------------------------------
 ** Your Network Provider: combahton IT Services (178.251.*.*)


============[ Multination ]============
 Dazn:					No
 HotStar:				No
 Disney+:				No
 Netflix:				Originals Only
 YouTube Premium:			Yes (Region: DE)
 Amazon Prime Video:			Yes (Region: DE)
 TVBAnywhere+:				Yes
 iQyi Oversea Region:			DE
 Viu.com:				No
 YouTube CDN:				Frankfurt
 Netflix Preferred CDN:		Stockholm
 Spotify Registration:			No
 Steam Currency:			EUR
 ChatGPT:				Yes
=======================================
===============[ Europe ]==============
 Rakuten TV:				Yes
 Funimation:				No
 SkyShowTime:				No
 HBO Max:				No
 Maths Spot:				Failed (Network Connection)
 ---GB---
 Sky Go:				Yes
 BritBox:				Yes
 ITV Hub:				No
 Channel 4:				No
 Channel 5:				No
 BBC iPLAYER:				No
 Discovery+ UK:				No
 ---FR---
 Salto:					Failed (Network Connection)
 Canal+:				No
 Molotov:				No
 ---DE---
 Joyn:					Yes
 Sky:					Yes
 ZDF: 					Yes
 ---NL---
 NLZIET:				Failed
 videoland:				Failed (Network Connection)
 NPO Start Plus:			No
 ---ES---
 PANTAYA:				Failed (Network Connection)
 ---IT---
 Rai Play:				Yes
 ---RU---
 Amediateka:				Yes
=======================================
===========[ North America ]===========
 FOX:					No
 Hulu:					Failed
 NFL+:					No
 ESPN+:[Sponsored by Jam]		No
 Epix:					No
 Starz:					No
 Philo:					No
 FXNOW:					No
 TLC GO:				No
 HBO Max:				No
 Shudder:				Yes
 BritBox:				Yes
 Crackle:				No
 CW TV:					No
 A&E TV:				No
 NBA TV:				Yes
 NBC TV:				No
 Fubo TV:				No
 Tubi TV:				No
 Sling TV:				Yes
 Pluto TV:				Yes
 Acorn TV:				Yes
 SHOWTIME:				Yes
 encoreTVB:				No
 Funimation:				No
 Discovery+:				No
 Paramount+:				Yes
 Peacock TV:				No
 Popcornflix:				No
 Crunchyroll:				No
 Directv Stream:			No
 KBS American:				Failed (Network Connection)
 KOCOWA:				No
 Maths Spot:				Failed (Network Connection)
 ---CA---
 CBC Gem:				No
 Crave:					Yes
=======================================
===============[ Sport ]===============
 Dazn:					No
 Star+:					No
 ESPN+:[Sponsored by Jam]		No
 NBA TV:				Yes
 Fubo TV:				No
 Mola TV:				No
 Setanta Sports:			No
 Optus Sports:				No
 Bein Sports Connect:			No
 Eurosport RO:				Yes
=======================================


 ** Checking Results Under IPv6
--------------------------------
 ** Your Network Provider: Ian David Klemm (2a09:bfc7:0:*:*)


============[ Multination ]============
 Dazn:					Failed (Network Connection)
 HotStar:				No
 Disney+:				Yes (Region: NL)
 Netflix:				Yes (Region: DE)
 YouTube Premium:			Yes (Region: DE)
 Amazon Prime Video:			Unsupported
 TVBAnywhere+:				Failed (Network Connection)
 iQyi Oversea Region:			Failed
 Viu.com:				Failed
 YouTube CDN:				Frankfurt
 Netflix Preferred CDN:		Frankfurt
 Spotify Registration:			Yes (Region: NL)
 Steam Currency:			Failed (Network Connection)
 ChatGPT:				Yes
=======================================
===============[ Europe ]==============
 Rakuten TV:				Failed (Network Connection)
 Funimation:				IPv6 Not Support
 SkyShowTime:				Yes (Region: NL)
 HBO Max:				Failed (Network Connection)
 Maths Spot:				IPv6 Not Support
 ---GB---
 Sky Go:				Failed (Network Connection)
 BritBox:				Yes
 ITV Hub:				Failed (Network Connection)
 Channel 4:				Failed (Network Connection)
 Channel 5:				IPv6 Not Support
 BBC iPLAYER:				Failed
 Discovery+ UK:				IPv6 Not Support
 ---FR---
 Salto:					Failed (Network Connection)
 Canal+:				Failed (Network Connection)
 Molotov:				No
 ---DE---
 Joyn:					Failed (Network Connection)
 Sky:					Failed (Network Connection)
 ZDF: 					Failed (Network Connection)
 ---NL---
 NLZIET:				Failed
 videoland:				Failed (Network Connection)
 NPO Start Plus:			Failed (Network Connection)
 ---ES---
 PANTAYA:				Failed (Network Connection)
 ---IT---
 Rai Play:				Failed (Network Connection)
 ---RU---
 Amediateka:				Failed (Network Connection)
=======================================
===========[ North America ]===========
 FOX:					No
 Hulu:					Failed
 NFL+:					IPv6 Not Support
 ESPN+:[Sponsored by Jam]		No
 Epix:					Failed (Network Connection)
 Epix:					Failed
 Starz:					Failed (Network Connection)
 Philo:					IPv6 Not Support
 FXNOW:					IPv6 Not Support
 TLC GO:				IPv6 Not Support
 HBO Max:				Failed (Network Connection)
 Shudder:				No
 BritBox:				Yes
 Crackle:				No
 CW TV:					No
 A&E TV:				IPv6 Not Support
 NBA TV:				Yes
 NBC TV:				No
 Fubo TV:				IPv6 Not Support
 Tubi TV:				No
 Sling TV:				Yes
 Pluto TV:				Yes
 Acorn TV:				Failed (Network Connection)
 SHOWTIME:				Failed (Network Connection)
 encoreTVB:				Failed (Network Connection)
 Funimation:				IPv6 Not Support
 Discovery+:				IPv6 Not Support
 Paramount+:				Yes
 Peacock TV:				No
 Popcornflix:				IPv6 Not Support
 Crunchyroll:				IPv6 Not Support
 Directv Stream:			No
 KBS American:				IPv6 Not Support
 KOCOWA:				IPv6 Not Support
 Maths Spot:				IPv6 Not Support
 ---CA---
 CBC Gem:				Failed (Network Connection)
 Crave:					Failed (Network Connection)
=======================================
===============[ Sport ]===============
 Dazn:					Failed (Network Connection)
 Star+:					No
 ESPN+:[Sponsored by Jam]		No
 NBA TV:				Yes
 Fubo TV:				IPv6 Not Support
 Mola TV:				IPv6 Not Support
 Setanta Sports:			IPv6 Not Support
 Optus Sports:				No
 Bein Sports Connect:			IPv6 Not Support
 Eurosport RO:				IPv6 Not Support
=======================================
```

## OpenAI解锁测试

OpenAI Access Checker. Made by Vincent
https://github.com/missuo/OpenAI-Checker
-------------------------------------
\[IPv4\]
Your IPv4: 178.251.\*.\* - combahton IT Services
Your IP supports access to OpenAI. Region: DE
-------------------------------------
\[IPv6\]
Your IPv6: 2a09:bfc7:0:\*::\* - Ian David Klemm
Your IP supports access to OpenAI. Region: NL
-------------------------------------
