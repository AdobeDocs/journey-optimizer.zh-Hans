---
solution: Journey Optimizer
product: journey optimizer
title: 直邮快速入门
description: 了解如何在 Journey Optimizer 中创建直邮消息
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: 直邮、消息、营销活动
exl-id: bb52f400-6289-4a7f-a34f-98eb5d27c76a
TQID: https://experienceleague.adobe.com/Gmtr-7HW70-cg7va8iHfR5xKdYts-ZdDCm6CeQHJ0tg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: cb1f1586-9fb4-4de2-8332-02cebb88d42did: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: e7702a4706509a8181ee39cccc510656c5230a16
workflow-type: tm+mt
source-wordcount: 487
ht-degree: 89%

---

# 直邮快速入门 {#create-direct}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解直邮渠道的工作方式，以便您生成第三方提供商用于向客户发送实体邮件的提取文件。

>[!ENDSHADEBOX]

直邮是一种离线渠道，允许您生成第三方直邮服务提供商向客户发送邮件所需的提取文件并进行个性化设置。

在创建直邮营销活动或历程时，Journey Optimizer 会自动生成一个文件，其中包含所有定位的轮廓和所选数据，如邮政地址和轮廓属性。 此文件将会被发送到您选择的服务器，以便您选择的第三方直邮服务提供商可以访问该文件，该提供商将为您处理实际的邮寄过程。

您需要与所选的第三方直邮提供商合作，从您的客户处获得任何必要的同意（如有），以便您的客户可以从您那里接收邮件。

使用邮寄服务受适用的第三方直邮提供商的附加条款与条件的约束。  Adobe 无法控制您使用第三方产品，因此无需承担责任。 有关直邮营销活动邮寄的任何问题或协助请求，请与您选择的第三方直邮提供商联系。

## 开始之前 {#before-you-start}

在创建直邮消息之前，请配置[文件路由和直邮渠道配置](direct-mail-configuration.md)。 您还需要在 Adobe Experience Platform 中拥有受众和配置文件数据（例如邮寄地址）。

发送直邮消息的主要步骤如下：

![从配置到投递的直邮创建工作流程](assets/dm-creation-process.png)

>[!AVAILABILITY]
>
>直邮消息可以在历程和营销活动的上下文中创建。 不可用于 API 触发的营销活动。

![Journey Optimizer 中直邮渠道的动画概览](../rn/assets/do-not-localize/gif-dm.gif)

## 其他资源 {#additional-resources}

* **[创建直邮](create-direct-mail.md)** - 了解如何创建直邮投放和配置离线渠道的提取文件。
* **[配置直邮渠道](direct-mail-configuration.md)** – 设置直邮表面和文件路由配置。
* **[直邮中的批量决策](../experience-decisioning/batch-decisioning-direct-mail.md)** — 使用决策功能对直邮的提取文件进行个性化设置，或导出下游系统的决策数据。
* **[测试和发送直邮](test-send-direct-mail.md)** - 了解如何测试、验证和发布直邮投放。
* **[直邮教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/channels/direct-mail-channel/direct-mail){target="_blank"}** - 浏览关于直邮功能和最佳实践的分步视频教程。

## 操作说明视频 {#how-to-video}

了解如何利用 Adobe Journey Optimizer 中的直邮渠道在您的历程中自动安排直邮投放。

+++ 观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3479162?quality=12)

+++

如需查看相同步骤的书面演示，请参阅[直邮渠道教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/channels/direct-mail-channel/direct-mail){target="_blank"}。

关于直邮的常见问题，请参阅上文中的[其他资源](#additional-resources)部分。
