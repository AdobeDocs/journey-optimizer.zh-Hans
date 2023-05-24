---
solution: Journey Optimizer
product: journey optimizer
title: 与 Adobe Campaign Standard 集成
description: 瞭解如何將Journey Optimizer與Adobe Campaign Standard整合
feature: Actions
topic: Administration
role: Admin,Developer
level: Intermediate
keywords: campaign， standard，整合，上限，動作
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 5%

---

# 与 Adobe Campaign Standard 集成 {#using_adobe_campaign_standard}

您可以使用Adobe Campaign Standard的「交易訊息」功能來傳送電子郵件、推播通知和簡訊。

如果您有Adobe Campaign Standard，則可使用內建動作來連線至Adobe Campaign Standard。

必須發佈Campaign Standard交易式訊息及其相關事件，才能在Journey Optimizer中使用。 如果事件已發佈，但訊息尚未發佈，則不會顯示在Journey Optimizer介面中。 如果訊息已發佈，但其關聯事件尚未發佈，則會顯示在Journey Optimizer介面中，但無法使用。

## 重要说明 {#important-notes}

* Adobe Campaign Standard動作會自動定義每5分鐘4000次呼叫的上限規則。 這與Adobe Campaign Standard交易式訊息的官方規模相對應。 閱讀中有關交易式訊息傳送SLA的詳細資訊 [Adobe Campaign Standard產品說明](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html).

* Adobe Campaign Standard整合是透過動作清單中的專屬內建動作來設定。 需要為每個沙箱設定此設定。

* 您無法搭配「區段」資格或「讀取區段」活動使用Campaign Standard動作。

* 歷程不能同時使用訊息和Campaign Standard動作。

## 設定動作 {#configure-action}

以下是設定它的步驟：

1. 選取 **[!UICONTROL 設定]** 在「管理」選單區段中。 在  **[!UICONTROL 動作]** 區段，按一下 **[!UICONTROL 管理]**. 将显示操作列表。

1. 選取內建 **[!UICONTROL AdobeCampaignStandard]** 動作。 動作設定窗格會在畫面右側開啟。

   ![](assets/actioncampaign.png)

1. 複製您的Adobe Campaign Standard執行個體URL並貼到 **[!UICONTROL URL]** 欄位。

1. 按一下 **[!UICONTROL 測試執行個體URL]** 以測試例項的有效性。

   >[!NOTE]
   >
   >此測試會驗證：
   >
   >主機為「.campaign.adobe.com」、「.campaign-sandbox.adobe.com」、「.campaign-demo.adobe.com」、「.ats.adobe.com」或「.adls.adobe.com」。
   >
   >URL以https開頭，
   >
   >與此Adobe Campaign Standard例項關聯的組織與Journey Optimizer的組織相同。

設計您的歷程時，三個動作將適用於 **[!UICONTROL 動作]** 類別： **[!UICONTROL 電子郵件]**， **[!UICONTROL 推播]**， **[!UICONTROL 簡訊]** (請參閱 [使用Adobe Campaign動作](../building-journeys/using-adobe-campaign-standard.md))。

![](assets/journey58.png)

您可以使用 **回應** 事件，用於回應相同歷程中傳送之Campaign Standard訊息的相關追蹤資料。 對於推播通知，您可以對點選、傳送或失敗的訊息做出反應。 對於SMS訊息，您可以對已傳送或失敗的訊息做出反應。 對於電子郵件，您可以對點選、傳送、開啟或失敗的訊息做出反應。 另請參閱 [回應事件](../building-journeys/reaction-events.md).

如果您使用協力廠商系統來傳送訊息，則需要新增及設定自訂動作。 另請參閱 [關於自訂動作組態](../action/about-custom-action-configuration.md).
