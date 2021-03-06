---
title: 停用Istio
description: 本节介绍了如何在集群中卸载 Istio 以及如何在命名空间或工作负载中禁用 Istio。
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
  - rancher 2.5
  - Istio
  - 基于角色的访问控制策略
---

## 概述

本节介绍了如何在集群中卸载 Istio 以及如何在命名空间或工作负载中禁用 Istio。

## 在集群中卸载 Istio

1. 从**集群资源管理器**导航到**应用市场**中的**安装的应用程序**，并找到`rancher-istio`。
1. 选择`istio-system`命名空间中的所有应用程序，并单击**删除**。

**结果：**集群中的`rancher-istio`应用程序被删除。Istio sidecar 不能部署在集群的任何工作负载上。

:::note 说明
不能再禁用和重新启用你的 Istio 安装。如果你想为将来的安装保存你的设置，请查看并保存单个 YAML，以便为将来的安装提供参考/重用。
:::

## 在命名空间禁用 Istio

1. 在**集群资源管理器**视图中，使用侧边导航选择**命名空间**页。
1. 在**命名空间**页面，您将看到一个命名空间的列表。转到您要禁用的命名空间，并单击选择**以表格形式编辑**或**以 Yaml 形式编辑**。
1. 删除命名空间中的`istio-injection=enabled`标签。
1. 单击**保存**。

**结果：**当工作负载部署在此命名空间中时，它们将不具备 Istio sidecar。

## 在工作负载中禁用 Istio

在命名空间中禁用 Istio，然后在其中重新部署工作负载。它们将在没有 Istio sidecar 的情况下被部署。
