---
title: "Kubectl 常用命令"
date: "2023-10-07"
categories: 
  - "Kubernetes"
---

## 1\. kubectl 命令摘要

基础命令（初级）Basic Commands（Beginner）

| 命令 | 说明 |
| --- | --- |
| kubectl create | 通过 yaml/json 文件或者标准输入创建一个资源对象，支持很多子命令 例如 namespace pod deployment service 等 |
| kubectl expose | 将 yaml/json 文件中定义的资源对象的端口暴露给新的 service 资源对象 |
| kubectl run | 创建并运行一个或多个容器镜像 |
| kubectl set | 配置资源对象设置特定功能 |

基础命令（中级）Basic Commands（Intermediate）

| 命令 | 说明 |
| --- | --- |
| kubectl explain | 查看资源对象的详细信息(一般用一编写 yaml 的时候做一个提示 kubectl explain deployment 会出现 deployment 下面可以写的字段以及字段属性还有 可以逐级使用) |
| kubectl get | 获取一个或多个资源对象的信息 |
| kubectl edit | 使用默认编辑器编辑服务器上定义的资源对象 |
| kubectl delete | 通过 yaml/json 文件、标准舒服、资源名称或标签选择器来删除资源 |

部署命令 DeployCommands

| 命令 | 说明 |
| --- | --- |
| kubectl rollout | 资源管理对象的部署 |
| kubectl rollout-update | 使用 rc（replication controller）来做滚动更新 |
| kubectl scale | 扩容或者缩容 deployment replicaset replication contrller 等 |
| kubectl autoscale | 自动设置在 k8s 系统中运行的 pod 数量（水平自动伸缩） |

集群管理命令 Cluster Manager Commands

| 命令 | 说明 |
| --- | --- |
| kubectl cetificate | 修改证书资源对象 |
| kubectl cluster-info | 查看集群信息 |
| kubectl top | 显示资源 cpu 内存 存储使用情况 |
| kubectl cordon | 标记节点为不可调度 |
| kubectl uncordon | 指定节点为可调度 |
| kubectl drain | 安全的驱逐节点的所有 pod |
| kubectl taint | 将一个或多个节点设置为污点 |

故障排查和调试命令 Troubleshooting adn Debugging Commands

| 命令 | 说明 |
| --- | --- |
| kubectl describe | 显示一个或多个资源对象的详细信息 |
| kubectl logs | 输出 pod 资源对象中一个容器的日志 |
| kubectl attach | 连接到一个运行的容器 |
| kubectl exec | 在指定容器内执行命令 |
| kubectl port-forward | 将本机指定端口映射到 pod 资源对象的端口 |
| kubectl proxy | 将本机指定端口映射到 kube-apiserver |
| kubectl cp | 用于 pod 与主机交换文件 |
| kubectl auth | 检查验证 |

高级命令 Advanced Commands

| 命令 | 说明 |
| --- | --- |
| kubectl diff | 对比本地 yaml/json 文件与 kube-apiserver 中运行的配置文件是否有差异 |
| kubectl apply | 通过 yaml/json 文件 标准输入对资源进行配置更新或者创建 |
| kubectl patch | 通过 patch 方式修改资源对象字段（补丁式） |
| kubectl replace | 通过 yaml/json 文件或者标准输入来替换资源对象 |
| kubectl wait | 在一个或者多个资源上等待条件达成 |
| kubectl convert | 转换 yaml/json 文件为不同的资源版本 |
| kubectl kustomize | 定制 kubernetes 配置 |

设置命令 Settings Commands

| 命令 | 说明 |
| --- | --- |
| kubectl label | 增删改资源的标签 |
| kubectl annotate | 更新一个或者多个资源对象的注释（annotaion）信息 |
| kubectl completion | 命令自动补全 |

其他命令 Other Commands

| 命令 | 说明 |
| --- | --- |
| kubectl config | 管理 kubeconfig 配置文件 |
| kubectl plugin | 运行命令行插件功能 |
| kubectl version | 查看客户端服务端的系统版本信息 |
| kubectl api-versions | 列出当前 kubernetes 系统支持的资源组和资源版本表现形式为/ |
| kubectl api-resources | 列出当前 kubernetes 系统支持的 resource 资源列表 |
| kubectl options | 查看支持的参数列表 |

