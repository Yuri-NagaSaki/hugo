---
title: "Docker部署Misskey"
date: "2023-04-03"
categories: 
  - "docker"
  - "laboratory"
---

![](https://catcat.blog/wp-content/uploads/2023/10/image-144.png)

整个搭建过程一开始参考了官网的，发现稍微有点复杂，然后搜索到了下面两个小伙伴的经验分享，非常有帮助，感谢付出！

搭建分享：[使用 Docker 最小化部署 Misskey](https://candinya.com/posts/minimal-misskey-docker-deploy/)

> 本教程基本~借鉴~抄自上面的搭建教程 XD

使用分享：[Fediverse 不止 Mastodon——Misskey 介绍](https://akaito.xyz/post/misskey/#top)

## 1\. 简介

Misskey 是由日本开发者しゅいろ (syuilo) 所创立的去中心化社交网络服务，其官方实例是 [misskey.io](https://misskey.io/)。Misskey 和 Mastodon 一样，采用了 ActivityPub 协议，因此可以与联邦宇宙 Fediverse 互通。

简单来说，它就是一个去中心化的微博！

我们创建的则是一个实例，不同的实例是可以互相访问互动的。

### 1.1 相关地址

官方实例地址：[https://misskey.io/](https://misskey.io/) （如果你不想自己搭建，可以直接加入官方的实例，不过貌似是日文的。）

官方网站：[https://misskey-hub.net/en/](https://misskey-hub.net/en/)

GitHub 地址：[https://github.com/misskey-dev/misskey](https://github.com/misskey-dev/misskey) （3k star）

实例列表：[https://join.misskey.page/zh-CN/instances](https://join.misskey.page/zh-CN/instances) （如果你不想自己搭建，也可以加入一个实例来使用）

## 2\. 项目展示

![](https://catcat.blog/wp-content/uploads/2023/10/image-145.png)

## 3\. 搭建环境

- 系统：Debian 11

- 安装好 Docker、Docker-compose

- 服务: Unesty 春季促销 高配德国vds

## 4.开始搭建

```
sudo -i

mkdir -p /root/data/docker_data/misskey

cd /root/data/docker_data/misskey
```

### docker-compose.yml 内容

```
# Misskey minimal deploy config
version: "3"

services:
  web:
    restart: always # 自动重启，请注意如果您对您的配置没有信心，请不要开启这个选项，以避免进程崩溃反复重启耗费大量资源！
    image: misskey/misskey:latest # 这里使用了官方镜像，以避免本地构建时资源不足的问题
    container_name: misskey_web # 容器名，方便管理，您可以自行修改为您觉得合适的内容
    links:
      - db
      - redis
    ports:
      - "3001:3001"
    networks:
      - internal_network
      - external_network
    volumes:
      - ./config:/misskey/.config:ro # 用于映射配置文件，请根据您的实际配置来决定文件夹名称，设定为只读即可；
      - ./files:/misskey/files # 用户上传到本地的文件，如果您一开始就接入外部存储（如wasabi或是AWS S3）您可以忽略这块配置

  redis:
    restart: always
    image: redis:latest
    container_name: misskey_redis
    networks:
      - internal_network
    volumes:
      - ./redis:/data # redis数据库的数据文件夹映射，创建后默认在 ./redis 文件夹中

  db:
    restart: always
    image: postgres:12.2-alpine
    container_name: misskey_db
    networks:
      - internal_network
    env_file:
      - ./config/docker.env # 需要使用配置文件中设置的 Docker 环境变量
    volumes:
      - ./db:/var/lib/postgresql/data # 主数据库的数据文件夹映射，创建后默认在 ./db 文件夹中

networks:
  internal_network: # 内部网络
    internal: true
  external_network: # 外部网
```

```
mkdir config
cd config
vim default.yml
```

### default.yml 内容

```
#━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Misskey configuration
#━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

#   ┌─────┐
#───┘ URL └─────────────────────────────────────────────────────

# Final accessible URL seen by a user.
url:        # 注意改成自己最后反向代理想要的网址

# ONCE YOU HAVE STARTED THE INSTANCE, DO NOT CHANGE THE
# URL SETTINGS AFTER THAT!

#   ┌───────────────────────┐
#───┘ Port and TLS settings └───────────────────────────────────

#
# Misskey requires a reverse proxy to support HTTPS connections.
#
#                 +----- https://example.tld/ ------------+
#   +------+      |+-------------+      +----------------+|
#   | User | ---> || Proxy (443) | ---> | Misskey (3000) ||
#   +------+      |+-------------+      +----------------+|
#                 +---------------------------------------+
#
#   You need to set up a reverse proxy. (e.g. nginx)
#   An encrypted connection with HTTPS is highly recommended
#   because tokens may be transferred in GET requests.

# The port that your Misskey server should listen on.
port: 3001

#   ┌──────────────────────────┐
#───┘ PostgreSQL configuration └────────────────────────────────

db:
  host: db
  port: 5432

  # Database name
  db: misskey

  # Auth
  user: example-misskey-user
  pass: example-misskey-pass

  # Whether disable Caching queries
  #disableCache: true

  # Extra Connection options
  #extra:
  #  ssl: true

#   ┌─────────────────────┐
#───┘ Redis configuration └─────────────────────────────────────

redis:
  host: redis
  port: 6379
  #family: 0  # 0=Both, 4=IPv4, 6=IPv6
  #pass: example-pass
  #prefix: example-prefix
  #db: 1

#   ┌─────────────────────────────┐
#───┘ Elasticsearch configuration └─────────────────────────────

#elasticsearch:
#  host: localhost
#  port: 9200
#  ssl: false
#  user: 
#  pass: 

#   ┌───────────────┐
#───┘ ID generation └───────────────────────────────────────────

# You can select the ID generation method.
# You don't usually need to change this setting, but you can
# change it according to your preferences.

# Available methods:
# aid ... Short, Millisecond accuracy
# meid ... Similar to ObjectID, Millisecond accuracy
# ulid ... Millisecond accuracy
# objectid ... This is left for backward compatibility

# ONCE YOU HAVE STARTED THE INSTANCE, DO NOT CHANGE THE
# ID SETTINGS AFTER THAT!

id: 'aid'

#   ┌─────────────────────┐
#───┘ Other configuration └─────────────────────────────────────

# Whether disable HSTS
#disableHsts: true

# Number of worker processes
#clusterLimit: 1

# Job concurrency per worker
# deliverJobConcurrency: 128
# inboxJobConcurrency: 16

# Job rate limiter
# deliverJobPerSec: 128
# inboxJobPerSec: 16

# Job attempts
# deliverJobMaxAttempts: 12
# inboxJobMaxAttempts: 8

# IP address family used for outgoing request (ipv4, ipv6 or dual)
#outgoingAddressFamily: ipv4

# Syslog option
#syslog:
#  host: localhost
#  port: 514

# Proxy for HTTP/HTTPS
#proxy: http://127.0.0.1:3128

#proxyBypassHosts: [
#  'example.com',
#  '192.0.2.8'
#]

# Proxy for SMTP/SMTPS
#proxySmtp: http://127.0.0.1:3128   # use HTTP/1.1 CONNECT
#proxySmtp: socks4://127.0.0.1:1080 # use SOCKS4
#proxySmtp: socks5://127.0.0.1:1080 # use SOCKS5

# Media Proxy
#mediaProxy: https://example.com/proxy

# Proxy remote files (default: false)
#proxyRemoteFiles: true

# Sign to ActivityPub GET request (default: false)
#signToActivityPubGet: true

#allowedPrivateNetworks: [
#  '127.0.0.1/32'
#]

# Upload or download file size limits (bytes)
#maxFileSize: 262144000
```

```
docker.env 内容
# db settings
POSTGRES_PASSWORD=example-misskey-pass
POSTGRES_USER=example-misskey-user
POSTGRES_DB=misskey
```

```
启动
cd ..    # 来到dockercompose文件所在的文件夹下
docker-compose run --rm web yarn run init   # 初始化数据库
docker-compose up -d 
```

## 5\. 使用教程

### 5.1 安装和配置

详细使用参考：[Fediverse 不止 Mastodon——Misskey 介绍](https://akaito.xyz/post/misskey/#top)

## 6.BUG解决

排障  
在初次安装完服务器后，出现了上传图片时报 Internal Server Error的问题，通过 docker logs 查看日志发现：

![](https://catcat.blog/wp-content/uploads/2023/10/image-146.png)

原因来自权限不足，进入misskey安装目录修改权限

```
sudo chown -R 991:991 files
```

## 参考资料

搭建参考：[使用 Docker 最小化部署 Misskey](https://candinya.com/posts/minimal-misskey-docker-deploy/)

使用参考：[Fediverse 不止 Mastodon——Misskey 介绍](https://akaito.xyz/post/misskey/#top)

官方实例地址：[https://misskey.io/](https://misskey.io/)

官方网站：[https://misskey-hub.net/en/](https://misskey-hub.net/en/)

GitHub 地址：[https://github.com/misskey-dev/misskey](https://github.com/misskey-dev/misskey) （3k star）
