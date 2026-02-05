---
solution: Journey Optimizer
product: journey optimizer
title: 使用操作历程活动
description: 了解如何添加通用操作活动，以在历程画布中配置单个操作和多操作入站操作组。
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: 历程，消息，推送，短信，电子邮件，应用程序内， Web，内容卡，基于代码的体验
exl-id: 0ed97ffa-8efc-45a2-99ae-7bcb872148d5
version: Journey Orchestration
source-git-commit: bf5d018fa6c3e88cf84345e892de72ada9f2c489
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 15%

---

# 使用操作活动 {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_action_activity"
>title="操作活动"
>abstract="一般&#x200B;**操作**&#x200B;活动允许您配置一个原生渠道操作和多个入站活动，您还可以添加对任何内置渠道操作的优化。"

>[!AVAILABILITY]
>
>此功能为限量发布版。请联系 Adobe 代表获取访问权限。

[!DNL Journey Optimizer]附带了一个新的通用&#x200B;**操作**&#x200B;活动，该活动允许配置单个内置渠道操作以及多个入站活动。

它允许：

* 简化历程画布中的原生操作配置。
* 创建多操作入站操作组的功能。
* 将优化设置添加到任何内置渠道操作。

>[!NOTE]
>
>您还可以设置自定义操作以在[!DNL Journey Optimizer]中发送消息。 [了解详情](#recommendation)

## 向历程添加操作  {#add-action}

要将内置渠道操作添加到历程，请执行以下步骤。

1. 通过[事件](general-events.md)或[读取受众](read-audience.md)活动开始您的历程。

1. 从调色板的&#x200B;**[!UICONTROL 操作]**&#x200B;部分，将&#x200B;**[!UICONTROL 操作]**&#x200B;活动拖放到画布中。

1. 选择要在历程中利用的内置渠道活动。

   ![显示渠道操作和自定义操作选项的操作类型下拉列表](assets/journey-action-type-cbe.png)

1. 向操作添加标签并选择&#x200B;**[!UICONTROL 配置操作]**。

   ![带有标签和描述字段的操作活动配置窗格](assets/journey-action-configure.png){width="80%"}

1. 您将被定向到历程操作配置屏幕的&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡。

   选择要用于所选渠道的配置。

   “管理”菜单中的![操作选项卡显示自定义和Adobe操作](assets/journey-action-actions-tab.png)

1. 如果您选择了入站渠道，则可以添加多个操作。 [了解详情](#multi-action)

1. 根据选定的渠道配置活动。 在[本节](journeys-message.md)中了解如何配置内置渠道操作。

1. 使用&#x200B;**[!UICONTROL 优化]**&#x200B;部分运行内容实验、利用定位规则，或使用实验和定位的高级组合。

   [此部分](../content-management/gs-message-optimization.md)中详细说明了这些不同的选项以及要遵循的步骤。

1. 使用&#x200B;**[!UICONTROL 语言]**&#x200B;部分在历程操作中创建多种语言的内容。 为此，请单击&#x200B;**[!UICONTROL 添加语言]**&#x200B;按钮，然后选择所需的&#x200B;**[!UICONTROL 语言设置]**。

   有关如何设置和使用多语言功能的详细信息，请参阅[此部分](../content-management/multilingual-gs.md)。

根据所选通信渠道，可以使用其他设置。 展开以下部分以获取更多信息。

+++**应用上限规则**（电子邮件、推送、短信）

在&#x200B;**[!UICONTROL 业务规则]**&#x200B;下拉列表中，选择一个规则集以将上限规则应用于历程操作。

利用渠道规则集，可设置按通信类型划分的频率封顶，以防止消息类似的客户超载。

[了解如何使用规则集](../conflict-prioritization/rule-sets.md)

+++

+++**跟踪参与情况**（电子邮件、短信）。

使用&#x200B;**[!UICONTROL 操作跟踪]**&#x200B;部分跟踪收件人对电子邮件或短信投放的反应。

一旦执行历程，即可从历程报表访问跟踪结果。

[了解有关历程报告的更多信息](../reports/journey-global-report-cja.md)

+++

+++**启用快速传递模式** （推送）。

快速传递模式是一个[!DNL Journey Optimizer]加载项，允许通过营销活动以非常快的速度发送大量推送消息。

当消息投放延迟对业务至关重要，并且您想要在手机上发送紧急推送警报（例如，向已安装您的新闻频道应用程序的用户发送突发新闻）时，可使用快速投放。

了解如何在此页面[上为推送通知](../push/create-push.md#rapid-delivery)启用快速传递模式。

有关使用快速投放模式时的性能的详细信息，请参阅 [Adobe Journey Optimizer 产品说明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}。

+++

+++**分配优先级得分**（Web、应用程序内、基于代码）

在&#x200B;**[!UICONTROL 冲突管理]**&#x200B;部分中，您可以为历程操作分配优先级得分，这样您便可以在存在多个历程操作或使用相同渠道配置的营销活动时为集客操作设置优先级。

在默认情况下，操作的优先级分数从历程的总体优先级分数继承。

[了解如何为渠道操作分配优先级得分](../conflict-prioritization/priority-scores.md#priority-action)

+++

+++**设置其他投放规则**（内容卡片）

对于内容卡历程，您可以启用其他投放规则以选择触发消息的事件和条件。

[了解如何创建内容卡片](../content-card/create-content-card.md)

+++

+++**定义触发器**（应用程序内）

对于应用程序内消息，您可以使用&#x200B;**[!UICONTROL 编辑触发器]**&#x200B;按钮选择触发消息的事件和条件。

[了解如何创建应用程序内消息](../in-app/create-in-app.md)

+++

## 添加多个入站操作 {#multi-action}

>[!CONTEXTUALHELP]
>id="ajo_multi_action_journey"
>title="添加多个入站操作"
>abstract="您可以在一个历程中选择多个入站操作。此功能使您能够同时向不同地点传递多个基于代码的体验、应用程序内消息、内容卡或 Web 操作，每个操作包含一个特定的内容。"

为了简化旅程编排，您可以在单个旅程操作中定义多个入站操作。

>[!NOTE]
>
>此容量仅适用于入站渠道。 不支持当前出站渠道，如电子邮件。

利用此功能，您可以向不同位置同时交付各种基于代码的体验、应用程序内消息、内容卡或Web操作，而无需创建多个历程操作。 它将所有数据整合到一个历程中，使历程的部署更轻松，并允许更流畅的报告。

例如，您可以将基于代码的体验发送到内容略有不同的多个端点。 为此，请在同一历程操作中创建多个基于代码的操作，每个操作具有不同的端点配置。

要在单个历程操作节点中定义多个入站操作，请执行以下步骤。

1. 通过[事件](general-events.md)或[读取受众](read-audience.md)活动开始您的历程。

1. 从调色板的&#x200B;**[!UICONTROL 操作]**&#x200B;部分，将&#x200B;**[!UICONTROL 操作]**&#x200B;活动拖放到画布中。

1. 选择&#x200B;**[!UICONTROL 多项操作]**&#x200B;作为操作类型。

   在编排下的历程调色板中![多操作活动](assets/journey-multi-action.png)

1. 根据需要添加标签并选择&#x200B;**[!UICONTROL 配置操作]**。

   ![带有标签和描述字段的多操作配置窗格](assets/journey-multi-action-configure.png){width="60%"}

1. 您将被定向到历程操作配置屏幕的&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡。

   ![显示要执行的操作列表的多操作配置](assets/journey-multi-action-configuration.png){width="70%"}

1. 从&#x200B;**操作**&#x200B;部分中选择入站操作（**基于代码的体验**、**应用程序内消息**、**内容卡**&#x200B;或&#x200B;**[!UICONTROL Web]**）。

1. 选择渠道配置并定义该操作的特定内容。

1. 使用&#x200B;**[!UICONTROL 添加操作]**&#x200B;按钮从下拉列表中选择其他入站操作。

   ![添加操作按钮，以在多操作活动中包含其他操作](assets/journey-multi-action-add.png){width="80%"}

1. 继续以类似方式添加更多操作。 可在历程操作组中添加最多10个集客操作。

历程处于[实时](publish-journey.md)状态后，将同时激活所有操作。
<!--
## Next steps {#next}

Once your action is configured, you can design its content. [Learn more]-->
