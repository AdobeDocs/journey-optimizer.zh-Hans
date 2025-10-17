---
solution: Journey Optimizer
product: journey optimizer
title: 文本消息（短信/彩信/RCS）快速入门
description: 了解如何在 Journey Optimizer 中创建和发布文本消息
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
source-git-commit: 0a9c36b75f7433eadbc8894fb7252a8f846c78b2
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 29%

---

# 文本消息快速入门 {#get-started-sms}

使用 [!DNL Journey Optimizer] 向客户的移动设备发送文本消息（短信/彩信/RCS）。您可以在短信/彩信/RCS 编辑器中创建、个性化和预览文本格式的消息。

可以在历程或营销活动中创建和发送短信。对于短信、彩信和 RCS，使用短信操作。

* 在&#x200B;**历程**&#x200B;中。创建历程、添加短信活动并定义基本设置。然后，浏览到右侧的SMS操作窗格，为SMS、MMS或RCS消息创建内容。 [了解如何创建历程](../building-journeys/journey-gs.md)

* 在&#x200B;**营销活动**&#x200B;中。创建一个营销活动，选择“短信”作为操作并定义基本设置。然后，编辑消息内容以定义要发送的短信、彩信或 RCS 消息。[了解如何创建营销活动](../campaigns/create-campaign.md#configure)

>[!IMPORTANT]
>
>如果这是您首次创建短信，请确保已配置短信渠道。 [了解详情](sms-configuration.md)

## 短信功能 {#sms-capabilities}

Adobe Journey Optimizer提供全面的文本消息传送功能，可通过多个渠道吸引客户：

**短信（短信服务）**

发送最多160个字符的纯文本消息。 SMS是所有移动设备中支持最广泛的文本消息格式。

**MMS（多媒体消息服务）**

使用多媒体内容（包括视频、图像、音频剪辑和GIF）增强您的通信。 除了媒体文件之外，MMS消息最多可包含1600个字符的文本。 [了解有关MMS限制的更多信息](../start/guardrails.md#sms-guardrails)

**RCS （丰富通信服务）**

使用高级功能（如轮播、丰富卡片、建议的操作和增强的媒体支持）发送品牌交互式消息。 RCS在支持的设备上提供更丰富的消息传送体验。

## 主要功能 {#key-features}

**Personalization和动态内容**

使用个性化编辑器创建个性化文本消息。 添加用户档案属性、条件内容和动态数据，以针对每位收件人定制消息。 [了解个性化](../personalization/personalize.md)

**多个提供程序支持**

Adobe Journey Optimizer与领先的短信服务提供商集成：

* **Sinch** - [配置指南](sms-configuration-sinch.md)
* **Twilio** - [配置指南](sms-configuration-twilio.md)
* **Infobip** - [配置指南](sms-configuration-infobip.md)
* **自定义提供商** — 使用自定义API集成配置任何其他SMS提供商。 [了解详情](sms-configuration-custom.md)

**URL缩短和跟踪**

向消息中添加缩短的可跟踪URL以监测参与情况。 需要子域配置才能实现URL缩短功能。 [了解如何配置SMS子域](sms-subdomains.md)

**选择退出管理**

通过内置的选择退出管理确保遵守行业标准和法规。 Journey Optimizer会自动处理Sinch和Infobip提供商的标准选择退出关键词（STOP、QUIT、CANCEL等）。 [了解选择退出管理](sms-opt-out.md)

**预览和测试**

使用测试用户档案和示例数据发送之前，请先测试您的文本消息。 预览个性化、内容和格式，以确保消息正确显示。 [了解如何发送邮件](send-sms.md)

**Reporting &amp; Analytics**

通过全面的报告功能跟踪短信活动和历程的性能：

* [通过短信发送营销活动报告](../reports/campaign-global-report-cja-sms.md)
* [短信历程报告](../reports/journey-global-report-cja-sms.md)

## 配置要求 {#configuration-requirements}

在发送文本消息之前，您必须：

1. **选择SMS提供程序** — 从Sinch、Twilio、Infobip中选择，或配置自定义提供程序
2. **设置API凭据** — 将提供商的API令牌和服务ID与Journey Optimizer集成
3. **创建渠道配置** — 为营销和事务性消息设置短信配置
4. **配置子域（可选）** — 只有在您打算在邮件中使用URL缩短时才需要

这些配置步骤通常由系统管理员执行。 [开始使用短信配置](sms-configuration.md)

## 快速入门指南 {#quick-start}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="sms-configuration.md">
<img alt="验证" src="../assets/do-not-localize/sms-config.jpg">
</a>
<div>
<a href="sms-configuration.md"><strong>配置短信渠道</strong></a>
</div>
<p>设置短信提供商和渠道配置</p>
</td>
<td>
<a href="create-sms.md">
<img alt="潜在客户" src="../assets/do-not-localize/sms-create.jpeg">
</a>
<div><a href="create-sms.md"><strong>创建短信</strong>
</div>
<p>设计并个性化您的短信、彩信或RCS内容</p>
</td>
<td>
<a href="send-sms.md">
<img alt="不频繁" src="../assets/do-not-localize/sms-sending.jpg">
</a>
<div>
<a href="send-sms.md"><strong>预览和发送</strong></a>
</div>
<p>测试您的短信并将其发送给受众</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="验证" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>管理选择退出</strong></a>
</div>
<p>处理取消订阅请求并确保法规遵从性</p>
</td>
</tr></table>

## 其他资源 {#additional-resources}

**配置指南**

* [短信渠道配置概述](sms-configuration.md)
* [创建短信渠道配置](sms-configuration-surface.md)
* [配置短信子域以缩短URL](sms-subdomains.md)

**提供程序设置指南**

* [配置 Sinch 提供程序](sms-configuration-sinch.md)
* [配置 Twilio 提供程序](sms-configuration-twilio.md)
* [配置 Infobip 提供程序](sms-configuration-infobip.md)
* [配置自定义短信提供程序](sms-configuration-custom.md)

**内容创建和管理**

* [创建短信/彩信消息](create-sms.md)
* [预览、测试和发送消息](send-sms.md)
* [短信中的Personalization](../personalization/personalize.md)
* [动态内容](../personalization/get-started-dynamic-content.md)

**合规性和隐私**

* [选择退出管理](sms-opt-out.md)
* [隐私和同意](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**性能跟踪**

* [通过短信发送营销活动报告](../reports/campaign-global-report-cja-sms.md)
* [短信历程报告](../reports/journey-global-report-cja-sms.md)

**历程与营销活动集成**

* [将短信消息添加到历程](../building-journeys/journeys-message.md)
* [创建短信营销活动](../campaigns/create-campaign.md)

## 操作说明视频 {#videos}

**配置和发送SMS消息**

了解如何配置、创作短信消息，并将其包含在客户历程中。

+++观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3422699?captions=chi_hans&learn=on)

+++

**探索移动消息传送功能**

了解Adobe Journey Optimizer为营销人员提供的全面的移动消息传送功能。

+++观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3430378?captions=chi_hans&quality=12&learn=on)

+++

**发送品牌RCS消息**

了解如何在 Adobe Journey Optimizer 中使用自定义 SMS 提供商配置并发送品牌化的交互式 RCS 消息。

+++观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3464765?captions=chi_hans)

+++

**相关主题**

* [在历程中添加消息](../building-journeys/journeys-message.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [护栏和限制](../start/guardrails.md#sms-guardrails)
