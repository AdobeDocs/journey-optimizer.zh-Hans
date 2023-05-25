---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer中的推送通知流程
description: 了解推送通知数据流和组件
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

# 推送通知数据流和组件 {#get-started-push}

此页面可帮助您设置和了解中涉及推送通知的关键服务和工作流 [!DNL Journey Optimizer].


>[!AVAILABILITY]
>
>新 **移动载入快速入门工作流** 现已可用。 使用此新产品功能可快速配置Mobile SDK以开始收集和验证移动事件数据，并发送移动推送通知。 作为公开测试版，此功能可通过数据收集主页访问。[了解详情](mobile-onboarding-wf.md)

了解如何在上创建推送通知 [此页面](create-push.md).

在中配置推送渠道的步骤 [!DNL Adobe Journey Optimizer] 详细信息 [此页面](push-configuration.md).

下图显示了与关联的数据流相关的系统和服务，重点说明了如何从端到端服务的角度发送推送通知。

![](assets/push-flow.png)

1. 使用Apple APN和Google FCM推送消息服务注册品牌移动应用程序(Android或iOS)
1. 消息服务生成一个推送令牌，该令牌是一个标识符，用于 [!DNL Adobe Journey Optimizer] 将用于通过推送通知定位特定设备。
1. 之前生成的推送令牌将传递到Adobe Experience Platform并与Real-time Customer Profile同步；此操作通过OOTB完成，并且易于集成客户端SDK
1. 推送消息创作位置 [!DNL Adobe Journey Optimizer]，将根据渠道平面（即消息预设）创建推送消息
1. 推送消息可包含在历程的编排画布中
1. 在历程发布后，根据历程条件的客户配置文件将获得接收推送通知的资格，推送消息有效负载将在此步骤中个性化
1. 个性化推送有效负载被转发到内部推送消息投放服务
1. 然后，此内部服务将验证与消息关联的应用程序的凭据，并且
1. 将消息发送到Apple和Google消息服务以进行最终投放
1. 会记录来自消息服务的反馈，并记录错误和成功以在历程实时和全局报告中报告
1. 推送通知将发送到最终用户设备
1. 最终用户推送通知交互通过SDK集成从最终用户客户端作为体验事件发送

## 关键服务在推送通知中的作用 {#roles-of-key-services}

* **推送通知服务提供商** 是核心组件Web服务，用于将通知从远程服务器发送到移动应用程序。

   [!DNL Adobe Journey Optimizer]  支持Android和iOS平台，因此可与以下集成：
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging)  — 向Android移动应用程序发送通知
   * [Apple推送通知服务(APN)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html)  — 向iOS移动应用程序发送通知

* **Adobe Experience Platform Mobile SDK** 它通过与Android和iOS兼容的SDK，为您的移动设备提供客户端集成API。 SDK提供了 [!DNL Adobe Journey Optimizer] 扩展公开了各种特定于推送消息的API，并支持数据流，例如注册推送令牌或向Adobe Experience Platform发送推送跟踪事件或任何其他自定义体验事件。 SDK还提供了多种其他扩展，以支持其他Adobe Experience Cloud以及第三方合作伙伴功能。

   SDK集成还需要设置Adobe Experience Platform [数据收集](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html){target="_blank"} 服务，例如：

   * 创建数据流以配置用户档案和体验事件数据集，数据流将针对这些数据集进入Adobe Experience Platform
   * 创建客户端移动属性和添加扩展。 SDK与这些扩展紧密集成，以提供无缝的数据收集体验。
   * 注册移动应用程序包标识符和应用程序凭据

* **Adobe Experience Platform Real-time Customer Profile**  通过组合来自多个渠道（包括Web、移动设备、CRM和第三方）的数据，维护每个客户的整体视图。 档案允许您将您的客户数据整合到一个统一视图中，并提供每个客户交互的带时间戳的可操作帐户。给定应用程序用户的推送令牌会根据用户的配置文件存储为记录数据，而用户与推送通知的交互作为时间序列事件数据来跟踪。 [详细了解Adobe Experience Platform Real-time Customer Profile](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}.

* **[!DNL Adobe Journey Optimizer]** ：当您的移动应用程序与上述组件集成就绪并且您的客户配置文件位于Adobe Experience Platform中后，您便可以在中创作和编排推送通知 [!DNL Adobe Journey Optimizer] 与您的用户互动。

## 推送技术设置和从业者工作流 {#push-technical-setup}

下图显示了配置构成推送数据流骨架的组件时涉及的端到端各个步骤。 已根据执行配置的角色和正在配置的组件对措施项进行分类。

![](assets/user-flow.png)

**相关主题**

* [配置推送渠道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report.md#push-global)
* [创建推送通知](create-push.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在营销策划中添加消息](../campaigns/create-campaign.md)