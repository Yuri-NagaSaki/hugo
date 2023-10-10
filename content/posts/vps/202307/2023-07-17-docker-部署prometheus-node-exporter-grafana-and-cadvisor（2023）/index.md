---
title: "Docker 部署Prometheus Node Exporter Grafana and cAdvisor（2023）"
date: "2023-07-17"
categories: 
  - "docker"
  - "laboratory"
---

![](https://catcat.blog/wp-content/uploads/2023/07/image-33-1024x514.png)

![](https://catcat.blog/wp-content/uploads/2023/07/image-34-1024x517.png)

## Docker compose 文件

```
git clone https://github.com/Sayyiku/DataEye.git
mkdir -p promgrafnode/prometheus
mkdir -p promgrafnode/grafana/provisioning
touch promgrafnode/docker-compose.yml
touch promgrafnode/prometheus/prometheus.yml

docker-compose up -d
```

![](https://catcat.blog/wp-content/uploads/2023/07/image-35-1024x259.png)

## Node Exporter 被控端部署

```
docker run -d -p 9100:9100 \
  -v "/root/docker/node-exporter/proc:/host/proc:ro" \
  -v "/root/docker/node-exporter/sys:/host/sys:ro" \
  -v "/root/docker/node-exporter/:/rootfs:ro" \
  --net="host" \
  --name node-exporter \
  prom/node-exporter
```

## [prometheus.yml](https://github.com/Sayyiku/DataEye/commit/2e3ab0e9609afb9f32b262fbeeb68589edfea193)

```
global: 
  scrape_interval: 1m

scrape_configs: 
  - job_name: "prometheus" 
    scrape_interval: 1m 
    static_configs: 
    - targets: ["localhost:9090"]

  - job_name: "node" 
    static_configs: 
    - targets: ["node-exporter:9100"]
    
   - job_name: "cadvisor" 
    scrape_interval: 5s 
    static_configs: 
    - targets: ["your ip:8081"]
  
  - job_name: "AWS-SG" 
    scrape_interval: 5s 
    static_configs: 
    - targets: ["your ip:9100"]
  
  - job_name: "Spaceberg-20T"   
    scrape_interval: 5s 
    static_configs: 
    - targets: ["your ip:9100"]
```

## Prometheus 和 Node Exporter 架构

Prometheus 和 Node Exporter 协同工作。您可以在同一台机器上运行 Prometheus 和 Node Exporter。但是，您很可能希望在许多其他远程 Linux 主机上运行 Node Exporter。

安装 Node Exporter 后，您可以在 Prometheus 配置文件中引用 Node Exporter 实例以及要监控的所有节点。这些可能是在您的环境中运行的 Linux 虚拟机。

Prometheus 将从位于远程 Prometheus 实例上的 Node Exporter http 端点收集数据。您可以启用其他收集器并收集所需的指标并使用 Prometheus 访问这些指标。

Prometheus UI 允许您查看服务发现并测试添加到 Prometheus 配置中的目标。在 Prometheus 配置文件中，您定义用于将 Prometheus 服务器连接到配置的 Node Exporter 实例的端点和端口。同样，您可以在 Prometheus 用户界面中验证您的连接。

## 使用 Prometheus Server 监控 URL 配置 Grafana

容器启动并运行后，您必须将 Prometheus 数据源添加到 Grafana。打开 Grafana，然后单击左下角的设置齿轮。然后单击 Prometheus，使用 Prometheus 服务器的 URL 配置 Grafana。

![](https://catcat.blog/wp-content/uploads/2023/07/image-36-1024x520.png)

添加数据源

![](https://catcat.blog/wp-content/uploads/2023/07/image-37-1024x186.png)

![](https://catcat.blog/wp-content/uploads/2023/07/image-38-1024x463.png)

添加 Prometheus 服务器 URL 的 IP 和端口，以 Prometheus 格式提取指标。

![](https://catcat.blog/wp-content/uploads/2023/07/image-39-1024x731.png)

## 将 Prometheus Node Exporter 指标可视化为 Grafana 仪表板

在[Grafana.com](http://grafana.com/)上，下载 ID 或 JSON 模板来创建快速、简单的仪表板，因为它消除了手动仪表板创建过程中的繁重工作。

![](https://catcat.blog/wp-content/uploads/2023/07/image-40-1024x516.png)

![](https://catcat.blog/wp-content/uploads/2023/10/image-174.png)
