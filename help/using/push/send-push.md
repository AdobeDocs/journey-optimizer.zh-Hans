---
solution: Journey Optimizer
product: journey optimizer
title: 检查并发送推送通知
description: 了解如何在Journey Optimizer中检查并发送推送通知
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 7%

---

# 检查并发送推送通知 {#send-push}

## 预览推送通知 {#preview-push}

定义消息内容后，您可以使用测试用户档案预览其内容。 如果插入个性化内容，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

为此，请单击 **[!UICONTROL 模拟内容]** 然后添加测试用户档案。 然后，您可以选择预览内容的设备类型： **[!UICONTROL iOS]** 或 **[!UICONTROL Android]**.

![](assets/push_preview_3.png)

有关如何选择测试用户档案和预览内容的详细信息，请参阅 [内容管理](../content-management/preview-test.md) 部分。

## 验证推送通知 {#push-validate}

必须在编辑器的上半部分检查警报。 其中一些是简单的警告，但其他警告可能会阻止您发送消息。 可能会发生两种类型的警报：警告和错误。

* **警告** 请参阅建议和最佳实践。

* **错误** 阻止测试或激活历程，只要它们未解析，例如：

   * **[!UICONTROL 消息的推送版本为空]**：当推送通知正文或标题缺失时，显示此错误。 了解如何在中定义推送通知内容 [本节](create-push.md).

   * **[!UICONTROL 表面不存在]**：如果在创建消息后删除了所选表面，则无法使用消息。 如果出现此错误，请在消息中选择另一个曲面 **[!UICONTROL 属性]**. 在中了解有关渠道界面的更多信息 [本节](../configuration/channel-surfaces.md).

   * **[!UICONTROL 推送iOS/Android有效负载已超出4KB的限制]**：推送通知大小不能超过4KB。 要遵守此限制，请尝试减少使用图像或表情符号。 了解如何在中管理推送通知内容 [本节](../push/create-push.md).

  ![](assets/push_alert.png)


>[!NOTE]
>
> 为了提高可投放性，您应始终按照提供商支持的格式使用电话号码。 例如，Twilio和Sinch仅支持E.164格式的电话号码。

## 发送推送通知{#push-send}

当您的推送消息准备就绪时，完成您的 [历程](../building-journeys/journey-gs.md) 或 [营销活动](../campaigns/create-campaign.md) 发送它。

**相关主题**

* [配置推送渠道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report.md#push-global)
* [创建推送通知](create-push.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在营销活动中添加消息](../campaigns/create-campaign.md)

