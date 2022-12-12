---
solution: Journey Optimizer
product: journey optimizer
title: 创建营销活动
description: 了解如何在 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: ef838945e0c3595de8ad920203b278bb51671d16
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 0%

---

# 创建营销活动 {#create-campaign}

>[!NOTE]
>
>在创建新营销活动之前，请确保您有一个表面渠道（即消息预设）和一个Adobe Experience Platform区段可供使用。 请通过以下章节了解更多信息：
>
>* [创建通道曲面](../configuration/channel-surfaces.md)
>* [区段快速入门](../segment/about-segments.md)


## 创建您的第一个营销活动 {#create}

1. 访问 **[!UICONTROL Campaigns]** 菜单，然后单击 **[!UICONTROL Create campaign]**.

   >[!NOTE]
   >
   >您还可以复制现有的实时营销活动以创建新营销活动。 [了解更多](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

1. 在 **[!UICONTROL Properties]** 部分，指定您希望如何执行营销活动：

   * **[!UICONTROL Scheduled]**
   * **[!UICONTROL API-triggered]**

   有关促销活动类型和相关参与的详细信息，请参阅此 [部分](#campaigntype).

1. 在 **[!UICONTROL Actions]** 部分，选择用于发送消息的渠道和渠道表面，然后单击 **[!UICONTROL Create]**.

   曲面是由 [系统管理员](../start/path/administrator.md). 它包含用于发送消息的所有技术参数，如标头参数、子域、移动设备应用程序等。 [了解更多](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >下拉列表中只列出与营销活动类型兼容的渠道表面。

1. 指定营销活动的标题和描述。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 要为营销活动分配自定义或核心数据使用标签，请单击 **[!UICONTROL Manage access]** 按钮。 [了解有关对象级别访问控制(OLA)的更多信息](../administration/object-based-access.md)

## 创建消息 {#content}

在 **[!UICONTROL Actions]** 部分创建要与营销活动一起发送的消息。

1. 单击 **[!UICONTROL Edit content]** 按钮，然后创建和设计消息内容。

   了解在以下页面中创建消息内容的详细步骤：

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="商机" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>创建电子邮件</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="不频繁" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>创建推送通知</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="验证" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>创建短信消息</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. 定义内容后，使用 **[!UICONTROL Simulate content]** 按钮来预览和测试使用测试用户档案的内容。 [了解更多](../email/preview.md).

1. 单击箭头可返回至营销活动创建屏幕。

   ![](assets/create-campaign-design.png)

1. 在 **[!UICONTROL Actions tracking]** 部分，指定是否要跟踪收件人对投放的反应：您可以跟踪点击和/或打开次数。

   一旦执行了营销活动，即可从营销活动报表访问跟踪结果。 [进一步了解营销活动报告](../reports/campaign-global-report.md)

## 定义受众 {#audience}

1. 定义要定位的受众。 为此，请单击 **[!UICONTROL Select audience]** 按钮以显示可用Adobe Experience Platform区段列表。 [了解有关区段的更多信息](../segment/about-segments.md)

   >[!NOTE]
   >
   >对于API触发的营销活动，需要通过API调用来设置受众。 [了解更多](api-triggered-campaigns.md)

   在 **[!UICONTROL Identity namespace]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >属于某个客户群的不同身份中没有选定身份（命名空间）的个人将不会被营销活动定位。

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## 计划营销活动 {#schedule}

1. 要在特定日期或定期频率执行营销活动，请配置 **[!UICONTROL Schedule]** 中。 [了解如何计划营销活动](#schedule)

1. 要为营销活动分配自定义或核心数据使用标签，请单击 **[!UICONTROL Manage access]** 按钮。 [了解有关对象级别访问控制(OLA)的更多信息](../administration/object-based-access.md)

营销活动准备就绪后，您可以查看并发布它。 [了解更多](#review-activate)

## 营销活动类型 {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="营销活动类型"
>abstract="对于通过指定发送日期的营销消息， **已计划** 类型是最合适的。 但是，如果要发送诸如密码重置或卡放弃之类的事务型消息，请 **API触发** 类型是最佳选择。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="促销活动类别"
>abstract="类别值直接链接到促销活动类型值。 为 **营销** 类别和API触发的类别类型 **事务型**"

可用的营销活动类型有两种：

* **[!UICONTROL Scheduled]**:立即执行营销活动或在指定日期执行营销活动。 计划的营销活动旨在发送 **营销** 键入消息。

* **[!UICONTROL API-triggered]**:使用API调用执行营销活动。 API触发的营销活动旨在发送 **事务性** 消息，即在个人执行操作后发出的消息：密码重置、卡放弃等。 [了解如何使用API触发营销活动](api-triggered-campaigns.md)
