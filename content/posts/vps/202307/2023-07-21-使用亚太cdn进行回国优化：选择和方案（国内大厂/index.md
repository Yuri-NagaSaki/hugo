---
title: "使用亚太CDN进行回国优化：选择和方案（国内大厂篇（搬运）"
date: "2023-07-21"
categories: 
  - "laboratory"
---

原贴链接：[西普拉斯驿站](https://www.nodeseek.com/jump?to=https%3A%2F%2Fpost.cplus8.com%2Fd%2F616)

以下方案针对域名没有备案主要用户在国内希望国内访客可以获得较好访问速度的站长，对于那些有备案的来说，就不必这样大费周章来琢磨了，最佳方案仍是使用国内节点

> 主机圈里的确有这样一类建站鸡子：流量少，带宽小，性能一般，线路优良，它们的存在给国内访客带来了很好的体验。但倘若很不幸，我的朋友，你在购买机子时没有未雨绸缪，想到自己以后要搭建网站这茬呢？（像是买了SoftLayer的香港）不要着急，只要您的机器在当地的互联尚可（比如香港有hkix，Equinix等交换中心），您便可以选择使用cdn的方式进行弥补优化，本文将依据我们的测试数据（延迟，线路，QoS等），给您提供一些良好的回国优化方案。

值得注意的是，本文限定节点范围为亚洲沿太平洋地区，同时也默认了您的源站在此区域。尽管有些线路如9299连美国等可以使链接延迟在200ms以下，但是物理距离摆在那里，对于精益求精的我来说还是无法接受的。同时，对于亚太周边均值延迟120ms将不会推荐给您。由于测量手段受限，所以本文讨论的皆是去程。- 
诚挚建议您在阅读本帖之前，阅读- 
[国内至国际骨干 ISP 线路整理](https://www.gd1214b.icu/post/qfDddx_kZ/) 它将有助于您的理解。- 
那么我们先从国内大厂开始

## 国内篇

国内的话做cdn大约分为两个派别，一是像阿里云这种云厂商，利用自身优势顺便也做了cdn；另一部分则是如ChinaCache（蓝汛）这种做cdn起家的。

### 阿里云

| 运营商 | 地区 | 当地ISP | 测试IP | 质量评分 | 备注 |
| --- | --- | --- | --- | --- | --- |
| 移动 | 香港 | 中国移动香港 | 182.239.104.69 | ●●●●● | 普通CMI①，无qos②，上海延迟30ms③ |
|  | 澳门 | 澳门电讯ctm | 125.31.22.28 | ●●●●◐ | ①③，少数地区会有丢包，QOS |
|  | 台湾 | 台湾阿里云 | 47.246.38.211 | ●●●● | ①②，经中华电信，上海到此60ms④ |
|  |  | 台湾Zenlayer | 192.169.122.232 | ●●●● | ①②④ |
|  | 东南亚 | 马来西亚u.com.my | 188.214.64.212 | ●●●◐ | ①②，经新加坡starhub，上海到此80ms |
|  | 日本 | 日本大阪府阿里云 | 47.89.66.69 | ●●●◐ | ①②，上海到此80ms |
| 联通 | 香港 | 中国移动香港 | 182.239.104.69 | ●●●● | 走移动cmi香港，无qos |
|  |  | 香港宽频HKBN | 203.185.10.151 | ●●●◐ | 169连香港，经香港NTT,延迟略高，上海或广州至此50ms+ |
|  |  | 数码通SmartTone | 203.78.41.167 | ●● | 169连香港，经hkbn，延迟波动大，50-120ms |
|  | 澳门 | 澳门电讯ctm | 125.31.22.28 | ●●● | 169直连澳门，qos影响大，广州至此最低10ms，时常波动到100ms+ |
|  | 台湾 | 台湾阿里云 | 47.246.38.211 | ●●● | 169，②，经中华电信，30-130ms |
|  |  | 台湾zenlayer | 192.169.122.232 | ●●●● | 169，②，经中华电信，上海至此稳定20ms左右 |
|  | 日本 | 大阪府阿里云 | 47.89.66.69 | ●●● | 169，②，走kddi，平均延迟80ms |
|  |  | 东京Zenlayer | 192.169.122.232 | ●●● | 169，走日本ntt，上海出口至此35ms，有轻微qos |
|  | 韩国 | 阿里云 | 39.125.80.160 | ●●●● | 169，②，走sk，上海至此40ms |
| 电信 | 香港 | 中国移动香港 | 182.239.104.69 | ●●●●◐ | 163接香港，②，转香港移动，上海香港延迟均为30ms左右 |
|  |  | 香港宽频HKBN | 203.185.10.151 | ●●●◐ | 有随机qos，延迟略高，上海或广州至此50ms+ |
|  |  | 数码通SmartTone | 203.78.41.167 | ●●● | qos偏严重，经hkbn，上海或广州至此50ms+ |
|  |  | 香港有线电视 | 222.166.1.39 | ●●●◐ | 有59.43段cn2路由，qos偏严重，广州延迟最低10ms，被qos后达700ms |
|  | 澳门 | 澳门电讯ctm | 125.31.22.28 | ●●●◐ | cn2/CTGNet接香港，阿里云转，qos偏严重 |
|  | 日本 | 大阪府阿里云 | 47.89.66.69 | ●●● | 中度qos，163，kddi，平均延迟120ms |
|  | 韩国 | 阿里云 | 39.125.80.160 | ●●● | 中度qos，上海至此最低30ms |

境外加速默认分配给境内的CNAME记录的简直就是一坨矢，虽然分配了新加坡、日本等等地的节点，但是不是被墙就是绕美。所谓自己动手丰衣足食的意义，或许正在于此吧。以下是我们的结果

#### 港澳台地区

- 香港- 
    阿里云在香港，既有自家的阿里云节点，也有香港各大固网ISP/移动网络提供商的节点，如香港移动，数码通，hkbn等。对比起其他家的cdn，最精细化的就是阿里云了，像在大陆地区的策略一样，移动，电信，联通都给你来一个不同的节点。事实上有互联网交换中心的存在，给个自家节点，通过hkix等就可以很容易的完成部署了。不过既然他有这么多，那我就用起来吧。- 
    虽说阿里云确实像电信买的CN2带宽，但cdn并没有资格用上，都拿去当精品带宽卖钱去了，因而三网绕美，走PCCW回来。

中国移动香港方面似乎不错，阿里云部署了一段182.239.104.\*,80个ip。

电信方面延迟相当于普通的163水平，不过，无论从广州出口出发或者是上海出口出发，到节点的延迟，都是35ms左右，不排除有广州出口有绕上海的可能，也可能是因为移动那玩意就这样。庆幸的是，这玩意优先级很高,即使是晚高峰时期也不会被电信主动QoS,自己保证的，之前能在100毫秒以内打开的网站不会突然飙升至一秒。- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689475178-687066-screenshot-2023-07-16-10-38-43-1.png%7Etplv-66hnoafy04-new.image)

![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689474524-371738-screenshot-2023-07-16-10-25-35-1.png%7Etplv-66hnoafy04-new.image)\- 
而联通移动方面，在出境前就已经都汇聚到上海移动出口，和普通的CMI质量差不多。所以如果你有其他方案，联通移动都还是不用走香港移动为妙。- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689475106-153346-screenshot-2023-07-16-10-32-23-1.png%7Etplv-66hnoafy04-new.image)

