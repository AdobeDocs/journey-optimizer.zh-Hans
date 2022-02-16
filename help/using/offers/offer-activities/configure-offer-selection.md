---
title: 在决策中配置优惠选择
description: 了解如何在决策中管理选件选择
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: 77d7694524eaca447f0cf4e19881f1688fc4e789
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 4%

---

# 在决策中配置优惠选择 {#offers-selection-in-decisions}

如果多个选件符合给定版面的条件，您可以在配置决策时选择为每个用户档案选择最佳选件的方法。 您可以按以下方式对选件进行排名：
* 选件优先级
* 排名公式
* [人工智能排名](#use-ranking-strategy) （仅供选定用户抢先访问）

![](../../assets/offer-rank-by.png)

## 选件优先级 {#offer-priority}

默认情况下，当多个选件符合在决策中放置给定版面的条件时，具有最高级别的选件 **优先级** 会先送给客户。

![](../../assets/offer-priority.png)

创建选件时会分配选件的优先级分数。 了解如何在 [此部分](../offer-library/creating-personalized-offers.md).

## 排名公式 {#assign-ranking-formula}

除了选件优先级之外，Journey Optimizer还允许您创建 **排名公式**. 这些公式可确定在给定版面中应首先显示哪个选件，而不是考虑选件的优先级得分。

例如，您可以提升结束日期现在后不到24小时的所有选件的优先级，或者如果用户档案的目标点为“正在运行”，则提升“正在运行”类别中的选件。

了解如何在中创建排名公式 [此部分](../offer-library/create-ranking-formulas.md).

创建排名公式后，可将其分配给决策中的版面。 为此，请执行以下步骤：

1. 创建决策或编辑现有决策。 请参阅[创建决策](../offer-activities/create-offer-activities.md)。

1. 添加将包含您的选件的版面。 请参阅 [创建版面](../offer-library/creating-placements.md).

1. 为每个版面添加一个收藏集。 请参阅 [创建收藏集](../offer-library/creating-collections.md).

1. 选择 **[!UICONTROL Ranking formula]** 作为排名方法，然后单击 **[!UICONTROL Add ranking]**.

   ![](../../assets/offer-activity-ranking.png)

1. 选择所需的排名公式，然后单击 **[!UICONTROL Select]**.

   ![](../../assets/ranking-selection.png)

排名公式现在与版面相关联。

如果多个选件符合在此版面中显示的条件，则决策将使用排名公式的公式来计算要先交付的选件。

## 人工智能排名 {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->

您还可以使用经过培训的模型系统，通过选择排名策略自动对选件进行排名以显示给定用户档案。 了解如何在 [此部分](../offer-library/create-ranking-strategies.md).

>[!CAUTION]
>
>目前，只能对选定用户提前访问AI排名。

创建排名策略后，可将其分配给决策中的版面。 为此，请执行以下步骤：

1. 创建决策或编辑现有决策。 请参阅[创建决策](../offer-activities/create-offer-activities.md)。

1. 添加将包含您的选件的版面。 请参阅 [创建版面](../offer-library/creating-placements.md).

1. 为每个版面添加一个收藏集。 请参阅 [创建收藏集](../offer-library/creating-collections.md).

1. 选择对选件进行排名 **[!UICONTROL AI ranking]** 从下拉列表中，单击 **[!UICONTROL Add ranking]**.

   ![](../../assets/ranking-selection-ai-ranking.png)

1. 选择您创建的排名策略。 将显示排名策略的所有详细信息。

   ![](../../assets/ranking-selection-ai-ranking-selected.png)

1. 单击 **[!UICONTROL Select]**。排名策略现在与版面相关联。

如果多个选件符合条件，则经过培训的模型系统将确定应首先为给定版面显示哪个选件。

