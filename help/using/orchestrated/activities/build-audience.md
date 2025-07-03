---
solution: Journey Optimizer
product: journey optimizer
title: 使用构建受众活动
description: 了解如何在编排的活动中使用构建受众活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 34%

---

# 构建受众 {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="生成受众活动"
>abstract="您可以使用&#x200B;**生成受众**&#x200B;活动，定义将进入协同营销活动的受众。在协同营销活动的上下文中发送消息时，消息受众不是在渠道活动中定义的，而是在&#x200B;**构建受众**&#x200B;活动中定义的。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[访问和管理协调的营销活动](../access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](../gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](../create-orchestrated-campaign.md)<br/><br/>[编排活动](../orchestrate-activities.md)<br/><br/>[启动和监控营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用规则生成器](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md)<br/><br/>[重新定位](../retarget.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[并加入](and-join.md) - <b>[生成受众](build-audience.md)</b> - [更改维度](change-dimension.md) - [渠道活动](channels.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [保存受众](save-audience.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

作为营销人员，您可以通过直观的界面创建复杂的受众区段，从而根据各种标准和行为来定位用户，从而更有效地定制营销活动。

为此，请使用&#x200B;**[!UICONTROL 构建受众]**&#x200B;定位活动。 此活动定义进入编排营销活动的受众。 在协调的活动中发送消息时，会在&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动中定义受众，而不是在协调的活动中定义受众。

## 配置生成受众活动 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="受众"
>abstract="选择您的受众，就像设计新投放时使用受众一样。"

请按照以下步骤配置&#x200B;**[!UICONTROL 生成受众]**&#x200B;活动：

1. 添加一个&#x200B;**[!UICONTROL 生成受众]**&#x200B;活动。

   ![](../assets/build-audience.png)

1. 定义&#x200B;**[!UICONTROL 标签]**。

1. 按照以下选项卡中详述的步骤配置受众。

1. 选择&#x200B;**[!UICONTROL 定位维度]**。通过定位维度，可定义操作面向的群体：收件人、合同受益人、操作人员、订阅者等。默认情况下从收件人中选择目标。

1. 单击&#x200B;**[!UICONTROL 继续]**。

1. 使用查询建模器定义您的查询。 [在本节中了解有关查询建模器的更多信息](../orchestrated-rule-builder.md)

1. 指定在受众为空时是否应生成叫客过渡。

## 示例{#build-audience-examples}

以下是包含两个&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动的编排营销活动示例。 第一个定向的是购物车中包含项目的用户档案，随后是电子邮件投放。 第二个使用愿望清单定位用户档案，然后进行短信投放。

![](../assets/build-audience-2.png)
