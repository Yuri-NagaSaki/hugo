---
title: "在ubuntu上通关mosh替代ssh连接解决vps延迟高的问题"
date: "2023-03-14"
categories: 
  - "laboratory"
---

Mobile Shell 是一款免费且快速的远程终端应用程序。它允许漫游，支持间歇性连接，并提供用户击键的智能本地回显和行编辑。您已经了解了 SSH。Mosh 旨在支持 SSH 的典型交互使用。由于 Mosh 更健壮且响应更快，尤其是在 Wi-Fi、蜂窝和长距离链路上，因此它被认为是交互式 SSH 终端的良好替代品。Mosh 也几乎适用于所有 GNU/Linux、FreeBSD、Solaris、Mac OS X 和 Android。

### **什么是 Mosh 及其工作原理？**

Mosh 是免费的命令行软件，用于通过 Internet 从客户端计算机连接到服务器以运行远程终端。它可用于 GNU/Linux、BSD、macOS、Solaris、Android、Chrome 和 iOS。Mosh 类似于 SSH，具有旨在提高移动用户可用性的附加功能。Mosh 比 SSH 更智能。当 SSH 客户端在显示您的输入之前等待来自服务器的 TCP 响应时，Mosh 会实时显示您的输入，甚至会给出带下划线的输入预测。mosh 程序将通过 SSH 连接到**_user@host_**以建立连接。如您所知，SSH 可能会提示用户输入密码或使用公钥身份验证来登录。但是 mosh 在服务器计算机上运行 mosh-server 进程（作为用户）。这样，与众所周知的相比，Mosh 带来了一些明显的优势SSH连接。

在长时间延迟或不可靠的链接上，Mosh 速度更快，响应更快。所以，不难说 Mosh 是 SSH 的替代品。当连接丢失时，Mosh 会尝试自动重新连接到您，甚至在您不注意的情况下。

_让我们在下面回顾一下**使用 Mosh 而不是 SSH 的**最重要原因：_

1- 即使您的 IP 发生变化，Mosh 也会保持连接状态。

2- 当您的网络在失去互联网连接后恢复正常或您将系统置于睡眠模式时，Mosh 将恢复与您的网络机器的连接。

3- 您无需成为超级用户即可安装或运行 Mosh。

4- Mosh 客户端通过 SSH 登录服务器，用户提供与之前相同的凭据。

5- Mosh 将在您的终端中运行，例如 xterm、gnome-terminal、urxvt、Terminal.app、iTerm、emacs、screen 或 tmux。

6- 与 SSH 不同，Mosh 不会填满网络缓冲区，因此 Control-C 始终可以停止失控的进程。假设如果您请求一个 200MB 的文件而不是 100MB，您可以通过按**CTRL+C**立即停止它。

### **Mosh 外壳的优势**

您现在对 Mosh Shell 了解更多，如果您不确定是否将其替换为 SSH，请查看以下列表：

1- Mosh 非常高效。

2- Mosh 在低带宽或间歇性连接上运行良好。

3- 与 ET 一样，连接在 WiFi 网络和中断中持续存在。

4- Mosh 允许您在 SSH 和 ET 仍在等待命令完成或连接重新建立时输入。

5- 处理丢包的机制。

6- Mosh 能够使用与 SSH 中相同的旧方法登录。

## **如何在 Ubuntu 20.04 上安装 Mosh Shell**

要在你的 Ubuntu 20.04 系统上安装 Mosh 包，你只需要运行以下命令：

```
apt-get update -y
```

```
apt-get install mosh -y
```

**_注意_：**如果您正在运行[防火墙](https://blog.eldernode.com/setup-firewall-ufw-ubuntu-20/)与 iptables 一样，使用以下命令手动打开这些端口：

```
sudo iptables -I INPUT 1 -p udp --dport 60000:61000 -j ACCEPT
```

### **在 Ubuntu Linux 上将 Mosh Shell 配置为 SSH 替代方案**

安装 Mosh shell 后，您就可以**开始**使用它了。因此，运行以下命令连接到您的远程系统：

```
mosh root@Your_IP_Address
```

然后，您应该能够连接到您的远程系统。此外，您可以通过运行以下命令来检查已安装的 Mosh 的**版本：**

```
mosh--version
```

Mosh 支持很多选项，要查看所有选项，请输入：

```
mosh--help
```
