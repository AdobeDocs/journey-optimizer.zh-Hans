---
solution: Journey Optimizer
product: journey optimizer
title: WhatsApp 消息快速入门
description: 了解如何在 Journey Optimizer 中创建和发送 WhatsApp 消息
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
TQID: https://experienceleague.adobe.com/uHzRC9X6rB9EXH4gIFiRxFaeNcrTD0-40RrxZkN4XFg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b8df23d2-98a2-4406-86cc-2babe8728d36id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 43066cc40499d87771b251766d5fa6b96afb1bb5
workflow-type: ht
source-wordcount: 707
ht-degree: 100%

---

# WhatsApp 消息快速入门 {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解 WhatsApp 渠道在 Journey Optimizer 中的工作方式及其先决条件和限制，以便您可以决定如何将 WhatsApp 添加到您的历程和营销活动中。

>[!ENDSHADEBOX]

您现在可以使用 Meta 的 [Cloud API](https://developers.facebook.com/docs/whatsapp/cloud-api/) 直接通过 Journey Optimizer 发送 WhatsApp 消息。 此功能可以将 WhatsApp 无缝集成到历程和营销活动中，加强与收件人的沟通，并增强其参与度。

* 在&#x200B;**历程**&#x200B;中。 创建历程、添加 **WhatsApp** 活动并定义基本设置，然后定位到&#x200B;**[!UICONTROL 操作：WhatsApp]** 右侧窗格，创建 WhatsApp 消息的内容。 在[此页面](../building-journeys/journey-gs.md)中了解如何创建历程。

* 在&#x200B;**营销活动**&#x200B;中。 创建营销活动，选择 **WhatsApp** 作为您的操作并定义基本设置，然后编辑消息内容以定义要发送的 WhatsApp 消息。 了解如何创建[操作营销活动](../campaigns/campaign-action.md#action-campaign-action) | [API 触发的营销活动](../campaigns/api-triggered-campaigns.md) | [编排的营销活动](../orchestrated/create-orchestrated-campaign.md#create)

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## 用例 {#use-cases}

当您的受众已使用 WhatsApp，并且您想要将丰富的内容与真正的双向对话结合起来时，该平台的效果最佳。

| 好处 | 原因 | 示例用例 |
| --- | --- | --- |
| 高全球参与度 | 广泛使用的消息平台，在许多区域有很高的采用率 | 触达已在 WhatsApp 上活跃的国际受众 |
| 丰富的交互式消息 | 支持图像、视频、按钮和快速回复 | 产品目录、带快速回复选项的预约确认 |
| 双向对话体验 | 收件人可以在同一会话中回复 | 客户支持对话、订单跟踪问题 |
| 交互式多屏幕体验 | WhatsApp Flow 模板允许您在聊天中构建引导式多步交互 | 调查、销售线索获取表单 |
| 通过官方 API 实现合规性和信任 | 通过经 Meta 验证的 Cloud API 以及发件人验证功能进行投放 | 经过品牌验证的通信内容，有助于建立收件人的信任 |
| 与其他渠道集成 | 可与历程和营销活动结合，并与其他渠道搭配使用 | 使用 WhatsApp 作为补充接触点的多渠道历程 |

## 何时不使用 {#when-not-to-use}

由于 WhatsApp 依赖于受众采用和明确同意，因此它并非适用于所有场景。在以下情况下考虑其他渠道：

* 您的受众不使用 WhatsApp，因为其采用率因区域和人口统计特征而异
* 收件人没有明确同意选择启用，而这是 Meta 的消息政策所要求的
* 消息具有紧急性，需要保证投放成功，考虑到 WhatsApp 的投放和模板审核约束，短信或推送更为适用
* 内容较长或较复杂，更适合通过电子邮件发送，因为电子邮件可提供更大的空间和更丰富的格式
* 实时对话支持对您而言不可行，因为双向 WhatsApp 会话会带来及时回复的预期

## 先决条件 {#prereq}

将 WhatsApp 与 Journey Optimizer 集成需要具有：

* Meta 企业管理帐户
* [经过发件人姓名和电话号码验证的 WhatsApp 商业帐户](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [具有适当权限的用户授权令牌](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [已批准的 Meta 模板](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

在继续集成之前，您还需要了解以下信息：

* [WhatsApp 内容规则](https://www.whatsapp.com/legal/messaging-guidelines)
* [遵守 Meta 的政策](https://www.whatsapp.com/legal)
* [24 小时对话限制](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## 限制 {#limitations}

以下限制适用于 WhatsApp 渠道：

* Adobe Journey Optimizer 中的 WhatsApp 渠道支持 HIPAA，但 Adobe BAA 未覆盖第三方供应商。 客户需对合规性和供应商验证自行负责。

* 请注意，尚不支持自动或预定义答复消息。

* 自 2025 年 4 月起，已暂时停止向使用美国电话号码（以 +1 拨号代码和美国区号组成的号码）的 WhatsApp 用户发送所有营销模板消息。 [在 Meta 文档中了解详情](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* 原生集成功能不允许与第三方业务服务提供商 (BSP) 集成。

## 操作方法视频 {#video}

以下视频展示了如何将 WhatsApp 集成为 Adobe Journey Optimizer 中的原生渠道，从而大规模提供安全、实时、个性化的消息。

+++ 观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3470244?learn=on)

+++

## 其他学习资源

浏览有关 WhatsApp 消息和配置的更多视频教程。

➡️ [WhatsApp 渠道教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/channels/whatsapp/whatsapp-introduction){target="_blank"}

