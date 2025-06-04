---
solution: Journey Optimizer
product: journey optimizer
title: 使用构建受众活动
description: 了解如何在编排的活动中使用构建受众活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 32b13d4fd62abc8052c1bf64d8a2d5e97bd0f464
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 44%

---

# 构建受众 {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="生成受众活动"
>abstract="您可以使用&#x200B;**生成受众**&#x200B;活动，定义将进入协同营销活动的受众。在协同营销活动的上下文中发送消息时，消息受众不是在渠道活动中定义的，而是在&#x200B;**生成受众**&#x200B;活动中定义的。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库  | 编排的营销活动活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](../gs-campaign-creation.md) | [创建协调的营销活动](../create-orchestrated-campaign.md)<br/><br/>[协调活动](../orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](../send-messages.md)<br/><br/>[开始并监视营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用查询Modeler](../orchestrated-query-modeler.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[And-join](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/><br/>

作为营销人员，您可以使用用户友好的界面轻松创建复杂查询，从而让我能够根据各种标准和行为来细分受众，从而更有效地定制营销活动。

要执行此操作，请使用&#x200B;**构建受众**&#x200B;定位活动。 利用此活动，可定义将进入编排营销活动的受众。 在协同营销活动的上下文中发送消息时，消息受众不是在渠道活动中定义的，而是在&#x200B;**生成受众**&#x200B;活动中定义的。

要定义受众群体，您可以：

* 选择现有受众。
* 选择预定义过滤器。
* 通过定义和组合筛选条件，使用查询建模器构建新受众。

>[!NOTE]
>
>无法使用构建受众活动定位从文件加载的受众。 为此，您需要先使用&#x200B;**加载文件**&#x200B;活动，然后再使用&#x200B;**协调**&#x200B;活动。


## 配置生成受众活动 {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="受众"
>abstract="选择您的受众，就像设计新投放时使用受众一样。"

请按照以下步骤配置&#x200B;**生成受众**&#x200B;活动：

![](../assets/build-audience.png)

1. 添加一个&#x200B;**生成受众**&#x200B;活动。
1. 定义一个标签。
1. 定义受众类型：**创建您自己的**&#x200B;或&#x200B;**读取受众**。
1. 按照以下选项卡中详述的步骤配置受众。


要创建自己的查询，请执行以下步骤：

1. 选择&#x200B;**创建您自己的（查询）**。
1. 选择&#x200B;**定位维度**。通过定位维度，可定义操作面向的群体：收件人、合同受益人、操作人员、订阅者等。默认情况下从收件人中选择目标。
1. 单击&#x200B;**继续**。
1. 使用查询建模器定义您的查询。 [在本节中了解有关查询建模器的更多信息](../orchestrated-query-modeler.md)

## 示例{#build-audience-examples}

以下是包含两个&#x200B;**构建受众**&#x200B;活动的编排营销活动示例。 第一个示例针对扑克玩家受众，然后是电子邮件投放。第二个示例针对 VIP 客户受众，然后是短信投放。

![](../assets/workflow-audience-example.png)
