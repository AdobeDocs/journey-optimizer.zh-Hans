---
solution: Journey Optimizer
product: journey optimizer
title: 配置活动操作
description: 了解如何配置营销活动操作。
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 创建，优化器，营销活动，界面，消息
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 10%

---


# 配置活动操作 {#action-campaign-action}

使用&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡为您的消息选择渠道配置并配置其他设置，如跟踪、内容实验或多语言内容。

1. **选择频道**

   导航到&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡，单击&#x200B;**[!UICONTROL 添加操作]**&#x200B;按钮并选择通信渠道。

   ![](assets/create-campaign-add-action.png)

   >[!NOTE]
   >
   >可用渠道因您的许可模式和插件而异。

1. **选择渠道配置**

   配置由[系统管理员](../start/path/administrator.md)定义。 它包含用于发送消息的所有技术参数，如标头参数、子域、移动应用程序等。[了解如何设置渠道配置](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **创建内容试验**

   使用&#x200B;**[!UICONTROL 内容试验]**&#x200B;部分定义多种传递处理，以衡量哪种传递处理对目标受众的效果最佳。 单击&#x200B;**[!UICONTROL 创建试验]**&#x200B;按钮，然后按照本节中详述的步骤操作：[创建内容试验](../content-management/content-experiment.md)。

1. **添加多语言内容**

   使用&#x200B;**[!UICONTROL 语言]**&#x200B;部分在营销策划中创建多种语言的内容。 为此，请单击&#x200B;**[!UICONTROL 添加语言]**&#x200B;按钮，然后选择所需的&#x200B;**[!UICONTROL 语言设置]**。 有关如何设置和使用多语言功能的详细信息，请参阅此部分： [开始使用多语言内容](../content-management/multilingual-gs.md)

根据所选通信渠道，可以使用其他设置。 展开以下部分以获取更多信息。

+++**应用上限规则**（电子邮件、直邮、推送、短信）

在&#x200B;**[!UICONTROL 业务规则]**&#x200B;下拉列表中，选择一个规则集以将上限规则应用于营销活动。 利用渠道规则集，可设置按通信类型划分的频率封顶，以防止对具有类似消息的客户造成过载。 [了解如何使用规则集](../conflict-prioritization/rule-sets.md)

+++

+++**跟踪参与情况**（电子邮件、短信）。

使用&#x200B;**[!UICONTROL 操作跟踪]**&#x200B;部分跟踪收件人对电子邮件或短信投放的反应。 执行营销活动后，即可从营销活动报表访问跟踪结果。 [了解有关营销活动报告的更多信息](../reports/campaign-global-report-cja.md)

+++

+++**启用快速传递模式** （推送）。

快速传递模式是一个[!DNL Journey Optimizer]加载项，允许通过营销活动以非常快的速度发送大量推送消息。 当消息投放延迟对业务至关重要，并且您想要在手机上发送紧急推送警报（例如，向已安装您的新闻频道应用程序的用户发送突发新闻）时，可使用快速投放。 有关使用快速传递模式时性能的详细信息，请参阅[Adobe Journey Optimizer产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html)。

+++

+++**分配优先级得分**（Web、应用程序内、基于代码）

通过为营销活动分配优先级得分，您可以在存在强加的限制（如频率上限）时为入站营销活动设置优先级。 输入一个数值（从 0 到 100）。请注意，数值越高，优先级越高。[了解如何为历程和营销活动分配优先级分数](../conflict-prioritization/priority-scores.md)

+++

+++**设置其他投放规则**（内容卡片）

对于内容卡营销活动，您可以启用其他投放规则以选择触发消息的事件和标准。 [了解如何创建内容卡](../content-card/create-content-card.md)

+++

+++**定义触发器**（应用程序内）

对于应用程序内消息，您可以使用&#x200B;**[!UICONTROL 编辑触发器]**&#x200B;按钮选择触发消息的事件和条件。 [了解如何创建应用程序内消息](../in-app/create-in-app.md)

+++

## 后续步骤 {#next}

活动操作就绪后，即可设计其内容。 [了解详情](campaign-content.md)
