---
solution: Journey Optimizer
product: journey optimizer
title: 预览短信消息
description: 了解如何在Journey Optimizer中预览和测试短信消息
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 6%

---

# 发送短信消息 {#send-sms}

## 预览短信消息 {#preview-sms}

定义消息内容后，即可使用测试用户档案进行预览和测试。 如果插入个性化内容，则可以利用测试用户档案数据检查此内容在消息中的显示方式。

1. 单击 **[!UICONTROL 模拟内容]**.

1. 单击 **[!UICONTROL 管理测试用户档案]** 添加测试用户档案。

1. 通过 **[!UICONTROL 身份命名空间]** 和 **[!UICONTROL 标识值]** 字段。 然后，单击 **[!UICONTROL 添加用户档案]**.

   ![](assets/sms_preview_3.png)

1. 选择测试用户档案后，可以关闭 **[!UICONTROL 添加测试用户档案]** 窗口。

   ![](assets/sms_preview_1.png)

1. 在“预览和测试”窗口中，测试用户档案数据会用于消息内容。

   例如，对于此短信消息，两种消息内容都是个性化的：

   ![](assets/sms_preview_2.png)

## 验证短信{#sms-preview}

>[!NOTE]
>
> 为了更好地交付，您应始终使用提供商支持的格式的电话号码。 例如， Twilio和Sinch仅支持E.164格式的电话号码。

您还必须检查编辑器上部的警报。  其中一些是简单的警告，但其他警告可能会阻止您使用消息。 可以发生两种类型的警报：

* **警告** 请参阅建议和最佳实践。 例如，如果短信消息为空，则会显示一条消息。

* **错误** 阻止您测试或激活历程，但前提是这些历程未得到解决。 例如，将显示一条消息，警告您主题行缺失。

![](assets/sms-alert-button.png)

当短信消息准备就绪时，完成 [历程](../building-journeys/journey-gs.md) 或 [营销活动](../campaigns/create-campaign.md) 来发送。

**相关主题**

* [配置短信渠道](sms-configuration.md)
* [短信报告](../reports/journey-global-report.md#sms-global)
* [创建短信消息](create-sms.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
