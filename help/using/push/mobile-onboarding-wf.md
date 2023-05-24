---
solution: Journey Optimizer
product: journey optimizer
title: 移动端加入快速入门工作流程
description: 瞭解如何使用行動入門快速入門工作流程
topic: Mobile
feature: Push
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: 82477d40-cfea-456b-a7b1-9cfebd76db35
source-git-commit: 62954221f9797fc4ac7b5e066ffea6f99c17ad45
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 10%

---

# 移动端加入快速入门工作流程 {#mobile-wf}

新 **行動入門快速入門工作流程** 是一項新產品功能，可快速設定Adobe Experience Platform Mobile SDK、開始收集和驗證行動事件資料，並透過傳送推播通知 [!DNL Journey Optimizer].

此功能可透過 **[!DNL Adobe Experience Platform Data Collection]** 首頁提供給所有客戶，作為公開測試版。

## 快速入门{#gs-mobile-wf}

此新工作流程透過減少總點按次數並加快Journey Optimizer的行動設定，使資料收集設定自動化。 此快速入門工作流程會帶您完成四個簡單步驟，以 [設定](##setup-mobile-wf)， [實作](#implement-mobile-wf)， [驗證](#valid-mobile-wf)、和 [檢閱](#review-mobile-wf) 您的行動設定。

若要存取新的行動入門快速入門工作流程，請瀏覽 **[!DNL Data Collection]** 解決方案切換器中的。 然後選取 **[!DNL Start Collecting Mobile Data]** 卡片。

![](assets/mobile-wf-home.png)

以下是一些額外功能：

* 簡單的四步驟工作流程和使用者介面。
* 提供基本設定，以開始透過收集行動事件資料 [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} 幾分鐘內。
* 運用測試及驗證基本行動推送事件的功能 [Adobe Experience Platform保證](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}.
* 自動建立及設定所有必要的資料收集和Journey Optimizer資產。
* 在產品指引和工具提示中。
* 視需要提供更進階實作的自然轉換。

## 設定 {#setup-mobile-wf}

此工作流程的第一步會自動建立及設定所有必要的資料收集和Journey Optimizer資產，例如行動屬性、行動擴充功能、Journey Optimizer擴充功能、規則、資料元素等。

接受測試版條款與條件後，請輸入行動應用程式的名稱，然後按一下 **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

提供iOS和Android平台的資訊，包括您的應用程式ID和驗證金鑰或金鑰檔案。

## 实施{#implement-mobile-wf}

下一個步驟提供將程式碼安裝到行動應用程式的逐步指南。

![](assets/mobile-wf-add-code.png)


## 验证{#valid-mobile-wf}

檢閱並檢查實作以驗證實作。 您可以傳送測試推播通知。

![](assets/mobile-wf-valid.png)


## 请查看 {#review-mobile-wf}

自動化設定已完成。 您現在可以造訪標籤行動屬性、設定規則或資料元素，並開始使用Adobe Journey Optimizer傳送推播通知。

![](assets/mobile-wf-done.png)


**相关主题**

* [推送通知入门](get-started-push.md)
* [推播通知資料流程和元件](push-gs.md)
* [設定推播通道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report.md#push-global)
* [创建推送通知](create-push.md)
