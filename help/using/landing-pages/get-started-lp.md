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
TQID: https://experienceleague.adobe.com/wr4XGNostKoN8jZ50VRAQPoGg9tsNhMOyJGEt1mASso
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: b19d9237-76be-466d-a869-aacf2d72205fid: fb9a80eb-bebc-492f-a0e9-584595621ebbid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2956c3df01f4b2e753111ecf54163ec4084fecf2
workflow-type: tm+mt
source-wordcount: 781
ht-degree: 94%

---

# 登陆页面入门 {#get-started-lp}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;登陆页面将电子邮件、广告或营销活动中的点击转变成一个专用的Web目标，客户可以在其中选择加入或退出、管理其偏好并共享配置文件数据，从而帮助您扩大公认的受众并捕获支持个性化的第一方数据。

>[!ENDSHADEBOX]

登陆页面是指用户在从电子邮件、网站、广告或任何其他数字位置点进后被定向到的独立网页。

[!DNL Journey Optimizer]允许您创建和设计登陆页面，以将用户定向到在线表单，在该表单中，用户可以选择启用或选择禁用接收通信，或订阅特定服务（如新闻稿）。

➡️ [在此视频中了解有关配置订阅和创建登陆页面的更多信息](#video)

## 何时使用登陆页面 {#when-to-use}

当您想要执行以下操作时使用登陆页面：

* 允许客户通过电子邮件或营销活动中的链接&#x200B;**选择加入或选择退出**&#x200B;营销通信或特定服务或新闻稿，包括目标服务的订阅列表。 [了解详情](lp-use-cases.md#subscription-to-a-service)
* 发送通信之前&#x200B;**收集同意**，并在选择启用或选择禁用时发送&#x200B;**确认电子邮件**。 [了解详情](lp-use-cases.md#send-confirmation-email)
* 使用&#x200B;**[!UICONTROL 数据捕获]**&#x200B;登陆页面上的表单&#x200B;**捕获或更新轮廓数据**，用于渐进式分析、偏好设置、注册和类似场景。 [了解详情](#data-capture-lp)
* 将用户重定向到&#x200B;**专用 Web 表单**，而无需生成除[!DNL Journey Optimizer]之外的外部页面
* 使用[!DNL Journey Optimizer]的内容设计功能生成&#x200B;**响应式登陆页面**

### 使用登陆页面捕获数据 {#data-capture-lp}

**[!UICONTROL 数据捕获]**&#x200B;登陆页面允许您嵌入已发布的表单，以便访客能够通过表单预设中配置的流连接提交写入到[!DNL Adobe Experience Platform]数据集的属性。 [了解如何在登陆页面中创建和嵌入表单](lp-forms.md)

>[!NOTE]
>
>**已知用户档案（[!DNL Adobe Experience Platform]中标识的现有用户档案）支持通过登陆页面表单捕获数据**。 登陆页面应通过&#x200B;**个性化链接**（例如电子邮件营销活动）打开，这样才能在页面加载时解析轮廓身份标识。

以下是示例用例：

1. **渐进式轮廓扩充** – 通过个性化登录页面从已知客户收集其他属性（如电话号码、出生日期或位置），以扩充其现有 [!DNL Experience Platform] 轮廓，用来进行细分和个性化处理。

2. **偏好设置中心更新** - 允许已知订阅者通过登陆页面管理其通信偏好设置（渠道、主题兴趣），更改通常在大约 15 分钟内显示在其[!DNL Experience Platform]用户档案中。

3. **事件或网络研讨会注册** - 从注册页面上的已知用户档案中捕获特定于事件的数据，使用注册属性更新用户档案并触发确认历程。

4. **忠诚度或计划注册** – 让现有客户通过登录页面提交额外详细信息来注册忠诚度计划或会员等级，从而扩充轮廓，以用于进行下游目标选择。

5. **竞赛或抽奖活动参与** - 让已知客户通过登陆页面表单参加竞赛或抽奖；捕获活动特定的详细信息（答案、偏好设置或声明）并将其写入用户档案以支持资格判定、获奖者选择和后续旅程。

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
<img alt="Journey Optimizer 中登录页面的表单列表" src="../assets/do-not-localize/lp-design.jpg">
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

创建登陆页面之前，请完成以下设置步骤：

1. **配置子域** - 设置专用于托管登陆页面的子域。 [了解详情](lp-subdomains.md)
1. **创建登陆页面预设** - 预设定义应用于登陆页面的子域和其他设置。 [了解详情](lp-presets.md#lp-create-preset)
1. **创建订阅列表**（对于订阅用例）- 如果希望客户订阅或取消订阅特定服务，则必需执行此操作。 [了解详情](subscription-list.md)
1. **创建表单**（用于数据捕获用例）- 如果要在&#x200B;**[!UICONTROL 数据捕获]**&#x200B;登陆页面上嵌入表单并将提交内容发送到[!DNL Experience Platform]，则必需执行此操作。 [了解详情](lp-forms.md)

## 工作原理 {#how-it-works}

创建和部署登陆页面应遵循以下顺序：

1. **创建和配置登陆页面** - 选择预设，设置主页面，然后添加任何所需子页面。 [了解详情](create-lp.md#create-landing-page)
1. **设计页面** - 使用[!DNL Journey Optimizer]的拖放编辑器生成页面内容和表单。 [了解详情](design-lp.md)
1. **测试和发布登陆页面** - 预览页面，测试表单行为，然后发布以使其上线。 [了解详情](create-lp.md#test-landing-page)
1. **在消息或历程中添加链接** - 将登陆页面 URL 添加到电子邮件、营销活动或历程操作，以便客户可以访问该页面。 [了解详情](../email/message-tracking.md#insert-links)

## 操作方法视频{#video}

以下视频演示如何创建订阅列表、设置选择订阅或选择退订某项服务的登陆页面、将选择订阅或选择退订选项集成到消息并配置相关历程。

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)

➡️ **实际应用示例：**&#x200B;探索[登陆页面用例](lp-use-cases.md)以了解有关订阅管理、确认电子邮件和数据捕获场景的分步示例。
