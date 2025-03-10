---
solution: Journey Optimizer
product: journey optimizer
title: 使用分支活动
description: 了解如何在多步营销活动中使用分支活动
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 83%

---

# 分叉 {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="“分叉”活动"
>abstract="利用&#x200B;**分叉**&#x200B;活动，可创建叫客过渡以同时开始若干活动。"


>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="“分叉”活动过渡"
>abstract="默认情况下，使用&#x200B;**分叉**&#x200B;活动创建两个过渡。单击&#x200B;**添加过渡**&#x200B;按钮以定义其他叫客过渡并输入其标签。"

**分叉**&#x200B;活动是一种&#x200B;**流量控制**&#x200B;活动。可使用它创建叫客过渡以同时开始多个活动。

## 配置分支活动{#fork-configuration}

请按照以下步骤操作，配置&#x200B;**分叉**&#x200B;活动：

![](../assets/workflow-fork.png)

1. 将&#x200B;**分支**&#x200B;活动添加到您的多步骤营销活动。
1. 单击&#x200B;**添加过渡**&#x200B;以添加新的叫客过渡。默认情况下会定义两个过渡。
1. 请为每个过渡添加标签。

## 示例{#fork-example}

在下面的示例中，我们使用两个&#x200B;**分叉**&#x200B;活动：

* 在两个查询之前使用一个分叉活动，同时执行这两个查询。
* 在交集之后使用一个分叉活动，同时向目标群体发送一封电子邮件和一条短信。

![](../assets/workflow-fork-example.png)
