---
solution: Journey Optimizer
product: journey optimizer
title: 历程限制
description: 进一步了解历程限制
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# 限制 {#journey-limitations}

以下是与历程使用相关的限制。

## 一般操作限制

* 没有发送限制。 
* 系统会在发生错误时执行三次重试。 您无法根据收到的错误消息调整重试次数。 
* 内置 **反应** 事件允许您对即装即用的操作做出反应(请参阅 [页面](../building-journeys/reaction-events.md))。 如果要对通过自定义操作发送的消息做出响应，则需要配置专用事件。 
* 不能并行放置两个操作，必须先添加一个，然后再添加另一个操作。

## 历程版本限制 {#journey-versions-limitations}

* 从v1中的事件活动开始的历程不能以其他版本中的事件以外的内容开头。 您不能使用 **区段鉴别** 事件。
* 历程从 **区段鉴别** v1中的活动必须始终以 **区段鉴别** 中。
* 中选择的区段和命名空间 **区段鉴别** （第一个节点）在新版本中无法更改。
* 在所有历程版本中，重新进入规则必须相同。
* 历程从 **读取区段** 在后续版本中，无法以其他事件开头。
 

## 自定义操作限制

* 自定义操作URL不支持动态参数。 
* 仅支持POST和PUT调用方法。 
* 查询参数或标头的名称不得以“。”开头 或“$”。 
* 不允许使用IP地址。 
* 内部Adobe地址(.adobe.) 不允许。
 

## 事件限制

* 对于系统生成的事件，必须先在Journey Optimizer中配置用于启动客户旅程的流数据，才能获取唯一的编排ID。 此编排ID必须附加到传入Adobe Experience Platform的流有效负载中。 此限制不适用于基于规则的事件。
 

## 数据源限制

* 可以在客户历程中利用外部数据源来实时查找外部数据。 这些源必须通过REST API可用，支持JSON并能够处理请求量。

## 从创建用户档案的同时开始的历程 {#journeys-limitation-profile-creation}

在Adobe Experience Platform中，基于API的配置文件创建/更新存在延迟。 延迟方面的服务级别目标(SLT)从摄取到统一配置文件（针对第95个百分位数的请求）在每秒20K请求(RPS)的量下小于1分钟。

如果历程同时触发到用户档案创建，并立即检查/检索用户档案服务中的信息，则该历程可能无法正常工作。

您可以从以下两种解决方案之一进行选择：

* 在第一个事件后添加等待活动，以便Adobe Experience Platform获得执行向用户档案服务摄取所需的时间。

* 设置不会立即利用用户档案的历程。 例如，如果历程设计为确认帐户创建，则体验事件可能包含发送第一条确认消息（名字、姓氏、电子邮件地址等）所需的信息。

## 读取区段限制

* 流式处理区段始终是最新的，但在检索时不会计算批处理区段。 它们仅在每日批量评估时间每天进行评估。
