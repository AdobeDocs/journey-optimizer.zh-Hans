---
solution: Journey Optimizer
product: journey optimizer
title: 关于事件
description: 了解事件
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: 事件，事件，历程，定义，开始
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 56%

---

# 关于事件{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="关于事件"
>abstract="事件与个人相关联。它与个人的行为有关（例如，某人购买了产品、访问了商店、退出了网站等）或者与个人相关的某件事情有关（例如，某人达到 10 000 个忠诚点）。这就是 Journey Optimizer 在历程中将侦听的内容，以编排最佳的后续行动。"

事件配置允许您定义 [!DNL Journey Optimizer] 将作为事件接收的信息。您可以使用多个事件（在历程的不同步骤中），而多个历程可以使用相同的事件。

>[!CAUTION]
>
>事件配置为 **必需** 并且必须由 **数据工程师**.

您可以配置两种类型的事件：

* **单一** 事件：这些事件链接到人员。 它与人员的行为相关（例如，某人购买产品、访问商店、退出网站等） 或者与个人相关的某件事情有关（例如，某人达到 10 000 个忠诚点）。这就是 [!DNL Journey Optimizer] 在历程中将侦听的内容，以编排最佳的后续行动。单一事件可以是基于规则的，也可以是系统生成的。 要了解如何创建单一事件，请参阅此 [页面](../event/about-creating.md).

* **商业** 事件：与单一事件相反，商业事件是指不链接到特定用户档案的事件。 例如，可以是新闻警报、体育更新、航班更改或取消、库存更新、天气事件等。 虽然这些活动不是特定于某个用户档案，但它们可能与任意数量的用户档案有关：订阅特定新闻主题的个人、航班上的乘客、对缺货产品感兴趣的购物者等。 业务事件始终基于规则。 在历程中放置业务事件时，会自动添加 **读取受众** 活动之后。 要了解如何创建业务事件，请参阅此 [页面](../event/about-creating-business.md).


>[!NOTE]
>
>如果您编辑在草稿或实时历程中使用的事件，则只能更改名称、描述或添加有效负载字段。我们严格限制草稿或实时历程的版本，以避免中断历程。

单一历程（从事件或受众资格开始）包含护栏，可防止同一事件多次错误触发历程。 默认情况下，重新访问用户档案会被暂时阻止 5 分钟。例如，如果某个事件在 12:01 触发某个特定用户档案的历程，而另一个事件在 12:03 到达（无论是同一事件还是其他事件触发同一历程），则对于此用户档案，该历程将不会重新开始。

➡️ [在视频中发现此功能](#video)

## 事件ID类型{#event-id-type}

对于业务事件，事件ID类型始终基于规则。

对于单一事件，有两种类型的事件ID：

* **基于规则**&#x200B;的事件：此类型的事件不生成 eventID。使用简单表达式编辑器，您只需定义规则即可，系统将使用该规则来识别将触发历程的相关事件。此规则可以基于事件有效负荷中可用的任何字段，例如用户档案的位置或添加到用户档案购物车的项目数。

  >[!CAUTION]
  >
  >为基于规则的事件定义上限规则。它将历程可为给定组织处理的合格事件数限制为每秒5000个。 它对应于Journey Optimizer SLA。 请参阅您的Journey Optimizer许可和 [Journey Optimizer产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html).

* **系统生成**&#x200B;的事件：这些事件需要 eventID。创建事件时会自动生成此 eventID 字段。推送事件的系统不应生成 ID，它应传递有效负荷预览中可用的 ID。

>[!NOTE]
>
>Journey Optimizer 要求将事件流式传输到数据收集核心服务 (DCCS) 才能触发历程。批量摄取的事件或来自内部 Journey Optimizer 数据集（消息反馈、电子邮件跟踪等）的事件无法用于触发历程。对于无法获取流式传输的事件的用例，请基于这些事件构建受众并使用 **读取受众** 活动。 从技术上讲，可以使用受众资格，但根据所使用的操作，可能会导致下游挑战。 此数据不一定需要转至实时用户档案。如果要在单独的历程中使用事件进行分段或查找，我们建议您为用户档案启用数据集。

## 数据周期 {#data-cycle}

事件是 POST API 调用。事件通过流式引入API发送到Adobe Experience Platform。 通过事务性消息传送 API 发送的事件的 URL 目标称为“入口”。事件的有效负载遵循 XDM 格式。

有效负载包含流式引入API工作所需的信息（在标头中）和所需的信息 [!DNL Journey Optimizer] 工作以及在旅程中使用的信息（在正文中，例如放弃购物车的金额）。 流式引入有两种模式，即验证和未验证。有关流式引入 API 的详细信息，请参阅[此链接](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hans)。

事件通过流式引入API到达后，会流入名为Pipeline的内部服务，然后流入Adobe Experience Platform。 如果事件架构启用了实时客户资料服务标志，并且数据集 ID 也具有实时客户资料标志，则会流入实时客户资料服务。

对于系统生成的事件，Pipeline会筛选有效负载包含以下内容的事件 [!DNL Journey Optimizer] eventIDs（请参阅下面的事件创建流程）由提供 [!DNL Journey Optimizer] 并包含在事件有效负载中。 对于基于规则的事件，系统会使用eventID条件标识事件。 这些事件通过 [!DNL Journey Optimizer] 侦听，并触发相应的旅程。

## 操作说明视频 {#video}

了解如何配置事件、指定流媒体端点和事件的有效负载。

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

了解商业事件的适用用例。 了解如何使用商业事件构建历程以及可以应用的最佳实践。

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
