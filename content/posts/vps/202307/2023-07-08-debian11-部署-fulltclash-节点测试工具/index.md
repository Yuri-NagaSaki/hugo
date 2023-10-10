---
title: "Debian11 部署 FullTclash 节点测试工具"
date: "2023-07-08"
categories: 
  - "laboratory"
---

## 介绍

**_[官方仓库](https://github.com/AirportR/FullTclash)_**

FullTclash bot 是承载其测试任务的Telegram 机器人（以下简称bot）,目前支持以clash配置文件为载体的**批量**联通性测试,支持以下测试条目:

> - Netflix Youtube DisneyPlus Bilibili steam货币 OpenAI(ChatGPT) 落地ip风险(IP欺诈度) 维基百科

以及HTTP延迟测试和链路拓扑测试（节点出入口分析）。

## 环境准备

```
apt update && apt upgrade
apt install -y git && git clone https://github.com/AirportR/FullTclash.git && cd FullTclash
apt install python3-pip screen fontconfig
cd FullTclash
pip3 install -r requirements.txt
```

## 安装字体

去这里挑选 [Nerd Fonts](https://www.nerdfonts.com/)

```
将字体文件复制到系统字体目录：将你下载字体文件（通常是以 .ttf、.otf 或 .woff 结尾的文件）复制到 /usr/share/fonts/ 目录下。

sudo cp your_font.ttf /usr/share/fonts/
将 your_font.ttf 替换为你的字体文件的实际路径和文件名。

更新字体缓存：运行以下命令来更新系统的字体缓存：

sudo fc-cache -f -v
这将重新扫描字体目录并更新字体缓存。

验证字体安装：你可以使用命令 fc-list 来列出系统中安装的字体。在终端中运行以下命令来查看字体列表：

fc-list
如果你能在列表中看到你的自定义字体，那么安装就成功了。
```

## Bot环境准备

\- Telegram 的api\_id 、api\_hash [获取地址](https://my.telegram.org/apps) (部分TG账号已被拉黑，无法正常使用)

\- 去 [@BotFather](https://t.me/BotFather) 那里创建一个机器人，获得该机器人的bot\_token，应形如：

bot\_token = "123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11"

\- 去这里 [@userinfobo](https://t.me/userinfobo) 获取用户id

## 运行

```
screen ## 创建新的终端
cd FullTclash/./resources
cp config.yaml.example config.yaml
vim config.yaml
## 以下是要修改的

bot:
 api_id: 123456 #改成自己的api_id
 api_hash: 123456ABCDefg #改成自己的api_hash
 bot_token: 123456:ABCDefgh123455  # bot_token, 从 @BotFather 获取
 # 如果是在中国大陆地区使用，则程序需要代理才能连接上Telegram服务器。写入如下信息：
 proxy: 127.0.0.1:7890 #socks5 替换成自己的代理地址和端口

## 执行
python3 -c 'import sys; sys.stdout.reconfigure(encoding="utf-8"); exec(open("main.py").read())'
```

![](https://catcat.blog/wp-content/uploads/2023/07/image-15.png)

![](https://catcat.blog/wp-content/uploads/2023/07/image-16-1024x598.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-168.png)
