---
title: 决策数据集
description: 本節列出匯出資料集中用於決策的所有欄位
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 064762b7-9774-42eb-bcef-1d92bc94a988
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '1552'
ht-degree: 3%

---

# 决策数据集 {#decisions-dataset}

每次修改優惠時，都會更新自動產生的決定資料集。

![](../assets/dataset-activities.png)

資料集中最近成功的批次顯示在右側。 資料集的結構描述階層檢視會顯示在左窗格中。

>[!NOTE]
>
>瞭解如何在中存取優惠資料庫每個物件的匯出資料集 [本節](../export-catalog/access-dataset.md).

以下為可用於以下專案的所有欄位清單： **[!UICONTROL 決定物件存放庫 — 決定]** 資料集（先前稱為決定物件存放庫 — 活動）。

<!--A decision (formerly known as offer decision) is used to control the decisioning process. It specifies the filter applied to the total inventory to narrow down offers by topic/category, the placement to narrow down the inventory to those offers that technically fit into the reserved space for the offer and specifies a fallback option should the combined constraints disqualify all available personalization offers.-->

+++ 标识符

**欄位：** _id
**標題：** 識別碼
**說明：** 記錄的唯一識別碼。
**类型：**&#x200B;字符串

+++

+++ _experience（体验）

**欄位：** 體驗(_E)
**型別：** 物件

+++

+++ 體驗>決策(_E)

**欄位：** 決策
**型別：** 物件

+++

+++ _experience >決策>條件

**欄位：** 條件
**標題：** 條件
**說明：** 定義一組決定條件，其中每個條件都包含一組限制。
**型別：** 陣列

+++

+++ _experience >決策>條件>說明

**欄位：** 說明
**標題：** 說明
**說明：** 條件說明。 它可用來傳達人類對於如何或為何建構此標準，以及此標準如何影響決策的可讀意圖。
**类型：**&#x200B;字符串

+++

+++_體驗>決策>條件>選項選取

**欄位：** optionSelection
**標題：** 選項選取
**說明：** 選項選擇會定義選項在此內容中的有效性/適用性。
**型別：** 物件

* 描述

   **欄位：** 說明
   **標題：** 說明
   **說明：** 選項選擇說明。 它可用來傳達人類對於如何或為何建構此選項選擇及/或哪個選項會相符的可讀意圖。
   **类型：**&#x200B;字符串

* 選項篩選器

   **欄位：** 篩選
   **標題：** 選項篩選器
   **說明：** 參考以集合限定詞（先前稱為「標籤」）為基礎的篩選器，其使用附加的集合限定詞來比對來自詳細目錄的選項。 該值是被參考的決策規則的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/filter 。
   **类型：**&#x200B;字符串

* 設定檔限制型別

   **欄位：** optionSelectionType
   **標題：** 設定檔限制型別
   **說明：** 決定目前是否設定了任何限制，以及如何表示限制。 可能是透過篩選查詢或透過一或多個區段會籍。
   **类型：**字符串
   **可能的值：** &quot;none&quot; （預設）、&quot;directList&quot;、&quot;filter&quot;

* 選項清單

   **欄位：** 選項
   **標題：** 選項清單
   **說明：** 直接指定選項而不評估篩選查詢的清單。 可以指定選項清單或選項篩選規則。
   **型別：** 陣列

<!--Missing title under Option List? Desc = An identifier of an decision option entity. The value value refers to an `@id` property of a decision option. Type: string-->

+++

+++_體驗>決策>條件>位置

**欄位：** 位置
**標題：** 放置限制
**說明：** 位置限制指出此條件僅適用於列出的位置。 只有當目標位置位於 `xdm:placements` list是考慮的選項選取專案。 否則會略過整個決定條件。 當「xdm：placements」清單被省略或空白時，任何目標位置都會考量此條件。 此處列出的版位會強制套用選項選取的隱含條件。 要考慮的選項必須具有目標位置的表示。
**型別：** 陣列

* 位置識別碼

   **標題：** 位置識別碼
   **說明：** 位置圖元的參照。 該值是被參考之位置的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/placement 。
   **类型：**&#x200B;字符串

+++

+++_體驗>決策>條件> profileConstraints

**欄位：** profileConstraint
**標題：** 設定檔限制
**說明：** 在此前後關聯中，設定檔限制會決定選項選取目前是否符合此設定檔識別的資格。 如果設定檔限制不需要考慮每個選項的值（亦即選項選取範圍中的選項不變），則評估為「false」的設定檔限制會取消整個選項選取範圍。 另一方面，會針對選項選取的每個合格選項，評估將選項作為引數的設定檔限制規則。
**型別：** 物件

+++

+++_體驗>決策>條件> profileConstraints >說明

**欄位：** 說明
**標題：** 說明
**說明：** 設定檔限制說明。 它可用來傳達人類對於如何或為何建構此設定檔限制及/或其將包含或排除哪個選項的可讀意圖。
**类型：**&#x200B;字符串

+++

+++ _experience >決策>條件> profileConstraints >適用性規則

**欄位：** 適用性規則
**標題：** 適用性規則
**說明：** 決策規則的參考，對於指定的設定檔和/或其他指定的內容XDM物件，其評估為true或false。 此規則用於決定選項是否符合給定設定檔的資格。 該值是被參考的決策規則的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/rule 。
**类型：**&#x200B;字符串

+++

+++ _experience >決策>條件> profileConstraints >設定檔限制型別

