---
solution: Journey Optimizer
product: journey optimizer
title: 短信选择禁用管理
description: 瞭解如何透過簡訊管理選擇退出
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 63237c02f632d289dba845acdcd0859f2d6de9c9
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 31%

---

# 短信选择禁用管理 {#sms-opt-out}

根据行业标准和法规，所有短信营销消息都必须包含一种让接收者能够轻松取消订阅的方式。[進一步瞭解隱私權與選擇退出管理](../privacy/opt-out.md)

>[!IMPORTANT]
>
>文字訊息通訊可能會受到各種法律規範要求的約束，具體取決於其性質、您傳送文字訊息的位置以及收件者的位置。 雖然Adobe Journey Optimizer會處理長程式碼和免付費號碼的訊息（如下所述），但請洽詢您的法律顧問，以確保您的文字訊息通訊符合所有適用的法律規範要求。

## 原生傳入關鍵字{#sms-native-keywords}

依預設，Adobe Journey Optimizer會針對免付費和長程式碼訊息處理下列標準英文回複訊息：STOP、UNSTOP、START、QUIT、CANCEL、END和UNSUBSCRIBE。 請注意，搭配Journey Optimizer使用時，只有Sinch支援原生關鍵字。

這些關鍵字通常會觸發來自第三方提供者的自動標準回覆。 您可以直接与提供商或通过其文档网站确认此信息。

無需任何步驟，即可確保SMS選擇退出功能在Adobe Journey Optimizer中運作，因為關鍵字回應STOP、UNSTOP、START、QUIT、CANCEL、END和UNSUBSCRIBE會自動識別。 在Adobe Journey Optimizer中即時更新設定檔選擇退出狀態。


## 封鎖清單{#sms-blocklists}

除了Adobe Journey Optimizer根據選擇退出狀態停止傳送（用於與Twilio或Sinch直接整合）之外，大部分的SMS閘道提供者也會維護封鎖清單，確保SMS訊息不會傳送給選擇退出的個人。 如果您使用Sinch或Twilio以外的提供者，並透過以下方式傳送SMS： [自訂頻道](../building-journeys/using-custom-actions.md)，您需要向提供者確認。


## 短代码 {#short-codes}

依預設，Adobe Journey Optimizer不會處理短程式碼的選擇加入或說明關鍵字。 為確保符合業界法規與選擇退出處理規則，您必須確認您的短程式碼符合所有准則。

不過，Journey Optimizer不支援根據不同寄件者ID傳入關鍵字的全域選擇退出。

## 字母数字发件人 ID {#alphanumeric}

字母数字发件人 ID 仅用于单向消息传递，且无法接收入站消息。因此，Adobe Journey Optimizer 的短信 STOP、START、HELP 关键字不适用于字母发件人 ID。您必须提供其他说明，例如写信给支持团队、拨打支持电话或发短信给其他电话号码或代码，以允许用户选择退出接收通过字母数字发件人 ID 发送的消息。

## 视频 {#video-sms}

要详细了解原生入站关键词支持（START、STOP 和 UNSTOP）如何用于短信，请参阅以下视频：

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