## 2\. 常见的 RESOURCE\_NAME

| 名称 | 缩写 |
| --- | --- |
| all |  |
| certificatesigningrequests | (缩写 csr) |
| clusterrolebindings |  |
| clusterrol |  |
| componentstatuses | (缩写 cs) |
| configmaps | (缩写 cm) |
| controllerrevisions |  |
| cronjobs |  |
| customresourcedefinition | (缩写 crd) |
| daemonsets | (缩写 ds) |
| deployments | (缩写 deploy) |
| endpoints | (缩写 ep) |
| events | (缩写 ev) |
| horizontalpodautoscalers | (缩写 hpa) |
| ingresses | (缩写 ing) |
| jobs |  |
| limitranges | (缩写 limits) |
| namespaces | (缩写 ns) |
| networkpolicies | (缩写 netpol) |
| nodes | (缩写 no) |
| persistentvolumeclaims | (缩写 pvc) |
| persistentvolumes | (缩写 pv) |
| poddisruptionbudgets | (缩写 pdb) |
| podpreset |  |
| pods | (缩写 po) |
| podsecuritypolicies | (缩写 psp) |
| podtemplates |  |
| replicasets | (缩写 rs) |
| replicationcontrollers | (缩写 rc) |
| resourcequotas | (缩写 quota) |
| rolebindings |  |
| roles |  |
| secrets |  |
| serviceaccounts | (缩写 sa) |
| services | (缩写 svc) |
| statefulsets | (缩写 sts) |
| storageclasses | (缩写 sc) |

## 3\. kubectl 重要命令详解

### kubectl create

通过配置文件名或 stdin 创建一个集群资源对象。支持 JSON 和 YAML 格式的文件。

语法：

```
kubectl create -f FILENAME
```

示例：

```
# 通过 pod.yml 文件创建一个 pod
kubectl create -f ./pod.yml

# 通过 stdin 的 yml 创建一个 pod
cat pod.yml | kubectl create -f -

# 为 gitlab-runner 在 namespace 下授权管理员角色
kubectl create rolebinding deploy-runner --clusterrole=cluster-admin --serviceaccount=deploy:default --namespace=hsh-pre-service
```

### kubectl expose

将资源暴露为新的 Kubernetes Service。指定 deployment、service、replica set、replication controller 或 pod，并使用该资源的选择器作为指定端口上新服务的选择器。deployment 或 replica set 只有当其选择器可转换为 service 支持的选择器时，即当选择器仅包含 matchLabels 组件时才会作为暴露新的 Service。

语法：

```
kubectl expose (-f FILENAME | TYPE NAME) [--port=port] [--protocol=TCP|UDP] [--target-port=number-or-name] [--name=name] [--external-ip=external-ip-of-service] [--type=type]
```

示例：

```
# 为 rc 的 nginx 创建 service，并通过 service 的 80 端口转发至容器的 8000 端口上
kubectl expose rc nginx --port=80 --target-port=8000

# 由 “nginx-controller.yml” 中指定的 type 和 name 标识的 rc 创建 service，并通过 service 的 80 端口转发至容器的 8000 端口上
kubectl expose -f nginx-controller.yml --port=80 --target-port=8000
```

### kubectl get

获取一个或多个资源对象的信息。

语法：

```
kubectl get RESOURCE_NAME
```

示例：

```
# 查看 master 状态
kubectl get componentstatuses
 
# 查看所有命名空间
kubectl get namespaces
 
# 列出所有的 pods
kubectl get pods
 
# 显示更多的 pods 列表信息(例如 pod 的 ip 和所处的 node)
kubectl get pods -o wide
 
# 列出名字为 web 的 rc
kubectl get replicationcontroller web
 
# 获取名字为 web-pod-13cd8 的 pod 的信息，并以 json 格式输出
kubectl get -o json pod web-pod-13cd8
 
# 根据 pod 文件查找 pod，并以 json 格式输出
kubectl get -f pod.yaml -o json
 
# 获取 pod 容器的状态
kubectl get -o template pod/kube-dns-795f5f6f9c-ldxxs --template {{.status.phase}}
 
# 同时获取所有的 rc 和 service
kubectl get rc,services
 
# 获取符合条件的所有 rc,svc,pod
kubectl get rc/web service/frontend pods/web-pod-13cd8
 
# 获取所有 resource
kubectl get all
```

