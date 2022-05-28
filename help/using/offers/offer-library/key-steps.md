---
title: 创建优惠的关键步骤
description: 探索创建选件所需的关键步骤
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 13%

---

# 创建和管理优惠的关键步骤 {#key-steps-to-manage-offers}

创建、配置和管理选件以及在决策中使用这些选件的主要步骤如下所示。

![](../assets/offer-create-manage-process.png)

有关完整的端到端示例，请参阅如何配置选件、在决策中使用这些选件以及在电子邮件中利用此决策，以了解 [本页](../offers-e2e.md).

## 创建组件 {#create-components}

在开始创建选件之前，您必须定义要在选件中使用的多个组件。

1. **创建版面**，这些容器将用于显示选件。 例如，您可以创建一个仅以图像格式专用于选件的版面，该版面位于消息顶部。

1. **创建决策规则** 将指定提供选件的条件。

1. **创建标记** 选件关联的URL，从而可以轻松地将选件组织并搜索到库中。

1. 如果您想要定义规则以确定应首先为给定版面显示哪个选件（而不是考虑选件的优先级得分），则可以 **创建排名公式**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">创建投放位置</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">创建决策规则</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">创建标记</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../ranking/create-ranking-formulas.md">创建排名公式</a></p></td>
</table>

## 创建和管理优惠 {#create-and-manage-offers}

1. **创建选件**，并配置其内容和属性。

1. **创建后备优惠**，如果客户不符合任何选定选件的资格，则这是最后显示的选件。

1. **创建收藏集** 以包含您创建的个性化选件并在决策中使用它们。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">创建选件</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">创建后备优惠</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">创建收藏集</a></p></td></tr>
</table>

## 创建和配置决策 {#create-and-configure-decisions}

1. **创建决策** 将版面与个性化选件和备用选件结合使用。 offer decisioning引擎将使用此组合来查找特定用户档案的最佳选件。

1. **配置决策**. 为此，请选择版面，然后为每个版面选择一个收藏集和一个回退。

1. 如果需要，您可以 **分配排名公式** 到投放。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">创建决策</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">配置决策</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">分配排名</a></p></td>
</tr>
</table>
