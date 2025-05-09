---
solution: Journey Optimizer
product: journey optimizer
title: 使用AND — 连接活动
description: 了解如何在编排的活动中使用AND — 连接活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 77%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="AND-join 活动"
>abstract="您可以使用 **And-join** 活动，同步协同营销活动的多个执行分支。一旦完成所有之前的活动，即会触发该活动。这样在继续执行协同营销活动之前，就可以确保某些活动已经完成。"

**AND-连接**&#x200B;活动是&#x200B;**流量控制**&#x200B;活动。它允许您同步编排营销活动的多个执行分支。

一旦激活所有集客过渡，换言之，一旦完成所有先行工作，此活动就会触发其所有叫客过渡。这允许您在继续执行编排的活动之前，确保已完成某些活动。

## 配置 AND-join 活动{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="合并选项"
>abstract="选择您要参加的活动。在&#x200B;**主要集合**&#x200B;下拉列表中，选择要保留的集客过渡群体。"

请按照以下步骤操作，配置 **AND-连接**&#x200B;活动：

![](../assets/workflow-andjoin.png)

1. 添加多项活动（例如渠道活动），来构成至少两个不同的执行分支。
1. 向任何分支添加一个 **AND-连接**&#x200B;活动。
1. 在&#x200B;**合并选项**&#x200B;部分中，选中您之前希望加入的所有活动。
1. 在&#x200B;**主集**&#x200B;下拉列表中，选择您要保留的集客过渡群体。叫客过渡只能包含集客过渡群体之一。

## 示例{#and-join-example}

下方的示例展示了两个经过编排的活动分支，其中包含电子邮件和短信投放。 当两个集客过渡均启用时，将触发 AND-连接。只有在两次投放完成后才会发送推送通知。

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
