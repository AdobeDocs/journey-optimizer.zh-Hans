---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer中的推播通知流程
description: 瞭解推播通知資料流程和元件
topic: Mobile
feature: Push
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 014cc551cb125ba6dc20a4f572e6cd7024d9fab5
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 8%

---

# 推播通知資料流程和元件 {#get-started-push}

此頁面可協助您設定並瞭解中與推播通知有關的主要服務和工作流程。 [!DNL Journey Optimizer].


>[!AVAILABILITY]
>
>新 **行動入門快速入門工作流程** 現已推出。 使用此新產品功能快速設定Mobile SDK，以開始收集和驗證行動事件資料，並傳送行動推播通知。 作为公开测试版，此功能可通过数据收集主页访问。[了解详情](mobile-onboarding-wf.md)

瞭解如何在上建立推播通知 [此頁面](create-push.md).

在中設定推送管道的步驟 [!DNL Adobe Journey Optimizer] 詳細資訊： [此頁面](push-configuration.md).

下圖顯示與相關資料流程相關的系統和服務，重點說明如何從端對端服務的角度傳送推播通知。

![](assets/push-flow.png)

1. 使用Apple的APN和Google FCM推送訊息服務註冊品牌行動應用程式(Android或iOS)
1. 傳訊服務會產生推播權杖，其為識別碼，可 [!DNL Adobe Journey Optimizer] 會使用來透過推播通知鎖定特定裝置。
1. 先前產生的推播權杖會傳遞至Adobe Experience Platform並與即時客戶設定檔同步；這是透過易於整合的使用者端SDK在OOTB中完成
1. 推送訊息的編寫位置 [!DNL Adobe Journey Optimizer]，推送訊息會針對頻道介面建立（即訊息預設集）
1. 推播訊息可包含在歷程中的協調畫布上
1. 在歷程發佈後，根據歷程條件的客戶設定檔符合接收推送通知的資格，在此步驟中會個人化推送訊息裝載
1. 個人化推送裝載會轉送至內部推送訊息傳遞服務
1. 然後，此內部服務會驗證與訊息相關聯之應用程式的認證，並且
1. 傳送訊息至Apple與Google訊息服務，以進行最終傳送
1. 會記錄來自訊息服務的回饋，並記錄錯誤和成功，以便在Journey Live和全域報告中報告
1. 推播通知會傳送至一般使用者裝置
1. 一般使用者推播通知互動會透過SDK整合，從一般使用者使用者端以體驗事件的形式傳送

## 推送通知中重要服務的角色 {#roles-of-key-services}

* **推播通知服務提供者** 是從遠端伺服器傳送通知至行動應用程式的核心元件Web服務。

   [!DNL Adobe Journey Optimizer]  同時支援Android和iOS平台，因此將與下列專案整合：
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging)  — 傳送通知至Android行動應用程式
   * [Apple推播通知服務(APN)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html)  — 傳送通知至iOS行動應用程式

* **Adobe Experience Platform Mobile SDK** 透過與Android和iOS相容的SDK，為您的行動裝置提供使用者端整合API。 SDK提供 [!DNL Adobe Journey Optimizer] 擴充功能可公開多種推送訊息專用API，並啟用資料流程，例如註冊推送代號、傳送推送追蹤事件或任何其他自訂體驗事件至Adobe Experience Platform。 SDK還提供多種其他擴充功能，可啟用其他Adobe Experience Cloud以及第三方合作夥伴功能。

   SDK整合也需要設定Adobe Experience Platform [資料彙集](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html){target="_blank"} 服務例如：

   * 建立資料串流，以設定資料流入Adobe Experience Platform所依據的設定檔和體驗事件資料集
   * 建立使用者端行動屬性並新增擴充功能。 SDK與這些擴充功能緊密整合，以提供順暢的資料收集體驗。
   * 註冊行動應用程式套件組合識別碼和應用程式認證

* **Adobe Experience Platform即時客戶個人檔案**  透過合併來自多個管道（包括網路、行動裝置、CRM和協力廠商）的資料，維護每個個別客戶的整體檢視。 档案允许您将您的客户数据整合到一个统一视图中，并提供每个客户交互的带时间戳的可操作帐户。特定應用程式使用者的推播權杖會根據使用者的設定檔儲存為記錄資料，而使用者與推播通知的互動則會作為時間序列事件資料受到追蹤。 [進一步瞭解Adobe Experience Platform即時客戶個人檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}.

* **[!DNL Adobe Journey Optimizer]** ：一旦您的行動應用程式與上述元件整合就緒，且您的客戶設定檔位於Adobe Experience Platform中，您即可在中製作及協調推播通知 [!DNL Adobe Journey Optimizer] 與您的使用者互動。

## 推播技術設定和從業人員工作流程 {#push-technical-setup}

下圖顯示設定構成推送資料流程骨架之元件的各種端對端步驟。 已根據執行設定的角色和正在設定的元件，將行動專案分類。

![](assets/user-flow.png)

**相关主题**

* [設定推播頻道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report.md#push-global)
* [创建推送通知](create-push.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在行銷活動中新增訊息](../campaigns/create-campaign.md)