---
solution: Journey Optimizer
product: journey optimizer
title: 使用更改维度活动
description: 了解如何使用更改维度活动
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 22%

---

# 更改维度 {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="生成补集"
>abstract="可使用剩余群体（已排除的重复项）生成额外的出站过渡。为此，请打开生成补集选项为此，请打开&#x200B;**生成补集**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="“更改维度”活动"
>abstract="通过此活动，可在构建受众时更改目标选择维度。它根据数据模板和输入维度移动轴。例如，您可以从“合同”维度切换到“客户”维度。"

**更改维度**&#x200B;活动是&#x200B;**定位**&#x200B;活动。 利用此活动，可在构建多步营销活动时更改定向维度。 它根据数据模板和输入维度移动轴。

例如，您可以将多步骤营销活动的定向维度从“收件人”切换为“订阅者应用程序”，以便向定向收件人发送推送通知。

>[!IMPORTANT]
>
>请注意，不应将&#x200B;**[!UICONTROL 更改维度]**&#x200B;和&#x200B;**[!UICONTROL 更改数据源]**&#x200B;活动添加到一行中。 如果需要连续使用这两个活动，请确保在它们之间包含&#x200B;**[!UICONTROL 扩充]**&#x200B;活动。 这可以确保正确执行并防止潜在的冲突或错误。

## 配置更改维度活动 {#configure}

按照以下步骤配置&#x200B;**更改维度**&#x200B;活动：

1. 将&#x200B;**更改维度**&#x200B;活动添加到您的多步骤营销活动。

   ![](../assets/workflow-change-dimension.png)

1. 定义&#x200B;**新目标维度**。 在维度更改期间，将保留所有记录。 其他选项尚不可用。

1. 执行多步骤营销活动以查看结果。 比较更改维度活动之前和之后的表中的数据，并比较多步骤促销活动表的结构。

## 示例 {#example}

在本例中，我们希望向所有已购买的用户档案发送短信投放。 为此，我们首先使用链接到自定义“购买”定向维度的&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动来定向发生的所有购买。

然后，我们使用&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动将多步骤营销活动定向维度切换为“收件人”。 这样，我们便能够定位匹配查询的收件人。

![](../assets/workflow-change-dimension-example.png)
