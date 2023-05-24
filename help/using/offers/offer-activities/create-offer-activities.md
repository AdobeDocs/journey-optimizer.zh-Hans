---
title: 创建决策
description: 瞭解如何建立決定
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 7a217c97-57e1-4f04-a92c-37632f8dfe91
source-git-commit: 93e3ed9e1a9a437353b800aee58952b86eab9370
workflow-type: tm+mt
source-wordcount: '1449'
ht-degree: 3%

---

# 创建决策 {#create-offer-activities}

決定是優惠的容器，可運用優惠決定引擎，根據傳遞的目標來挑選最佳優惠。

➡️ [在本影片中瞭解如何建立優惠方案活動](#video)

決策清單可在 **[!UICONTROL 選件]** 功能表> **[!UICONTROL 決定]** 標籤。 篩選器可協助您根據決策的狀態或開始和結束日期來擷取決策。

![](../assets/activities-list.png)

建立決定之前，請確定已在優惠資料庫中建立下列元件：

* [投放位置](../offer-library/creating-placements.md)
* [收藏集](../offer-library/creating-collections.md)
* [个性化优惠](../offer-library/creating-personalized-offers.md)
* [后备优惠](../offer-library/creating-fallback-offers.md)

## 建立決定 {#create-activity}

1. 存取決定清單，然後按一下 **[!UICONTROL 建立決定]**.

1. 指定決定的名稱。

1. 視需要定義開始和結束日期及時間，然後按一下 **[!UICONTROL 下一個]**.

   ![](../assets/activities-name.png)

1. 若要將自訂或核心資料使用標籤指派給決策，請選取 **[!UICONTROL 管理存取權]**. [進一步瞭解物件層級存取控制(OLAC)](../../administration/object-based-access.md)

## 定義決定範圍 {#add-decision-scopes}

1. 從下拉式清單中選取位置。 它會新增至您決定中的第一個決定範圍。

   ![](../assets/activities-placement.png)

1. 按一下 **[!UICONTROL 新增]** 以選取此位置的評估准則。

   ![](../assets/activities-evaluation-criteria.png)

   每個條件都包含與適用性限制相關聯的優惠方案集合，以及用於決定要顯示在位置中的優惠方案的排名方法。

   >[!NOTE]
   >
   >至少需要一個評估標準。

1. 選取包含要考量之優惠方案的優惠方案集合，然後按一下 **[!UICONTROL 新增]**.

   ![](../assets/activities-collection.png)

   >[!NOTE]
   >
   >您可以按一下 **[!UICONTROL 開啟優惠收藏]** 在新標籤中顯示集合清單的連結，可讓您瀏覽集合及其包含的優惠。

   選取的集合會新增至條件。

   ![](../assets/activities-collection-added.png)

1. 使用 **[!UICONTROL 資格]** 欄位以限制此位置的優惠方案選擇。

   此限制可使用套用 **決定規則**，或一或數個 **Adobe Experience Platform區段**. 兩者皆詳見 [本節](../offer-library/add-constraints.md#segments-vs-decision-rules).

   * 若要將優惠方案的選擇限製為Experience Platform區段的成員，請選取 **[!UICONTROL 區段]**，然後按一下 **[!UICONTROL 新增區段]**.

      ![](../assets/activity_constraint_segment.png)

      從左窗格新增一或多個區段，並使用 **[!UICONTROL 和]** / **[!UICONTROL 或]** 邏輯運運算元。

      ![](../assets/activity_constraint_segment2.png)

      瞭解如何在中使用區段 [本節](../../segment/about-segments.md).

   * 如果您想使用決定規則新增選擇限制，請使用 **[!UICONTROL 決定規則]** 選項並選取您選擇的規則。

      ![](../assets/activity_constraint_rule.png)

      瞭解如何在中建立決定規則 [本節](../offer-library/creating-decision-rules.md).

1. 当您选择区段或决策规则时，可以看到有关估计符合资格的配置文件的信息。按一下 **[!UICONTROL 重新整理]** 以更新資料。

   >[!NOTE]
   >
   >當規則引數包含不在設定檔中的資料（例如內容資料）時，設定檔預估不可用。 例如，適用性規則要求目前天氣為≥80度。

   ![](../assets/activity_constraint-estimate.png)

1. 定義您要用來為每個設定檔選取最佳優惠方案的排名方法。 [了解详情](../offer-activities/configure-offer-selection.md)。

   ![](../assets/activity_ranking-method.png)

   * 依預設，如果有多個優惠方案符合此位置的資格， **[!UICONTROL 優惠優先順序]** 方法使用優惠中定義的值：會將具有最高優先順序分數的優惠傳送給使用者。

   * 如果您想使用特定的計算分數來選擇要遞送的合格優惠方案，請選取 **[!UICONTROL 公式]** 或 **[!UICONTROL AI模型]**. [了解详情](../offer-activities/configure-offer-selection.md)。

1. 按一下 **[!UICONTROL 新增]** 為相同位置定義更多條件。

   ![](../assets/activity_add-collection.png)

1. 新增多個條件時，系統會以特定順序評估這些條件。 系統會先評估新增至序列的第一個集合，依此類推。 [了解详情](#evaluation-criteria-order)

   若要變更預設順序，您可以拖放收藏集，以視需要重新排序。

   ![](../assets/activity_reorder-collections.png)

1. 您也可以同時評估多個條件。 若要這麼做，請將集合拖放至其他集合上方。

   ![](../assets/activity_move-collection.png)

   它們現在具有相同的排名，因此將同時進行評估。 [了解详情](#evaluation-criteria-order)

   ![](../assets/activity_same-rank-collections.png)

1. 若要在此決定中新增其他優惠位置，請使用 **[!UICONTROL 新範圍]** 按鈕。 對每個決定範圍重複上述步驟。

   ![](../assets/activity_new-scope.png)

### 評估准則順序 {#evaluation-criteria-order}

如上所述，評估准則包含集合、資格限制和排名方法。 您可以設定評估准則要評估的順序順序，但也可以合併多個評估准則，以便一起評估而不是單獨評估。

例如，您有兩個集合，一個在評估標準A中，一個在評估標準B中。要求傳回兩個優惠方案。 假設有兩個來自評估標準A的合格優惠方案和三個來自評估標準B的合格優惠方案。

* 如果兩個評估准則為 **未合併** 和/或依序順序（1和2），評估准則的前兩個合格優惠方案會傳回在第一列。 如果第一個評估條件中沒有兩個符合資格的優惠，決定引擎會依序移至下一個評估條件，以找出仍需要多少優惠方案，最終將視需要傳回遞補。

   ![](../assets/activity_consecutive-rank-collections.png)

* 如果兩個集合為 **同時評估**，由於評估標準A中有兩個符合資格優惠方案，評估標準B中有三個符合資格優惠方案，因此這五個優惠方案都會根據各自排名方法決定的值棧疊在一起。 要求兩個優惠方案，因此將傳回這五個優惠方案中的前兩個合格優惠方案。

   ![](../assets/activity_same-rank-collections.png)

## 新增遞補優惠 {#add-fallback}

定義決定範圍後，請定義遞補優惠，此遞補優惠將作為不符合優惠方案適用性規則和限制的客戶的最後手段。

若要這麼做，請從決定中定義之位置的可用遞補優惠清單中選取它，然後按一下 **[!UICONTROL 下一個]**.

![](../assets/add-fallback-offer.png)

>[!NOTE]
>
>您可以按一下 **[!UICONTROL 開啟優惠資料庫]** 在新標籤中顯示優惠方案清單的連結。

## 檢閱並儲存決定 {#review}

如果所有專案皆已正確設定，則會顯示決定屬性的摘要。

1. 確定決定已準備好用於向客戶呈現優惠方案。 會顯示所有決定範圍及其包含的遞補優惠。

   ![](../assets/review-decision.png)

1. 您可以展開或收合每個位置。 您可以預覽每個位置的可用優惠方案、資格和排名詳細資料。 您也可以顯示預估合格設定檔的相關資訊。 按一下 **[!UICONTROL 重新整理]** 以更新資料。

   ![](../assets/review-decision-details.png)

1. 单击&#x200B;**[!UICONTROL 完成]**。
1. 選取 **[!UICONTROL 儲存並啟動]**.

   ![](../assets/save-activities.png)

   您也可以將決定儲存為草稿，以便稍後編輯及啟動。

決定會顯示在清單中，並附有 **[!UICONTROL 即時]** 或 **[!UICONTROL 草稿]** 狀態，取決於您是否在上一步啟動。

現在已準備好用來將優惠方案提供給客戶。

## 决策列表 {#decision-list}

從決定清單中，您可以選取要顯示其屬性的決定。 您也可以從那裡編輯和變更其狀態(**草稿**， **即時**， **完成**， **已封存**)、複製決定或刪除決定。

![](../assets/decision_created.png)

選取 **[!UICONTROL 編輯]** 按鈕以返回決定版本模式，您可以在其中修改決定 [詳細資料](#create-activity)， [決定範圍](#add-decision-scopes) 和 [遞補優惠](#add-fallback).

>[!IMPORTANT]
>
>如果對歷程訊息中使用的優惠決定進行變更，您需要取消發佈歷程並重新發佈。  這將確保將變更納入歷程的訊息中，且訊息與最新更新一致。

選取即時決定並按一下 **[!UICONTROL 停用]** 將決定狀態設回 **[!UICONTROL 草稿]**.

若要再次將狀態設定為 **[!UICONTROL 即時]**，選取 **[!UICONTROL 啟動]** 現在顯示的按鈕。

![](../assets/decision_activate.png)

此 **[!UICONTROL 更多動作]** 按鈕會啟用下面所述的動作。

![](../assets/decision_more-actions.png)

* **[!UICONTROL 完成]**：將決定的狀態設為 **[!UICONTROL 完成]**，這表示該決定無法再被呼叫。 此動作僅適用於啟用的決定。 該決定仍然可以從清單中使用，但您不能將其狀態設定回 **[!UICONTROL 草稿]** 或 **[!UICONTROL 已核准]**. 您只能複製、刪除或封存它。

* **[!UICONTROL 複製]**：使用相同的屬性、決定範圍和遞補優惠建立決定。 依預設，新決定具有 **[!UICONTROL 草稿]** 狀態。

* **[!UICONTROL 刪除]**：從清單中移除決定。

   >[!CAUTION]
   >
   >決定及其內容將無法再存取。 此操作无法撤销。
   >
   >如果決定用於其他物件，則無法刪除該決定。

* **[!UICONTROL 封存]**：將決定狀態設為 **[!UICONTROL 已封存]**. 該決定仍然可以從清單中使用，但您不能將其狀態設定回 **[!UICONTROL 草稿]** 或 **[!UICONTROL 已核准]**. 您只能複製或刪除它。

您也可以選取對應的核取方塊，同時刪除或變更多個決定的狀態。

![](../assets/decision_multiple-selection.png)

如果您想要變更具有不同狀態的多個決定的狀態，則只會變更相關狀態。

![](../assets/decision_change-status.png)

建立決定後，您可以從清單中按一下其名稱。

![](../assets/decision_click-name.png)

這可讓您存取該決定的詳細資訊。 選取 **[!UICONTROL 變更記錄]** 按Tab鍵至 [監視所有變更](../get-started/user-interface.md#changes-log) 已針對此決定進行。

![](../assets/decision_information.png)

## 操作方法视频{#video}

瞭解如何在決定管理中建立優惠方案活動。

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)


