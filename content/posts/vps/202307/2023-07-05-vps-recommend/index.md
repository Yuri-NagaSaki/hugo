---
title: "什么值得买-持续更新ing（VPS推荐）"
date: "2023-07-05"
weight: 1
categories: 
  - "vps"
---

> ## 前言
> 
> 经常有朋友会问我 "什么 VPS 适合建站、跑项目"、"什么 VPS 适合用来科学上网"、"什么 VPS 适合离线下载，PT下载" 之类的问题。于是准备写一篇我使用的VPS（什么值得买推荐）。

**PS:这里不会出现CloudCone,Racknerd等超兽王商家的推荐，以下均目前本人所持，长期使用的商家。**

## 项目,建站,性能需求VPS，VDS推荐

这种需求的话，一般对cpu，内存啊都有较大的需求。

### 1.Hybula

荷兰阿弥斯特丹的一个商家，其主要网络坐落在该地，直接连接到 Doetinchem 机房。网络传输由一个大规模的 AS35133 骨干网络提供支持，同时结合了 peering 和 transit，保证了网络的高质量。该公司在阿姆斯特丹的主要数据中心：Equinix、Interxion/ DRE、Nikhef、Iron Mountain等均有业务。该网络目前由CDN77、NovoSrve和ERA-IX上游支持，因此具有接入Arelion（Telia）、Lumen（Level3）、Cogent、NTT、GTT、Core-Backbone、Liberty Global、Telecom Italia Sparkle、HE、AMS-IX、NL-ix、Cloudflare、Google等网络的能力。此外，该服务商还拥有优化到CTGNet（AS23764）、中国电信（AS4134）、中国移动（AS58453）、中国联通（AS4837）等网络的路由，以保障服务畅通。但是由于价格并不便宜，但质量非常优秀，适合建站或者跑项目，提供高达 480G DDos 的保护，口碑很好。但由于价格异常昂贵，不受普通人的喜欢。

#### 相关测试

