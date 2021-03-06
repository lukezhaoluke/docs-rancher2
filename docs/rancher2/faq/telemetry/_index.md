---
title: 遥测
description: 什么是遥测？遥测收集了关于 Rancher 安装规模、组件版本以及使用的功能特性的集合信息。Rancher Labs 可用这些信息持续提升产品，并对第三方严格保密。
keywords:
  - rancher
  - rancher中文
  - rancher中文文档
  - rancher官网
  - rancher文档
  - Rancher
  - rancher 中文
  - rancher 中文文档
  - rancher cn
  - 常见问题
  - 遥测
---

## 什么是遥测？

遥测收集了关于 Rancher 安装规模、组件版本以及使用的功能特性的集合信息。Rancher Labs 可用这些信息持续提升产品，并对第三方严格保密。

## 遥测共收集了哪些信息？

我们不会收集如用户名、密码、名字和地址等用户信息。

主要收集的信息如下：

- 每个集群的规模（CPU 核数和内存）和节点统计信息（最小值、平均值、最大值和总值）
- 逻辑资源如集群、项目、命名空间和 Pod 的统计信息
- 部署集群和节点所使用的主机驱动的计数信息（如 GKE，EC2，导入，自定义）
- 部署的 Kubernetes、操作系统和 Docker 的版本
- 是否部署了一些可选的组件（例如鉴权服务提供者）
- Rancher 的镜像名称和版本
- 安装版本的独立随机 Identifier

## 如何查看被发送的信息？

如果开启了遥测，您可以访问`https://<your rancher server>/v1-telemetry`来查看当前发送的数据。

如果未开启遥测，收集数据的进程不运行，则没有数据被收集和发送。

## 如何关闭或开启遥测？

Rancher 初始化完成后，系统管理员可以访问**全局**中的**系统设置**菜单，在`telemetry-opt`处单击编辑修改为`in` 或 `out`，`in`表示开启遥测，`out`表示关闭遥测。