香港宽频HKBN以及数码通方面，移动绕到欧洲再回来，没有什么价值

![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689479898-497501-screenshot-20230716-115801.jpg%7Etplv-66hnoafy04-new.image)\- 
而电信联通则要分类而论了。HKBN的ip话绕道日本NTT,不错就是那个大名鼎鼎晚高峰炸的的离谱的NTT,我的建议是能不用则不用。- 
真•蹦蹦炸弹- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689604862-304992-screenshot-2023-07-17-22-40-32.png%7Etplv-66hnoafy04-new.image)

![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689493288-951202-screenshot-2023-07-16-10-52-48-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689496207-124443-20230716-162633.jpg%7Etplv-66hnoafy04-new.image)

数码通的ip则不同电信联通两者走普通网163/169香港经HKBN连接，电信有一定的程度的QoS，联通用起来非常丝滑。- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689495295-853467-screenshot-2023-07-16-16-00-13-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689495345-316979-screenshot-2023-07-16-15-56-26-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689495428-54970-20230716-161654.jpg%7Etplv-66hnoafy04-new.image)

- 最后还有一段香港有线电视的。- 
    移动虽说也是直连到香港，但是到hkix那一跳延迟就高起来，最终荣获600ms的佳绩，可喜可贺啊- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689496618-951036-20230716-163515.jpg%7Etplv-66hnoafy04-new.image)\- 
    联通的情况也差不多- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689498453-959929-20230716-164948.jpg%7Etplv-66hnoafy04-new.image)\- 
    电信不得了了，用上了59.43段的高贵CN2带宽，美中不足的是也有Qos.- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689499180-581764-screenshot-2023-07-16-16-48-32-1.png%7Etplv-66hnoafy04-new.image)\- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689499229-232685-20230716-164150.jpg%7Etplv-66hnoafy04-new.image)

