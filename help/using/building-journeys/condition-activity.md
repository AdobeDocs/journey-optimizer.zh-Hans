---
solution: Journey Optimizer
product: journey optimizer
title: 条件活动
description: 瞭解條件活動
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 活動，條件，畫布，歷程
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
source-git-commit: 603174032552214686cc0f2b9ea0854f348ce949
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 17%

---

# 条件活动{#condition-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_condition"
>title="条件活动"
>abstract="此活动允许您定义个人在历程中的流动方式。根据不同的标准，将会创建多条路径。您还可以创建在出现超时或错误时的替代路径。"

可使用下列型別的條件：

* [資料來源條件](#data_source_condition)
* [時間條件](#time_condition)
* [百分比分割](#percentage_split)
* [日期條件](#date_condition)
* [設定檔上限](#profile_cap)

![](assets/journey49.png)

## 關於條件活動 {#about_condition}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_simple"
>title="关于简单表达式编辑器"
>abstract="使用简单表达式编辑器模式，您可以根据字段组合执行简单查询。所有可用的字段都显示在屏幕的左侧。将字段拖放到主区域中。要组合不同元素，请将它们互相联锁，以创建不同的分组和/或分组级别。然后，您可以选择逻辑运算符来组合同一级别上的元素。"

在歷程中使用數個條件時，您可以為每個條件定義標籤，以便更輕鬆地加以識別。

按一下 **[!UICONTROL 新增路徑]** 如果要定義多個條件。 對於每個條件，新路徑都會在活動後新增到畫布中。

![](assets/journey47.png)

請注意，歷程的設計具有功能影響。 在條件之後定義數個路徑時，只會執行第一個符合條件的路徑。 這表示您可以透過將路徑置於彼此上方或下方來改變路徑的優先順序。

例如，以第一個路徑的條件「Person is a VIP」以及第二個路徑的條件「Person is a male」為例。 如果符合兩個條件的人(身為VIP的男性)通過此步驟，即使此人也有資格使用第二個路徑，也會選擇第一個路徑，因為第一個路徑「在上」。 若要變更此優先順序，請以其他垂直順序移動您的活動。

![](assets/journey48.png)

您可以針對不符合所定義條件的對象建立其他路徑，方法是勾選 **[!UICONTROL 顯示上述案例以外的其他案例的路徑]**. 請注意，此選項不適用於分割條件。 另請參閱 [百分比分割](#percentage_split).

簡單模式可讓您根據欄位的組合執行簡單查詢。 所有可用的字段都显示在屏幕的左侧。将字段拖放到主区域中。要组合不同元素，请将它们互相联锁，以创建不同的分组和/或分组级别。然后，您可以选择逻辑运算符来组合同一级别上的元素：

* AND：兩個條件的交集。 只會考慮符合所有條件的元素。
* 或：兩個條件的聯合。 考虑至少符合一个条件的元素。

![](assets/journey64.png)

如果您使用 [Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target="_blank"} 若要建立區段，您可以在歷程條件中運用它們。 請參閱 [在條件中使用區段](../building-journeys/condition-activity.md#using-a-segment).


>[!NOTE]
>
>使用簡單編輯器無法對時間序列執行查詢（例如購買清單、過去對訊息的點按）。 為此，您需要使用進階編輯器。 请参阅[此页](expression/expressionadvanced.md)。

当操作或条件中发生错误时，个人历程将停止。唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL 在逾時或錯誤的情況下新增替代路徑]**. 请参阅[此小节](../building-journeys/using-the-journey-designer.md#paths)。

在簡單編輯器中，您也會在事件和資料來源類別下方找到歷程屬性類別。 此類別包含與給定設定檔的歷程相關的技術欄位。 这是系统从实时历程中检索到的信息，如历程 ID 或遇到的特定错误。[了解详情](expression/journey-properties.md)

## 資料來源條件 {#data_source_condition}

這可讓您根據資料來源或先前位於歷程中事件的欄位來定義條件。 瞭解如何在中使用運算式編輯器 [本節](expression/expressionadvanced.md).

使用進階運算式編輯器，您可以設定更進階的條件，以操控集合或使用需要傳遞引數的資料來源。 [了解详情](../datasource/external-data-sources.md)。

![](assets/journey50.png)

## 時間條件{#time_condition}

這可讓您根據一天中的小時和/或星期來執行不同的動作。 例如，您可以決定在白天傳送推播通知，在工作日於夜間傳送電子郵件。

>[!NOTE]
>
>時區不是條件專屬的時區，而是在歷程屬性中的歷程層級定義。 请参见[此页面](../building-journeys/timezone-management.md)。

![](assets/journey51.png)

有三個篩選選項可供使用：

* 小時：可讓您根據一天中的時間設定條件。 然後定義開始和結束時間。 個人只能在已定義的時數範圍內輸入路徑。
* 星期：可讓您根據星期設定條件。 然後，選取您希望個人輸入路徑的日期。
* 星期幾和小時：此選項會結合前兩個選項。

## 百分比分割 {#percentage_split}

此選項可讓您隨機分割對象，以針對每個群組定義不同的動作。 定義每個路徑的分割數與重新分割。 分割計算是統計性的，因為系統無法預測有多少人會在此歷程活動中流動。 因此，分割的誤差邊界非常低。 此函式以Java隨機機製為基礎(請參閱此 [頁面](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html))。

在測試模式中，達到分割時，一律會選擇頂端分支。 如果您希望測試選擇不同的路徑，可以重新組織分割分支的位置。 请参见[此页面](../building-journeys/testing-the-journey.md)。

>[!NOTE]
>
>請注意，在百分比分割條件中沒有按鈕可新增路徑。 路徑數目將取決於分割數目。 在分割條件中，您無法新增其他情況的路徑，因為它不會發生。 人們總是會進入其中一個分割路徑。

![](assets/journey52.png)

## 日期條件 {#date_condition}

這可讓您根據日期定義不同的流程。 例如，如果人員在「銷售」期間進入步驟，您會將特定訊息傳送給他們。 在餘下的年份，您將傳送另一則訊息。

>[!NOTE]
>
>時區不再為條件所特有，現在已在歷程屬性中的歷程層級定義。 请参阅[此页](../building-journeys/timezone-management.md)。

![](assets/journey53.png)

## 設定檔上限 {#profile_cap}

使用此條件型別可設定歷程路徑的設定檔數目上限。 达到此限制后，输入的用户档案会采用替代路径。 這可確保您的歷程絕不會超過定義的限制。

>[!NOTE]
>
>建議您定義高值設定檔上限。 母體達到確切上限數目的精確度和可能性只會隨著上限的增加而增加。 對於小數字（例如50的上限），數字將不能始終相符，因為在設定檔採取替代路徑之前可能未達到限制。

您可以使用此條件型別來增加傳送量。 檢視此 [使用案例](ramp-up-deliveries-uc.md).

預設上限為1000。

計數器僅適用於選取的歷程版本。 重複歷程或建立新版本時，計數器會重設為零。 重設後，輸入的設定檔會再次採用公稱路徑，直到達到計數器限製為止。

在週期性歷程上定義設定檔上限時，計數器不會在每次週期性之後重設。

即使您將替代路徑移動到歷程畫布上的名義路徑上方，名義路徑始終優先於替代路徑。

對於即時歷程，需要考量以下臨界值以確保達到限制：

* 對於大於10000的上限，要插入的相異設定檔數量必須至少為上限的1.3倍。
* 對於低於10000的上限，要插入的相異設定檔數量必須是1000加上上限。

在測試模式中未考慮設定檔上限。

![](assets/profile-cap-condition.png)

## 在条件中使用区段 {#using-a-segment}

本節說明如何在歷程條件中使用區段。 如需區段及如何建立區段的詳細資訊，請參閱 [本節](../segment/about-segments.md).

若要在歷程條件中使用區段，請遵循下列步驟：

1. 開啟歷程，拖放 **[!UICONTROL 條件]** 活動並選擇 **資料來源條件**.
   ![](assets/journey47.png)

1. 按一下 **[!UICONTROL 新增路徑]** 每個需要的額外路徑。 對於每個路徑，按一下 **[!UICONTROL 運算式]** 欄位。

   ![](assets/segment3.png)

1. 在左側，展開 **[!UICONTROL 區段]** 節點。 拖放您要用於條件的區段。 依預設，區段的條件為true。

   ![](assets/segment4.png)

   >[!NOTE]
   >
   >請注意，只有個人擁有 **已實現** 和 **現有** 區段參與狀態會視為區段的成員。 如需如何評估區段的詳細資訊，請參閱 [Segment Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.
