---
title: 应用程序内消息传送入门
description: 了解如何使用 Journey Optimizer 发送应用程序内通知
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内、消息、创建、入门
exl-id: 51562843-7b50-4eb5-bf79-5ce03f7549cb
TQID: https://experienceleague.adobe.com/b139LQsPe3HwKe1O5cyBx4Nj4jpW3GXCFIVIWTAIlbg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: cc5c44e2-54a1-4927-b794-442cd87d8f74id: c96d2aa5-76a2-443d-8d23-5de95577c909id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 601
ht-degree: 43%

---

# 应用程序内渠道入门 {#gs-in-app}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;开始使用 Adobe Journey Optimizer 中的应用程序内消息渠道，通过推送促进功能、优惠和入门引导的通知来吸引应用程序用户参与互动。

>[!ENDSHADEBOX]

应用程序内消息是可发送给应用程序内用户的通知，可将其引导至特定的目标点。 这些通知可用于不同的用途，例如推广新功能、提供特殊产品建议或帮助用户入门。 利用应用程序内消息，您可以有效地与受众互动，并引导受众注意应用程序的重要方面。

使用 Journey Optimizer 创建应用程序内通知，并配置体验选项，包括消息布局和显示、文本和按钮选项。

</br>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="inapp-configuration.md">
<img alt="验证" src="../assets/do-not-localize/inapp-config.jpg">
</a>
<div>
<a href="inapp-configuration.md"><strong>配置应用程序内渠道</strong></a>
</div>
<p>
</td>
<td>
<a href="create-in-app.md">
<img alt="潜在客户" src="../assets/do-not-localize/inapp-create.jpeg">
</a>
<div><a href="create-in-app.md"><strong>创建应用程序内消息</strong>
</div>
<p>
</td>
<td>
<a href="design-in-app.md">
<img alt="不频繁" src="../assets/do-not-localize/inapp-design.jpg">
</a>
<div>
<a href="design-in-app.md"><strong>设计应用程序内内容</strong></a>
</div>
<p></td>
<td>
<a href="../reports/campaign-global-report-cja-inapp.md">
<img alt="验证" src="../assets/do-not-localize/inapp-report.jpg">
</a>
<div>
<a href="../reports/campaign-global-report-cja-inapp.md"><strong>访问应用程序内报告</strong></a>
</div>
<p>
</td>
</tr></table>

## 用例

当您希望在用户已参与您的应用程序并充分利用即时关注机会时，应用程序内消息可以发挥最佳效果。

| 好处 | 原因 | 示例用例 |
| --- | --- | --- |
| 高用户参与度 | 在用户处于应用程序会话活动状态时访问用户 | 功能公告、入门提示 |
| 上下文相关触发器 | 可根据应用程序内行为或位置触发 | 在用户访问相关屏幕后立即突出显示功能 |
| 实时投放 | 不依赖于推送令牌或外部投放服务 | 当前会话期间显示的时间敏感提示 |
| 不依赖于外部渠道 | 完全在应用程序中工作，与其他渠道的选择加入状态无关 | 联系选择退出推送通知的用户 |
| 更好的转化潜力 | 在积极关注的时刻提供，提高响应率 | 追加销售或交叉销售优惠，调查提示 |
| 自定义和分段 | 布局、文本和按钮可以根据特定受众进行定制 | 不同用户区段的个性化载入流程 |
| 非侵入式设计 | 可以设计为补充而不是中断用户体验 | 与应用程序UI一致的横幅或模式 |

## 何时不使用

应用程序内消息取决于活动会话，因此它们并非适用于所有场景。 在以下情况下考虑其他渠道：

* 用户未主动使用应用程序，因为消息永远不会显示
* 消息是一个严重或时间敏感问题，需要联系应用程序外的用户，例如中断或安全警报
* 通信是合规的或合法的，需要应用程序内消息无法提供的读取确认
* 目标是为不太可能打开应用程序的非活动用户重新激活帐户或开展回馈活动
* 该消息是大容量事务型更新，如订单确认，更适合通过电子邮件或短信发送
* 过度使用可能导致横幅失明，即用户开始忽略显示过于频繁的消息
* 当消息要传递时，用户可能处于脱机状态或没有应用程序连接



## 其他资源

* **[创建应用程序内消息](create-in-app.md)** - 了解如何为移动应用程序创建和配置应用程序内消息。
* **[配置应用程序内渠道](inapp-configuration.md)** – 使用正确的移动应用程序配置设置应用程序内消息渠道。
* **[设计应用程序内的内容](design-in-app.md)** - 自定义应用程序内消息布局、样式、按钮和交互元素。
* **[Web 的应用程序内消息](create-in-app-web.md)** - 了解如何为 Web 应用程序创建和传递应用程序内消息。
* **[应用程序内渠道教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/channels/in-app-channel/in-app-messages-overview){target="_blank"}** - 浏览有关应用程序内消息传送功能和最佳实践的分步视频教程。

