---
title: 创建收件箱
description: 开始使用 Adobe Journey Optimizer 中的收件箱，向用户传递持久、非侵入式消息。
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: c2bb6cf702a14b4eef8f2209082e39cd73338378
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 92%

---

# 开始使用收件箱 {#inbox-gs}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解收件箱渠道如何将营销消息保留在您的应用程序或网站内的一个永久位置，以便用户能够返回阅读并在方便时对其执行操作。

>[!ENDSHADEBOX]

收件箱可在移动应用程序或网站内提供一个集中的位置，用于持久展示低摩擦的消息。 应用程序内和推送功能在轻扫或点按后可能会消失；收件箱可保持消息可用，以便人们可以在适合时打开、阅读和操作这些消息。

收件箱基于内容卡渠道构建，并增加了以下功能：

* **持久消息**：内容会保留在收件箱中，直到您将其删除或消息过期，这样用户便可以在关闭通知或离开应用程序后返回收件箱。
* **集中式位置**：应用或网站中用于相关营销消息的单个邮箱。
* **灵活的实施**：使用现成的收件箱容器或在您自己的 UI 中定制体验。
* **阅读状态**：可以在打开邮件的设备上将邮件标记为已读或未读。

## 快速入门指南

按照以下步骤配置和使用收件箱：

1. [配置 Adobe Journey Optimizer](inbox-configuration.md)

   在&#x200B;**渠道配置**&#x200B;下添加&#x200B;**收件箱**&#x200B;渠道配置，以便 Journey Optimizer 了解收件箱运行的位置和方式（网页或规则，或者移动应用程序表面）。

1. [在 Journey Optimizer 中创建收件箱](inbox-create.md)

   创建使用&#x200B;**内容卡**&#x200B;操作的营销活动，并选择&#x200B;**收件箱**&#x200B;作为投放位置 – 可通过 UI 设定运行计划，或由 API 触发。

1. [设计收件箱](inbox-design.md)

   选择收件箱模板和列表或扩展版面，以便消息符合您的品牌和 UX。

1. [创建内容卡并将其链接到收件箱](../content-card/create-content-card.md)

   在设计器中创作信息卡内容，完成收件箱特定选项，然后激活您的营销活动，以便消息到达收件箱。

## 其他资源

* [收件箱 UI (iOS)](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS)：使用 Adobe Experience Platform Mobile SDK（iOS 15 或更高版本、Xcode 15 或更高版本、Swift 5.1 或更高版本）在 iOS 应用程序中实施 Journey Optimizer 收件箱的相关要求、公共 API 表面、收件箱设置以及教程链接。

* [获取并显示收件箱](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox)：加载 Journey Optimizer 收件箱消息并呈现 Android 上的收件箱 UI（Adobe Developer 文档）。

* [自定义收件箱](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox)：调整 Android 应用程序的收件箱布局、样式和交互行为（Adobe Developer 文档）。

* [监听收件箱事件](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events)：订阅 Android 上的用户操作和生命周期更新的收件箱回调（Adobe Developer 文档）。
