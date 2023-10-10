---
title: "Nat机部署qbittorrent"
date: "2023-08-29"
categories: 
  - "laboratory"
---

## 安装qbittorrent

采用一键脚本

```
bash <(wget -qO- https://raw.githubusercontent.com/jerry048/Dedicated-Seedbox/main/Install.sh) <用户名称> <用户密码> <缓存大小(单位:GiB，且为整数)>
```

## 端口转发

填入8080

![](https://catcat.blog/wp-content/uploads/2023/08/image-8.png)

## 修改配置文件

使用 root 用户登录到服务器；  
找到 `qbittorrent.conf` 文件（如 `~/.config/qBittorrent/qBittorrent.conf` ）并打开；  
在`[Preferences]`中 设置

```
WebUI\HostHeaderValidation=false
WebUI\CSRFProtection=false
```

如果没有 `WebUI\CSRFProtection` 选项，可自行添加；  
修改完成后保存并退出；  
重新启动 `qbittorrent` 服务，即可使用
