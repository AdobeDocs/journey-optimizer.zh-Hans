---
solution: Journey Optimizer
product: journey optimizer
title: 區段資格事件
description: 了解客户细分资格事件
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 資格，事件，區段，歷程，平台
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 53%

---

# 區段資格事件 {#segment-qualification}

## 关于客户细分资格事件{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="区段鉴别事件"
>abstract="此活动允许您的历程侦听 Adobe Experience Platform 区段中配置文件的进入和退出，以便使个人进入历程或在历程中向前推进。"

此活动允许您的历程侦听 Adobe Experience Platform 区段中配置文件的进入和退出，以便使个人进入历程或在历程中向前推进。有关创建客户细分的更多信息，请参阅此[部分](../segment/about-segments.md)。

假设您拥有“白银客户”客户细分。通过此活动，您可以使所有新的白银客户进入历程，并向其发送一系列个性化消息。

此类事件可定位为历程的第一步或后续步骤。

>[!IMPORTANT]
>
>请记住，Adobe Experience Platform 客户细分每天计算一次（**批处理**&#x200B;客户细分）或实时计算（**流式处理**&#x200B;客户细分，使用 Adobe Experience Platform 的“高频受众”选项）。
>
>如果对所选客户细分进行流式处理，则属于此客户细分的个人可能会实时进入该历程。如果區段為批次，則新符合此區段資格的人可能會在Adobe Experience Platform上執行區段計算時進入歷程。
>
>以读取区段、区段鉴别或业务事件活动开始的历程中，无法使用体验事件字段组。


1. 展開 **[!UICONTROL 事件]** 類別與放置 **[!UICONTROL 區段資格]** 活動放入您的畫布。

   ![](assets/segment5.png)

1. 新增 **[!UICONTROL 標籤]** 至活動。 此步骤是可选的。

1. 按一下 **[!UICONTROL 區段]** 欄位並選取您要運用的區段。

   >[!NOTE]
   >
   >请注意，您可以自定义列表中显示的列，并对其进行排序。

   ![](assets/segment6.png)

   新增區段後， **[!UICONTROL 複製]** 按鈕可讓您複製其名稱和ID：

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. 在 **[!UICONTROL 行為]** 欄位，選擇您要監聽區段入口、出口或兩者。

   >[!NOTE]
   >
   >請注意 **[!UICONTROL 輸入]** 和 **[!UICONTROL 退出]** 對應至 **已實現** 和 **已退出** 來自Adobe Experience Platform的區段參與狀態。 如需如何評估區段的詳細資訊，請參閱 [Segment Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target="_blank"}.

1. 选择命名空间。只有在將事件定位為歷程的第一步時，才需要此專案。 依預設，欄位會使用上次使用的名稱空間預先填入。

   >[!NOTE]
   >
   >您只能選取以人物為基礎的身分名稱空間。 如果您已定義查閱表格的名稱空間（例如：產品查閱的ProductID名稱空間），它將無法在 **名稱空間** 下拉式清單。

   ![](assets/segment7.png)

有效负荷包含以下可以在条件和操作中使用的上下文信息：

* 行为（入口、出口）
* 资格时间戳
* 客户细分 ID

在後續的條件或動作中使用運算式編輯器時 **[!UICONTROL 區段資格]** 活動，則您可存取 **[!UICONTROL 區段資格]** 節點。 您可以選擇 **[!UICONTROL 上次合格時間]** 和 **[!UICONTROL 狀態]** （進入或退出）。

请参阅[条件活动](../building-journeys/condition-activity.md#about_condition)。

![](assets/segment8.png)

包含區段資格事件的新歷程在發佈十分鐘後即可運作。 此時間間隔對應於專用服務的快取重新整理間隔。 因此，您必須等待十分鐘才能使用此歷程。

## 最佳实践 {#best-practices-segments}

此 **[!UICONTROL 區段資格]** 活動可讓在Adobe Experience Platform區段中取得資格或被取消資格的個人在歷程中立即進入。

该信息的接收速度很快。所做的测量显示速度为每秒接收 10,000 个事件。因此，您应该确保了解入口峰值可能如何出现、如何避开，以及如何使历程针对此类情况做好准备。

### 批处理客户细分{#batch-speed-segment-qualification}

在对批处理客户细分使用客户细分资格时，请注意，在每日计算时将出现入口峰值。峰值的大小将取决于每天进入（或退出）客户细分的个人数量。

此外，如果在历程中新建并立即使用批处理客户细分，则第一批计算可能会使大量个人进入历程。

### 流式处理客户细分{#streamed-speed-segment-qualification}

在对流式处理客户细分使用客户细分资格时，由于持续评估客户细分，因此入口/出口出现大量峰值的风险较小。如果客户细分定义导致大量客户同时获得资格，则仍然可能出现峰值。

如需串流區段的詳細資訊，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### 如何避免过载{#overloads-speed-segment-qualification}

以下是一些最佳實務，有助於避免在歷程中運用的系統過載（資料來源、自訂動作、管道動作活動）。

請勿使用，在 **[!UICONTROL 區段資格]** 活動，批次區段建立後立即生效。 它将避免第一个计算峰值。请注意，如果您要使用从未计算的客户细分，则历程画布中将显示黄色警告。

![](assets/segment-error.png)

為歷程中使用的資料來源和動作設定上限規則，以避免其過載。 進一步瞭解 [Journey Orchestration檔案](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target="_blank"}. 请注意，上限规则不带重试。如果您需要重試，您必須核取方塊，以在歷程中使用替代路徑 **[!UICONTROL 在逾時或錯誤的情況下新增替代路徑]** 在條件或動作中。

在生产历程中使用客户细分之前，请始终首先评估每天符合此客户细分条件的个人数量。若要這麼做，您可以檢查 **[!UICONTROL 區段]** 功能表，開啟區段，然後檢視 **[!UICONTROL 一段時間的設定檔]** 圖表。

![](assets/segment-overload.png)