### kubectl edit

使用默认编辑器 编辑服务器上定义的资源。使用命令行工具获取的任何资源都可以使用 edit 命令编辑。edit 命令会打开使用 KUBE\_EDITOR，GIT\_EDITOR 或者 EDITOR 环境变量定义的编辑器，可以同时编辑多个资源，但所编辑过的资源只会一次性提交。edit 除命令参数外还接受文件名形式。文件默认输出格式为 YAML。要以 JSON 格式编辑，请指定 “-o json” 选项。

语法：

```
kubectl edit (RESOURCE/NAME | -f FILENAME)
```

示例：

```
# 编辑名为 “docker-registry” 的 service
kubectl edit svc/docker-registry

# 使用替代的编辑器
KUBE_EDITOR="nano" kubectl edit svc/docker-registry

# 以 YAML 格式输出编辑 deployment “mydeployment”，并将修改的配置保存在 annotation 中
kubectl edit deployment/mydeployment -o yaml --save-config
```

### kubectl delete

通过配置文件名、stdin、资源名称或label选择器来删除资源。支持 JSON 和 YAML 格式文件。可以只指定一种类型的参数：文件名、资源名称或 label 选择器。

注意：执行 delete 命令时不会检查资源版本，如果在执行 delete 操作时有人进行了更新操作，那么更新操作将连同资源一起被删除。

语法：

```
kubectl delete ([-f FILENAME] | TYPE [(NAME | -l label | --all)])
```

示例：

```
# 使用 pod.yml 中指定的资源类型和名称删除 pod
kubectl delete -f ./pod.yml

# 根据传入 stdin 的 yml 所指定的类型和名称删除 pod
cat pod.json | kubectl delete -f -

# 删除名为“foo”和“bar”的 pod 和 service
kubectl delete pod,service foo bar

# 删除 Label 标签名为 name = myLabel 的 pod 和 service
kubectl delete pods,services -l name=myLabel

# 强制删除 dead node上 的 pod
kubectl delete pod foo --grace-period=0 --force

# 删除所有 pod
kubectl delete pods --all
```

### kubectl rollout

对资源进行管理，可用资源包括：deployments daemonsets

包含下列子命令：

- _history_（查看历史版本）

- _pause_（暂停资源）

- _resume_（恢复暂停资源）

- _status_（查看资源状态）

- _undo_（回滚版本）

语法：

```
kubectl rollout SUBCOMMAND
```

示例：

```
# 查看 deployment 的历史记录
kubectl rollout history deployment/abc

# 查看 daemonset 修订版 revision=3 的详细信息
kubectl rollout history daemonset/abc --revision=3

# 将 deployment 标记为暂停。只要 deployment 在暂停中，使用 deployment 更新将不会生效。
kubectl rollout pause deployment/nginx

# 恢复已暂停的 deployment
kubectl rollout resume deployment/nginx

# 查看 deployment 的状态
kubectl rollout status deployment/nginx

# 回滚到之前的 deployment 版本
kubectl rollout undo deployment/abc
kubectl rollout undo --dry-run=true deployment/abc

# 回滚到 daemonset 修订 revision=3 版本
kubectl rollout undo daemonset/abc --to-revision=3

# 将名为 foo 中的 pod 副本数设置为 3
kubectl scale --replicas=3 rs/foo

# 将由“foo.yaml”配置文件中指定的资源对象和名称标识的 Pod 资源副本设为 3
kubectl scale --replicas=3 -f foo.yaml

# 如果 mysql 当前副本数为 2，则将其扩展至 3
kubectl scale --current-replicas=2 --replicas=3 deployment/mysql

# 设置多个 RC 中 Pod 副本数量
kubectl scale --replicas=5 rc/foo rc/bar
```

### kubectl describe

输出指定的一个/多个资源的详细信息，此命令组合调用多条 API，输出指定的一个或者一组资源的详细描述。

语法：

```
kubectl describe (-f FILENAME | TYPE [NAME_PREFIX | -l label] | TYPE/NAME)
```

示例：

