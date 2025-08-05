---
solution: Journey Optimizer
product: journey optimizer
title: 使用“拆分”活动
description: 了解如何在编排的活动中使用拆分活动
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 82%

---


# 拆分 {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="拆分活动"
>abstract="通过&#x200B;**拆分**&#x200B;活动，可根据不同的选择标准（如筛选规则或群体大小）将传入的群体分为多个子集。"

**[!UICONTROL 拆分]**&#x200B;活动是一种&#x200B;**[!UICONTROL 目标选择]**&#x200B;活动，可让您根据定义的选择标准（例如筛选规则或群体大小）将传入群体划分为多个子集。

## 配置拆分活动 {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="拆分活动的区段"
>abstract="添加所需数量的子集以划分传入的群体。<br/></br>执行&#x200B;**拆分**&#x200B;活动时，将群体按将其添加到活动的顺序划分为不同的子集。在开始协调的活动之前，请确保已使用箭头按钮按适合您需要的顺序订购了子集。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_filter"
>title="拆分活动筛选条件"
>abstract="要将筛选条件应用到子集，请单击&#x200B;**[!UICONTROL 创建筛选器]**，然后使用规则生成器配置所需的筛选规则。 例如，包括其电子邮件地址位于数据库中的传入群体的轮廓。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_limit"
>title="拆分活动限制"
>abstract="要限制子集选择的轮廓数，请打开&#x200B;**[!UICONTROL 启用限制]**&#x200B;选项，并指定要包括的群体的数量或百分比。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_sorting"
>title="拆分活动排序"
>abstract="在为子集设置群体限制时，您可以根据特定的轮廓属性按升序或降序顺序对所选轮廓进行排名。为此，请打开&#x200B;**启用排序**&#x200B;选项。例如，您可以限制子集以仅包含购买金额最高的前 50 个轮廓。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_complement"
>title="拆分生成补集"
>abstract="配置完所有子集后，您可以选择与任何子集均不匹配的剩余群体，并将其包含到附加出站过渡中。为此，请打开&#x200B;**生成补集**&#x200B;选项。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_generatesubsets"
>title="在同一个表中生成所有子集"
>abstract="切换该选项可将所有子集组合到单个输出过渡中。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_emptytransition"
>title="跳过空过渡"
>abstract="如果传入的群体为空，则切换&#x200B;**[!UICONTROL 跳过空过渡]**&#x200B;选项，以禁用此子集的输出过渡。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_enable_overlapping"
>title="启用输出群体的重叠"
>abstract=" **[!UICONTROL 启用输出群体重叠]**&#x200B;选项可让您管理属于多个子集的群体。当未选中该框时，拆分活动将确保收件人不会出现在多个输出转换中，即使它满足多个子集的标准。它们将位于符合条件的第一个选项卡的目标中。选中此框后，如果收件人符合筛选条件，则可以在多个子集中找到他们。"

请执行以下步骤来配置&#x200B;**[!UICONTROL 拆分]**&#x200B;活动：

1. 将&#x200B;**[!UICONTROL 拆分]**&#x200B;活动添加到您的编排营销活动中。

1. 活动配置窗格随即打开，其中包含默认子集。单击&#x200B;**[!UICONTROL 添加区段]**&#x200B;按钮以添加所需数量的子集，对传入群体进行分段。

   ![](../assets/orchestrated-split-1.png)

   >[!IMPORTANT]
   >
   >**拆分**&#x200B;活动按子集的添加顺序处理这些子集。例如，如果第一个子集捕获了群体的 70%，则下一个子集会将其标准应用于剩余的 30%。
   >
   >在运行“编排”活动之前，请确保按预期对子集进行排序。 使用箭头按钮调整其位置。

1. 添加子集后，活动将显示与子集一样多的输出过渡。我们强烈建议更改每个子集的标签，以便在编排的活动画布中轻松识别它们。

1. 为每个子集配置过滤器：

   1. 单击子集以打开其设置。

   1. 单击&#x200B;**[!UICONTROL 创建筛选器]**&#x200B;以使用规则生成器定义筛选规则，例如，选择具有有效电子邮件地址的用户档案。

      ![](../assets/orchestrated-split-1.png)

   1. 要限制所选轮廓的数量，请启用&#x200B;**[!UICONTROL 启用限制]**&#x200B;并指定一个数字或百分比。

   1. 要在子集为空时跳过过渡，请启用&#x200B;**[!UICONTROL 跳过空过渡]。**

1. 要包含与任何子集不匹配的轮廓，请启用&#x200B;**[!UICONTROL 生成补集]**。这会为剩余群体创建一个额外的出站过渡。

   >[!NOTE]
   >
   >启用&#x200B;**[!UICONTROL 在同一表中生成所有子集]**，以将所有子集分组到单个过渡中。

1. 使用&#x200B;**[!UICONTROL 启用输出群体重叠]**，以允许轮廓出现在多个子集中：

   * **如果未勾选**，则每个轮廓将仅被分配给一个子集，即分配给符合标准的第一个子集，即使该轮廓符合其他子集的条件。

   * **如果勾选**，如果轮廓满足每个子集的条件，则可以包含在多个子集中。

现已配置该活动。在编排的活动执行中，群体将按照其添加到活动的顺序划分为不同的子集。

## 示例{#split-example}

在下面的示例中，**[!UICONTROL 拆分]**&#x200B;活动用于根据要使用的通信渠道将受众划分为不同的子集：

* **子集 1“电子邮件”**：包括已提供电话号码的轮廓。

* **子集 2“短信”**：根据存储在数据库中的手机号码选择目标轮廓。

* **补集过渡**：捕获不符合任一子集的条件的其他剩余轮廓。

![](../assets/orchestrated-split-3.png)
