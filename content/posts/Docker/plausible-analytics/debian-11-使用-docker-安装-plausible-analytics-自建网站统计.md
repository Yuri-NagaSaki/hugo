---
title: "<strong>Debian 11 使用 Docker 安装 Plausible Analytics 自建网站统计</strong>"
date: "2023-02-26"
categories: 
  - "docker"
featuredImage: https://cdn.lirica.cn/webp/00009.webp
license: CC BY-NC-SA 4.0

hiddenFromHomePage: false
hiddenFromSearch: false
---

> 原文地址 [u.sb](https://u.sb/docker-plausible/)

本文将指导如何在 Debian 11 下使用 Docker 安装 Plausible Analytics 自建网站统计。

_PS：本文同时适用于任何可安装 Docker 的 Linux 发行版。_

## [](#为什么要自建网站统计？)为什么要自建网站统计？

原因很简单，自己网站的数据当然要自己保管，你希望你网站的数据都被第三方卖给「所谓的」大数据分析公司吗？

[Plausible Analytics](https://github.com/plausible/analytics) 是一款以隐私保护著称的网站统计软件，经过几个月的试用，基本可以满足所有的需求，可以取代商业化的 Google Analytics 等产品。[](#安装-docker-和-docker-compose-t2)

## [](#安装-plausible-analytics)安装 Plausible Analytics

建议安装在 `/opt/plausible` 目录：

```
mkdir -p /opt/plausible
cd /opt/plausible
```

首先，我们需要建立一个 `docker-compose.yaml` 文件，请按照实际需求修改参数：

```
version: "3.8"
services:
  mail:
    image: bytemark/smtp
    restart: always

  plausible_db:
    image: postgres:12
    volumes:
      - db-data:/var/lib/postgresql/data
    environment:
      - POSTGRES_PASSWORD=postgres
    restart: always

  plausible_events_db:
    image: yandex/clickhouse-server:21.3.2.5
    volumes:
      - event-data:/var/lib/clickhouse
      - ./clickhouse/clickhouse-config.xml:/etc/clickhouse-server/config.d/logging.xml:ro
      - ./clickhouse/clickhouse-user-config.xml:/etc/clickhouse-server/users.d/logging.xml:ro
    ulimits:
      nofile:
        soft: 262144
        hard: 262144
    restart: always

  plausible:
    image: plausible/analytics:latest
    command: sh -c "sleep 10 && /entrypoint.sh db createdb && /entrypoint.sh db migrate && /entrypoint.sh db init-admin && /entrypoint.sh run"
    depends_on:
      - plausible_db
      - plausible_events_db
      - mail
      - geoip
    volumes:
      - ./geoip:/geoip:ro
    ports:
      - 127.0.0.1:8000:8000
    env_file:
      - plausible-conf.env
    restart: always

  geoip:
    image: maxmindinc/geoipupdate
    env_file:
      - geoip.env
    volumes:
      - ./geoip:/usr/share/GeoIP

volumes:
  db-data:
    driver: local
  event-data:
    driver: local
  geoip:
    driver: local
```

然后我们在相同目录建立一个 `geoip` 的文件夹和 `plausible-conf.env` 的文件：

```
mkdir -p geoip
touch plausible-conf.env
touch geoip.env
```

修改 `plausible-conf.env`，按照官网的[教程](https://plausible.io/docs/self-hosting-configuration)进行配置，假设你的网址是 `https://stat.example.com/`，举例如下：

```
ADMIN_USER_EMAIL=管理员邮箱
ADMIN_USER_NAME=管理员用户名
ADMIN_USER_PWD=管理员密码
BASE_URL=https://stat.example.com/
SECRET_KEY_BASE=随机字符
MAILER_EMAIL=网站通知邮箱
SMTP_HOST_ADDR=SMTP 主机名
SMTP_HOST_PORT=SMTP 端口
SMTP_USER_NAME=SMTP 用户名
SMTP_USER_PWD=SMTP 密码
DISABLE_REGISTRATION=true
GEOLITE2_COUNTRY_DB=/geoip/GeoLite2-Country.mmdb
```

`SECRET_KEY_BASE` 需要一串 64 位的随机字符，可以试用 `openssl rand -base64 64` 或者 `pwgen 64` 生成。

`DISABLE_REGISTRATION` 设置 `true` 即关闭用户注册。

SMTP 可以使用市面上所有的邮件发送产品，或者懒人也可以直接用 Gmail 之类的免费服务，也可以自己搭建 [Mailcow](https://mailcow.email/) 自己用，教程在[这儿](https://u.sb/docker-mailcow/)。

然后我们注册个 [Maxmind](https://www.maxmind.com/) 帐号，注册成功后在左侧菜单 `Account` > `Manage License Keys` 里点击 `Generate new license key` 获取一个 `License key` 并记录 `Account ID` 和这个 `License key`：

然后修改 `geoip.env`，并填入如下信息：

```
GEOIPUPDATE_EDITION_IDS=GeoLite2-Country
GEOIPUPDATE_FREQUENCY=168 
GEOIPUPDATE_ACCOUNT_ID=你的 Account ID
GEOIPUPDATE_LICENSE_KEY=你的 License Key
```

然后抓取镜像并启动：

```
docker-compose pull
docker-compose up -d
```

启动完成后即可试用 `http://127.0.0.1:8000/` 访问 Plausible，如果需要对外进行服务，我们还需要配置 Nginx 反向代理。

重启 Nginx 后生效我们即可访问 `https://stat.example.com/`

## [](#更新-plausible-analytics)更新 Plausible Analytics

万能的 Docker 更新大法：

```
docker-compose pull

docker-compose up -d

docker system prune
```

## [](#备份-plausible-analytics)备份 Plausible Analytics

### 备份

```
# backup.sh
#!/usr/bin/env sh

docker-compose stop
docker run --rm -v plausible_db-data:/volume -v `pwd`:/backup loomchild/volume-backup backup plausible_db-data
docker run --rm -v plausible_event-data:/volume -v `pwd`:/backup loomchild/volume-backup backup plausible_event-data
docker-compose start -d
```

导入脚本

```
# restore.sh
#!/usr/bin/env sh

docker-compose stop
docker run --rm -v plausible_db-data:/volume -v `pwd`:/backup loomchild/volume-backup restore -f plausible_db-data
docker run --rm -v plausible_event-data:/volume -v `pwd`:/backup loomchild/volume-backup restore -f plausible_event-data
docker-compose start -d
```

## [](#卸载-plausible-analytics)卸载 Plausible Analytics

```
docker-compose down
rm -rf /opt/plausible
docker image rm postgres:12
docker image rm maxmindinc/geoipupdate:latest
docker image rm plausible/analytics:latest
docker image rm yandex/clickhouse-server:21.3.2.5
docker image rm bytemark/smtp:latest
docker volume rm plausible_db-data
docker volume rm plausible_event-data
```

## [](#wordpress-添加方法)WordPress 添加方法

直接修改你使用的主题的 `header.php` 文件，在 `<?php wp_head(); ?>` 后面添加统计代码即可。

不想修改主题的也可以直接装官方的[插件](https://wordpress.org/plugins/plausible-analytics/)。

## [](#vuepress-添加方法)VuePress 添加方法

如果你使用 `VuePress v1.x`，那么修改 `.vuepress/config.js` 文件，在 `module.exports` 加入：

```
['script', {}, `
const script = document.createElement('script');
script.async = true;
script.defer = true;
script['data-domain'] = '统计域名';
script.src = 'https://stat.example.com/js/plausible.js';
document.head.appendChild(script);`
],
```

如果你试用 `VuePress v2.x`，那么修改 `.vuepress/config.ts` 文件，在 `export default` 加入：

```
['script', {}, `
const script = document.createElement('script');
script.async = true;
script.defer = true;
script['data-domain'] = '统计域名';
script.src = 'https://stat.example.com/js/plausible.js';
document.head.appendChild(script);`
],
```

## [](#next-js-添加方法)Next.js 添加方法

安装 [next-plausible](https://github.com/4lejandrito/next-plausible) 这个包，然后使用类似如下的代码：

```
import PlausibleProvider from 'next-plausible'

export default function MyApp({ Component, pageProps }) {
  return (
    <PlausibleProvider domain="统计域名" customDomain="https://stat.example.com" selfHosted>
      <Component {...pageProps} />
    </PlausibleProvider>
  )
}
```

更多的添加方法请查看官网的[文档](https://plausible.io/docs/integration-guides)。
