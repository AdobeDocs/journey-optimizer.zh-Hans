---
solution: Journey Optimizer
product: journey optimizer
title: 开始使用 [!DNL Journey Optimizer] 配置
description: 详细了解 [!DNL Journey Optimizer] 配置
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---


# 开始使用 [!DNL Journey Optimizer] 配置 {#start-optimizer-configuration}

访问 [!DNL Journey Optimizer] 首次配置了生产沙盒，并根据您的合同分配了特定数量的IP。

要创建历程和发送消息，您需要完成以下配置步骤。

## 配置消息和渠道

1. 要创建和发送消息，您需要根据渠道执行特定配置。

   * 对于 **电子邮件** 渠道中，您需要将子域委派给Adobe并创建IP池以将IP地址分组到一起。 [了解更多](../email/get-started-email-config.md)

   * 对于 **推送** 渠道，您需要在 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch]. [了解更多](../push/push-configuration.md)

   * 对于 **短信** 渠道中，您需要配置实例以发送短信，包括将提供商设置与 [!DNL Journey Optimizer]. [了解更多](../sms/sms-configuration.md)

1. 完成后，您必须创建 **通道曲面** 配置投放消息所需的所有技术参数。 [了解更多](channel-surfaces.md)

1. 您还可以：

   * 管理在向抑制列表发送电子邮件地址之前执行重试的天数。 [了解更多](manage-suppression-list.md)

   * 启用 **BBC电子邮件选项** 来保存发送给个人的邮件副本。 [了解更多](archiving-support.md#enable-bcc)

   * 配置 **频率规则** 以避免过度关注收件人。 [了解更多](frequency-rules.md)

   * 当Adobe Experience Platform中有多个地址/号码可用时，确定要优先为收件人使用的电子邮件地址和/或电话号码。 [了解更多](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>这些步骤必须由 [Adobe Journey Optimizer系统管理员](../start/path/administrator.md).

## 配置历程

要构建历程，您需要配置 **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** 和 **[!UICONTROL Actions]**. [了解更多](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* 的 **数据源** 配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息。 [了解更多](../datasource/about-data-sources.md)

* **事件** 允许您一直触发旅程，以实时向流入旅程的个人发送消息。 在事件配置中，您可以配置历程中预期的事件。 传入事件的数据按照Adobe体验数据模型(XDM)进行标准化。 事件来自经过身份验证和未经身份验证的事件（例如Adobe Mobile SDK事件）的流摄取API。 [了解更多](../event/about-events.md)

* [!DNL Journey Optimizer] 附带内置消息功能，允许您设计和发送内容。 如果您使用第三方系统来发送消息，请创建 **自定义操作**. [了解更多](../action/action.md)