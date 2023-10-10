---
title: "ServerStatus-Rust Debian11 保姆级部署教程"
date: "2023-09-04"
categories: 
  - "laboratory"
---

> 本来探针部署在大阪的Oracle Arm上，无奈号被清退了，只得重新部署

## 效果

![](https://catcat.blog/wp-content/uploads/2023/09/image-10-1024x556.png)

## 准备资料

- TG BOT API

- TG CHAT ID

- Vercel

- VPS

- 域名（可选）

## 搭建服务端

通过[@BotFather](https://t.me/BotFather)获得`bot_token`，红框内指向内容就是你的token

![](https://catcat.blog/wp-content/uploads/2023/09/image-1-1024x664.png)

通过[](https://t.me/getmyid_bot)[@Get My ID](https://t.me/getmyid_bot)获得`chat_id`

![](https://catcat.blog/wp-content/uploads/2023/09/image-2.png)

### 服务端部署

```
apt install wget curl unzip vim
新建目录并且进入
mkdir -p /opt/ServerStatus && cd /opt/ServerStatus
编辑.sh文件
vim server.sh
```

如果是部署到**ARM**架构，记得按照注释修改`OS_ARCH`变量，文件内容如下：

```
#!/bin/bash
set -ex

WORKSPACE=/opt/ServerStatus
mkdir -p ${WORKSPACE}
cd ${WORKSPACE}

# 下载, arm 机器替换 x86_64 为 aarch64
OS_ARCH="x86_64"
latest_version=$(curl -m 10 -sL "https://api.github.com/repos/zdz/ServerStatus-Rust/releases/latest" | grep "tag_name" | head -n 1 | awk -F ":" '{print $2}' | sed 's/\"//g;s/,//g;s/ //g')

wget --no-check-certificate -qO "server-${OS_ARCH}-unknown-linux-musl.zip"  "https://github.com/zdz/ServerStatus-Rust/releases/download/${latest_version}/server-${OS_ARCH}-unknown-linux-musl.zip"

unzip -o "server-${OS_ARCH}-unknown-linux-musl.zip"

# systemd service
mv -v stat_server.service /etc/systemd/system/stat_server.service

systemctl daemon-reload

# 启动
systemctl start stat_server

# 状态查看
systemctl status stat_server

# 使用以下命令开机自启
systemctl enable stat_server

# https://fedoraproject.org/wiki/Systemd/zh-cn
# https://docs.fedoraproject.org/en-US/quick-docs/understanding-and-administering-systemd/index.html
```

运行`.sh`文件：

```
bash -ex server.sh
```

修改`config.toml`配置文件，本地修改配置文件参考[config.toml](https://raw.githubusercontent.com/zdz/ServerStatus-Rust/master/config.toml)

```
vim /opt/ServerStatus/config.toml
```

config.toml参考

```
# 管理员账号,不设置默认随机生成，用于查看 /detail, /map
jwt_secret = "" # 修改这个, 使用 openssl rand -base64 16 生成 secret 第8行
admin_user = ""  第9行
admin_pass = "" 第10行
hosts =  第22行
# 开关 true 打开
enabled = false  第60行
bot_token = "<tg bot token>" 第61行
chat_id = "<chat id>" 第62行
```

测试配置文件

```
# 测试配置文件是否有效
./stat_server -c config.toml -t
# 根据配置发送测试消息，验证通知是否生效
./stat_server -c config.toml --notify-test
```

![](https://cdn.lirica.cn/wordpress/2023/09/image-3-1024x93.png)

![](https://cdn.lirica.cn/wordpress/2023/09/image-4.png)

重启服务端服务

```
systemctl restart stat_server
```

测试访问（ip:8080）

![](https://cdn.lirica.cn/wordpress/2023/09/image-5-1024x199.png)

## 主题配置

通过前后端分离实现主题配置，前端通过**Vercel**部署

首先fork[HinataKato/hotaru\_theme\_for\_RustVersion: The frontend of ServerStatus-Hotaru based on Vue 3.0 (github.com)](https://github.com/HinataKato/hotaru_theme_for_RustVersion)到自己账户下：

![](https://cdn.lirica.cn/wordpress/2023/09/image-7-1024x460.png)

vercel导入该库

![](https://cdn.lirica.cn/wordpress/2023/09/image-8-1024x299.png)

直接部署即可，不需要修改任何东西。等待部署完成后打开fork的仓库连接，通过Codespaces修改项目

![](https://cdn.lirica.cn/wordpress/2023/09/image-9-1024x570.png)

在仓库根目录创建`vercel.json`，文件内容如下，将`http://xxx.com/`改为**自己的域名或`IP地址:端口`**，如果支持HTTPS，记得将`http://`全部改为`https://`：

```
{
    "routes": [
        {
            "src": "/json/stats.json",
            "dest": "http://ip:端口/json/stats.json"
        },
        {
            "src": "/detail",
            "dest": "http://ip:端口/detail"
        },
        {
            "src": "/map",
            "dest": "http://ip:端口/map"
        },
        {
            "src": "/i",
            "dest": "http://ip:端口/i"
        },
        {
            "src": "/report",
            "dest": "http://ip:端口/report"
        }
    ]
}
```

commit推送分支，随意Message

![](https://catcat.blog/wp-content/uploads/2023/09/image-11-1024x556.png)

等待重新部署连接后端

![](https://catcat.blog/wp-content/uploads/2023/09/image-12-1024x298.png)

添加自己域名

![](https://catcat.blog/wp-content/uploads/2023/09/image-13-1024x330.png)

等待下发生效，部署完成

## 搭建客户端

创建目录

```
cd
apt install wget curl unzip vim
mkdir -p /opt/ServerStatus && cd /opt/ServerStatus
```

编辑`.sh`文件

```
vim client.sh
```

如果是部署到**ARM**架构，记得按照注释修改`OS_ARCH`变量，文件内容如下：

```
#!/bin/bash
set -ex

WORKSPACE=/opt/ServerStatus
mkdir -p ${WORKSPACE}
cd ${WORKSPACE}

# 下载, arm 机器替换 x86_64 为 aarch64
OS_ARCH="x86_64"
latest_version=$(curl -m 10 -sL "https://api.github.com/repos/zdz/ServerStatus-Rust/releases/latest" | grep "tag_name" | head -n 1 | awk -F ":" '{print $2}' | sed 's/\"//g;s/,//g;s/ //g')

wget --no-check-certificate -qO "client-${OS_ARCH}-unknown-linux-musl.zip"  "https://github.com/zdz/ServerStatus-Rust/releases/download/${latest_version}/client-${OS_ARCH}-unknown-linux-musl.zip"

unzip -o "client-${OS_ARCH}-unknown-linux-musl.zip"

# systemd service
mv -v stat_client.service /etc/systemd/system/stat_client.service

systemctl daemon-reload

# 启动
systemctl start stat_client

# 状态查看
systemctl status stat_client

# 使用以下命令开机自启
systemctl enable stat_client

# 停止
# systemctl stop stat_client

# https://fedoraproject.org/wiki/Systemd/zh-cn
# https://docs.fedoraproject.org/en-US/quick-docs/understanding-and-administering-systemd/index.html

# 修改 /etc/systemd/system/stat_client.service 文件，将IP改为你服务器的IP或你的域名
```

运行`.sh`文件：

```
bash -ex client.sh
```

如果需要使用vnstat数据，参考[zdz/ServerStatus-Rust: ✨ Rust 版 ServerStatus 探针、威力加强版 (github.com)](https://github.com/zdz/ServerStatus-Rust#5-%E5%BC%80%E5%90%AF-vnstat-%E6%94%AF%E6%8C%81)安装vnstat并配置：

```
# 在client端安装 vnstat
## Centos
sudo yum install epel-release -y
sudo yum install -y vnstat
## Ubuntu/Debian
sudo apt install -y vnstat

# 修改 /etc/vnstat.conf
# 一般来说只要修改BandwidthDetection和MaxBandwidth就够了
# BandwidthDetection 0
# MaxBandwidth 0
# 默认不是 eth0 网口的需要置空 Interface 来自动选择网口
# 没报错一般不需要改
# Interface ""
systemctl restart vnstat

# 确保 version >= 2.6
vnstat --version
# 测试查看月流量 (刚安装可能需等一小段时间来采集数据)
vnstat -m
vnstat --json m
```

在修改配置文件前，可以先试试看自己的服务是否可以使用：(此处域名是你ververl部署的域名，用户名和密码是对应的host)

```
./stat_client -a https://probe.catcat.blog/report -u 用户名 -p 密码
```

![](https://cdn.lirica.cn/wordpress/2023/09/image-14-1024x174.png)

如果可以使用，就可以修改`stat_client.service`配置文件了:

```
vim /etc/systemd/system/stat_client.service
```

参考如下，**只修改`ExecStart=/opt/ServerStatus/stat_client`这一行**，如果是HTTP记得将https改成http，不使用vnstat的话，请删除`-n`，即只保留`-a "https://probe.catcat.blog/report" -u 用户名 -p 密码`。

```
[Unit]
Description=ServerStatus-Rust Client
After=network.target

[Service]
User=root
Group=root
Environment="RUST_BACKTRACE=1"
WorkingDirectory=/opt/ServerStatus
# EnvironmentFile=/opt/ServerStatus/.env
ExecStart=/opt/ServerStatus/stat_client -a "https://probe.catcat.blog/report" -u 用户名 -p 密码 -n
ExecReload=/bin/kill -HUP $MAINPID
Restart=on-failure

[Install]
WantedBy=multi-user.target

# /etc/systemd/system/stat_client.service
# journalctl -u stat_client -f -n 100
```

修改完成后先重载文件再重启客户端服务：

```
systemctl daemon-reload
systemctl restart stat_client
```

通过`systemctl status stat_client`查看服务状态，如下就没问题了

![](https://cdn.lirica.cn/wordpress/2023/09/image-16-1024x439.png)
