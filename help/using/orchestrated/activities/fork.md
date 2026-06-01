---
solution: Journey Optimizer
product: journey optimizer
title: 使用“分叉”活动
description: 了解如何在编排的活动中使用分支活动
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/b0FyVaM0LcSz1DLGd-UEhHqBqXMWcb0rbimJA6E7WOM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29c
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 256
ht-degree: 47%

---

# 分叉 {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="分叉活动"
>abstract="利用&#x200B;**分叉**&#x200B;活动，可创建叫客过渡以同时开始若干活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="分叉活动过渡"
>abstract="默认情况下，使用&#x200B;**分叉**&#x200B;活动创建两个过渡。 单击&#x200B;**添加过渡**&#x200B;按钮以定义其他叫客过渡并输入其标签。"

**[!UICONTROL 分叉]**&#x200B;活动是一个&#x200B;**[!UICONTROL 流程控制]**&#x200B;组件，可用于创建多个出站过渡，实现多个活动的并行运行。

## 配置“分叉”活动{#fork-configuration}

请按照以下步骤操作，配置&#x200B;**[!UICONTROL 分叉]**&#x200B;活动：

![](../assets/workflow-fork.png)

1. 将&#x200B;**[!UICONTROL 分支]**&#x200B;活动添加到您的编排营销活动中。

1. 定义一个&#x200B;**[!UICONTROL 标签]**。

1. 为每个出站过渡分配标签。 默认提供两个过渡。

1. 要移除过渡，请单击 ![](../assets/do-not-localize/Smock_Delete_18_N.svg) 图标。

1. 如果需要，请单击&#x200B;**[!UICONTROL 添加过渡]**&#x200B;以添加其他出站过渡。

## 示例 {#fork-examples}

以下是&#x200B;**[!UICONTROL 分支]**&#x200B;活动的典型用法：使用两个不同的电子邮件渠道（一个营销和一个事务性）定位相同的受众，以比较投放行为。

在&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动选择目标群体后，**[!UICONTROL 分支]**&#x200B;将创建两个并行分支：

* **分支1**&#x200B;连接到营销电子邮件渠道活动。 报文遵循标准业务规则，并且仅发送给选择加入的用户档案。
* **分支2**&#x200B;连接到事务型电子邮件渠道活动。 消息绕过业务规则，将传递到所有用户档案，而不管选择加入状态如何。

![](../assets/workflow-fork.png)

此模式有助于了解渠道类别设置如何影响投放行为，以及在单次营销活动运行时向同一受众发送不同消息类型。
