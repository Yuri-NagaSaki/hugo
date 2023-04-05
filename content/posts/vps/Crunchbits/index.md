---
title: "Crunchbits 评测"
date: "2023-02-23"
tags: [VPS]
categories: [vps]
featuredImage: https://cdn.lirica.cn/webp/00000.webp
license: CC BY-NC-SA 4.0

hiddenFromHomePage: false
hiddenFromSearch: false
---

> 前言 Crunchbits，这是一家 2021 年 11 月 30 日成立的美国主机商，主营 NVMe KVM VPS、EPYC 高频 NVMe VPS、锐龙 5950X NVMe KVM VPS、大硬盘存储 VPS、GPU 显卡服务器和独立服务器，数据中心位于美国 爱达荷州。

## 前言

![](https://i.imgtg.com/2023/02/23/sEdxg.png)

Crunchbits，这是一家 2021 年 11 月 30 日成立的美国主机商，主营 NVMe KVM VPS、EPYC 高频 NVMe VPS、锐龙 5950X NVMe KVM VPS、大硬盘存储 VPS、GPU 显卡服务器和独立服务器，数据中心位于美国 爱达荷州。

美西，距离西雅图、圣荷西、洛杉矶都比较近。

目前网站仅支持信用卡、比特币和 Paypal 付款（暂不支持支付宝）。

本次推荐套餐：

**4GB 锐龙 5950X 带 450GB 硬盘！**

- 1 锐龙 5950X vCore

- 4GB DDR4 **ECC** 内存

- 50GB 第 4 代 NVMe 操作系统 / 主磁盘

- **450GB 硬盘**存储磁盘

- 10TB 带宽 @ **2.5Gbps**

- 1 个 IPv4 + 1 个 IPv6 /64

- $ 8 / 月 **$ 6.8 / 月** 带优惠券：**ONLYTOWEL**

- [**购买地址**](https://crunchbits.com/)

> 注意：HDD 块存储必须在成功订购后发工单让老板添加。

工单参考：

> 标题：
> 
> Add a 450GB HDD to my hard drive
> 
> 内容：
> 
> Dear crunchbits,
> 
> I don’t currently have a 450GB HDD as a drive, please help add it, thanks!

特色：

- NVMe

- 大存储

- 5950X

- 带免费备份功能，可以设置指定时间自动备份（备份保留一份，仅备份 50GB NVMe 上的内容，无法备份 450G HDD 上的内容）

- 美西

缺陷：

- 新商家，不知道会不会跑路（可以月付，PayPal 上车，消除风险）

- 线路可能没那么好（美西其实还凑合，实在不行可以反代解决）

## 1\. 官方网站

官网：[https://crunchbits.com/](https://loll.cc/crunchbits)

## 2\. 注意点

- 个人信息里面的街道啥的也要完善好

- 地址什么的要填合乎逻辑的地址，可以不准确但是不要乱填

如果万一订单被判定欺诈，可以发工单和客服沟通。

如果需要翻译，可以用这个：[https://www.deepl.com/translator](https://www.deepl.com/translator)

## 3\. 套餐介绍

### 3.1 Ryzen 5950X CPU NVMe VPS Plans

最低配折后 **$6.8/** 月，优惠码：`ONLYTOWEL`（85 折循环优惠码）

| **内存** | **Ryzen 5950X Cores**CPU | 固态硬盘 | HDD 硬盘 | **Bandwidth @ 2.5Gbps** | **IPv4 | IPv6** | 折前价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 4GB | **1** 5950X Cores | 50GB NVMe | 450GB HDD | 10TB | 1 IPv4 | 1 /64 | **$8/mo** | [购买链接](https://loll.cc/crunchbits) |
| 8GB | **2** 5950X Cores | 100GB NVMe | 900GB HDD | 20TB | 1 IPv4 | 1 /64 | **$16/mo** | [购买链接](https://loll.cc/crunchbits) |
| 16GB | **4** 5950X Cores | 200GB NVMe | **1.8TB** HDD | 40TB | 1 IPv4 | 1 /64 | **$32/mo** | [购买链接](https://loll.cc/crunchbits) |
| 32GB | **8** 5950X Cores | 400GB NVMe | **3.6TB** HDD | 80TB | 1 IPv4 | 1 /64 | **$64/mo** | [购买链接](https://loll.cc/crunchbits) |

本次测试款为最低配 6.8 刀 / 月款。

## 4\. VPS 测试（1C4G）

### 4.1 基本情况

鸡况如下：

![](https://i.imgtg.com/2023/02/23/sD7k1.png)

### 4.2 速度测试

![](https://i.imgtg.com/2023/02/23/sDNmI.png)

测试我们重点看`Upload Speed`, 我们从 VPS 上取东西（下载），对 VPS 来说就是上传。

以上海`Shanghai 5G`为例子，显示的`Upload Speed`是`305.71 Mbit/s`，差不多是平时说的 300M 带宽，对应到我们实际的理论下载速度就 =`305.71/8`\=`38.21M/s`

开启 BBR 之后：

![](http://img.laoda.de/i/2023/02/07/gw5qzs-2.webp)

![](http://img.laoda.de/i/2023/02/07/gvls86-2.webp)

### 4.4 PING 值

![](https://i.imgtg.com/2023/02/23/sDA5F.png)

### 4.5 网络测试

#### 4.5.1 机器

Test IPv4: 204.9.39.100

Test IPv6: 2606:a8c0:1:99::a

#### 4.5.2 官网节点测速

Looking glass: [https://lg-cda.crunchbits.com](https://lg-cda.crunchbits.com/)

### 回程测试

![](https://i.imgtg.com/2023/02/23/sDKA6.png)

总结  
\-- 不跑路的话香中香
