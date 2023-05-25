---
title: 创建应用程序内通知
description: 了解如何在Journey Optimizer中创建应用程序内消息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内、消息、创建、入门
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 64be9c41085dead10ff08711be1f39760a81ff95
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 6%

---

# 创建应用程序内消息 {#create-in-app}

<!--
>[!BEGINTABS]

>[!TAB Add an In-app message to a journey]

>[!AVAILABILITY]
>
>The In-app activity is currently available as a beta to select users only. To join the beta program, contact Adobe Customer Care.

1. Open your journey, then drag and drop an **[!UICONTROL In-app]** activity from the **[!UICONTROL Actions]** section of the palette.

    When a profile reaches the end of their journey, any in-app messages displayed to them will automatically expire. For that reason, a Wait activity is automatically added after your In-app activity to ensure proper timing.

    ![](assets/in_app_journey_1.png)

1. Enter a **[!UICONTROL Label]** and **[!UICONTROL Description]** for your message.

1. Choose the [In-app surface](inapp-configuration.md) to use.

    ![](assets/in_app_journey_2.png)

1. You can now start designing your content with the **[!UICONTROL Edit content]** button. [Learn more](design-in-app.md)

1. Click **[!UICONTROL Edit trigger]** to configure your Trigger. 

    ![](assets/in_app_journey_4.png)

1. Choose the frequency of your trigger when your In-app message is active:

    * **[!UICONTROL Show every time]**: Always show the message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show once]**: Only show this message the first time the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur.
    * **[!UICONTROL Show until click through]**: Show this message when the events selected in the **[!UICONTROL Mobile app trigger]** drop-down occur until an interact event is sent by the SDK with an action of "clicked".

1. From the **[!UICONTROL Mobile app trigger]** dropdown(s), choose the event(s) and criteria that will trigger your message:

    1. From the left drop-down, select the event required to trigger the message.
    1. From the right drop-down, select the validation required on the selected event.
    1. Click the **[!UICONTROL Add]** button if you want the trigger to consider multiple events or criteria. Then, repeat the steps above.
    1. Select how your events are linked, e.g. choose **[!UICONTROL And]** if you want **both** triggers to be true in order for a message to be shown or choose **[!UICONTROL Or]** if you want the message to be shown if **either** of the triggers are true.
    1. Click **[!UICONTROL Save]** when your Triggers have been configured.

    ![](assets/in_app_journey_3.png)
    
1. If necessary, complete your journey flow by dragging and dropping additional actions or events. [Learn more](../building-journeys/about-journey-activities.md)

1. Once your In-app message is ready, finalize the configuration and publish your journey to activate it.

For more information on how to configure a journey, refer to [this page](../building-journeys/journey-gs.md).

>[!TAB Add an In-app message to a campaign]
-->

1. 访问 **[!UICONTROL 营销活动]** 菜单，然后单击 **[!UICONTROL 创建营销活动]**.

1. 在 **[!UICONTROL 属性]** 部分，选择何时执行营销活动：已计划或API触发。 要了解有关促销活动类型的更多信息，请参阅 [此页面](../campaigns/create-campaign.md#campaigntype).

1. 在 **[!UICONTROL 操作]** 部分，选择 **[!UICONTROL 应用程序内消息]** 和 **[!UICONTROL 应用程序表面]** 之前为您的应用程序内消息配置的。 然后，单击 **[!UICONTROL 创建]**.

   在中了解有关应用程序内配置的更多信息 [此页面](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. 从 **[!UICONTROL 属性]** 部分，输入 **[!UICONTROL 标题]** 和 **[!UICONTROL 描述]** 描述。

1. 要将自定义或核心数据使用标签分配给应用程序内消息，请选择 **[!UICONTROL 管理访问权限]**. [了解详情](../administration/object-based-access.md)。

1. 单击 **[!UICONTROL 选择受众]** 按钮，从可用的Adobe Experience Platform区段列表中定义要定位的受众。 [了解详情](../segment/about-segments.md)。

   ![](assets/in_app_create_2.png)

1. 在 **[!UICONTROL 身份命名空间]** 字段，选择要使用的命名空间，以标识所选区段中的个人。 [了解详情](../event/about-creating.md#select-the-namespace)。

1. 单击 **[!UICONTROL 创建试验]** 开始配置内容实验并创建处理以衡量其性能并为目标受众确定最佳选项。 [了解详情](../campaigns/content-experiment.md)

1. 单击 **[!UICONTROL 编辑触发器]** 选择将触发消息的事件和条件：

   1. 单击 **添加条件** 您希望触发器考虑多个事件或标准。
   1. 选择事件的链接方式，例如，选择 **[!UICONTROL 和]** 如果您愿意 **两者** 触发器为true，以便显示或选择消息 **[!UICONTROL 或]** 如果您希望显示消息，如果 **任一** 的触发条件为真。
   1. 单击 **[!UICONTROL 创建组]** 将触发器组合在一起。

   ![](assets/in_app_create_3.png)

1. 选择应用程序内消息处于活动状态时触发的频率。 可以使用以下选项：

   * **[!UICONTROL Everytime]**：当在中选择了事件时，始终显示消息 **[!UICONTROL 移动应用程序触发器]** 出现下拉列表。
   * **[!UICONTROL 一次]**：仅在第一次在中选择事件时显示此消息 **[!UICONTROL 移动应用程序触发器]** 出现下拉列表。
   * **[!UICONTROL 点进之前]**：当在中选择事件时显示此消息 **[!UICONTROL 移动应用程序触发器]** 在SDK通过“已单击”操作发送交互事件之前，将会出现下拉列表。
   * **[!UICONTROL X次数]**：显示此消息X次。

1. 如有需要，选择所需的 **[!UICONTROL 星期几]** 或 **[!UICONTROL 一天中的时间]** 此时将显示应用程序内消息。

1. 营销活动设计为按特定日期或重复频率执行。 了解如何配置 **[!UICONTROL 计划]** 中的促销活动 [本节](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. 您现在可以使用开始设计内容 **[!UICONTROL 编辑内容]** 按钮。 [了解详情](design-in-app.md)

   ![](assets/in_app_create_4.png)

<!--
>[!ENDTABS]
-->

## 操作方法视频{#video}

以下视频介绍如何在营销活动中创建、配置和发布应用程序内消息。

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**相关主题：**

* [设计应用程序内消息](design-in-app.md)
* [测试并发送应用程序内消息](send-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
* [应用程序内配置](inapp-configuration.md)