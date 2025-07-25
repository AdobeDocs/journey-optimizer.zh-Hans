---
title: 创建产品建议的关键步骤
description: 探索创建产品建议所需的关键步骤
badge: label="旧版" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 87f3da0a1d73f9aa26c7420d260778286bacdf0c
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 7%

---

# 创建和管理优惠的关键步骤 {#key-steps-to-manage-offers}

下面介绍了创建、配置和管理优惠以及在决策中使用优惠的主要步骤。

![](../assets/offer-create-manage-process.png)

如需一个完整的端到端示例，说明如何配置优惠、在决策中使用优惠并在电子邮件中利用此决策，请查看[此页面](../offers-e2e.md)。

## 创建组件 {#create-components}

在开始创建选件之前，必须定义将在选件中使用的多个组件。

1. [创建投放位置](creating-placements.md)，投放位置是将用于展示优惠的容器。 例如，您可以创建一个投放位置，该投放位置将仅用于图像格式的选件，并位于消息顶部。

1. [创建决策规则](creating-decision-rules.md)，以指定提供优惠的条件。

1. [创建要关联到选件的收藏集限定符](creating-tags.md)（以前称为“标记”），从而允许您轻松地将其整理并搜索到库中。

1. 如果要定义规则以确定在给定投放位置应首先显示哪个优惠（而不是考虑优惠的优先级分数），则可以[创建排名公式](../ranking/create-ranking-formulas.md)。

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Create placements</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Create decision rules</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Create collection qualifiers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Create ranking formulas</a>
</div>
<p>
</td>
</tr>
</table>
-->

## 创建和管理优惠 {#create-and-manage-offers}

1. [创建选件](creating-personalized-offers.md)，并配置其内容和属性。

1. [创建后备优惠](creating-fallback-offers.md)，如果客户不符合任何选定优惠的资格，则将这些后备优惠作为最后要显示的优惠。

1. [创建收藏集](creating-collections.md)以包含您创建的个性化优惠，并在决策中使用它们。

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Create offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Create fallback offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Create collections</a>
</div>
<p>
</td>
</tr>
</table>
-->

## 创建和配置决策 {#create-and-configure-decisions}

1. [创建将投放位置与个性化优惠和备用优惠相结合的决策](../offer-activities/create-offer-activities.md)。 决策引擎将使用此组合来查找适合特定用户档案的最佳选件。

1. [配置决策](../offer-activities/create-offer-activities.md#add-decision-scopes)。 为此，请选择投放位置，并为每个投放位置选择收藏集和备用。

1. 如果需要，您可以在配置决策时[将排名公式](../offer-activities/configure-offer-selection.md#assign-ranking-formula)或[AI排名](../offer-activities/configure-offer-selection.md#use-ranking-strategy)分配给投放位置。

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Create decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configure decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assign ranking</a>
</div>
<p>
</td>
</tr>
</table>
-->