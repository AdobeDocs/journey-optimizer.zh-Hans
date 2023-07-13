---
solution: Journey Optimizer
product: journey optimizer
title: 与 Adobe Campaign Standard 集成
description: 了解如何将Journey Optimizer与Adobe Campaign Standard集成
feature: Actions
topic: Administration
role: Admin,Developer
level: Intermediate
keywords: campaign， standard，集成，上限，操作
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 5%

---

# 与 Adobe Campaign Standard 集成 {#using_adobe_campaign_standard}

您可以使用Adobe Campaign Standard的事务性消息传送功能发送电子邮件、推送通知和短信。

如果您有Adobe Campaign Standard，则可使用内置操作来允许连接到Adobe Campaign Standard。

必须发布Campaign Standard事务型消息及其相关事件，才能在Journey Optimizer中使用。 如果事件已发布但消息未发布，则它将不会显示在Journey Optimizer界面中。 如果消息已发布，但其关联事件未发布，则它将在Journey Optimizer界面中可见，但不可用。

## 重要说明 {#important-notes}

* 为Adobe Campaign Standard操作自动定义每5分钟4000次调用的上限规则。 这与Adobe Campaign Standard事务性消息传递的官方规模相对应。 有关事务性消息传递SLA的更多信息，请参阅 [Adobe Campaign Standard产品描述](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html).

* Adobe Campaign Standard集成是通过操作列表中的专用内置操作设置的。 需要为每个沙盒配置此设置。

* 您无法将Campaign Standard操作用于“受众”资格或“读取受众”活动。

* 历程不能同时使用消息和Campaign Standard操作。

## 配置操作 {#configure-action}

以下是配置它的步骤：

1. 选择 **[!UICONTROL 配置]** 在“管理”菜单部分中。 在  **[!UICONTROL 操作]** 部分，单击 **[!UICONTROL 管理]**. 将显示操作列表。

1. 选择内置 **[!UICONTROL AdobeCampaignStandard]** 操作。 操作配置窗格将在屏幕右侧打开。

   ![](assets/actioncampaign.png)

1. 复制Adobe Campaign Standard实例URL并将其粘贴到 **[!UICONTROL URL]** 字段。

1. 单击 **[!UICONTROL 测试实例URL]** 以测试实例的有效性。

   >[!NOTE]
   >
   >此测试可验证：
   >
   >主机为“.campaign.adobe.com”、“.campaign-sandbox.adobe.com”、“.campaign-demo.adobe.com”、“.ats.adobe.com”或“.adls.adobe.com”。
   >
   >URL以https开头，
   >
   >与此Adobe Campaign Standard实例关联的组织与Journey Optimizer的组织相同。

设计旅程时，以下三个操作将可用： **[!UICONTROL 操作]** 类别： **[!UICONTROL 电子邮件]**， **[!UICONTROL 推送]**， **[!UICONTROL 短信]** (请参阅 [使用Adobe Campaign操作](../building-journeys/using-adobe-campaign-standard.md))。

![](assets/journey58.png)

您可以使用 **反应** 事件，用于对与在同一历程中发送的Campaign Standard消息相关的跟踪数据做出反应。 对于推送通知，您可以对点击、发送或失败的消息做出反应。 对于短信消息，您可以对已发送或失败的消息做出反应。 对于电子邮件，您可以对点击、发送、打开或失败的消息做出反应。 参见 [反应事件](../building-journeys/reaction-events.md).

如果您使用第三方系统来发送消息，则需要添加和配置自定义操作。 参见 [关于自定义操作配置](../action/about-custom-action-configuration.md).
