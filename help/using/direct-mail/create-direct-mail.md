---
title: 建立直接郵件訊息
description: 瞭解如何在Journey Optimizer中建立直接郵件訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 直接郵件、訊息、行銷活動
hide: true
hidefromtoc: true
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
badge: label="Beta" type="Informative"
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---

# 建立直接郵件訊息 {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="直邮创建"
>abstract="在计划的营销活动中创建直邮，并设计直邮提供商向您的客户发送邮件所需的提取文件。"

>[!BEGINSHADEBOX]

本文档包括以下内容：

* **[创建直邮](create-direct-mail.md)**
* [配置直邮](direct-mail-configuration.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>直接郵件目前是以私人測試版的形式提供，且可能會不時更新，恕不另行通知。

直接郵件是離線頻道，可讓您個人化並產生直接郵件供應商傳送郵件給客戶所需的擷取檔案。

當您建立直接郵件時，Journey Optimizer會產生一個檔案，其中包含所有目標設定檔和所選資料（例如郵寄地址、設定檔屬性）。 然後，您的直接郵件提供者將能夠擷取該檔案，並負責實際傳送。

直接郵件訊息只能在已排程行銷活動的內容中建立。 它們不可用於API觸發的行銷活動或歷程。

>[!IMPORTANT]
>
>在傳送直接郵件訊息之前，請確定您已設定：
>
>1. A [檔案路由設定](../direct-mail/direct-mail-configuration.md#file-routing-configuration) 會指定應該上傳及儲存解壓縮檔案的伺服器，
>1. A [直接郵件訊息表面](../direct-mail/direct-mail-configuration.md#direct-mail-surface) 會參照檔案路由設定。


## 建立您的直接郵件訊息 {#create}

建立和傳送直接郵件訊息的步驟如下：

1. 建立新的排程行銷活動，選取 **[!UICONTROL 直接郵件]** 作為您的動作，並選擇要使用的管道表面。 [瞭解如何建立直接郵件介面](../direct-mail/direct-mail-configuration.md#direct-mail-surface)

   ![](assets/direct-mail-campaign.png)

1. 按一下 **[!UICONTROL 建立]** 然後定義行銷活動的基本資訊（名稱、說明）。 [瞭解如何設定行銷活動](../campaigns/create-campaign.md)

1. 按一下 **[!UICONTROL 編輯內容]** 按鈕來設定要傳送給直接郵件提供者的擷取檔案。

1. 在中定義擷取檔案的名稱 **[!UICONTROL 檔案名稱]** 欄位。

   有时您可能需要在提取文件的开头或结尾添加信息。若要這麼做，請使用 **[!UICONTROL 附註]** 欄位，然後指定是否要以頁首或頁尾的形式包含附註。

   <!--Click on the button to the right of the Output file field and enter the desired label. You can use personalization fields, content blocks and dynamic text (see Defining content). For example, you can complete the label with the delivery ID or the extraction date.-->

   ![](assets/direct-mail-properties.png)

1. 使用左側區域來定義要在擷取檔案中顯示為欄的資訊：

   1. 按一下 **[!UICONTROL 新增]** 按鈕以新增欄，然後從清單中選取它。

   1. 在 **[!UICONTROL 格式設定]** 部分，指定欄的標籤，然後定義要顯示的設定檔屬性，使用 [運算式編輯器](../personalization/personalization-build-expressions.md).

      ![](assets/direct-mail-content.png)

   1. 若要使用選取的欄排序解壓縮檔案，請切換 **[!UICONTROL 排序方式]** 選項開啟。 此 **[!UICONTROL 排序方式]** 圖示隨即會顯示在檔案結構中欄的標籤旁。

1. 重複這些步驟，視需要新增欄數，以建置解壓縮檔案。 請注意，您最多可以新增50欄。

   您可以隨時刪除欄，方法是選取該欄並按一下 **[!UICONTROL 移除]** 按鈕來自 **[!UICONTROL 格式設定]** 區段。

   ![](assets/direct-mail-complete.png)

1. 定義直接郵件內容後，請完成行銷活動的設定。

   當行銷活動開始時，擷取檔案會自動產生並匯出至中指定的伺服器。 [檔案路由設定](../direct-mail/direct-mail-configuration.md).
