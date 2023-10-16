---
title: 创建优惠的关键步骤
description: 探索创建选件所需的关键步骤
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: fe295f020934893cbe90ba987742b5f9d3931158
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 13%

---

# 创建和管理优惠的关键步骤 {#key-steps-to-manage-offers}

下面介绍了创建、配置和管理优惠以及在决策中使用优惠的主要步骤。

![](../assets/offer-create-manage-process.png)

要获取一个完整的端到端示例，其中显示如何配置优惠、在决策中使用优惠并在电子邮件中利用此决策，请查看 [此页面](../offers-e2e.md).

## 创建组件 {#create-components}

在开始创建选件之前，必须定义将在选件中使用的多个组件。

1. **创建投放位置**，是用于展示选件的容器。 例如，您可以创建一个投放位置，该投放位置将仅用于图像格式的选件，并位于消息顶部。

1. **创建决策规则** 列明优惠的展示条件。

1. **创建收藏集限定符** （之前称为“标记”）可关联到选件，从而让您轻松地将其整理并搜索到库中。

1. 如果要定义规则以确定在给定投放位置应首先显示哪个优惠（而不是考虑优惠的优先级评分），则可以 **创建排名公式**.

<table style="table-layout:fixed"><tr style="border: 0;">
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">创建投放位置</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">创建决策规则</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">创建标记</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../ranking/create-ranking-formulas.md">创建排名公式</a></p></td>
</tr>
</table>

## 创建和管理优惠 {#create-and-manage-offers}

1. **创建优惠**，并配置其内容和属性。

1. **创建后备优惠**，这是客户没有资格获得任何选定优惠时显示的最后选用优惠。

1. **创建收藏集** 将您创建的个性化优惠包含在决策中使用它们。

<table style="table-layout:fixed"><tr style="border: 0;">
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">创建优惠</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">创建后备优惠</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">创建收藏集</a></p></td>
</tr>
</table>

## 创建和配置决策 {#create-and-configure-decisions}

1. **创建决策** 该功能会将投放位置与个性化优惠和备用优惠相结合。 决策引擎将使用此组合来查找适合特定用户档案的最佳选件。

1. **配置决策**. 为此，请选择投放位置，并为每个投放位置选择收藏集和备用。

1. 如果需要，您可以 **分配排名公式** 到投放位置。

<table style="table-layout:fixed"><tr style="border: 0;">
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">创建决策</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">配置决策</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">分配排名</a></p></td>
</tr>
</table>
