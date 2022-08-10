---
title: 创建营销活动
description: 了解如何在 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 6%

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

1. 在 **[!UICONTROL Properties]** 部分，指定您希望何时执行营销活动：

   * **[!UICONTROL Scheduled]**:立即执行营销活动或在指定日期执行营销活动。 计划的营销活动旨在发送 **营销** 键入消息。
   * **[!UICONTROL API-triggered]**:使用API调用执行营销活动。 API触发的营销活动旨在发送 **事务性** 消息，即在个人执行操作后发出的消息：密码重置、卡放弃等。 [了解如何使用API触发营销活动](api-triggered-campaigns.md)

1. 在 **[!UICONTROL Actions]** 部分，选择用于发送消息的渠道和渠道表面，然后单击 **[!UICONTROL Create]**.

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >下拉列表中只列出与促销活动类型（营销或事务型）兼容的渠道表面。

1. 指定营销活动的标题和描述。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 在 **[!UICONTROL Actions]** 部分，配置要与营销活动一起发送的消息：

   1. 单击 **[!UICONTROL Edit content]** 按钮，然后配置和设计消息内容。 [了解有关消息的更多信息](../messages/get-started-content.md).

      内容准备就绪后，单击箭头以返回营销活动创建屏幕。

      ![](assets/create-campaign-design.png)

   1. 在 **[!UICONTROL Actions tracking]** 部分，指定是否要跟踪收件人对投放的反应。

      一旦执行了营销活动，即可从营销活动报表访问跟踪结果。 [进一步了解营销活动报告](campaign-global-report.md)

1. 定义要定位的受众。 为此，请单击 **[!UICONTROL Select audience]** 按钮以显示可用的Adobe Experience Platform区段列表。 [了解有关区段的更多信息](../segment/about-segments.md)

   >[!NOTE]
   >
   >对于API触发的营销活动，需要通过API调用来设置受众。 [了解详情](api-triggered-campaigns.md)

   在 **[!UICONTROL Identity namespace]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解有关命名空间的更多信息](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >属于某个客户群的不同身份中没有选定身份（命名空间）的个人将不会被营销活动定位。

1. 配置营销活动的开始和结束日期。 默认情况下，营销活动配置为在手动激活后启动，并在消息发送一次后以soons结束。

1. 此外，您还可以指定执行营销活动中配置的操作的频率。

   >[!NOTE]
   >
   >对于由API触发的营销活动，由于通过API触发操作，因此无法安排特定日期和时间重复的发生。 但是，开始日期和结束日期是相关的，这可确保如果在窗口之后之前进行API调用，则这些调用会出错。

   ![](assets/create-campaign-schedule.png)

1. 如果要创建由API触发的营销活动，请 **[!UICONTROL cURL request]** 部分，用于检索 **[!UICONTROL Campaign ID]** 以在API调用中使用。 [了解详情](api-triggered-campaigns.md)

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

## 其他资源

* [营销活动入门](get-started-with-campaigns.md)
* [创建API触发的营销活动](api-triggered-campaigns.md)
* [修改或停止营销活动](modify-stop-campaign.md)
* [营销活动实时报告](campaign-live-report.md)
* [营销活动全局报告](campaign-global-report.md)
