---
solution: Journey Optimizer
product: journey optimizer
title: 创建短信消息
description: 了解如何在Journey Optimizer中创建短信消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 7%

---

# 创建短信消息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="创建短信"
>abstract="添加文本消息，然后使用表达式编辑器对其进行个性化设置。"

使用 [!DNL Journey Optimizer] 在客户的移动设备上向客户发送短信。 您可以从短信编辑器创建、个性化和预览文本格式的消息。

>[!NOTE]
>
>根据行业标准和法规，所有短信营销消息都必须包含一种方式，以便收件人轻松取消订阅。 为此，短信收件人可以使用选择加入和选择退出关键词进行回复。 [了解如何管理选择退出](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

可以创建短信投放：

* 在 **历程**:在历程中添加短信活动并定义基本设置后，请使用 **[!UICONTROL 操作：短信]** 用于创建短信消息内容的右窗格。

   有关如何配置历程的更多信息，请参阅此 [页面](../building-journeys/journey-gs.md).

* 在 **Campaign**:创建营销活动后，选择短信作为您的操作并定义基本设置。

   有关如何配置营销活动的更多信息，请参阅此 [页面](../campaigns/create-campaign.md#configure).

如果您是首次创建短信消息，请确保已配置短信渠道。 [了解详情](../configuration/sms-configuration.md)。

## 定义短信内容{#sms-content}

要开始个性化短信消息，请执行以下步骤：

1. 单击 **[!UICONTROL 消息]** 字段来打开表达式编辑器。

   ![](assets/sms-content.png)

1. 使用表达式编辑器定义内容并添加动态内容。 您可以使用任何属性，如配置文件名称或城市。 详细了解 [个性化](../personalization/personalize.md) 和 [动态内容](../personalization/get-started-dynamic-content.md) 在表达式编辑器中。

1. 单击 **[!UICONTROL 保存]** 并在预览中查看您的消息。

   ![](assets/sms-content-preview.png)

## 验证短信{#sms-preview}

>[!NOTE]
>
> 为了更好地交付，您应始终使用提供商支持的格式的电话号码。 例如， Twilio和Sinch仅支持E.164格式的电话号码。

定义消息内容后，即可使用测试用户档案进行预览和测试。 如果插入 [个性化内容](../personalization/personalize.md)，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

要可视化显示您的短信消息在移动设备上的显示方式，请单击 **[!UICONTROL 模拟内容]** 选项卡。 进一步了解 [此部分](../design/preview.md).

您还必须检查编辑器上部的警报。  其中一些是简单的警告，但其他警告可能会阻止您使用消息。 有关详细信息，请参阅[此部分](alerts.md)。

![](assets/sms-alert-button.png)

<!--
## How-to video

Learn how to configure, author, and include SMS messaging into your customer journeys.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)
-->
**相关主题**

* [配置短信渠道](../configuration/sms-configuration.md)
* [短信报告](../reports/journey-global-report.md#sms-global)
* [创建新消息](get-started-content.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
