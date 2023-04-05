---
title: "vps 测试脚本"
date: "2023-02-23"
weight: 1
categories: 
  - "vps"
featuredImage: https://cdn.lirica.cn/webp/00003.webp
license: CC BY-NC-SA 4.0

hiddenFromHomePage: false
hiddenFromSearch: false
---

## 1.vps体检脚本

```
bash <(curl -L -s https://bench.kangjw.me/kkb.sh)
bash <(wget -qO- --no-check-certificate https://gitlab.com/spiritysdx/za/-/raw/main/ecs.sh)
 
```

## 2.回程脚本

```
curl https://raw.githubusercontent.com/zhucaidan/mtr_trace/main/mtr_trace.sh|bash
```

## 3.Docker一键脚本(仅支持debian)

```
apt install wget curl sudo vim git -y 
curl -fsSL https://get.docker.com | bash -s docker
```

## 4.Node NVM脚本

```
安装 nvm (可选)
nvm 可以用于管理 Node.js。

打开终端，使用一键脚本，可以便捷地安装 nvm：

bash -c "$(curl -fsSL https://gitee.com/RubyKids/nvm-cn/raw/master/install.sh)"
重启终端即可生效

安装 Node.js 最新的 LTS 版本：

nvm install --lts
```

## 5.GPT 解锁测试

```
bash <(curl -Ls https://cpp.li/openai)
```

## 6.综合工具箱

```
wget -O box.sh https://raw.githubusercontent.com/BlueSkyXN/SKY-BOX/main/box.sh && chmod +x box.sh && clear && ./box.sh
```

## 7.流媒体测试

```
bash <(curl -L -s https://raw.githubusercontent.com/lmc999/RegionRestrictionCheck/main/check.sh)
```

## 8.Oracle 修改root脚本

```
#!/bin/bash
echo root:11235879 |sudo chpasswd root
sudo sed -i 's/^#\?PermitRootLogin.*/PermitRootLogin yes/g' /etc/ssh/sshd_config;
sudo sed -i 's/^#\?PasswordAuthentication.*/PasswordAuthentication yes/g' /etc/ssh/sshd_config;
sudo service sshd restart
```

默认密码是: 11235879  
登录后一定要修改密码！命令：`passwd`
