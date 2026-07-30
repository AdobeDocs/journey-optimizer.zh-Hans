---
solution: Journey Optimizer
product: journey optimizer
title: 推送通知入门
description: 了解如何在 Journey Optimizer 中创建推送通知
feature: Overview, Push
topic: Content Management
role: User
level: Beginner
exl-id: c1f16edd-efdf-41c2-a0ad-5f55009008f5
TQID: https://experienceleague.adobe.com/S-3ZtTNfgZGEFChfjaXPihxGWpdkWacrWF9AWc-AyZY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 651
ht-degree: 57%

---

# 推送通知入门 {#gs-push-notification}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;开始使用 Adobe Journey Optimizer 中的推送通知，以便通过历程和营销活动联系您的移动应用程序用户和 Web 访客。

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>如果您是首次创建推送通知，请确保已配置推送渠道。 [了解详情](push-gs.md)。

推送通知可帮助您随时联系移动应用用户和 Web 访问者，尤其是当他们未主动使用应用或浏览网站时。 推送通知可帮助您实现各种用例，例如提供有关服务的更新、要求用户执行操作、向用户发送新交易的提醒等。 终端用户需要先选择启用，设备平台才会允许其接收或查看通知。 用户可在应用程序安装完成后首次启动时、后续会话或工作流程中（视情况而定）选择启用。

[!DNL Journey Optimizer] 支持推送通知，并帮助您以行业领先的吞吐率发送高度相关的通知。 推送通知可能包括个性化和基于历程的上下文，以便利用您的品牌对[!DNL Adobe CX Enterprise]的数据洞察。

可以通过以下方式创建推送通知：

* 在&#x200B;**历程**&#x200B;中：在历程中添加推送活动并定义基本设置后，请使用&#x200B;**[!UICONTROL 操作：推送]**&#x200B;右侧窗格，创建推送通知内容。 [了解如何创建历程](../building-journeys/journey-gs.md)

* 在&#x200B;**营销活动**&#x200B;中：创建营销活动后，选择推送通知作为您的操作并定义基本设置。 了解如何创建[操作营销活动](../campaigns/campaign-action.md#action-campaign-action) | [API 触发的营销活动](../campaigns/api-triggered-campaigns.md) | [编排的营销活动](../orchestrated/create-orchestrated-campaign.md#create)

使用专用选项卡定义 **iOS**、**Android** 和 **Web** 平台的推送通知设置。

>[!NOTE]
>
>虽然 **[!DNL Journey Optimizer]** 提供了在电子邮件和短信消息中管理选择退出的方法，但推送通知不需要您采取任何操作，因为收件人可以通过其设备自行取消订阅。 例如，在下载或使用应用程序时，用户可以选择停止发送通知。 同样，他们可以通过移动操作系统或 Web 浏览器设置更改通知设置。 要验证轮廓在 AEP 轮廓查看器中的推送同意状态，请参阅[检查推送选择退出状态](../privacy/opt-out.md#push-opt-out-status)。

</br>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-push.md">
<img alt="潜在客户" src="../assets/do-not-localize/push-create.jpg">
</a>
<div><a href="create-push.md"><strong>创建推送通知</strong>
</div>
<p>
</td>
<td>
<a href="design-push.md">
<img alt="不频繁" src="../assets/do-not-localize/push-design.jpg">
</a>
<div>
<a href="design-push.md"><strong>设计推送通知</strong></a>
</div>
<p></td>
<td>
<a href="send-push.md">
<img alt="验证" src="../assets/do-not-localize/push-sending.jpg">
</a>
<div>
<a href="send-push.md"><strong>发送推送通知</strong></a>
</div>
<p>
</td>
<td>
<a href="push-gs.md">
<img alt="验证" src="../assets/do-not-localize/push-config.jpg">
</a>
<div>
<a href="push-gs.md"><strong>配置推送通知</strong></a>
</div>
<p>
</td>
</tr></table>

## 用例

当您需要直接快速联系用户的设备时，推送通知的工作效果最佳，无需用户进入您的应用程序或检查其收件箱。

| 好处 | 原因 | 示例用例 |
| --- | --- | --- |
| 时效性更新 | 即刻交付，即使用户没有主动使用您的应用程序 | 航班延误警报，订单状态更改，突发新闻 |
| 重新参与 | 提示用户在处于非活动状态一段时间后返回您的应用程序 | 购物车放弃提醒、回馈活动 |
| 与短信相比降低了成本 | 与短信不同，不收取每条消息的运营商费用 | 大量促销或事务性通知 |
| 丰富的交互式内容 | 支持图像、操作按钮和深层链接 | 带点击购买按钮的产品促销活动，富媒体预览 |
| 设备本机功能 | 利用其他渠道不可用的操作系统级功能 | 振动警报、应用程序图标徽章、地理围栏位置触发器 |
| 高选择加入可能性 | 系统提示用户尽早选择加入应用程序安装或首次启动 | 载入流程、第一天参与活动 |

## 何时不使用

推送通知不适合每条消息。 在以下情况下考虑其他渠道：

* 您的受众推送选择加入率很低，或者对通知表现出抵制态度，因为消息可能永远不会到达受众
* 消息需要长格式内容，电子邮件可处理得更好，并允许更详细的格式设置
* 该内容是敏感内容或隐私内容，不应在锁屏界面中显示，因为在该界面中，设备附近的任何人都可以看到
* 您的大多数用户都从桌面而不是移动应用程序访问您的服务，因为推送通知在此类应用程序中的覆盖范围有限或无法访问

