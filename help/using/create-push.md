---
title: 配置推送通知
description: 了解如何在Journey Optimizer中创建推送通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 5866a5ad181b9b745cedc4fa740d131cf7c88863
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 10%

---

# 创建推送通知 {#create-push-notification}

一旦 [已创建消息](create-message.md)，请单击 **[!UICONTROL Push Notification]** 选项卡，以定义推送通知的设置和内容。

![](assets/create-content-push.png)

使用专用选项卡定义的推送通知设置 **iOS** 和 **Android** 操作系统。

>[!NOTE]
>
>的 **[!UICONTROL Compose Message]** 部分对这两个 **[!UICONTROL iOS]** 和 **[!UICONTROL Android]** 选项卡。 此部分中的任何更改都将应用于这两个选项卡。

## 标题与正文

要撰写消息，请单击 **[!UICONTROL Title]** 和 **[!UICONTROL Body]** 字段。 使用表达式编辑器定义内容和个性化数据。 在的表达式编辑器中了解有关个性化的更多信息 [此部分](personalization/personalize.md)

使用设备预览部分可视化推送通知在iOS和Android设备上的显示方式。

## 点击行为 {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="关于点击行为"
>abstract="选择收件人单击推送通知正文时的行为。"

选择收件人单击推送通知正文时的行为。

![](assets/title-body-push.png)

* 使用 **[!UICONTROL Open app]** 用于打开与消息关联的应用程序的选项 **[!UICONTROL Preset]**.
* 使用 **[!UICONTROL Deeplink]** 用于将收件人重定向到应用程序内的特定内容的选项。 在关联的字段中输入深层链接。
* 使用 **[!UICONTROL Web URL]** 将收件人重定向到外部URL的选项。 在关联的字段中输入URL。

## 添加媒体

在iOS版本的推送通知中，您可以添加将在通知中显示的图像、视频或GIF。

在Android版本中，您只能添加图像图标和用于扩展通知的图像。

![](assets/push-config-add-media.png)

有两个选项可用。 您可以：

* 单击 **[!UICONTROL Add media]** 按钮以在 **[!DNL Adobe Experience Manager Assets Essentials]**.

   了解如何使用 **[!DNL Adobe Experience Manager Assets Essentials]** in [本页](assets-essentials.md).

* 或者，通过单击 **[!UICONTROL Add media]** 字段。 在这种情况下，您可以添加个性化。

添加后，媒体会显示在通知正文的右侧。

## 添加按钮

您可以通过向推送内容添加按钮来创建可操作的通知。

如果设备屏幕已锁定，则不会显示以下按钮：只有 **标题** 和 **消息** 显示。 如果其设备已解锁，则收件人将看到这些按钮。

在iOS版本中，最多可添加4个按钮。 在Android版本中，最多可添加3个按钮。

>[!NOTE]
>
>对于iOS，请使用 **[!UICONTROL iOS category]** 字段将操作与通知类别关联。

