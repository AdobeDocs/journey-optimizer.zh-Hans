---
solution: Journey Optimizer
product: journey optimizer
title: 在编排的活动中使用等待活动
description: 了解如何在编排的活动中使用等待活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: d59643f18a335fe1e094156a1cfee65b717b9fce
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 11%

---

# 等待 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="等待活动"
>abstract="**等待**&#x200B;活动用于将过渡从一个活动推迟另一个活动。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库  | 编排的营销活动活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](../gs-campaign-creation.md) | [创建协调的营销活动](../create-orchestrated-campaign.md)<br/><br/>[协调活动](../orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](../send-messages.md)<br/><br/>[开始并监视营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用查询Modeler](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[And-join](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**等待**&#x200B;活动是一个&#x200B;**流量控制**&#x200B;组件，用于在编排的营销活动中的两个活动之间引入延迟。 这有助于确保您的跟进活动在更合适的时间进行，并且更切合用户参与。

例如，您可以在电子邮件投放后等待几天，以跟踪打开数和点击数，然后再发送跟进消息。

## 配置{#wait-configuration}

请按照以下步骤操作，配置&#x200B;**等待**&#x200B;活动：

1. 将&#x200B;**等待**&#x200B;活动添加到您的编排营销活动中。

1. 选择最适合您需求的等待类型：

   * **持续时间**：以秒、分钟、小时或天为单位指定延迟，然后再继续下一个活动。

   * **固定时间**：设置下一个活动开始的特定日期和时间。

   ![](../assets/wait_activity.png)

## 示例{#wait-example}

以下示例说明了典型使用案例中的&#x200B;**等待**&#x200B;活动。  带有促销代码的电子邮件会发送给庆祝其生日的用户档案。 29天后，将向同一组发送短信，提醒其生日促销代码即将过期。

![](../assets/wait-example.png)
