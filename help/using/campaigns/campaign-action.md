---
solution: Journey Optimizer
product: journey optimizer
title: 配置营销活动操作
description: 了解如何配置营销活动操作。
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 创建，优化器，营销活动，界面，消息
exl-id: fed96e48-2e54-4bd4-ae17-77434d1b90eb
source-git-commit: 378ead41924496f52f22026b3f0e05a9c9c76f89
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 34%

---

# 配置营销活动操作 {#action-campaign-action}

使用&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡为您的消息选择渠道配置并配置其他设置，如跟踪、内容试验或多语言内容。

1. **选择频道**

   导航到&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡，单击&#x200B;**[!UICONTROL 添加操作]**&#x200B;按钮并选择通信渠道。

   ![](assets/create-campaign-add-action.png)

   >[!NOTE]
   >
   >可用渠道因您的许可模式和插件而异。

   如果选择入站渠道（基于代码的体验、应用程序内消息、内容卡或Web操作），则可以添加更多入站操作，在单个营销活动中总计最多10个操作。 [了解如何操作](#multi-action)

1. **选择渠道配置**

   配置由[系统管理员](../start/path/administrator.md)定义。它包含用于发送消息的所有技术参数，如标头参数、子域、移动应用程序等。[了解如何设置渠道配置](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **利用优化**

   使用&#x200B;**[!UICONTROL 消息优化]**&#x200B;部分运行内容实验、利用定位规则，或使用实验和定位的高级组合。 本节详细介绍了这些不同的选项以及要遵循的步骤：[促销活动中的优化](campaigns-message-optimization.md)。
<!--
1. **Create a content experiment**

    Use the **[!UICONTROL Content experiment]** section to define multiple delivery treatments in order to measure which one performs best for your target audience. Click the **[!UICONTROL Create experiment]** button then follow the steps detailed in this section: [Create a content experiment](../content-management/content-experiment.md).-->

1. **添加多语言内容**

   使用&#x200B;**[!UICONTROL 语言]**&#x200B;部分，在营销活动中创建多种语言内容。要进行此操作，请单击&#x200B;**[!UICONTROL 添加语言]**&#x200B;按钮，然后选择所需的&#x200B;**[!UICONTROL 语言设置]**。有关如何设置和使用多语言功能的详细信息，请参阅此部分： [开始使用多语言内容](../content-management/multilingual-gs.md)。

根据所选通信渠道，可以使用其他设置。 展开以下部分以获取更多信息。

+++**应用上限规则**（电子邮件、直邮、推送、短信）

在&#x200B;**[!UICONTROL 业务规则]**&#x200B;下拉列表中，选择一个规则集以将上限规则应用于营销活动。 利用渠道规则集，可设置按通信类型划分的频率封顶，以防止对具有类似消息的客户造成过载。 [了解如何使用规则集](../conflict-prioritization/rule-sets.md)

+++

+++**跟踪参与情况**（电子邮件、短信）。

使用&#x200B;**[!UICONTROL 操作跟踪]**&#x200B;部分，跟踪收件人对电子邮件或短信投放的反应。执行营销活动后，即可从营销活动报告获取跟踪结果。[了解关于营销活动报告的更多信息](../reports/campaign-global-report-cja.md)

+++

+++**启用快速传递模式** （推送）。

快速投放模式是一个 [!DNL Journey Optimizer] 附加组件，允许通过营销活动以非常快的速度发送大量推送消息。如果消息投放延迟对业务有重大影响，并且您想要在手机上发送紧急推送警报（例如，向已安装新闻频道应用程序的用户发送突发新闻），可使用快速投放。有关使用快速投放模式时的性能的详细信息，请参阅 [Adobe Journey Optimizer 产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html)。

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

## 添加多个入站操作 {#multi-action}

>[!CONTEXTUALHELP]
>id="ajo_multi_action"
>title="添加多个入站操作"
>abstract="您可以在单个营销活动中选择多个入站操作。此功能使您能够同时向不同地点传递多个基于代码的体验、应用程序内消息、内容卡或 Web 操作，每个操作包含一个特定的内容。"

为简化活动编排，您可以在单个活动内定义多个集客操作，每个操作都包含特定内容。

>[!NOTE]
>
>此容量仅适用于入站渠道。 不支持当前出站渠道，如电子邮件。

利用此功能，您可以向不同位置同时提供各种基于代码的体验、应用程序内消息、内容卡或Web操作，而无需创建多个营销活动。 它使营销活动的部署更轻松，并允许更流畅的报表，将所有数据整合到一个营销活动中。

例如，您可以将基于代码的体验发送到内容略有不同的多个端点。 为此，请在同一营销策划中创建多个基于代码的操作，每个操作具有不同的端点配置。

要在营销策划中定义多个集客操作，请执行以下步骤。

1. 从&#x200B;**操作**&#x200B;部分中选择入站操作（**基于代码的体验**、**应用程序内消息**、**内容卡**&#x200B;或&#x200B;**[!UICONTROL Web]**）。

1. 选择渠道配置并定义该操作的特定内容。

1. 使用&#x200B;**[!UICONTROL 添加操作]**&#x200B;按钮从下拉列表中选择其他入站操作。

   ![](assets/create-campaign-multi-action.png){width="80%"}

1. 继续以类似方式添加更多操作。 在一个营销活动中最多可添加10个集客操作。

营销活动处于[实时](review-activate-campaign.md)状态后，将同时激活所有操作。

## 后续步骤 {#next}

活动操作就绪后，即可设计其内容。 [了解详情](campaign-content.md)
