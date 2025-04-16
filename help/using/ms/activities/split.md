---
solution: Journey Optimizer
product: journey optimizer
title: 使用拆分活动
description: 了解如何在编排的活动中使用拆分活动
hide: true
hidefromtoc: true
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 76%

---

# 拆分 {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="拆分活动"
>abstract="通过&#x200B;**拆分**&#x200B;活动，可根据不同的选择标准（如筛选规则或群体大小）将传入的群体分为多个子集。"

**拆分**&#x200B;活动是一个&#x200B;**定位**&#x200B;活动，通过它可根据不同的选择标准（如筛选规则或群体大小）将集客群体分为多个子集。

## 配置拆分活动 {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="拆分活动的区段"
>abstract="添加所需数量的子集以划分传入的群体。<br/></br>执行&#x200B;**拆分**&#x200B;活动时，将群体按将其添加到活动的顺序划分为不同的子集。在开始编排的活动之前，请确保已使用箭头按钮按适合您需求的顺序订购了子集。"

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
>abstract=" **[!UICONTROL 启用输出群体重叠]**&#x200B;选项可让您管理属于多个子集的群体。当未选中该框时，拆分活动将确保收件人不会出现在多个输出转换中，即使它满足多个子集的标准。它们将位于符合条件的第一个选项卡的目标中。选中此框后，如果收件人符合过滤条件，则可以在多个子集中找到他们。"

请执行以下步骤来配置&#x200B;**拆分**&#x200B;活动：

1. 将&#x200B;**拆分**&#x200B;活动添加到您的编排营销活动中。

1. 活动配置窗格随即打开，其中包含默认子集。单击&#x200B;**添加区段**&#x200B;按钮以添加所需数量的子集，对传入群体进行分段。

   ![](../assets/workflow-split.png)

   >[!IMPORTANT]
   >
   >执行&#x200B;**拆分**&#x200B;活动时，将按填充添加到该活动的顺序跨不同的子集进行分段。 例如，如果第一个子集恢复初始群体的 70%，则下一个添加的子集仅将其选择标准应用于剩余的 30%，依此类推。
   >
   >在开始精心策划的活动之前，请确保已按照适合您需求的顺序订购了子集。 要实现此目的，请使用箭头按钮更改子集的位置。

1. 添加子集后，活动将显示与子集一样多的输出转换。我们强烈建议更改每个子集的标签，以便在编排的活动画布中轻松识别它们。

1. 配置每个子集筛选传入群体的方式。为此，请执行以下步骤：

   1. 打开子集以显示其属性。

   1. 要将筛选条件应用于子集，请单击&#x200B;**[!UICONTROL 创建筛选条件]**&#x200B;并使用查询建模器配置所需的筛选规则。例如，包括其电子邮件地址位于数据库中的传入群体的轮廓。

   1. 要限制子集选择的轮廓数，请打开&#x200B;**[!UICONTROL 启用限制]**&#x200B;选项，并指定要包括的群体的数量或百分比。

   1. 要在传入群体为空时禁用过渡，请打开&#x200B;**[!UICONTROL 跳过空过渡]**&#x200B;选项。 如果没有与子集匹配的用户档案，则编排的活动将不会转换为下一个活动。

      ![](../assets/workflow-split-subset.png)

1. 配置完所有子集后，您可以选择与任何子集均不匹配的剩余群体，并将其包含到附加出站过渡中。为此，请打开&#x200B;**[!UICONTROL 生成补集]**&#x200B;选项。

   ![](../assets/workflow-split-complement.png)

   >[!NOTE]
   >
   >**[!UICONTROL 在同一表]**&#x200B;中生成所有子集选项允许您将所有子集分组到单个输出转换中。

1. 通过&#x200B;**[!UICONTROL 启用输出群体的重叠]**&#x200B;选项，您可以管理属于多个子集的群体：

   * 当未选中该框时，拆分活动将确保收件人不会出现在多个输出转换中，即使它满足多个子集的标准。它们将位于第一个选项卡的目标中，并带有匹配条件。
   * 选中此框后，如果收件人符合过滤条件，则可以在多个子集中找到他们。最佳实践是使用排他性标准。

现已配置该活动。在编排的活动执行中，群体将按照其添加到活动的顺序划分为不同的子集。

## 示例{#split-example}

在下面的示例中，**[!UICONTROL 拆分]**&#x200B;活动用于根据要使用的通信渠道将受众划分为不同的子集：

* **子集 1“推送”**：此子集包含已安装我们的移动应用程序的所有轮廓。
* **子集 2“短信”**：手机用户：对于未归入子集 1 的剩余群体，子集 2 应用筛选规则来选择数据库中带手机的轮廓。
* **补集过渡**：此过渡捕获不符合子集 1 或子集 2 的条件的所有剩余轮廓。具体来说，它包括既没有安装移动应用程序也没有手机的轮廓，例如未安装移动应用程序或缺少注册的手机号码的用户。

![](../assets/workflow-split-example.png)
