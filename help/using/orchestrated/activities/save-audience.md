---
solution: Journey Optimizer
product: journey optimizer
title: 使用保存受众活动
description: 了解如何在编排的活动中使用保存受众活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: a19fe429d34a88c6159ab3b2b4dfa3768bcd24ad
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 4%

---

# 保存受众 {#save-audience}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[访问和管理协调的营销活动](../access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](../gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](../create-orchestrated-campaign.md)<br/><br/>[编排活动](../orchestrate-activities.md)<br/><br/>[启动和监控营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用规则生成器](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md)<br/><br/>[重新定位](../retarget.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[并加入](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [渠道活动](channels.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - <b>[保存受众](save-audience.md)</b> - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++


**[!UICONTROL 保存受众]**&#x200B;活动是一个&#x200B;**[!UICONTROL 定位]**&#x200B;活动，通过该活动可更新现有受众或利用之前在编排的营销活动中生成的群体创建新受众。 创建受众后，这些受众将添加到应用程序受众列表中，并可从&#x200B;**[!UICONTROL 受众]**&#x200B;菜单访问。

此活动对于保留在同一编排的营销活动中计算的受众区段特别有用，以便将来营销活动中重复使用。 它通常连接到其他定向活动，如&#x200B;**[!UICONTROL 构建受众]**&#x200B;或&#x200B;**[!UICONTROL 组合]**，以捕获并保存生成的群体。

## 配置保存受众活动 {#save-audience-configuration}

按照以下步骤配置&#x200B;**[!UICONTROL 保存受众]**&#x200B;活动：

1. 将&#x200B;**[!UICONTROL 保存受众]**&#x200B;活动添加到您的编排的营销活动中。

1. 输入将标识所保存受众的&#x200B;**[!UICONTROL 受众标签]**。

1. 单击&#x200B;**[!UICONTROL 添加受众属性]**&#x200B;以定义如何构建和存储受众数据以供将来重用。

   ![](../assets/save-audience-1.png)

1. 然后，选择适当的&#x200B;**[!UICONTROL 主标识字段]**&#x200B;和&#x200B;**[!UICONTROL 标识命名空间]**&#x200B;以确保精确的配置文件解析。

   ![](../assets/save-audience-2.png)

1. 通过保存并发布编排的活动以完成设置。 这将生成并存储您的受众。

随后，受众的详细信息视图中会提供所保存受众的内容，可通过&#x200B;**[!UICONTROL 受众]**&#x200B;菜单访问该视图。

![](../assets/save-audience-3.png)

## 示例 {#save-audience-example}

以下示例演示了如何使用定位创建简单的受众。 查询可识别过去30天内购买的所有用户档案。 然后，**[!UICONTROL 保存受众]**&#x200B;活动会捕获这些配置文件，以创建最近购买者的可重用受众。

![](../assets/save-audience-4.png)