- 澳门- 
    澳门电信业的格局大抵是与别处不同的，不能说是一超多强，只能说是一家独大。CTM澳门电讯以自己专营权优势，占据很大的市场份额。所以CDN厂商来澳门部署节点时，一般都像CTM购买服务器。阿里云在澳门没有机房，也不例外的买了段125.\*的，QoS等级不是很高。- 
    移动经自家的cmi/as58453香港连接至澳门，电信经CN2/CTGNet到香港转由阿里云香港连到CTM，联通则是直连。- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689502776-104215-screenshot-2023-07-16-18-11-45-1.png%7Etplv-66hnoafy04-new.image)\- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689506362-90648-screenshot-2023-07-16-18-21-10-1.png%7Etplv-66hnoafy04-new.image)\- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689506366-943323-screenshot-2023-07-16-18-28-22-1.png%7Etplv-66hnoafy04-new.image)\- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689506593-84895-screenshot-2023-07-16-18-15-54-1.png%7Etplv-66hnoafy04-new.image)

- 台湾- 
    主要为阿里云自家的节点和老朋友Zenlayer的。- 
    自家节点上，仅有电信绕美，移动联通正常直连到台湾中华电信再到阿里云，平均延迟略高于香港，平均延迟延迟为60ms。但联通方面有些不稳。- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689511741-855992-microsoft-edge-screenshot-2023716-gmt08-00-20-48-54png.png%7Etplv-66hnoafy04-new.image)\- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689511856-641545-microsoft-edge-screenshot-2023716-gmt08-00-20-50-18png.png%7Etplv-66hnoafy04-new.image)\- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689512005-334718-microsoft-edge-screenshot-2023716-gmt08-00-20-53-16png.png%7Etplv-66hnoafy04-new.image)\- 
    Zenlayer的话和上述结果差不多，联通会比上面好些（不过延迟条也还是锯齿状的- 
    ![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689512178-75512-microsoft-edge-screenshot-2023716-gmt08-00-20-56-12png.png%7Etplv-66hnoafy04-new.image)

#### 东南亚

虽说阿里云在东南亚如越南，印尼，新加坡等地都有建机房，但是并没有针对回国进行优化。更何况本土运营商，大都只服务于当地罢了。- 
尽管有少部分的线路延迟还不错，但其一有可能经过香港中转，那为何不选用香港的呢？其二，路由策略太过于鬼畜，有些沿海地区能收到直连的路由，延迟在80ms上下，但有些地方收不到，可能走了ntt之类的线路，延迟起飞。- 
因而，东南亚地区没什么好推荐的。- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689520229-64204-screenshot-2023-07-16-21-32-07.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689520338-835544-20230716-231132.jpg%7Etplv-66hnoafy04-new.image)

（美丽的图表- 
因为移动cmi在东南亚的优势，其实还有段马来西亚u.com.my可以走- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689522716-804075-20230716-235143.jpg%7Etplv-66hnoafy04-new.image)

#### 日本

仍是自家节点和zenlayer好搭档，部署在东京和大阪府。- 
阿里云的大阪府节点，三网走KDDI,延迟120ms上下，电信依旧有QoS，联通所有连接走北京出口- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689524084-96895-screenshot-2023-07-17-00-05-49-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689524091-939808-screenshot-2023-07-17-00-05-54-1.png%7Etplv-66hnoafy04-new.image)\- 
东京则跑不动了，绕路 延迟up- 
而东京的Zenlayer也只能勉强拉动联通。- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-16%2F1689524459-107521-20230717-002043.jpg%7Etplv-66hnoafy04-new.image)

#### 韩国

只有自家的，ip归属显示SK.- 
电信联通直连，华北延迟40ms，仅次于华南连港澳，移动绕日。- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689560791-704099-screenshot-2023-07-17-00-32-22-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689560797-898782-screenshot-2023-07-17-00-34-15-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689560805-848705-screenshot-2023-07-17-00-35-02-1.png%7Etplv-66hnoafy04-new.image)

