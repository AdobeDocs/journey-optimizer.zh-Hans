---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer启动和监控编排的营销活动
description: 了解如何使用Adobe Journey Optimizer启动和监控编排的营销活动。
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 0ae8372c179707a87a6b512a5420753a4aaef754
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 2%

---

# 构建重定位查询 {#retarget}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建和计划营销活动](create-orchestrated-campaign.md)<br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[启动并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/><b>[重新定位](retarget.md)</b> | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

正在进行文档

>[!ENDSHADEBOX]

通过重新定位，可根据收件人对之前编排的营销活动的响应方式与其进行跟踪。 例如，您可以向已收到但未单击第一封邮件的用户档案发送第二封电子邮件。

编排的营销活动为此提供了两个主要数据源：

- **邮件反馈**：捕获与投放相关的事件，例如已发送的邮件、已打开的邮件、已退回的邮件等。

- **电子邮件跟踪**：捕获用户操作，例如点击和打开。

## 创建基于反馈的重定位规则

基于反馈的重定位规则允许您根据&#x200B;**消息反馈**&#x200B;数据集中捕获的消息投放事件重定位收件人。 这些事件包括发送、打开、退回或标记为垃圾邮件的邮件。

利用此数据，您可以定义规则来识别收到之前消息但未参与该消息的收件人，从而实现基于特定投放状态的跟进通信。

1. 创建新的&#x200B;**编排的营销活动**。

2. 添加&#x200B;**生成受众**&#x200B;活动并将定向维度设置为&#x200B;**收件人(caas)**。

3. 在&#x200B;**规则生成器**&#x200B;中，单击&#x200B;**添加条件**&#x200B;并从属性选取器中选择&#x200B;**消息反馈**。 单击&#x200B;**确认**。

4. 为&#x200B;**反馈状态**&#x200B;添加条件，并将值设置为&#x200B;**已发送消息**。

5. 要定位特定的编排活动，请执行以下操作：

   - 添加其他条件，搜索`entity`，然后导航到：\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`。

   - 选择&#x200B;**编排的营销活动名称**&#x200B;并指定营销活动名称。

6. 要定位该编排活动中的特定消息或活动，请执行以下操作：

   - 添加其他条件，搜索`entity`，然后导航到：\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`。

   - 选择&#x200B;**编排的营销活动操作名称**&#x200B;并指定营销活动操作名称。

     单击画布中活动旁边的![信息图标](assets/do-not-localize/info-icon.svg)可以找到操作名称。

   >[!TIP]
   >
   >您还可以按&#x200B;**促销活动ID** (UUID)进行筛选，而不是使用名称，该筛选可在促销活动属性中找到。

## 创建基于跟踪的重定位规则

基于跟踪的重定位规则使用&#x200B;**电子邮件跟踪**&#x200B;数据集中的数据，根据收件人与消息的交互情况来定位收件人。 它捕获用户操作，如电子邮件打开和链接点击。

要根据邮件交互（例如，打开或单击）重新定位收件人，请按如下方式使用&#x200B;**电子邮件跟踪**&#x200B;实体：

1. 创建新的&#x200B;**编排的营销活动**，然后添加一个&#x200B;**构建受众**&#x200B;活动，其中将&#x200B;**收件人(caas)**&#x200B;作为定向维度，以重点关注以前编排的营销活动收件人。

1. 为&#x200B;**电子邮件跟踪**&#x200B;添加新条件。 单击&#x200B;**确认**&#x200B;以创建“电子邮件跟踪存在，例如”条件。

1. 在该条件下，添加条件并搜索&#x200B;**交互类型**&#x200B;属性。

1. 从自定义条件选项中，使用&#x200B;**Included in**&#x200B;作为运算符，并根据您的用例选择一个或多个值。 例如：
   - **消息已打开**
   - 已单击&#x200B;**消息链接**

1. 要将跟踪数据与特定营销活动关联，请执行以下操作：

   - 在电子邮件跟踪块中添加条件。

   - 导航到`_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`。

   - 为&#x200B;**协调的营销活动名称**&#x200B;添加条件，如果需要，**协调的营销活动操作名称**&#x200B;添加条件。

     单击画布中活动旁边的![信息图标](assets/do-not-localize/info-icon.svg)可以找到操作名称。

   >[!TIP]
   >
   >您还可以按&#x200B;**促销活动ID** (UUID)进行筛选，而不是使用名称，该筛选可在促销活动属性中找到。
