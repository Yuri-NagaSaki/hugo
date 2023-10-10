---
title: "RustDesk Debian 自建中继服务器"
date: "2023-04-11"
categories: 
  - "laboratory"
---

## 1、简介

开源的虚拟与远程桌面基础架构。远程桌面软件，开箱即用，无需任何配置。您完全掌控数据，不用担心安全问题。您可以使用我们的注册 / 中继服务器，或者自建，亦或者开发您的版本。

如果只是使用 RustDesk 软件且不需要自己搭建服务器的话，可以直接在官网下载对应的系统版本即可使用，不过由于共享使用作者的服务器画质和响应速度可能存在问题。此处建议有自己云服务器的同学自己搭建中继服务器，画质和响应速度会得到大幅度提升。

软件官网：[RustDesk](https://link.juejin.cn?target=https%3A%2F%2Frustdesk.com%2F)

## 2、搭建中继服务器

本博客基于：Debian 11 搭建，并采用 pm2 启动的方式进行管理

> 自建中继服务器基本要求：
> 
> 硬件要求很低，最低配置的云服务器就可以了，CPU 和内存要求都是最小的。关于网络大小，如果 TCP 打洞直连失败，就要耗费中继流量，一个中继连接的流量在 30k-3M 每秒之间（1920x1080 屏幕），取决于清晰度设置和画面变化。如果只是办公需求，平均在 100K/s。

### 2.1 下载中继服务器软件

#### 2.1.1 进入 RustDeck 官网下载软件

官网下载地址：[rustdesk-server](https://link.juejin.cn?target=https%3A%2F%2Fgithub.com%2Frustdesk%2Frustdesk-server)，找的与自己系统相匹配的软件包

#### 2.1.2 上传到自己的服务器

① 在 `/usr/local/lib` 目录下建立文件夹 `rustdesk`

```
mkdir rustdesk
```

② 使用 FTP 软件上传软件包到 `/usr/local/lib/rustdesk` 目录下

或者使用 `wget` 命令直接下载

```
wget https://github.com/rustdesk/rustdesk-server/releases/download/1.1.7-1/rustdesk-server-linux-amd64.zip
```

③ 解压软件包

```
unzip rustdesk-server-linux-amd64.zip
```

> 此时软件包以及可以使用，但是建议安装 pm2 进行服务的启停和管理
> 
> 启动命令
> 
> ```
> ./hbbs -r <hbbr运行所在主机的地址[:port]> 
> ./hbbr
> ```

### 2.2 安装 nodejs

① 在 `/usr/local/lib` 目录下建立文件夹 `nodejs`

```
mkdir nodejs
```

② 下载 nodejs，[nodejs 官网](https://link.juejin.cn?target=https%3A%2F%2Fnodejs.org%2Fzh-cn%2Fdownload%2F)使用 FTP 软件上传到目录 `/usr/local/lib/nodejs`

或者使用 `wget` 命令直接下载

```
wget https://nodejs.org/dist/v16.14.0/node-v16.14.0-linux-x64.tar.xz
```

> 注意：需要安装 nodejs16 + 版本

③ 解压文件，配置软连接

```
# 解压文件
tar -xvf node-v16.14.0-linux-x64.tar.xz
# 配置软连接
ln -s /usr/local/lib/nodejs/node-v16.14.0-linux-x64/bin/node /usr/local/bin
ln -s /usr/local/lib/nodejs/node-v16.14.0-linux-x64/bin/npm /usr/local/bin
```

④ 检查是否配置成功

```
node -v
npm -v
```

### 2.3 安装 pm2 包并启动服务

① 使用 npm 命令安装 pm2

```
npm install -g pm2
```

② 使用 pm2 运行 hbbs/hbbr

进入中继软件所在目录执行以下命令

```
pm2 start hbbs -- -r <your-relay-server-ip[:port]> 
pm2 start hbbr 
```

③ 查看服务运行情况

```
pm2 list
```

> hhbs 的`-r`参数不是必须的，他只是方便你不用在客户端指定中继服务器，如果是默认 21117 端口，可以不填 port。客户端指定的中继服务器优先级高于这个。
> 
> 官网指出填不填都可以，但是最好加上参数；

### 2.4 配置防火墙

找到你服务器的防火墙或安全组配置，开放以下端口，如图 2-2 所示；

- TCP(**21115, 21116, 21117, 21118, 21119**)

- UDP(**21116**)

> 务必在防火墙开启这几个端口， **请注意 21116 同时要开启 TCP 和 UDP**。
> 
> - hbbs 监听 21115(tcp), 21116(tcp/udp), 21118(tcp)；
> 
> - hbbr 监听 21117(tcp), 21119(tcp)；
> 
> - 21115 是 hbbs 用作 NAT 类型测试；
> 
> - 21116/UDP 是 hbbs 用作 ID 注册与心跳服务；
> 
> - 21116/TCP 是 hbbs 用作 TCP 打洞与连接服务；
> 
> - 21117 是 hbbr 用作中继服务, 21118 和 21119 是为了支持网页客户端；
> 
> - 如果您不需要网页客户端（21118，21119）支持，对应端口可以不开；

## 3、配置使用

### 3.1 不使用密钥连接

将第二步配置好的服务器地址，填写到 RustDesk 软件的 ID / 中继服务器配置，配置完成后即可进行远程连接。

① 打开 RustDesk 软件，找到菜单选项，

② 配置 ID 服务器和中继服务器地址

> 注意
> 
> ① 修改 IP 地址为你自己的 IP 地址！！！
> 
> ② **连接端和被连接端都需要添加中继服务器配置！！！**（否则会报id不存在的错误）

### 3.2 使用密钥链接

上述中配置完成后已经可以进行正常的远程桌面操作和访问，但是因为通信之间没有进行加密，难免会被恶意攻击和盗取数据，因此建议中继地址加入强制密钥访问。

① 重启 `hbbs/hbbr` 服务强制开启加密连接

```
pm2 start hbbs -r <relay-server-ip[:port]> -k _
pm2 start hbbr -k _
```

② 找到密钥文件

密钥文件配置在中继软件目录下的 `id_ed25519.pub`，使用命令查看密钥

```
cat ./id_ed25519.pub
```

③ 配置密钥

在 key 选项处添加的密钥信息即可实现加密连接；
