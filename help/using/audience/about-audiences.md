---
solution: Journey Optimizer
product: journey optimizer
title: 关于 Adobe Experience Platform 受众
description: 了解如何使用 Adobe Experience Platform 受众
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 100%

---

# Adobe Experience Platform 受众入门指南 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="受众"
>abstract="通过利用 Real-Time Customer Profile 数据，Adobe Experience Platform 让您能够轻松地构建区段定义，从而创建目标受众，用于捕捉客户的独特行为和偏好。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="选择营销活动受众"
>abstract="此列表显示所有可用的 Adobe Experience Platform 受众。选择营销活动的目标受众。营销活动中配置的消息将发送到属于所选受众的所有个人。[详细了解受众](../audience/about-audiences.md)。"

[!DNL Journey Optimizer]允许您使用 Real-Time Customer Profile 数据直接从&#x200B;**[!UICONTROL 受众]**&#x200B;菜单构建并利用 Adobe Experience Platform 受众，并将其用于历程或活动。

请参阅 [Adobe Experience Platform 分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hans)以了解详情。

## 在 [!DNL Journey Optimizer] 中使用受众 {#segments-in-journey-optimizer}

您可通过不同方式在 **[!DNL Journey Optimizer]** 中利用受众：

* 为&#x200B;**营销活动**&#x200B;选择受众，消息将发送给属于所选受众的所有个人。[了解如何定义营销活动的受众](../campaigns/create-campaign.md#define-the-audience-audience)。

* 在历程中使用&#x200B;**读取受众**&#x200B;编排活动，使受众中的所有个人进入历程并接收历程中包含的消息。

  假设您拥有“白银客户”受众。通过此活动，您可以使所有白银客户进入历程，并向其发送一系列个性化消息。[了解如何配置读取受众活动](../building-journeys/read-audience.md#configuring-segment-trigger-activity)。

* 在历程中使用&#x200B;**受众鉴别**&#x200B;事件活动，根据 Adobe Experience Platform 受众进出条件，在历程中添加个人或让个人继续留在该历程中。

  例如，您可以让所有新的白银客户进入历程并向其发送消息。有关如何使用此活动的更多信息，请参阅[了解如何配置受众鉴别活动](../building-journeys/audience-qualification-events.md)。

* 使用历程中的&#x200B;**条件**&#x200B;活动，根据受众成员资格构建条件。[了解如何在条件中使用受众](../building-journeys/condition-activity.md#using-a-segment)。

## 受众评估方法{#evaluation-method-in-journey-optimizer}

在 Adobe Journey Optimizer 中，受众是使用以下两种评估方法之一通过区段定义生成的：

* **流式分段**：当新数据流入系统时，受众的用户档案列表会保持实时更新。

  流式分段是一个持续的数据选择过程，会更新区段以响应用户活动。构建区段定义并保存生成的受众后，该区段定义将应用于传入 Journey Optimizer 的数据。这意味着当个人的用户档案数据发生更改时，将会在受众中添加或删除个人，从而确保您的目标受众始终相关。

* **批量分段**：每 24 小时评估一次受众的用户档案列表。

  批量分段是流式分段的替代方法，是通过区段定义一次性处理所有用户档案数据的过程。这会创建受众的快照，可保存和导出以供使用。但是，与流式分段不同，批量分段不会连续实时更新受众列表，并且在下一次批量处理之前，上一次批量处理之后输入的新数据不会体现在受众中。”

系统根据分段定义规则的复杂性和评估成本，确定为每个受众进行批量分段或流式分段。您可以在受众列表的&#x200B;**[!UICONTROL 评估方法]**&#x200B;列中查看每个受众的评估方法。

![](assets/evaluation-method.png)

>[!NOTE]
>
>如果&#x200B;**[!UICONTROL 评估方法]**&#x200B;列没有显示，您需要使用列表右上角的配置按钮进行添加。

首次定义受众后，在符合条件时，用户档案会被添加到受众。

从先前数据回填受众最多可能需要 24 小时。回填受众后，受众会持续保持最新状态，并始终准备好用于定位。