单击 **[!UICONTROL Add button]** 要定义设置，请执行以下操作：标签和关联的操作。 可能的操作与 [点击行为](#on-click-behavior).

单击 **[!UICONTROL Expand view]** 以预览个性化按钮。

![](assets/push_buttons.png)

## 发送无提示通知

无提示推送通知（或后台通知）是交付给应用程序的隐藏指令。 例如，它用于通知您的应用程序新内容的可用性或在后台启动下载。

选择 **[!UICONTROL Silent Notification]** 用于静默通知应用程序的选项：在这种情况下，通知会直接转给应用程序。 设备屏幕上未显示任何警报。

使用 **[!UICONTROL Custom data]** 部分添加键值对。

## 自定义数据

在 **[!UICONTROL Custom data]** 部分，则可以根据移动应用程序配置将自定义变量添加到有效负载。 有关如何在Adobe Experience Platform中设置推送通知和AdobeLaunch的更多信息，请参阅 [此部分](push-gs.md)

## 高级选项

您可以配置 **[!UICONTROL Advanced options]** ，以获取推送通知。 以下列出了可用参数：

| 参数 | 描述 |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS/Android) | 可折叠的消息是一种消息，如果消息已过时，则可以用新消息替换该消息。 可折叠消息的常见用例是消息，用于告知移动设备应用程序从服务器同步数据。 例如，一个可更新用户最新得分的体育应用程序。 只有最新的消息才相关。 另一方面，通过不可折叠的消息，非常的消息对客户端应用程序很重要，需要发送。 |
| **[!UICONTROL Custom sound]** (iOS/Android) | 移动终端在收到通知时要播放的声音。 需要在应用程序中捆绑声音。 |
| **[!UICONTROL Badges]** (iOS/Android) | 标记用于直接在应用程序图标上显示新的未读信息数。<br/>当用户打开或从应用程序中读取新内容时，标记值将消失。在设备上收到通知时，可能会刷新或增加相关应用程序的标记值。<br/>例如，如果您存储的是客户的未读文章数，则可以利用个性化功能为每个客户发送唯一的未读文章标记值。 如需更多个性化信息，请参阅 [此部分](personalization/personalize.md). |
| **[!UICONTROL Notification group]**  (仅限iOS) | 将通知组与推送通知关联。<br/>从iOS 12开始，通知组允许您将消息线程和通知主题合并到线程ID中。 例如，品牌可能会在一个组ID下发送营销通知，而在一个或多个不同ID下保留更多操作类型通知。<br/>为了说明这一点，您可以具有groupID:123 “查看新的Sweaters春季系列”和groupID:456 “您的包已送达”通知组。 在本例中，所有投放通知都将捆绑在组ID下：456。 |
| **[!UICONTROL Notification channel]** （仅限Android） | 将通知渠道关联到推送通知。<br/>从Android 8.0（API级别26）开始，必须将所有通知分配给渠道才能显示。 有关更多信息，请参阅 [Android开发人员文档](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** (仅限iOS) | 发送推送负载中的可用内容标志，以确保应用程序在收到推送通知后立即唤醒，这意味着应用程序将能够访问有效载荷数据。<br/> 即使应用程序在后台运行且无需任何用户交互（例如点按推送通知），这项操作仍可正常运行。 但是，如果应用程序未运行，则不适用此设置。 有关更多信息，请参阅 [Apple 开发人员文档](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html)。 |
| **[!UICONTROL Add mutable-content flag]** (仅限iOS) | 发送推送负载中的可变内容标记，并将允许推送通知内容由iOS SDK中提供的通知服务应用程序扩展进行修改。 有关更多信息，请参阅 [Apple 开发人员文档](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html)。<br/>然后，您可以利用移动应用程序扩展进一步修改从发送的推送通知的内容或演示 [!DNL Journey Optimizer]. 例如，用户可以利用此选项解密数据、更改通知的正文或标题文本、向通知添加线程标识符等。 |
| **[!UICONTROL Notification visibility]** （仅限Android） | 定义推送通知的可见性。 <br/><b>私有</b> 将在所有锁屏上显示通知，但在安全的锁屏上隐藏敏感或隐私信息。 <br/><b>公共</b> 将在所有锁屏上全部显示通知。 <br/><b>密码</b> 不会在安全的锁屏上显示通知的任何部分。 <br/>有关更多信息，请参阅 [Android开发人员文档](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** （仅限Android） | 将推送通知的重要性从“低”定义为“最大”。 这可确定发送推送通知时“侵入”的程度。 有关更多信息，请参阅 [Android开发人员文档](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** （仅限Android） | 为推送通知设置高优先级或普通优先级。 有关消息优先级的更多信息，请参阅 [Google 开发人员文档](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message)。 |

**相关主题**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [配置推送渠道](push-gs.md)
* [创建新消息](create-message.md)
* [在历程中添加消息](building-journeys/journeys-message.md)
