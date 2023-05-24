---
solution: Journey Optimizer
product: journey optimizer
title: 在历程中使用区段
description: 瞭解如何在歷程中使用區段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 活動，歷程，讀取，區段，平台
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 13%

---

# 在历程中使用区段 {#segment-trigger-activity}

## 新增讀取區段活動 {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="读取区段活动"
>abstract="利用读取区段活动，您可以允许属于 Adobe Experience Platform 区段的所有个人进入历程。进入历程的操作可以执行一次，也可以定期执行。"

使用 **讀取區段** 活動，讓區段的所有個人進入歷程。 进入历程的操作可以执行一次，也可以定期执行。

以中建立的「Luma應用程式開啟和結帳」區段為例 [建立區段](../segment/about-segments.md) 使用案例。 透過「讀取區段」活動，您可以讓屬於此區段的所有個人進入歷程，並讓他們流入將運用所有歷程功能（條件、計時器、事件、動作）的個人化歷程。

>[!NOTE]
>
>对于使用“读取区段”活动的历程，可以同时启动的历程数具有上限。系统将重试，但请不要同时启动超过 5 个历程（读取区段、预定或“尽快”开始），可以将它们分散到不同的时间，例如间隔 5 到 10 分钟。
>
>以读取区段、区段鉴别或业务事件活动开始的历程中，无法使用体验事件字段组。

### 設定活動 {#configuring-segment-trigger-activity}

設定「讀取區段」活動的步驟如下：

1. 展開 **[!UICONTROL 協調流程]** 類別與放置 **[!UICONTROL 讀取區段]** 活動放入您的畫布。

   活動必須定位為歷程的第一步。

1. 新增 **[!UICONTROL 標籤]** 至活動（選用）。

