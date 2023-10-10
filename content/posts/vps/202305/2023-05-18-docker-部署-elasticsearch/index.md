---
title: "Docker 部署 elasticsearch"
date: "2023-05-18"
categories: 
  - "docker"
  - "laboratory"
---

需要宿主机安装 `docker` 服务

- 使用 `elasticsearch:7.10.1` 镜像

```
- 挂载了主配置文件（主配置文件中启用了xpack认证）
- 挂载了 data 数据目录
- 挂载了 log 日志文件
- 设置集群模式为 single-node
- 设置了 es 使用的内存大小
```

- 可根据实际情况修改参数

```
docker run -d --restart=always --user=root \
    --privileged=true \
    --name elasticsearch \
    -p 9200:9200 \
    -p 9300:9300 \
    --ulimit nofile=65536:65536 \
    -v "/data/elasticsearch/elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml" \
    -v "/data/elasticsearch/data":/usr/share/elasticsearch/data \
    -v "/data/elasticsearch/logs":/usr/share/elasticsearch/logs \
    -e "discovery.type=single-node" \
    -e ES_JAVA_OPTS="-Xms8G -Xmx8G" \
    elasticsearch:7.10.1
```

## 服务器目录配置信息[#](#1751269258)

### 目录信息[#](#531924179)

```
# tree /data/elasticsearch/ -L 1
/data/elasticsearch/
├── data # 数据目录
├── elasticsearch.yml  # 配置文件
└── logs # 日志

# mkdir /data/elasticsearch/{data,logs} -pv
# cd /data/
# chown 1000 elasticsearch -R
```

### 配置信息[#](#1832956682)

```
# vim /data/elasticsearch/elasticsearch.yml
cluster.name: "test_evescn"
network.host: 0.0.0.0
#xpack.security.enabled: true
http.cors.allow-headers: Authorization
xpack.security.enabled: true
xpack.security.transport.ssl.enabled: true
```

### 执行 docker 命令启动容器[#](#3419337727)

- 可根据实际情况修改参数

```
docker run -d --restart=always --user=root \
    --privileged=true \
    --name elasticsearch \
    -p 9200:9200 \
    -p 9300:9300 \
    --ulimit nofile=65536:65536 \
    -v "/data/elasticsearch/elasticsearch.yml:/usr/share/elasticsearch/config/elasticsearch.yml" \
    -v "/data/elasticsearch/data":/usr/share/elasticsearch/data \
    -v "/data/elasticsearch/logs":/usr/share/elasticsearch/logs \
    -e "discovery.type=single-node" \
    -e ES_JAVA_OPTS="-Xms8G -Xmx8G" \
    elasticsearch:7.10.1
```

## 启动 xpack 认证[#](#1823197683)

```
# docker exec -it elasticsearch bash
# elasticsearch-setup-passwords interactive

.... 设置 es_xpack 认证的6个账户密码 ....
```
