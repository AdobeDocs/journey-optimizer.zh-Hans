---
title: 与 Adobe Campaign Standard 集成
description: 了解如何与Adobe Campaign Standard集成
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: d1902ac35d78ba73051b41b4fc82dc284382d1a4
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 5%

---

# 与 Adobe Campaign Standard 集成 {#using_adobe_campaign_standard}

您可以使用Adobe Campaign Standard的事务性消息传送功能发送电子邮件、推送通知和短信。

如果您拥有Adobe Campaign Standard，则可以使用内置操作来允许与Adobe Campaign Standard建立连接。

必须发布Campaign Standard事务型消息及其关联事件，才能在Journey Optimizer中使用。 如果事件已发布但消息未发布，则它将不会显示在Journey Optimizer界面中。 如果消息已发布，但未发布其关联事件，则它将在Journey Optimizer界面中可见，但将不可用。

## 重要说明 {#important-notes}

* 对于Adobe Campaign Standard操作，会自动定义每5分钟4000个调用的上限规则。 这对应于Adobe Campaign Standard事务型消息传递的官方规模。 有关事务性消息传递SLA的更多信息，请参阅 [Adobe Campaign Standard产品描述](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html).

* Adobe Campaign Standard集成通过操作列表中的专用内置操作进行设置。 需要为每个沙盒配置此设置。

* 不能将Campaign Standard操作与区段鉴别或读取区段活动结合使用。

* 历程不能同时使用消息和Campaign Standard操作。

## 配置操作 {#configure-action}

以下是配置该插件的步骤：

1. 选择 **[!UICONTROL Configurations]** 在“管理”菜单部分。 在  **[!UICONTROL Actions]** ，单击 **[!UICONTROL Manage]**. 将显示操作列表。

1. 选择内置 **[!UICONTROL AdobeCampaignStandard]** 操作。 操作配置窗格将在屏幕右侧打开。

   ![](assets/actioncampaign.png)

1. 复制Adobe Campaign Standard实例URL并将其粘贴到 **[!UICONTROL URL]** 字段。

1. 单击 **[!UICONTROL Test the instance URL]** 来测试实例的有效性。

   >[!NOTE]
   >
   >此测试验证：
   >
   >主机为“.campaign.adobe.com”、“.campaign-sandbox.adobe.com”、“.campaign-demo.adobe.com”、“.ats.adobe.com”或“.adls.adobe.com”。
   >
   >URL以https开头，
   >
   >与此Adobe Campaign Standard实例关联的组织与Journey Optimizer的组织相同。

设计历程时，可在 **[!UICONTROL Action]** 类别： **[!UICONTROL Email]**, **[!UICONTROL Push]**, **[!UICONTROL SMS]** (请参阅 [使用Adobe Campaign操作](../building-journeys/using-adobe-campaign-standard.md))。

![](assets/journey58.png)

您可以使用 **反应** 事件来响应与在同一历程中发送的Campaign Standard消息相关的跟踪数据。 对于推送通知，您可以对点击、发送或失败的消息做出反应。 对于短信消息，您可以对已发送或失败的消息做出响应。 对于电子邮件，您可以对点击、发送、打开或失败的消息做出响应。 请参阅 [反应事件](../building-journeys/reaction-events.md).

如果您使用第三方系统来发送消息，则需要添加和配置自定义操作。 请参阅 [关于自定义操作配置](../action/about-custom-action-configuration.md).