[Hybula 荷兰 AMD 7950X](https://catcat.blog/hybula-7950x.html)

[Hybula 荷兰 AMD EPYC Milan VPS](https://catcat.blog/hybula-nl-amd-epyc-milan-vps.html)

#### 购买链接

官网地址：[Hybula 官网](https://www.hybula.com/)（无AFF）

促销请关注 [Hybula-lowendtalk](https://lowendtalk.com/profile/discussions/Hybula)

### 2.SpeedyPage

来自英国伦敦的商家，有英国伦敦，美国阿什本，日本东京，新加坡，悉尼机房。每款VPS都有DDoS防护. 承诺 60天退款保证/99.99 SLA/不超售/免费每日备份, 支持PayPal、信用卡、支付宝付款。CPU大多为AMD 5950X ，7950X。IP解锁也还可以。价格适中，经常有9折优惠活动。

#### 相关测试

[SpeedyPage Singapore-5950X](https://catcat.blog/speedypage-sg5950x.html)

[SpeedyPage Tokyo-5950X](https://catcat.blog/speedypage-jp-bench.html)（根据消息，马上要升级为7950x了）

[SpeedyPage Ashburn-7950X](https://catcat.blog/speedypage-7950x-vps.html)

#### 购买链接

官网地址：[SpeedyPage 官网](https://my.speedypage.com/aff.php?aff=190)（含AFF）

促销请关注 [SpeedyPage-lowendtalk](https://lowendtalk.com/profile/speedypage)

### 3.Hetzner

俗称欧洲阿里云，性能钢炮。Hetzner 拥有数十万台服务器，是欧洲最大的数据中心运营商之一。自 1997 年成立以来，Hetzner 一直为私人和企业客户提供强大的托管产品和可靠的 IT 基础设施。通过结合其在创新技术、有吸引力的价格、专家支持和灵活的客户服务方面的优势，Hetzner 在德国和欧洲内外扩大了市场。Hetzner 是一家德国公司，在纽伦堡和法尔肯施泰因（均位于德国）和芬兰赫尔辛基拥有并运营着自己的高科技数据中心，最近又在美国弗吉尼亚州阿什本增设了一个新机房。一共有四个数据中心：德国 2 个，芬兰 1 个，美国 1 个。Hetzner 家的 VPS 和独服价格实惠，性能稳定，NVMe SSD，10Gbp 带宽，支持信用卡、Paypal 付款。就是到国内网络比较慢。AMD EPYC 处理器的 VPS 套餐性能强劲。

#### 相关测试

[Hetzner-Dedicated-VDS-EPYC-9654](https://catcat.blog/hetzner-dedicated.html)

[Hetzner-Shared vCPU-VPS-X86](https://catcat.blog/hetzner%e7%be%8e%e8%a5%bf%e4%bf%84%e5%8b%92%e5%86%88vps%e8%af%84%e6%b5%8b.html)

[Hetzner-Shared vCPU-VPS-ARM](https://catcat.blog/hetzner-arm-%e5%92%8cx86-%e5%af%b9%e6%af%94%e8%af%84%e6%b5%8b.html)

[Hetzner-Dedicated server](https://catcat.blog/hetzner-25%e6%ac%a7%e6%9d%9c%e7%94%ab%e6%b5%8b%e8%af%95.html)

#### 购买链接

官网地址：[Hetzner 官网](https://hetzner.cloud/?ref=5WVbNP94ckFR)（使用该链接首次注册或者购买机器，可以得到 20 欧的试用金（有效期一个月），可以试用各种型号的 VPS）

### 4.Crunchbits

一家 2021 年 11 月 30 日成立的美国主机商，主营 NVMe KVM VPS、EPYC 高频 NVMe VPS、锐龙 5950X NVMe KVM VPS、大硬盘存储、VDS锐龙 7950X 、GPU 显卡服务器和独立服务器，数据中心位于美国 爱达荷州。最近在Low疯狂的促销，生意火爆。

#### 相关测试

[Crunchbits-5950X](https://catcat.blog/crunchbits.html)

[Crunchbits-7950x VDS](https://catcat.blog/crunchbits-17-vds.html)

[Crunchbits Special](https://catcat.blog/crunchbits-special.html)[](http://img.laoda.de/i/2023/02/11/ibby0z-2.webp)

#### 购买链接

官网地址：[Crunchbits 官网](https://crunchbits.com/)（无AFF）

促销请关注 [Crunchbits-lowendtalk](https://lowendtalk.com/profile/crunchbits)

### 5.Liteserver 

2007年的老商家，自有ASN AS60404，主机托管于荷兰Serverius DC1资料中心，有NVMe及HDD可选，均提供1Gbps网络线路，流量会使用完成后会限速10Mbps。Liteserver的性价比很不错，在欧洲的口碑良好。支持NVME和HDD款互相切换，2022年黑五有五折优惠。

#### 相关测试

[Liteserver-NVME](https://catcat.blog/112-2.html)

#### 购买链接

官网地址：[Liteserver官网](https://clients.liteserver.nl/aff.php?aff=621)（有AFF）

## 离线下载 PT下载推荐

对于下载需求分为两类，短期存储和长期存储。通过 VPS 下载中转然后上传到网盘，不需要长期保存，下载完传到网盘就删除，通常一部电影的大小在 5G 左右，一般 VPS 只有 10-20G 左右磁盘容量，除去系统和软件的占用，最多只能 1-2 个任务同时进行。如果有同时下载更多任务的需求，或者需要长期存储，那就需要考虑更大的空间，或者直接上大盘鸡了。

PT下载对网络和内存CPU都有一定的考验，流量消耗极大，常规机器刷力堪忧。

> **BT 下载注意事项：** 其中一些是不抗 DMCA 版权投诉的，搞 BT 下载有被投诉的风险。不过在开启强制加密的情况下可以一定程度规避版权投诉的风险，因为加密后的传输内容是没有人知道的。有一点是需要注意的，国外 BT 资源网站（比如 rarbg）提供的热门新影视、游戏等资源可能是版权方的蜜罐，尤其是那种无中文字幕的资源(俗称生肉)，选择资源时应该尽量避开这种，否则即使是加密也可能会遭到投诉。

### 1.Alwyzon （可刷PT，但注意流量，保种优秀）

奥地利云服务商 Alwyzon，Hohl IT e.U.旗下品牌，主要售卖 KVM 虚拟化的 VPS，大硬盘存储 VPS 和独立服务器，在奥地利最大互联网中心 Interxion 园区内运营所有服务器。欧洲对等互联优秀。

#### 相关测试

[Alwyzon-STORAGE SERVERS](https://catcat.blog/%e5%a5%a5%e5%9c%b0%e5%88%a9%e5%a4%a7%e7%9b%98%e9%b8%a1%e6%b5%8b%e8%af%84.html)

#### 购买链接

官网地址：[Alwyzon 官网](https://www.alwyzon.com/en)（无AFF）

### 2.HostBrr （可刷PT，但注意流量，Hetzner转售）

Hetzner转售商，性价比极高。价格低廉（平均单价 2.2$/1TB），适合保种，离线下载用

#### 相关测试

[Hostbbr ipv6 nat VPS（_E5-1650V3_）](https://catcat.blog/hostbbr.html)

[Hostbbr ipv6 nat VPS （W-2145）](https://catcat.blog/hostbbr-3t%e8%b6%85%e5%a4%a7%e5%ad%98%e5%82%a8vps%e6%b5%8b%e8%af%84.html)

#### 购买链接

官网地址：[HostBrr 官网](https://my.hostbrr.com/order/forms/a/MzQw)（含AFF）

促销请关注 [HostBrr-lowendtalk](https://lowendtalk.com/profile/labze)

### 3.BuyVM（PT刷力很烂，离线下载不错，唯一优点抗DMCA）

运营了十多年的老牌 VPS 商家，其无限流量 VPS 低至 3.5 美元/月，加上仅需 1.25 美元/月的 256G 附加存储空间，总共只需 4.75 美元/月就可以拥有一个 256G 无限流量大盘鸡。使用支付宝付款通过加拿大元汇率结算更优惠，折合人民币每月只需 24 元左右。连续付三个月可以升级为PRO用户，带宽升级到10G无限。由于极具性价比，所以经常处于缺货状态。有需求建议先**注册账号**，可抢先一步下单，切勿错失良机。

#### 相关测试

[BuyVM-Luxembourg-5900X](https://catcat.blog/buyvm-%e5%8d%a2%e6%a3%ae%e5%a0%a1-5900x-%e4%b8%8d%e9%99%90%e6%b5%81%e9%87%8f.html)

#### 购买链接

官网地址：[BuyVM官网](https://my.frantech.ca/aff.php?aff=6455)

### 4.Liteserver (网络优秀，适合保种，离线下载，抗DMCA)

2007年的老商家，自有ASN AS60404，主机托管于荷兰Serverius DC1资料中心，有NVMe及HDD可选，均提供1Gbps网络线路，流量会使用完成后会限速10Mbps。Liteserver的性价比很不错，在欧洲的口碑良好。支持NVME和HDD款互相切换，2022年黑五有五折优惠。

#### 相关测试

[Liteserver-NVME](https://catcat.blog/112-2.html)

#### 购买链接

官网地址：[Liteserver官网](https://clients.liteserver.nl/aff.php?aff=621)（有AFF）

## 线路优化推荐

中国地大物博，同样的一台 VPS，面对不同的地域，不同的运营商，它的表现会完全不一样，因而在线路这一块差距很大，没有绝对的好用这一说法。

参考线路：线路优先度 CN2 GIA>CN2 GT>163 直连

三网回程 GIA > 三网回程 9929 > 三网回程 4837 等

### 1.BangwagonHost（俗称搬瓦工）

其在美国洛杉矶 / 费利蒙市 / 新泽西 / 纽约 / 荷兰阿姆斯特丹 / 中国香港以及日本大阪均有机房，其中洛杉矶有三网直连、CN2 GT、CN2 GIA 顶级线路接入，香港有 CN2 GIA 顶级线路接入，日本大阪有软银 (BBTEC, Soft­Bank) 线路接入，荷兰有联通 CU PM (AS9929/AS10099) 精品线路接入。顶级线路、自研面板、十几个机房随意切换是所有 VPS 商家中独树一帜的存在。**价格昂贵，毫无性价比，机器性能稀烂，只能代理使用。**

#### 相关测试

[BangwagonHost The Plan 所有机房测评](https://catcat.blog/%e6%90%ac%e7%93%a6%e5%b7%a517%e4%b8%aa%e6%9c%ba%e6%88%bf%e7%b3%bb%e5%88%97%e6%b5%8b%e8%af%84.html)

#### 购买链接

官网地址：[BangwagonHost官网](https://bandwagonhost.com/aff.php?aff=71041)（含AFF）

### 2.Misaka

Misaka（御坂网络），原名ZeptoVM，成立于2017年2月，算是国人商家里面比较热门和做的比较大的了，有多地节点以及自有骨干，旗下俄罗斯CN2产品非常出名，之后自研面板投入使用以及建立品牌后成立Misaka，面板使用体验不错，镜像实行全自动编译，保证最新可靠。虽然提供直连线路，但Misaka的主攻方向为海外市场，老板Aveline技术人员出身，曾经发生过因为成本问题给用户降配的情况，之后商标换成Misaka机器价格变高就没有发生过了。现在优化系列都是接入的**10g口三网CMI**。

#### 相关测试

[Misaka-HK全面测试](https://catcat.blog/misaka%e9%a6%99%e6%b8%af-%e6%b5%8b%e8%af%84.html)

#### 购买链接

官网地址：[Misaka官网](http://misaka.io)（无AFF）