1. 在 **[!UICONTROL 區段]** 欄位，選擇將進入歷程的Adobe Experience Platform區段，然後按一下 **[!UICONTROL 儲存]**.

   请注意，您可以自定义列表中显示的列，并对其进行排序。

   >[!NOTE]
   >
   >只有具備下列條件的個人 **已實現** 和 **現有** 區段參與狀態將進入歷程。 如需如何評估區段的詳細資訊，請參閱 [Segment Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

   ![](assets/read-segment-selection.png)

   新增區段後， **[!UICONTROL 複製]** 按鈕可讓您複製其名稱和ID：

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. 在 **[!UICONTROL 名稱空間]** 欄位，選擇要使用的名稱空間以識別個人。 依預設，欄位會使用上次使用的名稱空間預先填入。 [進一步瞭解名稱空間](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >屬於區段(其不同身分中沒有所選身分（名稱空間）)的個人無法進入歷程。 您只能選取以人物為基礎的身分名稱空間。 如果您已定義查閱表格的名稱空間（例如：產品查閱的ProductID名稱空間），它將無法在 **名稱空間** 下拉式清單。

1. 設定 **[!UICONTROL 節流率]** 欄位至讀取區段活動的輸送量限制。

   此值會儲存在歷程版本裝載中。 預設值為每秒5,000則訊息。 您可以將此值從每秒500則訊息修改為每秒20,000則訊息。

   >[!NOTE]
   >
   >每個沙箱的整體節流率設定為每秒20,000則訊息。 因此，在同一沙箱中同時執行的所有讀取區段的節流率每秒最多可新增20,000則訊息。 您無法修改此上限。

1. 此 **[!UICONTROL 讀取區段]** 活動可讓您指定區段進入歷程的時間。 若要這麼做，請按一下 **[!UICONTROL 編輯歷程排程]** 連結以存取歷程的屬性，然後設定 **[!UICONTROL 排程器型別]** 欄位。

   ![](assets/read-segment-schedule.png)

   依預設，區段會進入歷程 **[!UICONTROL 儘快]**. 如果您想要讓區段在特定日期/時間或循環基礎上進入歷程，請從清單中選取所需的值。

   >[!NOTE]
   >
   >請注意 **[!UICONTROL 排程]** 區段僅在以下情況下可用： **[!UICONTROL 讀取區段]** 已在畫布中捨棄活動。

   ![](assets/read-segment-schedule-list.png)

   **增量讀取** 選項：當具有週期性歷程時 **讀取區段** 第一次執行時，區段中的所有設定檔都會進入歷程。 此選項可讓您在第一次發生後，只將目標設定為自上次執行歷程以來進入區段的個人。

   **在重複時強制重新進入**：此選項可讓您讓歷程中仍存在的所有設定檔在下次執行時自動退出。 例如，如果您在每日循環歷程中等候2天，透過啟用此選項，設定檔將一律會在下次歷程執行（也就是之後的那天）中移動，無論它們是否在下次執行的對象中。 如果此歷程中設定檔的生命週期可能長於週期性頻率，請勿啟用此選項以確保設定檔可完成其歷程。

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>一次性讀取區段歷程在歷程執行30天後會移至「已完成」狀態。 对于计划的读取区段，此期限为上次执行后的 30 天。 

### 测试并发布历程 {#testing-publishing}

此 **[!UICONTROL 讀取區段]** 活動可讓您在單一設定檔上測試歷程，或在符合區段資格之設定檔中隨機選取的100個測試設定檔上測試歷程。

若要這麼做，請啟動測試模式，然後從左窗格中選取所需的選項。

![](assets/read-segment-test-mode.png)

然後您可以照常設定並執行測試模式。 [瞭解如何測試歷程](testing-the-journey.md).

測試執行後， **[!UICONTROL 顯示記錄]** 按鈕可讓您根據選取的測試選項檢視測試結果：

* **[!UICONTROL 一次一個設定檔]**：測試記錄會顯示與使用單一測試模式時相同的資訊。 有關詳細資訊，請參閱 [本節](testing-the-journey.md#viewing_logs)

* **[!UICONTROL 一次最多100個設定檔]**：測試記錄檔可讓您追蹤從Adobe Experience Platform匯出區段的進度，以及所有進入歷程的人員的個人進度。

   請注意，一次使用最多100個設定檔測試歷程不允許您使用視覺流程追蹤歷程中個人的進度。

   ![](assets/read-segment-log.png)

測試成功後，您就可以發佈歷程(請參閱 [發佈歷程](publishing-the-journey.md))。 屬於區段的個人將在歷程屬性中指定的日期/時間進入歷程 **[!UICONTROL 排程器]** 區段。

>[!NOTE]
>
>對於以區段為基礎的週期性歷程，一旦執行了歷程的最後一次發生，該歷程將自動關閉。 如果未指定結束日期/時間，您必須手動將歷程關閉至新入口，才能將其結束。

## 區段型歷程中的對象鎖定目標

區段型歷程一律以 **讀取區段** 活動以擷取屬於Adobe Experience Platform區段的個人。

屬於區段的對象會擷取一次或定期擷取。

進入歷程後，您可以建立受眾協調使用案例，使個人從初始區段流入歷程的不同分支。

**区段**

您可以使用條件來執行分段，方法是 **條件** 活動。 例如，您可以讓VIP人員採用特定路徑，而非VIP人員則採用其他路徑。

區段可根據：

* 資料來源資料
* 歷程資料中事件部分的內容，例如：有人點按了一小時前收到的訊息嗎？
* 日期，例如：某人瀏覽歷程時，我們是在6月嗎？
* 時間，例如：現在是個人時區的早上嗎？
* 根據百分比分割歷程中流動的對象的演演算法，例如：90% - 10%以排除控制組

![](assets/read-segment-audience1.png)

**排除**

相同 **條件** 用於區段的活動（請參閱上文）也可讓您排除部分母體。 例如，您可以排除VIP人員，方法是讓他們流入後面有結束步驟的分支。

此排除可能發生在區段擷取之後、基於母體計數目的或沿著多步驟歷程。

![](assets/read-segment-audience2.png)

**Union**

歷程可讓您建立N個分支，並在分段後將其聯結。

因此，您可以讓兩個受眾回到共同體驗。

例如，在歷程中連續十天追蹤不同體驗後，VIP和非VIP客戶可以返回相同路徑。

聯合後，您可以執行細分或排除來再次分割對象。

![](assets/read-segment-audience3.png)
