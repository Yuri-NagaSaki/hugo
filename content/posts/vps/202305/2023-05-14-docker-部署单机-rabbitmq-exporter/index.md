---
title: "Docker 部署单机 RabbitMQ + exporter"
date: "2023-05-14"
categories: 
  - "docker"
  - "laboratory"
---

## 资源清单

| 主机 | IP |
| --- | --- |
| rabbitmq | 10.0.0.1 |

| 软件 | 版本 |
| --- | --- |
| docker | 20.10.12 |
| docker-compose | 1.23.1 |
| rabbitmq | 3.8.34 |

## 一、`Docker` 安装

### 1\. 使用国内 `yum` 源

```
# yum install -y yum-utils device-mapper-persistent-data lvm2
# yum-config-manager --add-repo https://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
```

### 2\. 卸载旧版本的 `docker`

```
## 如果主机上已经有docker存在且不是想要安装的版本，需要先进行卸载。
# yum remove -y docker \
              docker-client \
              docker-client-latest \
              docker-common \
              docker-latest \
              docker-latest-logrotate \
              docker-logrotate \
              docker-selinux \
              docker-engine-selinux \
              docker-engine \
              container*
```

### 3\. 安装 `Docker20.10` 版本

```
# yum -y install docker-ce-20.10.12-3.el7 docker-ce-cli-20.10.12-3.el7
```

### 4\. 设置镜像加速

```
# mkdir /etc/docker
# vi /etc/docker/daemon.json

{
  "registry-mirrors": ["https://xxxxxxxxx.mirror.aliyuncs.com"]
}
```

### 5\. 启动 `docker`

```
# systemctl start docker
# systemctl enable docker
# systemctl status docker
```

## 二、`Docker-compose` 安装

### 1\. `Docker-compose` 安装

```
## github.com 可能访问超时，可以使用下面的获取下载下来后上传服务器即可
# curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

# curl -k "https://dl.cactifans.com/zabbix_docker/docker-compose" -o /usr/bin/docker-compose

# chmod a+x /usr/bin/docker-compose
```

### 2\. 查看 `docker-compose` 版本

```
# docker-compose version
```

## 三、部署服务

### 1\. `docker-compose.yaml` 资源清单

```
version: '3'

services:
  rabbitmq:
    image: rabbitmq:3.8.34-management
    hostname: rabbitmq
    container_name: rabbitmq
    deploy:
      resources:
        limits:
          cpus: '1'
          memory: 2G
    ports:
      - "15672:15672"
      - "15692:15692"
      - "5672:5672"
      # rabbitmq-exporter port
      - "9419:9419"
    volumes:
      - /data/rabbitmq/:/var/lib/rabbitmq
      - /etc/localtime:/etc/localtime
    restart: always

  rabbitmq_exporter:
    image: kbudde/rabbitmq-exporter:1.0.0-RC19
    container_name: rabbitmq_exporter
    environment:
      RABBIT_USER: admin
      RABBIT_PASSWORD: admin
    depends_on:
      - rabbitmq
    network_mode: "service:rabbitmq"
    restart: always
```

### 2\. 部署服务

```
# docker-compose up -d

# docker-compose ps -a
```

### 3\. 初始化 rabbimq 账号信息

```
# cat init_rabbitmq.sh

#!/bin/bash

# reset first node
echo "1、Reset first rabbitmq node."
docker exec rabbitmq /bin/bash -c 'rabbitmqctl stop_app'
docker exec rabbitmq /bin/bash -c 'rabbitmqctl reset'
docker exec rabbitmq /bin/bash -c 'rabbitmqctl start_app'

# add user and userrole
echo "2、Starting to create user."
docker exec rabbitmq /bin/bash -c 'rabbitmqctl add_user admin admin'

echo "3、Set tags for new user."
docker exec rabbitmq /bin/bash -c 'rabbitmqctl set_user_tags admin administrator'

echo "4、Grant permissions to new user."
docker exec rabbitmq /bin/bash -c "rabbitmqctl set_permissions -p '/' admin '.*' '.*' '.*'"

echo "5、Delete guest user"
docker exec rabbitmq /bin/bash -c "rabbitmqctl delete_user guest"
```

```
# bash init_rabbitmq.sh
```
