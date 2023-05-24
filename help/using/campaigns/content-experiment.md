---
solution: Journey Optimizer
product: journey optimizer
title: 建立內容實驗
description: 瞭解如何在行銷活動中建立內容實驗
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: 內容，實驗，多個，對象，處理
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
badge: label="Beta" type="Informative"
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 10%

---

# 创建内容试验 {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="内容体验"
>abstract="您可以选择改变投放内容、主题或发件人，以便定义多种投放处理方法并确定最适合您受众的组合。"

>[!BEGINSHADEBOX]

本文档包括以下内容：

* [内容试验入门](get-started-experiment.md)
* **[创建内容试验](content-experiment.md)**
* [了解统计计算](experiment-calculations.md)
* [配置实验报表](reporting-configuration.md)
* [实验报表中的统计计算](experiment-report-calculations.md)

>[!ENDSHADEBOX]

Journey Optimizer內容實驗可讓您定義多個傳送處理方式，以衡量哪個方式最適合您的目標對象。 您可以選擇變更傳遞內容、主旨或寄件者。 感興趣的對象會隨機分配給每個處理，以決定哪個處理在指定的量度方面效果最佳。

>[!NOTE]
>
>開始內容實驗之前，請確定您的報告設定已針對自訂資料集設定。 有关详细信息，请参阅[此部分](reporting-configuration.md)。

在下列範例中，傳遞目標已分割為兩個群組，每個群組代表目標人口的45%，以及一個保留群組10%，這些群組將不會收到傳遞。

目標對象中的每個人都會收到一個版本的電子郵件，主旨列是以下兩個版本之一：

* 直接推廣新系列和影像的10%優惠方案的使用者。
* 另一個只宣傳特殊優惠而沒有指定沒有任何影像的10%折扣。

此處的目標是檢視收件者是否會根據收到的實驗與電子郵件互動。 因此，我們將選擇 **[!UICONTROL 電子郵件開啟次數]** 作為此內容實驗中的主要目標量度。

![](assets/content_experiment.png)

## 建立您的行銷活動 {#campaign-experiment}

1. 從 **[!UICONTROL 行銷活動]** 頁面，按一下 **[!UICONTROL 建立行銷活動]**.

   ![](assets/content_experiment_1.png)

<!--
1. In the **[!UICONTROL Properties]** section, choose your **[!UICONTROL Campaign type]**:

    * **[!UICONTROL Scheduled]**: designed to send marketing messages and can be executed immediately or at a specified date.

    * **[!UICONTROL API-Triggered]**: designed to send transactional messages, such as password reset notifications or cart abandonment reminders. 
    
        To execute an API-triggered campaign, you will need to make an API call. [Learn more](api-triggered-campaigns.md)
-->
1. 選取您的頻道，然後 **[!UICONTROL 表面]** 您要用於此傳遞，然後按一下 **[!UICONTROL 建立]**. 如需詳細資訊，請參閱 [管道表面](../configuration/channel-surfaces.md) 頁面。

   ![](assets/content_experiment_2.png)

1. 設定 **[!UICONTROL 屬性]** 您的傳遞內容：
   * **[!UICONTROL 名称]**
   * **[!UICONTROL 描述]**

