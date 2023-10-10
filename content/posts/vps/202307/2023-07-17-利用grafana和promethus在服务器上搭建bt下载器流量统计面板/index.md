---
title: "利用Grafana和Promethus在服务器上搭建BT下载器流量统计面板"
date: "2023-07-17"
categories: 
  - "docker"
  - "laboratory"
---

## 效果

![](https://catcat.blog/wp-content/uploads/2023/10/image-175.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-176.png)

## 准备工作

- Grafana 和 Promethus部署成功

- 准备好你所有下载的用户名/密码并确保可联通

## 准备配置文件

vim config.yml

```
root@Sakura:~# cat config.yml 
qb:  

  client: qbittorrent  

  host: http://ip:8080

  username: your username

  password: password

qb2:  

  client: qbittorrent  

  host: http://ip:8080

  username: your username  

  password: password

de:  

  client: deluge 

  host: http://ip:prot

  username: your username  

  password: password

tr:  

  client: Transmission 

  host: http://ip:prot

  username: your username  

  password: password
```

## 部署

```
docker run -d -p 9000:9000 -v /root/config.yml:/config/config.yml leishi1313/downloader-exporter
```

其中/root/config.yml是你上面文件的位置，可以使用pwd命令查看

![](https://catcat.blog/wp-content/uploads/2023/10/image-177.png)

## 检查是否成功连接

`IP:9000`确认下是否有如下页面，有类似输出代表downloader-exporter成功部署

![](https://catcat.blog/wp-content/uploads/2023/10/image-178.png)

## Grafana新建面板

![](https://catcat.blog/wp-content/uploads/2023/10/image-179.png)

### 选择数据源

![](https://catcat.blog/wp-content/uploads/2023/10/image-180.png)
