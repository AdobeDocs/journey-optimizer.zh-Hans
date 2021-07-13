---
title: 在决策中配置优惠选择
description: 了解如何在决策中管理选件选择。
feature: 优惠
topic: 集成
role: User
level: Intermediate
source-git-commit: 807157d4d6fc1dba018bbe796c8bd213504589dc
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 4%

---

# 在决策中配置优惠选择 {#offers-selection-in-activities}

如果多个选件符合给定版面的条件，您可以在配置决策（以前称为选件活动）时，选择为每个用户档案选择最佳选件的方法。 您可以按以下方式对选件进行排名：
* 选件优先级
* 排名公式

## 选件优先级 {#about-offers-priority}

默认情况下，当多个选件符合在决策中放置给定版面的条件（以前称为选件活动）时，将首先向客户交付具有最高&#x200B;**优先级**&#x200B;的选件。

![](../../assets/offer-priority.png)

创建选件时会分配选件的优先级分数。 了解如何在[此部分](../offer-library/creating-personalized-offers.md)中创建个性化选件。

## 排名公式 {#assign-ranking-formula}

除了选件优先级之外，Journey Optimizer还允许您创建&#x200B;**排名公式**。 这些公式可确定在给定版面中应首先显示哪个选件，而不是考虑选件的优先级得分。

例如，您可以提升结束日期现在后不到24小时的所有选件的优先级，或者如果用户档案的目标点为“正在运行”，则提升“正在运行”类别中的选件。

了解如何在[此部分](../offer-library/create-ranking-formulas.md)中创建排名公式。

创建排名公式后，您可以将其分配给决策中的版面（以前称为选件活动）。 为此，请执行以下步骤：

1. 创建决策或编辑现有决策。 请参阅[创建决策](../offer-activities/create-offer-activities.md)。

1. 添加将包含您的选件的版面。 请参阅[创建版面](../offer-library/creating-placements.md)。

1. 为每个版面添加一个收藏集。 请参阅[创建集合](../offer-library/creating-collections.md)。

1. 从下拉列表中选择按&#x200B;**[!UICONTROL Ranking]**&#x200B;对选件进行排名，然后单击&#x200B;**[!UICONTROL Add ranking]**。

   ![](../../assets/offer-activity-ranking.png)

1. 选择所需的排名公式，然后单击&#x200B;**[!UICONTROL Select]**。

   ![](../../assets/ranking-selection.png)

排名公式现在与版面相关联。

如果多个选件符合在此版面中显示的条件，则决策将使用排名公式的公式来计算要先交付的选件。
