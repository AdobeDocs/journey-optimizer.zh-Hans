---
title: 在决策中配置优惠选择
description: 了解如何在决策中管理优惠选择。
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# 在决策{#offers-selection-in-activities}中配置优惠选择

## 关于优惠优先级{#about-offers-priority}

默认情况下，当多个优惠有资格在决定中放置给定位置(以前称为优惠活动)时，具有最高&#x200B;**优先级**&#x200B;的优惠将首先交付给客户。 优惠在创建优惠时会分配优先级分数(请参阅[创建个性化优惠](../offer-library/creating-personalized-offers.md))。

![](../../assets/offer-priority.png)

此外，Journey Optimizer还允许您创建&#x200B;**排名公式**。 这些公式决定了在给定位置应首先显示哪些优惠，而不是考虑优惠的优先级得分。 例如，您可以提升结束日期在24小时后的所有优惠的优先级，或者，如果用户档案的兴趣点为“正在运行”，则提升“正在运行”类别的优惠。

有关如何创建排名公式的详细信息，请参阅[本节](../offer-library/create-ranking-formulas.md)。

## 将排名公式分配给位置{#assign-ranking-formula}

一旦创建了排名公式，您就可以将其分配给决策中的版面。 为此，请按照以下步骤操作：

* 创建决策或编辑现有决策，然后创建将包含您的优惠的版面（请参阅[创建决策](../offer-activities/create-offer-activities.md)）。

* 对于每个位置，从下拉列表中选择&#x200B;**[!UICONTROL Ranking]**，然后单击&#x200B;**[!UICONTROL Add ranking]**。

   ![](../../assets/offer-activity-ranking.png)

* 选择所需的排名公式，然后单击&#x200B;**[!UICONTROL Select]**。

   ![](../../assets/ranking-selection.png)

排名公式现在与版面相关联。 如果多个优惠符合在此位置中显示的条件，则该决定将使用排名公式的公式来计算首先传送的优惠。
