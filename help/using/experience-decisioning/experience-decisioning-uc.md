---
title: 决策用例
description: Learn how to create decisions using experiments with the code-based channel
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
exl-id: 09770df2-c514-4217-a71b-e31c248df543
source-git-commit: 83ad828a4d342bba10284cdd20d22eb325e3e1f7
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 7%

---

# 决策用例 {#experience-decisioning-uc}

This use case presents all the steps needed to use Decisioning with the [!DNL Journey Optimizer] code-based channel.

<!--In this use case, you create a campaign where you define two delivery treatments - each containing a different decision policy in order to measure which one performs best for your target audience.-->

In this use case, you are unsure if a specific ranking formula will perform better than the pre-assigned offer priorities.

To measure which one performs best for your target audience, create a campaign where you define two delivery treatments:

<!--Set up the experiment such that:-->

* The first treatment contains one selection strategy with priority as the ranking method.
* The second treatment contains a different selection strategy for which a formula is the ranking method.

## 创建选择策略

First, you need to build two selection strategies: one with priority as the ranking method, and another one with a formula as the ranking method.

### 创建第一个选择策略

在第一个选择策略中，选择优先级作为排名方法。 请按照以下步骤操作。

1. 创建决策项。 [了解如何操作](items.md)

1. 将决策项的&#x200B;**[!UICONTROL Priority]**&#x200B;设置为与其他项相比。 如果配置文件符合多个项目的条件，则较高的优先级会授予该项目优先于其他项目的权限。

   ![](assets/exd-uc-item-priority.png)

   >[!NOTE]
   >
   >优先级是integer数据类型。 整数数据类型的所有属性都应包含整数值（无小数）。

1. 定义受众或规则，将项目限制为仅访问特定用户档案。 [了解如何设置决策项的资格](items.md#eligibility)

1. 设置上限规则以定义可显示优惠的最大次数。 [了解如何操作](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. 创建包含决策项的&#x200B;**收藏集**。 [了解详情](collections.md)

1. Create a **selection strategy**. [了解如何操作](selection-strategies.md#create-selection-strategy)

1. Select the [collection](collections.md) that contains the offer(s) to consider.

1. [Choose the ranking method](#select-ranking-method) to use to select the best offer for each profile. In this case, select **[!UICONTROL Offer priority]**. [了解详情](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png)

   <!--If multiple offers are eligible for this strategy, the [Offer priority](#offer-priority) method uses the value defined in the offers.-->

### Create the second selection strategy

In the second selection strategy, select a formula as the ranking method. 请按照以下步骤操作。

1. Create a decision item. [了解如何操作](items.md)

<!--1. Set the same **[!UICONTROL Priority]** as for the first decision item. TBC?-->

1. Define audiences or rules to restrict the item to specific profiles only. [Learn how to set the decision item&#39;s eligibility](items.md#eligibility)

1. Set capping rules to define the maximum number of times an offer can be presented. [了解如何操作](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. 创建包含决策项的&#x200B;**收藏集**。 [了解详情](collections.md)

1. 创建&#x200B;**选择策略**。 [了解如何操作](selection-strategies.md#create-selection-strategy)

1. 选择包含要考虑的选件的[收藏集](collections.md)。

1. [选择要用于为每个配置文件选择最佳选件的排名方法](#select-ranking-method)。 在这种情况下，选择&#x200B;**[!UICONTROL 公式]**&#x200B;以使用特定的计算得分来选择要投放的合格优惠。 [了解详情](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png)

<!--
## Create decision items and selection strategies

You first need to create items, group them together in collections, set up rules and ranking methods. These elements will allow you to build selection strategies.

1. Navigate to **[!UICONTROL Decisioning]** > **[!UICONTROL Catalogs]** and create several decision items. Set constraints using audiences or rules to restrict each item to specific profiles only. [Learn more](items.md)

1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)

1. Create **collections** to categorize and group your decision items according to your preferences. [Learn more](collections.md)

1. Create **decision rules** to determine to whom a decision item can be shown. [Learn more](rules.md)

1. Create **ranking methods** and apply them within decision strategies to determine the priority order for selecting decision items. [Learn more](ranking.md)

1. Build **selection strategies** that leverage collections, decision rules, and ranking methods to identify the decision items suitable for displaying to profiles. [Learn more](selection-strategies.md)
-->

## 创建决策策略

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

1. 创建营销活动，然后选择&#x200B;**[!UICONTROL 基于代码的体验]**&#x200B;操作。 [了解详情](../code-based/create-code-based.md)

1. 从&#x200B;**[!UICONTROL 编辑内容]**&#x200B;窗口，开始个性化处理A。

1. 选择&#x200B;**[!UICONTROL 决策]**&#x200B;图标，单击&#x200B;**[!UICONTROL 创建决策]**&#x200B;并填写决策详细信息。 [了解详情](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Select the first strategy that you created. Click **[!UICONTROL Add strategy]**.

1. 单击&#x200B;**[!UICONTROL 创建]**。The new decision is added under **[!UICONTROL Decisions]**.

   ![](assets/decision-code-based-decision-added.png)

1. Click the more actions icon (three dots) and select **[!UICONTROL Add]**. Now you can add all the decision attributes you want inside this.

   ![](assets/decision-code-based-add-decision.png)

1. You can also add any other attribute available in the personalization editor, such as profile attributes.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. 在营销活动摘要页面中，单击&#x200B;**[!UICONTROL 创建试验]**&#x200B;以开始配置内容试验。 [了解详情](../content-management/content-experiment.md)

1. 从&#x200B;**[!UICONTROL 编辑内容]**&#x200B;窗口中，选择处理B ，然后重复上述步骤以创建另一个决策。

1. 选择您创建的第二个策略。 单击&#x200B;**[!UICONTROL 添加策略]**。

1. 保存您的内容。
