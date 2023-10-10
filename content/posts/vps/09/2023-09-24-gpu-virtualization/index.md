---
title: "GPU 虚拟化研究和方案"
date: "2023-09-24"
categories: 
  - "gpu"
  - "laboratory"
---

> **常见术语**  
> **GPU —————** Graphics Processing Unit，显卡  
> **CUDA ————** Compute Unified Device Architecture，英伟达 2006 年推出的计算 API  
> **VT/VT-x/VT-d —** Intel Virtualization Technology。-x 表示 x86 CPU，-d 表示 Device。  
> **SVM —————** AMD Secure Virtual Machine。AMD 的等价于 Intel VT-x 的技术。  
> **EPT —————** Extended Page Table，Intel 的 CPU 虚拟化中的页表虚拟化硬件支持。  
> **NPT —————** Nested Page Table，AMD 的等价于 Intel EPT 的技术。  
> **SR-IOV ———** Single Root I/O Virtualization。PCI-SIG 2007 年推出的 PCIe 虚拟化技术。  
> **PF —————** Physical Function，亦即物理卡  
> **VF —————** Virtual Function，亦即 SR-IOV 的虚拟 PCIe 设备  
> **MMIO ———** Memory Mapped I/O。设备上的寄存器或存储，CPU 以内存读写指令来访问。  
> **CSR ————** Control & Status Register，设备上的用于控制、或反映状态的寄存器。CSR 通常以 MMIO 的方式访问。  
> **UMD ————** User Mode Driver。GPU 的用户态驱动程序，例如 CUDA 的 UMD 是 libcuda.so  
> **KMD ————** Kernel Mode Driver。GPU 的 PCIe 驱动，例如英伟达 GPU 的 KMD 是 nvidia.ko  
> **GVA ————** Guest Virtual Address，VM 中的 CPU 虚拟地址  
> **GPA ————** Guest Physical Address，VM 中的物理地址  
> **HPA ————** Host Physical Address，Host 看到的物理地址  
> **IOVA ————** I/O Virtual Address，设备发出去的 DMA 地址  
> **PCIe TLP ——** PCIe Transaction Layer Packet  
> **BDF ————** Bus/Device/Function，一个 PCIe/PCI 功能的 ID  
> **MPT ————** Mediated Pass-Through，受控直通，一种设备虚拟化的实现方式  
> **MDEV ———** Mediated Device，Linux 中的 MPT 实现  
> **PRM ————** Programming Reference Manual，硬件的编程手册  
> **MIG ————** Multi-Instance GPU，Ampere 架构高端 GPU 如 A100 支持的一种 hardware partition 方案

## GPU工作流程

1. 应用层调用 GPU 支持的某个 API，如 OpenGL 或 CUDA

3. OpenGL 或 CUDA 库，通过 UMD (User Mode Driver)，提交 workload 到 KMD (Kernel Mode Driver)

5. KMD 写 CSR MMIO，把它提交给 GPU 硬件

7. GPU 硬件开始工作... 完成后，DMA 到内存，发出中断给 CPU

9. CPU 找到中断处理程序 —— KMD 此前向 OS Kernel 注册过的 —— 调用它

11. 中断处理程序找到是哪个 workload 被执行完毕了，...最终驱动唤醒相关的应用

## **PCIe 直通**

只能 1:1，不支持 1:N。其实并不能算真正的虚拟化。

原理：VM 中，使用原生的 GPU 驱动。它向 VM 内核分配内存，把 GPA 填入到 GPU 的 CSR 寄存器，GPU 用它作为 IOVA 来发起 DMA 访问，VT-d 保证把 GPA 翻译为正确的 HPA，从而 DMA 到达正确的物理内存。

## K8S容器下

### 1.vCUDA 架构（腾讯目前使用）

优点：支持显存和算力隔离，支持超小粒度切分，**开源方案**。

缺点：是由于是在CUDA层实现能力，需要替换CUDA库，故用户对其感知较大，需要对齐版本，存在一定的兼容性问题。

