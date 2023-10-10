---
title: "Debian 11 上使用 Minicube 部署 Kubernetes 集群"
date: "2023-09-07"
categories: 
  - "k8s"
  - "laboratory"
---

我这边采用的是Hetzner的独立服务器配置，VPS也能部署

```
 CPU 型号          : Intel(R) Core(TM) i7-7700 CPU @ 3.60GHz
 CPU 核心数        : 1 物理核心, 4 总核心, 8 总线程数
 CPU 频率          : 4089.603 MHz
 CPU 缓存          : L1: 256.00 KB / L2: 1.00 MB / L3: 8.00 MB
 硬盘空间          : 678.17 GiB / 936.60 GiB
 启动盘路径        : /dev/md1
 内存              : 24.31 GiB / 62.59 GiB
 Swap              : [ no swap partition or swap file detected ]
 系统在线时间      : 14 days, 19 hour 25 min
 负载              : 1.42, 1.76, 2.01
 系统              : Debian GNU/Linux 11 (bullseye) (x86_64)
 AES-NI指令集      : ✔ Enabled
 VM-x/AMD-V支持    : ✔ Enabled
 架构              : x86_64 (64 Bit)
 内核              : 5.10.0-23-amd64
 TCP加速方式       : bbr
 虚拟化架构        : Dedicated
 NAT类型           : 开放型
 IPV4 ASN          : AS24940 Hetzner Online GmbH
 IPV4 位置         : Berlin / Berlin / DE
 IPV6 ASN          : AS24940 Hetzner Online GmbH
 IPV6 位置         : Nuremberg / DE-BY
```

> ## 环境准备
> 
> 2 CPUs or more  
> 2GB of free memory  
> 20GB of free disk space  
> Internet connection  
> Container or virtual machine manager, such as: [Docker](https://minikube.sigs.k8s.io/docs/drivers/docker/), [QEMU](https://minikube.sigs.k8s.io/docs/drivers/qemu/), [Hyperkit](https://minikube.sigs.k8s.io/docs/drivers/hyperkit/), [Hyper-V](https://minikube.sigs.k8s.io/docs/drivers/hyperv/), [KVM](https://minikube.sigs.k8s.io/docs/drivers/kvm2/), [Parallels](https://minikube.sigs.k8s.io/docs/drivers/parallels/), [Podman](https://minikube.sigs.k8s.io/docs/drivers/podman/), [VirtualBox](https://minikube.sigs.k8s.io/docs/drivers/virtualbox/), or [VMware Fusion/Workstation](https://minikube.sigs.k8s.io/docs/drivers/vmware/) 

## 安装 Kubectl

```
依次执行
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x ./kubectl
sudo mv kubectl /usr/local/bin/

### 检查Kubectl是否安装成功
kubectl version -o yaml
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-39-1024x694.png)

## 安装Minikube

```
依次执行
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64
sudo install minikube-darwin-amd64 /usr/local/bin/minikube
检查是否安装成功
minikube version
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-40-1024x180.png)

## 启动Minikube

```
我这边采用的是Root权限下启动需要执行的，如果直接minikube启动，会有权限警告错误
minikube start --driver=docker --force
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-41-1024x406.png)

### 错误整理：

Root登录权限下直接通过minikube start 启动集群

```
minikube v1.31.2 on Debian 11.7
Automatically selected the docker driver. Other choices: ssh, none
The "docker" driver should not be used with root privileges. If you wish to continue as root, use --force.
If you are running minikube within a VM, consider using --driver=none:
https://minikube.sigs.k8s.io/docs/reference/drivers/none/
X Exiting due to DRV_AS_ROOT: The "docker" driver should not be used with root privileges. 
```

解决方案：1.更换用户 2.以 **minikube start --driver=docker --force** 命令启动集群

## 检查集群状态

```
kubectl cluster-info
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-42-1024x105.png)

## 检查正在运行的节点

```
kubectl get nodes
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-43-1024x116.png)

## 访问Minikube 容器

```
minikube ssh
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-44-1024x107.png)

退出容器Shell

```
exit
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-45-1024x110.png)

## 停止和删除 Kubernetes 集群

```
minikube stop
minikube delete
```

## 检查Minikube状态

```
minikube status
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-46.png)

