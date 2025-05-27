---
solution: Journey Optimizer
product: journey optimizer
title: 与 Adobe Campaign Standard 集成
description: 了解如何将Journey Optimizer与Adobe Campaign Standard集成
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: campaign， standard，集成，上限，操作
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: d92c280e40419d2e3ec62a7ba85cd492a0867fde
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 3%

---

# 与 Adobe Campaign Standard 集成 {#using_adobe_campaign_standard}

如果您有Adobe Campaign Standard，则可使用内置操作来允许与Adobe Campaign Standard的连接。 您可以使用Adobe Campaign Standard的事务性消息传送功能发送电子邮件、推送通知和短信。

必须发布Campaign Standard事务型消息及其关联的事件，才能在Journey Optimizer中使用。 如果事件已发布但消息未发布，则不会在Journey Optimizer界面中看到该消息。 如果消息已发布，但其关联事件未发布，则它将在Journey Optimizer界面中可见，但不可用。

## 护栏和限制 {#important-notes}

* 为Adobe Campaign Standard操作自动定义每5分钟4000次调用的上限规则。 在[Adobe Campaign Standard产品描述](https://helpx.adobe.com/cn/legal/product-descriptions/campaign-standard.html){target="_blank"}中阅读有关事务性消息传递SLA的更多信息。

* Adobe Campaign Standard集成通过操作列表中的专用内置操作进行设置。 必须为每个沙盒配置此设置。

* Campaign Standard操作不能用于“受众”资格或“读取受众”活动。

* 历程不能同时使用[内置渠道操作](../building-journeys/journeys-message.md)和[Campaign Standard操作](../building-journeys/using-adobe-campaign-standard.md)。

## 配置操作 {#configure-action}

在Journey Optimizer中，必须为每个事务型消息配置一个操作。

要配置Campaign Standard操作，请执行以下步骤：

1. 在“管理”菜单部分中选择&#x200B;**[!UICONTROL 配置]**。

1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;部分中，单击&#x200B;**[!UICONTROL 管理]**。 将显示操作列表。

1. 选择内置&#x200B;**[!UICONTROL AdobeCampaignStandard]**&#x200B;操作。 操作配置窗格将在屏幕右侧打开。

   ![](assets/actioncampaign.png)

1. 复制Adobe Campaign Standard实例URL并将其粘贴到&#x200B;**[!UICONTROL URL]**&#x200B;字段中。

1. 单击&#x200B;**[!UICONTROL 测试实例URL]**&#x200B;以测试实例的有效性。

   >[!NOTE]
   >
   >此测试将验证：
   >
   >* 主机为“.campaign.adobe.com”、“.campaign-sandbox.adobe.com”、“.campaign-demo.adobe.com”、“.ats.adobe.com”或“.adls.adobe.com”
   >
   >* URL以https开头
   >
   >* 与此Adobe Campaign Standard实例关联的组织与Journey Optimizer的OrganizationRG相同

完成此配置后，在设计历程时，**[!UICONTROL 操作]**&#x200B;类别中有三个操作可用： **[!UICONTROL 电子邮件]**、**[!UICONTROL 推送]**、**[!UICONTROL 短信]**。 [了解如何使用它们](../building-journeys/using-adobe-campaign-standard.md)。

![](assets/journey58.png)

使用&#x200B;**反应**&#x200B;事件对与在同一历程中发送的Campaign Standard消息相关的跟踪数据做出反应：

* 对于推送通知，历程可以对点击、发送或失败的消息做出反应。

* 对于短信消息，历程可对已发送或失败的消息做出反应。

* 对于电子邮件，历程可以对点击、发送、打开或失败的消息做出反应。 [了解有关反应事件的更多信息](../building-journeys/reaction-events.md)。

使用第三方系统发送消息时，必须添加并配置自定义操作。 [了解有关自定义操作配置的更多信息](../action/about-custom-action-configuration.md)。