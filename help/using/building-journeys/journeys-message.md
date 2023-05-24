---
solution: Journey Optimizer
product: journey optimizer
title: 在历程中添加消息
description: 瞭解如何在歷程中新增訊息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，訊息，推播，簡訊，電子郵件，應用程式內
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 22%

---

# 电子邮件、应用程序内消息、推送、短信{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] 內建訊息功能。 您只需在歷程中新增推播、簡訊、應用程式內或電子郵件訊息活動，並定義設定和內容即可。 接著會在歷程內容中執行並傳送。

您也可以設定傳送訊息給您的特定動作：

* 如果您使用協力廠商系統來傳送訊息，可以建立自訂動作。 在本節瞭解更多 [區段](../action/action.md).

* 如果您使用的是Campaign和Journey Optimizer，請參閱下列章節：

   * [[!DNL Journey Optimizer] 和Campaign Classic v7/Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] 和Campaign Standard](../action/acs-action.md)

若要在歷程中新增訊息，請遵循下列步驟：

1. 通过[事件](general-events.md)或[读取区段](read-segment.md)活动开始您的历程。

1. 從 **動作** 區段，拖放 **電子郵件**，和 **應用程式內**，和 **簡訊** 或 **推播** 活動放入畫布。

1. 設定您的活動。 在以下頁面中瞭解建立訊息內容的詳細步驟：

   <table style="table-layout:fixed">
   <tr style="border: 0;">
   <td>
   <a href="../email/create-email.md">
   <img alt="潜在客户" src="../assets/do-not-localize/email.jpg">
   </a>
   <div><a href="../email/create-email.md"><strong>创建电子邮件</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../in-app/create-in-app.md">
   <img alt="潜在客户" src="../assets/do-not-localize/in-app.jpg">
   </a>
   <div><a href="../in-app/create-in-app.md"><strong>建立應用程式內訊息</strong>
   </div>
   <p>
   </td>
   <td>
   <a href="../push/create-push.md">
   <img alt="不频繁" src="../assets/do-not-localize/push.jpg">
   </a>
   <div>
   <a href="../push/create-push.md"><strong>建立推播通知<strong></a>
   </div>
   <p>
   </td>
   <td>
   <a href="../sms/create-sms.md">
   <img alt="验证" src="../assets/do-not-localize/sms.jpg">
   </a>
   <div>
   <a href="../sms/create-sms.md"><strong>建立簡訊訊息</strong></a>
   </div>
   <p>
   </td>
   </tr>
   </table>

## 更新即時內容{#update-live-content}

您可以在即時歷程中更新訊息內容（電子郵件、應用程式內、推播、簡訊）。

若要這麼做，請開啟您的即時歷程、選取訊息活動並按一下 **編輯內容**.

![](assets/add-a-message2.png)

但是，您無法變更個人化中使用的屬性，無論是設定檔屬性或內容資料（來自事件或歷程屬性）。

如果您修改內容資料，將會顯示下列錯誤訊息：ERR_AUTHORING_JOURNEYVERSION_201

如果您修改了設定檔屬性，將會顯示下列錯誤訊息：ERR_AUTHORING_JOURNEYVERSION_202

請注意，針對應用程式內活動，可以在歷程上線時對內容進行任何變更，但無法修改應用程式內觸發器。

## 发送时间优化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="关于发送时间优化"
>abstract="Adobe Journey Optimizer 的发送时间优化功能由 Adobe 的 AI 服务提供支持，可以预测发送电子邮件或推送消息的最佳时间，从而根据历史打开率和点击率最大限度地提高参与度。"

### 關於傳送時間最佳化 {#about-send-time}

Adobe Journey Optimizer 的发送时间优化功能由 Adobe 的 AI 服务提供支持，可以预测发送电子邮件或推送消息的最佳时间，从而根据历史打开率和点击率最大限度地提高参与度。使用我們的機器學習模型，為每位使用者安排個人化的傳送時間，以提高您訊息的開啟及點閱率。

傳送時間最佳化模型會擷取您的Adobe Journey Optimizer資料，並檢視使用者層級的開啟（針對電子郵件和推播）和點按（針對電子郵件）率，以判斷客戶何時最有可能參與您的傳訊。 傳送時間最佳化需要至少一個月的訊息追蹤資料，才能提出明智的建議。 系統會使用下列分數，為每位使用者自動挑選最佳時間：

* 一週中每天最佳的一小時，以最大化參與度
* 一週中最佳的一天，可讓參與度最大化
* 一週中最佳一天中最佳的一小時，以最大化參與度

無論您談論的是評分或訓練，此模式會有所不同。 培訓最初每週進行，然後每季度進行。 評分最初為每週，然後每月進行。

* 訓練 — 開發用來建立評分的演演算法
* 評分 — 根據已訓練的模型，將評分套用至個別設定檔

此資訊會儲存在使用者的設定檔中，並在歷程執行時參考，以告知Adobe Journey Optimizer何時傳送您的訊息。

>[!CAUTION]
>
>此功能與高載模式不相容。

### 激活发送时间优化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="激活发送时间优化"
>abstract="通过选择相应的单选按钮，选择是针对电子邮件打开操作还是针对电子邮件点进操作进行优化。您还可以为“发送于下一个”选项输入一个值，选择限定系统使用的发送时间。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="激活发送时间优化"
>abstract="推送消息默认为打开选项，因为点击不适用于推送消息。 您还可以为“发送于下一个”选项输入一个值，选择限定系统使用的发送时间。"

透過選取「 」，對電子郵件或推送訊息啟用傳送時間最佳化 **傳送時間最佳化** 從活動引數切換。

![](../building-journeys/assets/jo-message5.png)

對於電子郵件訊息，選擇是否最佳化電子郵件開啟次數，或透過選取適當的選項按鈕來最佳化電子郵件點進次數。 推送消息默认为打开选项，因为点击不适用于推送消息。 

您也可以輸入「 」的值，選擇將系統使用的傳送時間括起來。 **傳送於下一個** 選項。 如果您選擇「六小時」作為值， [!DNL Journey Optimizer] 將會檢查每個使用者設定檔，並在歷程執行時間的6小時內挑選最佳傳送時間。

**如果最佳時間在視窗之外，會發生什麼情況？**

以下列設定為例：

* 點按時最佳化
* 動作預定在上午10點開始
* 視窗為3小時

設定檔在視窗外可以有最佳的開啟時間。 例如，John的最佳點按開啟時間是下午5點。

設定檔層級會有一週中每個小時的分數。 在此範例中，電子郵件一律會在視窗中傳送。 在執行階段，系統會檢查該視窗（從上午10點開始的3小時視窗）內的分數清單。 然後系統會比較10、11和中午的分數，並選取最高分數。 屆時會傳送電子郵件。
