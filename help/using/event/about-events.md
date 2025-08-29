---
solution: Journey Optimizer
product: journey optimizer
title: 使用历程事件
description: 了解如何使用历程中的事件
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 事件，事件，历程，定义，开始
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 461bf985a890d0f2f2723241846df0666248eea0
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 47%

---

# 使用历程事件 {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="历程事件"
>abstract="事件与个人相关联。它与一个人的行为（例如，一个人购买了产品、访问了商店、退出了网站等）或与一个人相关的某件事（例如，一个人达到了 10,000 个忠诚度积分）有关。Journey Optimizer 可监听历程中的单一事件，以编排最佳的后续操作。"

使用事件单独触发历程，在每个用户进入历程时向其交付实时消息。

在事件配置中，您可以配置历程中的预期事件。传入事件的数据按照Adobe体验数据模型(XDM)进行标准化。 事件来自已验证和未验证事件（如 Adobe Mobile SDK 事件）的流摄取 API。您可以使用多个事件（在历程的不同步骤中），而多个历程可以使用同一个事件。

事件配置是&#x200B;**必需的**，必须由数据工程师执行。

您可以配置两种类型的事件： **单一事件**&#x200B;和&#x200B;**商业事件**。


➡️ [通过观看视频了解此功能](#video)

## 单一事件 {#unitary-events}

**单一**&#x200B;事件事件已链接到人员。 它与人员的行为相关（例如，某人购买产品、访问商店、退出网站等）或与人员发生的事情相关（例如，某人达到10,000个忠诚点）。 这是[!DNL Journey Optimizer]在历程中将侦听的内容，以编排最佳的后续行动。 单一事件可以是基于规则的，也可以是系统生成的。 要了解如何创建单一事件，请参阅此[页面](../event/about-creating.md)。

单一历程（以事件或受众资格筛选开始）包含护栏，可防止同一事件多次错误触发历程。默认情况下，会在 5 分钟内暂时阻止用户档案重新进入。例如，如果某个事件在 12:01 触发某个特定轮廓的历程，而另一个事件在 12:03 到达（无论是同一事件还是其他事件触发同一历程），则对于此轮廓，该历程将不会重新开始。

## 业务事件 {#business-events}

**业务**&#x200B;事件未链接到特定配置文件。 例如，它可以是新闻警报、体育更新、航班更改或取消、库存更新、天气事件等。 虽然这些活动不是特定于某个用户档案，但它们可能与任意数量的用户档案有关：订阅特定新闻主题的个人、航班上的乘客、对缺货产品感兴趣的购物者等。 业务事件始终基于规则。 在历程中放置业务活动时，它会在之后自动添加&#x200B;**读取受众**&#x200B;活动。在此页面[上了解如何创建业务活动](../event/about-creating-business.md)。


## 事件ID类型 {#event-id-type}

对于&#x200B;**business**&#x200B;事件，该事件ID类型始终基于规则。

对于&#x200B;**单一**&#x200B;事件，有两种类型的事件ID：

* **基于规则**&#x200B;的事件：此类型的事件不生成 eventID。使用简单表达式编辑器，您只需定义规则即可，系统将使用该规则来识别将触发历程的相关事件。此规则可以基于事件有效负荷中可用的任何字段，例如轮廓的位置或添加到轮廓购物车的项目数。

  >[!CAUTION]
  >
  >为基于规则的事件定义上限规则。它将历程可为给定组织处理的合格事件数限制为每秒5,000个。 它对应于Journey Optimizer SLA。 请参阅您的Journey Optimizer许可和[Journey Optimizer产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html)。

* **系统生成**&#x200B;的事件：这些事件需要 eventID。创建事件时会自动生成此 eventID 字段。推送事件的系统不应生成 ID，它应传递有效负荷预览中可用的 ID。

>[!NOTE]
>
>Journey Optimizer 要求将事件流式传输到数据收集核心服务 (DCCS) 才能触发历程。无法使用批量摄取的事件或来自内部 Journey Optimizer 数据集（消息反馈、电子邮件跟踪等）的事件来触发历程。对于无法获取流式处理事件的用例，请根据这些事件构建一个受众，然后使用&#x200B;**读取受众**&#x200B;活动。从技术上讲，可以使用受众资格，但根据所使用的操作，可能会导致下游挑战。 此数据不一定需要转至实时轮廓。如果要使用事件进行分段，我们建议您为用户档案启用数据集。

## 数据周期 {#data-cycle}

事件是 POST API 调用。事件通过流式引入API发送到Adobe Experience Platform。 通过事务性消息传递API发送的事件的URL目标称为“入口”。 事件的有效负载遵循 XDM 格式。

有效负载包含流式引入API工作所需的信息（在标题中）和[!DNL Journey Optimizer]工作所需的信息以及要在旅程中使用的信息（在正文中，例如放弃购物车的数量）。 流式引入有两种模式，即验证和未验证。有关流式引入 API 的详细信息，请参阅[此链接](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hans){target="_blank"}。

事件通过流式引入API到达后，会流入名为Pipeline的内部服务，然后流入Adobe Experience Platform。 如果事件架构启用了实时客户轮廓服务标志，并且数据集 ID 也具有实时客户轮廓标志，则会流入实时客户轮廓服务。

对于系统生成的事件，Pipeline会筛选有效负载由[!DNL Journey Optimizer]提供并包含在事件有效负载中的事件，这些有效负载包含[!DNL Journey Optimizer]个事件ID（请参阅下面的事件创建流程）。 对于基于规则的事件，系统会使用eventID条件标识事件。 这些事件通过 [!DNL Journey Optimizer] 侦听，并触发相应的旅程。

## 更新和删除事件 {#update-event}


为避免破坏现有历程，在编辑草稿、实时或已关闭历程中使用的事件时，只能更改名称、描述或添加有效负载字段。

无法删除实时、草稿或已关闭历程中使用的任何事件。 要删除已使用的事件，您必须停止使用该事件的历程，和/或将其从使用它的草稿历程中删除。 您可以检查&#x200B;**[!UICONTROL 在]**&#x200B;中使用的字段。 它会显示使用该特定事件的历程数。 您可以单击&#x200B;**[!UICONTROL 查看历程]**&#x200B;按钮以显示相应历程的列表。

## 操作说明视频 {#video}

了解如何配置事件、指定流媒体端点和事件的有效负载。

>[!VIDEO](https://video.tv.adobe.com/v/3431516?quality=12&captions=chi_hans)

了解商业事件的适用用例。 了解如何使用商业事件构建历程以及可以应用的最佳实践。

>[!VIDEO](https://video.tv.adobe.com/v/3416324?quality=12&captions=chi_hans)
