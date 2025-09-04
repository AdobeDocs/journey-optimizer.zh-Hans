---
solution: Journey Optimizer
product: journey optimizer
title: 使用“并行汇聚”活动
description: 了解如何在编排的活动中使用AND — 连接活动
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 84%

---


# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="AND-join 活动"
>abstract="您可以使用 **And-join** 活动，使某个精心编排的营销活动的多个执行分支彼此同步。一旦完成所有之前的活动，即会触发该活动。这样可以在继续执行精心编排的营销活动之前，确保某些特定活动已经完成。"

**[!UICONTROL 并行汇聚]**&#x200B;活动是一种&#x200B;**[!UICONTROL 流程控制]**&#x200B;活动。它允许您同步编排营销活动的多个执行分支。

一旦激活所有入站过渡，换言之，一旦完成所有先行工作，此活动就会触发其所有出站过渡。这允许您在继续执行Orchestrated营销活动之前确保某些活动已完成。

## 配置 AND-join 活动{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="合并选项"
>abstract="选择您要参加的活动。在&#x200B;**主要集合**&#x200B;下拉列表中，选择要保留的集客过渡群体。"

请按照以下步骤操作，配置&#x200B;**[!UICONTROL 并行汇聚]**&#x200B;活动：

![](../assets/workflow-andjoin.png)

1. 添加多项活动（例如渠道活动）以创建至少两个不同的执行分支。

1. 向任一分支插入一个&#x200B;**[!UICONTROL 并行汇聚]**&#x200B;活动。

1. 在&#x200B;**[!UICONTROL 合并选项]**&#x200B;部分下，选择要加入的所有先前活动。

1. 在&#x200B;**[!UICONTROL 主集]**&#x200B;下拉列表中，选择您要保留的入站过渡群体。

## 示例{#and-join-example}

此示例说明了两个协调的营销活动分支，每个分支均具有电子邮件投放，一个以黄金会员为目标选择，一个以白银会员为目标选择。一旦触发了两个传入的过渡，**[!UICONTROL 并行汇聚]**&#x200B;就会激活，并且仅在两个电子邮件投放完成后（延迟 7 天）才会发送短信。

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
