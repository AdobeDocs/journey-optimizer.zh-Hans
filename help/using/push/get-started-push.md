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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 100%

---

# 推送通知入门 {#gs-push-notification}

>[!IMPORTANT]
>
>如果您是首次创建推送通知，请确保已配置推送渠道。 [了解详情](push-gs.md)。

推送通知可帮助您随时联系移动应用用户和 Web 访问者，尤其是当他们未主动使用应用或浏览网站时。 推送通知可帮助您实现各种用例，例如提供有关服务的更新、要求用户执行操作、向用户发送新交易的提醒等。 终端用户需要先选择启用，设备平台才会允许其接收或查看通知。 用户可在应用程序安装完成后首次启动时、后续会话或工作流程中（视情况而定）选择启用。

[!DNL Journey Optimizer] 支持推送通知，并帮助您以行业领先的吞吐率发送高度相关的通知。 推送通知可能包含个性化和基于历程的上下文，以便利用 Adobe Experience Cloud 中有关您的品牌的数据洞察内容。

可以通过以下方式创建推送通知：

* 在&#x200B;**历程**&#x200B;中：在历程中添加推送活动并定义基本设置后，请使用&#x200B;**[!UICONTROL 操作：推送]**&#x200B;右侧窗格，创建推送通知内容。 [了解如何创建历程](../building-journeys/journey-gs.md)

* 在&#x200B;**营销活动**&#x200B;中：创建营销活动后，选择推送通知作为您的操作并定义基本设置。 了解如何创建[操作营销活动](../campaigns/campaign-action.md#action-campaign-action) | [API 触发的营销活动](../campaigns/api-triggered-campaigns.md) | [编排的营销活动](../orchestrated/create-orchestrated-campaign.md#create)

使用专用选项卡定义 **iOS**、**Android** 和 **Web** 平台的推送通知设置。

>[!NOTE]
>
>虽然 **[!DNL Journey Optimizer]** 提供了在电子邮件和短信消息中管理选择退出的方法，但推送通知不需要您采取任何操作，因为收件人可以通过其设备自行取消订阅。 例如，在下载或使用应用程序时，用户可以选择停止发送通知。 同样，他们可以通过移动操作系统或 Web 浏览器设置更改通知设置。 要验证轮廓在 AEP 轮廓查看器中的推送同意状态，请参阅[检查推送选择退出状态](../privacy/opt-out.md#push-opt-out-status)。

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
