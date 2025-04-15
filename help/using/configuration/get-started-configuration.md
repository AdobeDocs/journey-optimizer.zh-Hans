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
source-git-commit: e052cf9bcd42cecbaaeb9047990ed603dd0730a0
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 48%

---


# 渠道配置入门 {#start-optimizer-configuration}

首次访问 [!DNL Journey Optimizer] 时，系统会为您预置一个生产沙盒，并根据合同分配特定数量的 IP。


要能够发送消息，您需要完成下面列出的配置步骤：

1. 作为[Adobe Journey Optimizer系统管理员](../start/path/administrator.md)，定义您的渠道配置。 请在以下页面中了解如何设置这些配置：

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/get-started-email-config.md"><img alt="电子邮件" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/get-started-email-config.md"><strong>电子邮件</strong></a></div></td>
<td><a href="../sms/sms-configuration.md"><img alt="短信" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/sms-configuration.md"><strong>短信</strong></a></div></td>
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
<div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong>内容卡</strong></a></div></td>
</tr></table>

>[!NOTE]
>
>对于移动渠道，[引导式渠道设置](set-mobile-config.md)有助于快速配置营销渠道，确保所有所需资源在Experience Platform、Journey Optimizer和数据收集中随时可用。 这使您的营销团队能够开始创建营销活动和历程。

1. 完成后，您必须创建&#x200B;**通道配置**&#x200B;以配置传递消息所需的所有技术参数。 [了解有关渠道配置的更多信息](channel-surfaces.md)

1. 您还可以：

   * 管理在将电子邮件地址发送到禁止列表之前执行重试的天数。[了解详情](manage-suppression-list.md)

   * 启用&#x200B;**密送电子邮件选项**，保存发送给客户的邮件副本。[了解详情](archiving-support.md#enable-bcc)

   * 配置&#x200B;**业务规则**&#x200B;以避免过度向收件人发送请求。 [了解详情](../configuration/rule-sets.md)

   * 在 Adobe Experience Platform 中存在多个地址/号码时，确定要优先用于收件人的电子邮件地址和/或电话号码。[了解详情](primary-email-addresses.md)
