---
solution: Journey Optimizer
product: journey optimizer
title: WhatsApp 消息入门
description: 了解如何在 Journey Optimizer 中创建和发送 WhatsApp 消息
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
source-git-commit: 7f507dc0113e85191429c2c48b873112b590e3ce
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 55%

---

# WhatsApp 消息入门 {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**目录**

* **[WhatsApp 消息入门](get-started-whatsapp.md)**
* [WhatsApp 配置入门](whatsapp-configuration.md)
* [创建 WhatsApp 消息](create-whatsapp.md)
* [检查并发送 WhatsApp 消息](send-whatsapp.md)

>[!ENDSHADEBOX]

您现在可以通过Meta的[Cloud API](https://developers.facebook.com/docs/whatsapp/cloud-api/)直接通过Journey Optimizer发送WhatsApp消息。 此功能可将WhatsApp无缝集成到历程和营销活动中，从而增强与收件人的沟通和参与。

* 在&#x200B;**历程**&#x200B;中。创建历程、添加 **WhatsApp** 活动并定义基本设置，然后定位到&#x200B;**[!UICONTROL 操作：WhatsApp]** 右侧窗格，创建 WhatsApp 消息的内容。在[此页面](../building-journeys/journey-gs.md)中了解如何创建历程。

* 在&#x200B;**营销活动**&#x200B;中。创建营销活动，选择 **WhatsApp** 作为您的操作并定义基本设置，然后编辑消息内容以定义要发送的 WhatsApp 消息。在[此页面](../campaigns/create-campaign.md#configure)中了解如何创建营销活动。

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## 先决条件 {#prereq}

将 WhatsApp 与 Journey Optimizer 集成需要具有：

* Meta 企业管理帐户
* WhatsApp 企业帐户
* WhatsApp 电话号码
* [具有适当权限的用户授权令牌](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [已批准的 Meta 模板](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)
* [Meta Webhook的配置](https://developers.facebook.com/docs/whatsapp/webhooks/)


在继续集成之前，您还需要了解以下信息：

* [WhatsApp 内容规则](https://www.whatsapp.com/legal/messaging-guidelines)
* [遵守 Meta 的政策](https://www.whatsapp.com/legal)
* [24 小时对话限制](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## 限制 {#limitations}

以下限制适用于WhatsApp渠道：

* Adobe Journey Optimizer中的WhatsApp渠道支持HIPAA，但Adobe的BAA不包含第三方供应商。 客户自行负责法规遵从性和供应商验证。

* 请注意，不支持自动或预定义的响应消息。

* 自2025年4月起，向拥有美国电话号码（一个由+1拨号代码和美国区号组成的号码）的WhatsApp用户发送的所有营销模板消息已暂时暂停。 [在元文档中了解详情](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* 本机集成功能不允许与第三方业务服务提供商(BSP)集成。

## 操作说明视频 {#video}


下方视频演示了如何使用 WhatsApp 操作创建历程。

+++ 观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3451621?learn=on)

+++
