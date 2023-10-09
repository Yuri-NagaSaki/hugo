---
title: Debian 12 安装 Kubernetes，并配置主从节点（kubeadm方式）
author: 猫猫博客
type: post
date: 2023-09-20T05:47:07+00:00
url: /debian-12-安装-kubernetes，并配置主从节点.html
ai_summon_excerpt:
  - 这篇文章标题为《Debian 12 安装 Kubernetes，并配置主从节点（kubeadm方式）》的文章介绍了在Debian 12上使用kubeadm安装和配置Kubernetes的步骤。文章包括了节点设置、准备工作、安装Docker、安装cri-dockerd以及安装kubeadm、kubelet和kubectl等内容。
views:
  - 123
categories:
  - Kubernetes
  - 实验室

---
 

记录 Kubernetes 的安装与配置步骤。这次使用 kubeadm。

#### <a href="#机器们" target="_blank"  rel="nofollow" >#</a>节点设置 {.wp-block-heading}

  * va， Master 节点
  * ca， Worker 节点
  * kr， Worker 节点

#### <a href="#准备工作" target="_blank"  rel="nofollow" >#</a>准备工作 {.wp-block-heading}

更新系统到最新，然后移除不再需要的软件，清理无用的安装包。

<pre class="wp-block-code"><code>sudo apt update && sudo apt full-upgrade -y
sudo apt autoremove
sudo apt autoclean</code></pre>

如果更新了内核，重启。

Kubernetes 的机器不能有 swap 分区，所以要卸载 swap 分区。

然后编辑 `/etc/fstab` 文件，注释或删除 swap 那行（如有）。

开启转发等：

<pre class="wp-block-code"><code>cat &lt;&lt;EOF | sudo tee /etc/modules-load.d/k8s.conf
overlay
br_netfilter
EOF

sudo modprobe overlay
sudo modprobe br_netfilter

# sysctl params required by setup, params persist across reboots
cat &lt;&lt;EOF | sudo tee /etc/sysctl.d/k8s.conf
net.bridge.bridge-nf-call-iptables  = 1
net.bridge.bridge-nf-call-ip6tables = 1
net.ipv4.ip_forward                 = 1
EOF

# Apply sysctl params without reboot
sudo sysctl --system</code></pre>

<a href="https://kubernetes.io/docs/setup/production-environment/container-runtimes/#docker" target="_blank"  rel="nofollow" >根据 kubernetes 官方文档</a>，要安装官方版本的 docker，因此按照 docker 官方文档安装。

#### <a href="#安装-docker" target="_blank"  rel="nofollow" >#</a>安装 docker {.wp-block-heading}

删除非官方安装的 docker，如果你看过本站对于 docker 的介绍，那就需要卸载非官方 docker。对于 Docker 官方的版本 和 Debian 仓库中维护的版本的区别，Debian 仓库中的 Docker 版本低一些，有没有其区别不确定。

卸载非官方版本 Docker，因为会与官方版本冲突。

<pre class="wp-block-code"><code>for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done</code></pre>

<a href="https://docs.docker.com/engine/install/debian/#install-using-the-repository" target="_blank"  rel="nofollow" >官方文档</a> 安装

<pre class="wp-block-code"><code>sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo \
  "deb &#91;arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list &gt; /dev/null

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin</code></pre>

启动 docker 并设置开机自动运行

<pre class="wp-block-code"><code>sudo systemctl enable docker --now</code></pre>

**注意**，官方 Docker 与 Debian 仓库里的 docker-compose 不同，官方 Docker 用 `docker compose` 来 compose，compose 作为一个插件，Debian 仓库中的 docker-compose 用 `docker-compose` 来 compose。

#### <a href="#安装-cri-dockerd" target="_blank"  rel="nofollow" >#</a>安装 cri-dockerd {.wp-block-heading}

