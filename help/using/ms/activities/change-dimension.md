---
solution: Journey Optimizer
product: journey optimizer
title: 使用更改维度活动
description: 了解如何使用更改维度活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: f0213f1270e9821b61a5dc396e39f5707f8f4b42
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 26%

---

# 更改维度 {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="生成补集"
>abstract="可使用剩余群体（已排除的重复项）生成额外的出站过渡。为此，请打开生成补集选项为此，请打开&#x200B;**生成补集**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="更改维度活动"
>abstract="通过此活动，可在构建受众时更改目标市场选择维度。它根据数据模板和输入维度移动轴。例如，您可以从“合同”维度切换到“客户”维度。"

**更改维度**&#x200B;活动是&#x200B;**定位**&#x200B;活动。 利用此活动，可在构建编排的营销活动时更改定向维度。 它根据数据模板和输入维度移动轴。

例如，您可以将编排营销活动的目标维度从“用户档案”切换为“合同”，以便向目标合同所有者发送消息。

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## 配置更改维度活动 {#configure}

按照以下步骤配置&#x200B;**更改维度**&#x200B;活动：

1. 将&#x200B;**更改维度**&#x200B;活动添加到您的编排的营销活动中。

   ![](assets/change-dimension.png)

1. 定义&#x200B;**新目标维度**。 在维度更改期间，将保留所有记录。

1. 执行编排的活动以查看结果。 比较更改维度活动之前和之后表中的数据，并比较编排的活动表的结构。

## 示例 {#example}

在本例中，我们希望向所有已购买的用户档案发送短信投放。 为此，我们首先使用链接到自定义“购买”定向维度的&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动来定向发生的所有购买。

然后，我们使用&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动将编排的活动定向维度切换为“收件人”。 这样，我们便能够定位匹配查询的收件人。

![](assets/change-dimension-example.png)
