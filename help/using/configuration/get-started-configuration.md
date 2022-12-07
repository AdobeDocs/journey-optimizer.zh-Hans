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
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 40%

---


# 开始使用 [!DNL Journey Optimizer] 配置 {#start-optimizer-configuration}

首次访问 [!DNL Journey Optimizer] 时，系统会为您预置一个生产沙盒，并根据您的合同分配特定数量的 IP。

要创建历程和发送消息，您需要完成以下配置步骤。

## 配置消息和渠道

定义渠道表面，调整和自定义消息。

* [委派以Adobe子域](about-subdomain-delegation.md) 要用于发送电子邮件和 [创建IP池](ip-pools.md) 将随您的实例配置的IP地址分组到一起。

* 管理在将电子邮件地址发送到禁止列表之前执行重试的天数。[了解详情](manage-suppression-list.md)

* 在 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch] 中定义推送通知设置。[了解详情](../push/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

* 配置您的实例以发送短信（当前仅适用于一组组织 — 有限可用性）。 [了解详情](../sms/sms-configuration.md)

* 创建渠道界面以配置传送消息所需的所有技术参数。 [了解详情](channel-surfaces.md)

* 在Adobe Experience Platform中提供多个地址/号码时，确定要优先用于收件人的电子邮件地址和/或电话号码。 [了解详情](primary-email-addresses.md)

## 配置历程

要构建历程，您需要配置 **[!UICONTROL 数据源]**, **[!UICONTROL 事件]** 和 **[!UICONTROL 操作]**. [了解详情](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* 的 **数据源** 配置允许您定义与系统的连接，以检索将在您的历程中使用的其他信息。 [了解详情](../datasource/about-data-sources.md)

* **事件**&#x200B;允许您统一触发历程，向流入历程的个人实时发送消息。在事件配置中，您可以配置历程中的预期事件。传入事件的数据按照 Adobe 体验数据模型 (XDM) 进行标准化。事件来自已验证和未验证事件（如 Adobe Mobile SDK 事件）的流摄取 API。[了解详情](../event/about-events.md)

* [!DNL Journey Optimizer] 附带内置消息功能，允许您设计和发送内容。 如果您使用第三方系统来发送消息，请创建 **自定义操作**. [了解详情](../action/action.md)