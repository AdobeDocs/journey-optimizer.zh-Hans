---
solution: Journey Optimizer
product: journey optimizer
title: 发送时间优化
description: 瞭解如何在訊息中最佳化引數傳送時間
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 傳送時間，傳送，訊息，最佳化，歷程， AI，智慧
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 36%

---

# 发送时间优化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="关于发送时间优化"
>abstract="Adobe Journey Optimizer 的发送时间优化功能由 Adobe 的 AI 服务提供支持，可以预测发送电子邮件或推送消息的最佳时间，从而根据历史打开率和点击率最大限度地提高参与度。"

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

## 激活发送时间优化{#activate-send-time-optimization}

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
