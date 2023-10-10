---
title: "AdGuard 去除广告与 Clash 网络代理同时进行"
date: "2023-03-19"
categories: 
  - "laboratory"
---

## [#](#不只是厌烦广告) 不只是厌烦广告

广告的存在必然是有它的合理性的。它能帮助生产者在别种渠道获取回报，以便支持他继续免费提供作品，或将价格降至更可接受的范围。但某些投放广告的方式实在不恰当，为了将利益最大化，不惜牺牲原有的体验，这总是很令用户反感的。不仅严重影响用户体验，还容易给用户留下负面印象，打击宣传效果。但是指望所有广告投放者严格规范自己行为、以符合标准的形式投放广告是不切实际的。毕竟在巨大的利益前，人都可以不当人。

借助各种广告拦截工具，很大程度上就是为了拦截这些侵入式的、扰人的广告。这不仅能够保障用户体验，还能节省带宽和性能开销。

但不止于此，AdGuard 还能胜任保护隐私的使命。也许你只是在搜索引擎中搜索了一份讲义，之后打开购物 App 全在给你推这方面的教材。对于比较在意个人隐私的人而言，这是不能容忍的。我希望尽可能少的隐私被他人掌握。

在拦截广告的同时，AdGuard 还可以对一些跟踪器进行拦截。当我们浏览网页时，不仅发送了请求，还传递了许多额外的信息。如访问时的 IP 地址、正在使用的浏览器和系统信息、语言首选项、前一个访问的网站，甚至读取 Cookie 得知更多有关的信息。广告联盟等通过这些信息确定「你」是你、建立关于你的模型，以便进行更个性化的推送。

为杜绝此类现象，AdGuard 不仅拦截跟踪器，还拦截某些不安全的接口、拦截网站之间的联系、伪造浏览器信息等。这些是单靠插件和规则很难做到的，也是我选择应用的一个原因。

## [#](#adguard-是怎么做好这件事的) AdGuard 是怎么做好这件事的

