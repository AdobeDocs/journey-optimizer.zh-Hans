---
solution: Journey Optimizer
product: journey optimizer
title: 變更執行地址
description: 瞭解如何從設定檔服務決定要使用的電子郵件地址。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 主要，執行，電子郵件，目標，設定檔，最佳化工具
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 23%

---

# 變更執行地址 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="定义要使用的地址"
>abstract="当数据库中有多个电子邮件地址或电话号码（个人、职业等）时，您可以选择优先向哪个电子邮件地址或电话号码发送。"

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="定义要使用的地址"
>abstract="编辑字段，用于确定优先向其发送的配置文件的电子邮件地址或电话号码。"

當您定位設定檔時，資料庫中可能會提供數個電子郵件地址或電話號碼（專業電子郵件地址、個人電話號碼等）。

在這種情況下， [!DNL Journey Optimizer] 使用 **[!UICONTROL 執行欄位]** 以決定從設定檔服務優先使用哪個電子郵件地址或電話號碼。

若要檢查目前預設使用的欄位，請存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 一般]** > **[!UICONTROL 執行欄位]** 功能表。

![](assets/primary-address-execution-fields.png)

目前的值會用於沙箱層級的所有傳送。 您可以視需要更新這些欄位。

在大多數情況下，您會全域變更執行欄位，並定義用於所有電子郵件或簡訊訊息的值。 <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## 更新管理設定 {#admin-settings}

若要在沙箱層級全域變更執行欄位，請遵循以下步驟。

1. 存取  **[!UICONTROL 頻道]** > **[!UICONTROL 一般]** > **[!UICONTROL 執行欄位]** 功能表。

1. 按一下 **[!UICONTROL 編輯]** 以變更預設值。

   ![](assets/primary-address.png)

1. 按一下您選擇的目前欄位或編輯圖示以選擇新欄位。

   ![](assets/primary-address-edit.png)

1. 將顯示可用電子郵件型別XDM欄位的清單。 選取要使用的欄位。

   ![](assets/primary-address-select-field.png)

1. 按一下 **[!UICONTROL 儲存]** 以確認您的選擇。

執行欄位已更新，現在會作為主要地址使用。

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## 覆寫歷程引數中的值 {#journey-parameters}

僅針對特定使用案例，您可以全域覆寫執行欄位集，並在歷程層級（尤其是電子郵件頻道）定義不同的值。

新增 **[!UICONTROL 電子郵件]** 動作變成 [歷程](../email/create-email.md#create-email-journey-campaign)，主要電子郵件地址會顯示在歷程進階引數下。

在某些特定內容中，您可以使用覆寫此值 **[!UICONTROL 啟用引數覆寫]** 圖示右側 **[!UICONTROL 地址]** 欄位。

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>仅应针对特定用例使用电子邮件地址覆盖。大多数情况下，无需更改电子邮件地址，应使用&#x200B;**[!UICONTROL 执行字段]**&#x200B;中定义为主地址的值。

覆寫此值可能很實用，例如：

* 测试电子邮件。您可以新增自己的電子郵件地址：發佈歷程後，系統會傳送電子郵件給您。
* 傳送電子郵件給清單的訂閱者。 在[此用例](../building-journeys/message-to-subscribers-uc.md)中了解更多。
