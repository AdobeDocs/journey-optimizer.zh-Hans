---
solution: Journey Optimizer
product: journey optimizer
title: 检查并测试您的短信
description: 了解如何在Journey Optimizer中检查和发送短信
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 75638e9b463278efab16b2b85ed2707640f088f2
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 3%

---

# 检查并发送您的短信(SMS/MMS){#send-sms}

## 预览您的短信 {#preview-sms}

定义消息内容后，您可以使用测试用户档案预览其内容。 如果插入个性化内容，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

为此，请单击&#x200B;**[!UICONTROL 模拟内容]**，然后添加测试用户档案以使用测试用户档案数据检查您的消息。

![](assets/sms_preview_2.png)

有关如何选择测试用户档案和预览内容的详细信息，请参阅[内容管理](../content-management/preview-test.md)部分。

## 验证您的内容 {#sms-validate}

必须在编辑器的上半部分检查警报。 其中一些是简单的警告，但其他警告可能会阻止您发送消息。 可能会发生两种类型的警报：警告和错误。

![](assets/sms-alert-button.png)

* **警告**&#x200B;参考推荐和最佳实践。 例如，如果文本消息为空，则会显示警告消息。

* **错误**&#x200B;会阻止您测试或激活历程，或发布营销活动，前提是这些错误未解决。 例如，当主题行缺失时，会有一条错误消息警告您。


>[!NOTE]
>
> 要改善可投放性，请按照提供商支持的格式使用电话号码。 例如，Twilio和Sinch仅支持E.164格式的电话号码。

## 发送您的短信 {#sms-send}

当您的短信准备就绪时，请完成[历程](../building-journeys/journey-gs.md)或[营销活动](../campaigns/create-campaign.md)的配置以发送该短信。

**相关主题**

* [配置短信渠道](sms-configuration.md)
* [短信/彩信报告](../reports/journey-global-report.md#sms-global)
* [创建文本消息](create-sms.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
