---
title: 决策用例
description: 了解如何使用基于代码的渠道的实验创建决策
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
exl-id: 09770df2-c514-4217-a71b-e31c248df543
source-git-commit: aa0791b7ca3eb4c39f700fbe23937b5529f44376
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 5%

---

# 决策用例 {#experience-decisioning-uc}

此用例展示了将Decisioning用于基于[!DNL Journey Optimizer]代码的渠道所需的所有步骤。

在此示例中，您不确定特定排名公式的性能是否优于预先分配的选件优先级。 要测量哪个选项对目标受众的效果最佳，可使用[内容实验](../content-management/content-experiment.md)创建营销活动，其中定义了两种投放处理：

* 第一个处理使用优先级作为排名方法。
* 第二种处理方法使用公式作为排名方法。

## 创建选择策略

首先，需要构建两种选择策略：一种使用优先级作为排名方法，另一种使用公式作为排名方法。

>[!NOTE]
>
>您还可以创建单个决策项目，而无需运行选择策略。 将为每个项目设置的优先级将适用。

### 使用优先级创建策略

要构建优先级为排名方法的第一个选择策略，请执行以下步骤。

1. 创建决策项。 [了解如何操作](items.md)

1. 将决策项的&#x200B;**[!UICONTROL Priority]**&#x200B;设置为与其他项相比。 如果配置文件符合多个项目的条件，则较高的优先级会授予该项目优先于其他项目的权限。

   ![](assets/exd-uc-item-priority.png){width="80%"}

   >[!NOTE]
   >
   >优先级是integer数据类型。 整数数据类型的所有属性都应包含整数值（无小数）。

1. 设置决策项目的资格：

   * 定义受众或规则，将项目限制为仅访问特定用户档案。 [了解详情](items.md#eligibility)

   * 设置上限规则以定义可显示优惠的最大次数。 [了解详情](items.md#capping)

1. 如果需要，请重复上述步骤以创建其他决策项目。

1. 创建包含决策项的&#x200B;**收藏集**。 [了解详情](collections.md)

1. 创建[选择策略](selection-strategies.md#create-selection-strategy)并选择包含要考虑的选件的[收藏集](collections.md)。

1. [选择排名方法](#select-ranking-method)，用于为每个配置文件选择最佳选件。 在这种情况下，选择&#x200B;**[!UICONTROL 优惠优先级]**：如果多个优惠符合此策略的条件，则决策引擎将在优惠中使用设置为&#x200B;**[!UICONTROL 优先级]**&#x200B;的值。 [了解详情](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png){width="80%"}

### 使用公式创建另一个策略

要构建第二个选择策略，并选择公式作为排名方法，请执行以下步骤。

1. 创建决策项。 [了解如何操作](items.md)

   <!--Do you need to set the same **[!UICONTROL Priority]** as for the first decision item, or it won't be considered at all?-->

1. 设置决策项目的资格：

   * 定义受众或规则，将项目限制为仅访问特定用户档案。 [了解详情](items.md#eligibility)

   * 设置上限规则以定义可显示优惠的最大次数。 [了解详情](items.md#capping)

1. 如果需要，请重复上述步骤以创建其他决策项目。

1. 创建包含决策项的&#x200B;**收藏集**。 [了解详情](collections.md)

1. 创建[选择策略](selection-strategies.md#create-selection-strategy)并选择包含要考虑的选件的[收藏集](collections.md)。

1. [选择要用于为每个配置文件选择最佳选件的排名方法](#select-ranking-method)。 在这种情况下，选择&#x200B;**[!UICONTROL 公式]**&#x200B;以使用特定的计算分数来确定要投放的合格优惠。 [了解详情](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png)

## 构建基于代码的体验营销活动

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

配置两个选择策略后，请创建一个基于代码的体验营销活动，其中为每个策略定义不同的处理方式，以便比较哪个策略的表现最佳。

1. 创建营销活动，然后选择&#x200B;**[!UICONTROL 基于代码的体验]**&#x200B;操作。 [了解详情](../code-based/create-code-based.md)

1. 在营销活动摘要页面中，单击&#x200B;**[!UICONTROL 创建试验]**&#x200B;以开始配置内容试验。 [了解详情](../content-management/content-experiment.md)

   ![](assets/exd-uc-create-experiment.png){width="80%"}

1. 从营销活动摘要页面中，选择基于代码的配置，然后单击&#x200B;**[!UICONTROL 编辑内容]**。

   ![](assets/exd-uc-edit-cbe-content.png){width="80%"}

1. 在内容版本窗口中，要开始个性化&#x200B;**处理A**，请单击&#x200B;**[!UICONTROL 编辑代码]**。

   ![](assets/exd-uc-experiment-treatment-a.png){width="80%"}

1. 从[代码编辑器](../code-based/create-code-based.md#edit-code)中，选择&#x200B;**[!UICONTROL 决策策略]**，单击&#x200B;**[!UICONTROL 添加决策策略]**&#x200B;并填写决策详细信息。 [了解详情](create-decision.md#add)

   ![](assets/decision-code-based-create.png)

1. 在&#x200B;**[!UICONTROL 策略序列]**&#x200B;部分中，单击&#x200B;**[!UICONTROL 添加]**&#x200B;按钮，然后选择&#x200B;**[!UICONTROL 选择策略]**。 [了解详情](create-decision.md#select)

   ![](assets/decision-code-based-strategy-sequence.png){width="80%"}

   >[!NOTE]
   >
   >您还可以选择&#x200B;**[!UICONTROL 决策项]**&#x200B;来添加单个项，而无需通过选择策略运行。 将为每个项目设置的优先级将适用。

1. 选择您创建的第一个策略。

   ![](assets/exd-uc-experiment-strategy-priority.png){width="80%"}

1. 保存更改并单击&#x200B;**[!UICONTROL 创建]**。 新决策已添加到&#x200B;**[!UICONTROL 决策策略]**&#x200B;下。

1. 单击&#x200B;**[!UICONTROL 插入策略]**&#x200B;按钮。 将添加与决策策略对应的代码。 然后，将您需要的所有属性（包括配置文件属性）添加到代码。 [了解详情](create-decision.md#use-decision-policy)

   ![](assets/exd-uc-experiment-insert-policy.png){width="80%"}

1. 保存更改。

1. 返回内容编辑窗口，选择+按钮以添加&#x200B;**处理B**，选择它并单击&#x200B;**[!UICONTROL 编辑代码]**。

   ![](assets/exd-uc-experiment-treatment-b.png){width="80%"}

1. 重复上述步骤以创建另一个决策策略并选择您创建的第二个选择策略。<!--Do you need to create exactly the same content to compare only the ranking method?-->

1. 保存更改并[发布基于代码的体验营销活动](../code-based/publish-code-based.md)。

您可以使用[试验性营销活动报告](../reports/campaign-global-report-cja-experimentation.md)和[决策报告](cja-reporting.md)来跟踪营销活动的执行情况。<!--TBC how to check which treatment performs best-->