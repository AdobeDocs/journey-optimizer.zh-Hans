---
solution: Journey Optimizer
product: journey optimizer
title: 开始使用 [!DNL Journey Optimizer] 渠道配置
description: 了解有关 [!DNL Journey Optimizer] 渠道配置的更多信息
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: 配置、进行配置、消息、渠道、沙盒、Optimizer
TQID: https://experienceleague.adobe.com/zHp3C6KVKfRsQbi4B710ACFuMQhGuVxjaNIrXkxwhMc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c343082f-e963-4f57-a96b-b64d27f8118e
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: efb19423-4da4-4fd1-88d8-5ee8c71ae766
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d9c480cc48c4352e82d1f4624c65fc16a60b959
workflow-type: tm+mt
source-wordcount: 497
ht-degree: 30%

---

# 渠道配置快速入门 {#start-optimizer-configuration}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何配置渠道、子域、IP预热和业务规则，以便在Adobe Journey Optimizer中开始发送消息。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_channels_rate_controls"
>title="渠道速率控制"
>abstract="渠道速率控制"

首次访问 [!DNL Journey Optimizer] 时，系统会为您设置一个生产沙盒，并根据合同分配特定数量的 IP。

要能够发送消息，您需要完成下面列出的配置步骤：

1. 作为[Adobe Journey Optimizer系统管理员](../start/path/administrator.md)，定义特定于渠道的配置。 请在以下页面中了解如何设置这些配置：

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../email/get-started-email-config.md"><img alt="电子邮件" src="../channels/assets/do-not-localize/email.png"></a>
    <div align="center"><a href="../email/get-started-email-config.md"><strong>电子邮件</strong></a></div></td>
    <td><a href="../mobile/mobile-configuration.md"><img alt="短信" src="../channels/assets/do-not-localize/sms.png"></a>
    <div align="center"><a href="../mobile/mobile-configuration.md"><strong>短信</strong></a></div></td>
    <td><a href="../push/push-configuration.md"><img alt="推送" src="../channels/assets/do-not-localize/push.png"></a>
    <div align="center"><a href="../push/push-configuration.md"><strong>推送通知</strong></a></div></td>
    <td><a href="../direct-mail/direct-mail-configuration.md"><img alt="直邮" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
    <div align="center"><a href="../direct-mail/direct-mail-configuration.md"><strong>直邮</strong></a></div></td>
    </tr></table>

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../in-app/inapp-configuration.md"><img alt="应用程序内" src="../channels/assets/do-not-localize/inapp.jpg"></a>
    <div align="center"><a href="../in-app/inapp-configuration.md"><strong>应用程序内</strong></a></div></td>
    <td><a href="../web/web-configuration.md"><img alt="Web" src="../channels/assets/do-not-localize/web.jpg"></a>
    <div align="center"><a href="../web/web-configuration.md"><strong>Web</strong></a></div></td>
    <td><a href="../code-based/code-based-configuration.md"><img alt="基于代码的体验" src="../channels/assets/do-not-localize/code.png"></a>
    <div align="center"><a href="../code-based/code-based-configuration.md"><strong>基于代码的体验</strong></a></div></td>
    <td><a href="../content-card/content-card-configuration-prereq.md"><img alt="内容卡片" src="../channels/assets/do-not-localize/cards.png"></a>
    <div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong>内容卡片</strong></a></div></td>
    </tr></table>

   有关其他渠道，请参阅：[iOS Live活动](../mobile-live/mobile-live-configuration.md)、[WhatsApp](../whatsapp/whatsapp-configuration.md)和[LINE](../line/line-configuration.md)。

   >[!NOTE]
   >
   >对于移动渠道，[引导式渠道设置](set-mobile-config.md)有助于快速配置营销渠道，确保所有所需资源在Experience Platform、Journey Optimizer和数据收集中随时可用。 这使您的营销团队能够开始创建营销活动和历程。

1. 完成后，您必须通过创建&#x200B;**通道配置**&#x200B;来配置传递消息所需的所有技术参数。 [了解有关渠道配置的更多信息](channel-surfaces.md)

1. 根据您使用的渠道、环境和需求，还必须执行以下步骤：

   * 您的渠道的子域配置和委派，如[电子邮件](about-subdomain-delegation.md)、[短信](../mobile/mobile-subdomains.md)、[登陆页面](../landing-pages/lp-subdomains.md)和[Web体验](../web/web-delegated-subdomains.md)。

   * 设置IP预热计划以实现最佳可投放性。 [了解详情](ip-warmup-gs.md)

   * 定义电子邮件发送的允许列表。 [了解详情](allow-list.md)

   * 管理在将电子邮件地址发送到禁止列表之前执行重试的天数。 [了解详情](manage-suppression-list.md)

   * 启用&#x200B;**密件抄送电子邮件选项**&#x200B;以保留发送给个人的邮件副本。 [了解详情](archiving-support.md#enable-bcc)

   * 配置&#x200B;**业务规则**&#x200B;以避免过度向收件人发送请求。 [了解详情](../conflict-prioritization/rule-sets.md)

   * 在 Adobe Experience Platform 中存在多个地址/号码时，确定要优先用于收件人的电子邮件地址和/或电话号码。 [了解详情](primary-email-addresses.md)

## 其他资源

* **[配置渠道界面](channel-surfaces.md)** — 了解如何设置和管理电子邮件、推送、短信和其他渠道的渠道界面。
* **[子域委派](delegate-subdomain.md)** — 了解如何将子域委派给Adobe以便电子邮件可投放性和品牌化。
* **[IP热身](ip-warmup-gs.md)** — 了解IP地址热身的最佳实践，以改善电子邮件可投放性和发件人信誉。
* **[管理禁止列表](manage-suppression-list.md)** — 了解如何管理禁止列表以处理退回和维护列表卫生。
* **[配置移动应用程序](set-mobile-config.md)** — 设置推送通知和应用程序内消息传送的移动应用程序配置。
* **[配置iOS Live活动](../mobile-live/mobile-live-configuration.md)** — 设置您的环境以将实时活动发送到iPhone锁屏界面和Dynamic Island。
* **[配置WhatsApp](../whatsapp/whatsapp-configuration.md)** — 通过Meta的Cloud API为营销活动和历程设置WhatsApp消息传送。
* **[配置LINE](../line/line-configuration.md)** — 为营销活动和历程设置LINE消息。
* **[配置教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/configure-channels){target="_blank"}** — 浏览有关渠道配置和最佳实践的分步视频教程。
