---
solution: Journey Optimizer
product: journey optimizer
title: 在编排的活动中使用测试活动
description: 了解如何使用测试活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 29%

---

# 测试 {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="”测试“活动"
>abstract="**测试**&#x200B;活动是&#x200B;**流量控制**&#x200B;活动。它允许您根据指定条件启用过渡。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="条件"
>abstract="**测试**&#x200B;活动可以有多个输出过渡。在执行协同营销活动期间，将会按顺序测试每个条件，直到满足其中一个条件。如果没有满足任何条件，协同营销活动会沿着&#x200B;**[!UICONTROL 默认条件]**&#x200B;路径继续。如果没有激活默认条件，协同营销活动会在此时停止。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用协调的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[访问和管理协调的营销活动](../access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](../gs-campaign-creation.md)<br/><br/>[创建和计划营销活动](../create-orchestrated-campaign.md)<br/><br/>[编排活动](../orchestrate-activities.md)<br/><br/>[启动和监控营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用规则生成器](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md)<br/><br/>[重新定位](../retarget.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[并加入](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [渠道活动](channels.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [保存受众](save-audience.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

**[!UICONTROL 测试]**&#x200B;活动是&#x200B;**[!UICONTROL 流量控制]**&#x200B;活动。它允许您根据指定条件启用过渡。

## 配置测试活动 {#test-configuration}

按照以下步骤配置&#x200B;**[!UICONTROL 测试]**&#x200B;活动：

1. 将&#x200B;**[!UICONTROL Test]**&#x200B;活动添加到您的编排的营销活动中。

1. 默认情况下，**[!UICONTROL Test]**&#x200B;活动提供简单的布尔测试。 如果满足“True”过渡中定义的条件，则将激活此过渡。 否则，将激活默认的“False”过渡。

1. 要配置与过渡关联的条件，请单击&#x200B;**[!UICONTROL 打开个性化对话框]**&#x200B;图标。 使用表达式编辑器定义激活此过渡所需的规则。 您还可以利用事件变量、条件和日期/时间函数。

   此外，您可以修改&#x200B;**[!UICONTROL 标签]**&#x200B;字段，以便在编排的活动画布上个性化过渡名称。

   ![](../assets/workflow-test-default.png)

1. 您可以向&#x200B;**[!UICONTROL 测试]**&#x200B;活动添加多个输出过渡。 为此，请单击&#x200B;**[!UICONTROL 添加条件]**按钮，并为每个过渡配置标签和相关条件。
v
1. 在执行协同营销活动期间，将会按顺序测试每个条件，直到满足其中一个条件。如果不满足任何条件，则编排的营销活动将沿&#x200B;**[!UICONTROL 默认条件]**&#x200B;的路径继续。 如果没有激活默认条件，工作流会在此时停止。

## 示例 {#example}

在此示例中，根据&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动定向的用户档案数激活不同的过渡：

* 如果定向的用户档案超过10,000个，则会发送电子邮件。
* 对于1,000到10,000个用户档案，将发送短信。
* 如果目标用户档案低于1,000，则会被定向到“请勿联系”过渡。

![](../assets/workflow-test-example.png)

为此，已在“电子邮件”和“短信”条件中利用`vars.recCount`事件变量来计数目标用户档案的数量并激活相应的过渡。

![](../assets/workflow-test-example-config.png)
