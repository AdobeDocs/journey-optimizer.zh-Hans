---
title: 创建营销策划
description: 了解如何在 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: b9fa6bff926eb8cee476fa53feb38ed783e048fc
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 3%

---


# 创建营销策划 {#create-campaign}

>[!NOTE]
>
>在创建新营销活动之前，请确保您有消息预设和Adobe Experience Platform区段可供使用。 请通过以下章节了解更多信息：
>
>* [创建消息预设](../configuration/message-presets.md)
>* [区段入门](../segment/about-segments.md)


## 配置营销活动 {#configure}

创建营销活动的步骤如下：

1. 访问 **[!UICONTROL Campaigns]** 菜单，然后单击 **[!UICONTROL Create campaign]**.

   ![](assets/create-campaign.png)

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date,
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. In this case, profiles to be targeted and triggers for actions need to be set via the API call.-->

1. 在 **[!UICONTROL Actions]** 部分，选择用于发送消息的渠道和消息表面（即消息预设）。

   ![](assets/create-campaign-action.png)

1. 指定营销活动的标题和描述。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

   ![](assets/create-campaign-properties.png)

1. 在 **[!UICONTROL Actions]** 部分，配置要与营销活动一起发送的消息：

   1. 单击 **[!UICONTROL Edit content]** 按钮，然后配置和设计消息。 [了解如何配置消息](../messages/get-started-content.md).

      内容准备就绪后，单击箭头以返回营销活动创建屏幕。

      ![](assets/create-campaign-design.png)

   1. 在 **[!UICONTROL Actions tracking]** 部分，指定是否要跟踪收件人对投放的反应。

      一旦执行了营销活动，即可从营销活动报表访问跟踪结果。 [进一步了解营销活动报告](campaign-global-report.md)

      ![](assets/create-campaign-action-properties.png)

1. 定义要定位的受众。 为此，请单击 **[!UICONTROL Select audience]** 按钮以显示可用的Adobe Experience Platform区段列表。 [了解有关区段的更多信息](../segment/about-segments.md)

   ![](assets/create-campaign-audience.png)

   <!--By default, the targeted audience for in-app messages includes all the users of the selected mobile application.-->

   在 **[!UICONTROL Identity namespace]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >属于某个客户群的不同身份中没有选定身份（命名空间）的个人将不会被营销活动定位。 <!--info vue dans section journeys, read segment-->

   <!--If you are creating a campaign to send an in-app message, you can choose how and when the message will be shown to the audience using existing mobile app triggers.-->
   <!-- where are triggers configured?-->

1. 配置营销活动的开始和结束日期。

   默认情况下，营销活动配置为在手动激活后启动，并在消息发送一次后以soons结束。

1. 此外，您还可以配置执行营销活动中配置的操作的频率。

   ![](assets/create-campaign-schedule.png)

营销活动准备就绪后，您可以查看并发布它(请参阅 [查看和激活营销活动](#review-activate))。

## 查看和激活营销活动 {#review-activate}

配置营销活动后，您需要先查看其参数和内容，然后再激活它。 为此，请执行以下步骤：

1. 在营销活动配置屏幕中，单击 **[!UICONTROL Review to activate]** 以显示营销活动摘要。

   摘要允许您根据需要修改营销活动，并检查是否有参数不正确或缺失。

   >[!IMPORTANT]
   >
   >如果出现错误，您将无法激活营销活动。 继续之前，请解决错误。

   ![](assets/create-campaign-alerts.png)

1. 检查营销活动配置是否正确，然后单击 **[!UICONTROL Activate]**.

   ![](assets/create-campaign-review.png)

1. 营销活动现已激活，并且 **[!UICONTROL Live]** 状态(或 **[!UICONTROL Scheduled]**  如果您指定了开始日期)。 [进一步了解营销活动状态](get-started-with-campaigns.md#statuses)

   营销活动中配置的消息将立即执行或在指定的日期执行。

   >[!NOTE]
   >
   >激活营销活动后，即使消息已执行，营销活动仍将保持“实时”状态。 要更改其状态，您需要手动停止它。 [了解如何停止营销活动](modify-stop-campaign.md)

1. 激活营销活动后，您可以随时打开营销活动信息以检查其信息。 利用摘要，可获取有关定向用户档案数量以及已提交和已失败操作的统计信息。

   您还可以通过单击 **[!UICONTROL Reports]** 按钮。 [了解详情](campaign-global-report.md)

   ![](assets/create-campaign-summary.png)

   >[!IMPORTANT]
   >
   >在营销活动中创建的消息专用于 [!DNL Journey Optimizer] 活动功能。 创建后，它们将只能从营销策划访问，且不会显示在 **[!UICONTROL Messages]** 菜单。