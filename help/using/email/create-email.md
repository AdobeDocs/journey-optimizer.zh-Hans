---
solution: Journey Optimizer
product: journey optimizer
title: 创建电子邮件
description: 了解如何在 Journey Optimizer 中创建电子邮件
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 创建，电子邮件，开始，历程，营销活动
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 9%

---

# 创建电子邮件 {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="电子邮件创建"
>abstract="只需三个简单的步骤即可定义您的电子邮件参数。"

在中创建电子邮件 [!DNL Journey Optimizer]，请执行以下步骤。

## 在历程或营销策划中创建电子邮件 {#create-email-journey-campaign}

添加 **[!UICONTROL 电子邮件]** 操作到历程或营销策划，并根据您的案例执行以下步骤。

>[!BEGINTABS]

>[!TAB 向历程添加电子邮件]

1. 打开您的历程，然后拖放 **[!UICONTROL 电子邮件]** 活动 **[!UICONTROL 操作]** 的子菜单。

1. 提供有关消息的基本信息（标签、描述、类别）。

1. 选择 [电子邮件界面](email-settings.md) 。

   ![](assets/email_journey.png)

>[!NOTE]
>
>如果您从历程发送电子邮件，则可以利用Adobe Journey Optimizer的发送时间优化功能，根据历史打开率和点击率预测发送消息的最佳时间，以最大限度地提高参与度。 [了解如何使用发送时间优化](../building-journeys/journeys-message.md#send-time-optimization)

有关如何配置旅程的更多信息，请参阅 [本页](../building-journeys/journey-gs.md).

>[!TAB 向营销活动添加电子邮件]

1. 创建新的计划营销活动或API触发的营销活动，然后选择 **[!UICONTROL 电子邮件]** 作为您的操作。

1. 选择 [电子邮件界面](email-settings.md) 。

   ![](assets/email_campaign.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 完成创建电子邮件促销活动的步骤，如促销活动属性、 [受众](../segment/about-segments.md)和 [计划](../campaigns/create-campaign.md#schedule).

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

有关如何配置营销活动的详细信息，请参阅 [本页](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## 定义电子邮件内容 {#define-email-content}

<!-- update the quarry component with right ID value-->

>[!CONTEXTUALHELP]
>id="test_id"
>title="配置电子邮件内容"
>abstract="创建电子邮件的内容。定义其主题，然后利用电子邮件设计器构建和个性化电子邮件正文。"

1. 在历程或营销活动配置屏幕中，单击 **[!UICONTROL 编辑内容]** 按钮以配置电子邮件内容。 [了解详情](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. 在 **[!UICONTROL 标题]** 部分 **[!UICONTROL 编辑内容]** 屏幕， **[!UICONTROL 从名称]**, **[!UICONTROL 从电子邮件]** 和 **[!UICONTROL 密送]** 字段来自您选择的电子邮件界面。 [了解详情](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. 您可以添加主题行。 直接在相应的字段中键入纯文本，或使用 [表达式编辑器](../personalization/personalization-build-expressions.md) 个性化主题行。

1. 单击 **[!UICONTROL 编辑电子邮件正文]** 按钮以开始使用 [!DNL Journey Optimizer] Email Designer。 [了解详情](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. 如果您在营销活动中，也可以单击 **[!UICONTROL 代码编辑器]** 按钮，以使用显示的弹出窗口以纯HTML方式编码您自己的内容。

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >如果您已通过Email Designer创建或导入内容，则此内容将以HTML显示。

## 检查警报 {#check-email-alerts}

设计消息时，如果缺少键设置，则界面（位于屏幕右上方）中会显示警报。

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>如果看不到此按钮，则未检测到任何警报。

系统检查的设置和元素如下所示。 您还将找到有关如何调整配置以解决相应问题的信息。

可以发生两种类型的警报：

* **警告** 请参阅建议和最佳实践，例如：

   * **[!UICONTROL 电子邮件正文中不存在选择退出链接]**:最佳做法是向电子邮件正文中添加退订链接。 了解如何在 [此部分](../privacy/opt-out.md#opt-out-management).

      >[!NOTE]
      >
      >营销类型电子邮件必须包含选择退出链接，这对于事务型邮件不是必需的。消息类别(**[!UICONTROL 营销]** 或 **[!UICONTROL 事务型]**) [通道表面](email-settings.md#email-type) 级别和时间 [创建消息](#create-email-journey-campaign) 从历程或营销策划。

   * **[!UICONTROL HTML的文本版本为空]**:请不要忘记定义电子邮件正文的文本版本，因为当HTML内容无法显示时，会使用该文本版本。 了解如何在中创建文本版本 [此部分](text-version-email.md).

   * **[!UICONTROL 电子邮件正文中存在空链接]**:检查电子邮件中的所有链接是否正确。 了解如何在 [此部分](content-from-scratch.md).

   * **[!UICONTROL 电子邮件大小已超过100KB的限制]**:为获得最佳投放，请确保电子邮件的大小不超过100KB。 了解如何在 [此部分](content-from-scratch.md).

* **错误** 阻止您测试或激活历程/营销活动，但前提是这些事件未得到解决，例如：

   * **[!UICONTROL 主题行缺失]**:电子邮件主题行是必填项。 了解如何在中定义和个性化 [此部分](create-email.md).

   <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL 消息的电子邮件版本为空]**:未配置电子邮件内容时，会显示此错误。 了解如何在 [此部分](get-started-email-design.md).

   * **[!UICONTROL 曲面不存在]**:如果在消息创建后删除了所选曲面，则无法使用消息。 如果出现此错误，请在消息中选择另一个曲面 **[!UICONTROL 属性]**. 了解有关 [此部分](../configuration/channel-surfaces.md).


>[!CAUTION]
>
>要使用电子邮件测试或激活历程/营销活动，您必须解析所有 **错误** 警报。

## 预览并发送电子邮件

定义消息内容后，您可以预览该内容以控制电子邮件的呈现，并使用测试用户档案检查个性化设置。 [了解详情](preview.md)

![](assets/email_designer_edit_simulate.png)

准备好电子邮件后，完成 [历程](../building-journeys/journey-gs.md) 或 [营销活动](../campaigns/create-campaign.md)，然后激活以发送消息。

>[!NOTE]
>
>要通过电子邮件开始和/或交互跟踪收件人的行为，请确保 **[!UICONTROL 跟踪]** 部分在历程的 [电子邮件活动](../building-journeys/journeys-message.md) 或在电子邮件中 [营销活动](../campaigns/create-campaign.md).<!--to move?-->

<!--

## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] Expression editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 

-->

