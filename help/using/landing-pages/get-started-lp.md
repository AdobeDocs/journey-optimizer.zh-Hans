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
source-git-commit: 90b7d9bfe40e6d68e22a9f1aa8ef6d302a1035d9
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 48%

---

# 登陆页面入门 {#get-started-lp}

登陆页面是指用户在从电子邮件、网站、广告或任何其他数字位置点进后被定向到的独立网页。

[!DNL Journey Optimizer] 允许您创建和设计登陆页面，以将用户定向到在线表单，在该表单中，用户可以选择启用或选择禁用接收通信，或订阅特定服务（如新闻稿）。

➡️ [在此视频中了解有关配置订阅和创建登陆页面的更多信息](#video)

## 何时使用登陆页面 {#when-to-use}

当您想要执行以下操作时使用登陆页面：

* 允许客户&#x200B;**从电子邮件或营销活动中的链接选择加入或选择退出**&#x200B;营销通信
* 允许客户&#x200B;**订阅或取消订阅特定服务或新闻稿**
* 在发送通信前&#x200B;**收集同意**，并通过自动电子邮件确认操作
* 将用户重定向到&#x200B;**专用Web窗体**，而无需在[!DNL Journey Optimizer]外部构建外部页面

## 开始之前 {#prerequisites}

在创建登陆页面之前，请完成以下设置步骤：

1. **配置子域** — 设置专用于托管登陆页面的子域。 [配置登陆页面子域](lp-subdomains.md)
1. **创建登陆页面预设** — 预设定义了应用于登陆页面的子域和其他设置。 [创建预设](lp-presets.md#lp-create-preset)
1. **创建订阅列表**（对于订阅用例） — 如果您希望客户订阅或取消订阅特定服务，则此为必需字段。 [创建订阅列表](subscription-list.md)

## 工作原理 {#how-it-works}

创建和部署登陆页面应遵循以下顺序：

1. **创建并配置**&#x200B;您的登陆页面 — 选择一个预设，设置主页面，然后添加任何所需的子页面。 [创建登陆页面](create-lp.md)
1. **设计页面** — 使用[!DNL Journey Optimizer]的拖放编辑器生成页面内容和表单。 [设计登陆页面](design-lp.md)
1. **测试和发布** — 预览页面，测试表单行为，然后发布以使其上线。 [管理您的登陆页面](manage-lp.md)
1. **消息或历程中的链接** — 将登陆页面URL添加到电子邮件、营销活动或历程操作，以便客户可以访问该页面。

## 主要功能 {#capabilities}

* 利用 [!DNL Journey Optimizer] 内容设计功能可轻松构建&#x200B;**响应式登陆页面**。
* 快捷、实时地设置&#x200B;**选择启用和选择禁用流程**。
* 创建订阅列表，使用户能够&#x200B;**订阅服务**。[了解详情](lp-use-cases.md#subscription-to-a-service)
* 向收件人提供&#x200B;**取消订阅功能**&#x200B;选择不接收通信。[了解详情](lp-use-cases.md#opt-out)
* 选择启用或选择禁用时，发送&#x200B;**确认电子邮件**。 [了解详情](lp-use-cases.md#send-confirmation-email)

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

## 操作方法视频{#video}

以下视频演示如何创建订阅列表、设置登陆页面以提供服务订阅或退订、将（取消）订阅选项集成到消息并配置相关历程。

>[!VIDEO](https://video.tv.adobe.com/v/344396?captions=chi_hans&quality=12&learn=on)
