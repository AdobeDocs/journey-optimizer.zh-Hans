---
solution: Journey Optimizer
product: journey optimizer
title: 与 Adobe Campaign v7/v8 集成
description: 瞭解如何將Journey Optimizer與Adobe Campaign v7/v8整合
feature: Actions
topic: Administration
role: Admin,Developer
level: Intermediate
keywords: campaign， acc，整合
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 22%

---

# 与 Adobe Campaign v7/v8 集成 {#integrating-with-adobe-campaign-classic}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Adobe Campaign v7/v8 操作"
>abstract="此集成可用于 Adobe Campaign Classic v7 和 v8。它让您可以使用 Adobe Campaign 事务性消息传递功能发送电子邮件、推送通知和 SMS。Journey Optimizer 实例和 Campaign 实例之间的连接在配置时由 Adobe 设置。"

此整合適用於Adobe Campaign Classic v7 （從7.1版開始）和Adobe Campaign v8。 它让您可以使用 Adobe Campaign 事务性消息传递功能发送电子邮件、推送通知和 SMS。

Journey Optimizer 实例和 Campaign 实例之间的连接在配置时由 Adobe 设置。

本頁面介紹端對端使用案例 [區段](../building-journeys/ajo-ac.md).

對於每個已設定的動作，歷程設計工具浮動視窗中都有動作活動可用。 请参阅此[章节](../building-journeys/using-adobe-campaign-classic.md)。

## 重要说明 {#important-notes}

* 無訊息限制。 系統會根據目前的Campaign SLA，將每5分鐘可傳送的訊息數量上限設為4000封。 因此，Journey Optimizer應僅用於單一使用案例（個別事件，而非區段）。

* 您必須在要使用的每個範本的畫布上設定一個動作。 您需要在Journey Optimizer中，為您要從Adobe Campaign使用的每個範本設定一個動作。

* 建議您使用針對這項整合而代管的專用訊息中心執行個體，以避免影響您可能進行的任何其他Campaign作業。 行銷伺服器可以是託管式或內部部署。 所需的版本編號為21.1版本候選版本或更新版本。

* 沒有驗證裝載或Campaign訊息是否正確。

* 促銷活動動作不可與區段資格事件搭配使用。

## 先决条件 {#prerequisites}

在Campaign中，您需要建立並發佈交易式訊息及其相關事件。 請參閱 [Adobe Campaign檔案](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target="_blank"}.

您可以依照以下模式，建置與每則訊息相對應的JSON裝載。 之後，當您在Journey Optimizer中設定動作時，就會貼上此裝載（請參閱下文）

示例如下：

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **頻道**：為您的Campaign交易範本定義的管道
* **事件型別**：Campaign事件的內部名稱
* **ctx**：變數，根據您訊息中的個人化設定而定。

## 設定動作 {#configure-action}

在Journey Optimizer中，您需要為每個交易式訊息設定一個動作。 执行以下步骤：

1. 建立新動作。 请参阅此[章节](../action/action.md)。
1. 輸入名稱和說明。
1. 在 **動作型別** 欄位，選取 **Adobe Campaign Classic**.
1. 按一下 **裝載** 欄位並貼上與Campaign訊息相對應的JSON裝載範例。 聯絡Adobe以取得此裝載。
1. 視您想要在歷程畫布上對應欄位，將不同的欄位調整為靜態或變數。 某些欄位，例如電子郵件地址和個人化欄位(ctx)的管道引數，您可能想要定義為要在歷程內容中對應的變數。
1. 单击&#x200B;**保存**。

![](assets/accintegration1.png)
