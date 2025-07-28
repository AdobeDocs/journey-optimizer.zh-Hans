---
solution: Journey Optimizer
product: journey optimizer
title: 在编排的营销活动中使用等待活动
description: 了解如何在编排的活动中使用等待活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 62%

---

# 等待 {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="等待活动"
>abstract="**等待**&#x200B;活动用于将过渡从一个活动推迟另一个活动。"


+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](../gs-schemas.md)</li><li>[手动架构](../manual-schema.md)</li><li>[文件上载架构](../file-upload-schema.md)</li><li>[摄取数据](../ingest-data.md)</li></ul>[访问和管理编排的营销活动](../access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](../gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](../create-orchestrated-campaign.md)<br/><br/>[编排活动](../orchestrate-activities.md)<br/><br/>[开始和监控营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用规则生成器](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md)<br/><br/>[重定向](../retarget.md) | [活动快速入门](about-activities.md)<br/><br/>活动：<br/>[并行汇聚](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [渠道活动](channels.md) - [合并](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分叉](fork.md) - [协调](reconciliation.md) - [保存受众](save-audience.md) - [拆分](split.md) - <b>[等待](wait.md)</b> |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

**[!UICONTROL 等待]**&#x200B;活动是一个&#x200B;**[!UICONTROL 流量控制]**&#x200B;组件，用于在编排的营销活动中的两个活动之间引入延迟。 这有助于确保在更合适的时间进行后续行动，并且使后续行动对用户参与度的影响更大。

例如，您可以在投放电子邮件后等待几天，以便跟踪打开数和点击数，然后再发送后续消息。

## 配置{#wait-configuration}

请按照以下步骤操作，配置&#x200B;**[!UICONTROL 等待]**&#x200B;活动：

1. 将&#x200B;**[!UICONTROL 等待]**&#x200B;活动添加到您的编排营销活动中。

1. 选择最适合您需求的等待类型：

   * **[!UICONTROL 持续时间]**：以秒、分钟、小时或天为单位指定延迟，然后再进行下一个活动。

   * **[!UICONTROL 固定时间]**：设置下一个活动开始的特定日期和时间。

   ![](../assets/wait_activity.png)

## 示例{#wait-example}

下面的示例展示了典型用例中的&#x200B;**[!UICONTROL 等待]**&#x200B;活动。将会发送包含促销代码的电子邮件给庆祝生日的轮廓。在 29 天之后，将向同一组轮廓发送短信，提醒其生日促销代码即将过期。

![](../assets/wait-example.png)
