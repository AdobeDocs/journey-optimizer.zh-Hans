---
solution: Journey Optimizer
product: journey optimizer
title: 在编排的活动中使用测试活动
description: 了解如何使用“测试”活动
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
version: Campaign Orchestration
source-git-commit: 8175f63d4e1055d285d2f3f12a498a9dbd3fa1ba
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 26%

---


# 测试 {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="”测试“活动"
>abstract="**测试**&#x200B;活动是&#x200B;**流量控制**&#x200B;活动。 它允许您根据指定条件启用过渡。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="条件"
>abstract="**测试**&#x200B;活动可以有多个输出过渡。 在精心编排的营销活动的执行过程中，会按顺序测试每个条件，直到满足其中一个条件。 如果未满足任何条件，精心编排的营销活动会沿着&#x200B;**[!UICONTROL 默认条件]**&#x200B;路径继续。 如果默认条件未激活，精心编排的营销活动会在此时停止。"

**[!UICONTROL 测试]**&#x200B;活动是&#x200B;**[!UICONTROL 流量控制]**&#x200B;活动。 根据您定义的条件，通过激活不同的过渡，使用它来分支营销活动流。 每个条件都可以评估集客过渡中的数据，并且您可以选择哪个过渡首先按评估条件的顺序运行。

## 配置测试活动 {#test-configuration}

要设置&#x200B;**[!UICONTROL 测试]**&#x200B;活动，请执行以下操作：

1. 将&#x200B;**[!UICONTROL Test]**&#x200B;活动拖放到您的编排活动画布中。

1. 默认情况下，活动提供单个布尔测试：当满足“True”条件时，将激活该过渡；否则，将激活“False”（默认）过渡。

   ![](../assets/test-1.png)

1. 通过填写以下字段来定义过渡条件：

   * **标签**：过渡的名称，以便您可以在画布上识别它。

   * **条件类型**：默认情况下要计算群体计数的数据。  此处还列出了变量（来自全局变量或触发信号），可以选择这些变量以根据变量值设定条件。 [了解如何在编排的营销活动中使用变量](../variables-orchestrated-campaigns.md)

   * **运算符**：要应用的比较，例如，等于、大于、小于。 运算符列表取决于条件类型的数据类型。

   * **值**：要与条件类型进行比较的值。

   ![](../assets/test-2.png)

1. 要在两个以上的结果上分支，请单击“添加条件”**&#x200B;**，并为每个其他过渡定义标签和条件。

1. 在运行时，营销活动按顺序评估条件，并遵循第一个匹配的条件。 当没有条件匹配时，如果设置了&#x200B;**[!UICONTROL 默认条件]**，则执行操作；否则，营销活动将在&#x200B;**[!UICONTROL Test]**&#x200B;活动处停止。

## 示例 {#example}

在此示例中，根据&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动定向的用户档案数激活不同的过渡。 条件将按顺序评估；最后一个过渡是默认设置，在没有匹配的先前条件时使用。

* 如果选择的目标轮廓数量超过 10,000 个，则发送电子邮件。
* 默认（无匹配条件）：当计数为10,000或更少时，群体将被定向到“请勿联系”过渡。

![](../assets/workflow-test-example.png)
