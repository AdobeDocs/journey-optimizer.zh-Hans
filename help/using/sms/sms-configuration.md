---
solution: Journey Optimizer
product: journey optimizer
title: 設定簡訊頻道
description: 瞭解如何設定您的環境，以使用Journey Optimizer傳送SMS
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 33dccf32b60a6afb58931823016821fc1effcbd8
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 19%

---

# 配置短信渠道 {#sms-configuration}

[!DNL Journey Optimizer] 可讓您建立歷程並傳送訊息給目標對象。

傳送SMS前，請設定您的執行個體。 您需要 [整合提供者設定](#create-api) 使用Journey Optimizer和 [建立簡訊表面](#message-preset-sms) （即簡訊預設集）。 这些步骤必须由 [Adobe Journey Optimizer 系统管理员](../start/path/administrator.md)执行。

## 先决条件{#sms-prerequisites}

Adobe Journey Optimizer目前與Sinch和Twilio等協力廠商提供者整合，這些協力廠商提供獨立於Adobe Journey Optimizer的SMS服務。

在SMS設定之前，您必須使用這些SMS提供者之一建立帳戶，以接收API權杖和服務ID，這可讓您在Adobe Journey Optimizer和適用的SMS提供者之間建立連線。

您對簡訊服務的使用將受限於適用簡訊提供者的其他條款與條件。 鑑於Sinch和Twilio是透過整合可供Adobe Journey Optimizer使用者使用的協力廠商產品，如有任何與SMS服務相關的問題或詢問，Sinch或Twilio的使用者需要聯絡適用的SMS提供者以尋求協助。 Adobe無法控制第三方產品，因此不負責第三方產品。

>[!CAUTION]
>
>若要存取和編輯SMS子網域，您必須擁有 **[!UICONTROL 管理SMS子網域]** 生產沙箱的許可權。

## 建立新的API認證 {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="使用 Journey Optimizer 配置 SMS 供应商"
>abstract="选择您的供应商并填写 SMS API 凭据。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="使用 Journey Optimizer 配置 SMS 供应商"
>abstract="在发送 SMS 之前，您必须将供应商设置与 Journey Optimizer 集成。完成后，您将需要创建一个 SMS 表面。这些步骤必须由 Adobe Journey Optimizer 系统管理员执行。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html?lang=zh-Hans#message-preset-sms" text="创建 SMS 渠道表面"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="选择 SMS 供应商配置"
>abstract="选择为您的 SMS 供应商配置的 API 凭据。"

若要使用Journey Optimizer設定簡訊供應商，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL API認證]** 功能表。 按一下 **[!UICONTROL 建立新的API認證]** 按鈕。

   ![](assets/sms_6.png)

1. 選取您的 **[!UICONTROL 簡訊供應商]**：

   * **[!DNL Sinch]**

      尋找您的 **[!UICONTROL 服務ID]** 和 **[!UICONTROL API權杖]**，從您的Sinch帳戶存取SMS > API功能表。

   * **[!DNL Twilio]**

      尋找您的 **[!UICONTROL 服務ID]** 和 **[!UICONTROL API權杖]**，存取主控台控制面板頁面的「帳戶資訊」窗格。


1. 輸入 **[!UICONTROL 名稱]** 以取得您的API認證。

1. 輸入您的 **[!UICONTROL 服務ID]** 和 **[!UICONTROL API權杖]**.

   ![](assets/sms_7.png)

1. 按一下 **[!UICONTROL 提交]** 完成API認證的設定時。

建立和設定API認證後，您現在需要為SMS訊息建立管道表面（即訊息預設集）。

## 建立簡訊表面 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定义 SMS 类别"
>abstract="选择使用此表面的 SMS 消息类型：营销性的推广 SMS 消息，此时需要用户同意；或者事务性的非商业 SMS 消息，例如密码重置。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="选择退出营销 SMS 消息"

設定簡訊頻道後，您必須建立頻道介面，才能從傳送SMS訊息 **[!DNL Journey Optimizer]**.

若要建立管道曲面，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL 品牌化]** > **[!UICONTROL 管道表面]**. 按一下 **[!UICONTROL 建立管道表面]** 按鈕。

   ![](assets/preset-create.png)

1. 輸入表面的名稱和說明（選擇性），然後選取SMS通道。

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 和連字型大小 `-` 個字元。

1. 定義 **簡訊設定**.

   ![](assets/preset-sms.png)

   * 選取 **[!UICONTROL 簡訊型別]** 將與介面一併傳送的電子郵件： **[!UICONTROL 異動]** 或 **[!UICONTROL 行銷]**.

      * 選擇 **行銷** 促銷簡訊：這些訊息需要使用者同意。
      * 選擇 **異動** 非商業訊息，例如訂單確認、密碼重設通知或傳遞資訊。

      >[!CAUTION]
      >
      >**異動** SMS訊息可傳送給從行銷通訊取消訂閱的設定檔。 這些訊息只能在特定內容中傳送。

      建立SMS訊息時，您必須選擇符合您為訊息選取的類別的有效頻道介面。

   * 選取 **[!UICONTROL 簡訊設定]** 以與曲面相關聯。

      有關如何設定環境以傳送SMS訊息的詳細資訊，請參閱 [本節](#create-api).

   * 輸入 **[!UICONTROL 寄件者號碼]** 您&#x200B;想要用於通訊。

   * 選取您的 **[!UICONTROL 簡訊執行欄位]** 以選取 **[!UICONTROL 設定檔屬性]** 與設定檔的電話號碼相關聯。


1. 如果您想要在SMS訊息中使用URL縮短功能，請從 **[!UICONTROL 子網域]** 清單。

   >[!NOTE]
   >
   >若要能夠選取子網域，請確定您先前已設定至少一個SMS子網域。 [了解如何操作](sms-subdomains.md)

1. 設定好所有引數後，按一下 **[!UICONTROL 提交]** 以確認。 您也可以將管路曲面儲存為拔模，並在稍後恢復其組態。

   ![](assets/sms_preset_2.png)

1. 建立管道曲面後，它會顯示於清單中，並具有 **[!UICONTROL 處理中]** 狀態。

   >[!NOTE]
   >
   >如果檢查未成功，請在中進一步瞭解可能的失敗原因 [本節](#monitor-channel-surfaces).

1. 檢查成功後，管道表面會取得 **[!UICONTROL 作用中]** 狀態。 已準備好用於傳遞訊息。

   ![](assets/preset-active.png)

您現在可以使用Journey Optimizer傳送SMS訊息。

**相关主题**

* [创建短信消息](create-sms.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在行銷活動中新增訊息](../campaigns/create-campaign.md)

