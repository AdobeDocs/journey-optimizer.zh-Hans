---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer中的推送通知流
description: 了解推送通知数据流和组件
topic: Mobile
feature: Push
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 014cc551cb125ba6dc20a4f572e6cd7024d9fab5
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 6%

---

# 推送通知数据流和组件 {#get-started-push}

此页面可帮助您在中设置并了解与推送通知相关的关键服务和工作流 [!DNL Journey Optimizer].


>[!AVAILABILITY]
>
>新 **移动载入快速启动工作流** 现已可用。 使用此新产品功能可快速配置Mobile SDK，以开始收集和验证移动事件数据，以及发送移动推送通知。 此功能可通过数据收集主页作为公共测试版访问。 [了解详情](mobile-onboarding-wf.md)

了解如何在 [本页](create-push.md).

在中配置推送渠道的步骤 [!DNL Adobe Journey Optimizer] 详见 [本页](push-configuration.md).

下图显示了与关联数据流相关的系统和服务，重点说明了如何从端到端服务角度交付推送通知。

![](assets/push-flow.png)

1. 在Apple的APNs和Google FCM推送消息服务中注册您的品牌移动应用程序(Android或iOS)
1. 消息传送服务会生成推送令牌，该令牌是 [!DNL Adobe Journey Optimizer] 将用于通过推送通知来定位特定设备。
1. 之前生成的推送令牌将传递到Adobe Experience Platform并与实时客户资料同步；这是通过OOTB与易于集成的客户端SDK来完成的
1. 在中创作推送消息 [!DNL Adobe Journey Optimizer]，则会根据渠道表面（即，消息预设）创建推送消息
1. 推送消息可能包含在编排画布上的历程
1. 在历程发布后，基于历程条件的客户用户档案将被鉴定为接收推送通知，在此步骤中将个性化推送消息负载
1. 个性化推送负载被转发到内部推送消息传递服务
1. 然后，此内部服务将验证与该消息关联的应用程序的凭据，并
1. 将消息发送到Apple和Google消息传送服务以进行最终交付
1. 在历程实时和全局报告中，已记录来自消息传送服务的反馈，并记录了错误和成功案例
1. 推送通知会交付给最终用户设备
1. 最终用户推送通知交互通过SDK集成从最终用户客户端以Experience事件的形式发送

## 关键服务在推送通知中的角色 {#roles-of-key-services}

* **推送通知服务提供商** 是核心组件web服务，用于将通知从远程服务器传递到移动应用程序。

   [!DNL Adobe Journey Optimizer]  同时支持Android和iOS平台，因此可与以下内容集成：
   * [Firebase Cloud Messaging(FCM)](https://firebase.google.com/docs/cloud-messaging)  — 向Android移动设备应用程序发送通知
   * [Apple推送通知服务(APNs)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html)  — 向iOS移动设备应用程序发送通知

* **Adobe Experience Platform Mobile SDK** 它通过与Android和iOS兼容的SDK为手机提供客户端集成API。 SDK提供了 [!DNL Adobe Journey Optimizer] 扩展可公开各种特定于推送消息的API，并启用数据流，例如注册推送令牌或将推送跟踪事件或任何其他自定义体验事件发送到Adobe Experience Platform。 该SDK还提供了各种其他扩展，这些扩展可启用其他Adobe Experience Cloud以及第三方合作伙伴功能。

   SDK集成还需要设置Adobe Experience Platform [数据收集](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=zh-Hans){target="_blank"} 服务，例如：

   * 创建数据流以配置数据流入Adobe Experience Platform的用户档案和体验事件数据集
   * 创建客户端移动资产并添加扩展。 SDK与这些扩展紧密集成，以提供无缝的数据收集体验。
   * 注册移动设备应用程序包标识符和应用程序凭据

* **Adobe Experience Platform实时客户资料**  通过整合来自多个渠道（包括web、移动设备、CRM和第三方）的数据，维护每个客户的整体视图。 档案允许您将您的客户数据整合到一个统一视图中，并提供每个客户交互的带时间戳的可操作帐户。给定应用程序用户的推送令牌将作为记录数据存储在用户的配置文件中，而用户与推送通知进行的交互将作为时间序列事件数据进行跟踪。 [进一步了解Adobe Experience Platform实时客户资料](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}.

* **[!DNL Adobe Journey Optimizer]** :当您的移动设备应用程序与上述组件的集成到位且客户配置文件位于Adobe Experience Platform中后，您便可以在 [!DNL Adobe Journey Optimizer] 以与用户互动。

## 推送技术设置和从业人员工作流 {#push-technical-setup}

下图显示了配置构成推送数据流骨架的组件时涉及的各种端到端步骤。 已根据执行配置的角色和要配置的组件对操作项目进行分类。

![](assets/user-flow.png)

**相关主题**

* [配置推送渠道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report.md#push-global)
* [创建推送通知](create-push.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在营销活动中添加消息](../campaigns/create-campaign.md)