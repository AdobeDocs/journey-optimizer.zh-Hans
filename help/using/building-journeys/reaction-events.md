---
solution: Journey Optimizer
product: journey optimizer
title: 反应事件
description: 了解如何使用反应事件响应消息跟踪数据（如历程中的打开数和点击数），并为无反应者配置超时路径。
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 历程，事件，反应，跟踪，平台
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/6myO49j2-TgkX0-diC8JDePxvMBPjZGnMYdxO466cP4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: e57d1da4-32c2-4cc6-945c-9feb219156ff
  - id: ebd64fe4-362a-4a1c-9476-b2573ed12a95
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 541
ht-degree: 14%

---

# 反应事件 {#reaction-events}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何使用反应活动响应消息跟踪数据（如同一历程中的打开数和点击数），并为未参与的个人配置超时路径。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="反应事件"
>abstract="您可以通过此活动，对在同一历程中与所发送消息相关的跟踪数据做出反应。 我们在与 [!DNL Adobe Experience Platform] 共享时实时捕获此信息。"

## 概述 {#overview}

在面板中可用的不同事件活动中，您会找到内置的&#x200B;**[!UICONTROL 反应]**&#x200B;事件。 您可以通过此活动，对在同一历程中与所发送消息相关的跟踪数据做出反应。 我们在与 [!DNL Adobe Experience Platform] 共享时实时捕获此信息。

您可以对单击或打开的消息做出反应。 例如，如果某人打开了之前的电子邮件或单击了其中的内容，则您可以发送另一封邮件；如果某人未参与您的通信，则您可以发送另一封后续邮件。

查看[操作活动](../building-journeys/about-journey-activities.md#action-activities)。

如果没有对您的消息做出反应，您可以使用&#x200B;**[!UICONTROL 反应]**&#x200B;活动执行操作。 为此，请创建与&#x200B;**[!UICONTROL 反应]**&#x200B;活动平行的第二个路径，并添加&#x200B;**[!UICONTROL 等待]**&#x200B;活动。 如果在&#x200B;**[!UICONTROL 等待]**&#x200B;活动中定义的时段内没有反应，将选择第二个路径。 例如，您可以选择发送跟进消息。

## 如何配置反应事件 {#configure}

![具有渠道选择和事件类型选项的反应事件配置](assets/journey45.png)

按照以下步骤配置反应事件：

1. 将&#x200B;**[!UICONTROL 反应]**&#x200B;活动&#x200B;**立即**&#x200B;放置在历程画布上的[渠道操作活动](journey-action.md)之后。
1. 向反应添加&#x200B;**[!UICONTROL 标签]**。 此步骤是可选的。
1. 从下拉列表中，选择要做出反应的操作活动。 您可以选择位于路径前面步骤中的任何操作活动。
1. 根据您选择的操作，选择要做出反应的内容。
1. 您可以定义事件超时（40秒到90天之间）和超时路径。 这会为未在定义的持续时间内做出反应的个人创建第二个路径。 测试使用反应事件的历程时，测试模式&#x200B;**[!UICONTROL 等待时间]**&#x200B;的默认值和最小值为40秒。 请参阅[此小节](../building-journeys/testing-the-journey.md)。

## 护栏和限制 {#guardrails-limitations}

* 必须在历程画布中的[渠道操作活动](journey-action.md)之后&#x200B;**立即**&#x200B;放置&#x200B;**[!UICONTROL 反应]**&#x200B;活动。
* 如果之前没有渠道操作活动，则不能使用&#x200B;**[!UICONTROL 反应]**&#x200B;活动。
* 不支持在渠道操作与&#x200B;**[!UICONTROL 反应]**&#x200B;活动之间放置&#x200B;**[!UICONTROL 等待]**&#x200B;活动或任何其他活动，这可能会导致反应无法按预期运行。
* 反应事件只能跟踪在同一历程中发送的消息。 它们无法跟踪在其他历程中发生的消息。
* 反应事件跟踪“已跟踪”类型链接的点击次数。 未考虑退订和镜像页面链接。
* 使用电子邮件中包含的0像素图像跟踪电子邮件打开次数。 如果电子邮件客户端（如Gmail）阻止图像，则不会考虑电子邮件打开次数。
