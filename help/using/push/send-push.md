---
solution: Journey Optimizer
product: journey optimizer
title: 預覽和測試推播通知
description: 瞭解如何在Journey Optimizer中預覽和測試推播通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 9%

---

# 預覽和測試推播通知 {#send-push}

## 預覽推播通知 {#preview-push}

定义消息内容后，即可使用测试配置文件对其进行预览和测试。如果您已插入個人化內容，可使用測試設定檔資料檢查此內容在訊息中的顯示方式。

1. 按一下 **[!UICONTROL 模擬內容]**.

1. 按一下 **[!UICONTROL 管理測試設定檔]** 以新增測試設定檔。

1. 使用尋找您的測試設定檔 **[!UICONTROL 身分名稱空間]** 和 **[!UICONTROL 身分值]** 欄位。 然後，按一下 **[!UICONTROL 新增設定檔]**.

   ![](assets/push_preview_1.png)

1. 選取測試設定檔後，您可以關閉 **[!UICONTROL 新增測試設定檔]** 視窗。

1. 從 **預覽和測試** 視窗，測試設定檔資料會新增至訊息內容。

   選取要預覽內容的裝置型別： **[!UICONTROL iOS]** 或 **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## 驗證推播通知 {#push-validate}


您必須在編輯器的上方區段中檢查警示。 其中一些是簡單的警告，但其他警告可能會阻止您傳送訊息。 可能會發生兩種型別的警報：警告和錯誤。

* **警告** 請參閱建議和最佳實務。

* **錯誤** 防止您測試或啟動歷程，只要它們未解決，例如：

   * **[!UICONTROL 訊息的推送版本為空白]**：當遺失推播通知本文或標題時，會顯示此錯誤。 瞭解如何在中定義推播通知內容 [本節](create-push.md).

   * **[!UICONTROL 表面不存在]**：如果您選取的表面在建立訊息後遭到刪除，則無法使用訊息。 如果發生此錯誤，請在訊息中選取另一個曲面 **[!UICONTROL 屬性]**. 進一步瞭解中的管道表面 [本節](../configuration/channel-surfaces.md).

   * **[!UICONTROL 推播iOS/Android承載已超過4KB的限制]**：推播通知大小不得超過4KB。 為遵守此限制，請嘗試減少使用影像或表情符號。 瞭解如何在中管理您的推播通知內容 [本節](../push/create-push.md).

   ![](assets/push_alert.png)


>[!NOTE]
>
> 為了提供更好的傳遞能力，您應該一律使用提供者支援格式的電話號碼。 例如，Twilio和Sinch僅支援E.164格式的電話號碼。

## 发送推送通知{#push-send}

當您的推送訊息就緒時，請完成設定 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md) 以傳送。

**相关主题**

* [設定推播頻道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report.md#push-global)
* [创建推送通知](create-push.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在行銷活動中新增訊息](../campaigns/create-campaign.md)

