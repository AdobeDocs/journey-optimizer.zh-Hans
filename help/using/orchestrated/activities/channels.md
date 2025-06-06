---
solution: Journey Optimizer
product: journey optimizer
title: 在多步营销活动中添加渠道活动
description: 了解如何在多步营销活动中添加渠道活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 5872e192c849b7a7909f0b50caa1331b15490d79
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 44%

---

# 渠道活动 {#channel}

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库  | 编排的营销活动活动 |
|---|---|---|---|
| [开始使用编排的营销活动](../gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](../configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](../gs-campaign-creation.md) | [创建协调的营销活动](../create-orchestrated-campaign.md)<br/><br/>[协调活动](../orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](../send-messages.md)<br/><br/>[开始并监视营销活动](../start-monitor-campaigns.md)<br/><br/>[报告](../reporting-campaigns.md) | [使用查询Modeler](../orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](../build-query.md)<br/><br/>[编辑表达式](../edit-expressions.md) | [开始使用活动](about-activities.md)<br/><br/>活动：<br/>[And-join](and-join.md) - [生成受众](build-audience.md) - [更改维度](change-dimension.md) - [组合](combine.md) - [重复数据删除](deduplication.md) - [扩充](enrichment.md) - [分支](fork.md) - [协调](reconciliation.md) - [拆分](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

通过Adobe Journey Optimizer，您可以跨入站和出站渠道自动执行营销活动。 您可以将渠道活动合并到编排的活动画布中，以创建跨渠道编排的活动，从而根据客户行为和数据触发操作。 [此页面](../../channels/gs-channels.md)上列出了支持的渠道。

例如，您可以创建一个欢迎电子邮件促销活动，其中包含跨不同渠道的一系列消息，例如电子邮件、短信、推送和直邮。 您还可以在客户完成购买后发送跟进电子邮件，或者通过短信向客户发送个性化的生日消息。

通过使用渠道活动，您可以创建全面、个性化的营销活动，通过多个接触点吸引客户并推动转化。

## 先决条件 {#channel-activity-prereq}

开始使用相关活动构建编排的营销活动：

* 在插入渠道活动之前，必须定义受众。 受众是投放的主要目标：接收消息的用户档案。

* 要发送定期投放，请使用&#x200B;**调度程序**&#x200B;活动启动编排的营销活动。 您还可以对一次性投放使用&#x200B;**调度程序**&#x200B;活动来设置该投放的联系日期。 还可以在投放设置中设置该联系日期。

## 配置渠道活动 {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="电子邮件活动"
>abstract="电子邮件活动让您可以在多步骤营销活动中发送电子邮件，并允许一次性和重复发送消息。它可用于自动将电子邮件发送到在同一多步骤营销活动中计算的目标。您可以将渠道活动合并到多步骤营销活动画布中，创建可根据客户行为和数据触发操作的跨渠道营销活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="短信活动"
>abstract="短信活动可让您在多步骤营销活动中发送短信，并允许一次性和重复发送消息。它可用于自动将短信发送到在同一多步骤营销活动中计算的目标。您可以将渠道活动合并到多步骤营销活动画布中，创建可根据客户行为和数据触发操作的跨渠道营销活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="推送 iOS 活动"
>abstract="推送 iOS 活动让您可以作为多步骤营销活动的一部分发送 iOS 推送通知。可一次性和重复投放多步骤营销活动，自动将 iOS 推送通知发送到同一工作流程中的预定义目标。可将渠道活动合并到工作流画布中，以创建可根据客户行为和数据触发操作的跨渠道工作流。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="推送 Android 活动"
>abstract="推送 Android 活动让您可以作为多步骤营销活动的一部分发送 Android 推送通知。可一次性和重复投放，自动将 Android 推送通知发送到同一多步骤营销活动中的预定义目标。您可以将渠道活动合并到多步骤营销活动画布中，创建可根据客户行为和数据触发操作的跨渠道营销活动。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="直邮活动"
>abstract="直邮活动有助于在多步骤营销活动中直接发送邮件，并允许一次性和重复发送消息。它可用于自动生成直邮提供商所需的提取文件。您可以将渠道活动合并到多步骤营销活动画布中，创建可根据客户行为和数据触发操作的跨渠道营销活动。"

要在编排的活动上下文中设置投放，请执行以下步骤：

1. 添加渠道活动：**[!UICONTROL 电子邮件]**、**[!UICONTROL 短信]**、**[!UICONTROL 推送通知(Android)]**、**[!UICONTROL 推送通知(iOS)]**&#x200B;或&#x200B;**[!UICONTROL 直邮]**。

1. 选择&#x200B;**投放类型**：单次或循环。

   * **单次投放**&#x200B;是一次性投放，只发送一次，例如，黑色星期五的电子邮件。
   * **循环投放**&#x200B;根据其执行频率被多次发送。 每次运行编排的活动时，都会重新计算受众，并将投放内容发送到更新的受众，其中包含更新的内容。 例如，这可以是每周新闻稿或定期生日电子邮件。

1. 选择投放&#x200B;**模板**。模板是专用于渠道的预配置的投放设置。每个渠道都有一个内置模板，默认情况下会预填充。

   ![](../assets/delivery-activity-in-wf.png)

   您可以从渠道活动配置左窗格中选择模板。 如果之前选择的受众与渠道不兼容，则您无法选择模板。要解决此问题，请更新&#x200B;**构建受众**&#x200B;活动以选择具有正确目标映射的受众。

1. 单击&#x200B;**创建投放**。然后，您可以使用与创建独立投放相同的方式定义消息设置和内容。 您还可以测试和模拟内容。

1. 导航回工作流。 如果要继续工作流，请切换&#x200B;**生成叫客过渡**&#x200B;选项以在渠道活动后添加过渡。

1. 单击&#x200B;**开始**&#x200B;以启动编排的营销活动。

   默认情况下，启动编排的活动会触发消息准备阶段，而不会立即发送消息。

1. 打开您的渠道活动，通过&#x200B;**查看和发送**&#x200B;按钮确认发送。

1. 在投放仪表板中，单击&#x200B;**发送**。

## 示例 {#cross-channel-workflow-sample}

这是一个跨渠道编排的活动示例，其中包含一个分段和两个投放。 这项精心策划的活动针对所有居住在巴黎并对咖啡机感兴趣的客户。 在这些人群中，会向普通客户发送一封电子邮件，而向 VIP 客户发送一条短信。

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

您还可以创建一个循环的编排活动，在下午8点向所有居住在巴黎的客户发送个性化的短信。

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
