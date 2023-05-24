---
title: 應用程式內設定
description: 瞭解如何設定環境，以使用Journey Optimizer傳送應用程式內訊息
role: Admin
level: Intermediate
keywords: 應用程式內、訊息、設定、平台
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: e35aeba17f45145cc7712740cbcf1f0e169760fc
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 11%

---

# 配置应用程序内渠道 {#inapp-configuration}

在傳送應用程式內訊息之前，您必須在以下位置設定應用程式內頻道： [!DNL Adobe Experience Platform Data Collection].

1. 從您的 [!DNL Adobe Experience Platform Data Collection] 帳戶，存取 **[!UICONTROL 資料流]** 功能表並按一下 **[!UICONTROL 新增資料串流]**. 如需資料流建立的詳細資訊，請參閱 [此頁面](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. 選取 [!DNL Adobe Experience Platform] 服務。

   [!DNL Edge Segmentation] 和 [!DNL Adobe Journey Optimizer] 必須選取。

   ![](assets/inapp_config_6.png)

1. 然後，存取 **[!UICONTROL 應用程式表面]** 功能表，然後按一下 **[!UICONTROL 建立應用程式表面]**.

   ![](assets/inapp_config_1.png)

1. 將名稱新增至您的 **[!UICONTROL 應用程式表面]**.

1. 從Apple iOS下拉式清單，輸入 **iOS套件組合ID**. 請參閱 [Apple檔案](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) 有關下列專案的詳細資訊： **套件組合ID**.

   ![](assets/inapp_config_2.png)

1. 從Android下拉式清單，輸入 **Android套件名稱**. 請參閱 [Android檔案](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) 有關下列專案的詳細資訊： **封裝名稱**.

1. 按一下 **[!UICONTROL 儲存]** 當您完成設定 **[!UICONTROL 應用程式表面]**.

   ![](assets/inapp_config_3.png)

   您的 **[!UICONTROL 應用程式表面]** 現在使用應用程式內訊息建立新行銷活動時，即可使用。 [了解详情](create-in-app.md)

1. 建立應用程式表面後，您現在需要建立行動屬性。

   請參閱 [此頁面](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) 以取得詳細程式。

   ![](assets/inapp_config_4.png)

1. 從新建立屬性的「擴充功能」功能表中，安裝下列擴充功能：

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP保證
   * 同意
   * 識別
   * 行動核心
   * 配置文件

   請參閱 [此頁面](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en#add-a-new-extension) 以取得詳細程式。

   ![](assets/inapp_config_5.png)

應用程式內頻道現已設定。 您可以開始傳送應用程式內訊息給使用者。

**相关主题：**

* [创建应用程序内消息](create-in-app.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [設計應用程式內訊息](design-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