#### 总结

电信方面，推荐使用香港移动，香港有线电视，澳门ctm，韩国SK,日本KDDI.- 
联通推荐使用香港数码通，香港移动，澳门ctm，韩国sk，日本kddi- 
移动推荐使用香港移动，台湾Zenlayer,阿里云.

### 腾讯云

不愧是跟AWS达成了合作伙伴关系，好家伙，境外节点全都是用从AWS买的ec2，这边建议有条件的直接上AWS的CloudFront.- 
关于cloudfront/aws的选择将在国外篇提及。

### 华为云

华为云在海外cdn方面分为两部分，其中一部分是自家的，其表现为证书响应值为" n.cdnhwc3.com"，web服务器是openrest还有一部分就是网宿的，证书值为default.chinacenter.com.- 
此处先讨论完华为云自家的节点，网速的节点将在下文进行讨论。

#### 香港

简言之，这里是移动的主场。有段223开头的香港移动以及和记环球通讯HGC,移动均可直表现伤和普通的cmi差不多，质量上香港移动＞HGC.- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689582146-620826-screenshot-2023-07-17-16-16-42-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689582237-890926-screenshot-2023-07-17-16-11-30-1.png%7Etplv-66hnoafy04-new.image)\- 
还有段华为云自己的119.8.22.\*- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689585744-467013-screenshot-2023-07-17-17-21-54.png%7Etplv-66hnoafy04-new.image)\- 
另外的一段经pccw的靠谱云往大陆被pccw qos很离谱，这里不在叙述。

- 澳门- 
    路由和上文的阿里云的125段一样的，不过华为买的是45开头的。- 
    不同点表现为移动到广州出口无路由，联通会有随机性的丢包，但给电信用非常合适，不会遇到主动QoS,延迟会比cn2多个5ms，无伤大雅

![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689586655-858685-screenshot-2023-07-17-17-37-12-1.png%7Etplv-66hnoafy04-new.image "your-discribition")

![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689586980-558997-screenshot-2023-07-17-17-41-54-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689586985-555404-screenshot-2023-07-17-17-42-07-1.png%7Etplv-66hnoafy04-new.image)

- 台湾- 
    抱歉 华为云在台湾无cdn节点。 东南亚 移动方面可以尝试新加坡移动、TATA，马来西亚maxis

自家的新加坡华为云也还OK。- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689596875-91088-screenshot-2023-07-17-20-26-59-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689596880-701488-screenshot-2023-07-17-20-27-07-1.png%7Etplv-66hnoafy04-new.image)

#### 日本

华为云的日本节点是靠谱云和奥飞数据这两家，其中奥飞数据可以给联通走走，是日本ntt直连，他家这质量主么好？怪。靠谱云那边全炸了，不用看- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689604088-486920-20230717-222639.jpg%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689604518-419023-20230717-223404.jpg%7Etplv-66hnoafy04-new.image)

#### 韩国

力量薄弱地区+1 仅有zenlayer，同样电信qos严重，联通还能动，移动脸肿- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689605279-795714-screenshot-2023-07-17-22-47-18-1.png%7Etplv-66hnoafy04-new.image)

### 天翼云

他家境外cdn接入了华为云平台，分配了网宿的节点以及……- 
电信自家机房的CN2节点，对没错，这个质量绝对第一。- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689606514-297538-screenshot-2023-07-17-22-59-56-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689606519-67100-screenshot-2023-07-17-23-00-35-1.png%7Etplv-66hnoafy04-new.image)\- 
![This in image](https://cubox.pro/c/filters:no_upscale()?valid=true&imageUrl=https%3A%2F%2Fcplus.ddwoo.top%2Fassets%2Ffiles%2F2023-07-17%2F1689606526-973116-screenshot-2023-07-17-23-00-39-1.png%7Etplv-66hnoafy04-new.image)\- 
天翼云不仅只有香港cn2，还有新加坡 马来西亚等地的cn2，这里根据实际情况选择即可，首推的还是香港cn2.- 
云厂商这边大概就这么几家，其他的像青云，百度云的没有境外加速业务，又拍云境外就一个香港zenlayer和一个法国节点也不必多讲；而UCLOUD境外接入的是Stackpath,京东云境外接的是Cloudflare，这些将在国外篇提及。- 
待续……- 
此贴仅仅是胡言乱语，错漏之处还望谅解。
