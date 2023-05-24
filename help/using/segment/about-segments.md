---
solution: Journey Optimizer
product: journey optimizer
title: 关于 Adobe Experience Platform 区段
description: 瞭解如何設定Adobe Experience Platform區段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 6c255d66fb89ba756add062d8a4315dd622fd8e7
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 9%

---

# 開始使用Adobe Experience Platform區段 {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="区段"
>abstract="通过利用实时客户配置文件数据，Adobe Experience Platform 让您能够轻松地创建目标区段，用于捕捉客户的独特行为和偏好。"

[!DNL Journey Optimizer]  可讓您直接從使用即時客戶個人檔案資料建立Adobe Experience Platform區段 **[!UICONTROL 區段]** 選單，並用於您的歷程或行銷活動。

此外，區段也可以從區段服務本身建立。 進一步瞭解 [Adobe Experience Platform Segmentation Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## 在中使用區段 [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

您可以在中運用區段 **[!DNL Journey Optimizer]** 以不同方式：

* 選擇區段作為 **行銷活動的對象**，此訊息會傳送給屬於所選區段的所有個人。 [瞭解如何定義行銷活動的對象](../campaigns/create-campaign.md#define-the-audience-audience).

* 使用 **讀取區段** 歷程中的協調活動，讓區段中的所有個人進入歷程並接收歷程中包含的訊息。

   假设您拥有“白银客户”客户细分。透過此活動，您可以讓所有銀級客戶進入歷程，並向他們傳送一系列個人化訊息。 [瞭解如何設定讀取區段活動](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* 使用 **區段資格** 歷程中的事件活動，用於根據Adobe Experience Platform區段入口和出口，讓個人進入歷程或是在歷程中前進。

   例如，您可以讓所有新的銀級客戶進入歷程，並向他們傳送訊息。 有關如何使用此活動的詳細資訊，請參閱 [瞭解如何設定區段資格活動](../building-journeys/segment-qualification-events.md).

* 使用 **條件** 歷程中的活動，以根據區段成員資格建立條件。 [瞭解如何在條件中使用區段](../building-journeys/condition-activity.md#using-a-segment).

## 對象評估方法{#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer中，對象是使用下列兩種評估方法之一從區段定義產生的：

* **串流區段**：當新資料流入系統時，區段的對象清單會即時保持最新。

   流式分段是一个持续的数据选择过程，它会更新区段以响应用户活动。建立並儲存區段後，區段定義會套用至傳入Journey Optimizer的資料。 這表示當個人設定檔資料變更時，系統就會在區段中新增或移除該個人，進而確保您的目標對象永遠相關。

* **批次細分**：每隔24小時評估區段的對象清單。

   批次細分是可透過區段定義一次處理所有設定檔資料的串流細分的替代方法。 這會建立對象的快照，可儲存並匯出以供使用。 不過，與串流細分不同，批次細分不會持續即時更新對象清單，而且批次程式之後傳入的新資料不會反映在區段中，直到下一個批次程式。」

系統會根據評估區段規則的複雜性和成本，針對每個區段定義來決定批次區段和串流區段之間的劃分。 您可以檢視中每個區段的評估方法 **[!UICONTROL 評估方法]** 區段清單的欄。

![](assets/evaluation-method.png)

>[!NOTE]
>
>如果 **[!UICONTROL 評估方法]** 欄不顯示，您需要使用清單右上角的設定按鈕新增它。

在您首次定義區段後，設定檔只要符合資格，就會新增至對象。

從先前資料回填對象最長可能需要24小時。 回填對象後，對象會持續保持最新狀態，並隨時準備好進行目標定位。
