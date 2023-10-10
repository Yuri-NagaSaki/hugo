---
title: "RabbitMQ 使用之 rabbitmq-plugins"
date: "2023-04-07"
categories: 
  - "rabbitmq"
  - "laboratory"
---

# rabbitmq-plugins

> rabbitmq-plugins 是管理 RabbitMQ broker 插件的命令行。

## 语法[#](#3945256341)

```
rabbitmq-plugins [-n node] {command} [command options ...]
```

## 说明[#](#2565978315)

rabbitmq-plugins 用于启用（enable）、禁用（disable）和浏览（browse）插件。 这些操作必须要由具有对 RabbitMQ 配置目录可写权限的用户执行。

一些插件依赖于其他的插件才能正常工作， rabbitmq-plugins 遍历这些依赖关系并且启用所有必需的插件。在 rabbitmq-plugins 命令行中列出的插件被标记为显式启用；依赖插件被标记为隐式启用。隐式启用的插件，在他们不需要的时候，在不再需要时会自动禁用。

启用、禁用和设置命令将更新插件文件，然后尝试连接到代理，并确保它运行所有启用的插件。默认情况下，如果无法连接到运行的代理（例如，如果它已停止），则会显示警告。指定 --online 或 --offline 来更改此行为。

## Commands[#](#3822054227)

```
list [-v] [-m] [-E] [-e] [pattern]
-v 显示所有插件的详情（详细）
-m 仅仅只显示插件的名称 (简约)
-E 仅仅只显示显式启用的插件
-e 仅仅只显示显式、隐式启用的插件
```

pattern 表示用于过滤插件名称的模式  
该命令，显示所有的插件，它们的版本号，依赖关系和描述。显示的每个插件内容的前缀是在 \[\] 内加上两种状态指示符，第一个指示符是 ""，表示该插件没有被启用；"E"的指示符表示该插件被显示启用；"e"的指示符表示该插件被隐式启用； 或者"!" 表示该插件被启用但缺失，因此无法运行。  
第二个指示符是 ""表示该插件没有运行；"\*" 表示在运行。如果给出了可选模式，则只显示名称匹配模式的插件。

```
rabbitmq-plugins list
# 显示所有的插件，每一行一个


rabbitmq-plugins list -v
# 显示所有的插件，并且显示插件的版本号和描述信息


rabbitmq-plugins list -v management
# 显示所有名称含有 "management" 的插件


rabbitmq-plugins list -e rabbit
# 显示所有显示或者隐式启动的插件
```

```
rabbitmq-plugins enable [--offline] [--online] {plugin ...}
# --offline 仅仅修改启动的插件文件
# --online 将与正在运行的代理连接失败视为致命错误
# plugin 一个或者多个待启用的插件
# 该命令将启用指定的插件和他们所有依赖的插件
```

```
rabbitmq-plugins disable [--offline] [--online] {plugin ...}
# --offline 仅仅修改启动的插件文件
# --online 将与正在运行的代理连接失败视为致命错误
# plugin 一个或者多个待禁用的插件
# 该命令将禁用指定的插件和他们所依赖的插件
```

```
rabbitmq-plugin set [--offline] [--online] {plugin ...}
# --offline 仅仅修改启用的插件文件
# --online 将与正在运行的代理连接失败视为致命错误
# plugin 零个或者多个待启用的插件
# 该命令将启用待指定的插件和他们所依赖的插件。和 rabbitmq-plugins enable 不同，该命令忽略了和覆盖了所有已存在的启用的插件。
# rabbitmq-plugins set 没有任何插件参数时，是合法的，表示禁用所有的插件
# rabbitmq-plugins set rabbitmq_management
# 上述命令，表示启用management插件，并且禁用其他所有插件
```

## 使用[#](#599074668)

通过命令 `rabbitmq-plugins enable rabbitmq_management` 来启动`rabbitmq_management` 插件，即可通过 web 端来查看集群的状态，有以下节点需要注意

如果通过 `localhost:15672` 查看`rabbitmq`服务器的信息，可以通过`guest`帐号来登录认证查看，但是由于默认情况下 `guest` 帐号具有所有的操作权限，并且还是默认帐号，处于安全因素的考虑，guest 用户只能通过 localhost 登录使用。所以最好是修改 guest 帐号的密码，且创建新的帐号来管理查看 rabbitmq 服务器
