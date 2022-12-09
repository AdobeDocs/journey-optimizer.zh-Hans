---
solution: Journey Optimizer
product: journey optimizer
title: 配置推送通知
description: 了解如何在Journey Optimizer中创建推送通知
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# 创建推送通知 {#create-push-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push"
>title="推送消息创建"
>abstract="添加推送消息，然后使用表达式编辑器对其进行个性化设置。"

## 在历程或营销策划中创建推送通知 {#create}

要创建推送通知，请执行以下步骤：

>[!BEGINTABS]

>[!TAB 向历程添加推送]

1. 打开您的历程，然后从面板的“操作”部分拖放推送活动。

   ![](assets/push_create_1.png)

1. 提供有关消息的基本信息（标签、描述、类别），然后选择要使用的消息界面。

   ![](assets/push_create_2.png)

   >[!NOTE]
   >
   >如果您从历程发送推送通知，则可以利用Adobe Journey Optimizer的发送时间优化功能，根据历史打开率和点击率预测发送消息以最大化参与度的最佳时间。 [了解如何使用发送时间优化](../building-journeys/journeys-message.md#send-time-optimization)

   有关如何配置旅程的更多信息，请参阅 [本页](../building-journeys/journey-gs.md)

1. 在历程配置屏幕中，单击 **[!UICONTROL Edit content]** 按钮来配置推送内容。 [设计推送通知](design-push.md)

1. 定义消息内容后，即可使用测试用户档案进行预览和测试。

1. 在推送准备就绪后，完成 [历程](../building-journeys/journey-gs.md) 来发送。

   要通过推送开始和/或交互跟踪收件人的行为，请确保在 [电子邮件活动](../building-journeys/journeys-message.md).

>[!TAB 向营销活动添加推送]

1. 创建新的计划营销活动或API触发的营销活动，选择 **[!UICONTROL Push notification]** 作为您的操作，然后选择 **[!UICONTROL App surface]** 。 [了解有关推送配置的更多信息](push-configuration.md).

   ![](assets/push_create_3.png)

1. 单击 **[!UICONTROL Create]**.

1. 从 **[!UICONTROL Properties]** ，编辑营销活动的 **[!UICONTROL Title]** 和 **[!UICONTROL Description]**.

   ![](assets/push_create_4.png)

1. 单击 **[!UICONTROL Select audience]** 按钮，以从可用Adobe Experience Platform区段列表中定义要定位的受众。 [了解更多](../segment/about-segments.md).

1. 在 **[!UICONTROL Identity namespace]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解更多](../event/about-creating.md#select-the-namespace).

   ![](assets/push_create_5.png)

1. 营销活动设计为在特定日期或定期频率执行。 了解如何配置 **[!UICONTROL Schedule]** 在 [此部分](../campaigns/create-campaign.md#schedule).

1. 从 **[!UICONTROL Action triggers]** 菜单，选择 **[!UICONTROL Frequency]** 在您的推送通知中：

   * 一次
   * 每日
   * 每周
   * 每月

1. 在营销活动配置屏幕中，单击 **[!UICONTROL Edit content]** 按钮来配置推送内容。 [设计推送通知](design-push.md)

1. 定义消息内容后，即可使用测试用户档案进行预览和测试。

1. 在推送准备就绪后，完成 [营销活动](../campaigns/create-campaign.md) 来发送。

   要通过推送开始和/或交互跟踪收件人的行为，请确保在 [营销活动](../campaigns/create-campaign.md).

>[!ENDTABS]

**相关主题**

* [配置推送渠道](push-gs.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)

## 快速投放模式 {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="快速投放模式"
>abstract="快速投放模式允许您在推送渠道上执行向受众大小在30M以下的高速消息发送。"

快速交付模式（以前称为历程中的突发模式）是 [!DNL Journey Optimizer] 附加组件，允许通过营销活动以大量量发送非常快速的推送消息。

当消息投放的延迟对业务至关重要时，如果您想在手机上发送紧急推送警报（例如，向已安装您的新闻渠道应用程序的用户发送突发新闻），可使用快速投放。

有关使用快速投放模式时性能的更多信息，请参阅 [Adobe Journey Optimizer产品说明](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

### 先决条件 {#prerequisites}

快速投放消息具有以下要求：

* 快速交付适用于 **[!UICONTROL Scheduled]** 仅限促销活动，且不适用于API触发的促销活动、
* 推送消息中不允许进行个性化，
* 目标受众必须包含少于3000个用户档案，
* 使用快速投放模式，最多可同时执行5个营销活动。

### 激活快速投放模式

1. 创建推送通知营销活动并打开 **[!UICONTROL Rapid delivery]** 选项。

![](assets/create-campaign-burst.png)

1. 配置消息内容并选择要定位的受众。 [了解如何创建营销活动](#create)

   >[!IMPORTANT]
   >
   >确保消息内容不包含任何个性化，并且受众包含的用户档案少于3000万。

1. 与往常一样，查看并激活您的营销活动。 请注意，在测试模式下，消息不会通过快速投放模式发送。