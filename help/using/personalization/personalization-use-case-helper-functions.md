---
solution: Journey Optimizer
product: journey optimizer
title: 個人化使用案例&colon；購物車放棄電子郵件
description: 瞭解如何透過使用案例個人化電子郵件內文。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，協助程式，使用案例，個人化
exl-id: 9c9598c0-6fb1-4e2f-b610-ccd1a80e516e
source-git-commit: 02fc8825f61bd365b02788bbcd3e0647f5842bfa
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 3%

---

# 個人化使用案例：購物車放棄電子郵件 {#personalization-use-case-helper-functions}

在此範例中，您將個人化電子郵件內文。 此訊息會鎖定購物車中仍有商品但尚未完成購買的客戶。

您將使用下列型別的協助程式功能：

* 此 `upperCase` 字串函式，以大寫字母插入客戶的名字。 [了解详情](functions/string.md#upper)。
* 此 `each` 協助程式，可列出購物車中的專案。 [了解详情](functions/helpers.md#each)。
* 此 `if` 協助程式，在購物車中插入產品特定附註。 [了解详情](functions/helpers.md#if-function)。

<!-- **Context**: personalization based on contextual data from the journey -->

➡️ [在本影片中瞭解如何使用協助程式函式](#video)

開始之前，請確定您知道如何設定這些元素：

* 單一事件。 [了解详情](../event/about-events.md)。
* 以事件開始的歷程。 [了解详情](../building-journeys/using-the-journey-designer.md)。
* 歷程中的電子郵件訊息。 [了解详情](../email/create-email.md)
* 電子郵件內文。 [了解详情](../email/content-from-scratch.md)。

执行以下步骤：

1. [建立初始事件和歷程](#create-context).
1. [建立電子郵件訊息](#configure-email).
1. [以大寫字母插入客戶的名字](#uppercase-function).
1. [將購物車內容新增至電子郵件](#each-helper).
1. [插入產品專屬備註](#if-helper).
1. [测试并发布历程](#test-and-publish).

## 步驟1：建立初始事件和相關歷程 {#create-context}

購物車內容是歷程中的內容相關資訊。 因此，您必須先將初始事件和電子郵件新增至歷程，才能將購物車特定資訊新增至電子郵件。

1. 建立其結構描述包含 `productListItems` 陣列。
1. 將此陣列中的所有欄位定義為此事件的裝載欄位。

   進一步瞭解產品清單專案資料型別 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html){target="_blank"}.

1. 建立從此事件開始的歷程。
1. 新增 **電子郵件** 活動至歷程。

   ![](assets/personalization-uc-helpers-8.png)

## 步驟2：建立電子郵件{#configure-email}

1. 在 **電子郵件** 活動，按一下 **[!UICONTROL 編輯內容]**，然後按一下 **[!UICONTROL 電子郵件設計工具]**.

   ![](assets/personalization-uc-helpers-1.png)

1. 從電子郵件設計工具首頁的左側浮動視窗，將三個結構元件拖放至訊息內文上。

1. 將HTML內容元件拖放至每個新結構元件上。

   ![](assets/personalization-uc-helpers-2.png)

## 步驟3：以大寫字母插入客戶的名字 {#uppercase-function}

1. 在電子郵件設計工具首頁上，按一下您要新增客戶名字的HTML元件。
1. 在內容工具列上，按一下 **[!UICONTROL 顯示原始程式碼]**.

   ![](assets/personalization-uc-helpers-3.png)

1. 在 **[!UICONTROL 編輯HTML]** 視窗，新增 `upperCase` 字串函式：
   1. 在左側功能表中，選取 **[!UICONTROL 輔助函式]**.
   1. 使用搜尋欄位來尋找「大寫」。
   1. 從搜尋結果中新增 `upperCase` 函式。 若要這麼做，請按一下旁邊的加號(+) `{%= upperCase(string) %}: string`.

      運算式編輯器會顯示此運算式：

      ```handlebars
      {%= upperCase(string) %}
      ```

      ![](assets/personalization-uc-helpers-4.png)

1. 從運算式中移除「字串」預留位置。
1. 新增名字Token：
   1. 在左側功能表中，選取 **[!UICONTROL 設定檔屬性]**.
   1. 選取 **[!UICONTROL 個人]** > **[!UICONTROL 全名]**.
   1. 新增 **[!UICONTROL 名字]** 運算式的Token。

      運算式編輯器會顯示此運算式：

      ```handlebars
      {%= upperCase(profile.person.name.firstName) %}
      ```

      ![](assets/personalization-uc-helpers-5.png)

      進一步瞭解中的個人名稱資料型別 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/person-name.html){target="_blank"}.

1. 按一下 **[!UICONTROL 驗證]**，然後按一下 **[!UICONTROL 儲存]**.

   ![](assets/personalization-uc-helpers-6.png)

1. 儲存訊息。

## 步驟4：插入購物車中的專案清單 {#each-helper}

1. 重新開啟訊息內容。

1. 在電子郵件設計工具首頁上，按一下您要列出購物車內容的HTML元件。
1. 在內容工具列上，按一下 **[!UICONTROL 顯示原始程式碼]**.

   ![](assets/personalization-uc-helpers-3.png)

1. 在 **[!UICONTROL 編輯HTML]** 視窗，新增 `each` 協助程式：
   1. 在左側功能表中，選取 **[!UICONTROL 輔助函式]**.
   1. 使用搜尋欄位來尋找「each」。
   1. 從搜尋結果中新增 `each` 協助程式。

      運算式編輯器會顯示此運算式：

      ```handlebars
      {{#each someArray as |variable|}} {{/each}}
      ```

      ![](assets/personalization-uc-helpers-9.png)

1. 新增 `productListItems` 陣列至運算式：

   1. 從運算式中移除「someArray」預留位置。
   1. 在左側功能表中，選取 **[!UICONTROL 內容屬性]**.

      **[!UICONTROL 內容屬性]** 只有在歷程內容已傳遞至訊息後，才能使用。

   1. 選取 **[!UICONTROL Journey Optimizer]** > **[!UICONTROL 事件]** > ***[!UICONTROL event_name]***一下，然後展開 **[!UICONTROL productListItems]** 節點。

      在此範例中， *event_name* 代表事件的名稱。

   1. 新增 **[!UICONTROL 產品]** 運算式的Token。

      運算式編輯器會顯示此運算式：

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems.product as |variable|}} {{/each}}
      ```

      在此範例中， *event_ID* 代表事件的ID。

      ![](assets/personalization-uc-helpers-10.png)

   1. 修改運算式：
      1. 移除「.product」字串。
      1. 將「變數」預留位置取代為「產品」。

      此範例顯示修改後的運算式：

      ```handlebars
      {{#each context.journey.events.event_ID.productListItems as |product|}}
      ```


1. 將此程式碼貼到開頭 `{{#each}}` 標籤與結尾 `{/each}}` 標籤：

   ```html
   <table>
      <tbody>
         <tr>
            <td><b>#name</b></td>
            <td><b>#quantity</b></td>
            <td><b>$#priceTotal</b></td>
         </tr>
      </tbody>
   </table>
   ```

1. 新增專案名稱、數量和價格的個人化代號：

   1. 從HTML表格中移除預留位置「#name」。
   1. 從先前的搜尋結果中新增 **[!UICONTROL 名稱]** 運算式的Token。

   重複這些步驟兩次：

   * 將預留位置「#quantity」取代為 **[!UICONTROL 數量]** token。
   * 將預留位置「#priceTotal」取代為 **[!UICONTROL 總價]** token。

   此範例顯示修改後的運算式：

   ```handlebars
   {{#each context.journey.events.event_ID.productListItems as |product|}}
      <table>
         <tbody>
            <tr>
               <td><b>{{context.journey.events.event_ID.productListItems.name}}</b></td>
               <td><b>{{context.journey.events.event_ID.productListItems.quantity}}</b></td>
               <td><b>${{context.journey.events.event_ID.productListItems.priceTotal}}</b></td>
            </tr>
         </tbody>
      </table>
   {{/each}}
   ```

1. 按一下 **[!UICONTROL 驗證]**，然後按一下 **[!UICONTROL 儲存]**.

   ![](assets/personalization-uc-helpers-11.png)

## 步驟5：插入產品特定附註 {#if-helper}

1. 在「電子郵件設計工具」首頁上，按一下要插入附註的HTML元件。
1. 在內容工具列上，按一下 **[!UICONTROL 顯示原始程式碼]**.

   ![](assets/personalization-uc-helpers-3.png)

1. 在 **[!UICONTROL 編輯HTML]** 視窗，新增 `if` 協助程式：
   1. 在左側功能表中，選取 **[!UICONTROL 輔助函式]**.
   1. 使用搜尋欄位來尋找「if」。
   1. 從搜尋結果中新增 `if` 協助程式。

      運算式編輯器會顯示此運算式：

      ```handlebars
      {%#if condition1%} render_1
         {%else if condition2%} render_2
         {%else%} default_render
      {%/if%}
      ```

      ![](assets/personalization-uc-helpers-12.png)

1. 從運算式中移除此條件：

   ```handlebars
   {%else if condition2%} render_2
   ```

   此範例顯示修改後的運算式：

   ```handlebars
   {%#if condition1%} render_1
      {%else%} default_render
   {%/if%}
   ```

1. 將產品名稱Token新增至條件：
   1. 從運算式中移除「condition1」預留位置。
   1. 在左側功能表中，選取 **[!UICONTROL 內容屬性]**.
   1. 選取 **[!UICONTROL Journey Orchestration]** > **[!UICONTROL 事件]** > ***[!UICONTROL event_name]***一下，然後展開 **[!UICONTROL productListItems]** 節點。

      在此範例中， *event_name* 代表事件的名稱。

   1. 新增 **[!UICONTROL 名稱]** 運算式的Token。

      運算式編輯器會顯示此運算式：

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name%}
         render_1
         {%else%} default_render
      {%/if%}
      ```

      ![](assets/personalization-uc-helpers-13.png)

1. 修改運算式：
   1. 在運算式編輯器中，在「 」後面指定產品名稱 `name` token。

      請使用此語法，其中 *product_name* 代表產品的名稱：

      ```javascript
      = "product_name"
      ```

      在此範例中，產品名稱為「Juno Jacket」：

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         render_1
         {%else%} default_render
      {%/if%}
      ```

   1. 將「render_1」預留位置替換為註記文字。

      示例：

      ```handlebars
      {%#if context.journey.events.`event_ID`.productListItems.name = "Juno Jacket" %}
         Due to longer than usual lead times on the Juno Jacket, please expect item to ship two weeks after purchase.
         {%else%} default_render
      {%/if%}
      ```

   1. 從運算式中移除&quot;default_render&quot;預留位置。
1. 按一下 **[!UICONTROL 驗證]**，然後按一下 **[!UICONTROL 儲存]**.

   ![](assets/personalization-uc-helpers-14.png)

1. 儲存訊息。

## 步驟6：測試並發佈歷程 {#test-and-publish}

1. 開啟 **[!UICONTROL 測試]** 切換，然後按一下 **[!UICONTROL 觸發事件]**.

   ![](assets/personalization-uc-helpers-15.png)

1. 在 **[!UICONTROL 事件設定]** 視窗，輸入輸入值，然後按一下 **[!UICONTROL 傳送]**.

   測試模式僅適用於測試設定檔。

   ![](assets/personalization-uc-helpers-16.png)

   電子郵件會傳送至測試設定檔的地址。

   在此範例中，電子郵件會包含有關Juno Jacket的附註，因為此產品已在購物車中：

   ![](assets/personalization-uc-helpers-17.png)

1. 確認沒有錯誤，然後發佈歷程。


## 相关主题 {#related-topics}

### Handlebars函式 {#handlebars}

* [辅助程序](functions/helpers.md)

* [字符串函数](functions/string.md)

### 用例 {#use-case}

* [使用設定檔資訊、內容和選件進行個人化](personalization-use-case.md)

* [使用決策型優惠進行個人化](../offers/offers-e2e.md)

## 操作方法视频{#video}

瞭解如何使用輔助函式。

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
