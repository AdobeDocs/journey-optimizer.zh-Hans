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
source-git-commit: d6a46a6db9bcef4def71e915389d725c69d851c3
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 2%

---

# 检查并发送您的短信(SMS/MMS){#send-sms}

## 预览您的短信 {#preview-sms}

定义消息内容后，您可以使用测试用户档案或示例输入数据（从CSV/JSON文件上传或手动添加）来预览其内容。 如果插入个性化内容，则可以检查此内容在消息中的显示方式。

为此，请单击&#x200B;**[!UICONTROL 模拟内容]**，然后使用测试用户档案数据检查您的消息。

![](assets/sms_preview_2.png)

有关如何预览和测试内容的详细信息，请参阅[内容管理](../content-management/preview-test.md)部分。

### 字符编码和限制 {#sms-character-limits}

访问&#x200B;**[!UICONTROL 模拟内容]**&#x200B;菜单时会显示字符计数，以协助规划和管理短信消息。

![](assets/sms_preview_3.png)

Journey Optimizer在其短信编辑器中使用UTF-8编码，允许您键入或粘贴双字节或Unicode字符。 这些字符随后被传输到服务提供商进行交付。 大多数SMS提供商使用GSM 7位编码处理具有160个字符限制的标准消息，并在检测到具有70个字符限制的非GSM字符时切换到UTF-16 (UCS-2)。

请注意，字符计数不反映动态个性化或非GSM 7位特殊字符引入的变体。

>[!IMPORTANT]
>
>Journey Optimizer短信投放报告不考虑串联消息和动态个性化，因此可能无法反映从提供商发送的实际消息数。 有关详细使用和计费信息，请联系您的Adobe代表。
>
>要了解最大程度地减少短信计费超额的最佳实践，请参阅[用于字符优化的短信最佳实践](sms-cost-optimization.md)。

## 验证您的内容 {#sms-validate}

>[!NOTE]
>
> 要改善可投放性，请按照提供商支持的格式使用电话号码。 例如，Twilio和Sinch仅支持E.164格式的电话号码。

必须在编辑器的上半部分检查警报。 其中一些是简单的警告，但其他警告可能会阻止您发送消息。 可能会发生两种类型的警报：警告和错误。

![](assets/sms-alert-button.png)

* **警告**&#x200B;参考推荐和最佳实践。 例如，如果文本消息为空或动态内容可能超过字符限制，则会显示警告消息。

  **字符限制：**&#x200B;每个区段160个字符（GSM 7位），Unicode/表情符号最多70个字符，总共1500个字符。

* **错误**&#x200B;会阻止您测试或激活历程，或发布营销活动，前提是这些错误未解决。 例如，当主题行缺失时，会有一条错误消息警告您。

即使您的模拟消息较短，也可能会显示警报&#x200B;**“已超出短信文本字符限制”**，因为验证会通过以最长时间评估所有条件分支、个性化字段和动态内容来计算&#x200B;**最大可能长度**。

验证会计算所有可能配置文件数据的最大长度，而模拟会显示一个测试配置文件的实际输出。

## 发送您的短信 {#sms-send}

>[!IMPORTANT]
>
> 如果您的营销活动受批准政策的约束，则需要请求批准才能发送短信。 [了解详情](../test-approve/gs-approval.md)

当您的短信准备就绪时，请完成[历程](../building-journeys/journey-gs.md)或[营销活动](../campaigns/create-campaign.md)的配置以发送该短信。

**相关主题**

* [配置短信渠道](sms-configuration.md)
* [短信/彩信报告](../reports/journey-global-report-cja-sms.md)
* [创建文本消息](create-sms.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
