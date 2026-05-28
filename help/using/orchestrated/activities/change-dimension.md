---
solution: Journey Optimizer
product: journey optimizer
title: 使用“更改维度”活动
description: 了解如何使用“更改维度”活动
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/yN2RlYom4xpdiG0G8pt3U4MeY0C1JjDudDqYg-HPv1w
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 50%

---

# 更改维度 {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="生成补集"
>abstract="可使用剩余群体（已排除的重复项）生成额外的出站过渡。为此，请打开生成补集选项 为此，请打开&#x200B;**生成补集**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="更改维度活动"
>abstract="通过此活动，可在生成受众时更改定位维度。 它根据数据模板和输入维度移动轴。 例如，您可以从“合同”维度切换到“客户”维度。"

作为营销人员，您可以通过在编排的营销活动中从一个数据实体转移到相关数据实体来增强受众定位。 这使您能够越过轮廓并专注于特定行为，例如购买、预订或其他交互。

要实现此目的，请使用&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动。 它允许您在编排的营销活动期间调整定向维度。

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.
-->

## 配置“更改维度”活动 {#configure}

请按照以下步骤配置&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动：

1. 将&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动添加到您的编排营销活动。

   ![](../assets/orchestrated-change-dimension.png)

1. 定义&#x200B;**[!UICONTROL 新目标维度]**。 “更改”维度步骤使用外部联接：输入群体中的所有记录都会通过，包括新维度中没有匹配条目的记录。

   >[!IMPORTANT]
   >
   >新定向维度中没有匹配用户档案的记录将在消息投放时&#x200B;**静默排除**。 此排除项当前未反映在排除日志中。 要尽早识别不匹配的记录，请在更改维度步骤之后对过渡使用&#x200B;**预览结果**&#x200B;选项，并在继续之前验证记录计数是否符合您的预期。


## 示例 {#example}

在此用例中，主要是向在过去一个月内创建了愿望清单的轮廓发送短信。

在开始&#x200B;**[!UICONTROL 生成受众]**&#x200B;活动时，使用&#x200B;**[!UICONTROL 愿望清单]**&#x200B;目标维度识别所有相关愿望清单。

然后，添加&#x200B;**[!UICONTROL 更改维度]**&#x200B;活动以将定向维度从&#x200B;**[!UICONTROL 愿望清单]**&#x200B;切换为&#x200B;**[!UICONTROL 收件人]。** 此步骤可确保编排的营销活动定向到与这些愿望清单关联的正确用户档案，从而允许将短信发送到预期用户档案。

![](../assets/orchestrated-change-dimension-example.png)
