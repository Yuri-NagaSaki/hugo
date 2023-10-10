---
title: "ChatGPT增加对sentry.io的规则"
date: "2023-05-28"
categories: 
  - "laboratory"
---

## ChatGPT封禁可能的原因

- 使用的同一网络中有大规模滥用账户导致被波及

- 访问来源网络不在OpenAI的支持区域中

- 续费使用高风险的虚拟支付账户

经试验，chatgpt网页版在使用过程中，js会向sentry.io发送跨域请求，其中包含一个key，sentry.io是一个提供日志收集的第三方平台，如果用户使用域名分流的方式，或者机场后端解锁只过滤了openai.com，就会导致原本梯子的ip泄露。

因此建议将sentry.io添加进相关规则列表。  

## Clash For Windows修改规则

### 右键订阅选择rule

![](https://catcat.blog/wp-content/uploads/2023/05/image-5.png)

### 将**sentry.io**填入输入框，type类型选择**DOMAIN-SUFFIX**，代  
理选择**REJECT**，点击**Save（添加）**

![](https://catcat.blog/wp-content/uploads/2023/05/image-6.png)

### 打开网页**sentry.io**，在CFW的connections里观察该域名是否走了刚刚修改规则的代理，如果是，说明修改成功。

##