**_开源地址：[https://github.com/tkestack/vcuda-controller](https://github.com/tkestack/vcuda-controller)_**

![](https://catcat.blog/wp-content/uploads/2023/09/image-110.png)

### 2.cGPU 架构（阿里云）

优点：支持容器级GPU虚拟化，多个容器共享GPU，且实现显存和算力隔离，对cuda库等无侵入用户无感，在nvidia-container.-runtime层实现能力。  
缺点：只能在阿里云使用

产品白皮书：[https://developer.aliyun.com/article/771984?utm\_content=g\_1000184528](https://developer.aliyun.com/article/771984?utm_content=g_1000184528)

![](https://catcat.blog/wp-content/uploads/2023/09/image-109.png)

### 3.**[k8s-device-plugin](https://github.com/4paradigm/k8s-device-plugin)**

**vGPU device plugin** 基于NVIDIA官方插件([NVIDIA/k8s-device-plugin](https://github.com/NVIDIA/k8s-device-plugin))，在保留官方功能的基础上，实现了对物理GPU进行切分，并对显存和计算单元进行限制，从而模拟出多张小的vGPU卡。在k8s集群中，基于这些切分后的vGPU进行调度，使不同的容器可以安全的共享同一张物理GPU，提高GPU的利用率。此外，插件还可以对显存做虚拟化处理（使用到的显存可以超过物理上的显存），运行一些超大显存需求的任务，或提高共享的任务数。

**_开源地址：[https://github.com/4paradigm/k8s-device-plugin](https://github.com/4paradigm/k8s-device-plugin)_**

### 4.qGPU（腾讯最新方案）

腾讯云 Tencent Kubernetes Engine qGPU 服务（以下简称 TKE qGPU）是腾讯云推出的 GPU 容器虚拟化产品，支持多个容器共享 GPU 卡并支持容器间算力和显存精细隔离，同时提供业界唯一的在离线混部能力，在精细切分 GPU 资源的基础上，在最大程度保证业务稳定的前提下，提高 GPU 使用率，帮助客户大幅度节约 GPU 资源成本。

qGPU 依托 TKE 对外开源的 [Elastic GPU](https://github.com/elastic-ai/elastic-gpu) 框架，可实现对 GPU 算力与显存的细粒度调度，并支持多容器共享 GPU 与多容器跨 GPU 资源分配。同时依赖底层强大的 qGPU 隔离技术，可做到 GPU 显存和算力的强隔离，在通过共享使用 GPU 的同时，尽量保证业务性能与资源不受干扰。

**_产品文档：[https://cloud.tencent.com/document/product/457/61448](https://cloud.tencent.com/document/product/457/61448)_**

![](https://catcat.blog/wp-content/uploads/2023/09/image-111-1024x787.png)

### 5.OrionX (趋动科技)

Orion vGPU软件是一个为云或者数据中心内的AI应用，CUDA应用提供GPU资源池化，提供GPU虚拟化能力的系统软件。通过高效的通讯机制，使得AI应用，CUDA应用可以运行在云或者数据中心内任何一个物理机，Container或者VM内而无需挂载物理GPU。同时为这些应用程序提供在GPU资源池中的硬件算力。通过这种Orion GPU池化的能力，可以提供多个优点：

- 兼容已有的AI应用和CUDA应用，使其仍然具有使用GPU加速的性能

- 为AI应用和CUDA应用在云和数据中心的部署提供了很大的灵活度。无需受GPU服务器位置、资源数量的约束。

- Orion GPU资源随AI应用和CUDA应用启动时分配，随应用程序退出时自动释放。减少GPU空闲时间，提高共享GPU的周转率。

- 通过对GPU资源池的管理和优化，提高整个云和数据中心GPU的利用率和吞吐率。

- 通过统一管理GPU，减轻GPU的管理复杂度和成本。

**_产品白皮书：https://virtaitech.com/development/index?doc=4381wjhd22vqhys8f1ts893jn4_**

![](https://catcat.blog/wp-content/uploads/2023/09/image-112-1024x544.png)

## 商业方案

### 1.vGPU

英伟达官方提供，授权费很贵，且只能用于虚拟机平台，不能用于docker容器

原理：在 NVIDIA 虚拟 GPU 助力的虚拟化环境中，NVIDIA 虚拟 GPU (vGPU) 软件与 Hypervisor 一同安装在虚拟化层上。此软件可创建虚拟 GPU，使每个虚拟机 (VM) 都能共享安装在服务器上的物理 GPU。对于要求非常严苛的工作流程，单个 VM 可充分利用多个物理 GPU。我们的软件包含适用于各种 VM 的显卡或计算驱动。由于通常由 CPU 完成的工作分流到 GPU，因而用户可以获得更出色的体验。虚拟化和云环境可支持要求苛刻的工程和创意应用程序，以及计算密集型工作负载（例如 AI 和数据科学）。

地址：[https://www.nvidia.cn/data-center/virtualization/it-management/](https://www.nvidia.cn/data-center/virtualization/it-management/)

产品白皮书：[https://www.nvidia.cn/data-center/virtualization/resources/](https://www.nvidia.cn/data-center/virtualization/resources/)

### 2.MPS

英伟达最早提供的一种GPU任务共享案，基于MP1 seNver和MPl cliet提供共享计算能力，其致命缺点是erver或者client异常退出，会对其它dlient端造成大影响，这在生产环境中基本无法接受。（不建议）

### 3.Citrix XenServer

XenServer 是一个服务器虚拟化平台，它为虚拟化服务器和客户机操作系统提供虚拟化性能，几乎与裸机服务器的性能相匹配。

XenServer 使用 Xen 系统管理程序对安装了 XenServer 的每个服务器进行虚拟化，从而使每个服务器能够以卓越的性能同时托管多个虚拟机。 此外，还可以使用 XenServer 通过业界标准的共享存储器体系结构以及资源集群，将多个支持 Xen 的服务器合并成一个功能强大的资源池。 在此过程中， XenServer 支持将多个服务器作为资源池进行无缝虚拟化。 对这些资源进行动态控制，以提供最佳性能，提高弹性和可用性，并最大限度地使用数据中心资源。

官方白皮书：[https://www.citrix.com/products/citrix-hypervisor/](https://www.citrix.com/products/citrix-hypervisor/)

### 4.VMware ESXi 

教程：[在ESXI7上使用NVIDIA A6000 虚拟化GPU vgpu](https://www.bilibili.com/video/BV1n3411v7rD/?vd_source=14f013fcfb2dafa379f8b493e71432ee)

## wiki

1.[https://en.wikipedia.org/wiki/Comparison\_of\_platform\_virtualization\_software](https://en.wikipedia.org/wiki/Comparison_of_platform_virtualization_software)

2.[https://en.wikipedia.org/wiki/GPU\_virtualization](https://en.wikipedia.org/wiki/GPU_virtualization)
