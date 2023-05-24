---
title: 创建优惠的关键步骤
description: 探索创建选件所需的关键步骤
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 13%

---

# 创建和管理优惠的关键步骤 {#key-steps-to-manage-offers}

建立、設定和管理優惠以及在決定中使用優惠的主要步驟如下所示。

![](../assets/offer-create-manage-process.png)

如需顯示如何設定優惠方案的完整端對端範例、在決定中使用優惠方案，並在電子郵件中利用此決定，請檢視 [此頁面](../offers-e2e.md).

## 创建组件 {#create-components}

在開始建立優惠方案之前，您必須定義幾個要用於優惠方案的元件。

1. **建立版位**，此容器會用來展示您的優惠方案。 例如，您可以建立專屬於影像格式之優惠方案的版位，並位於訊息頂端。

1. **建立決定規則** 會指定提供優惠的條件。

1. **建立集合限定詞** （先前稱為「標籤」）可讓您關聯至優惠方案，輕鬆加以整理並在資料庫中搜尋。

1. 如果您想要定義規則，以決定應先針對指定位置顯示哪個優惠方案（而不是考慮優惠方案的優先順序分數），您可以 **建立排名公式**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">创建投放位置</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">创建决策规则</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">创建标记</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../ranking/create-ranking-formulas.md">创建排名公式</a></p></td>
</table>

## 创建和管理优惠 {#create-and-manage-offers}

1. **建立優惠方案**，並設定其內容和屬性。

1. **建立遞補優惠**，如果客戶不符合任何選定優惠方案的資格，這是最後要顯示的優惠方案。

1. **建立集合** 將您建立的個人化優惠納入決策中，並使用這些優惠。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">建立優惠方案</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">创建后备优惠</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">创建收藏集</a></p></td></tr>
</table>

## 建立及設定決定 {#create-and-configure-decisions}

1. **建立決定** 此維度會將刊登版位與個人化優惠和遞補優惠結合在一起。 決策引擎將使用此組合來尋找特定設定檔的最佳選件。

1. **設定決定**. 若要這麼做，請選取版位，並針對每個版位，選取集合和備援。

1. 如有需要，您可以 **指派排名公式** 至某個版位。

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">创建决策</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">設定決定</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">指派排名</a></p></td>
</tr>
</table>
