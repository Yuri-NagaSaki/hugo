---
title: "Spaceberg 法国4T 大容量存储服务器测评"
date: "2023-06-11"
categories: 
  - "vps"
  - "eu"
---

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 7 minutes
Processor  : Intel(R) Xeon(R) Gold 6226R CPU @ 2.90GHz
CPU cores  : 4 @ 2893.202 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 1.9 GiB
Swap       : 0.0 KiB
Disk       : 4.0 TiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-20-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : OVH SAS
ASN        : AS16276 OVH SAS
Host       : OVH
Location   : Roubaix, Hauts-de-France (HDF)
Country    : France

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ----
Read       | 446.46 MB/s (111.6k) | 5.59 GB/s    (87.3k)
Write      | 447.64 MB/s (111.9k) | 5.62 GB/s    (87.8k)
Total      | 894.11 MB/s (223.5k) | 11.21 GB/s  (175.2k)
           |                      |
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ----
Read       | 10.11 GB/s   (19.7k) | 14.92 GB/s   (14.5k)
Write      | 10.65 GB/s   (20.8k) | 15.91 GB/s   (15.5k)
Total      | 20.76 GB/s   (40.5k) | 30.84 GB/s   (30.1k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 5.45 Gbits/sec  | 7.73 Gbits/sec  | 4.02 ms
Scaleway        | Paris, FR (10G)           | busy            | 6.97 Gbits/sec  | 4.21 ms
NovoServe       | North Holland, NL (40G)   | 5.49 Gbits/sec  | 6.66 Gbits/sec  | 8.55 ms
Uztelecom       | Tashkent, UZ (10G)        | 3.58 Gbits/sec  | 2.09 Gbits/sec  | 89.1 ms
Clouvider       | NYC, NY, US (10G)         | 1.04 Gbits/sec  | 482 Mbits/sec   | 80.3 ms
Clouvider       | Dallas, TX, US (10G)      | 1.58 Gbits/sec  | 593 Mbits/sec   | 115 ms
Clouvider       | Los Angeles, CA, US (10G) | 1.29 Gbits/sec  | 1.12 Gbits/sec  | 136 ms

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping
----- | ----- | ---- | ---- | ----
Clouvider       | London, UK (10G)          | 5.41 Gbits/sec  | 6.62 Gbits/sec  | 4.03 ms
Scaleway        | Paris, FR (10G)           | 5.49 Gbits/sec  | 6.50 Gbits/sec  | 4.23 ms
NovoServe       | North Holland, NL (40G)   | 5.47 Gbits/sec  | 5.82 Gbits/sec  | 8.59 ms
Uztelecom       | Tashkent, UZ (10G)        | 4.11 Gbits/sec  | 1.83 Gbits/sec  | 89.0 ms
Clouvider       | NYC, NY, US (10G)         | 2.35 Gbits/sec  | 1.73 Gbits/sec  | 80.2 ms
Clouvider       | Dallas, TX, US (10G)      | 1.56 Gbits/sec  | 966 Mbits/sec   | 115 ms
Clouvider       | Los Angeles, CA, US (10G) | 1.28 Gbits/sec  | 1.02 Gbits/sec  | 136 ms

Geekbench 5 Benchmark Test:
---------------------------------
Test            | Value
                |
Single Core     | 1023
Multi Core      | 3882
```
