---
title: 创建选择策略
description: 了解如何创建选择策略
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="有限发布版"
exl-id: 1b73b398-050a-40bb-a8ae-1c66e3e26ce8
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 21%

---

# 创建选择策略 {#selection-strategies}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_strategies"
>title="定义您的选择策略"
>abstract="选择策略是一个可重复的项，它由与资格约束和排名方法关联的收藏集组成，以确定在决策策略中选择时要显示的报价。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/create-decision.html" text="创建决策策略"

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_eligibility"
>title="限制符合条件的轮廓"
>abstract="可限制为此选择策略选择优惠。默认情况下，所有轮廓都符合条件，但您可以使用受众或规则将选件选择限制为仅特定轮廓。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html" text="使用受众"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/selection/rules.html" text="使用决策规则"

选择策略可重复使用，并且包括与资格约束关联的集合以及确定在[决策策略](create-decision.md)中选择时显示的优惠的排名方法。

## Access and manage selection strategies

1. ************

1. All the selection strategies created so far are listed. Filters are available to help you retrieve strategies according to the ranking method.

   ![](assets/strategy-list-filters.png)

1. Click a selection strategy name to edit it.

1. The collection, ranking method and eligibility selected for each strategy are also displayed. You can click the icon next to each collection name to directly edit a collection.

   ![](assets/strategy-list-edit-collection.png)

## Create a selection strategy

To create a selection strategy, follow the steps below.

1. 在&#x200B;**[!UICONTROL 选择策略]**&#x200B;清单中，单击&#x200B;**[!UICONTROL 创建选择策略]**。

   ![](assets/strategy-create-button.png)

1. 为策略添加名称。

   >[!NOTE]
   >
   >当前只有默认的&#x200B;**[!UICONTROL 选件]**&#x200B;目录可用。

1. Fill in the details for your selection strategy, starting by the name.

   ![](assets/strategy-create-screen.png)

1. [](collections.md)

1. ****

   ![](assets/strategy-create-eligibility.png)

   * ****[了解如何使用受众](../audience/about-audiences.md)

   * ****[](rules.md)

1. Define the ranking method you want to use to select the best offer for each profile. [了解详情](#select-ranking-method)

   ![](assets/strategy-create-ranking.png)

   * 默认情况下，如果多个选件符合此策略的条件，则[选件优先级](#offer-priority)方法将使用选件中定义的值。

   * 如果要使用特定的计算得分来选择要投放的合格优惠，请选择[公式](#ranking-formula)或[AI模型](#ai-ranking)。

1. 单击&#x200B;**[!UICONTROL 创建]**。现在可在[决策策略](create-decision.md)中使用

## 选择排名方法 {#select-ranking-method}

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_ranking"
>title="定义如何为优惠排名"
>abstract="如果多个选件符合给定选择策略的条件，请在创建选择策略时，选择将为每个轮廓选择最佳选件的方法：优先级或排名公式。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/create-decision.html" text="创建决策策略"

If several offers are eligible for a given selection strategy, you can choose the method that will select the best offer for each profile when creating a selection strategy. You can rank offers by:

* [优惠优先级](#offer-priority)
* [公式](#ranking-formula)
* [人工智能排名](#ai-ranking)

### 优惠优先级 {#offer-priority}

默认情况下，当多个优惠符合决策策略中的给定投放位置条件时，具有最高&#x200B;**优先级**&#x200B;的项目将首先交付给客户。

![](assets/item-priority.png)

[](items.md)

### 排名公式 {#ranking-formula}

除了优惠优先级之外，Journey Optimizer还允许您创建&#x200B;**排名公式**。 这些公式决定应首先为给定投放位置显示哪项优惠，而不是考虑优惠的优先级评分。

例如，您可以提升结束日期距现在不到24小时的所有选件的优先级，或者，如果用户档案的兴趣点为“正在运行”，则提升“正在运行”类别中的选件。 在[本节](ranking.md)中了解如何创建排名公式。

Once created, you can use this formula in a selection strategy. If multiple offers are eligible to be presented when using this selection strategy, the decision will use the selected formula to calculate which offer to deliver first.

### 人工智能排名 {#ai-ranking}

You can also use a trained model system that automatically ranks offers to display for a given profile by selecting an AI model. [](ranking.md)

Once an AI model has been created, you can use it in a selection strategy. If multiple offers are eligible, the trained model system will determine which offer should be presented first for this selection strategy.
