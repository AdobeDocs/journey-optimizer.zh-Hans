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
source-git-commit: d0dd382521aeb2c7e18dc547c2ec55fa1472ab8d
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 14%

---

# 登陆页面入门 {#get-started-lp}

登陆页面是指用户在从电子邮件、网站、广告或任何其他数字位置点进后被定向到的独立网页。

[!DNL Journey Optimizer]允许您创建和设计登陆页面，以将您的用户定向到在线表单，他们可以在其中选择加入或选择退出接收您的通信或特定服务（如新闻稿）。

➡️ [在此视频中了解有关配置订阅和创建登陆页面的更多信息](#video)

## 何时使用登陆页面 {#when-to-use}

当您想要执行以下操作时使用登陆页面：

* 允许客户&#x200B;**从电子邮件或促销活动中的链接**&#x200B;选择加入或选择退出营销通信或特定服务或新闻稿，包括目标服务的订阅列表。 [了解详情](lp-use-cases.md#subscription-to-a-service)
* 在发送通信前&#x200B;**收集同意**，并在选择加入或选择退出时发送&#x200B;**确认电子邮件**。 [了解详情](lp-use-cases.md#send-confirmation-email)
* **使用**&#x200B;数据捕获&#x200B;**[!UICONTROL 登陆页面上的表单捕获或更新配置文件数据]**，用于渐进式分析、首选项、注册和类似方案。 [了解详情](#data-capture-lp)
* 将用户重定向到&#x200B;**专用Web窗体**，而无需在[!DNL Journey Optimizer]外部构建外部页面
* 使用&#x200B;**的内容设计功能构建**&#x200B;响应式登陆页面[!DNL Journey Optimizer]

### 使用登陆页面捕获数据 {#data-capture-lp}

**[!UICONTROL 数据捕获]**&#x200B;登陆页面允许您嵌入已发布的表单，以便访客能够通过表单预设中配置的流连接提交写入到[!DNL Adobe Experience Platform]数据集的属性。 [了解如何在登陆页面中创建和嵌入表单](lp-forms.md)

>[!NOTE]
>
>**已知配置文件**（在[!DNL Adobe Experience Platform]中标识的现有配置文件）支持通过登陆页面表单捕获数据。 登陆页面应通过&#x200B;**个性化链接**（例如电子邮件促销活动）打开，以便在页面加载时解析用户档案身份。

以下是示例用例：

1. **渐进式配置文件扩充** — 通过个性化登录页面从已知客户那里收集其他属性（如电话号码、出生日期或位置），以扩充其现有[!DNL Experience Platform]配置文件以进行分段和个性化。

2. **首选项中心更新** — 允许已知订阅者通过登陆页面管理其通信首选项（渠道、主题兴趣），更改通常在大约15分钟内反映在其[!DNL Experience Platform]配置文件中。

3. **事件或网络研讨会注册** — 从注册页面上的已知配置文件中捕获特定于事件的数据，使用注册属性更新配置文件并触发确认历程。

4. **忠诚度或计划注册** — 通过登陆页面提交其他详细信息，丰富下游定位的配置文件，允许现有客户注册忠诚度计划或会员等级。

5. **竞赛或竞赛项目** — 让已知客户通过登陆页面表单参加竞赛或抽奖；捕获项目特定的详细信息（答案、偏好设置或声明）并将它们写入配置文件以支持资格、入选者选择和后续历程。

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
<a href="lp-forms.md">
<img alt="Journey Optimizer中登录页面的Forms列表" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>在登陆页面中使用表单</strong></a>
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

1. **配置子域** — 设置专用于托管登陆页面的子域。 [了解详情](lp-subdomains.md)
1. **创建登陆页面预设** — 预设定义了应用于登陆页面的子域和其他设置。 [了解详情](lp-presets.md#lp-create-preset)
1. **创建订阅列表**（对于订阅用例） — 如果您希望客户订阅或取消订阅特定服务，则此为必需字段。 [了解详情](subscription-list.md)
1. **创建表单**（用于数据捕获用例） — 当您想要在&#x200B;**[!UICONTROL 数据捕获]**&#x200B;登陆页面上嵌入表单并将提交内容发送到[!DNL Experience Platform]时需要。 [了解详情](lp-forms.md)

## 工作原理 {#how-it-works}

创建和部署登陆页面应遵循以下顺序：

1. **创建和配置登陆页面** — 选择预设，设置主页面，然后添加任何所需的子页面。 [了解详情](create-lp.md#create-landing-page)
1. **设计页面** — 使用[!DNL Journey Optimizer]的拖放编辑器生成页面内容和表单。 [了解详情](design-lp.md)
1. **测试和发布登陆页面** — 预览页面，测试表单行为，然后发布以使其上线。 [了解详情](create-lp.md#test-landing-page)
1. **消息或历程中的链接** — 将登陆页面URL添加到电子邮件、营销活动或历程操作，以便客户可以访问该页面。 [了解详情](../email/message-tracking.md#insert-links)

## 操作方法视频{#video}

以下视频介绍如何创建订阅列表、设置登陆页面以选择加入或选择退出服务、将选择加入/选择退出选项集成到消息并配置相关历程。

>[!VIDEO](https://video.tv.adobe.com/v/344396?captions=chi_hans&quality=12&learn=on)