```
# 描述一个 node
kubectl describe nodes kubernetes-minion-emt8.c.myproject.internal

# 描述一个 pod
kubectl describe pods/nginx

# 描述 pod.yml 中的资源类型和名称指定的 pod
kubectl describe -f pod.yml

# 描述所有的 pod
kubectl describe pods

# 描述所有包含 label 标签名为 name=myLabel 的 pod
kubectl describe po -l name=myLabel

# 描述所有被 replication controller “frontend” 管理的 pod（rc 创建的 pod 都以 rc 的名字作为前缀）
kubectl describe pods frontend
```

### kubectl logs

输出 pod 中一个容器的日志，如果 pod 只包含一个容器则可以省略容器名。

语法：

```
kubectl logs [-f] [-p] POD [-c CONTAINER]
```

示例：

```
# 返回仅包含一个容器的 pod nginx 的日志快照
kubectl logs nginx

# 返回 pod ruby 中已经停止的容器 web-1 的日志快照
kubectl logs -p -c ruby web-1

# 持续输出 pod ruby 中的容器 web-1 的日志
kubectl logs -f -c ruby web-1

# 仅输出 pod nginx 中最近的 20 条日志
kubectl logs --tail=20 nginx

# 输出 pod nginx 中最近一小时内产生的所有日志
kubectl logs --since=1h nginx
```

### kubectl exec

在容器内部执行命令。

语法：

```
kubectl exec POD [-c CONTAINER] -- COMMAND [args...]
```

示例：

```

# 默认在 pod 123456-abcd 的第一个容器中运行“date”并获取输出
kubectl exec 123456-abcd date

# 在 pod 123456-abcd 的容器 ruby-container 中运行“date”并获取输出
kubectl exec 123456-abcd -c ruby-container date

# 切换到终端模式，将控制台输入发送到 pod 123456-abcd 的 ruby-container 的“bash”命令，并将其输出到控制台/错误控制台的信息发送回客户端
kubectl exec 123456-abcd -c ruby-container -i -t -- bash -il
```

### kubectl apply

通过配置文件名或 stdin 创建一个集群资源对象。支持 JSON 和 YAML 格式的文件。

语法：

```
kubectl apply -f FILENAME
```

示例：

```
# 通过 pod.yml 文件创建一个 pod
kubectl apply -f ./pod.yml

# 通过 stdin 的 yml 创建一个 pod
cat pod.yml | kubectl apply -f -
```

**使用 kubectl create 和 kubectl apply 创建资源对象的区别**：

| kubectl apply | kubectl create |
| --- | --- |
| 根据 yaml 文件中包含的字段（yaml 文件可以只写需要改动的字段），直接升级集群中的现有资源对象 | 首先删除集群中现有的所有资源，然后重新根据 yaml 文件（必须是完整的配置信息）生成新的资源对象 |
| yaml 文件可以不完整，只写需要的字段 | yaml 文件必须是完整的配置字段内容 |
| kubectl apply 只工作在 yaml 文件中的某些改动过的字段 | kubectl create 工作在 yaml 文件中的所有字段 |
| 在只改动了 yaml 文件中的某些声明时，而不是全部改动，你可以使用 kubectl apply | 在没有改动 yaml 文件时，使用同一个 yaml 文件执行命令 kubectl replace，将不会成功（fail 掉），因为缺少相关改动信息 |

### kubectl label

更新（增加、修改或删除）资源上的 label（标签）。label 必须以字母或数字开头，可以使用字母、数字、连字符、点和下划线，最长63个字符。如果 --overwrite 为 true，则可以覆盖已有的 label，否则尝试覆盖 label 将会报错。如果指定了 --resource-version，则更新将使用此资源版本，否则将使用现有的资源版本。

语法：

```
kubectl label [--overwrite] (-f FILENAME | TYPE NAME) KEY_1=VAL_1 ... KEY_N=VAL_N [--resource-version=version]
```

示例：

```

# 给名为 foo 的 Pod 添加 label unhealthy=true
kubectl label pods foo unhealthy=true

# 给名为 foo 的 Pod 修改 label 为 ‘status’ 的 value 值 ‘unhealthy’，且覆盖现有的 value
kubectl label --overwrite pods foo status=unhealthy

# 给 namespace 中的所有 pod 添加 label
kubectl label pods --all status=unhealthy

# 仅当 resource-version=1 时才更新名为 foo 的 Pod 上的 label
kubectl label pods foo status=unhealthy --resource-version=1

# 删除名为 “bar” 的 label（使用“ - ”减号相连）
kubectl label pods foo bar-
```
