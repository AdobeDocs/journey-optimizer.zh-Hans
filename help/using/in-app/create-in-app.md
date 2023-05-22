---
title: 建立應用程式內通知
description: 瞭解如何在Journey Optimizer中建立應用程式內訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内、消息、创建、入门
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 9bebcde9edde40a0fadba34d8b40757036a6436d
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 6%

---

# 创建应用程序内消息 {#create-in-app}

<!--
>[!BEGINTABS]

>[!TAB Add an In-app message to a journey]

>[!AVAILABILITY]
>
>The In-app activity is currently available as a beta to select users only. To join the beta program, contact Adobe Customer Care.

1. Open your journey, then drag and drop an **[!UICONTROL In-app]** activity from the **[!UICONTROL Actions]** section of the palette.

    When a profile reaches the end of their journey, any in-app messages displayed to them will automatically expire. For that reason, a Wait activity is automatically added after your In-app activity to ensure proper timing.

    ![](assets/in_app_journey_1.png)

1. Enter a **[!UICONTROL Label]** and **[!UICONTROL Description]** for your message.

1. Choose the [In-app surface](inapp-configuration.md) to use.

    ![](assets/in_app_journey_2.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. [Learn more](design-in-app.md)

1. Click **[!UICONTROL Edit trigger]** to configure your Trigger. 

    ![](assets/in_app_journey_4.png)

1. Choose the frequency of your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. From the **[!UICONTROL Mobile app trigger]** dropdown(s), choose the event(s) and criteria that will trigger your message:

    1. From the left drop-down, select the event required to trigger the message.
    1. From the right drop-down, select the validation required on the selected event.
    1. Click the **[!UICONTROL Add]** button if you want the trigger to consider multiple events or criteria. Then, repeat the steps above.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.
    1. Click **[!UICONTROL Save]** when your Triggers have been configured.

    ![](assets/in_app_journey_3.png)
    
1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Learn more](../building-journeys/about-journey-activities.md)

1. Once your In-app message is ready, finalize the configuration and publish your journey to activate it.

For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md).

>[!TAB Add an In-app message to a campaign]
-->

1. 存取 **[!UICONTROL 行銷活動]** 功能表，然後按一下 **[!UICONTROL 建立行銷活動]**.

1. 在 **[!UICONTROL 屬性]** 區段，選取行銷活動執行型別：已排程或API觸發。 進一步瞭解中的行銷活動型別 [此頁面](../campaigns/create-campaign.md#campaigntype).

1. 在 **[!UICONTROL 動作]** 區段，選擇 **[!UICONTROL 應用程式內訊息]** 和 **[!UICONTROL 應用程式表面]** 先前為您的應用程式內訊息所設定。 然後，按一下 **[!UICONTROL 建立]**.

   進一步瞭解中的應用程式內設定 [此頁面](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. 從 **[!UICONTROL 屬性]** 區段，輸入 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]** 說明。

1. 若要將自訂或核心資料使用標籤指派給應用程式內訊息，請選取 **[!UICONTROL 管理存取權]**. [了解详情](../administration/object-based-access.md)。

1. 按一下 **[!UICONTROL 選取對象]** 按鈕，從可用的Adobe Experience Platform區段清單定義目標對象。 [了解详情](../segment/about-segments.md)。

   ![](assets/in_app_create_2.png)

1. 在 **[!UICONTROL 身分名稱空間]** 欄位中，選擇要使用的名稱空間，以識別所選區段中的個人。 [了解详情](../event/about-creating.md#select-the-namespace)。

1. 按一下 **[!UICONTROL 編輯觸發程式]** 若要選擇將觸發訊息的事件和條件：

   1. 按一下 **新增條件** 如果您希望觸發器考量多個事件或條件。
   1. 選取事件的連結方式，例如，選擇 **[!UICONTROL 和]** 如果您需要 **兩者** 觸發器設為true，以便顯示或選擇訊息 **[!UICONTROL 或]** 如果您想要顯示訊息，如果 **兩者之一** 的觸發程式為true。
   1. 按一下 **[!UICONTROL 建立群組]** 將觸發程式群組在一起。

   ![](assets/in_app_create_3.png)

1. 選擇應用程式內訊息生效時的觸發頻率。 可以使用以下选项：

   * **[!UICONTROL 每次]**：一律顯示中選取的事件時的訊息 **[!UICONTROL 行動應用程式觸發程式]** 下拉式清單隨即出現。
   * **[!UICONTROL 一次]**：只會在中第一次選取事件時顯示此訊息 **[!UICONTROL 行動應用程式觸發程式]** 下拉式清單隨即出現。
   * **[!UICONTROL 直到點進為止]**：當在中選取事件時顯示此訊息 **[!UICONTROL 行動應用程式觸發程式]** 下拉式清單會一直出現，直到SDK以「已點按」的動作傳送互動事件為止。
   * **[!UICONTROL X次數]**：顯示此訊息X次。

1. 如有需要，請選擇要 **[!UICONTROL 星期]** 或 **[!UICONTROL 時間]** 將會顯示應用程式內訊息。

1. 行銷活動的設計目的是要在特定日期或循環頻率執行。 瞭解如何設定 **[!UICONTROL 排程]** 中的行銷活動 [本節](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. 您現在可以開始使用設計內容 **[!UICONTROL 編輯內容]** 按鈕。 [了解详情](design-in-app.md)

   ![](assets/in_app_create_4.png)

<!--
>[!ENDTABS]
-->

## 操作方法视频{#video}

以下影片說明如何在行銷活動中建立、設定和發佈應用程式內訊息。

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**相关主题：**

* [設計應用程式內訊息](design-in-app.md)
* [測試並傳送您的應用程式內訊息](send-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
* [應用程式內設定](inapp-configuration.md)