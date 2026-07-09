---
solution: Journey Optimizer
product: journey optimizer
title: 移动消息入门
description: 了解如何在Journey Optimizer中创建和发送移动消息
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
TQID: https://experienceleague.adobe.com/Ev0xJ86fpweQxgf-VjGUEl4ebk6BdzhVof2BgiMR9EM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c13ff12d-60f1-49cd-833a-d43359628223
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 1314
ht-degree: 19%

---

# 移动消息入门 {#get-started-sms}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;开始使用Adobe Journey Optimizer中的移动消息传送功能，以在历程和营销活动中创建、个性化和发送SMS、MMS和RCS消息，包括提供商支持、配置要求和RCS先决条件。

>[!ENDSHADEBOX]

使用[!DNL Journey Optimizer]从单个SMS/MMS/RCS编辑器跨三个渠道（**SMS**、**MMS**&#x200B;和&#x200B;**RCS**）向客户发送移动消息，您可以在其中创建、个性化和预览内容。

* **SMS（短信服务）**：发送最多160个字符的纯文本消息，所有移动设备均支持此功能。
* **MMS（多媒体消息服务）**：使用图像、视频、音频剪辑和GIF以及最多1,600个字符的文本丰富您的消息。 [了解有关彩信限制的更多信息](../start/guardrails.md#sms-guardrails)
* **RCS（丰富通信服务）**:Deliver&#x200B;品牌交互式内容，直接在您的客户的原生消息传递应用程序中，无需额外下载应用程序。

>[!IMPORTANT]
>
>如果这是您首次创建移动消息，请确保已配置移动消息渠道。 [了解详情](mobile-configuration.md)

可以使用移动设备消息操作在历程或营销活动中创建和发送移动设备消息：

* 在&#x200B;**历程**&#x200B;中：向历程添加移动消息操作，定义基本设置，然后在右侧的“移动消息操作”窗格中撰写内容。 [了解如何创建历程](../building-journeys/journey-gs.md)

* 在&#x200B;**促销活动**:Create&#x200B;中，选择移动消息作为您的操作，定义基本设置，然后编辑消息内容。 了解如何创建[操作营销活动](../campaigns/campaign-action.md#action-campaign-action) | [API 触发的营销活动](../campaigns/api-triggered-campaigns.md) | [编排的营销活动](../orchestrated/create-orchestrated-campaign.md#create)

## 用例 {#use-cases}

无论用户安装了您的应用程序还是建立了Internet连接，SMS、MMS和RCS都可以在需要可靠地联系用户时发挥最佳作用。

| 好处 | 原因 | 示例用例 |
| --- | --- | --- |
| 最大覆盖范围和即时性 | 接收消息不需要应用程序或互联网连接 | 在未安装智能手机应用程序的情况下联系用户 |
| 有保证的可见性 | 短信的打开率高于90% | OTP代码、约会提醒、投放通知 |
| 通过MMS/RCS提供丰富的内容 | 添加纯文本以外的图像、视频和交互式元素 | 品牌促销、产品目录 |
| 联系没有应用程序访问权限的用户 | 适用于尚未安装或打开应用程序的收件人 | 重新吸引失效的应用程序用户，引导非应用程序客户 |
| 高度紧急的CTA | 频繁地直接交付给设备用户检查 | 快闪销售、欺诈警报、服务中断通知 |
| 与其他渠道分层 | 对推送、电子邮件和应用程序内消息传送功能进行了补充，使覆盖面更广 | 将短信作为后备渠道的多渠道历程 |

## 何时不使用 {#when-not-to-use}

SMS、MMS和RCS并不总是最有效或最合适的选择。 在以下情况下考虑其他渠道：

* 由于短信和彩信是按消息计费的，并且每消息成本会快速大规模增加，因此高发送量会产生成本
* 内容长式或复杂，更适合电子邮件，它支持更丰富的格式和更长的文本
* 收件人未明确选择加入，这在大多数地区及报文传送法规中都带来了法律和合规风险

## 主要功能 {#key-features}

| 功能 | 描述 |
|---|---|
| **个性化** | 使用个性化编辑器，根据用户档案属性、条件内容和动态数据定制消息。 [了解详情](../personalization/personalize.md) |
| **提供程序支持** | 通过API集成与[Sinch](mobile-configuration-sinch.md)、[Twilio](mobile-configuration-twilio.md)、[Infobip](mobile-configuration-infobip.md)或任何[自定义提供程序](mobile-configuration-custom.md)连接。 |
| **URL正在缩短** | 添加缩短的可跟踪URL以监测参与。 需要子域配置。 [了解详情](mobile-subdomains.md) |
| **选择退出管理** | 内置处理标准选择退出关键词（STOP、QUIT、CANCEL等） Sinch和Infobip。 [了解详情](mobile-opt-out.md) |
| **预览和测试** | 发送之前使用测试用户档案和示例数据验证内容。 [了解详情](send-mobile-message.md) |
| **报告** | 使用专用的[营销活动报告](../reports/campaign-global-report-cja-sms.md)和[历程报告](../reports/journey-global-report-cja-sms.md)跟踪营销活动和历程表现。 |

## 配置要求 {#configuration-requirements}

在发送移动设备消息之前，您必须：

1. **选择SMS提供程序**：从Sinch、Twilio、Infobip中选择，或配置自定义提供程序
2. **设置API凭据**：将提供商的API令牌和服务ID与Journey Optimizer集成
3. **创建渠道配置**：为营销和事务性消息设置短信配置
4. **配置子域（可选）**：只有在您打算在邮件中使用URL缩短时才需要

这些配置步骤通常由系统管理员执行。 [短信配置入门](mobile-configuration.md)

### RCS要求 {#requirement-rcs}

在Journey Optimizer中使用RCS需要以下先决条件：

* **Sinch RCS API凭据**：管理员必须为Sinch RCS供应商配置API凭据（项目ID、应用程序ID和API令牌）。 [了解详情](mobile-configuration-sinch.md)
* **移动消息渠道配置**：管理员必须创建渠道配置，并选择启用了RCS的凭据，这样消息将以RCS而不是SMS发送。 [了解详情](mobile-configuration.md)
* **后备短信**：强烈推荐。 设备不支持RCS的收件人将不会收到消息，除非短信回退可用。 没有现有短信流量的客户应购买短信和短代码。 [了解详情](design-mobile.md#rcs-content)
* **支持的供应商**：本机RCS创作需要Sinch RCS（Adobe转售或直接）。 Twilio、Infobip和其他提供商必须使用自定义提供商集成。
* **设备支持**：Android和iOS设备支持RCS交付。 运营商和区域可用性各不相同，RCS在全球并非普遍可用。

## 其他资源 {#additional-resources}

浏览以下主题，了解有关Journey Optimizer中移动消息传递的更多信息。 另请参阅Mobile学习中心中的[SMS/MMS/RCS概述](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/mobile-learning-hub/mobile-channels-overview/sms-mms-rcs-overview){target="_blank"}，了解更多用例和最佳实践。

+++配置指南

了解如何设置和配置短信环境：

* [短信渠道配置概述](mobile-configuration.md)
* [创建短信渠道配置](mobile-configuration-surface.md)
* [配置短信子域以缩短 URL](mobile-subdomains.md)

+++

+++提供程序设置指南

针对每个短信服务提供程序的分步配置：

* [配置 Sinch 提供程序](mobile-configuration-sinch.md)
* [配置 Twilio 提供程序](mobile-configuration-twilio.md)
* [配置 Infobip 提供程序](mobile-configuration-infobip.md)
* [配置自定义短信提供程序](mobile-configuration-custom.md)

+++

+++内容创建和管理

创建、个性化并管理您的移动消息内容：

* [创建短信/RCS/彩信消息](create-mobile-message.md)
* [预览、测试和发送消息](send-mobile-message.md)
* [移动消息中的Personalization](../personalization/personalize.md)
* [动态内容](../personalization/get-started-dynamic-content.md)
* [使用 AI 助手生成短信内容](../content-management/generative-text.md)

+++

+++合规性和隐私

确保您的移动通讯符合法规和隐私标准：

* [选择退出管理](mobile-opt-out.md)
* [隐私和同意](../privacy/opt-out.md#opt-out-decision-management)

+++

+++效果跟踪

监测和分析短信营销活动和历程效果：

* [短信营销活动报告](../reports/campaign-global-report-cja-sms.md)
* [短信历程报告](../reports/journey-global-report-cja-sms.md)

+++

+++历程和营销活动集成

了解如何将短信集成到客户历程和营销活动中：

* [将短信消息添加到历程](../building-journeys/journey-action.md)
* [创建短信营销活动](../campaigns/create-campaign.md)

+++

+++RCS常见问题解答

**Twilio或Infobip是否提供本机RCS消息传递？**

不是。 使用第三方SMS提供程序（如Twilio或Infobip）时，Journey Optimizer中的本机RCS设计器不可用。 但是，可以通过[自定义提供程序集成](mobile-configuration-custom.md)发送RCS消息。

**为什么与RCS一起购买短信？**

应购买短信卷和短代码以启用短信回退，这是推荐的路径。 如果未配置短信，则设备或运营商不支持RCS的用户档案根本不会收到该消息。

**本机RCS消息传送是否适用于Sinch直接客户？**

可以。 使用Sinch的Conversational API的客户可以访问本机RCS创作，包括Adobe resell和Sinch direct客户。

**RCS是否在任何地方都可用？**

不是。 运营商在全球的采用率持续增长，但RCS并非在所有运营商和地区都得到普遍支持。 在规划RCS运动时，应研究区域可用性和载体支持。

**RCS消息在设备上出现的位置？**

RCS消息与标准SMS消息出现在设备的本机消息传送应用程序中的同一位置。 他们从经过认证的品牌发件人到达，向收件人发出信任信号，表明其信息是合法的。

**RCS消息的字符限制是多少？**

富媒体（单个）消息类型最多支持3,072个字符，远远超过标准短信160个字符的限制。 基本RCS消息类型限制为160个字符，符合标准SMS限制。

+++

## 操作说明视频 {#videos}

**配置和发送短信消息**

了解如何配置、创作短信消息，并将其包含在客户历程中。

+++观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3422699?captions=chi_hans&learn=on)

+++

**探索移动消息传送功能**

了解 Adobe Journey Optimizer 为营销人员提供的综合全面的移动端消息传送功能。

+++观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3430378?captions=chi_hans&quality=12&learn=on)

+++

**发送品牌 RCS 消息**

了解如何在 Adobe Journey Optimizer 中使用自定义短信提供商配置并发送品牌化的交互式 RCS 消息。

+++观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3464765?captions=chi_hans)

+++
