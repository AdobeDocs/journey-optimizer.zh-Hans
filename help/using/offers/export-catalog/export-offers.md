---
title: 个性化优惠数据集
description: 本節列出匯出之優惠方案資料集中使用的全部欄位
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: c7f691aa-8f89-4f23-b897-53211863eb6d
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '2014'
ht-degree: 3%

---

# 个性化优惠数据集 {#offers-dataset}

每次修改優惠方案時，都會更新自動產生的個人化內容優惠方案資料集。

![](../assets/dataset-offers.png)

資料集中最近成功的批次顯示在右側。 資料集的結構描述階層檢視會顯示在左窗格中。

>[!NOTE]
>
>瞭解如何在中存取優惠資料庫每個物件的匯出資料集 [本節](../export-catalog/access-dataset.md).

以下為可用於以下專案的所有欄位清單： **[!UICONTROL 決定物件存放庫 — 個人化優惠]** 資料集。

<!--Personalized offers form the set of choices for a decision. The objective for decisioning is to take a large inventory of items and apply numerous constraint rules to that inventory to narrow it down and then to rank the qualifying options according to a criteria. The resulting propositions assemble and personalize the experience for specific individuals.-->

+++ 标识符

**欄位：** _id
**標題：** 識別碼
**說明：** 記錄的唯一識別碼。
**类型：**&#x200B;字符串

+++