<a href="https://github.com/Mirantis/cri-dockerd/" target="_blank"  rel="nofollow" >cli-dockerd</a> 是 Kubernetes 控制 Docker 的中间层。cri: container runtime interface

<pre class="wp-block-code"><code>git clone https://github.com/Mirantis/cri-dockerd.git
cd cri-dockerd
make cri-dockerd
sudo mkdir -p /usr/local/bin
sudo install -o root -g root -m 0755 cri-dockerd /usr/local/bin/cri-dockerd
sudo install packaging/systemd/* /etc/systemd/system
sudo sed -i -e 's,/usr/bin/cri-dockerd,/usr/local/bin/cri-dockerd,' /etc/systemd/system/cri-docker.service
sudo systemctl daemon-reload
sudo systemctl enable cri-docker.service
sudo systemctl enable --now cri-docker.socket</code></pre>

注意，自行编译 cri-dockerd 需要 golang，如果提示找不到 go，安装 goalng: `sudo apt install golang`

**如果后面的命令遇到 socket 问题无法连接，重启服务器，暂时关闭防火墙等。**

#### <a href="#安装-kubeadm-kubelet-and-kubectl" target="_blank"  rel="nofollow" >#</a>安装 kubeadm, kubelet and kubectl {.wp-block-heading}

这部分依旧来自<a href="https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/#installing-kubeadm-kubelet-and-kubectl" target="_blank"  rel="nofollow" >官方文档</a> 注意虽然我们在 Debian 11/12 上安装，但是依旧是 xenial（Ubuntu 16.04 LTS） 的源。

<pre class="wp-block-code"><code>sudo apt-get update
sudo apt-get install -y apt-transport-https
curl -fsSL https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo gpg --dearmor -o /etc/apt/keyrings/kubernetes-archive-keyring.gpg
echo "deb &#91;signed-by=/etc/apt/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubelet kubeadm kubectl
sudo apt-mark hold kubelet kubeadm kubectl # 关闭这三个程序的自动更新</code></pre>

至此，Kubeadm 安装完成

#### <a href="#配置集群" target="_blank"  rel="nofollow" >#</a>配置集群 {.wp-block-heading}

<a href="https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/" target="_blank"  rel="nofollow" >官方文档</a>

一个很重要的问题是网络，k8s 集群中有很多台计算机，但是对外只有一个网络接口，比如你在 k8s 上运行一个网站，那么只能通过一个 ip 地址访问这个网站，但是集群中的每一台计算机都需要一个 ip 地址来通信，这个地址可以是私有地址，也可以是公网地址。k8s 本身不提供网络解决方案，需要<a href="https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/#pod-network" target="_blank"  rel="nofollow" >安装插件</a>，<a href="https://kubernetes.io/docs/concepts/cluster-administration/addons/" target="_blank"  rel="nofollow" >官方文档：installing addons</a>

这里选用了 <a href="https://www.tigera.io/project-calico/" target="_blank"  rel="nofollow" >https://www.tigera.io/project-calico/</a>，不同插件操作方法略有不同。

##### <a href="#设置-master-节点" target="_blank"  rel="nofollow" >#</a>设置 master 节点 {.wp-block-heading}

初始化：

<pre class="wp-block-code"><code>sudo kubeadm init --pod-network-cidr 192.168.0.0/16 --cri-socket unix:///var/run/cri-dockerd.sock --control-plane-endpoint master-node-01.acytoo.net</code></pre>

如果服务器本身没有公网 ip ，需要指定的 endpoint，可以是域名，也可以是 ip 地址。

如果一切正常，会得到下面这样的输出。<figure class="wp-block-image size-large">

<img decoding="async" loading="lazy" width="1024" height="425" src="https://cdn.lirica.cn/wordpress/2023/09/image-106-1024x425.png" alt="" class="wp-image-2228" srcset="https://catcat.blog/wp-content/uploads/2023/09/image-106-1024x425.png 1024w, https://catcat.blog/wp-content/uploads/2023/09/image-106-300x125.png 300w, https://catcat.blog/wp-content/uploads/2023/09/image-106-768x319.png 768w, https://catcat.blog/wp-content/uploads/2023/09/image-106.png 1402w" sizes="(max-width: 1024px) 100vw, 1024px" /> </figure> 

**记下输出中的 kubeadm join 命令，接下来添加工作节点需要 Token，每个 Token 默认 24 小时后过期**

_Token 过期或者忘记，可以使用 `kubeadm token create --print-join-command` 直接生成一个新的。_

根据提示，下一步操作。

<pre class="wp-block-code"><code>mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config</code></pre>

然后，安装网络插件 calico.

##### <a href="#安装-calico" target="_blank"  rel="nofollow" >#</a>安装 Calico {.wp-block-heading}

目前版本 3.26.1，请到官网找最新版本 <a href="https://docs.tigera.io/calico/latest/getting-started/kubernetes/self-managed-onprem/onpremises#install-calico-with-kubernetes-api-datastore-50-nodes-or-less" target="_blank"  rel="nofollow" >docs.tigera.io/calico/latest/getting-started/kubernetes/self-managed-onprem/onpremises</a>

<pre class="wp-block-code"><code>curl https://raw.githubusercontent.com/projectcalico/calico/v3.26.1/manifests/calico.yaml -O
kubectl apply -f calico.yaml</code></pre>

至此，主节点就设置好了，查看状态。

<pre class="wp-block-code"><code>kubectl get node
kubectl get pod
kubectl get pods --all-namespaces</code></pre>

默认情况下，出于安全的考虑，不能在主节点上跑 pod。

##### <a href="#设置-worker-节点" target="_blank"  rel="nofollow" >#</a>设置 worker 节点 {.wp-block-heading}

使用 `kubeadm join` 命令，在一台已经安装了 `kubeadm` 等程序的服务器上，执行

<pre class="wp-block-code"><code>sudo kubeadm join master-node-01.acytoo.net:6443 --token sluqvx.itdsjivbewuiinfx \
        --discovery-token-ca-cert-hash sha256:95669c834aa9e861aed6a08783d1f893223ec327ad2612aba016c2b457afb2345 \
        --cri-socket unix:///var/run/cri-dockerd.sock</code></pre>

worker 节点也需要安装 calico。

#### <a href="#可能的-error" target="_blank"  rel="nofollow" >#</a>可能的 error {.wp-block-heading}

我在配置时，遇到了很多问题，绝大多数通过命令行的 error 提示，都能明白哪里出问题了，比如，cri-socket 服务无法启动，看看是否安装正常，手动调用，然后重启；或者端口占用，指定 cri-socket 等等。

唯一困扰我较长的问题是，worker 遇到 socket 8080 连接不上的问题（使用 `kubectl get nods` 输出 8080 拒绝连接），使用 `kuneadm join` 是 NotReady 状态，网上有很多讨论，很多人说 worker 节点也要有 `$HOME/.kube/config/admin.conf` 文件，但我先 init，再 join 也不行。最后在主节点删除了出问题的 worker 节点，重新运行一次相同的命令就通了，没有 `admin.conf` 文件。

在主节点删除 worker node:

<pre class="wp-block-code"><code>kubectl drain &#91;node name] --ignore-daemonsets
kubectl delete node &#91;node name]</code></pre>

#### <a href="#查看状态" target="_blank"  rel="nofollow" >#</a>查看状态 {.wp-block-heading}

回到主节点，查看 node。

<pre class="wp-block-code"><code>kubectl get nodes</code></pre>

#### <a href="#结语" target="_blank"  rel="nofollow" >#</a>结语 {.wp-block-heading}

Kubernetes 可配置项多，安装工具多，安装方法多，本文使用 kubeadm 方法安装，calico 做为网络插件。理论上支持 Debian 10/11/12 以及以 Debian 为基础的其他发行版，如 Ubuntu 等。