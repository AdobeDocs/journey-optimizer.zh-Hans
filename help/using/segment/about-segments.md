---
solution: Journey Optimizer
product: journey optimizer
title: 关于 Adobe Experience Platform 区段
description: 了解如何配置Adobe Experience Platform区段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 6c255d66fb89ba756add062d8a4315dd622fd8e7
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 9%

---

# Adobe Experience Platform区段入门 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="区段"
>abstract="通过利用实时客户配置文件数据，Adobe Experience Platform 让您能够轻松地创建目标区段，用于捕捉客户的独特行为和偏好。"

[!DNL Journey Optimizer]  允许您直接从使用实时客户档案数据创建Adobe Experience Platform区段 **[!UICONTROL 区段]** 菜单，并将其用于您的历程或营销活动。

此外，还可以从分段服务本身创建区段。 了解详情，请参阅 [Adobe Experience Platform分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## 在中使用区段 [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

您可以在中利用区段 **[!DNL Journey Optimizer]** 以不同方式进行：

* 选择一个区段作为 **营销活动的受众**，消息将发送到属于选定区段的所有个人。 [了解如何定义营销活动的受众](../campaigns/create-campaign.md#define-the-audience-audience).

* 使用 **读取区段** 历程中的编排活动，以使区段中的所有个人进入历程并接收历程中包含的消息。

   假设您拥有“白银客户”客户细分。通过此活动，您可以让所有银牌客户进入历程，并向他们发送一系列个性化消息。 [了解如何配置读取区段活动](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* 使用 **区段鉴别** 历程中的事件活动，用于根据Adobe Experience Platform区段入口和出口，使个人进入历程或在此历程中前进。

   例如，您可以让所有新的白银客户进入历程并向他们发送消息。 有关如何使用此活动的更多信息，请参阅 [了解如何配置区段资格活动](../building-journeys/segment-qualification-events.md).

* 使用 **条件** 历程中的活动，以基于区段成员资格构建条件。 [了解如何在条件中使用区段](../building-journeys/condition-activity.md#using-a-segment).

## 受众评估方法{#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer中，受众是通过区段定义使用以下两种评估方法之一生成的：

* **流式客户细分**：当新数据流入系统时，区段的受众列表会实时保持最新。

   流式分段是一个持续的数据选择过程，它会更新区段以响应用户活动。构建并保存区段后，该区段定义将应用于传入Journey Optimizer的数据。 这意味着当个人资料数据发生更改时，即可在区段中添加或删除个人，从而确保您的目标受众始终相关。

* **批量分段**：每24小时评估一次区段的受众列表。

   批量分段是流式分段的替代方法，流式分段通过区段定义一次性处理所有用户档案数据。 这会创建受众的快照，可保存和导出以供使用。 但是，与流式分段不同，批量分段不会连续实时更新受众列表，并且在下一次批量处理之前，批量处理之后输入的新数据不会反映在分段中。”

系统根据分段规则的复杂性和评估成本，对每个分段定义进行批量分段和流式分段的确定。 您可以在中查看每个区段的评估方法 **[!UICONTROL 评估方法]** 段列表的列。

![](assets/evaluation-method.png)

>[!NOTE]
>
>如果 **[!UICONTROL 评估方法]** 列不显示，您需要使用列表右上角的配置按钮添加它。

首次定义区段后，用户档案会在符合条件时添加到受众。

从先前数据回填受众最多可能需要24小时。 回填受众后，受众会持续保持最新状态，并始终准备好进行定位。
