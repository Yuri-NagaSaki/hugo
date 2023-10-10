---
title: "Containerd task启动容器ctr: failed to create shim task: OCI runtime create failed"
date: "2023-03-21"
categories: 
  - "docker"
  - "laboratory"
---

错误信息如下:

```
ctr: failed to create shim task: OCI runtime create failed: unable to retrieve OCI runtime error (open /run/containerd/io.containerd.runtime.v2.task/i4t/nginx/log.json: no such file or directory): runc did not terminate successfully: exit status 127: unknown
```

我们执行的命令如下

```
[root@web01 ~]# ctr -n i4t c ls
CONTAINER    IMAGE                             RUNTIME                  
nginx        docker.io/library/nginx:alpine    io.containerd.runc.v2    
[root@web01 ~]# ctr -n i4t task start -d nginx
ctr: failed to create shim task: OCI runtime create failed: unable to retrieve OCI runtime error (open /run/containerd/io.containerd.runtime.v2.task/i4t/nginx/log.json: no such file or directory): runc did not terminate successfully: exit status 127: unknown
```

原因是 runc 异常，需要重新安装依赖

**解决办法:**  
这个是说缺少依赖包`libseccomp`，需要注意的是`centos7`中 yum 下载的版本是 2.3 的，版本不满足我们最新 containerd 的需求，需要下载 2.4 以上的

```
#卸载原来的
[i4t@web01 ~]# rpm -qa | grep libseccomp
libseccomp-devel-2.3.1-4.el7.x86_64
libseccomp-2.3.1-4.el7.x86_64
[i4t@web01 ~]# rpm -e libseccomp-devel-2.3.1-4.el7.x86_64 --nodeps
[i4t@web01 ~]# rpm -e libseccomp-2.3.1-4.el7.x86_64 --nodeps
#下载高于2.4以上的包
[i4t@web01 ~]# wget http://rpmfind.net/linux/centos/8-stream/BaseOS/x86_64/os/Packages/libseccomp-2.5.1-1.el8.x86_64.rpm
#安装
[i4t@web01 ~]# rpm -ivh libseccomp-2.5.1-1.el8.x86_64.rpm 
warning: libseccomp-2.5.1-1.el8.x86_64.rpm: Header V3 RSA/SHA256 Signature, key ID 8483c65d: NOKEY
Preparing...                          ################################# [100%]
Updating / installing...
   1:libseccomp-2.5.1-1.el8           ################################# [100%]
#查看当前版本
[root@web01 ~]# rpm -qa | grep libseccomp
libseccomp-2.5.1-1.el8.x86_64
```

执行 runc

```
[root@web01 ~]# runc
NAME:
   runc - Open Container Initiative runtime
runc is a command line client for running applications packaged according to
the Open Container Initiative (OCI) format and is a compliant implementation of the
Open Container Initiative specification.
runc integrates well with existing process supervisors to provide a production
container runtime environment for applications. It can be used with your
existing process monitoring tools and the container will be spawned as a
direct child of the process supervisor.
Containers are configured using bundles. A bundle for a container is a directory
that includes a specification file named "config.json" and a root filesystem.
The root filesystem contains the contents of the container.
To start a new instance of a container:
....
```
