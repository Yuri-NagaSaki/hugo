---
title: "Rabbitmq 如何安装插件"
date: "2023-04-08"
categories: 
  - "rabbitmq"
  - "laboratory"
---

# Rabbitmq 如何安装插件

> 安装 rabbitmq\_delayed\_message\_exchange 和 amqp\_client

## 查看本地插件[#](#2590308056)

```
# rabbitmq-plugins list
 Configured: E = explicitly enabled; e = implicitly enabled
 | Status:   * = running on rabbit@7f153b30f57e
 |/
[  ] rabbitmq_amqp1_0                  3.6.14
[  ] rabbitmq_auth_backend_ldap        3.6.14
[  ] rabbitmq_auth_mechanism_ssl       3.6.14
[  ] rabbitmq_consistent_hash_exchange 3.6.14
[  ] rabbitmq_event_exchange           3.6.14
[  ] rabbitmq_federation               3.6.14
[  ] rabbitmq_federation_management    3.6.14
[  ] rabbitmq_jms_topic_exchange       3.6.14
[E*] rabbitmq_management               3.6.14
[e*] rabbitmq_management_agent         3.6.14
[  ] rabbitmq_management_visualiser    3.6.14
[  ] rabbitmq_mqtt                     3.6.14
[  ] rabbitmq_random_exchange          3.6.14
[  ] rabbitmq_recent_history_exchange  3.6.14
[  ] rabbitmq_sharding                 3.6.14
[  ] rabbitmq_shovel                   3.6.14
[  ] rabbitmq_shovel_management        3.6.14
[  ] rabbitmq_stomp                    3.6.14
[  ] rabbitmq_top                      3.6.14
[  ] rabbitmq_tracing                  3.6.14
[  ] rabbitmq_trust_store              3.6.14
[e*] rabbitmq_web_dispatch             3.6.14
[  ] rabbitmq_web_mqtt                 3.6.14
[  ] rabbitmq_web_mqtt_examples        3.6.14
[  ] rabbitmq_web_stomp                3.6.14
[  ] rabbitmq_web_stomp_examples       3.6.14
[  ] sockjs                            0.3.4
```

## 安装 amqp\_client 插件[#](#658696601)

```
# rabbitmq-plugins enable amqp_client                  
Plugin configuration unchanged.

Applying plugin configuration to rabbit@7f153b30f57e... nothing to do.
```

## 安装 rabbitmq\_delayed\_message\_exchange 插件[#](#2373673857)

```
# rabbitmq-plugins enable rabbitmq_delayed_message_exchange
Error: The following plugins could not be found:
  rabbitmq_delayed_message_exchange
```

> 通过上述命令发现插件 rabbitmq\_delayed\_meaage\_exchange 没有安装，需要下载安装

## 下载 rabbitmq\_delayed\_meaage\_exchange[#](#585725620)

> 下载地址：[http://www.rabbitmq.com/community-plugins.html](http://www.rabbitmq.com/community-plugins.html)

```
# linux： 
wget https://dl.bintray.com/rabbitmq/community-plugins/3.6.x/rabbitmq_delayed_message_exchange/rabbitmq_delayed_message_exchange-20171215-3.6.x.zip
```

```
# unzip解压到
/usr/lib/rabbitmq/lib/rabbitmq_server-version/plugins/rabbitmq_delayed_message_exchange-20171201-3.7.x.ez
```

## 重新安装插件[#](#115400139)

```
# rabbitmq-plugins enable rabbitmq_delayed_message_exchange
Error: The following plugins could not be found:
  rabbitmq_delayed_message_exchange
```

## 参考文档

```
链接：https://blog.csdn.net/youjin/article/details/82586888
```
