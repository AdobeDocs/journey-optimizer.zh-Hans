---
title: 关于事件
description: 了解事件
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 51%

---

# 关于事件{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="关于事件"
>abstract="事件与个人相关联。它与个人的行为有关（例如，某人购买了产品、访问了商店、退出了网站等）或者与个人相关的某件事情有关（例如，某人达到 10 000 个忠诚点）。这就是Journey Optimizer在历程中将侦听的内容，以编排最佳的后续行动。"

事件配置允许您定义 [!DNL Journey Optimizer] 将作为事件接收的信息。您可以使用多个事件（在历程的不同步骤中），而多个历程可以使用相同的事件。

>[!CAUTION]
>
>事件配置为 **强制** 且必须由 **数据工程师**.

您可以配置两种类型的事件：

* **单一** 事件：这些事件与人员相关联。 它们与个人的行为相关（例如，某人购买了产品、访问了商店、退出了网站等） 或者与个人相关的某件事情有关（例如，某人达到 10 000 个忠诚点）。这就是 [!DNL Journey Optimizer] 在历程中将侦听的内容，以编排最佳的后续行动。统一事件可以是基于规则的事件，也可以是系统生成的事件。 要了解如何创建统一事件，请参阅 [页面](../event/about-creating.md).

* **商业** 事件：与单一事件不同，业务事件是指未与特定用户档案关联的事件。 例如，它可以是新闻警报、体育更新、航班更改或取消、库存更新、天气事件等。 虽然这些事件并非特定于用户档案，但可能与任意数量的用户档案有关：订阅特定新闻主题的个人、航班上的乘客、对缺货产品感兴趣的购物者等。 业务事件始终基于规则。 当您在历程中放置业务事件时，它会自动添加 **读取区段** 活动之后。 要了解如何创建业务事件，请参阅 [页面](../event/about-creating-business.md).


>[!NOTE]
>
>如果您编辑在草稿或实时历程中使用的事件，则只能更改名称、描述或添加有效负载字段。我们严格限制草稿或实时历程的版本，以避免中断历程。

➡️ [在视频中发现此功能](#video)

## 事件ID类型{#event-id-type}

对于业务事件，事件ID类型始终基于规则。

对于单一事件，事件ID有两种类型：

* **基于规则**&#x200B;的事件：此类型的事件不生成 eventID。使用简单表达式编辑器，您只需定义规则即可，系统将使用该规则来识别将触发历程的相关事件。此规则可以基于事件有效负荷中可用的任何字段，例如用户档案的位置或添加到用户档案购物车的项目数。

   >[!CAUTION]
   >
   >为基于规则的事件定义上限规则。它将历程可为给定组织处理的符合条件的事件数限制为每秒5000个。 它对应于Journey Optimizer SLA。 请参阅您的Journey Optimizer许可和 [Journey Optimizer产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html).

* **系统生成**&#x200B;的事件：这些事件需要 eventID。创建事件时会自动生成此 eventID 字段。推送事件的系统不应生成 ID，它应传递有效负荷预览中可用的 ID。

Journey Optimizer要求将事件流式传输或批量传输到Adobe Experience Platform。 此数据不一定需要转至实时用户档案。如果要在单独的历程中使用事件进行分段或查找，我们建议您为用户档案启用数据集。

## 数据周期 {#data-cycle}

事件是 POST API 调用。事件通过流摄取API发送到Adobe Experience Platform。 通过事务性消息传送 API 发送的事件的 URL 目标称为“入口”。事件的有效负载遵循 XDM 格式。

有效负载包含流式引入API工作所需的信息（在标头中）和 [!DNL Journey Optimizer] 工作和要在旅程中使用的信息（在主体中，例如放弃购物车的数量）。 流式引入有两种模式，即验证和未验证。有关流式引入 API 的详细信息，请参阅[此链接](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hans)。

事件通过流式引入API到达后，将流入名为Pipeline的内部服务，然后流入Adobe Experience Platform。 如果事件架构启用了实时客户资料服务标志，并且数据集 ID 也具有实时客户资料标志，则会流入实时客户资料服务。

对于系统生成的事件，Pipeline过滤器事件的有效负载包含 [!DNL Journey Optimizer] eventID（请参阅下面的事件创建过程），由 [!DNL Journey Optimizer] 和包含在事件有效负载中。 对于基于规则的事件，系统会使用eventID条件来标识该事件。 这些事件通过 [!DNL Journey Optimizer] 侦听，并触发相应的旅程。

## 操作说明视频 {#video}

了解如何配置事件、指定流媒体端点和事件的有效负载。

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

了解商业事件的适用用例。 了解如何使用商业事件构建历程以及可以应用的最佳实践。

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
