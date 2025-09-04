---
solution: Journey Optimizer
product: journey optimizer
title: 使用“分叉”活动
description: 了解如何在编排的活动中使用分支活动
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 86%

---


# 分叉 {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="分叉活动"
>abstract="利用&#x200B;**分叉**&#x200B;活动，可创建叫客过渡以同时开始若干活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="分叉活动过渡"
>abstract="默认情况下，使用&#x200B;**分叉**&#x200B;活动创建两个过渡。单击&#x200B;**添加过渡**&#x200B;按钮以定义其他叫客过渡并输入其标签。"

**[!UICONTROL 分叉]**&#x200B;活动是一个&#x200B;**[!UICONTROL 流程控制]**&#x200B;组件，可用于创建多个出站过渡，实现多个活动的并行运行。

## 配置“分叉”活动{#fork-configuration}

请按照以下步骤操作，配置&#x200B;**[!UICONTROL 分叉]**&#x200B;活动：

![](../assets/workflow-fork.png)

1. 将&#x200B;**[!UICONTROL 分支]**&#x200B;活动添加到您的编排营销活动中。

1. 定义一个&#x200B;**[!UICONTROL 标签]**。

1. 为每个出站过渡分配标签。默认提供两个过渡。

1. 要移除过渡，请单击 ![](../assets/do-not-localize/Smock_Delete_18_N.svg) 图标。

1. 如果需要，请单击&#x200B;**[!UICONTROL 添加过渡]**&#x200B;以添加其他出站过渡。
