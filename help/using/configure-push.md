---
title: 配置推送通知
description: 了解如何在Journey Optimizer中创建推送通知
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '934'
ht-degree: 13%

---

# 配置推送通知{#create-push-notification}

![](assets/do-not-localize/badge.png)

创建消息时，将在&#x200B;**[!UICONTROL Push Notification]**&#x200B;选项卡中配置推送通知（请参阅[创建消息](create-message.md)）。

您可以使用专用选项卡为iOS或Android操作系统配置推送通知内容。

![](assets/create-content-push.png)

## 标题与正文

要撰写消息，请单击&#x200B;**[!UICONTROL Title]**&#x200B;和&#x200B;**[!UICONTROL Body]**&#x200B;字段。 使用表达式编辑器定义内容和个性化数据。

了解有关[本节](personalization/personalize.md)中个性化的更多信息

使用中心部分可显示推送通知在iOS和Android终端中的显示方式。

>[!NOTE]
>
>**[!UICONTROL Compose Message]**&#x200B;部分对&#x200B;**[!UICONTROL iOS]**&#x200B;和&#x200B;**[!UICONTROL Android]**&#x200B;选项卡都是通用的。 本条的任何更改将适用于两个操作系统。

## 单击行为{#on-click-behavior}

选择收件人单击推送通知正文时的行为：

* 使用&#x200B;**[!UICONTROL Open app]**&#x200B;选项打开与消息&#x200B;**[!UICONTROL Preset]**&#x200B;关联的应用程序。
* 使用&#x200B;**[!UICONTROL Deeplink]**&#x200B;选项将收件人重定向到应用程序内的特定内容。 在关联字段中输入深层链接。
* 使用&#x200B;**[!UICONTROL Web URL]**&#x200B;选项将收件人重定向到外部URL。 在关联字段中输入URL。

## 发送无提示通知

静默推送通知（或后台通知）是传递到应用程序的隐藏指令。 例如，它用于向应用程序通知新内容的可用性或在后台启动下载。

选择&#x200B;**[!UICONTROL Silent Notification]**&#x200B;选项以静默通知应用程序：在这种情况下，通知会直接转让给应用程序。 设备屏幕上不显示警报。

使用&#x200B;**[!UICONTROL Custom data]**&#x200B;部分添加键/值对。

## 高级选项

配置&#x200B;**[!UICONTROL Advanced options]**。 可用参数有：

| 参数 | 可用性 | 描述 |
|---------|----------|---------|
| **[!UICONTROL Collapsible]** | iOS/Android | 可折叠的消息是可替换为新消息的消息。 例如，一个应用程序，它使用有关主题的最新新闻更新用户。 在这种情况下，只有最新的信息是相关的。 另一方面，对于不可折叠的消息，每条消息对客户端应用程序都很重要，需要传递。 |
| **[!UICONTROL Custom sound]** | iOS/Android | 当收到通知时，移动终端要播放的声音。 音效需要打包在应用程序中。 |
| **[!UICONTROL Badges]** | iOS/Android | 标记用于直接在应用程序图标上显示新的未读信息数。<br/>当用户打开或从应用程序中读取新内容时，标记值将消失。在设备上收到通知时，可能会刷新或增加相关应用程序的标记值。<br/>例如，如果您存储的是客户的未读文章数，则可以利用个性化来为每个客户发送唯一的未读文章徽章值。有关更多个性化信息，请参阅[本节](personalization/personalize.md)。 |
| **[!UICONTROL Notification group]** / | iOS | 将通知组与推送通知关联。<br/>从iOS 12开始，通知组允许您将消息线程和通知主题合并到线程ID中。例如，品牌可能会在一个组ID下发送营销通知，而在一个或多个不同ID下保留更多运营类型通知。<br/>为了说明这一点，您可以有groupID:123 “查看新的毛衣系列”和groupID:456 “您的包裹已送达”通知组。在此示例中，所有投放通知都将捆绑在组ID下：456。 |
| **[!UICONTROL Notification channel]** | Android | 将通知渠道关联到推送通知。<br/>从Android 8.0（API级别26）开始，必须将所有通知分配给渠道才能显示。有关详细信息，请参阅[Android开发人员文档](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels)。 |
| **[!UICONTROL Add content-availability flag]** | iOS | 发送推送有效负荷中的可用内容标志，以确保应用程序在收到推送通知后立即唤醒，这意味着应用程序将能够访问有效负荷数据。<br/> 即使应用程序在后台运行并且无需任何用户交互（例如点击推送通知），也能正常使用。 但是，如果应用程序未运行，则不适用。有关更多信息，请参阅 [Apple 开发人员文档](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)。 |
| **[!UICONTROL Add mutable-content flag]** | iOS | 发送推送有效负荷中的可变内容标志，并允许通过iOS SDK中提供的通知服务应用程序扩展修改推送通知内容。 有关更多信息，请参阅 [Apple 开发人员文档](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)。<br/>然后，您可以利用移动应用程序扩展进一步修改从发送的到达推送通知的内容或 [!DNL Journey Optimizer] 演示。例如，用户可以利用此选项解密数据、更改通知的正文或标题文本、向通知添加线程标识符等。 |
| **[!UICONTROL Notification visibility]** | Android | 定义推送通知的可见性。 <b>私有</b> 化将在所有锁屏上显示通知，但在安全的锁屏上隐藏敏感或私有信息。<b>Publicwill</b> 将在所有屏幕上显示通知的全部内容。<b>Secretwill不</b> 会在安全的锁屏上显示通知的任何部分。有关详细信息，请参阅[Android开发人员文档](https://developer.android.com/reference/android/app/Notification)。 |
| **[!UICONTROL Notification priority]** | Android | 定义从“低”到“最大”的推送通知重要性。 这决定了推送通知在发送时的“侵入”程度。 有关详细信息，请参阅[Android开发人员文档](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** | Android | 设置推送通知的高优先级或正常优先级。 有关消息优先级的更多信息，请参阅 [Google 开发人员文档](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)。 |

## 自定义数据

在&#x200B;**[!UICONTROL Custom data]**&#x200B;部分中，可以根据移动应用程序配置向负载添加自定义变量。 有关如何在Adobe Experience Platform和Adobe Launch中设置推送通知的详细信息，请参阅[本节](push-configuration.md)

