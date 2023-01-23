---
solution: Journey Optimizer
product: journey optimizer
title: 历程限制
description: 进一步了解历程限制
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 历程、限制
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 60%

---

# 限制 {#journey-limitations}

以下是与历程使用相关的限制。

## 一般操作限制

* 无发送限制。 
* 如果出现错误，系统将执行三次重试。无法根据收到的错误消息调整重试次数。 
* 内置 **反应** 事件允许您对即装即用的操作做出反应(请参阅 [页面](../building-journeys/reaction-events.md))。 如果要对通过自定义操作发送的消息做出响应，则需要配置专用事件。 
* 无法同时设置两个操作，必须先添加一个，然后再添加另一个操作。

## 历程版本限制 {#journey-versions-limitations}

* v1 中以事件活动开始的历程，在后续版本中无法以事件之外的其他内容开始。无法以&#x200B;**区段资格**&#x200B;事件开始历程。
* v1 中以&#x200B;**区段资格**&#x200B;活动开始的历程在后续版本中必须始终以&#x200B;**区段资格**&#x200B;开始。
* 中选择的区段和命名空间 **区段鉴别** （第一个节点）在新版本中无法更改。
* 在所有历程版本中，重新进入规则必须相同。
* 以&#x200B;**读取区段**开始的历程，在后续版本中无法以其他事件开头。
 

## 自定义操作限制

* 自定义操作 URL 不支持动态参数。 
* 仅支持 POST 和 PUT 调用方法. 
* 查询参数或标头的名称不得以“.”或“$”开始。 
* 不允许使用 IP 地址. 
* 不允许使用内部 Adobe 地址 (.adobe.)。 

## 事件限制

* 对于系统生成的事件，必须先在 Journey Optimizer 中配置用于启动客户历程的流数据，才能获取唯一的编排 ID。 此编排ID必须附加到传入Adobe Experience Platform的流有效负载中。 此限制不适用于基于规则的事件。 

## 数据源限制

* 可以在客户历程中利用外部数据源来实时查找外部数据。 这些源必须通过REST API可用，支持JSON并能够处理请求量。

## 历程从创建用户档案的同时开始 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中，创建/更新基于 API 的配置文件存在延迟。延迟方面的服务水平目标 (SLT) 是在每秒请求量 (RPS) 为 20K 的情况下，从摄取到统一配置文件的第 95% 的请求的延迟小于 1 分钟。

如果历程同时触发到配置文件创建，并立即检查/检索配置文件服务中的信息，则它可能无法正常工作。

您可以从以下两种解决方案中选择一种：

* 在第一个事件后添加等待活动，以便给 Adobe Experience Platform 提供向用户档案服务执行摄取所需的时间。

* 设置不会立即利用用户档案的历程。例如，如果历程设计为确认帐户创建，则体验事件可能包含发送第一条确认消息（名字、姓氏、电子邮件地址等）所需的信息。

## 读取区段限制

* 流式处理区段始终是最新的，但在检索时间中不会计算批处理区段。它们每天仅在每日批量评估时间中进行评估。
