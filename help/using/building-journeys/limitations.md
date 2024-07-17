---
solution: Journey Optimizer
product: journey optimizer
title: 历程限制
description: 了解有关历程限制的更多信息
feature: Journeys, Best Practices, Guardrails
topic: Content Management
role: User
level: Intermediate
keywords: 历程，限制
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 47%

---

# 限制 {#journey-limitations}

以下是有关使用历程的限制。

## 常规操作限制 {#action-limitations}

* 无发送限制。 
* 如果出现错误，系统将执行三次重试。无法根据收到的错误消息调整重试次数。 
* 内置&#x200B;**反应**&#x200B;事件允许您对开箱即用的操作做出反应（请参阅此[页面](../building-journeys/reaction-events.md)）。 如果要对通过自定义操作发送的消息做出反应，则需要配置专用事件。 
* 无法同时设置两个操作，必须先添加一个，然后再添加另一个操作。

## 历程版本限制 {#journey-versions-limitations}

* v1 中以事件活动开始的历程，在后续版本中无法以事件之外的其他内容开始。您无法通过&#x200B;**受众资格**&#x200B;事件开始历程。
* v1中以&#x200B;**受众资格**&#x200B;活动开始的历程在后续版本中必须始终以&#x200B;**受众资格**&#x200B;开始。
* 无法在新版本中更改在&#x200B;**受众资格** （第一个节点）中选择的受众和命名空间。
* 在所有历程版本中，重新进入规则必须相同。
* 从&#x200B;**读取受众**&#x200B;开始的历程，在后续版本中无法从其他事件开始。

## 自定义操作限制 {#custom-actions-limitations}

* 自定义操作 URL 不支持动态参数。 
* 仅支持POST和PUT调用方法。 
* 查询参数或标头的名称不得以“.”或“$”。 
* 不允许使用IP地址。 
* 不允许使用内部 Adobe 地址 (.adobe.)。

## 事件限制 {#events-limitations}

* 对于系统生成的事件，必须先在Journey Optimizer中配置用于启动客户历程的流数据，才能获取唯一的编排ID。 此编排ID必须附加到传入Adobe Experience Platform的流有效负载中。 此限制不适用于基于规则的事件。

## 数据源限制 {#data-sources-limitations}

* 可在客户历程中利用外部数据源实时查找外部数据。 这些源必须可通过REST API使用，支持JSON，并能够处理大量请求。

## 在创建配置文件的同时开始的历程 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中，创建/更新基于 API 的配置文件存在延迟。延迟方面的服务水平目标 (SLT) 是在每秒请求量 (RPS) 为 20K 的情况下，从摄取到统一配置文件的第 95% 的请求的延迟小于 1 分钟。

如果在创建用户档案的同时触发了历程，并立即检查/检索用户档案服务中的信息，则该事件可能无法正常工作。

您可以从以下两种解决方案中选择一种：

* 在第一个事件后添加等待活动，以便给 Adobe Experience Platform 提供向用户档案服务执行摄取所需的时间。

* 设置不会立即利用用户档案的历程。例如，如果历程旨在确认帐户创建，则体验事件可能包含发送第一条确认消息（名字、姓氏、电子邮件地址等）所需的信息。

## 读取受众限制 {#read-audiences-limitations}

* 流式处理受众始终会保持更新，但在检索时间中不会考虑批量区段。它们每天仅在每日批量评估时间中进行评估。
