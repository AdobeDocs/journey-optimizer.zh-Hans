---
solution: Journey Optimizer
product: journey optimizer
title: 登陆页面入门
description: 了解 Journey Optimizer 中的登陆页面
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: 登陆、登陆页面、开始、入门
exl-id: 0da96e32-52ad-4cc3-bac4-844b1f39ed16
source-git-commit: 2240a4bf85d3f5f41a12d128afdc15431dbab75b
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 22%

---

# 登陆页面入门 {#get-started-lp}

登陆页面是指用户在从电子邮件、网站、广告或任何其他数字位置点进后被定向到的独立网页。

[!DNL Journey Optimizer]允许您创建和设计登陆页面，以将您的用户定向到在线表单，他们可以在其中选择加入或选择退出接收您的通信或特定服务（如新闻稿）。

➡️ [在此视频中了解有关配置订阅和创建登陆页面的更多信息](#video)

## 何时使用登陆页面 {#when-to-use}

当您想要执行以下操作时使用登陆页面：

* 允许客户&#x200B;**从电子邮件或促销活动中的链接**&#x200B;选择加入或选择退出营销通信或特定服务或新闻稿，包括目标服务的订阅列表。 [了解详情](lp-use-cases.md#subscription-to-a-service)
* 在发送通信前&#x200B;**收集同意**，并在选择加入或选择退出时发送&#x200B;**确认电子邮件**。 [了解详情](lp-use-cases.md#send-confirmation-email)
* 将用户重定向到&#x200B;**专用Web窗体**，而无需在[!DNL Journey Optimizer]外部构建外部页面
* 使用&#x200B;**的内容设计功能构建**&#x200B;响应式登陆页面[!DNL Journey Optimizer]

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-lp.md">
<img alt="潜在客户" src="../assets/do-not-localize/lp-subscription.jpeg">
</a>
<div><a href="create-lp.md"><strong>创建登陆页面</strong>
</div>
<p>
</td>
<td>
<a href="subscription-list.md">
<img alt="不频繁" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong>创建订阅列表</strong></a>
</div>
<p></td>
<td>
<a href="design-lp.md">
<img alt="验证" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="design-lp.md"><strong>设计登陆页面</strong></a>
</div>
<p>
</td>
<td>
<a href="../reports/lp-report-live.md">
<img alt="验证" src="../assets/do-not-localize/lp-reporting.jpg">
</a>
<div>
<a href="../reports/lp-report-live.md"><strong>报告</strong></a>
</div>
<p>
</td>
</tr></table>

## 开始之前 {#prerequisites}

在创建登陆页面之前，请完成以下设置步骤：

1. [**配置子域**](lp-subdomains.md) — 设置专用于托管登陆页面的子域。
1. [**创建登陆页面预设**](lp-presets.md#lp-create-preset) — 预设定义了应用于登陆页面的子域和其他设置。
1. [**创建订阅列表**](subscription-list.md)（对于订阅用例） — 如果您希望客户订阅或取消订阅特定服务，则此为必需字段。

## 工作原理 {#how-it-works}

创建和部署登陆页面应遵循以下顺序：

1. [**创建和配置登陆页面**](create-lp.md) — 选择预设，设置主页面，然后添加任何所需的子页面。
1. [**设计页面**](design-lp.md) — 使用[!DNL Journey Optimizer]的拖放编辑器生成页面内容和表单。
1. [**测试**](create-lp.md#test-landing-page)&#x200B;和&#x200B;[**发布**](create-lp.md#publish-landing-page)&#x200B;您的登陆页面 — 预览页面，测试表单行为，然后发布以使其上线。
1. [**消息或历程中的链接**](../email/message-tracking.md#insert-links) — 将登陆页面URL添加到电子邮件、营销活动或历程操作，以便客户可以访问该页面。

## 操作方法视频{#video}

以下视频介绍如何创建订阅列表、设置登陆页面以选择加入或选择退出服务、将选择加入/选择退出选项集成到消息并配置相关历程。

>[!VIDEO](https://video.tv.adobe.com/v/344396?captions=chi_hans&quality=12&learn=on)
