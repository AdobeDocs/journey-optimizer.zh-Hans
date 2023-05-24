---
solution: Journey Optimizer
product: journey optimizer
title: 创建电子邮件
description: 了解如何在 Journey Optimizer 中创建电子邮件
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 建立，電子郵件，開始，歷程，行銷活動
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 9%

---

# 创建电子邮件 {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="电子邮件创建"
>abstract="只需三个简单的步骤即可定义您的电子邮件参数。"

若要在中建立電子郵件 [!DNL Journey Optimizer]，請遵循下列步驟。

## 在歷程或行銷活動中建立電子郵件 {#create-email-journey-campaign}

新增 **[!UICONTROL 電子郵件]** 對歷程或行銷活動的動作，並根據您的案例遵循以下步驟。

>[!BEGINTABS]

>[!TAB 新增電子郵件至歷程]

1. 開啟您的歷程，然後拖放 **[!UICONTROL 電子郵件]** 活動來自 **[!UICONTROL 動作]** 區段。

1. 提供訊息的基本資訊（標籤、說明、類別）。

1. 選擇 [電子郵件表面](email-settings.md) 以使用。

   ![](assets/email_journey.png)

   依預設，此欄位會預先填入使用者用於該管道的最後一個表面。

>[!NOTE]
>
>如果您從歷程傳送電子郵件，您可以運用Adobe Journey Optimizer的傳送時間最佳化功能，根據歷史開啟和點按率，預測傳送訊息的最佳時機，最大化參與度。 [瞭解如何使用傳送時間最佳化](../building-journeys/journeys-message.md#send-time-optimization)

有關如何設定歷程的詳細資訊，請參閱 [此頁面](../building-journeys/journey-gs.md).

>[!TAB 新增電子郵件至行銷活動]

1. 建立新的排程或API觸發的行銷活動，並選取 **[!UICONTROL 電子郵件]** 作為您的動作。

1. 選擇 [電子郵件表面](email-settings.md) 以使用。

   ![](assets/email_campaign.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 完成步驟以建立電子郵件行銷活動，例如行銷活動屬性、 [對象](../segment/about-segments.md)、和 [排程](../campaigns/create-campaign.md#schedule).

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

有關如何設定行銷活動的詳細資訊，請參閱 [此頁面](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## 定義您的電子郵件內容 {#define-email-content}

<!-- update the quarry component with right ID value-->

>[!CONTEXTUALHELP]
>id="test_id"
>title="配置电子邮件内容"
>abstract="创建电子邮件的内容。定义其主题，然后利用电子邮件设计器构建和个性化电子邮件正文。"

1. 在歷程或行銷活動設定畫面中，按一下 **[!UICONTROL 編輯內容]** 按鈕以設定電子郵件內容。 [了解详情](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. 在 **[!UICONTROL 頁首]** 部分 **[!UICONTROL 編輯內容]** 畫面， **[!UICONTROL 發件人名稱]**， **[!UICONTROL 從電子郵件]** 和 **[!UICONTROL 密件副本]** 欄位來自您選取的電子郵件表面。 [了解详情](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. 您可以新增主旨列。 直接在對應欄位中輸入純文字，或使用 [運算式編輯器](../personalization/personalization-build-expressions.md) 以個人化您的主旨列。

1. 按一下 **[!UICONTROL 編輯電子郵件內文]** 按鈕以開始建立您的內容 [!DNL Journey Optimizer] 電子郵件設計工具。 [了解详情](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. 如果您在行銷活動中，也可以按一下 **[!UICONTROL 代碼編輯器]** 按鈕來使用顯示的快顯視窗，以純HTML編碼您自己的內容。

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >如果您已透過電子郵件設計工具建立或匯入內容，此內容將會以HTML顯示。

## 检查警报 {#check-email-alerts}

當您設計訊息時，如果關鍵設定遺失，警示會顯示在介面（畫面右上方）中。

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>如果您沒有看到此按鈕，則表示未偵測到任何警示。

系統檢查的設定和元素如下所列。 您也會找到有關如何調整設定以解決相應問題的資訊。

可能會發生兩種型別的警報：

* **警告** 請參閱建議與最佳實務，例如：

   * **[!UICONTROL 電子郵件內文中不存在選擇退出連結]**：將取消訂閱連結新增至您的電子郵件內文為最佳實務。 瞭解如何在中設定它 [本節](../privacy/opt-out.md#opt-out-management).

      >[!NOTE]
      >
      >营销类型电子邮件必须包含选择退出链接，这对于事务型邮件不是必需的。訊息類別(**[!UICONTROL 行銷]** 或 **[!UICONTROL 異動]**)定義於 [管道表面](email-settings.md#email-type) 層級與時間 [建立訊息](#create-email-journey-campaign) 來自歷程或行銷活動。

   * **[!UICONTROL HTML的文字版本為空白]**：別忘了定義電子郵件內文的文字版本，因為當HTML內容無法顯示時將使用該版本。 瞭解如何在中建立文字版本 [本節](text-version-email.md).

   * **[!UICONTROL 電子郵件內文中存在空白連結]**：檢查電子郵件中的所有連結是否正確。 瞭解如何在中管理內容和連結 [本節](content-from-scratch.md).

   * **[!UICONTROL 電子郵件大小已超過100KB的限制]**：為獲得最佳傳送方式，請確定您的電子郵件大小不超過100KB。 瞭解如何在中編輯電子郵件內容 [本節](content-from-scratch.md).

* **錯誤** 防止您測試或啟動歷程/行銷活動，只要它們未解決，例如：

   * **[!UICONTROL 缺少主旨列]**：電子郵件主旨行是必填欄位。 瞭解如何在中定義及個人化它 [本節](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL 訊息的電子郵件版本為空白]**：尚未設定電子郵件內容時會顯示此錯誤。 瞭解如何在中設計電子郵件內容 [本節](get-started-email-design.md).

   * **[!UICONTROL 表面不存在]**：如果您選取的表面在建立訊息後遭到刪除，則無法使用訊息。 如果發生此錯誤，請在訊息中選取另一個曲面 **[!UICONTROL 屬性]**. 進一步瞭解中的管道表面 [本節](../configuration/channel-surfaces.md).


>[!CAUTION]
>
>若要能夠使用電子郵件測試或啟用歷程/行銷活動，您必須解決所有 **錯誤** 警報。

## 預覽並傳送您的電子郵件

定義訊息內容後，您可以預覽該內容以控制電子郵件的呈現，並使用測試設定檔檢查個人化設定。 [了解详情](preview.md)

![](assets/email_designer_edit_simulate.png)

當您的電子郵件準備就緒時，請完成 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md)，並啟動以傳送訊息。

>[!NOTE]
>
>若要透過電子郵件開啟次數和/或互動來追蹤收件者的行為，請確定 **[!UICONTROL 追蹤]** 區段已在歷程啟用 [電子郵件活動](../building-journeys/journeys-message.md) 或在電子郵件中 [行銷活動](../campaigns/create-campaign.md).<!--to move?-->

<!--

## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] Expression editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 

-->

