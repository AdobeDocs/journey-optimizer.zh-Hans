---
solution: Journey Optimizer
product: journey optimizer
title: 在编排的活动中使用测试活动
description: 了解如何使用“测试”活动
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 83%

---


# 测试 {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="”测试“活动"
>abstract="**测试**&#x200B;活动是&#x200B;**流量控制**&#x200B;活动。它允许您根据指定条件启用过渡。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="条件"
>abstract="**测试**&#x200B;活动可以有多个输出过渡。在编排营销活动的执行过程中，会按顺序测试每个条件，直到满足其中一个条件。如果未满足任何条件，精心编排的营销活动会沿着&#x200B;**[!UICONTROL 默认条件]**&#x200B;路径继续。如果默认条件未激活，精心编排的营销活动会在此时停止。"

**[!UICONTROL 测试]**&#x200B;活动是&#x200B;**[!UICONTROL 流量控制]**&#x200B;活动。它允许您根据指定条件启用过渡。

## 配置测试活动 {#test-configuration}

请按照以下步骤操作，配置&#x200B;**[!UICONTROL 测试]**&#x200B;活动：

1. 将&#x200B;**[!UICONTROL Test]**&#x200B;活动添加到您的编排营销活动中。

1. 默认情况下，**[!UICONTROL 测试]**&#x200B;活动会进行简单的布尔值测试。如果满足“True”过渡中定义的条件，则将激活此过渡。否则，将激活默认的“False”过渡。

1. 要配置与过渡关联的条件，请单击&#x200B;**[!UICONTROL 打开个性化对话框]**&#x200B;图标。使用表达式编辑器定义激活此过渡所需的规则。您还可以利用事件变量、条件和日期/时间函数。

   此外，您可以修改&#x200B;**[!UICONTROL 标签]**&#x200B;字段，以便在编排的活动画布上个性化过渡名称。

   ![](../assets/workflow-test-default.png)

1. 您可以向&#x200B;**[!UICONTROL 测试]**&#x200B;活动添加多个输出过渡。为此，请单击&#x200B;**[!UICONTROL 添加条件]**按钮，并为每个过渡配置标签和相关条件。
v
1. 在编排营销活动的执行过程中，会按顺序测试每个条件，直到满足其中一个条件。如果不满足任何条件，则编排的营销活动将沿着&#x200B;**[!UICONTROL 默认条件]**&#x200B;的路径继续。 如果未激活默认条件，则营销活动将在此时停止。

## 示例 {#example}

在此示例中，会根据&#x200B;**[!UICONTROL 生成受众]**&#x200B;活动选择的目标轮廓数量激活不同的过渡：

* 如果选择的目标轮廓数量超过 10,000 个，则发送电子邮件。
* 如果轮廓数量在 1,000 到 10,000 之间，则发送短信。
* 如果目标轮廓数量低于 1,000，则会被定向到“请勿联系”过渡。

![](../assets/workflow-test-example.png)

为此，已在“电子邮件”和“短信”条件中利用 `vars.recCount` 事件变量，计算目标轮廓的数量并激活相应的过渡。

![](../assets/workflow-test-example-config.png)
