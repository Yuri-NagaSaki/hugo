---
title: "Kubernetes 部署应用到集群中"
date: "2023-09-14"
categories: 
  - "k8s"
  - "laboratory"
---

#### 命令行运行

```
kubectl run testapp --image=ccr.ccs.tencentyun.com/k8s-tutorial/test-k8s:v1
kubectl get pod 查看是否成功建立

```

![](https://catcat.blog/wp-content/uploads/2023/09/image-77.png)

#### YML文件部署

##### pod.yaml 文件

```
apiVersion: v1
kind: Pod
metadata:
  name: test-pod
spec:
  # 定义容器，可以多个
  containers:
    - name: test-k8s # 容器名字
      image: ccr.ccs.tencentyun.com/k8s-tutorial/test-k8s:v1 # 镜像
```

#### 部署命令

```
mkdir Deployment && cd Deployment 
vim pod.yml # 填入上面的文件内容
kubectl apply -f pod.yml #创建pod
```

![](https://cdn.lirica.cn/wordpress/2023/09/image-78-1024x281.png)

#### Deployment方式

##### app.yml文件

```
apiVersion: apps/v1
kind: Deployment
metadata:
  # 部署名字
  name: test-k8s
spec:
  replicas: 2
  # 用来查找关联的 Pod，所有标签都匹配才行
  selector:
    matchLabels:
      app: test-k8s
  # 定义 Pod 相关数据
  template:
    metadata:
      labels:
        app: test-k8s
    spec:
      # 定义容器，可以多个
      containers:
      - name: test-k8s # 容器名字
        image: ccr.ccs.tencentyun.com/k8s-tutorial/test-k8s:v1 # 镜像

```

#### 部署命令

```
kubectl apply -f app.yml 
kubectl get deployment
```

![](https://catcat.blog/wp-content/uploads/2023/09/image-79-1024x266.png)

#### Deployment 通过 label 关联起来 Pods

![](https://catcat.blog/wp-content/uploads/2023/09/image-80.png)

### 常用命令

```
# 查看pod的IP等信息
kubectl get pod -o wide 
# 部署应用
kubectl apply -f app.yaml
# 查看 deployment
kubectl get deployment
# 查看 pod
kubectl get pod -o wide
# 查看 pod 详情
kubectl describe pod pod-name
# 查看 log
kubectl logs pod-name
# 进入 Pod 容器终端， -c container-name 可以指定进入哪个容器。
kubectl exec -it pod-name -- bash
# 伸缩扩展副本
kubectl scale deployment test-k8s --replicas=5
# 把集群内端口映射到节点
kubectl port-forward pod-name 8090:8080
# 查看历史
kubectl rollout history deployment test-k8s
# 回到上个版本
kubectl rollout undo deployment test-k8s
# 回到指定版本
kubectl rollout undo deployment test-k8s --to-revision=2
# 删除部署
kubectl delete deployment test-k8s
```

#### kubectl describe ID 查看 pod 详情

![](https://catcat.blog/wp-content/uploads/2023/09/image-81.png)

#### kubectl logs ID 查看日志

![](https://catcat.blog/wp-content/uploads/2023/09/image-82-1024x130.png)

#### kubectl logs ID -f 持续查看日志

![](https://catcat.blog/wp-content/uploads/2023/09/image-83-1024x127.png)

#### kubectl exec -it ID- bash 进入Pod

![](https://catcat.blog/wp-content/uploads/2023/09/image-84-1024x56.png)

#### kubectl scale deployment ID --replicas=5 伸缩扩展副本

![](https://catcat.blog/wp-content/uploads/2023/09/image-85-1024x344.png)

#### kubectl port-forward pod-name 1234:8080 映射容器内部端口

![](https://catcat.blog/wp-content/uploads/2023/09/image-86-1024x159.png)

![](https://catcat.blog/wp-content/uploads/2023/09/image-87.png)
