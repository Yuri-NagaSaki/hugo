---
title: "备份和迁移 Chevereto 的 Docker 服务（4.0.6）"
date: "2023-04-11"
categories: 
  - "docker"
  - "laboratory"
---

要备份和迁移 Chevereto 的 Docker 服务，需要执行以下步骤：

1. 停止正在运行的 Chevereto 容器，使用以下命令：

```
docker stop chevereto
```

2. 备份 `/var/www/html/images/` 目录，不同的 VPS 可能具有不同的备份和迁移方法。如果你是使用基于 Linux 的 VPS，可以使用 `tar` 命令进行备份。例如，执行以下命令将 `images` 目录备份到当前目录下：

```
tar -zcvf images_backup.tar.gz /var/www/html/images/
```

3. 导出数据库，使用以下命令：

```
docker exec CONTAINER /usr/bin/mysqldump -u root --password=root DATABASE > backup.sql
```

其中，`CONTAINER` 是 Chevereto 容器的名称或 ID，`DATABASE` 是 Chevereto 使用的数据库名称。

4. 拷贝备份文件和数据库导出文件到新的 VPS 上。

6. 在新的 VPS 上安装 Docker 和 Docker Compose，如果还没有安装可以根据对应操作系统的官方安装指南进行安装。例如，在 Ubuntu 20.04 上可以按照如下方式安装：

```
sudo apt-get update
sudo apt-get install docker-compose docker.io
```

6. 在新的 VPS 上创建一个新的目录。为了方便，可以将目录命名为 Chevereto，并切换到该目录中，使用以下命令：

```
mkdir Chevereto
cd Chevereto
```

7. 在 Chevereto 目录中创建一个新的 `docker-compose.yml` 文件，用于启动 Chevereto 服务。为了确保服务正常启动，请确保修改以下环境变量，使其与原始 Chevereto 服务相同：

- `CHEVERETO_DB_HOST`: 数据库的连接地址。

- `CHEVERETO_DB_USER`: 用于连接数据库的用户名。

- `CHEVERETO_DB_PASS`: 用于连接数据库的密码。

- `CHEVERETO_DB_NAME`: Chevereto 所使用的数据库名称。

- `CHEVERETO_ASSET_STORAGE_BUCKET`: 图片文件的存储路径。

具体的 `docker-compose.yml` 文件内容如下：

```
version: '3'
services:
  chevereto:
    image: ghcr.io/chevereto/chevereto:latest
    container_name: chevereto
    ports:
      - "80:80"
    environment:
      - CHEVERETO_DB_HOST=database
      - CHEVERETO_DB_USER=chevereto
      - CHEVERETO_DB_PASS=user_database_password
      - CHEVERETO_DB_NAME=chevereto
      - CHEVERETO_ASSET_STORAGE_TYPE=local
      - CHEVERETO_ASSET_STORAGE_URL=/images/_assets/
      - CHEVERETO_ASSET_STORAGE_BUCKET=/var/www/html/images/_assets/
    volumes:
      - /var/www/html/images:/var/www/html/images
    depends_on:
      - database
  database:
    image: ghcr.io/chevereto/chevereto-mariadb:latest
    container_name: chevereto_database
    environment:
      - MYSQL_ROOT_PASSWORD=root
      - MYSQL_DATABASE=chevereto
```

请确保 `docker-compose.yml` 文件位于 Chevereto 目录的根目录中，以便后续执行命令。

8. 通过以下命令在新的 VPS 上启动 Chevereto 服务：

```
docker-compose up -d
```

这将在新的 VPS 上启动 Chevereto 服务，并且根据环境变量设置连接到原来的数据库和读取备份的目录。在这之后，你可以通过浏览器访问新的 VPS 的 IP 地址或域名来检查 Chevereto 服务是否正常工作。
