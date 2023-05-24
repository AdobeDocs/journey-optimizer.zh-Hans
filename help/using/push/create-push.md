---
solution: Journey Optimizer
product: journey optimizer
title: 配置推送通知
description: 了解如何在 Journey Optimizer 中创建推送通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 16%

---

# 创建推送通知 {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="推送消息创建"
>abstract="添加您的推送消息，并使用表达式编辑器开始对其进行个性化设置。"

## 在歷程或行銷活動中建立推播通知 {#create}

若要建立推播通知，請遵循下列步驟：

>[!BEGINTABS]

>[!TAB 新增推播至歷程]

1. 開啟您的歷程，然後從浮動視窗的「動作」區段拖放「推播」活動。

   ![](assets/push_create_1.png)

1. 提供訊息的基本資訊（標籤、說明、類別），然後選擇要使用的訊息介面。 此 **[!UICONTROL 表面]** 依預設，欄位會以使用者用於該管道的最後一個表面預填。

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >如果您從歷程傳送推播通知，您可以運用Adobe Journey Optimizer的傳送時間最佳化功能，根據歷史開啟和點按率，預測傳送訊息的最佳時機，最大化參與度。 [瞭解如何使用傳送時間最佳化](../building-journeys/journeys-message.md#send-time-optimization)

   有關如何設定歷程的詳細資訊，請參閱 [此頁面](../building-journeys/journey-gs.md)

1. 在歷程設定畫面中，按一下 **[!UICONTROL 編輯內容]** 按鈕來設定推播內容。 [設計推播通知](design-push.md)

1. 定义消息内容后，即可使用测试配置文件对其进行预览和测试。

1. 推送就緒後，完成設定 [歷程](../building-journeys/journey-gs.md) 以傳送。

   若要透過推播開放點和/或互動追蹤收件者的行為，請確定追蹤區段中的專用選項已在 [電子郵件活動](../building-journeys/journeys-message.md).

>[!TAB 新增推播至行銷活動]

1. 建立新的排程或API觸發的行銷活動，選取 **[!UICONTROL 推播通知]** 作為您的動作，然後選擇 **[!UICONTROL 應用程式表面]** 以使用。 [進一步瞭解推播設定](push-configuration.md).

   ![](assets/push_create_3.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 從 **[!UICONTROL 屬性]** 區段，編輯您的行銷活動 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]**.

   ![](assets/push_create_4.png)

1. 按一下 **[!UICONTROL 選取對象]** 按鈕，從可用的Adobe Experience Platform區段清單定義目標對象。 [了解详情](../segment/about-segments.md)。

1. 在 **[!UICONTROL 身分名稱空間]** 欄位中，選擇要使用的名稱空間，以識別所選區段中的個人。 [了解详情](../event/about-creating.md#select-the-namespace)。

   ![](assets/push_create_5.png)

1. 行銷活動的設計目的是要在特定日期或循環頻率執行。 瞭解如何設定 **[!UICONTROL 排程]** 中的行銷活動 [本節](../campaigns/create-campaign.md#schedule).

1. 從 **[!UICONTROL 動作觸發程式]** 功能表，選擇 **[!UICONTROL 頻率]** 推播通知的：

   * 一次
   * 每日
   * 每周
   * 每月

1. 在Campaign設定畫面中，按一下 **[!UICONTROL 編輯內容]** 按鈕來設定推播內容。 [設計推播通知](design-push.md)

1. 定义消息内容后，即可使用测试配置文件对其进行预览和测试。

1. 推送就緒後，完成設定 [行銷活動](../campaigns/create-campaign.md) 以傳送。

   若要透過推播開放點和/或互動追蹤收件者的行為，請確定追蹤區段中的專用選項已在 [行銷活動](../campaigns/create-campaign.md).

>[!ENDTABS]

**相关主题**

* [設定推播頻道](push-gs.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)

## 快速传递模式 {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="快速传递模式"
>abstract="快速传递模式让您可以在推送渠道上，在不超过 3000 万的受众规模下执行高速消息发送。"

快速傳送模式（先前在歷程中稱為高載模式）是 [!DNL Journey Optimizer] 附加元件可讓您透過行銷活動以非常快的速度傳送大量推送訊息。

當您想要在行動電話上傳送緊急推播警報（例如傳送突發新聞給已安裝您新聞頻道應用程式的使用者）時，訊息傳送延遲對業務至關重要，可使用快速傳送。

如需有關使用快速傳送模式時的效能的詳細資訊，請參閱 [Adobe Journey Optimizer產品說明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html).

### 先决条件 {#prerequisites}

快速傳送訊息功能需滿足下列需求：

* 快速傳送可用於 **[!UICONTROL 已排程]** 行銷活動專用，不適用於API觸發的行銷活動，
* 推送訊息中不允許個人化，
* 目標對象必須包含少於3,000萬個設定檔，
* 您可以使用快速傳送模式同時執行最多5個行銷活動。

### 啟動快速傳遞模式

1. 建立推播通知行銷活動，並開啟 **[!UICONTROL 快速傳遞]** 選項。

![](assets/create-campaign-burst.png)

1. 設定訊息內容並選取要定位的對象。 [瞭解如何建立行銷活動](#create)

   >[!IMPORTANT]
   >
   >確保訊息內容不包含任何個人化，且對象包含少於3,000萬個設定檔。

1. 照常檢閱並啟用您的行銷活動。 請注意，在測試模式中，訊息不會透過快速傳送模式傳送。