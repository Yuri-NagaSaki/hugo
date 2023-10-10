---
title: "Docker 部署 kibana"
date: "2023-05-17"
categories: 
  - "docker"
  - "laboratory"
---

> 需要宿主机安装 `docker` 服务

- 使用 `kibana:7.10.1` 镜像

```
- 挂载了主配置文件
```

- 可根据实际情况修改参数

```
docker run -d --restart=always --name kibana \
    -p 5601:5601 \
    -v "/data/kibana/kibana.yml:/usr/share/kibana/config/kibana.yml" \
    kibana:7.10.1
```

## 服务器目录配置信息

### 目录信息[#](#2060504847)

```
# tree /data/kibana/
/data/kibana/
└── kibana.yml


# mkdir /data/kibana/ -pv
# chown 1000 -R /data/kibana/
```

### 配置信息[#](#535312965)

```
# vim /data/kibana/kibana.yml

#
# ** THIS IS AN AUTO-GENERATED FILE **
#

# Default Kibana configuration for docker target
server.name: kibana
server.host: "0.0.0.0"
server.port: 5601
elasticsearch.hosts: [ "http://ES_IP:9200" ]
elasticsearch.requestTimeout: 60000
monitoring.ui.container.elasticsearch.enabled: true
kibana.index: ".kibana"
i18n.locale: "zh-CN"
elasticsearch.username: "es_username"
elasticsearch.password: "es_password"
xpack.reporting.encryptionKey: "a_random_string"
xpack.security.encryptionKey: "something_at_least_32_characters"
```

### 执行 docker 命令启动容器[#](#1324945282)

- 可根据实际情况修改参数

```
docker run -d --restart=always --name kibana \
    -p 5601:5601 \
    -v "/data/kibana/kibana.yml:/usr/share/kibana/config/kibana.yml" \
    kibana:7.10.1
```