相较于传统去广告插件，AdGuard 在他们的 [KnowledgeBase 知识库](https://kb.adguard.com/en/general/how-ad-blocking-works) 中也提到，AdGuard 主要通过以下三种方式实现去广告：

- Request blocking：即按照规则阻止（Block）某些连接以达到去广告的目的。网页载入时，某些元素会请求（Request）其他资源。AdGuard 会根据规则检查请求，若命中广告或跟踪器等规则时便予以拦截，阻止其载入。

- Page code filtering：在网页载入前，AdGuard 会先根据规则过滤一遍网页源码并去除其中包含广告等的代码。相比 Request blocking 让某些元素请求不到，Page code filtering 直接剥除部分代码，让广告根本不去请求。

- CSS Injection and Javascript：有些广告是通过 JavaScript 动态插入网页的，无需请求外部资源。这样一来前两条便不起作用了，需要额外的操作。AdGuard 通过调整 CSS 和 JavaScript 针对这类广告更彻底的清除。

第一条很常见，而后两条由于浏览器插件限制，只能在客户端实现。在比如 HTTPS 过滤这些会在之后详细配置时再谈。

## [#](#好好配置-adguard) 好好配置 AdGuard

虽说 AdGuard 是付费应用，但也可不只是给钱办事就完事了。想要 AdGuard 发挥全部威力还需要好好配置一番。这里将以桌面端为例，介绍部分 AdGuard 功能，并给出我使用 AdGuard 保证上网体验和保护隐私的一个实践，希望能对你有所帮助。

> AdGuard 团队仍在积极开发，AdGuard 软件 / 插件也在快速迭代。本文所提及的内容有一定时效性，最终以 [AdGuard KnowledgeBase](https://kb.adguard.com/en) 为准。

![](https://catcat.blog/wp-content/uploads/2023/10/image-53.png)

### [#](#选取合适的拦截规则) 选取合适的拦截规则

绝大多情况下，拦截规则都是广告拦截工具的核心。拦截规则在 AdGuard 被称为广告拦截器，不仅有广告拦截，还能屏蔽跟踪器、社交媒体插件、恼人的弹窗等。不过要注意，虽然通过规则阻止部分元素加载理论上能够加快页面加载，但如果设置了过多的规则，每次都要进行大量比对，反而可能会适得其反。这里按需选取即可。

AdGuard 默认开启的拦截器不多，这里我开启了：

- 广告拦截

- AdGuard 基础过滤器

- EasyList

- 隐私

- AdGuard 防护跟踪保护过滤器

- EasyPrivacy

- 社交插件

- AdGuard 社交媒体过滤器

- Fanboy’s Social Blocking List（包含于 Fanboy’s Annoyances）

- 扰人的

- AdGuard 扰人广告过滤器

- Fanboy’s Annoyances

- 特定语言

- AdGuard 中文过滤器

- EasyList China

当然，即便如此还是可能会有「漏网之鱼」，可以借助「拓展 > AdGuard Extra」手动处理某些元素。

### [#](#隐形模式充分保护隐私) 隐形模式充分保护隐私

过滤器已能拦截部分跟踪器，而隐形模式才是专门涉及保护隐私的「大招」。尽管过滤器能拦截大部分网页跟踪器，但正如前面提到过的，「请求网页」这个行为本身就已经泄露很多信息了。隐形模式一步步帮你保护这些个人敏感信息。

#### [#](#常规) 常规

![](https://catcat.blog/wp-content/uploads/2023/10/image-54.png)

先是 4 个常规选项，能够初步阻止一些跟踪：

**隐藏您的搜索记录**会隐藏你使用搜索引擎连入某网站的查询记录，从而使网站难以得知你的管用搜索引擎。

**发送「请勿跟踪」请求**，AdGuard 在请求网页时一并发送一个请勿跟踪的请求。部分浏览器里也有此项功能，不过即便请求了不要跟踪，最终还是取决于网站的意愿。

**移除 HTTP 请求中的 X-Client-Data 数据头**，使用 Chrome 浏览器请求任何和 Google 有关的网页时（包括 Double Click 和 Google Analyse），Chrome 浏览器都会把浏览器信息等一同传递给 Google。移除 HTTP 请求中的 X-Client-Data 数据头正是为了拦截这一项的数据。

**剥离 URL 中的跟踪参数**将会剥离 URL 里的跟踪参数，可以适当避免跨站跟踪情况的发生。同时允许手动配置跟踪参数实现自定义屏蔽。

#### [#](#跟踪方式) 跟踪方式

紧接着，在跟踪方式里可以限制常见网页跟踪你的方法：

![](https://catcat.blog/wp-content/uploads/2023/10/image-55.png)

**自销毁第三方 Cookie**，Cookie 通常用于存储用户登陆信息等。而第三方 Cookie 指并非当前页面生成的 Cookie。即便生成 Cookie 的网站行为干净得体，但是这条 Cookie 被其他网站获取到也可能被滥用。相较于拦截第三方 Cookie，自销毁第三方 Cookie 不会导致第三方登陆失效（第三方登陆大多通过 Cookie 或授权头授权原网站）。我在此处将第三方 Cookie 超时时间上调至 4 小时。

**自销毁第一方 Cookie**，与前者很像，但是启用后同一网站超时后都需要重新登陆。带来许多不必要的繁琐，所以这里我将其保持关闭。

**禁止缓存第三方请求**，某些网站可能会在加载页面时加上电子标签（e-tags）。只要缓存未被清除，下次请求时这些标记就有可能一并发给服务端，从而泄露之后访问了哪些网站。

**拦截第三方授权头**，授权头主要用于登陆授权等，但是也能用于跟踪。且若使用 HTTP 未加密协议发送授权头还有可能导致密钥等重要信息的泄露。但拦截后可能导致某些应用、插件的工作。

#### [#](#浏览器-api) 浏览器 API

这一项只影响浏览器，不影响其他应用。在此可以禁止某些有安全隐患的浏览器 API。

![](https://catcat.blog/wp-content/uploads/2023/10/image-56.png)

**拦截 WebRTC**，WebRTC 是一种实时通讯协议，但它可能绕过代理泄露真实 IP 地址。禁用后可能影响 Google Voice （特别是网页版）的正常使用。

**拦截推送 API**、**拦截定位 API**，这两个 API 分别用于管理浏览器推送和定位。由于我很少使用桌面端的地图以及完全不需要浏览器推送，所以完全禁用这两项。

**拦截 Flash**、**拦截 Java**，随着前端技术更迭，现在几乎所有网站都移除了 Flash/Java 的依赖。此外 Flash/Java 还有许多严重安全隐患，在 2020 年确实不该让浏览器继续支持它们。

#### [#](#杂项) 杂项

![](https://catcat.blog/wp-content/uploads/2023/10/image-57.png)

这部分选项必须包含在请求中，不能被禁止，但可以伪造。

**隐藏您的第三方 Referrer** 可以隐藏你是从哪里跳转过去的。我使用的第三方 Referrer 是 `https://www.bing.com` 。

**隐藏您的 User-Agent**，User-Agent 同样是包含在网页请求头中的，User-Agent 将暴露你所使用的浏览器信息、操作系统等。建议开启此项以使用默认替代信息。

**隐藏您的 IP**，由于我平时一直开启代理，而这项似乎并无太大作用，于是我将其关闭了。

此外，还有拓展、高级设置中某些项值得留意。例如 AdGuard Extra、使用重定向驱动模式都是我额外开启的。

## [#](#移动端兼容代理与-https-过滤) 移动端兼容代理与 HTTPS 过滤

移动端配置项与桌面端大同小异，不再赘述。要注意的是为了更深层次地去广告，绝大多数去广告工具都需要借助系统代理。而如果你本身就有使用网络代理需求，那就比较麻烦了。AdGuard 专门针对此支持了转发至本地代理，这也是 AdGuard 最抓住我需求的一点。

### [#](#兼容-clash-网络代理) 兼容 Clash 网络代理

网络代理工具选择的是 [Clash For Android](https://github.com/Kr328/ClashForAndroid)，它很好地支持了开启本地代理的同时不占用系统代理、向内部暴露并监听 DNS 端口。

如果你所使用的代理服务商不支持 Clash 订阅或者 Clash 配置中不含 DNS 配置，你可能需要借助公共 API 整理 Clash 配置文件。

#### [#](#利用-api-整理-clash-配置文件) 利用 API 整理 Clash 配置文件

基于 [subconverter](https://github.com/tindy2013/subconverter) 项目，你可以在许多公共 API 上方便的整理 Clash 配置文件。特别的，你可以使用 subconverter 作者 TindyX 提供的 [公共 API](https://subcon.py6.pw/?config=https://gist.githubusercontent.com/tindy2013/1fa08640a9088ac8652dbd40c5d2715b/raw/default_with_clash_adg.yml) 直接将订阅转换为带 AdGuard DNS 的 Clash 配置文件。

请确保 Clash 配置文件至少包含类似以下内容：

```
port: 7890
socks-port: 7891
dns:
 enable: true
 ipv6: false
 listen: 127.0.0.1:5450
 enhanced-mode: redir-host
 default-nameserver:
    - 119.29.29.29
    - 119.28.28.28
    - 1.0.0.1
    - 208.67.222.222
    - 1.2.4.8
  nameserver:
    - https://dns.alidns.com/dns-query
    - https://1.1.1.1/dns-query
    - tls://dns.adguard.com:853
```

其中，默认 DNS 监听端口（ `dns.listen` ）为 `5450` 、默认 HTTP 代理端口（ `port` ）为 `7890` 、默认 SOCKS5 代理端口（ `socks-port` ）为 `7891` 。这些参数之后配置时会需要用到。

#### [#](#adguard-配置-clash-转发规则) AdGuard 配置 Clash 转发规则

首先，在「AdGuard > 侧边栏 > 应用管理」中对 Clash For Android 关闭通过 AdGuard 路由应用流量。

![](https://catcat.blog/wp-content/uploads/2023/10/image-58.png)

紧接着，将 Clash 配置导入 Clash For Android 后，在「设置 > 网络」中关闭「自动路由系统流量」以关闭 Clash For Android 的 VPN 模式。随后开启 Clash For Android 代理功能。

![](https://catcat.blog/wp-content/uploads/2023/10/image-59.png)

再到「AdGuard > 侧边栏 > 设置 > DNS > 选择 DNS 服务器」最下方「添加自定义 DNS 服务器」。名称任取、地址填写 `127.0.0.1:5450` （取决于之前配置的 `dns.listen` 参数）。

![](https://catcat.blog/wp-content/uploads/2023/10/image-60.png)

返回到「设置」，继续点击「网络 > 代理」，在下方「+ 添加代理」。名称任取、方式选 `HTTP` （ `SOCKS5` ）、地址填写 `127.0.0.1` 、端口填写 `7890` （ `7891` ）。配置完毕后点击「保存并选择」并开启上方代理开关。

![](https://catcat.blog/wp-content/uploads/2023/10/image-61.png)

再回到「网络」，继续点击「过滤方式」，选择「本地 VPN」。之后回到主界面，开启主开关，便能在不影响原有代理的前提下享受 AdGuard 为你隐私保驾护航。

### [#](#安装证书过滤-https) 安装证书过滤 HTTPS

AdGuard 支持在页面载入前过滤部分代码，但是 HTTPS 加密让 AdGuard 正常情况下无法在载入前得到具体内容，也就无从过滤了。AdGuard 通过安装证书解密流量（Surge/QuantimultX 也使用类似的思路过滤），但是 Target API 24（Android 7.0）以上的 App 不再认可**用户证书**。

对于已经刷入 Magisk 的用户，可以借助 `Move Certificates` 将证书转为**系统证书**，从而让 AdGuard HTTPS 过滤对**所有 App 生效**。

AdGuard 总是对几乎所有应用生效，这会一定的浪费性能。对于一些系统 App（电话、信息等）和一定不会有广告的 App，可以考虑关闭 AdGuard 过滤。

## [#](#后续) 后续

仔细思考下，AdGuard 作为一款付费去广告工具，其付费的合理性何在？为何不直接将一定费用支付给作者使其放弃投放广告，而偏偏选择支付给去广告工具，让作者得不到合理（也许有些是不合理）的收入。而且，去广告工具功能很快就会饱和，框架也会慢慢稳定下来，真正让去广告工具保持生命力的，或许是那一条一条的规则。

但不能就此否认 AdGuard 的贡献。即便它不是最老牌，即便它还有不足。

在我看来，去广告只是 AdGuard 中的一环，而且**不是最重要的一环**。「Guard」—— 守卫，对自己隐私的重视与不妥协，才似乎是它希望传递的主旋律。当相当一部分用户对自己隐私的无所谓，认为区区市井小民没必要为隐私下功夫，这是否在一定程度上促成某些不恰当的行为呢？

也许 AdGuard 并非最早实现这些特性的，但它怎么都是完成得非常出色的。它是第一个让我愿意和网络代理工具一起 7x24 后台常驻的、第一个让我在其他应用中
