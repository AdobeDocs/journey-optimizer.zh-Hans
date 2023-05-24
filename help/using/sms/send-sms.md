---
solution: Journey Optimizer
product: journey optimizer
title: 預覽和測試簡訊
description: 瞭解如何在Journey Optimizer中預覽和測試您的SMS訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 12%

---

# 預覽和測試簡訊 {#send-sms}

## 預覽簡訊 {#preview-sms}

定义消息内容后，即可使用测试配置文件对其进行预览和测试。如果您已插入個人化內容，可使用測試設定檔資料檢查此內容在訊息中的顯示方式。

1. 按一下 **[!UICONTROL 模擬內容]**.

1. 按一下 **[!UICONTROL 管理測試設定檔]** 以新增測試設定檔。

1. 使用尋找您的測試設定檔 **[!UICONTROL 身分名稱空間]** 和 **[!UICONTROL 身分值]** 欄位。 然後，按一下 **[!UICONTROL 新增設定檔]**.

   ![](assets/sms_preview_3.png)

1. 選取測試設定檔後，您可以關閉 **[!UICONTROL 新增測試設定檔]** 視窗。

1. 從 **預覽和測試** 視窗，測試設定檔資料會新增至訊息內容。

   ![](assets/sms_preview_2.png)


## 驗證您的SMS{#sms-validate}

您必須在編輯器的上方區段中檢查警示。 其中一些是簡單的警告，但其他警告可能會阻止您傳送訊息。 可能會發生兩種型別的警報：警告和錯誤。

* **警告** 請參閱建議和最佳實務。 例如，如果您的SMS訊息為空白，則會顯示警告訊息。

* **錯誤** 阻止您測試或啟用歷程，或發佈行銷活動（只要它們未解決）。 例如，當主旨行遺失時，錯誤訊息會警告您。

![](assets/sms-alert-button.png)

>[!NOTE]
>
> 若要改善您的傳遞能力，請以提供者支援的格式使用電話號碼。 例如，Twilio和Sinch僅支援E.164格式的電話號碼。

## 傳送簡訊{#sms-send}

當您的SMS訊息準備就緒時，完成您的 [歷程](../building-journeys/journey-gs.md) 或 [行銷活動](../campaigns/create-campaign.md) 以傳送。

**相关主题**

* [配置短信渠道](sms-configuration.md)
* [短信报告](../reports/journey-global-report.md#sms-global)
* [创建短信消息](create-sms.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
