---
title: 创建营销活动
description: 了解如何在 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 4%

---

# 创建营销活动 {#create-campaign}

>[!NOTE]
>
>在创建新营销活动之前，请确保您有表面渠道（即消息预设）和Adobe Experience Platform区段可供使用。 请通过以下章节了解更多信息：
>
>* [创建渠道平面](../configuration/channel-surfaces.md)
>* [区段入门](../segment/about-segments.md)


## 配置营销活动 {#configure}

创建营销活动的步骤如下：

1. 访问 **[!UICONTROL Campaigns]** 菜单，然后单击 **[!UICONTROL Create campaign]**.

   ![](assets/create-campaign.png)

   >[!NOTE]
   >
   >您还可以复制现有的实时营销活动以创建新营销活动。[了解详情](modify-stop-campaign.md#duplicate) <!-- check if only live campaigns-->

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date. Scheduled campaigns are aimed at sending **marketing** type messages.
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. API-triggered campaigns are aimed at sending **transactional** messages, i.e. messages sent out following an action performed by an individual: password reset, card abandonment etc. [Learn how to trigger a campaign using APIs](api-triggered-campaigns.md)-->

1. 在 **[!UICONTROL Actions]** 部分，选择用于发送消息的渠道和渠道表面，然后单击 **[!UICONTROL Create]**.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >下拉列表中只列出与促销活动类型（营销或事务型）兼容的渠道表面。

1. 指定营销活动的标题和描述。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 在 **[!UICONTROL Actions]** 部分，配置要与营销活动一起发送的消息：

   1. 单击 **[!UICONTROL Edit content]** 按钮，然后配置和设计消息内容。 [了解有关消息的更多信息](../messages/get-started-content.md)

      >[!NOTE]
      >
      >的 **[!UICONTROL Simulate content]** 按钮，可使用测试用户档案预览和测试内容。 [了解详情](../design/preview.md)

   1. 内容准备就绪后，单击箭头以返回营销活动创建屏幕。

      ![](assets/create-campaign-design.png)

   1. 在 **[!UICONTROL Actions tracking]** 部分，指定是否要跟踪收件人对投放的反应。

      一旦执行了营销活动，即可从营销活动报表访问跟踪结果。 [进一步了解营销活动报告](../reports/campaign-global-report.md)

1. 定义要定位的受众。 为此，请单击 **[!UICONTROL Select audience]** 按钮以显示可用的Adobe Experience Platform区段列表。 [了解有关区段的更多信息](../segment/about-segments.md)

   <!-- NOTE For API-triggered campaigns, the audience needs to be set via API call. [Learn more](api-triggered-campaigns.md)-->

   在 **[!UICONTROL Identity namespace]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >属于某个客户群的不同身份中没有选定身份（命名空间）的个人将不会被营销活动定位。

1. 配置营销活动的开始和结束日期。 默认情况下，营销活动配置为在手动激活后启动，并在消息发送一次后以soons结束。

1. 此外，您还可以指定执行营销活动中配置的操作的频率。

   <!-- NOTE For API-triggered campaigns, scheduling at a specific date and time with recurrence is not available as action is triggered via API. However, start and end date are relevant to ensure that, if an API call is made prior of after the window, then those get errored.-->

   ![](assets/create-campaign-schedule.png)

<!--1. If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

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

1. 营销活动现已激活，并且 **[!UICONTROL Live]** 状态(或 **[!UICONTROL Scheduled]**  如果您指定了开始日期)。 [进一步了解营销活动状态](get-started-with-campaigns.md#statuses). 营销活动中配置的消息将立即执行或在指定的日期执行。

   >[!NOTE]
   >
   >的 **[!UICONTROL Completed]** 状态会在营销活动激活后3天自动分配给该营销活动，或者如果营销活动已定期执行，则会在营销活动结束日期自动分配给该营销活动。
   >
   >如果未指定结束日期，营销活动将保持“正常”状态。 要更改营销活动，您需要手动停止营销活动。 [了解如何停止营销活动](modify-stop-campaign.md)

1. 激活营销活动后，您可以随时打开营销活动信息以检查其信息。 利用摘要，可获取有关定向用户档案数量以及已提交和已失败操作的统计信息。

   您还可以通过单击 **[!UICONTROL Reports]** 按钮。 [了解详情](../reports/campaign-global-report.md)

   ![](assets/create-campaign-summary.png)