## 访问Minikube Kubernetes Dashboard

默认情況下，Minikube 提供了一個 Web 端，可用来管理你的集群。

你可以使用以下命令列出所有 minikube 插件：minikube addons list

你可以看到以下输出：

```
[15:56 root@panel ~] > minikube addons list
|-----------------------------|----------|--------------|--------------------------------|
|         ADDON NAME          | PROFILE  |    STATUS    |           MAINTAINER           |
|-----------------------------|----------|--------------|--------------------------------|
| ambassador                  | minikube | disabled     | 3rd party (Ambassador)         |
| auto-pause                  | minikube | disabled     | minikube                       |
| cloud-spanner               | minikube | disabled     | Google                         |
| csi-hostpath-driver         | minikube | disabled     | Kubernetes                     |
| dashboard                   | minikube | disabled     | Kubernetes                     |
| default-storageclass        | minikube | enabled ✅   | Kubernetes                     |
| efk                         | minikube | disabled     | 3rd party (Elastic)            |
| freshpod                    | minikube | disabled     | Google                         |
| gcp-auth                    | minikube | disabled     | Google                         |
| gvisor                      | minikube | disabled     | minikube                       |
| headlamp                    | minikube | disabled     | 3rd party (kinvolk.io)         |
| helm-tiller                 | minikube | disabled     | 3rd party (Helm)               |
| inaccel                     | minikube | disabled     | 3rd party (InAccel             |
|                             |          |              | [info@inaccel.com])            |
| ingress                     | minikube | disabled     | Kubernetes                     |
| ingress-dns                 | minikube | disabled     | minikube                       |
| inspektor-gadget            | minikube | disabled     | 3rd party                      |
|                             |          |              | (inspektor-gadget.io)          |
| istio                       | minikube | disabled     | 3rd party (Istio)              |
| istio-provisioner           | minikube | disabled     | 3rd party (Istio)              |
| kong                        | minikube | disabled     | 3rd party (Kong HQ)            |
| kubevirt                    | minikube | disabled     | 3rd party (KubeVirt)           |
| logviewer                   | minikube | disabled     | 3rd party (unknown)            |
| metallb                     | minikube | disabled     | 3rd party (MetalLB)            |
| metrics-server              | minikube | disabled     | Kubernetes                     |
| nvidia-driver-installer     | minikube | disabled     | 3rd party (Nvidia)             |
| nvidia-gpu-device-plugin    | minikube | disabled     | 3rd party (Nvidia)             |
| olm                         | minikube | disabled     | 3rd party (Operator Framework) |
| pod-security-policy         | minikube | disabled     | 3rd party (unknown)            |
| portainer                   | minikube | disabled     | 3rd party (Portainer.io)       |
| registry                    | minikube | disabled     | minikube                       |
| registry-aliases            | minikube | disabled     | 3rd party (unknown)            |
| registry-creds              | minikube | disabled     | 3rd party (UPMC Enterprises)   |
| storage-provisioner         | minikube | enabled ✅   | minikube                       |
| storage-provisioner-gluster | minikube | disabled     | 3rd party (Gluster)            |
| volumesnapshots             | minikube | disabled     | Kubernetes                     |
|-----------------------------|----------|--------------|--------------------------------|
```

接下來，使用以下命令列出集群中目前运行的所有容器镜像：

```
kubectl get pods --all-namespaces
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-47-1024x235.png)

现在，韵行以下命令获取 Kubernetes 面板的 URL：

```
minikube dashboard --url
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-48-1024x288.png)

此時，Minikube 仪表盘已安装并运行在服务器上的 39509 端口上。但是，目前只能从本地地址访问它。 如果要从外部访问它，需要运行以下命令。

```
kubectl proxy --address='0.0.0.0' --disable-filter=true
```

現在，打開你的Chrome並输入 URL http://your-server-ip:8001/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/。 将被重定向到 Kubernetes 仪表盘，如下頁所示：

![](https://catcat.blog/wp-content/uploads/2023/09/image-49-1024x110.png)

![](https://catcat.blog/wp-content/uploads/2023/09/image-50-1024x575.png)
