---
title: "Hostbbr ipv6 ipv4 nat VPS"
date: "2023-08-29"
categories: 
  - "vps"
  - "eu"
---

## 套餐

> 1 vCore Intel Xeon E5-1650V3  
> 1 GB DDR4 ECC RAM  
> 1000 GB HDD Raid-6 storage (NVMe Cached)  
> 3000 GB Bandwidth @ 1 Gbps  
> IPv4 NAT (20 ports)  
> IPv6/64  
> Hosted in Falkenstein, Germany  
> $2.5/month $2/month with coupon BUDGETSTORAGE

## 测评

### yabs

```
Basic System Information:
---------------------------------
Uptime     : 0 days, 0 hours, 1 minutes
Processor  : Intel(R) Xeon(R) CPU E5-1650 v3 @ 3.50GHz
CPU cores  : 1 @ 3491.914 MHz
AES-NI     : ✔ Enabled
VM-x/AMD-V : ✔ Enabled
RAM        : 940.8 MiB
Swap       : 1024.0 MiB
Disk       : 1000.0 GiB
Distro     : Debian GNU/Linux 11 (bullseye)
Kernel     : 5.10.0-20-amd64
VM Type    : KVM
IPv4/IPv6  : ✔ Online / ✔ Online

IPv6 Network Information:
---------------------------------
ISP        : Hetzner Online GmbH
ASN        : AS24940 Hetzner Online GmbH
Host       : Hetzner
Location   : Falkenstein, Saxony (SN)
Country    : Germany

fio Disk Speed Tests (Mixed R/W 50/50):
---------------------------------
Block Size | 4k            (IOPS) | 64k           (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 126.17 MB/s  (31.5k) | 1.70 GB/s    (26.6k)
Write      | 126.50 MB/s  (31.6k) | 1.71 GB/s    (26.8k)
Total      | 252.68 MB/s  (63.1k) | 3.42 GB/s    (53.4k)
           |                      |                     
Block Size | 512k          (IOPS) | 1m            (IOPS)
  ------ | --- ---- | ---- ---- 
Read       | 3.18 GB/s     (6.2k) | 3.43 GB/s     (3.3k)
Write      | 3.35 GB/s     (6.5k) | 3.66 GB/s     (3.5k)
Total      | 6.54 GB/s    (12.7k) | 7.10 GB/s     (6.9k)

iperf3 Network Speed Tests (IPv4):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 170 Mbits/sec   | 528 Mbits/sec   | 23.3 ms        
Scaleway        | Paris, FR (10G)           | 932 Mbits/sec   | 924 Mbits/sec   | 24.8 ms        
NovoServe       | North Holland, NL (40G)   | 937 Mbits/sec   | busy            | 12.2 ms        
Uztelecom       | Tashkent, UZ (10G)        | 825 Mbits/sec   | 636 Mbits/sec   | 95.5 ms        
Clouvider       | NYC, NY, US (10G)         | 46.7 Mbits/sec  | 68.9 Mbits/sec  | 85.6 ms        
Clouvider       | Dallas, TX, US (10G)      | 31.4 Mbits/sec  | 49.0 Mbits/sec  | 126 ms         
Clouvider       | Los Angeles, CA, US (10G) | 25.9 Mbits/sec  | 36.8 Mbits/sec  | 146 ms         

iperf3 Network Speed Tests (IPv6):
---------------------------------
Provider        | Location (Link)           | Send Speed      | Recv Speed      | Ping           
----- | ----- | ---- | ---- | ---- 
Clouvider       | London, UK (10G)          | 166 Mbits/sec   | 399 Mbits/sec   | 23.4 ms        
Scaleway        | Paris, FR (10G)           | 919 Mbits/sec   | 836 Mbits/sec   | 21.5 ms        
NovoServe       | North Holland, NL (40G)   | busy            | 919 Mbits/sec   | 12.1 ms        
Uztelecom       | Tashkent, UZ (10G)        | 857 Mbits/sec   | 517 Mbits/sec   | 95.3 ms        
Clouvider       | NYC, NY, US (10G)         | 45.7 Mbits/sec  | 87.8 Mbits/sec  | 85.5 ms        
Clouvider       | Dallas, TX, US (10G)      | 30.9 Mbits/sec  | 44.0 Mbits/sec  | 126 ms         
Clouvider       | Los Angeles, CA, US (10G) | 25.9 Mbits/sec  | 33.2 Mbits/sec  | 145 ms         

Geekbench 6 Benchmark Test:
---------------------------------
Test            | Value                         
                |                               
Single Core     | 918                           
Multi Core      | 728                           
Full Test       | https://browser.geekbench.com/v6/cpu/2424430

YABS completed in 19 min 54 sec
```
