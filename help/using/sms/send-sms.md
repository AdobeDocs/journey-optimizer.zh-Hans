---
solution: Journey Optimizer
product: journey optimizer
title: 预览和测试短信消息
description: 了解如何在Journey Optimizer中预览和测试短信消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 12%

---

# 预览和测试短信消息 {#send-sms}

## 预览短信 {#preview-sms}

定义消息内容后，即可使用测试配置文件对其进行预览和测试。如果插入个性化内容，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

1. 单击 **[!UICONTROL 模拟内容]**.

1. 单击 **[!UICONTROL 管理测试用户档案]** 以添加测试用户档案。

1. 使用查找您的测试用户档案 **[!UICONTROL 身份命名空间]** 和 **[!UICONTROL 标识值]** 字段。 然后，单击 **[!UICONTROL 添加配置文件]**.

   ![](assets/sms_preview_3.png)

1. 选择测试用户档案后，您可以关闭 **[!UICONTROL 添加测试配置文件]** 窗口。

1. 从 **预览和测试** 窗口，测试用户档案数据添加到消息内容。

   ![](assets/sms_preview_2.png)


## 验证短信{#sms-validate}

必须在编辑器的上半部分检查警报。 其中一些是简单的警告，但其他警告可能会阻止您发送消息。 可能会发生两种类型的警报：警告和错误。

* **警告** 请参阅建议和最佳实践。 例如，如果短信消息为空，则会显示警告消息。

* **错误** 阻止测试或激活历程，或发布营销活动（只要它们未解析）。 例如，当主题行缺失时，会有一条错误消息警告您。

![](assets/sms-alert-button.png)

>[!NOTE]
>
> 要改善可投放性，请按照提供商支持的格式使用电话号码。 例如，Twilio和Sinch仅支持E.164格式的电话号码。

## 发送短信{#sms-send}

短信消息就绪后，完成配置 [历程](../building-journeys/journey-gs.md) 或 [营销活动](../campaigns/create-campaign.md) 发送它。

**相关主题**

* [配置短信渠道](sms-configuration.md)
* [短信报告](../reports/journey-global-report.md#sms-global)
* [创建短信消息](create-sms.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
