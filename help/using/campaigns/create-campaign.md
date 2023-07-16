---
solution: Journey Optimizer
product: journey optimizer
title: 创建营销活动
description: 了解如何在Journey Optimizer中创建营销活动
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 创建，优化器，营销活动，界面，消息
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: ceb37193797c69ee87f136f3abecf54b5927d6a2
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 28%

---

# 创建营销活动 {#create-campaign}

>[!NOTE]
>
>在创建新营销活动之前，请确保您拥有可供使用的表面渠道（即消息预设）和Adobe Experience Platform受众。 请参阅以下部分以了解详情：
>
>* [创建渠道平面](../configuration/channel-surfaces.md)
>* [受众入门](../audience/about-audiences.md)

要创建新营销活动，请访问 **[!UICONTROL 营销活动]** 菜单，然后单击 **[!UICONTROL 创建营销活动]**. 您还可以复制现有的实时营销活动以创建新营销活动。 [了解详情](modify-stop-campaign.md#duplicate)

## 选择营销活动类型和渠道 {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="营销活动类型"
>abstract="立即执行或在指定日期执行&#x200B;**计划的营销活动**，其旨在发送市场营销类型的消息。使用 API 调用执行 **API 触发的**&#x200B;活动。其旨在发送市场营销消息或事务性消息，如在个人执行操作后发送的消息：重置密码、丢弃购物车等。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="营销活动类别"
>abstract="如果正在创建计划的营销活动，则将自动选择&#x200B;**市场营销**&#x200B;类型。对于 API 触发的营销活动，选择要发送&#x200B;**市场营销**&#x200B;还是&#x200B;**事务性**&#x200B;消息，如在个人执行操作后发送的消息：重置密码、丢弃购物车等。"

1. 在 **[!UICONTROL 属性]** 部分，指定您希望如何执行营销策划。 有两种类型的营销活动可用：

   * **[!UICONTROL 已计划]**：立即执行营销活动，或在指定日期执行。 计划的营销活动旨在发送 **营销** 消息。 它们可以从用户界面配置和执行。

   * **[!UICONTROL API触发]**：使用API调用执行营销活动。 API触发的营销活动旨在发送 **营销**，或 **事务性** 消息，即在个人执行操作（密码重置、购物车购买等）后发送的消息。 [了解如何使用API触发营销活动](api-triggered-campaigns.md)

1. 如果正在创建计划的营销活动，则将自动选择&#x200B;**市场营销**&#x200B;类型。对于API触发的营销活动，请选择是否要发送 **营销** 或 **事务性** 信息。”

1. 在 **[!UICONTROL 操作]** 部分，选择用于发送消息的渠道和渠道平面。

   平面是由[系统管理员](../start/path/administrator.md)定义的配置。它包含用于发送消息的所有技术参数，如标头参数、子域、移动应用程序等。[了解详情](../configuration/channel-surfaces.md)。

   下拉列表中仅列出与营销活动类型兼容的渠道平面。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >如果您正在创建推送通知营销活动，则可以启用 **[!UICONTROL 快速投放模式]**，它是一个Journey Optimizer加载项，允许以非常快的速度大量发送推送消息。 [了解详情](../push/create-push.md#rapid-delivery)

1. 单击 **[!UICONTROL 创建]** 以创建营销活动。

## 定义营销活动属性 {#create}

1. 在 **[!UICONTROL 属性]** 部分，指定营销策划的名称和描述。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 此 **标记** 字段允许您向营销活动分配Adobe Experience Platform统一标记。 这样，您就可以轻松地对营销活动进行分类，并改进营销活动列表中的搜索。[了解如何使用标记](../start/search-filter-categorize.md#tags)

1. 要将自定义或核心数据使用标签分配给活动，请单击 **[!UICONTROL 管理访问权限]** 按钮。 [了解有关对象级访问控制(OLA)的更多信息](../administration/object-based-access.md)

## 创建消息并配置跟踪 {#content}

在 **[!UICONTROL 操作]** 部分，创建要与营销活动一起发送的消息。

1. 单击 **[!UICONTROL 编辑内容]** 按钮，然后创建和设计消息内容。

   在以下页面中了解创建消息内容的详细步骤：

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="潜在客户" src="../assets/do-not-localize/email.jpg">
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

1. 定义内容后，请使用 **[!UICONTROL 模拟内容]** 按钮，使用测试用户档案预览和测试您的内容。 [了解详情](../email/preview.md)。

1. 单击箭头以返回营销策划创建屏幕。

   ![](assets/create-campaign-design.png)

1. 在 **[!UICONTROL 操作跟踪]** 部分，指定是否要跟踪收件人对投放的反应：您可以跟踪点击和/或打开。

   执行营销活动后，即可从营销活动报表访问跟踪结果。 [了解有关活动报告的更多信息](../reports/campaign-global-report.md)

## 定义受众 {#audience}

单击 **[!UICONTROL 选择受众]** 按钮以显示可用Adobe Experience Platform区段的列表。 [了解有关区段的更多信息](../audience/about-audiences.md)

>[!NOTE]
>
>对于API触发的营销活动，需要通过API调用设置受众。 [了解详情](api-triggered-campaigns.md)

在 **[!UICONTROL 身份命名空间]** 字段，选择要使用的命名空间，以标识所选区段中的个人。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

>[!NOTE]
>
>如果属于区段的个人在不同的身份中没有选定的身份（命名空间），则营销活动不会将该个人设为目标。

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## 计划营销活动 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="营销活动开始"
>abstract="指定应发送消息的日期和时间。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="营销活动结束"
>abstract="指定应停止执行周期性营销活动的时间。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="营销活动操作触发器"
>abstract="定义营销活动消息的发送频率。"

默认情况下，营销活动在手动激活后开始，在发送一次消息后结束。

您可以定义发送营销活动消息的频率。 要执行此操作，请使用 **[!UICONTROL 操作触发器]** 活动创建屏幕中的选项，用于指定活动是应每日、每周还是每月执行。

如果不想在活动激活后立即执行活动，则可以使用指定发送消息的日期和时间 **[!UICONTROL 营销活动开始]** 选项。 此 **[!UICONTROL 营销活动结束]** 选项允许您指定何时应停止执行定期活动。

![](assets/create-campaign-schedule.png)

活动准备就绪后，您可以对其进行审核和发布。 [了解详情](review-activate-campaign.md)
