---
title: 创建营销活动
description: 了解如何在 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: 28380dbadf485ba05f7ef6788a50253876718441
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 11%

---

# 创建营销活动 {#create-campaign}

>[!NOTE]
>
>在创建新营销活动之前，请确保您有表面渠道（即消息预设）和Adobe Experience Platform区段可供使用。 请通过以下章节了解更多信息：
>
>* [创建渠道平面](../configuration/channel-surfaces.md)
>* [区段入门](../segment/about-segments.md)


## 创建您的第1个营销活动 {#create}

1. 访问 **[!UICONTROL Campaigns]** 菜单，然后单击 **[!UICONTROL Create campaign]**.

   >[!NOTE]
   >
   >您还可以复制现有的实时营销活动以创建新营销活动。 [了解详情](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

<!--1. In the **[!UICONTROL Properties]** section, specify when you want to execute the campaign:

    * **[!UICONTROL Scheduled]**: execute the campaign immediately or on a specified date. Scheduled campaigns are aimed at sending **marketing** type messages.
    * **[!UICONTROL API-triggered]**: execute the campaign using an API call. API-triggered campaigns are aimed at sending **transactional** messages, i.e. messages sent out following an action performed by an individual: password reset, card abandonment etc. [Learn how to trigger a campaign using APIs](api-triggered-campaigns.md)-->

1. 在 **[!UICONTROL Actions]** 部分，选择用于发送消息的渠道和渠道表面，然后单击 **[!UICONTROL Create]**.

   平面是由[系统管理员](../start/path/administrator.md)定义的配置。它包含用于发送消息的所有技术参数，如标头参数、子域、移动应用程序等。[了解详情](../configuration/channel-surfaces.md)。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >下拉列表中只列出与营销活动类型兼容的渠道表面。

<!--Only channel surfaces compatible with the campaign type (marketing or transactional) are listed in the drop-down list.-->

1. 指定营销活动的标题和描述。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 在 **[!UICONTROL Actions]** 部分，配置要与营销活动一起发送的消息：

   1. 单击 **[!UICONTROL Edit content]** 按钮，然后配置和设计消息内容。 [了解有关消息的更多信息](../messages/get-started-content.md).

      在以下页面中了解创建消息内容的详细步骤：

      * [创建电子邮件](../messages/create-email.md)
      * [创建推送通知](../messages/create-push.md)
      * [创建短信消息](../messages/create-sms.md)
   1. 定义内容后，使用 **[!UICONTROL Simulate content]** 按钮来预览和测试使用测试用户档案的内容。 [了解详情](../design/preview.md)。

   1. 单击箭头可返回至营销活动创建屏幕。

      ![](assets/create-campaign-design.png)

   1. 在 **[!UICONTROL Actions tracking]** 部分，指定是否要跟踪收件人对投放的反应：您可以跟踪点击和/或打开次数。

      一旦执行了营销活动，即可从营销活动报表访问跟踪结果。 [进一步了解营销活动报告](../reports/campaign-global-report.md)


1. 定义要定位的受众。 为此，请单击 **[!UICONTROL Select audience]** 按钮以显示可用的Adobe Experience Platform区段列表。 [了解有关区段的更多信息](../segment/about-segments.md)

   <!-- NOTE For API-triggered campaigns, the audience needs to be set via API call. [Learn more](api-triggered-campaigns.md)-->

   在 **[!UICONTROL Identity namespace]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >属于某个客户群的不同身份中没有选定身份（命名空间）的个人将不会被营销活动定位。

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

1. 要在特定日期或定期频率执行营销活动，请配置 **[!UICONTROL Schedule]** 中。 [了解如何计划营销活动](#schedule)

营销活动准备就绪后，您可以查看并发布它。 [了解详情](#review-activate)

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

1. 营销活动现已激活。 其状态为 **[!UICONTROL Live]**&#x200B;或 **[!UICONTROL Scheduled]** 输入开始日期。 [进一步了解营销活动状态](get-started-with-campaigns.md#statuses).

   营销活动中配置的消息将立即或在指定的日期发送。

   >[!NOTE]
   >
   >的 **[!UICONTROL Completed]** 状态会在营销活动激活后3天自动分配给该营销活动，或者如果营销活动已定期执行，则会在营销活动结束日期自动分配给该营销活动。
   >
   >如果未指定结束日期，营销活动将保留 **[!UICONTROL Live]** 状态。 要更改营销活动，您需要手动停止营销活动。 [了解如何停止营销活动](modify-stop-campaign.md)

1. 激活营销活动后，您可以随时打开营销活动信息以检查其信息。 利用摘要，可获取有关定向用户档案数量以及已提交和已失败操作的统计信息。

   您还可以通过单击 **[!UICONTROL Reports]** 按钮。 [了解详情](../reports/campaign-global-report.md)

   ![](assets/create-campaign-summary.png)

## 计划营销活动 {#schedule}

默认情况下，营销活动在手动激活后即开始，并在消息发送一次后结束。

您可以定义营销活动消息的发送频率。 为此，请使用 **[!UICONTROL Action triggers]** 营销活动创建屏幕中的选项，以指定应每日、每周还是每月执行营销活动。

如果您不想在营销活动激活后立即执行营销活动，则可以使用指定发送消息的日期和时间 **[!UICONTROL Campaign start]** 选项。 的  **[!UICONTROL Campaign end]** 选项，可指定应何时停止执行定期营销活动。

![](assets/create-campaign-schedule.png)
