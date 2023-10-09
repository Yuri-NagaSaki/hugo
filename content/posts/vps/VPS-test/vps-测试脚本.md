---
title: "vps 测试脚本"
date: "2023-02-23"
weight: 1
categories: 
  - "vps"
featuredImage: https://cdn.lirica.cn/wordpress/2023/07/109615256_p0.webp
license: CC BY-NC-SA 4.0

hiddenFromHomePage: false
hiddenFromSearch: false
---

记录一些常见的vps脚本
## 1.vps体检脚本

```
bash <(curl -L -s https://bench.kangjw.me/kkb.sh)
bash <(wget -qO- --no-check-certificate https://gitlab.com/spiritysdx/za/-/raw/main/ecs.sh)
wget -qO- bench.sh | bash
curl -sL yabs.sh | bash
wget -qO- benchy.pw | sh
bash <(curl -L -s check.unlock.media)
lscpu
Memory default via free -h --total
Storage default via df -hT --total
Default SWAP or partition via swapon --show
bash <(curl -sL https://raw.githubusercontent.com/LloydAsp/NodeBench/main/NodeBench.sh)

LemonBench
wget -qO- https://raw.githubusercontent.com/LemonBench/LemonBench/main/LemonBench.sh | bash -s -- --fast

GB6 跑分脚本，附带宽测试：
curl -sL yabs.sh | bash

GB6 剔除带宽测试，因为都是国外节点测试，国内跑没多大意义：
curl -sL yabs.sh | bash -s -- -i

GB5 跑分脚本，附带宽测试：
curl -sL yabs.sh | bash -5

GB5 剔除带宽测试：
curl -sL yabs.sh | bash -s -- -i -5

流媒体测试：
bash <(curl -L -s check.unlock.media)
全面测试：
bash <(wget -qO- https://down.vpsaff.net/linux/speedtest/superbench.sh)
多线路网速测试：
bash <(wget -qO- https://raw.githubusercontent.com/chiron688/linux_jobs/main/speed.sh)
 
```

## 2.回程脚本

```
curl https://raw.githubusercontent.com/zhucaidan/mtr_trace/main/mtr_trace.sh|bash
```

## 3.Docker一键脚本(仅支持debian)

```
apt install wget curl sudo vim git -y 
curl -fsSL https://get.docker.com | bash -s docker
```

## 4.Node NVM脚本

```
安装 nvm (可选)
nvm 可以用于管理 Node.js。

打开终端，使用一键脚本，可以便捷地安装 nvm：

curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
重启终端即可生效

安装 Node.js 最新的 LTS 版本：

nvm install --lts
```

## 5.GPT 解锁测试

```
bash <(curl -Ls https://cdn.jsdelivr.net/gh/missuo/OpenAI-Checker/openai.sh)
```

## 6.综合工具箱

```
wget -O box.sh https://raw.githubusercontent.com/BlueSkyXN/SKY-BOX/main/box.sh && chmod +x box.sh && clear && ./box.sh
```

## 7.流媒体测试

```
bash <(curl -L -s https://raw.githubusercontent.com/lmc999/RegionRestrictionCheck/main/check.sh)
```

## 8.Oracle 修改root脚本

```
#!/bin/bash
echo root:11235879 |sudo chpasswd root
sudo sed -i 's/^#\?PermitRootLogin.*/PermitRootLogin yes/g' /etc/ssh/sshd_config;
sudo sed -i 's/^#\?PasswordAuthentication.*/PasswordAuthentication yes/g' /etc/ssh/sshd_config;
sudo service sshd restart
```

默认密码是: 11235879  
登录后一定要修改密码！命令：`passwd`

## 9.Debian11开启bbr

```
 echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf
 echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf
 sysctl -p
查看内核是否已开启BBR

 sysctl net.ipv4.tcp_available_congestion_control
显示以下即已开启：
net.ipv4.tcp_available_congestion_control = reno cubic bbr


查看BBR是否启动

 lsmod | grep bbr
显示返回值即启动成功：

 tcp_bbr 20480 21
返回值有 tcp_bbr 模块即说明 bbr 启动。
```

## 10.Swap脚本

```
wget https://www.moerats.com/usr/shell/swap.sh && bash swap.sh
```

## 11.Oracle dd Debian11 脚本

```
bash <(wget --no-check-certificate -qO- 'https://moeclub.org/attachment/LinuxShell/InstallNET.sh') -d 11 -v 64 -a  -p 自定义密码
```

## 12.byte-unixbench 性能测试

```
git clone https://github.com/kdlucas/byte-unixbench.git
cd UnixBench
gcc --version
apt update
apt install build-essential
make
运行byte-unixbench测试：

在byte-unixbench目录中，运行以下命令来执行所有测试：
./Run
或者，您可以运行特定的测试。运行以下命令来列出可用的测试选项：
./Run -h
根据您的需求选择特定的测试。例如，要运行文件复制测试，可以使用以下命令：
./Run copy-file

wget --no-check-certificate https://github.com/teddysun/across/raw/master/unixbench.sh && chmod +x unixbench.sh && ./unixbench.sh
```

## 13.[PerformanceTest Linux](https://www.passmark.com/products/pt_linux/download.php) 测试

```
安装ncurses库：打开终端并使用以下命令安装ncurses库：

sudo apt update
sudo apt install libncurses5
这将使用包管理器apt安装libncurses5库。根据您的系统配置，您可能需要输入管理员密码以确认安装。

创建软链接：如果安装库后仍然出现问题，您可以尝试创建一个软链接。在终端中使用以下命令创建软链接：

sudo ln -s /usr/lib/libncurses.so.6 /usr/lib/libncurses.so.5
这将创建一个名为libncurses.so.5的软链接，指向已安装的libncurses.so.6文件。这可以解决某些应用程序对特定库版本的依赖性问题。

更新动态链接库缓存：执行以下命令更新动态链接库缓存：

sudo ldconfig
这将刷新系统的动态链接库缓存，使系统能够找到新安装的库文件。

./pt_linux_x64
执行脚本
```

## 14.回程多地区测试脚本

```
wget -qO- git.io/besttrace | bash
```

## 15.独立服务器检测硬盘通电时间

```
wget https://github.com/Aniverse/A/raw/i/a && bash a
```

## 16.[horonix-test-suite](https://my.oschina.net/u/2306127/blog/2250611)测试

```
apt --fix-broken install
apt install build-essential
sudo dpkg -i phoronix-test-suite_10.8.4_all.deb 
phoronix-test-suite benchmark smallpt
```

## 17.network-speed.xyz

```
wget -qO- network-speed.xyz | bash
region_name = na, sa, eu, asia, africa, middle-east, india, china, iran
wget -qO- network-speed.xyz | bash -s -- -r region_name
```