+++ _experience（体验） {#experience}

**欄位：** 體驗(_E)
**型別：** 物件

+++

+++ 體驗>決策(_E)

**欄位：** 決策
**型別：** 物件

+++

+++ 體驗>決策>行事曆限制(_E)

**欄位：** calendarConstraints
**標題：** 行事曆限制詳細資訊
**說明：** 行事曆限制會決定指定日期範圍的決定選項是否有效。 在該日期範圍以外，無法建議選項。
**型別：** 物件

* **結束日期和時間**

   **欄位：** endDate
   **標題：** 結束日期和時間
   **說明：** 決定選項有效性的結束日期。 已超過其結束日期的選項無法再於決策程式中建議。
   **类型：**&#x200B;字符串

* **開始日期和時間**

   **欄位：** startDate
   **標題：** 開始日期和時間
   **說明：** 決定選項有效性的開始日期。 尚未到達開始日期的選項無法在決策程式中建議。
   **类型：**&#x200B;字符串

+++

+++ _experience >決策>特性

**欄位：** 特性
**標題：** 決定選項特性
**說明：** 屬於此特定決定選項的其他特性或屬性。 不同的執行個體可以有不同的特性（地圖中的索引鍵）。 特性是用來區分一個決定選項與其他決定選項的名稱值組。 特徵會用作內容中的值，代表此決定選項，並作為分析和最佳化選項效能的功能。 當每個例項都具有相同的屬性或屬性時，該層面應模組化為衍生自決定選項詳細資訊的擴充功能結構。
**型別：** 物件

+++

+++ 體驗>決策>內容(_E)

**欄位：** 內容
**標題：** 內容詳細資料
**說明：** 在不同內容中呈現決定專案的內容專案。 單一決定選項可以有多個內容變體。 內容是導向對象以供在（數位）體驗中使用的資訊。 內容會透過管道傳送到特定位置。
**型別：** 陣列

+++

+++_體驗>決策>內容>元件

**欄位：** 元件
**說明：** 代表決定選項的內容元件，包括其所有語言變體。 特定元件可透過「dx：format」、「dc：subject」和「dc：language」或其組合找到。 此中繼資料用於尋找或表示與優惠方案相關聯的內容，並根據刊登版位合約加以整合。
**型別：** 陣列
**必填：** &quot;_type&quot;， &quot;_dc&quot; <!--TBC?-->

* **_experience >決策>內容>元件>內容元件型別**

   **欄位：** 型別(_t)
   **標題：** 內容元件型別
   **說明：** 列舉的一組URI，其中每個值對應到指定給內容元件的型別。 內容表示的某些消費者期望@type值是描述內容元件其他屬性的結構描述的參考。
   **类型：**&#x200B;字符串

* **_experience >決策>內容>元件> _dc**

   **欄位：** _dc
   **型別：** 物件
   **必填：** &quot;format&quot;

   * **格式**

      **欄位：** 格式
      **標題：** 格式
      **說明：** 資源的實體或數位表現形式。 通常，格式應包含資源的媒體型別。 格式可用於決定顯示或操作資源所需的軟體、硬體或其他裝置。 建議的最佳作法是從受控的辭彙(例如 [網際網路媒體型別](http://www.iana.org/assignments/media-types/) 定義電腦媒體格式)。
      **类型：**字符串
      **範例：** &quot;application/vnd.adobe.photoshop&quot;

   * **语言**
      **欄位：** 語言
      **標題：** 語言
      **說明：** 資源的語言。 \n語言是依照中定義的語言代碼指定的 [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)，這是XDM其他位置所使用的BCP 47的一部分。
      **型別：** 陣列
      **範例：** &quot;\n&quot;、&quot;pt-BR&quot;、&quot;es-ES&quot;

* **_experience >決策>內容>元件> _repo**

   **欄位：** 存放庫(_R)
   **型別：** 物件

   * **id**

      **欄位：** id
      **說明：** 選用的唯一識別碼，可參考內容存放庫中的資產。 使用Platform API擷取表示法時，使用者端可期待額外屬性\&quot;repo：resolveUrl\&quot;來擷取資產。
      **类型：**字符串
      **範例：** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e」

   * **name**

      **欄位：** 名稱
      **說明：** 對於透過\&quot;repo：id\&quot;尋找儲存外部資產的存放庫的位置，有一些提示。
      **类型：**&#x200B;字符串

   * **repositoryID**

      **欄位：** repositoryID
      **說明：** 選用的唯一識別碼，可參考內容存放庫中的資產。 使用Platform API擷取表示法時，使用者端可期待額外屬性\&quot;repo：resolveUrl\&quot;來擷取資產。
      **类型：**字符串
      **範例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **欄位：** resolveURL
      **說明：** 選用的唯一資源定位器，可讀取內容存放庫中的資產。 這可讓使用者端更容易取得資產，而無需瞭解資產的管理位置以及要呼叫的API。 這類似於HAL連結，但語意較簡單，且更有意義。
      **类型：**字符串
      **範例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;

* **_experience >決策>內容>元件>內容**

   **欄位：** 內容
   **說明：** 直接保留內容的選用欄位。 元件可以直接儲存簡單的內容，而不必參考資產存放庫中的內容。 此欄位不適用於複合、複雜和二進位內容資產。
   **类型：**&#x200B;字符串

* **_experience >決策>內容>元件> deliveryURL**

   **欄位：** deliveryURL
   **說明：** 選用的唯一資源定位器，可從內容傳遞網路或服務端點取得資產。 使用者代理程式會使用此URL來公開存取資產。
   **类型：**字符串
   **範例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience >決策>內容>元件> linkURL**

   **欄位：** linkURL
   **說明：** 選擇性唯一資源定位器，用於使用者互動。 此URL用於在使用者代理中將一般使用者引薦至，並且可被追蹤。
   **类型：**字符串
   **範例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

+++_體驗>決策>內容>位置

**欄位：** 刊登
**標題：** 刊登
**說明：** 要遵循的位置。 該值是被參考之優惠方案版位的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/placement 。
**类型：**&#x200B;字符串

+++

+++ _experience >決策>生命週期狀態

**欄位：** lifecycleStatus
**標題：** 生命週期狀態
**說明：** 生命週期狀態允許使用物件執行工作流程。 狀態可能會影響顯示物件或物件被視為相關的位置。 狀態變更是由使用物件的使用者端或服務所驅動。
**型別：** 字串
**可能的值：** 「草稿」（預設）、「已核准」、「即時」、「已完成」、「已封存」

+++

+++ 體驗>決策>決策選項名稱(_E)

**欄位：** 名稱
**標題：** 決定選項名稱
**說明：** 顯示在各種使用者介面中的選項名稱。
**类型：**&#x200B;字符串

+++

+++ _experience > decisioning > profileConstraints

**欄位：** profileConstraint
**標題：** 設定檔限制細節
**說明：** 在此上下文中，設定檔限制會決定某個選項是否符合此設定檔識別的資格。 如果設定檔限制不需要考慮每個選項的值（亦即選項選取範圍中的選項不變），則評估為「false」的設定檔限制會取消整個選項選取範圍。 另一方面，會針對選項選取的每個合格選項，評估將選項作為引數的設定檔限制規則。
**型別：** 物件

+++

+++_體驗>決策> profileConstraints >說明

**欄位：** 說明
**標題：** 說明
**說明：** 設定檔限制說明。 它可用來傳達人類對於如何或為何建構此設定檔限制及/或其將包含或排除哪個選項的可讀意圖。
**类型：**&#x200B;字符串

+++

+++_體驗>決策> profileConstraints >適用性規則

**欄位：** 適用性規則
**標題：** 適用性規則
**說明：** 決策規則的參考，對於指定的設定檔和/或其他指定的內容XDM物件，其評估為true或false。 此規則用於決定選項是否符合給定設定檔的資格。 該值是被參考的決策規則的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/rule 。
**类型：**&#x200B;字符串

+++

+++_體驗>決策> profileConstraints >設定檔限制型別

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

+++_體驗>決策> profileConstraints >區段識別碼

**欄位：** segmentIdentities
**標題：** 區段識別碼
**說明：** 區段的識別碼
**型別：** 陣列

* **标识符**

   **欄位：** _id
   **標題：** 識別碼
   **說明：** 相關名稱空間中區段的身分。
   **类型：**&#x200B;字符串

* **命名空间**

   **欄位：** 名稱空間
   **標題：** 名稱空間
   **說明：** 與關聯的名稱空間 `xid` 屬性。
   **型別：** 物件
   **必填：** &quot;code&quot;

   * **代码**

      **欄位：** 程式碼
      **標題：** 程式碼
      **說明：** 此程式碼是適用於名稱空間的可讀取識別碼，可用於請求技術性的名稱空間ID （用於身分圖表處理）。
      **类型：**&#x200B;字符串

* **體驗識別碼**

   **欄位：** xid
   **標題：** 體驗識別碼
   **說明：** 當出現時，這個值代表跨名稱空間的識別碼，在所有名稱空間中都是唯一，也就是所有名稱空間中的範圍識別碼。
   **类型：**&#x200B;字符串

+++

+++ 體驗>決策>排名(_E)

**欄位：** 排名
**標題：** 排名詳細資料
**說明：** 排名（優先順序）。 定義在決策標準內容下的視為\「最佳動作\」的專案。 在符合資格限制的所有選取選項中，排名順序將決定要建議的前（或前N個）選項。
**型別：** 物件

+++

+++_體驗>決策>排名>訂單評估

**欄位：** 訂購
**標題：** 訂單評估
**說明：** 評估一或多個決定選項的相對順序。 在順序值較低的選項上，會選取順序值較高的選項。 此方法所決定的值可以排序，但無法測量它們之間的距離，也無法加總或計算產品。 中間值和模式是唯一可用於序數資料的中心趨勢測量值。
**型別：** 物件

* **評分函式**

   **欄位：** 函式
   **標題：** 評分函式
   **說明：** 計算此決定選項之數值分數之函式的參考。 決策選項將依該分數排序（排名）。 此屬性的值是每次使用on選項叫用之函式的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/function 。
   **类型：**&#x200B;字符串

* **訂單評估型別**

   **欄位：** orderEvaluationType
   **標題：** 訂單評估型別
   **說明：** 指定使用哪個順序評估機制、決定選項的靜態優先順序、計算每個選項數值的評分函式，或接收排序清單的排名策略。
   **类型：**字符串
   **可能的值：** &quot;static&quot;、&quot;scoringFunction&quot;、&quot;rankingStrategy&quot;

* **排名策略**

   **欄位：** 排名策略
   **標題：** 排名策略
   **說明：** 對決定選項清單進行排名的策略參考。 決策選項將會以有序清單傳回。 此屬性的值是每次使用on選項叫用之函式的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/rankingStrategy 。
   **类型：**&#x200B;字符串

+++

+++_體驗>決策>排名>優先順序

**欄位：** 優先順序
**標題：** 優先順序
**說明：** 相對於所有其他選項的單一決定選項的優先順序。 未提供訂單函式的選項會使用此屬性來排定優先順序。 優先順序值較高的選項會在優先順序較低的選項之前選取。 如果兩個或多個合格選項共用最高優先順序值，則會以統一的隨機方式選擇一個選項，以用於決策主張。
**型別：** 整數
**最小值：** 0
**預設值：** 0

+++

+++ _experience >決策>標籤

**欄位：** 標籤
**標題：** 標籤
**說明：** 與此實體相關聯的一組集合限定詞（先前稱為「標籤」）。 集合限定詞用於篩選運算式，以將整體詳細目錄限製為子集（類別）。
**型別：** 陣列

+++

<!--Field without name under tags: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++_repo

**欄位：** 存放庫(_R)
**型別：** 物件

+++

+++ _repo >決定選項ETag

**欄位：** etag
**標題：** 決定選項ETag
**說明：** 決定選項物件拍攝快照時的修訂版本。
**类型：**&#x200B;字符串

+++