1. 定義要定位的對象。 若要這麼做，請按一下 **[!UICONTROL 選取對象]** 按鈕來顯示可用Adobe Experience Platform區段的清單。 [深入瞭解區段](../segment/about-segments.md)

   在 **[!UICONTROL 身分名稱空間]** 欄位中，選擇要使用的名稱空間，以識別所選區段中的個人。 [了解详情](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. 在 **[!UICONTROL 動作追蹤]** 區段，指定是否要追蹤收件者對傳送的反應：您可以追蹤點按和/或開啟。

   執行行銷活動後，即可從行銷活動報表存取追蹤結果。

1. 若要在特定日期或循環頻率執行行銷活動，請設定 **[!UICONTROL 排程]** 區段。 [了解详情](create-campaign.md)

1. 按一下 **[!UICONTROL 編輯內容]** 以開始個人化您的傳遞。 [了解详情](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. 從 **[!UICONTROL 編輯內容]** 視窗，開始個人化處理A。

   針對此處理方式，我們將直接在主旨行中指定特殊優惠方案，並新增個人化。

   ![](assets/content_experiment_5.png)

## 設定您的內容實驗 {#configure-experiment}

1. 當您的傳遞個人化時，從Campaign摘要頁面，按一下 **[!UICONTROL 建立實驗]** 以開始設定您的內容實驗。

   ![](assets/content_experiment_3.png)

1. 選取 **[!UICONTROL 成功量度]** 您想要為實驗設定。

   對於我們的實驗，我們選取 **[!UICONTROL 電子郵件開啟]** 測試收件者是否會開啟其電子郵件（如果促銷代碼在主題行中）。

   ![](assets/content_experiment_11.png)

1. 按一下 **[!UICONTROL 新增處理]** 以建立所需數量的新處理。

   ![](assets/content_experiment_8.png)

1. 變更 **[!UICONTROL 標題]** 以更佳地區分它們。

1. 選擇以新增 **[!UICONTROL 保留]** 群組至您的傳遞。 此群組將不會收到此行銷活動中的任何內容。

   開啟切換列會自動取得母體的10%，您可以視需要調整此百分比。

   ![](assets/content_experiment_12.png)

1. 然後，您可以選擇將精確百分比配置給每一個 **[!UICONTROL 處理]** 或只需開啟 **[!UICONTROL 平均分配]** 切換列。

   ![](assets/content_experiment_13.png)

1. 按一下 **[!UICONTROL 建立]** 設定您的設定時。

## 設計您的處理方式 {#treatment-experiment}

1. 從 **[!UICONTROL 編輯內容]** 視窗中，選取您的處理B以變更內容。

   在此，我們選擇不指定中的選件 **[!UICONTROL 主旨列]**.

   ![](assets/content_experiment_18.png)

1. 按一下 **[!UICONTROL 編輯電子郵件內文]** 以進一步個人化您的待遇B。

   ![](assets/content_experiment_9.png)

1. 設計您的處理方式後，按一下 **[!UICONTROL 更多動作]** 若要存取與處理相關的選項： **[!UICONTROL 重新命名]**， **[!UICONTROL 複製]** 和 **[!UICONTROL 刪除]**.

   ![](assets/content_experiment_7.png)

1. 如有需要，請存取 **[!UICONTROL 實驗設定]** 功能表以變更您的處理設定。

   ![](assets/content_experiment_19.png)

1. 定義訊息內容後，按一下 **[!UICONTROL 模擬內容]** 按鈕來控制傳遞的呈現，並使用測試設定檔檢查個人化設定。 [了解详情](../email/preview.md)

1. 當您的內容實驗準備就緒時，您可以從您的Campaign摘要頁面按一下 **[!UICONTROL 檢閱以啟動]** 以顯示行銷活動的摘要。 如果有任何引數不正確或遺失，則會顯示警報。

   ![](assets/content_experiment_15.png)

1. 檢查您的行銷活動是否已正確設定，然後按一下 **[!UICONTROL 啟動]** 以啟動它。

   ![](assets/content_experiment_14.png)

設定實驗與行銷活動後，您可以使用Campaign報告追蹤傳送成功。

## 目標報表 {#objectives-global}

>[!AVAILABILITY]
>
>內容實驗功能目前僅適用於一組組織（可用性限制）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/performance_report.gif)

此 **[!UICONTROL 目標]** Campaign報告的「 」索引標籤可讓您透過鎖定一個特定量度，更好地微調傳送的報告。

此 **[!UICONTROL 目標]** 清單連結至 **[!UICONTROL 資料集]** 定義系統連線，以擷取其他資訊。 內建清單 **[!UICONTROL 目標]** 可使用，但您可以透過新增來新增您自己的 **[!UICONTROL 資料集]**. 如需詳細程式，請參閱此 [區段](reporting-configuration.md).

選取您要鎖定目標之後，兩項 **[!UICONTROL 效能總覽]** 和 **[!UICONTROL 行銷活動目標]** Widget將提供您傳遞效能的詳細摘要。

使用 **[!UICONTROL 行銷活動目標]** widget，您也可以選擇將主要目標與其他量度比較。

請注意，如果需要，可以調整每個Widget的大小並將其刪除。 如需詳細資訊，請參閱此 [區段](../reports/global-report.md#modify-dashboard).

## 實驗報告 {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="成功量度"
>abstract="您之前在创建试验时选择的成功量度的总值，除以配置文件数。"

>[!AVAILABILITY]
>
>內容實驗功能目前僅適用於一組組織（可用性限制）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/experimentation_report_3.png)

從您的行銷活動 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 實驗]** tab會詳細說明與每個變體的表現以及是否有最佳表現相關的主要資訊。

請注意，定義績效最佳者可能需要一些時間，其將以此圖示表示 ![](assets/experimentation_report_1.png).

此 **[!UICONTROL 實驗結果]** Widget詳細說明每個變體的效能。 您可以變更基線，方法是從 **[!UICONTROL 基線]** 下拉式清單。 最佳處理方式將以星形圖示表示。

此表格會顯示下列量度：

* **[!UICONTROL 設定檔]**：針對此處理的設定檔數目。

* **[!UICONTROL 不重複傳出點按]**：跨傳出頻道的點按總數。

* **[!UICONTROL 每個設定檔計數]**：實驗目標量度的總值除以設定檔數量。

* **[!UICONTROL 信賴區間]**：基準線和績效最佳的處理之間的績效差異百分比。 [了解详情](../campaigns/experiment-calculations.md#confidence-intervals)。

* **[!UICONTROL 平均提升度]**：指定處理的轉換率超過基線的改善百分比。 [了解详情](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL 信賴度]**：指定處理與基準處理相同的證據。 [了解详情](../campaigns/experiment-calculations.md#understand-confidence)

如需這些結果的深入瞭解及如何解讀，請參閱 [此頁面](../campaigns/get-started-experiment.md#interpret-results).
