---
title: 创建选择策略
description: 了解如何创建选择策略
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="有限发布版"
exl-id: 1b73b398-050a-40bb-a8ae-1c66e3e26ce8
source-git-commit: f586d2de34939c1cd105c26dc64c656c1f0fb990
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 20%

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

选择策略可重复使用，并且包括与资格限制关联的集合以及确定在中选择时显示的优惠的排名方法 [决策策略](create-decision.md).

## 访问和管理选择策略

1. 转到 **[!UICONTROL Experience Decisioning]** > **[!UICONTROL 策略设置]** > **[!UICONTROL 选择策略]**.

1. 将列出迄今为止创建的所有选择策略。 过滤器可帮助您根据排名方法检索策略。

   ![](assets/strategy-list-filters.png)

1. 单击选择策略名称对其进行编辑。

1. 此外，还会显示针对每个策略选择的集合、排名方法和资格。 您可以单击每个收藏集名称旁边的图标以直接编辑收藏集。

   ![](assets/strategy-list-edit-collection.png)

## 创建选择策略

要创建选择策略，请执行以下步骤。

1. 从 **[!UICONTROL 选择策略]** 库存，单击 **[!UICONTROL 创建选择策略]**.

   ![](assets/strategy-create-button.png)

1. 为策略添加名称。

   >[!NOTE]
   >
   >当前仅默认 **[!UICONTROL 选件]** 目录可用。

1. 填写选择策略的详细信息，从名称开始。

   ![](assets/strategy-create-screen.png)

1. 选择 [收藏集](collections.md) 包含要考虑的选件。

1. 使用 **[!UICONTROL 资格]** 用于限制此选择策略的选件选择的字段。

   ![](assets/strategy-create-eligibility.png)

   * 要将优惠选择限制为Experience Platform受众的成员，请选择 **[!UICONTROL 受众]** 并从列表中选择一个受众。 [了解如何使用受众](../audience/about-audiences.md)

   * 如果要为决策规则添加选择约束，请使用 **[!UICONTROL 决策规则]** 选项并选择您选择的规则。 [了解如何创建规则](rules.md)

1. 定义要用于为每个用户档案选择最佳选件的排名方法。 [了解详情](#select-ranking-method)

   ![](assets/strategy-create-ranking.png)

   * 默认情况下，如果多个选件符合此策略的条件， [优惠优先级](#offer-priority) 方法使用在选件中定义的值。

   * 如果要使用特定的计算得分来选择要交付的合格优惠，请选择 [公式](#ranking-formula) 或 [AI模型](#ai-ranking).

1. 单击&#x200B;**[!UICONTROL 创建]**。它现在已准备好用于 [决策策略](create-decision.md)

## 选择排名方法 {#select-ranking-method}

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_ranking"
>title="定义如何为优惠排名"
>abstract="如果多个选件符合给定选择策略的条件，请在创建选择策略时，选择将为每个轮廓选择最佳选件的方法：优先级或排名公式。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/decisioning/experience-decisioning/create-decision.html" text="创建决策策略"

如果多个选件符合给定的选择策略的条件，则可以在创建选择策略时，选择为每个用户档案选择最佳选件的方法。 您可以通过以下方式排列选件：

* [优惠优先级](#offer-priority)
* [公式](#ranking-formula)
* [人工智能排名](#ai-ranking)

### 优惠优先级 {#offer-priority}

默认情况下，当多个优惠符合决策策略中的给定投放位置资格时，具有最高投放位置的项目 **优先级** 将首先交付给客户。

![](assets/item-priority.png)

创建时分配优惠的优先级分数 [决策项目](items.md).

### 排名公式 {#ranking-formula}

除了选件优先级之外，Journey Optimizer还允许您创建 **排名公式**. 这些公式决定应首先为给定投放位置显示哪项优惠，而不是考虑优惠的优先级评分。

例如，您可以提升结束日期距现在不到24小时的所有选件的优先级，或者，如果用户档案的兴趣点为“正在运行”，则提升“正在运行”类别中的选件。 了解如何在中创建排名公式 [本节](ranking.md).

创建后，您可以在选择策略中使用此公式。 使用此选择策略时，如果多个优惠都符合呈现的条件，决策将使用选定的公式计算首先要投放哪个优惠。

### 人工智能排名 {#ai-ranking}

您还可以使用经过训练的模型系统，该系统通过选择人工智能模型自动对要针对给定用户档案显示的选件进行排名。 了解如何在中创建AI模型 [本节](ranking.md).

创建AI模型后，您可以在选择策略中使用该模型。 如果多个选件符合条件，则经过训练的模型系统将确定应首先为此选择策略提供哪个选件。