**欄位：** profileConstraintType
**標題：** 設定檔限制型別
**說明：** 決定目前是否設定了任何限制，以及如何表示限制。 可能是透過規則或一個或多個區段會籍。
**型別：** 字串
**可能的值：**
* &quot;none&quot; （預設）
* &quot;eligibilityRule&quot;：&quot;設定檔限制表示為單一規則，在允許限製作業之前，必須評估為true。&quot;
* &quot;anySegments&quot;：&quot;設定檔限制表示為一或多個區段，而且設定檔必須是其中至少一個的成員，才允許限制動作。&quot;
* &quot;allSegments&quot;：&quot;設定檔限制表示為一或多個區段，而且設定檔必須是所有區段的成員，才允許限制動作。&quot;
* &quot;rules&quot;：&quot;設定檔限制是以許多不同規則來表示，例如，適用性、適用性、適用性，在允許限制動作之前，這些規則都必須評估為true。&quot;

+++

+++ _experience > decisioning >條件> profileConstraints > segmentIdentities

**欄位：** segmentIdentities
**標題：** 區段識別碼
**說明：** 區段的識別碼。
**型別：** 陣列

* 标识符

   **欄位：** _id
   **標題：** 識別碼
   **說明：** 相關名稱空間中區段的身分。
   **类型：**&#x200B;字符串

* namespace

   **欄位：** 名稱空間
   **標題：** 名稱空間
   **說明：** 與關聯的名稱空間 `xid` 屬性。
   **型別：** 物件
   **必填：** &quot;code&quot;

   * 代码

      **欄位：** 程式碼
      **標題：** 程式碼
      **說明：** 此程式碼是適用於名稱空間的可讀取識別碼，可用於請求技術性的名稱空間ID （用於身分圖表處理）。
      **类型：**&#x200B;字符串

* 體驗識別碼

   **欄位：** xid
   **標題：** 體驗識別碼
   **說明：** 當出現時，這個值代表跨名稱空間的識別碼，在所有名稱空間中都是唯一，也就是所有名稱空間中的範圍識別碼。
   **类型：**&#x200B;字符串

+++

+++_體驗>決策>條件>排名

**欄位：** 排名
**標題：** 排名詳細資料
**說明：** 排名（優先順序）。 定義在決定標準內容的背景下如何判斷\「最佳選項\」。 在符合設定檔限制的所有選定選項中，排名將決定要建議的前（或前N個）選項。
**型別：** 物件

+++

+++_體驗>決策>條件>排名>訂單

**欄位：** 訂購
**標題：** 訂單評估
**說明：** 評估一或多個決定選項的相對順序。 在順序值較低的選項上，會選取順序值較高的選項。 此方法所決定的值可以排序，但無法測量它們之間的距離，也無法加總或計算產品。 中間值和模式是唯一可用於序數資料的中心趨勢測量值。
**型別：** 物件

* 評分函式

   **欄位：** 函式
   **標題：** 評分函式
   **說明：** 計算此決定選項之數值分數之函式的參考。 決策選項將依該分數排序（排名）。 此屬性的值是每次使用on選項叫用之函式的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/function 。
   **类型：**&#x200B;字符串

* 訂單評估型別**

   **欄位：** orderEvaluationType
   **標題：** 訂單評估型別
   **說明：** 指定使用哪個順序評估機制、決定選項的靜態優先順序、計算每個選項數值的評分函式，或接收排序清單的排名策略。
   **类型：**字符串
   **可能的值：** &quot;static&quot;、&quot;scoringFunction&quot;、&quot;rankingStrategy&quot;

* 排名策略

   **欄位：** 排名策略
   **標題：** 排名策略
   **說明：** 對決定選項清單進行排名的策略參考。 決策選項將會以有序清單傳回。 此屬性的值是每次使用on選項叫用之函式的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/rankingStrategy 。
   **类型：**&#x200B;字符串

+++

+++ _experience >決策>條件>排名>優先順序

**欄位：** 優先順序
**標題：** 優先順序
**說明：** 相對於所有其他選項的單一決定選項的優先順序。 未提供訂單函式的選項會使用此屬性來排定優先順序。 優先順序值較高的選項會在優先順序較低的選項之前選取。 如果兩個或多個合格選項共用最高優先順序值，則會以統一的隨機方式選擇一個選項，以用於決策主張。
**型別：** 整數
**最小值：** 0
**預設值：** 0

+++

+++ _experience >決策>活動結束日期和時間

**欄位：** endTime
**標題：** 活動結束日期和時間
**說明：** 決定（先前稱為活動）結束日期和結束時間。 屬性具有在http://schema.org/Action上定義的schema.org的「endTime」屬性的語意。
**类型：**&#x200B;字符串

+++

+++ _experience >決策>遞補選項

**欄位：** 遞補內容
**標題：** 後援選項
**說明：** 在此決定的內容中決策時使用的備援選項參考不符合任何一般選項的資格（這通常發生在套用硬式限制時）。 值是參考之備援選項的URI (@id)。
**类型：**&#x200B;字符串

+++

+++ 體驗>決策>活動名稱(_E)

**欄位：** 名稱
**標題：** 活動名稱
**說明：** 顯示在各種使用者介面中的決定（先前稱為活動）名稱。
**类型：**&#x200B;字符串

+++

+++_體驗>決策>活動開始日期和時間

**欄位：** startTime
**標題：** 活動開始日期和時間
**說明：** 決定（先前稱為活動）開始日期和結束時間。 屬性具有在http://schema.org/Action上定義的schema.org的「startTime」屬性的語意。
**类型：**&#x200B;字符串

+++

+++ 存放庫(_R)

**欄位：** 存放庫(_R)
**型別：** 物件

+++

+++ _repo >活動ETag

**欄位：** etag
**標題：** 活動設定檔
**說明：** 建立快照時決定（先前稱為活動）物件的修訂版本。
**类型：**&#x200B;字符串

+++
