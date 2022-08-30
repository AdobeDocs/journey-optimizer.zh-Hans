---
title: 在营销活动中添加消息
description: 了解如何在营销活动中添加消息
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 87f9a4661b64cf24a8cd62bb9c70d5f1c9fcaddf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 79%

---


# 在营销活动中添加消息{#messages-in- campaigns}

在营销活动中，选择渠道以设计要发送给受众的消息并对其进行个性化设置。 在向营销活动添加电子邮件、短信或推送时，您可以立即发送或计划发送消息。

>[!NOTE]
>您还可以创建历程以发送触发的消息。 了解更多 [在此部分中](messages-in-journeys.md).

了解如何在营销活动中添加和配置消息 [在此部分中](../campaigns/create-campaign.md)

在以下页面中了解创建消息内容的详细步骤：

* [创建电子邮件](create-email.md)
* [创建推送通知](create-push.md)
* [创建短信消息](create-sms.md)

## 启用发送时间优化{#sto-in-journeys}

对于电子邮件和推送通知，您可以启用 **[!UICONTROL Send-time optimization]**。

使用 **[!UICONTROL Send-time optimization]** 安排每个用户的个性化发送时间，以增加消息的打开率和点击率。[了解详情](../messages/send-time-optimization.md)。

## 高级参数{#adv-settings}

默认情况下，高级参数处于只读和隐藏状态。

要访问高级参数，请单击消息窗格顶部的 **[!UICONTROL Show read-only fields]** 图标。

![](assets/show-read-only.png)

高级参数将显示在消息窗格的底部。这些参数由[系统管理员](../start/path/administrator.md)在与消息相关的[渠道平面](../configuration/channel-surfaces.md)（即消息预设）中定义。

对于推送通知，您可以显示以下参数：令牌、应用程序 ID、应用程序平台。

![](assets/push-adv-parameters.png)

对于电子邮件，您可以显示主电子邮件地址。

对于特定用途，您可以在特定上下文中覆盖这些值。要强制使用某个值，请单击字段右侧的&#x200B;**启用参数覆盖**&#x200B;图标。此选项可能非常有用，例如在下列操作中：

* 测试电子邮件，可添加您的电子邮件地址。发布历程后，将向您发送电子邮件。
* 请参阅列表中订阅者的电子邮件地址。在[此用例](../building-journeys/message-to-subscribers-uc.md)中了解更多。

单击同一图标可隐藏高级设置。

## 浏览消息{#browse-message}

在历程中使用多条消息时，您可以在 **Edit Content** 屏幕中进行切换。

![](assets/inline-messages-multi-content.png)

然后，您可以[检查警报](alerts.md)并从单个视图中[模拟](../design/preview.md)每个内容。

## 复制消息 {#duplicate-message}

您可以从历程画布复制现有消息。

为此，请执行以下步骤：

1. 选择要复制的消息。

1. 使用 **[!UICONTROL Action]** 窗格中的 **[!UICONTROL Copy]** 按钮。

   ![](assets/message-duplicate.png)

1. 按 **crtl+V** 来粘贴消息。

   消息将会被添加到历程画布。所有设置和配置都将被复制到新消息中。

   ![](assets/message-duplicated.png)

1. 重命名消息以便能够将初始消息与副本区分开（例如在编辑消息时），如下所示：

   ![](assets/multi-message.png)


>[!NOTE]
>
>对于电子邮件，您还可以将现有消息转换为模板。[了解详情](../design/email-templates.md)。

## 删除消息{#delete-message}

要删除消息，请使用渠道操作活动窗格顶部的垃圾桶图标。

![](assets/delete-message.png)

使用 **[!UICONTROL Confirm]** 按钮进行验证。
