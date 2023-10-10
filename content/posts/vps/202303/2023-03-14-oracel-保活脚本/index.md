---
title: "Oracel 保活脚本"
date: "2023-03-14"
categories: 
  - "docker"
  - "laboratory"
---

甲骨文官现在要收回闲置实例资源，使用率不高的免费实例可能会被清理。如果七天内符合以下条件，则 Oracle 会将免费实例视为空闲，并被回收。

- 95% 时间 CPU 利用率低于 10%

- 网络利用率低于 10%

- 内存利用率低于 10% （仅适用于 A1 形状）（ARM 实例）

官方公告地址：[https://docs.oracle.com/en-us/iaas/Content/FreeTier/freetier\_topic-Always\_Free\_Resources.htm](https://docs.oracle.com/en-us/iaas/Content/FreeTier/freetier_topic-Always_Free_Resources.htm)

甲骨文云 (Oracle Cloud) 将要清理闲置实例资源，很多童鞋使用甲骨文免费 vps 建站或者搭建梯子，ssr/v2ray 机场，如果删除的话，怪可惜的。甲骨文云 (Oracle Cloud) 免费 VPS 服务器如何保活？收集了一些甲骨文免费实例保活教程，有需要自行尝试。

## 计算圆周率占用 CPU 保活

```
nohup echo "scale=99999999;4*a(1)" | bc -lq > /dev/null &
nohup cpulimit -l 30   -p 22489 >/dev/null &
scale那个代表小数点后的位数，数越大计算时间越长
-l 那里可以控制cpu使用率0-200
-p 那里写程序的PID，通过top命令查找，或者 ps -aux | grep bc
运行以上指令后，执行 exit  命令，再关闭窗口退出 xshell，后台命令不会终止
或者直接 Shell 死循环：
nohup cpulimit -l 30 bash -c "while :;do a=1;done" > /dev/null 2>&1 &
如果报错，安装一下bc
apt install bc -y && apt install cpulimit -y
```

来源：[https://hostloc.com/thread-1131769-1-1.html](https://hostloc.com/thread-1131769-1-1.html)

## 甲骨文云 (Oracle Cloud) 一键保活脚本（一）

NeverIdle 项目地址：[https://github.com/layou233/NeverIdle](https://github.com/layou233/NeverIdle)

```
# 服务器安装 wget screen
yum install -y wget screen
# 下载编译后的可执行文件
# AMD服务器
wget https://github.com/layou233/NeverIdle/releases/download/0.1/NeverIdle-linux-amd64 -O NeverIdle
# ARM
wget https://github.com/layou233/NeverIdle/releases/download/0.1/NeverIdle-linux-arm64 -O NeverIdle
# 修改文件权限
chmod 777 NeverIdle
# 使用screen运行程序
screen -R baohuo
# 启动程序
./NeverIdle -c 2h -m 2 -n 4h
# 挂起screen 按 Ctrl+A+D
#再次进入screen 
screen -R baohuo
```

命令参数：

```
./NeverIdle -c 2h -m 2 -n 4h
```

其中：

- \-c 指启用 CPU 定期浪费，后面跟随每次浪费的间隔时间。如每 12 小时 23 分钟 34 秒浪费一次，则为 12h23m34s。按照格式填。

- \-m 指启用浪费的内存量，后面是一个数字，单位为 GiB。启动后会占用对应量的内存，并且保持不会释放，直到手动杀死进程。

- \-n 指启用网络定期浪费，后面跟随每次浪费的间隔时间。格式同 CPU。会定期执行一次 Ookla Speed Test（还会输出结果哦！）

## 甲骨文云 (Oracle Cloud) 一键保活脚本（二）

项目地址：[甲骨文一键自动锻炼](https://hostloc.com/thread-1132743-1-1.html)

每天 0 点开始每 3 小时让 cpu 自动锻炼 600 秒，一天锻炼 8 次共 80 分钟（负荷 10%～20%），满足 5% 时间 CPU 利用率大于 10%（每天至少 72 分钟)，锻炼量可以根据自己情况随心调节。

有宝塔的也可以用面板自带定时任务，甲骨文一键保活代码：

```
#AMD版本
cd /root && wget https://raw.githubusercontent.com/velor2012/lookbusy-docker/main/lookbusy -O lookbusy && chmod +x lookbusy && sudo echo "0 */3 * * * root timeout 600 /root/lookbusy -c 10-20 -r curve" >> /etc/crontab && grep -q centos /etc/os-release && service crond restart || service cron restart
#ARM版本
cd /root && wget https://raw.githubusercontent.com/velor2012/lookbusy-docker/main/lookbusy-arm -O lookbusy && chmod +x lookbusy && sudo echo "0 */3 * * * root timeout 600 /root/lookbusy -c 10-20 -r curve" >> /etc/crontab && grep -q centos /etc/os-release && service crond restart || service cron restart
```

查看执行日志：

```
cat /var/log/cron | grep lookbusy
```

一键卸载：

```
sed -i "/lookbusy/d" /etc/crontab && rm -f /root/lookbusy && grep -q centos /etc/os-release && service crond restart || service cron restart
```

## 甲骨文云 (Oracle Cloud) 一键保活脚本（三）

Oracle-server-keep-alive-script 项目地址：[Oracle-server-keep-alive-script](https://github.com/spiritLHLS/Oracle-server-keep-alive-script)

所有资源都是动态占用，实时调整，避免服务器有别的任何资源已经超过限额了仍然再占用资源。

适配系统：暂时已在 Ubuntu 中验证无问题，别的主流系统应该也没有问题。

可选占用：CPU，内存，带宽

安装完毕后等待 5 分钟看看占用情况 (CPU 占用初始压力参数很低，时间不够看不出负载的)，如果超过 10 分钟无占用则有问题请卸载脚本反馈问题

因为更新有延迟需要等待 CDN 加载最新脚本，请留意脚本当前更新日期：2023.02.04

选项 1 安装，选项 2 卸载，选项 3 退出脚本。安装过程中无脑回车则全部可选的占用都占用，不需要什么占用输入 n 再回车

最后会询问是否需要带宽占用的参数自定义，这时候默认选项就是 n，回车就使用默认配置，输入 y 再回车则需要按照提示自定义参数

```
curl -L https://raw.githubusercontent.com/spiritLHLS/Oracle-server-keep-alive-script/main/oalive.sh -o oalive.sh && chmod +x oalive.sh && bash oalive.sh
```

或

```
bash oalive.sh
```

或

```
bash <(wget -qO- --no-check-certificate https://raw.githubusercontent.com/spiritLHLS/Oracle-server-keep-alive-script/main/oalive.sh)
```

脚本说明：

- CPU 占用有计算素数模式和科学计算模式可自由选择，设定占用区间为 15~25%

- CPU 占用是动态的，每几秒检测一遍，计算任务动态调整，检测间隔也是动态调整

- CPU 占用增加了双重保险，不仅动态调整，还在守护进程中设置了最高占用，默认 30% 最高 (核数 \* 13% 如果低于 30% 时设置)

- 内存占用设定占用 20% 总内存，占用 300 秒休息 300 秒

- 内存占用每 300 秒检测一遍，动态调整增加占用的大小，如果你内存大于 20% 则不增加占用

- 带宽占用每 45 分钟下载一次 1G~10G 大小的文件进行占用，只下载不保存，下载过程中不会占用硬盘

- 带宽占用动态调整实际下载带宽 / 速率，限制下载时长最长 10 分钟，每次下载前先测试最大可用带宽实时调整为 20% 带宽下载

- 占用过程中使用守护进程和开机自启服务，保证占用任务持续且有效

- 可选择一键卸载所有占用服务，卸载会将所有脚本和服务卸载，包括任务、守护进程和开机自启的设置

资源定期浪费，可用于 Oracle 甲骨文保活。为了应对甲骨文最新回收机制而作的脚本。
