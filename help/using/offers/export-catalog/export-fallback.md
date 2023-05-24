---
title: 遞補優惠資料集
description: 本節列出匯出的資料集中用於遞補優惠的所有欄位
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 3%

---

# 遞補優惠資料集 {#fallback-dataset}

每次修改優惠方案時，都會更新自動產生的備援優惠方案資料集。

![](../assets/dataset-fallback.png)

資料集中最近成功的批次顯示在右側。 資料集的結構描述階層檢視會顯示在左窗格中。

>[!NOTE]
>
>瞭解如何在中存取優惠資料庫每個物件的匯出資料集 [本節](../export-catalog/access-dataset.md).

以下為可用於以下專案的所有欄位清單： **[!UICONTROL 決定物件存放庫 — 遞補優惠]** 資料集。

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

+++ _experience >決策>特性

**欄位：** 特性
**標題：** 決定選項特性
**說明：** 屬於此特定決定選項的其他特性或屬性。 不同的執行個體可以有不同的特性（地圖中的索引鍵）。 特性是用來區分一個決定選項與其他決定選項的名稱值組。 特徵會用作內容中的值，代表此決定選項，並作為分析和最佳化選項效能的功能。 當每個例項都具有相同的屬性或屬性時，該層面應模組化為衍生自決定選項詳細資訊的擴充功能結構。
**型別：** 物件

+++

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

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
      **說明：** 資源的實體或數位表現形式。 通常，格式應包含資源的媒體型別。 格式可用於決定顯示或操作資源所需的軟體、硬體或其他裝置。 建議的最佳作法是從受控的辭彙(例如 [網際網路媒體型別](http://www.iana.org/ assignments/media-types/)定義電腦媒體格式)。
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

+++

+++ _experience >決策>內容>位置

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

+++ _experience >決策>標籤

**欄位：** 標籤
**標題：** 標籤
**說明：** 與此實體相關聯的一組集合限定詞（先前稱為「標籤」）。 集合限定詞用於篩選運算式，以將整體詳細目錄限製為子集（類別）。
**型別：** 陣列

+++

<!--Field without name under collection qualifiers: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++ 存放庫(_R)

**欄位：** 存放庫(_R)
**型別：** 物件

+++

+++ _repo >決定選項ETag

**欄位：** etag
**標題：** 決定選項ETag
**說明：** 決定選項物件拍攝快照時的修訂版本。
**类型：**&#x200B;字符串

+++
