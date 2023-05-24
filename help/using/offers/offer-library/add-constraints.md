---
title: 將限制新增至優惠方案
description: 瞭解如何定義優惠方案顯示的條件
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7234a8e8-4ab0-4f17-a833-5e452fadac35
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '2357'
ht-degree: 17%

---

# 將限制新增至優惠方案 {#add-constraints}

>[!CONTEXTUALHELP]
>id="od_offer_constraints"
>title="关于优惠约束"
>abstract="通过约束，您可以指定与其他优惠相比，该优惠如何确定优先级并呈现给用户。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_constraints"
>title="关于优惠约束"
>abstract="通过约束，您可以指定与其他优惠相比，该优惠如何确定优先级并呈现给用户。"

>[!CONTEXTUALHELP]
>id="od_offer_priority"
>title="关于优惠优先级"
>abstract="在此字段中，您可以指定优惠的优先级设置。优先级是一个数字，用于对满足所有约束（例如资格、日期和上限）的优惠进行排名。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_priority"
>title="设置优先级"
>abstract="如果用户有资格获得多个优惠，则优先级有助于定义该优惠相对于其他优惠的优先级。优惠的优先级越高，与其他优惠相比其优先级就越高。"

限制可讓您定義優惠的顯示條件。

1. 設定 **[!UICONTROL 優惠資格]**. [了解详情](#eligibility)

   ![](../assets/offer-eligibility.png)

1. 定義 **[!UICONTROL 優先順序]** 相較於其他優惠方案的數量（如果使用者符合多個優惠方案的資格）。 优惠的优先级越高，与其他优惠相比其优先级就越高。

   ![](../assets/offer-priority.png)

1. 指定優惠方案的 **[!UICONTROL 上限]**，表示選件出現的次數。 [了解详情](#capping)

   ![](../assets/offer-capping.png)

1. 按一下 **[!UICONTROL 下一個]** 以確認您所定義的所有限制。

例如，如果您設定下列限制：

![](../assets/offer-constraints-example.png)

* 只有符合「金級忠誠客戶」決策規則的使用者才會考量此優惠。
* 優惠方案的優先順序設為「50」，這表示優惠方案會顯示在優先順序介於1到49之間的優惠方案之前，以及優先順序至少為51的優惠方案之後。
* 所有版位中每個使用者每月僅會顯示一次選件。

## 資格 {#eligibility}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_eligibility"
>title="定义资格"
>abstract="默认情况下，任何配置文件都有资格获得优惠，但您可以使用区段或决策规则将优惠限制为特定的配置文件。"

>[!CONTEXTUALHELP]
>id="od_offer_eligibility"
>title="关于优惠资格"
>abstract="在此部分中，您可以使用决策规则来确定哪些用户有资格享受优惠。"
>additional-url="https://video.tv.adobe.com/v/329373" text="观看演示视频"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_total_profile_estimate"
>title="对配置文件的总体估计"
>abstract="当您选择区段或决策规则时，可以看到有关估计符合资格的配置文件的信息。"

此 **[!UICONTROL 優惠資格]** 區段可讓您將優惠限制在您使用區段或決定規則定義的特定設定檔中。

>[!NOTE]
>
>進一步瞭解使用 **區段** 與 **決定規則** 在 [本節](#segments-vs-decision-rules).

* 根據預設， **[!UICONTROL 所有訪客]** 選項已選取，這表示任何設定檔都符合呈現優惠方案的資格。

   ![](../assets/offer-eligibility-default.png)

* 您也可以將優惠方案的呈現方式限制在一或多個成員中 [Adobe Experience Platform區段](../../segment/about-segments.md).

   若要這麼做，請啟動 **[!UICONTROL 屬於一或多個區段的訪客]** 選項，然後從左窗格新增一或多個區段，並使用 **[!UICONTROL 和]** / **[!UICONTROL 或]** 邏輯運運算元。

   ![](../assets/offer-eligibility-segment.png)

* 如果您想要關聯特定 [決定規則](../offer-library/creating-decision-rules.md) 至選件，選取 **[!UICONTROL 依定義的決定規則]**，然後將所需的規則從左窗格拖曳至 **[!UICONTROL 決定規則]** 區域。

   ![](../assets/offer_rule.png)

   >[!CAUTION]
   >
   >事件型優惠方案目前不支援 [!DNL Journey Optimizer]. 如果您根據以下專案建立決定規則： [事件](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}，您將無法在選件中運用它。

当您选择区段或决策规则时，可以看到有关估计符合资格的配置文件的信息。按一下 **[!UICONTROL 重新整理]** 以更新資料。

![](../assets/offer-eligibility-segment-estimate.png)

>[!NOTE]
>
>當規則引數包含不在設定檔中的資料（例如內容資料）時，設定檔預估不可用。 例如，適用性規則要求目前天氣為≥80度。

### 使用區段與決定規則 {#segments-vs-decision-rules}

若要套用限制，您可以將優惠方案的選取限制在一或多個成員中 **Adobe Experience Platform區段**，或您可以使用 **決定規則**，這兩個解決方案分別對應於不同的使用方式。

基本上，區段的輸出是設定檔清單，而決定規則是在決策流程期間，根據單一設定檔按需執行的函式。 這兩種使用方式的差異詳述如下。

* **区段**

   一方面，區段是一組Adobe Experience Platform設定檔，可根據設定檔屬性和體驗事件符合特定邏輯。 不過，Offer Management不會重新計算區段，因為區段在展示優惠方案時可能不是最新的。

   深入瞭解中的區段 [本節](../../segment/about-segments.md).

* **决策规则**

   另一方面，決定規則會根據Adobe Experience Platform中可用的資料，並決定可向誰顯示優惠方案。 在優惠或指定位置的決定中選取後，每次做出決定時都會執行規則，以確保每個設定檔都能取得最新和最佳優惠。

   進一步瞭解中的決定規則 [本節](creating-decision-rules.md).

## 上限 {#capping}

>[!CONTEXTUALHELP]
>id="od_offer_globalcap"
>title="关于优惠上限"
>abstract="在此字段中，可指定可呈现优惠的次数。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_capping"
>title="使用上限"
>abstract="为避免过度招揽客户，请使用上限定义可呈现优惠的最大次数。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints.html#capping-change-date" text="更改日期可能会影响上限"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping"
>title="设置上限频率"
>abstract="您可以选择每天、每周或每月重置优惠上限计数器。请注意，保存优惠后，您将无法更改所选频率。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_frequency_capping_impression"
>title="印象"
>abstract="仅入站频道可将印象用作上限事件。"

上限會用作限制，以定義可顯示優惠方案的最大次數。

限制使用者取得特定優惠方案的次數，可讓您避免過度向客戶提供需求，進而使用最佳優惠方案最佳化每個接觸點。

若要設定上限，請遵循下列主要步驟。

1. 確定 **[!UICONTROL 包含上限]** 切換按鈕已選取。 預設包含上限。

   >[!CAUTION]
   >
   >無法啟用或停用先前建立之優惠方案的頻率上限。 若要這麼做，您需要複製優惠或建立新優惠。

1. 定義哪些 **[!UICONTROL 事件上限]** 將考慮以增加計數器。 [了解详情](#capping-event)

1. 設定可顯示優惠方案的次數。 [了解详情](#capping-count)

1. 選擇您要將上限套用至所有使用者，還是隻套用一個設定檔。 [了解详情](#capping-type)

1. 設定 **[!UICONTROL 頻率]** 以定義上限計數的重設頻率。 [了解详情](#frequency-capping)

1. 如果您已定義數個 [表示方式](add-representations.md) 針對您的優惠，指定是否要套用上限 **[!UICONTROL 橫跨所有位置]** 或 **[!UICONTROL 針對每個位置]**. [了解详情](#placements)

1. 儲存並核准後，如果優惠方案已根據您定義的條件和時間範圍顯示您在此欄位中指定的次數，則其傳送將停止。

在準備電子郵件時會計算建議某個優惠方案的次數。 例如，如果您准备发送一封包含大量选件的电子邮件，则无论是否发送了这封电子邮件，这些数量都将计入您的最大上限。

<!--If an email delivery is deleted or if the preparation is done again before being sent, the capping value for the offer is automatically updated.-->

>[!NOTE]
>
>優惠方案過期時或優惠方案開始日期後2年（以先到者為準）時，上限計數器會重設。 瞭解如何在中定義優惠方案的日期 [本節](creating-personalized-offers.md#create-offer).

### 事件上限 {#capping-event}

此 **[!UICONTROL 事件上限]** 欄位可讓您定義 **[!UICONTROL 事件上限]** 將考慮以增加計數器：

![](../assets/offer-capping-event.png)

* **[!UICONTROL 決定事件]** （預設值）：可顯示選件的次數上限。
* **[!UICONTROL 印象]**：優惠方案可向使用者顯示的最大次數。

   >[!NOTE]
   >
   >閱聽作為上限事件可供使用 **傳入頻道** 僅限。

* **[!UICONTROL 點按次數]**：使用者可點按選件的次數上限。
* **[!UICONTROL 自訂事件]**：您可以定義自訂事件，用於限制傳送的優惠方案數量。 例如，您可以限制贖回次數，直到它們等於10000，或直到指定的設定檔贖回1次。 若要這麼做，請使用 [ADOBE EXPERIENCE PLATFORM XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"} 用於建立自訂事件規則的結構描述。

   <!--For example, you can cap on the number of redemptions so that the offer can be shown until redemptions equal 10000. You can only select XDM ExperienceEvents. -->

   在以下範例中，您想要限制結帳次數。

   1. 選取 **[!UICONTROL 自訂事件]** 從清單中使用 **[!UICONTROL 新增自訂事件]** 按鈕。

      ![](../assets/offer-capping-custom-event-add.png)

   1. 使用 **[!UICONTROL 建立自訂事件規則]** 產生器以選取相關事件。 您可以選擇要限制優惠方案的任何使用者動作。

      在這裡選擇 **[!UICONTROL 商務]** > **[!UICONTROL 結帳]** > **[!UICONTROL 值]** 並選取 **[!UICONTROL 存在]** 下拉式清單中的。

      ![](../assets/offer-capping-custom-event.png)

   1. 建立規則後，會顯示在 **[!UICONTROL 自訂事件查詢]** 欄位。

      ![](../assets/offer-capping-custom-event-query.png)

>[!CAUTION]
>
>對於決策事件以外的所有上限事件，決策管理意見反應可能不會自動收集，這可能會導致上限計數器無法正確增加。 [了解详情](../data-collection/data-collection.md)
>
>若要確保每個上限事件都受到追蹤並計入上限計數器中，請確定用來收集體驗事件的結構描述包含該事件的正確欄位群組。 [了解详情](../data-collection/schema-requirement.md)

### 上限計數 {#capping-count}

此 **[!UICONTROL 上限計數]** 欄位可讓您指定可顯示選件的次數。

![](../assets/offer-capping-times.png)

>[!NOTE]
>
>數字必須是大於0的整數。

例如，您定義了自訂上限事件，例如將結帳次數納入考量。 如果您在 **[!UICONTROL 上限計數]** 欄位，10次結帳後將不再傳送其他優惠方案。

### 上限型別 {#capping-type}

您也可以指定是否要將上限套用至所有使用者或一個特定設定檔：

![](../assets/offer-capping-total.png)

* 選取 **[!UICONTROL 總計]** 定義可在合併的目標對象中建議多少次選件，亦即在所有使用者中建議多少次。

   例如，如果您是擁有「TV doorbuster deal」的電子零售商，您只想要在所有設定檔中傳回200次選件。

* 選取 **[!UICONTROL 每個設定檔]** 以定義可向同一位使用者建議某個優惠方案的次數。

   例如，如果您是擁有「白金信用卡」優惠方案的銀行，您不希望此優惠方案在每個設定檔中顯示超過5次。 事實上，您相信，如果使用者看過5次選件且未採取行動，則他們有較高機會對下一個最佳選件採取行動。

### 频次上限 {#frequency-capping}

此 **[!UICONTROL 頻率]** 區段可讓您定義上限計數的重設頻率。 若要這麼做，請定義盤點期間（每日、每週或每月），並輸入您選擇的天數/周數/月數。

![](../assets/offer-capping-frequency.png)

>[!NOTE]
>
>重設會在您定義的當天凌晨12點UTC進行，或在一週/月的第一天（如適用）進行。 周開始日是星期日。 您選擇的任何期間不能超過2年（即對應的月數、周數或天數）。

例如，如果您希望每兩週重設一次上限計數，請選取 **[!UICONTROL 每週]** 從 **[!UICONTROL 重複]** 下拉式清單和型別 **2** 在另一個欄位中。 重設將於每隔一個星期日下午12點(UTC)進行。

>[!CAUTION]
>
>儲存您的優惠方案後，您將無法變更您為頻率選取的時間期間（每月、每週或每日）。

### 上限和版位 {#placements}

如果您已定義數個 [表示方式](add-representations.md) 針對您的優惠，指定是否要套用上限 **[!UICONTROL 橫跨所有位置]** 或 **[!UICONTROL 針對每個位置]**.

![](../assets/offer-capping-placement.png)

* **[!UICONTROL 橫跨所有位置]**：上限計數會加總與優惠方案相關之刊登版位的所有決策。

   例如，如果選件具有 **電子郵件** 位置和 **Web** 位置，而您將上限設定在 **所有版位中每個設定檔2個**，則無論版位組合為何，每個設定檔最多可以收到總共2次選件。

* **[!UICONTROL 針對每個位置]**：上限計數將分別套用每個位置的決定計數。

   例如，如果選件具有 **電子郵件** 位置和 **Web** 位置，而您將上限設定在 **每個位置的每個設定檔2個**，則每個設定檔都會收到最多2次的電子郵件版位優惠，以及另外2次的網路版位優惠。

### 變更日期對上限的影響 {#capping-change-date}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_offer_change_date"
>title="更改日期可能会影响上限"
>abstract="如果此优惠具有上限，则在更改开始或结束日期时可能会影响该上限。"

變更優惠方案的日期時，您必須謹慎操作，因為如果符合以下條件，這可能會對上限產生影響：

* 選件為 [已核准](#review).
* [上限](#capping) 已套用至選件。
* 上限是依設定檔定義。

>[!NOTE]
>
>瞭解如何在中定義優惠方案的日期 [本節](creating-personalized-offers.md#create-offer).

每個設定檔的上限會儲存每個設定檔的上限計數。 當您變更已核准優惠方案的開始和結束日期時，某些設定檔的上限計數可能會根據以下所述的不同情況而受到影響。

![](../assets/offer-capping-change-date.png)

以下是以下可能的情況： **變更優惠方案開始日期**：

| 案例：<br>若…… | 會發生什麼情況：<br>然後…… | 對上限計數的可能影響 |
|--- |--- |--- |
| ...優惠方案開始日期會在原始優惠方案開始日期之前更新， | ...上限計數將從新的開始日期開始。 | 否 |
| ...新的開始日期在目前的結束日期之前， | ...上限會以新的開始日期繼續，而每個設定檔的先前上限計數則會結轉。 | 否 |
| ...新的開始日期在目前的結束日期之後， | ...目前的上限將會到期，而新的上限計數將會從新開始日期的所有設定檔的0重新開始。 | 是 |

以下是以下可能的情況： **延長優惠方案結束日期**：

| 案例：<br>若…… | 會發生什麼情況：<br>然後…… | 對上限計數的可能影響 |
|--- |--- |--- |
| ...決策請求發生在原始優惠方案結束日期之前， | ...上限計數將更新，每個設定檔的上一個上限計數將結轉。 | 否 |
| ...在原始結束日期之前不會發生任何決策請求， | ...上限計數將在每個設定檔的原始結束日期重置。 新的上限計數隨後將從0重新開始，用於原始結束日期之後發生的任何新決策請求。 | 是 |

**示例**

假設您有一個優惠方案，其原始開始日期設為 **1月1日**，到期日 **1931年1月**.

1. 設定檔X、Y和Z會提供選件。
1. 開啟 **10年1月**，則優惠方案的結束日期會變更為 **2月15日**.
1. **1月11日至1月31日**，只有設定檔Z會呈現選件。

   * 因為決策請求發生在原始結束日期之前 **設定檔Z**，優惠方案的結束日期可延長至 **2月15日**.
   * 不過，由於下列專案的原始結束日期之前未發生任何活動： **設定檔X和Y**，其計數器將會過期，而其上限計數將會重設為0於 **1931年1月**.

![](../assets/offer-capping-change-date-ex.png)
