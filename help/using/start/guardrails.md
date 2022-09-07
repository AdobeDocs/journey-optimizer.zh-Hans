---
title: Journey Optimizer护栏和限制
description: 进一步了解Journey Optimizer护栏
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 4%

---

# 护栏和限制 {#limitations}

授权、产品限制和性能护栏列在 [Adobe Journey Optimizer产品描述页面](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}。

下文中介绍了使用 [!DNL Adobe Journey Optimizer] 时的额外护栏和限制。

## 消息护栏 {#message-guardrails}

* 您无法向使用 [!DNL Journey Optimizer].
* 您不能使用相同的发送域从 [!DNL Adobe Journey Optimizer] 和来自其他产品，例如 [!DNL Adobe Campaign] 或 [!DNL Adobe Marketo Engage] 例如。


## 决策管理护栏 {#offer-guardrails}

决策的性能护栏和静态限制列在 [AdobeOffer decisioning应用程序服务产品说明页面](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}。


## 登陆页面护栏 {#lp-guardrails}

* 只有一个 **表单** 组件可在单个主页面中使用。
* 的 **表单** 组件不能在子页面中使用。
* 您无法向登陆页面添加预标头。
* 您无法选择 **编码您自己的** 选项。

## 历程护栏 {#journeys-guardrails}

### 常规操作 {#general-actions-g}

* 没有发送限制。
* 系统会在发生错误时执行三次重试。 您无法根据收到的错误消息调整重试次数。
* 内置 **反应** 事件允许您对即装即用的操作做出响应。 请参阅[此页面](../building-journeys/reaction-events.md)以了解详情。如果要对通过自定义操作发送的消息做出响应，则需要配置专用事件。
* 不能并行放置两个操作，必须先添加一个，然后再添加另一个操作。
* 今天的历程存在技术限制，致使用户档案无法在同一历程中同时出现多次。 用户档案仍可以重新进入旅程（基于设置），但只有在完全退出该历程的上一个实例后才能重新进入该历程。
* 在大多数情况下，同一历程中不能同时存在多个用户档案。 如果启用了重新进入，则用户档案可以重新进入历程，但只有在完全退出该历程的上一个实例后才能重新进入历程。 [了解详情](../building-journeys/journey-end.md)

### 历程版本 {#journey-versions-g}

* 从v1中的事件活动开始的历程不能以其他版本中的事件以外的内容开头。 您不能使用 **区段鉴别** 事件。
* 历程从 **区段鉴别** v1中的活动必须始终以 **区段鉴别** 中。
* 中选择的区段和命名空间 **区段鉴别** （第一个节点）在新版本中无法更改。
* 在所有历程版本中，重新进入规则必须相同。
* 历程从 **读取区段** 在后续版本中，无法以其他事件开头。

### 自定义操作 {#custom-actions-g}

* 自定义操作URL不支持动态参数。
* 仅支持POST和PUT调用方法
* 查询参数或标头的名称不得以“。”开头 或 &quot;$&quot;
* 不允许使用IP地址
* 内部Adobe地址(.adobe.) 不允许。

### 活动 {#events-g}

* 对于系统生成的事件，必须先在Journey Optimizer中配置用于启动客户旅程的流数据，才能获取唯一的编排ID。 此编排ID必须附加到传入Adobe Experience Platform的流有效负载中。 此限制不适用于基于规则的事件。
* 业务事件不能与单一事件或区段鉴别活动结合使用。

### 数据源 {#data-sources-g}

* 可以在客户历程中利用外部数据源，以实时查找外部数据。 这些源必须通过REST API可用，支持JSON并能够处理请求量。

### 历程和用户档案创建 {#journeys-limitation-profile-creation}

在Adobe Experience Platform中，创建/更新基于API的配置文件会存在延迟。 延迟方面的服务级别目标(SLT)从摄取到统一配置文件（针对第95个百分位数的请求）在每秒20K请求(RPS)的量下小于1分钟。

如果历程同时触发到用户档案创建，并立即检查/检索用户档案服务中的信息，则该历程可能无法正常工作。

您可以从以下两种解决方案之一进行选择：

* 在第一个事件后添加等待活动，为Adobe Experience Platform提供执行向用户档案服务摄取所需的时间。

* 设置不会立即利用用户档案的历程。 例如，如果历程设计为确认帐户创建，则体验事件可能包含发送第一条确认消息（名字、姓氏、电子邮件地址等）所需的信息。

### 阅读区段 {#read-segment-g}

* 流式处理区段始终是最新的，但在检索时不会计算批处理区段。 它们仅在每日批量评估时间每天进行评估。
* 对于使用读取区段活动的历程，可以同时启动的历程数上限。 重试将由系统执行，但请通过将重试分隔5到10分钟，避免从同一时间开始的历程（具有读取区段、计划或“尽快”启动）。
