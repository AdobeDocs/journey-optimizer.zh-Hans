---
solution: Journey Optimizer
product: journey optimizer
title: 创建电子邮件
description: 了解如何在Journey Optimizer中创建电子邮件
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b7b333e96e0f4b32a0f94c3f1e67f0f3d3fc2816
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 5%

---

# 创建电子邮件 {#create-email-bis}

要创建电子邮件，请执行以下步骤。

## 1.在历程或营销策划中创建电子邮件

添加 **[!UICONTROL 电子邮件]** 操作到历程或营销策划，并根据您的案例执行以下步骤。

>[!BEGINTABS]

>[!TAB 向历程添加电子邮件]

1. 打开您的历程，然后拖放 **[!UICONTROL 电子邮件]** 活动 **[!UICONTROL 操作]** 的子菜单。

1. 提供有关消息的基本信息（标签、描述、类别）。

1. 选择 [电子邮件界面] 。

   ![](assets/email_journey.png)

有关如何配置旅程的更多信息，请参阅 [本页](../building-journeys/journey-gs.md).

>[!TAB 向营销活动添加电子邮件]

1. 创建新的计划营销活动或API触发的营销活动，然后选择 **[!UICONTROL 电子邮件]** 作为您的操作。

1. 选择 [电子邮件界面] 。

   ![](assets/email_campaign.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 完成创建电子邮件促销活动的步骤。

   ![](assets/email_campaign_steps.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->

有关如何配置营销活动的详细信息，请参阅 [本页](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## 定义电子邮件内容

1. 在历程或营销活动配置屏幕中，单击 **[!UICONTROL 编辑内容]** 按钮以配置电子邮件内容。 [了解详情]

   ![](assets/email_campaign_edit_content.png)

1. 在 **[!UICONTROL 标题]** 部分 **[!UICONTROL 编辑内容]** 屏幕， **[!UICONTROL 从名称]**, **[!UICONTROL 从电子邮件]** 和 **[!UICONTROL 密送]** 字段来自您选择的电子邮件界面。 [了解详情] <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. 您可以添加主题行。 直接在相应的字段中键入纯文本，或使用 [表达式编辑器](../personalization/personalization-build-expressions.md) 个性化主题行。

1. 单击 **[!UICONTROL 编辑电子邮件正文]** 按钮以开始使用 [!DNL Journey Optimizer] Email Designer。 [了解详情]

   ![](assets/email_designer_edit_email_body.png)

   您还可以单击 **[!UICONTROL 代码编辑器]** 按钮，以使用显示的弹出窗口以纯HTML方式编码您自己的内容。

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >如果您已通过Email Designer创建或导入内容，则此内容将以HTML显示。

## 预览电子邮件

定义消息内容后，您可以预览该内容以控制电子邮件的呈现，并使用测试用户档案检查个性化设置。 [了解详情]

![](assets/email_designer_edit_simulate.png)

您还必须检查编辑器上部的警报。  其中一些是简单的警告，但其他警告可能会阻止您使用消息。 [了解详情](alerts.md)。

## 验证电子邮件内容

准备好电子邮件后，完成 [历程](../building-journeys/journey-gs.md) 或 [营销活动](../campaigns/create-campaign.md) 和激活以发送消息。

>[!NOTE]
>
>要通过电子邮件开始和/或交互跟踪收件人的行为，请确保 **[!UICONTROL 跟踪]** 部分在历程的 [电子邮件活动](../building-journeys/journeys-message.md) 或在电子邮件中 [营销活动](../campaigns/create-campaign.md).

您还必须检查编辑器上部的警报。  其中一些是简单的警告，但其他警告可能会阻止您使用消息。 [了解详情](alerts.md)

