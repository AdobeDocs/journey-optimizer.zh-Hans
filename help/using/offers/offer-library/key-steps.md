---
title: 创建优惠的关键步骤
description: 探索创建选件所需的关键步骤。
feature: 优惠
topic: 集成
role: User
level: Intermediate
source-git-commit: 5631a1937b854c3e14d1816df9e8d30690588303
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 11%

---

# 创建和管理选件的关键步骤{#key-steps}

创建、配置和管理选件以及在决策中使用这些选件的主要步骤如下所示。

![](../../assets/offer-create-manage-process.png)

有关完整的端到端示例，说明如何配置选件、在决策中使用它们并在电子邮件中利用此决策，请查看[此页面](../offers-e2e.md)。

## 创建组件

在开始创建选件之前，您必须定义要在选件中使用的多个组件。

1. **创建版面**，这些容器将用于展示选件。例如，您可以创建一个仅以图像格式专用于选件的版面，该版面位于消息顶部。

1. **创建决** 策规则，以指定将根据哪些条件显示选件。

1. **创** 建要与选件关联的标记，以便轻松地将选件组织并搜索到库中。

1. 如果要定义规则以确定应首先为给定版面显示哪个选件（而不是考虑选件的优先级得分），则可以&#x200B;**创建排名公式**。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">创建投放位置</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">创建决策规则</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">创建标记</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../offer-library/create-ranking-formulas.md">创建排名公式</a></p></td>
</table>

## 创建和管理优惠

1. **创建选件**，并配置其内容和属性。

1. **创建备用选件**，如果客户不符合任何选定选件的资格，这是最后显示的选件。

1. **创建收** 藏集，以包含您创建的个性化选件并在决策中使用它们。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">创建选件</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">创建后备优惠</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">创建收藏集</a></p></td></tr>
</table>

## 创建和配置决策

1. **创建一** 个决策，将版面与个性化选件和后备选件结合使用。offer decisioning引擎将使用此组合来查找特定用户档案的最佳选件。

1. **配置决策**。为此，请选择版面，然后为每个版面选择一个收藏集和一个回退。

1. 如果需要，您可以在配置决策时，**为版面分配排名公式**。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">创建决策</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">配置决策</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">分配排名</a></p></td>
</tr>
</table>
