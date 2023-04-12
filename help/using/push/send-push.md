---
solution: Journey Optimizer
product: journey optimizer
title: 预览和测试推送通知
description: 了解如何在Journey Optimizer中预览和测试推送通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 9%

---

# 预览和测试推送通知 {#send-push}

## 预览推送通知 {#preview-push}

定义消息内容后，即可使用测试配置文件对其进行预览和测试。如果插入个性化内容，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

1. 单击 **[!UICONTROL 模拟内容]**.

1. 单击 **[!UICONTROL 管理测试用户档案]** 添加测试用户档案。

1. 通过 **[!UICONTROL 身份命名空间]** 和 **[!UICONTROL 标识值]** 字段。 然后，单击 **[!UICONTROL 添加用户档案]**.

   ![](assets/push_preview_1.png)

1. 选择测试用户档案后，可以关闭 **[!UICONTROL 添加测试用户档案]** 窗口。

1. 从 **预览和测试** 窗口中，测试用户档案数据会添加到消息内容中。

   选择要预览内容的设备类型： **[!UICONTROL iOS]** 或 **[!UICONTROL Android]**.

   ![](assets/push_preview_3.png)

## 验证推送通知 {#push-validate}


您必须在编辑器的上半部分检查警报。 其中一些是简单的警告，但其他一些可能会阻止您发送消息。 可以发生两种类型的警报：警告和错误。

* **警告** 请参阅建议和最佳实践。

* **错误** 阻止您测试或激活历程（只要它们未得到解析），例如：

   * **[!UICONTROL 消息的推送版本为空]**:当推送通知正文或标题缺失时，将显示此错误。 了解如何在 [此部分](create-push.md).

   * **[!UICONTROL 曲面不存在]**:如果在消息创建后删除了所选曲面，则无法使用消息。 如果出现此错误，请在消息中选择另一个曲面 **[!UICONTROL 属性]**. 了解有关 [此部分](../configuration/channel-surfaces.md).

   * **[!UICONTROL 推送iOS/Android有效负载超过4KB的限制]**:推送通知大小不能超过4KB。 要遵守此限制，请尽量减少使用图像或表情符号。 了解如何在 [此部分](../push/create-push.md).

   ![](assets/push_alert.png)


>[!NOTE]
>
> 为了更好地交付，您应始终使用提供商支持的格式的电话号码。 例如， Twilio和Sinch仅支持E.164格式的电话号码。

## 发送推送通知{#push-send}

在您的推送消息准备就绪后，完成 [历程](../building-journeys/journey-gs.md) 或 [营销活动](../campaigns/create-campaign.md) 来发送。

**相关主题**

* [配置推送渠道](push-configuration.md)
* [推送通知报告](../reports/journey-global-report.md#push-global)
* [创建推送通知](create-push.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在营销活动中添加消息](../campaigns/create-campaign.md)

