---
solution: Journey Optimizer
product: journey optimizer
title: 使用拆分活动
description: 了解如何在编排的活动中使用拆分活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: 38b65200435e0b997e79aefbb66549b9168188fd
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 54%

---

# 拆分 {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="拆分活动"
>abstract="通过&#x200B;**拆分**&#x200B;活动，可根据不同的选择标准（如筛选规则或群体大小）将传入的群体分为多个子集。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](../gs-campaign-creation.md) | [创建协调的营销活动](../create-orchestrated-campaign.md)<br/><br/>[协调活动](../orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](../send-messages.md)<br/><br/>[开始并监视营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用查询Modeler](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[And-join](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**[!UICONTROL 拆分]**&#x200B;活动是一个&#x200B;**[!UICONTROL 定位]**&#x200B;活动，该活动根据定义的选择条件（如筛选规则或群体大小）将传入群体划分为多个子集。

## 配置拆分活动 {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="拆分活动的区段"
>abstract="添加所需数量的子集以划分传入的群体。<br/></br>执行&#x200B;**拆分**&#x200B;活动时，将群体按将其添加到活动的顺序划分为不同的子集。在开始协同营销活动之前，请确保您已使用箭头按钮按照符合您需求的顺序为子集排序。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_filter"
>title="拆分活动筛选条件"
>abstract="要将筛选条件应用于子集，请单击&#x200B;**[!UICONTROL 创建筛选条件]**&#x200B;并使用查询建模器配置所需的筛选规则。例如，包括其电子邮件地址位于数据库中的传入群体的轮廓。"

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
   >**Split**&#x200B;活动按子集的添加顺序处理这些子集。 例如，如果第一个子集捕获了总人口的70%，则下一个子集将其标准应用于其余30%。
   >
   >在运行编排的活动之前，请确保按预期对子集进行排序。 使用箭头按钮调整其位置。

1. 添加子集后，活动将显示与子集一样多的输出转换。我们强烈建议更改每个子集的标签，以便在编排的活动画布中轻松识别它们。

1. 为每个子集配置过滤器：

   1. 单击子集以打开其设置。

   1. 单击&#x200B;**[!UICONTROL 创建过滤器]**&#x200B;以使用查询建模器定义过滤规则，例如，选择具有有效电子邮件地址的用户档案。

      ![](../assets/orchestrated-split-1.png)

   1. 要限制所选配置文件的数量，请启用&#x200B;**[!UICONTROL 启用限制]**&#x200B;并指定一个数字或百分比。

   1. 要在子集为空时跳过过渡，请启用&#x200B;**[!UICONTROL 跳过空过渡]。**

1. 要包含任何子集不匹配的配置文件，请启用&#x200B;**[!UICONTROL 生成补码]**。 这会为剩余群体创建一个额外的叫客过渡。

   >[!NOTE]
   >
   >启用&#x200B;**[!UICONTROL 在同一表]**&#x200B;中生成所有子集以将所有子集分组到单个转换中。

1. 使用&#x200B;**[!UICONTROL 启用输出群体的重叠]**&#x200B;以允许配置文件出现在多个子集中：

   * **如果未选中**，则每个配置文件将仅分配给一个子集，即分配给其标准匹配的第一个子集，即使它符合其他子集的条件。

   * **如果选中**，则如果配置文件满足每个子集的条件，则可以将其包含在多个子集中。

现已配置该活动。在编排的活动执行中，群体将按照其添加到活动的顺序划分为不同的子集。

## 示例{#split-example}

在下面的示例中，**[!UICONTROL 拆分]**&#x200B;活动用于根据要使用的通信渠道将受众划分为不同的子集：

* **子集1“电子邮件”**：包括已提供电话号码的用户档案。

* **子集2“短信”**：使用存储在数据库中的手机号码定向用户档案。

* **补充过渡**：捕获不符合任一子集条件的任何剩余配置文件。

![](../assets/orchestrated-split-3.png)
