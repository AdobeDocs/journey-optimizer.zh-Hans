---
title: 在决策中配置优惠选择
description: 了解如何在决策中管理选件选择。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8c7135d7-bf5a-4671-afdf-afec60907a56
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 4%

---

# 在决策中配置优惠选择 {#offers-selection-in-activities}

如果多个选件符合给定版面的条件，您可以在配置决策（以前称为选件活动）时，选择为每个用户档案选择最佳选件的方法。 您可以按以下方式对选件进行排名：
* 选件优先级
* 排名公式
* [AI排名](#use-ranking-strategy) （仅供选定用户提前访问）

![](../../assets/offer-rank-by.png)

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

## 人工智能排名 {#use-ranking-strategy}

<!--If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service,-->You can also use an trained model system that automatically ranks offers to display for a given profile by selecting a ranking strategy. Learn how to create a ranking strategy in [this section](../offer-library/create-ranking-strategies.md).

>[!CAUTION]
>
>目前，只能对选定用户提前访问AI排名。

创建排名策略后，您可以将其分配给决策中的版面（以前称为选件活动）。 为此，请执行以下步骤：

1. 创建决策或编辑现有决策。 请参阅[创建决策](../offer-activities/create-offer-activities.md)。

1. 添加将包含您的选件的版面。 请参阅[创建版面](../offer-library/creating-placements.md)。

1. 为每个版面添加一个收藏集。 请参阅[创建集合](../offer-library/creating-collections.md)。

1. 从下拉列表中选择按&#x200B;**[!UICONTROL AI ranking]**&#x200B;对选件进行排名。

   ![](../../assets/ranking-selection-ai-ranking.png)

1. 单击 **[!UICONTROL Add ranking]**。

   ![](../../assets/ranking-selection-ai-ranking-add.png)

1. 选择您创建的排名策略。 将显示排名策略的所有详细信息。

   ![](../../assets/ranking-selection-ai-ranking-selected.png)

1. 单击 **[!UICONTROL Select]**。

排名策略现在与版面相关联。

如果多个选件符合条件，则经过培训的模型系统将确定应首先为给定版面显示哪个选件。

<!--Result? Describe the impact for the user, i.e. what's the effect of selecting this ranking strategy for this collection/placement.-->

<!--Click **[!UICONTROL Next]** to confirm and save your decision.-->
