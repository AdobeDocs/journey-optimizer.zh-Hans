---
solution: Journey Optimizer
product: journey optimizer
title: 將歷程複製到另一個沙箱
description: 瞭解如何將歷程複製到另一個沙箱
feature: Journeys
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 沙箱，歷程，複製，環境
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 20%

---

# 将历程复制到另一个沙盒 {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="将历程复制到另一个沙盒"
>abstract="可以使用 Journey Optimizer 将整个历程从一个沙盒复制到另一个沙盒。例如，您可以将历程从暂存沙盒环境复制到生产沙盒。除了历程本身，Journey Optimizer 还会复制历程所依赖的大部分对象。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="沙盒详细信息"
>abstract="选择您要将历程复制到的目标沙盒。只有您组织内的沙盒可用。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="对象详细信息"
>abstract="这就是您要复制的历程。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="依赖对象"
>abstract="这是在历程中使用的关联对象的列表。此列表显示名称、对象类型以及内部 Journey Optimizer ID。"

可以使用 Journey Optimizer 将整个历程从一个沙盒复制到另一个沙盒。例如，您可以將歷程從中繼沙箱環境複製到生產沙箱。 除了歷程本身，Journey Optimizer也會複製歷程所依賴的大部分物件：區段、表面（即預設集）、結構描述、事件和動作。 有關已複製物件的詳細資訊，請參閱此 [區段](#limitations).

>[!CAUTION]
>
>我們不保證所有連結的元素都會複製到目的地沙箱。 我們強烈建議您在發佈歷程之前執行徹底的檢查。 這可讓您識別任何可能遺失的物件。

目標沙箱中的複製物件是唯一的，沒有覆寫現有元素的風險。 歷程及歷程內的任何訊息都會以草稿模式帶入。 這可讓您在目標沙箱上發佈之前執行徹底的驗證。 復製程式只會複製有關歷程的中繼資料和該歷程中的物件。 此程式不會複製任何設定檔或資料集資料。

若要將歷程複製到另一個沙箱，請執行以下步驟：

1. 在JOURNEY MANAGEMENT功能表區段中，按一下 **[!UICONTROL 歷程]**. 隨即顯示歷程清單。

2. 搜尋您要複製的歷程，按一下 **更多動作** 圖示（歷程名稱旁邊的三個點）並按一下 **複製到沙箱**.

   ![](assets/copy-sandbox1.png)

   此 **複製到沙箱** 畫面隨即顯示。

   ![](assets/copy-sandbox2.png)

3. 選取 **Target沙箱** 下拉式欄位中的。 只有您组织内的沙盒可用。

4. 檢閱 **相依物件** 區段。 这是在历程中使用的关联对象的列表。此列表显示名称、对象类型以及内部 Journey Optimizer ID。

5. 按一下 **複製** 按鈕，開始將歷程複製到目標沙箱。

   ![](assets/copy-sandbox3.png)

   復製程式隨即開始，並顯示每個個別物件的進度。 復製程式會因歷程的複雜度及需要複製多少物件而有所不同。 如果發生錯誤，則會顯示相關物件的訊息。

   ![](assets/copy-sandbox4.png)

6. 複製完成後，請按一下 **關閉**.

7. 存取您的目標沙箱，並對所有複製的物件執行徹底檢查。

## 復製程式和限制 {#limitations}

所有連結的元素可能不會複製到目的地沙箱。 Adobe強烈建議您執行徹底的檢查。 識別任何可能的遺失物件，並在發佈歷程之前手動建立。

下列物件已複製：

* 区段

   區段只能從一個沙箱複製到另一個沙箱。 區段一經複製，就無法在目的地沙箱中編輯。

* 架构

   此歷程中使用的結構描述已複製。

* 消息

   歷程中使用的管道動作活動。 訊息中用於個人化的欄位不會檢查完整性。 不會複製內容區塊。

* 歷程 — 畫布詳細資料

   畫布上的歷程表示，包括歷程中的物件，例如條件、動作、事件、讀取區段等。 跳轉活動會從複製中排除。

* 活动

   將會複製歷程中使用的事件和事件詳細資訊。

* 操作

   將會複製歷程中使用的動作和動作詳細資訊。

不會複製曲面（即預設集）。 系統會根據訊息型別和表面名稱，自動選取目標沙箱上最接近的相符專案。 如果在目標沙箱上找不到表面，則表面複製將失敗。 這表示訊息複製也會失敗，因為訊息需要可供設定的介面。 在此情況下，至少需要建立一個表面，以使用訊息的正確通道，復本才能運作。

對於結構描述、合併原則和區段，這些物件第二次嘗試複製時，只會被引用。 會將它們視為已存在的物件，並再次複製。 這表示這些物件只能複製一次。

Adobe Journey Optimizer參照結構描述、合併原則和區段後，需經過5分鐘的延遲，才不會在畫布中看到錯誤。 等待五分鐘，這些參考資料將可供使用。
