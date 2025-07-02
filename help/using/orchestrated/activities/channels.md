---
solution: Journey Optimizer
product: journey optimizer
title: 在多步营销活动中添加渠道活动
description: 了解如何在多步营销活动中添加渠道活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: cfb09467809a69516c34d52be3f41e7a1abdb7c3
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 17%

---

# 渠道活动 {#channel}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](../gs-campaign-creation.md) | [创建编排的营销活动](../create-orchestrated-campaign.md)<br/><br/>[编排活动](../orchestrate-activities.md)<br/><br/><br/>[启动并监视营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用查询Modeler](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[并加入](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - **[渠道活动](channels.md)** - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[!DNL Adobe Journey Optimizer]允许您跨渠道自动执行营销活动。 您可以将渠道活动合并到编排的活动画布中，以创建跨渠道编排的活动，从而根据客户行为和数据触发操作。

例如，您可以创建一个欢迎电子邮件活动，其中包含跨不同渠道（例如电子邮件、短信或推送消息）的一系列消息。您还可以在客户完成购买后发送跟进电子邮件，或者通过短信向客户发送个性化的生日消息。

通过使用渠道活动，您可以创建全面的个性化营销活动，在多个接触点吸引客户并促进转化。 支持的渠道包括电子邮件、短信和推送。

## 先决条件 {#channel-activity-prereq}

开始使用相关活动构建编排的营销活动：

* 在插入渠道活动之前，必须定义受众。 受众是投放的主要目标：接收消息的用户档案。 [了解如何使用生成受众活动](build-audience.md)

* 要发送定期投放，请使用&#x200B;**[!UICONTROL 调度程序]**&#x200B;活动启动编排的营销活动。 您还可以对一次性投放使用&#x200B;**[!UICONTROL 调度程序]**&#x200B;活动来设置该投放的联系日期。 还可以在投放设置中设置该联系日期。 [学习如何计划编排的营销活动](../create-orchestrated-campaign.md#schedule)

## 配置渠道活动 {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="电子邮件活动"
>abstract="通过电子邮件活动，您可以在编排的活动中发送一次性消息和定期消息的电子邮件。 它有助于自动执行向在同一编排的营销活动中算出的目标发送电子邮件的过程。 您可以将渠道活动合并到多步骤营销活动画布中，创建可根据客户行为和数据触发操作的跨渠道营销活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="短信活动"
>abstract="利用短信活动，您可以在编排的活动中发送一次性消息和定期消息的短信。 它有助于自动执行向在同一编排的营销活动中算出的目标发送短信的过程。 您可以将渠道活动合并到多步骤营销活动画布中，创建可根据客户行为和数据触发操作的跨渠道营销活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="推送活动"
>abstract="推送活动可让您在编排的活动中发送推送通知。 它允许同时交付一次性活动和定期编排的活动，在同一编排的活动中，自动向预定义目标发送推送通知。 您可以将渠道活动合并到活动画布中，以创建跨渠道活动，从而根据客户行为和数据触发操作。"

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity let you send iOS Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring orchestrated campaigns, automating the sending iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity ket you send Android Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending Android Push notifications to a predefined target within the same orchestrated campaign. You can combine channel activities into the orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="直邮活动"
>abstract="直邮活动有助于在编排的活动中发送一次性消息和定期消息的直邮。 它可用于自动生成直邮提供商所需的提取文件。您可以将渠道活动合并到编排的活动画布中，以创建跨渠道活动，从而根据客户行为和数据触发操作。"

要在编排的活动上下文中设置投放，请执行以下步骤。

### 添加渠道活动并定义其属性 {#add}

1. 将渠道活动添加到画布中。 可用的渠道活动包括&#x200B;**[!UICONTROL 电子邮件]**、**[!UICONTROL 短信]**&#x200B;和&#x200B;**[!UICONTROL 推送]**。

   ![显示具有可用活动的画布的图像](../assets/channel-add.png)

1. 选择添加的活动，然后单击&#x200B;**[!UICONTROL 编辑电子邮件]**、**[!UICONTROL 编辑短信]**&#x200B;或&#x200B;**[!UICONTROL 编辑推送]**&#x200B;按钮（具体取决于所选的渠道）。

   ![显示带有电子邮件活动的画布的图像](../assets/channel-edit.png)

1. 在&#x200B;**[!UICONTROL 属性]**&#x200B;选项卡中，输入营销活动的描述。

### 设置渠道配置和设置 {#configuration}

1. 选择&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡，然后选择要用于消息的通道配置。

   配置由[系统管理员](../../start/path/administrator.md)定义。 它包含用于发送消息的所有技术参数，如标头参数、子域、移动应用程序等。[了解如何设置渠道配置](../../configuration/channel-surfaces.md)。

1. 对于电子邮件和短信，使用跟踪选项来监控收件人对电子邮件或短信投放的反应。

   执行营销活动后，即可从营销活动报表访问跟踪结果。 [了解有关营销活动报告的更多信息](../../reports/campaign-global-report-cja.md)

1. 对于推送通知，请使用&#x200B;**[!UICONTROL 快速传递模式]**&#x200B;选项在推送渠道上向3000万以下的受众规模进行高速消息发送。

   快速传递模式是一个&#x200B;**[!DNL Journey Optimizer]**&#x200B;加载项，它允许大容量快速发送推送消息。 [了解详情](../../push/create-push.md#rapid-delivery)

1. **[!UICONTROL 内容试验]**&#x200B;部分允许您定义多个投放处理，以测量哪个处理对您的目标受众表现最佳。

   为此，请单击&#x200B;**[!UICONTROL 创建试验]**&#x200B;按钮，然后执行本节中详述的步骤： [创建内容试验试验功能](../../content-management/content-experiment.md)。

1. **[!UICONTROL 语言]**&#x200B;部分允许您在营销策划中创建多种语言的内容。

   为此，请单击&#x200B;**[!UICONTROL 添加语言]**&#x200B;按钮，然后选择所需的&#x200B;**[!UICONTROL 语言设置]**。 有关如何设置和使用多语言功能的详细信息，请参阅此部分： [开始使用多语言内容](../../content-management/multilingual-gs.md)

### 定义内容 {#content}

选择&#x200B;**[!UICONTROL Content]**&#x200B;选项卡以定义消息的内容。 内容创建过程取决于所选的渠道。

在以下页面中了解创建消息内容的详细步骤：

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../../email/create-email.md"><img alt="电子邮件" src="../../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../../email/create-email.md"><strong>电子邮件</strong></a></div></td>
<td><a href="../../sms/create-sms.md"><img alt="短信" src="../../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../../sms/create-sms.md"><strong>短信</strong></a></div></td>
<td><a href="../../push/create-push.md"><img alt="推送" src="../../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../../push/create-push.md"><strong>推送通知</strong></a></div></td>
</tr></table>

定义内容后，使用&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮，使用从CSV/JSON文件上传或手动添加的测试配置文件或示例输入数据预览和测试内容。 [了解详情](../../content-management/preview-test.md)

## 后续步骤 {#next}

使用&#x200B;**[!UICONTROL 返回]**&#x200B;箭头返回您的编排的营销活动。

显示“返回”按钮的![图像](../assets/channel-back.png)

您现在可以在画布中完成活动编排，并发布活动以开始发送消息。 [了解如何启动和监控编排的营销活动](../start-monitor-campaigns.md)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel orchestrated campaign example with a segmentation and two deliveries. The orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
