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
source-git-commit: 73a347c104fe28799c264f9a8b6c3e5e12c8d892
workflow-type: ht
source-wordcount: '825'
ht-degree: 100%

---

# 文本消息快速入门 {#get-started-sms}

使用 [!DNL Journey Optimizer] 向客户的移动设备发送文本消息（短信/彩信/RCS）。您可以在短信/彩信/RCS 编辑器中创建、个性化和预览文本格式的消息。

可以在历程或营销活动中创建和发送短信。对于短信、彩信和 RCS，使用短信操作。

* 在&#x200B;**历程**&#x200B;中。创建历程、添加短信活动并定义基本设置。然后，浏览到右侧的“短信操作”窗格，以创建短信、彩信或 RCS 消息的内容。[了解如何创建历程](../building-journeys/journey-gs.md)

* 在&#x200B;**营销活动**&#x200B;中。创建一个营销活动，选择“短信”作为操作并定义基本设置。然后，编辑消息内容以定义要发送的短信、彩信或 RCS 消息。了解如何创建[操作营销活动](../campaigns/campaign-action.md#action-campaign-action) | [API 触发的营销活动](../campaigns/api-triggered-campaigns.md) | [编排的营销活动](../orchestrated/create-orchestrated-campaign.md#create)

>[!IMPORTANT]
>
>如果您是首次创建文本消息，请确保已配置短信渠道。[了解详情](sms-configuration.md)

## 文本消息功能 {#sms-capabilities}

Adobe Journey Optimizer 提供全面的文本消息传送功能，可通过多个渠道吸引客户：

**短信（短信服务）**

发送最多 160 个字符的纯文本消息。短信是所有移动设备广泛支持的文本消息格式。

**彩信（多媒体消息服务）**

使用多媒体内容（包括视频、图像、音频剪辑和 GIF）增强通信效果。除了媒体文件之外，彩信消息最多可包含 1600 个字符的文本。[了解有关彩信限制的更多信息](../start/guardrails.md#sms-guardrails)

**RCS（丰富通信服务）**

使用高级功能（如轮播、丰富卡片、建议的操作和增强的媒体支持）发送品牌交互式消息。在支持的设备上，RCS 可提供更丰富的消息传送体验。

## 主要功能 {#key-features}

**个性化和动态内容**

使用个性化编辑器创建个性化文本消息。添加轮廓属性、条件内容和动态数据，针对每位收件人定制消息。[了解个性化](../personalization/personalize.md)

**支持多个提供程序**

Adobe Journey Optimizer 与领先的短信服务提供程序集成：

* **Sinch** - [配置指南](sms-configuration-sinch.md)
* **Twilio** - [配置指南](sms-configuration-twilio.md)
* **Infobip** - [配置指南](sms-configuration-infobip.md)
* **自定义提供程序** - 使用自定义 API 集成，配置任何其他短信提供程序。[了解详情](sms-configuration-custom.md)

**URL 缩短和跟踪**

向消息中添加缩短的可跟踪 URL，监测参与情况。需要子域配置才能实现 URL 缩短功能。[了解如何配置短信子域](sms-subdomains.md)

**选择禁用管理**

通过内置的选择禁用管理，确保遵守行业标准和法规。Journey Optimizer 可自动处理 Sinch 和 Infobip 提供商的标准选择禁用关键词（停止、退出、取消等）。[了解选择禁用管理](sms-opt-out.md)

**预览和测试**

在发送之前，使用测试配置文件和示例数据测试文本消息。预览个性化、内容和格式，确保消息显示正确。[了解如何发送消息](send-sms.md)

**报告和分析**

通过全面的报告功能，跟踪短信营销活动和历程的效果：

* [短信营销活动报告](../reports/campaign-global-report-cja-sms.md)
* [短信历程报告](../reports/journey-global-report-cja-sms.md)

## 配置要求 {#configuration-requirements}

在发送文本消息之前，您必须：

1. **选择短信提供程序** - 从 Sinch、Twilio、Infobip 中进行选择，或配置自定义提供程序
2. **设置 API 凭据** – 将提供商的 API 令牌和服务 ID 与 Journey Optimizer 集成
3. **创建渠道配置** – 为营销和事务性消息设置短信配置
4. **配置子域（可选）** - 只有打算在消息中使用 URL 缩短时才需要配置

这些配置步骤通常由系统管理员执行。[短信配置入门](sms-configuration.md)

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
<div><a href="create-sms.md"><strong>创建文本消息</strong></a>
</div>
<p>设计并个性化短信、彩信或 RCS 内容</p>
</td>
<td>
<a href="send-sms.md">
<img alt="不频繁" src="../assets/do-not-localize/sms-sending.jpg">
</a>
<div>
<a href="send-sms.md"><strong>预览和发送</strong></a>
</div>
<p>测试短信并将其发送给受众</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="验证" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>管理选择禁用</strong></a>
</div>
<p>处理取消订阅请求并确保合规</p>
</td>
</tr></table>

## 其他资源 {#additional-resources}

浏览以下主题，了解有关 Journey Optimizer 文本消息的更多信息。

+++配置指南

了解如何设置和配置短信环境：

* [短信渠道配置概述](sms-configuration.md)
* [创建短信渠道配置](sms-configuration-surface.md)
* [配置短信子域以缩短 URL](sms-subdomains.md)

+++

+++提供程序设置指南

针对每个短信服务提供程序的分步配置：

* [配置 Sinch 提供程序](sms-configuration-sinch.md)
* [配置 Twilio 提供程序](sms-configuration-twilio.md)
* [配置 Infobip 提供程序](sms-configuration-infobip.md)
* [配置自定义短信提供程序](sms-configuration-custom.md)

+++

+++内容创建和管理

创建、个性化和管理文本消息内容：

* [创建短信/彩信消息](create-sms.md)
* [预览、测试和发送消息](send-sms.md)
* [文本消息中的个性化](../personalization/personalize.md)
* [动态内容](../personalization/get-started-dynamic-content.md)

+++

+++合规性和隐私

确保您的文本消息符合法规和隐私标准：

* [选择退出管理](sms-opt-out.md)
* [隐私和同意](../privacy/opt-out.md#opt-out-decision-management)

+++

+++效果跟踪

监测和分析短信营销活动和历程效果：

* [短信营销活动报告](../reports/campaign-global-report-cja-sms.md)
* [短信历程报告](../reports/journey-global-report-cja-sms.md)

+++

+++历程和营销活动集成

了解如何将短信集成到客户历程和营销活动中：

* [将短信消息添加到历程](../building-journeys/journeys-message.md)
* [创建短信营销活动](../campaigns/create-campaign.md)

+++

## 操作说明视频 {#videos}

**配置和发送短信消息**

了解如何配置、创作短信消息，并将其包含在客户历程中。

+++观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3420509?learn=on)

+++

**探索移动消息传送功能**

了解 Adobe Journey Optimizer 为营销人员提供的综合全面的移动端消息传送功能。

+++观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3426021?quality=12&learn=on)

+++

**发送品牌 RCS 消息**

了解如何在 Adobe Journey Optimizer 中使用自定义短信提供商配置并发送品牌化的交互式 RCS 消息。

+++观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3464755)

+++

**相关主题**

* [在历程中添加消息](../building-journeys/journeys-message.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [护栏和限制](../start/guardrails.md#sms-guardrails)
* [短信和移动消息教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/channels/sms-channel/sms-mms-messages-overview){target="_blank"}
