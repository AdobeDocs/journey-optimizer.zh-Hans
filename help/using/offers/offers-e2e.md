---
title: 在電子郵件中使用個人化優惠
description: 探索一个端到端示例，其中显示配置选件和在电子邮件中使用它们所需的所有步骤。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 851d988a-2582-4c30-80f3-b881d90771be
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '1095'
ht-degree: 6%

---

# 用例：配置个性化优惠并将其添加到电子邮件中 {#configure-add-personalized-offers-email}

本節提供端對端範例，說明如何根據您先前建立的決定，設定優惠方案並在電子郵件中使用。

## 主要步驟 {#main-steps}

設定優惠（包含在決定中）並在電子郵件中運用此決定的關鍵步驟如下：

1. 建立優惠方案之前， [定義您的元件](#define-components)

   * 创建投放位置
   * 创建决策规则
   * 创建收藏集限定符 （先前稱為「標籤」）
   * 建立排名（選擇性）

1. [設定優惠方案](#configure-offers)

   * 建立優惠方案
   * 對於每個選件：

      * 建立表示，並為每個表示選取版位和資產
      * 為每個選件新增規則
      * 定義每個優惠方案的優先順序

1. [创建后备优惠](#create-fallback)

1. [建立集合](#create-collection) 以包含您建立的個人化優惠方案

1. [設定決定](#configure-decision)

   * 创建决策
   * 選取您建立的版位
   * 針對每個位置，選取集合
   * 選取每個位置的排名（選擇性）
   * 選取遞補內容

1. [在電子郵件中插入決定](#insert-decision-in-email)

   * 選取符合您要顯示之優惠方案的位置
   * 從與所選位置相容的專案中選取決定
   * 預覽您的優惠方案

在電子郵件中使用優惠方案的整體決定管理程式可描述如下：

![](assets/offers-e2e-process.png)

## 定義元件 {#define-components}

在開始建立優惠方案之前，您必須定義幾個要用於優惠方案的元件。

您會在 **[!UICONTROL 決定管理]** > **[!UICONTROL 元件功能表]**.

1. 從建立開始 **位置** 以取得優惠。

   您將使用這些版位來定義定義定義優惠決定時，產生的優惠將顯示在何處。

   在此範例中，使用下列頻道和內容型別建立三個版位：

   * *網頁 — 影像*
   * *電子郵件 — 影像*
   * *非數位 — 文字*

   ![](assets/offers-e2e-placements.png)

   建立刊登版位的詳細步驟已說明，請參閱 [本節](../../using/offers/offer-library/creating-placements.md).

1. 建立 **決定規則**.

   決定規則將為Adobe Experience Platform中的設定檔提供最佳優惠。

   使用設定兩個簡單規則 **[!UICONTROL XDM個人設定檔>人員>性別]** 屬性：

   * *女性客戶*
   * *男性客戶*

   ![](assets/offers-e2e-rules.png)

   建立規則的詳細步驟如下所述： [本節](../../using/offers/offer-library/creating-decision-rules.md).

1. 您也可以建立 **集合限定詞**.

   然後，您就可以將其與優惠方案建立關聯，並使用此集合限定詞將優惠方案群組在一起，形成一個集合。

   在此範例中，建立 *瑜伽* 集合限定詞。

   ![](assets/offers-e2e-tag.png)

   建立集合限定詞的詳細步驟如下所述： [本節](../../using/offers/offer-library/creating-tags.md).

1. 如果您想要定義規則，以決定應先針對指定位置顯示哪個優惠方案（而不是考慮優惠方案的優先順序分數），您可以建立 **排名公式**.

   建立排名公式的詳細步驟如下所述： [本節](../../using/offers/ranking/create-ranking-formulas.md#create-ranking-formula).

   >[!NOTE]
   >
   >在此範例中，我們將僅使用優先順序分數。 進一步瞭解 [適用性規則和限制](../../using/offers/offer-library/creating-personalized-offers.md#eligibility).

## 配置优惠 {#configure-offers}

您現在可以建立和設定優惠方案。 在此範例中，您將根據每個特定設定檔建立四個要顯示的選件。

1. 创建选件. 有关详细信息，请参阅[此部分](../../using/offers/offer-library/creating-personalized-offers.md#create-offer)。

1. 在此選件中，建立三種宣告。 每個表示都必須是您先前建立的版位與資產的組合：

   * 對應至 *網頁 — 影像* 刊登
   * 對應至 *電子郵件 — 影像* 刊登
   * 對應至 *非數位 — 文字* 刊登

   >[!NOTE]
   >
   >優惠方案可顯示在訊息中的不同位置，以創造更多機會，以便在不同的版位內容中使用優惠方案。

   進一步瞭解中的代表 [本節](../../using/offers/offer-library/creating-personalized-offers.md#representations).

1. 為前兩個版位選取適當的影像。 輸入自訂文字 *非數位 — 文字* 位置。

   ![](assets/offers-e2e-representations.png)

1. 在 **[!UICONTROL 優惠資格]** 區段，選取 **[!UICONTROL 依定義的決定規則]** 並拖放您選擇的規則。

   ![](assets/offers-e2e-eligibility.png)

1. 填寫 **[!UICONTROL 優先順序]**. 在此範例中，新增 *25*.

1. 檢閱您的選件，然後按一下 **[!UICONTROL 儲存並核准]**.

   ![](assets/offers-e2e-review.png)

1. 在此範例中，再建立三個具有相同表示但不同資產的優惠方案。 以不同的規則和優先順序指派他們，例如：

   * 第一個優惠 — 決定規則： *女性客戶*，優先順序： *25*
   * 第二個優惠 — 決定規則： *女性客戶*，優先順序： *15*
   * 第三個優惠 — 決定規則： *男性客戶*，優先順序： *25*
   * 第四個優惠 — 決定規則： *男性客戶*，優先順序： *15*

   ![](assets/offers-e2e-offers-created.png)

建立和設定優惠方案的詳細步驟已詳述於 [本節](../../using/offers/offer-library/creating-personalized-offers.md).

## 创建后备优惠 {#create-fallback}

1. 创建后备优惠.

1. 使用適當的資產，定義與優惠方案相同的表示（資產應與優惠方案中使用的資產不同）。

   每個表示都必須是您先前建立的版位與資產的組合：

   * 對應至 *網頁 — 影像* 刊登
   * 對應至 *電子郵件 — 影像* 刊登
   * 對應至 *非數位 — 文字* 刊登

   ![](assets/offers-e2e-fallback-representations.png)

1. 檢閱您的遞補優惠，然後按一下 **[!UICONTROL 儲存並核准]**.

![](assets/offers-e2e-fallback.png)

您的遞補優惠現在已準備好用於決定中。

建立和設定遞補優惠方案的詳細步驟已說明，請參閱 [本節](../../using/offers/offer-library/creating-fallback-offers.md).

## 创建收藏集 {#create-collection}

設定決定時，您需要將個人化優惠新增為集合的一部分。

1. 若要加快決策流程，請建立動態集合。

1. 使用 *瑜伽* 集合限定詞，以選取您先前建立的四個個人化優惠方案。

   ![](assets/offers-e2e-collection-using-tag.png)

建立集合的詳細步驟如下所述： [本節](../../using/offers/offer-library/creating-collections.md).

## 設定決定 {#configure-decision}

現在您必須建立決定，將刊登版位與您剛建立的個人化優惠和遞補優惠結合使用。

決策引擎將使用此組合來尋找特定設定檔的最佳優惠方案：在此範例中，它會根據您指派給每個優惠方案的優先順序和決策規則。

若要建立並設定優惠決定，請遵循下列主要步驟：

1. 创建决策. 有关详细信息，请参阅[此部分](../../using/offers/offer-activities/create-offer-activities.md#create-activity)。

1. 選取 *網頁 — 影像*， *電子郵件 — 影像* 和 *非數位 — 文字* 位置。

   ![](assets/offers-e2e-decision-placements.png)

1. 對於每個位置，新增您建立的集合。

   ![](assets/offers-e2e-decision-collection.png)

1. 如果您在以下情況下定義排名： [建置元件](#define-components)，您可以將其指派給決定中的版位。 如果有多個優惠方案符合在此位置中顯示的資格，決策會使用此公式來計算要先傳送哪個優惠方案。

   將排名公式指派至位置的詳細步驟如下所述： [本節](../../using/offers/offer-activities/configure-offer-selection.md#assign-ranking-formula).

1. 選取您建立的遞補優惠。 它將顯示為三個所選位置的可用遞補優惠。

   ![](assets/offers-e2e-decision-fallback.png)

1. 檢閱您的決定，然後按一下 **[!UICONTROL 儲存並核准]**.

   ![](assets/offers-e2e-review-decision.png)

您的決定現在已準備好用於提供最佳化和個人化優惠。

建立及設定決策的詳細步驟已說明，請參閱 [本節](../../using/offers/offer-activities/create-offer-activities.md).

## 在電子郵件中插入決定 {#insert-decision-in-email}

現在您的決定已上線，您可以將其插入電子郵件訊息。 若要這麼做，請遵循中詳述的步驟 [此頁面](../../using/email/add-offers-email.md).

![](assets/offers-e2e-offers-displayed.png)
