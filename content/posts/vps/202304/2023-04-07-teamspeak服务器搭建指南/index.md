---
title: "teamspeak服务器搭建指南"
date: "2023-04-07"
categories: 
  - "laboratory"
---

## 一、前言

首先搬上teamspeak的官网：[https://www.teamspeak.com/en/](https://www.teamspeak.com/en/)

先来介绍一下teamspeak吧，简单的来说，他是一款老牌的开源VoIP工具软件，可以进行语音通话，在线聊天，文件共享等等功能，不过呢，最大的特点还是它的可定制性强，以及非常低的带宽占用和计算机资源占用，下面的话我就以Ubuntu 20系统为例，简单的讲一下怎样去搭建一个属于你自己的语音服务器。

## 二、前期准备

首先，我们先做好前期的准备工作。你要准备的有：

- 一台服务器，拥有公网IP

- 下载好对应服务器系统的teamspeak服务端文件

- 下载好teamspeak客户端文件

- 能够远程链接你的服务器以及向服务器上传文件的工具，例如putty，Xshell，winscp或MobaXterm等

讲一下服务端的下载，进入teamspeak的官网之后，点击Downloads并选择server选项卡

并选择与你服务器系统相适应的服务端进行下载。我这里因为服务器安装的是64位Ubuntu系统，因此选择LINUX系统的SERVER 64-BIT服务端文件进行下载：

之后的操作也全都是在Linux系统下进行的操作，winserver版本更简单，下载下来直接双击运行唯一的一个exe文件就行了，这里不再赘述。

下载好服务端后，客户端的下载仍然差不多，选择client选项卡，下载你客户端系统相应的文件即可。

当然你也可以下新版客户端，好看一点，用起来大差不差

## 三、安装配置服务端

## 1、设置配置文件

在准备好文件之后，就开始安装服务端了，

首先升级系统更新依赖包

```
sudo apt update
```

一般来说，我们都是以roo权限登陆的服务器，但是由于teamspeak是不能用这一用户运行的，因此我们需要新建一个用户来运行teamspeak服务端文件：

```
useradd teamspeak -m
passwd teamspeak
```

第二个指令之后会要求你输入新建的这个用户的密码并再次确认，跟着走就行了。

接下来，将之前准备好的服务端文件上传至服务器并解压，同时重命名文件夹（我这里是直接上传至根目录）

```
tar -xvf teamspeak3-server_linux_amd64-3.13.7.tar.bz2
mv teamspeak3-server_linux_amd64 teamspeak3
```

注意，这里服务端的版本号可能随着更新而变化，使用的时候不要直接复制

由于我们是将用teamspeak这一用户来运行服务端文件，因此我们还要把它拷贝给该用户并设置权限：

```
cp -R teamspeak3 /home/teamspeak/
chown -R teamspeak:teamspeak /home/teamspeak/teamspeak3/
```

接下来就是运行服务端文件了，首先切换到我们刚才新建的用户：

```
su - teamspeak
```

接下来进入服务端文件所在的目录（也就是我们之前重命名并拷贝过来的那一个）：

```
cd teamspeak3
```

接下来先不急着运行，我们先来创建一个新文件。如果这里我们不这么做，那么在运行时服务端会报错，因为它没有读到这个授权文件：

1-

```
touch .ts3server_license_accepted
```

在授权文件建立好了之后，我们就可以运行服务端了：

```
./ts3server_startscript.sh start
```

运行之后，你可以看到这样一串I M P O R T A N T 的信息，那么恭喜你，服务端运行成功了

把这一段信息复制下来备用，之后Ctrl +c终止服务即可

## 2、打开防火墙

现在的服务器一般来说防火墙直接在面板的策略组里面放行就行了，总共放行三个端口：

- 9987/udp

- 10011/tcp

- 30033/tcp

如果你服务器上还有防火墙程序例如，可以再手动添加端口放行：

```
systemctl start firewalld
firewall-cmd --zone=public --add-port=9987/udp --permanent
firewall-cmd --zone=public --add-port=10011/tcp --permanent
firewall-cmd --zone=public --add-port=30033/tcp --permanent
firewall-cmd --reload
```

## 四、设置服务开机启动

首先还是先切换回root用户(会要求输入root用户密码)：

```
su -
```

然后我们来新建一个自定义服务文件ts3.service（这里编辑器你用vim也行）：

```
vim /lib/systemd/system/ts3.service
```

该配置文件内容如下：

```
[Unit]
Description=Teamspeak server
After=network.target
[Service]
WorkingDirectory=/home/teamspeak/teamspeak3
User=teamspeak
Group=teamspeak
Type=forking
ExecStart=/home/teamspeak/teamspeak3/ts3server_startscript.sh start inifile=ts3server.ini
ExecStop=/home/teamspeak/teamspeak3/ts3server_startscript.sh stop
PIDFile=/home/teamspeak/teamspeak3/ts3server.pid
RestartSec=15
Restart=always
[Install]
WantedBy=multi-user.target
```

注意：这里的WorkingDirectory，ExecStart，ExecStop， PIDFile这四个参数是你服务端文件的绝对路径，如果你之前文件夹的路径跟我不一样，这里记得修改。

之后保存退出并重启服务器即可。

在服务文件编辑完毕之后，我们就可以使用systemctl指令来启动teamspeak服务端并令其开机自启：

启动服务端

```
systemctl start ts3
```

关闭服务端

```
systemctl stop ts3
```

开机自启

```
systemctl enable ts3
```

查看服务端运行信息

```
systemctl status ts3
```

至此，服务端配置完毕，开始运行。

## 五、报错处理

但是别急，有可能你运行`systemctl status ts3`看到的是这样的信息：

![](https://catcat.blog/wp-content/uploads/2023/10/image-149.png)

这时候我们还是先停止服务器运行，并重启服务器：

```
systemctl disable ts3
systemctl stop ts3
reboot
```

接下来切到teamspeak用户，进入TS服务器目录，然后运行这条指令：

```
su - teamspeak
cd teamspeak3
./ts3server_minimal_runscript.sh createinifile=1
```

看到差不多这样的信息，就说明成功了

![](https://catcat.blog/wp-content/uploads/2023/10/image-150.png)

此时CTRL+C退出，并重新回到root，再次赋予开机启动并开启服务器，查看状态应该可以看到如下信息

```
su -
systemctl enable ts3
systemctl start ts3
systemctl status ts3
```

![](https://catcat.blog/wp-content/uploads/2023/10/image-151.png)

好了，服务器开启成功。
