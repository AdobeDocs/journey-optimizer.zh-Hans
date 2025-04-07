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
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 6%

---

# 检查和发送推送通知 {#send-push}

## 预览推送通知 {#preview-push}

定义消息内容后，您可以使用测试用户档案或从CSV/JSON文件上传的示例输入数据，或手动添加来预览其内容。 如果插入个性化内容，则可以检查此内容在消息中的显示方式。 [了解如何使用示例输入数据测试内容](../test-approve/simulate-sample-input.md)

为此，请单击&#x200B;**[!UICONTROL 模拟内容]**。 然后，您可以选择预览内容的设备类型： **[!UICONTROL iOS]**&#x200B;或&#x200B;**[!UICONTROL Android]**。

![](assets/push_preview_3.png)

有关如何预览和测试内容的详细信息，请参阅[内容管理](../content-management/preview-test.md)部分。

## 验证推送通知 {#push-validate}

必须在编辑器的上半部分检查警报。 其中一些是简单的警告，但其他警告可能会阻止您发送消息。 可能会发生两种类型的警报：警告和错误。

* **警告**&#x200B;参考推荐和最佳实践。

* **错误**&#x200B;会阻止您测试或激活历程，只要这些错误未解决，例如：

   * **[!UICONTROL 消息的推送版本为空]**：在缺少推送通知正文或标题时显示此错误。 在[本节](create-push.md)中了解如何定义推送通知内容。

   * **[!UICONTROL 配置不存在]**：如果在创建消息后删除了您选择的配置，则无法使用消息。 如果出现此错误，请在消息&#x200B;**[!UICONTROL 属性]**&#x200B;中选择其他配置。 在[本节](../configuration/channel-surfaces.md)中了解有关渠道配置的更多信息。

   * **[!UICONTROL 推送iOS/Android有效负载已超出4KB的限制]**：推送通知大小不能超过4KB。 要遵守此限制，请尝试减少使用图像或表情符号。 在[本节](../push/create-push.md)中了解如何管理推送通知内容。

  ![](assets/push_alert.png)


>[!NOTE]
>
> 为了提高可投放性，您应始终按照提供商支持的格式使用电话号码。 例如，Twilio和Sinch仅支持E.164格式的电话号码。

## 发送推送通知{#push-send}

>[!IMPORTANT]
>
> 如果您的营销活动受批准政策的约束，则需要请求批准才能发送推送通知。 [了解详情](../test-approve/gs-approval.md)

当推送消息准备就绪时，请完成[历程](../building-journeys/journey-gs.md)或[营销活动](../campaigns/create-campaign.md)的配置以发送该消息。

**相关主题**

* [配置推送渠道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report-cja-push.md)
* [创建推送通知](create-push.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在营销活动中添加消息](../campaigns/create-campaign.md)

