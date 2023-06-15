---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 护栏和限制
description: 详细了解 Journey Optimizer 护栏
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 70db4a6c235b8490fb80e24d133775f5f5a19eb1
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 99%

---

# 护栏和限制 {#limitations}

[Adobe Journey Optimizer 产品说明页面](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}列出了授权、产品限制和性能护栏。

您还需要[在开始之前了解针对 Real-time Customer Profile 数据的防护](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=zh-Hans){target="_blank"}。

下文中介绍了使用 [!DNL Adobe Journey Optimizer] 时的额外护栏和限制。

## 支持的浏览器 {#browsers}

Adobe [!DNL Journey Optimizer] 界面设计为可在最新版 Google Chrome 中发挥最佳表现。在旧版本或其他浏览器上使用某些功能时可能会遇到问题。

## 消息护栏 {#message-guardrails}

* 无法使用 [!DNL Journey Optimizer] 向电子邮件添加附件。
* 无法使用相同的发送域从 [!DNL Adobe Journey Optimizer] 和其他产品（例如 [!DNL Adobe Campaign] 或 [!DNL Adobe Marketo Engage]）发送消息。


## 登陆页面护栏 {#lp-guardrails}

* 在单个主页面中只能使用一个&#x200B;**表单**&#x200B;组件。
* 无法在子页面中使用&#x200B;**表单**&#x200B;组件。
* 无法向登陆页添加预编译标头。
* 设计主登录页面时，无法选择&#x200B;**自己编写代码**&#x200B;选项。

## 历程护栏 {#journeys-guardrails}

### 一般历程护栏 {#journeys-guardrails-journeys}

* 历程中的活动数量限制为 50 个。活动数显示在历程画布的左上角部分。这有助于提高可读性、QA和疑难解答。

### 常规操作 {#general-actions-g}

* 无发送限制。
* 如果出现错误，系统将执行三次重试。无法根据收到的错误消息调整重试次数。
* 使用内置的&#x200B;**反应**&#x200B;事件，可对开箱即用的操作做出反应。 请参阅[此页面](../building-journeys/reaction-events.md)以了解详情。如果要对通过自定义操作发送的消息做出反应，则需要配置专用事件。
* 无法同时设置两个操作，必须先添加一个，然后再添加另一个操作。
* 通常，同一历程中无法同时存在多个用户档案。如果启用了重新进入，则用户档案可以重新进入历程，但只有在完全退出该历程的上一个实例后才能重新进入历程。[了解详情](../building-journeys/end-journey.md)

### 历程版本 {#journey-versions-g}

* v1 中以事件活动开始的历程，在后续版本中无法以事件之外的其他内容开始。无法以&#x200B;**区段资格**&#x200B;事件开始历程。
* v1 中以&#x200B;**区段资格**&#x200B;活动开始的历程在后续版本中必须始终以&#x200B;**区段资格**&#x200B;开始。
* 无法在新版本中更改在&#x200B;**区段鉴别** （第一个节点）中选择的区段和命名空间。
* 在所有历程版本中，重新进入规则必须相同。
* 以&#x200B;**读取区段**&#x200B;开始的历程，在后续版本中无法以其他事件开头。
* 您无法创建具有增量读取的读取区段历程的新版本。您需要复制历程。

### 自定义操作 {#custom-actions-g}

* 自定义操作 URL 不支持动态参数。
* 仅支持 POST 和 PUT 调用方法
* 查询参数或标头的名称不得以“.”或“$”开始
* 不允许使用 IP 地址
* URL 和 API 不支持 Adobe 内部地址 (`.adobe.*`)。
* 无法移除内置的自定义操作。

### 事件 {#events-g}

* 对于系统生成的事件，必须先在 Journey Optimizer 中配置用于启动客户历程的流数据，才能获取唯一的编排 ID。此编排 ID 必须附加到传入 Adobe Experience Platform 的流有效负载中。此限制不适用于基于规则的事件。
* 业务事件无法与单一事件或区段资格活动结合使用。
* 单一历程（以事件或区段资格开始）包含护栏，可防止同一事件多次错误触发历程。默认情况下，重新访问用户档案会被暂时阻止 5 分钟。例如，如果某个事件在 12:01 触发某个特定用户档案的历程，而另一个事件在 12:03 到达（无论是同一事件还是其他事件触发同一历程），则对于此用户档案，该历程将不会重新开始。
* Journey Optimizer 要求将事件流式传输到数据收集核心服务 (DCCS) 才能触发历程。批量摄取的事件或来自内部 Journey Optimizer 数据集（消息反馈、电子邮件跟踪等）的事件无法用于触发历程。对于无法获取流式传输的事件的用例，请基于这些事件构建一个区段，然后改用&#x200B;**读取区段**&#x200B;活动。从技术上讲，可以使用区段鉴别，但根据所使用的操作，可能会导致下游挑战。

### 数据源 {#data-sources-g}

* 可在客户历程中利用外部数据源，以实时查找外部数据。这些源必须可通过 REST API 使用，支持 JSON，并能够处理大量请求。
* URL 和 API 不支持 Adobe 内部地址 (`.adobe.*`)。

### 历程和用户档案创建 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中，创建/更新基于 API 的配置文件存在延迟。延迟方面的服务水平目标 (SLT) 是在每秒请求量 (RPS) 为 20K 的情况下，从摄取到统一配置文件的第 95% 的请求的延迟小于 1 分钟。

如果在创建用户档案的同时触发了历程，并立即检查/检索用户档案服务中的信息，则该历程可能无法正常工作。

您可以从以下两种解决方案中选择一种：

* 在第一个事件后添加等待活动，以便给 Adobe Experience Platform 提供向用户档案服务执行摄取所需的时间。

* 设置不会立即利用用户档案的历程。例如，如果历程旨在确认帐户创建，则体验事件可能包含发送第一条确认消息（名字、姓氏、电子邮件地址等）所需的信息。

### 读取区段 {#read-segment-g}

* 流式处理区段始终是最新的，但在检索时间中不会计算批处理区段。它们每天仅在每日批量评估时间中进行评估。
* 对于使用“读取区段”活动的历程，可以同时启动的历程数具有上限。系统将重试，但请不要同时启动超过 5 个历程（读取区段、预定或“尽快”开始），可以将它们分散到不同的时间，例如间隔 5 到 10 分钟。

### 表达式编辑器 {#expression-editor}

* 以读取区段、区段鉴别或业务事件活动开始的历程中，无法使用体验事件字段组。您需要创建新区段并在历程中使用段内条件。


