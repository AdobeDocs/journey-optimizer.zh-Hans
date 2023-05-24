---
solution: Journey Optimizer
product: journey optimizer
title: 使用 Customer Journey Analytics
description: 開始使用Customer Journey Analytics
feature: Reporting
topic: Content Management
role: User
level: Beginner
exl-id: 5349b0cf-da4e-458c-89be-c75a38e4721a
source-git-commit: 0e45d6e4995f4f21dc5122203b715ae999e2b760
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 11%

---

# 使用 [!DNL Customer Journey Analytics] {#cja-ajo}


[!DNL Journey Optimizer] 與整合 [!DNL Customer Journey Analytics] 透過自動化報告發佈和自訂資料視覺效果，提供您所有歷程的整體檢視。

![](assets/cja.png)

在中建立您的歷程後 [!DNL Journey Optimizer]，您可以將客戶資料匯入 [!DNL Customer Journey Analytics] 以開始報告並瞭解客戶與您的歷程每次互動的影響。

➡️ [探索Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-landing.html){target="_blank"}

>[!NOTE]
>
>除了這項整合外，您也可以將Adobe Journey Optimizer資料集的內容匯出至雲端儲存位置，並將這項資訊用於報表或分析用途。 [瞭解如何將資料集匯出至雲端儲存位置](../data/export-datasets.md)
>
>請注意，資料集匯出功能目前為測試版，可供所有Adobe Journey Optimizer使用者使用。 如果您尚未拥有访问权限，请与 Adobe 代表联系，获取目标的访问权限。

使用前 [!DNL Customer Journey Analytics] 對於您的歷程，您必須先設定此整合：

1. [建立連線](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=zh-Hans) 在 [!DNL Customer Journey Analytics] 使用 **[!UICONTROL 資料集]** 您要傳送至Adobe Experience Platform。

   下列專案 [!DNL Journey Optimizer] 可以設定：
   * [歷程步驟事件](../data/datasets-query-examples.md#journey-step-event)：可讓您檢視誰進入您的歷程以及他們到達的距離。
   * [訊息回饋/追蹤資料集](../data/datasets-query-examples.md#message-feedback-event-dataset)：可讓您檢視所傳送訊息的傳遞資訊 [!DNL Journey Optimizer].
   * [實體和歷程資料集](../data/datasets-query-examples.md#entity-dataset)：可讓您搜尋好記的名稱，並在報表中使用這些名稱。

1. [建立資料檢視](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html) 以設定您要用於報表的維度和量度。

   您可以建立Journey Optimizer特定量度，以便更妥善地反映您的歷程資料。 [了解详情](https://experienceleague.adobe.com/docs/analytics-platform/using/integrations/ajo.html#configure-the-data-view-to-accommodate-journey-optimizer-dimensions-and-metrics)

使用 [!DNL Journey Optimizer] 替換為 [!DNL Customer Journey Analytics] 可能導致報表資料中的差異，原因如下：

* **兩者 [!DNL Journey Optimizer] 和 [!DNL Customer Journey Analytics] 從Azure Data Lake Storage (ADLS)同步資料以進行報告。**

   不同產品的傳入資料處理時間可能略有不同。 因此，顯示從指定日期到當天的報表時，資料可能不一致。 若要減少差異，請使用排除當天的日期範圍。

* **在 [!DNL Journey Optimizer] 報表，傳送的量度也包含「重試」量度。**

   **[!UICONTROL 重試]** 將不會包含在 **[!UICONTROL 已傳送]** 中的量度 [!DNL Customer Journey Analytics]. 這將導致 [!DNL Customer Journey Analytics] **[!UICONTROL 已傳送]** 顯示小於以下值的量度 [!DNL Journey Optimizer]. 不過，重試資料會融合至 **[!UICONTROL 訊息已成功傳送]** 或 **[!UICONTROL 彈回數]** 量度。
若要減少不一致的情況，請使用一週前或之後的日期範圍。

* **報告是從不同的資料來源提供。**

   這可能會導致產品之間出現1-2%的資料差異。
