---
title: 資料彙集
description: 進一步了解決策管理意見反應資料收集
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 278cb255-439c-4ce8-ab59-07df79774b98
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 3%

---

# 決策管理資料收集 {#data-collection}

## 瞭解資料彙集

您可以在Adobe Experience Platform中收集offer decisioning意見回饋，包括顯示哪些優惠方案以及使用者如何與其互動。 此資料可用於：
* 構成 [決定管理報告](../reports/get-started-events.md)；
* 使用 [頻率限定](../offer-library/add-constraints.md#capping) 規則；
* 建置 [AI模型](../ranking/create-ranking-strategies.md) ，可作為排名方法使用。

## 事件型別

收集資料的方式因您要擷取的事件型別而異。

### 決定事件

每次決策管理做出決策時，與該決策事件相關的資訊都是 **自動** 已傳送至所有管道的Adobe Experience Platform。 [了解详情](../reports/get-started-events.md)

### 曝光和點選事件

決定管理曝光次數和點按次數定義如下：

* 一個 **印象** 事件是向使用者顯示選件時。

* A **按一下** 事件是指使用者點按或互動選件時。

系統會根據「 」，擷取曝光次數和點按次數的反饋 [!DNL Journey Optimizer] 使用的管道。

**電子郵件** 編寫者 [!DNL Journey Optimizer] **自動** 追蹤曝光次數和點按次數。

不過， **大部分管道** 需要以「 」身分將曝光次數和點按次數資料傳送到Adobe Experience Platform **體驗事件**. 这包括：

* 使用的網頁 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans){target="_blank"} 以呈現選件

* 行動應用程式使用 [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"} to render offers - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer-decisioning/#ab-sj-tracking-servers){target="_blank"}
* 資訊站
* 透過協力廠商應用程式傳送的訊息
   <!--Mobile push notifications authored by [!DNL Journey Optimizer] - [Learn more](https://developer.adobe.com/client-sdks/documentation/adobe-journey-optimizer/api-reference/#handlenotificationresponse){target="_blank"}-->

>[!NOTE]
>
>使用決策API請求接收優惠的管道需要以體驗事件的形式傳送意見回饋。 換言之，如果選件需要有關如何轉譯的說明，您可以假設您應將意見反應作為體驗事件傳送。

### 自定义事件

與您優惠方案相連結的自訂事件回饋，可依據您自己的偏好設定傳送至Adobe Experience Platform。 例如，如果選件有多個按鈕，例如 *有興趣*， *不感興趣*&#x200B;等等，您可能會想要分別傳入這些事件，但這些事件也可以以體驗事件的形式傳入。

## 傳送意見回饋資料

若要傳送意見反應資料，您需要建立資料集以收集事件，並針對每個事件型別定義將傳送至Adobe Experience Platform的體驗事件。

* 瞭解如何建立要在其中收集體驗事件的資料集 [本節](create-dataset.md).

* 瞭解如何定義體驗事件，以便在以下位置傳送意見反應資料： [本節](schema-requirement.md).
