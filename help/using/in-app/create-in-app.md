---
title: 创建应用程序内通知
description: 了解如何在Journey Optimizer中创建应用程序内消息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内，消息，创建，开始
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 4%

---

# 创建应用程序内消息 {#create-in-app}

应用程序内消息是在营销活动的上下文中创建的。

>[!BEGINTABS]

>[!TAB 将应用程序内消息添加到历程]

>[!AVAILABILITY]
>
>应用程序内活动当前仅作为测试版提供给选定用户。 要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

1. 打开您的历程，然后拖放 **[!UICONTROL 应用程序内]** 活动 **[!UICONTROL 操作]** 的子菜单。

   当用户档案到达其历程结束时，向其显示的任何应用程序内消息都将自动过期。 因此，将在应用程序内活动之后自动添加等待活动，以确保设置正确的时间。

   ![](assets/in_app_journey_1.png)

1. 输入 **[!UICONTROL 标签]** 和 **[!UICONTROL 描述]** 的URL。

1. 选择 [应用程序内界面](inapp-configuration.md) 。

   ![](assets/in_app_journey_2.png)

1. 您现在可以使用 **[!UICONTROL 编辑内容]** 按钮。 [了解详情](design-in-app.md)

1. 单击 **[!UICONTROL 编辑触发器]** 来配置触发器。

   ![](assets/in_app_journey_4.png)

1. 选择应用程序内消息处于活动状态时触发的频率：

   * **[!UICONTROL 每次显示]**:在 **[!UICONTROL 移动设备应用程序触发器]** 下拉列表。
   * **[!UICONTROL 显示一次]**:仅当在 **[!UICONTROL 移动设备应用程序触发器]** 下拉列表。
   * **[!UICONTROL 点进前显示]**:在 **[!UICONTROL 移动设备应用程序触发器]** 下拉列表，直到SDK通过“已单击”操作发送interact事件。

1. 从 **[!UICONTROL 移动设备应用程序触发器]** 下拉列表中，选择将触发消息的事件和标准：

   1. 从左下拉菜单中，选择触发消息所需的事件。
   1. 从右下拉菜单中，选择选定事件所需的验证。
   1. 单击 **[!UICONTROL 添加]** 按钮。 然后，重复上述步骤。
   1. 选择事件的链接方式，例如选择 **[!UICONTROL 和]** 如果您愿意 **both** 触发器为true，以便显示或选择消息 **[!UICONTROL 或]** 如果您希望在 **e** 触发器是真的。
   1. 单击 **[!UICONTROL 保存]** 触发器配置后。

   ![](assets/in_app_journey_3.png)

1. 如有必要，可通过拖放其他操作或事件来完成您的历程流程。 [了解详情](../building-journeys/about-journey-activities.md)

1. 应用程序内消息准备就绪后，完成配置并发布历程以激活它。

有关如何配置旅程的更多信息，请参阅 [本页](../building-journeys/journey-gs.md).

>[!TAB 向营销活动添加应用程序内消息]

1. 访问 **[!UICONTROL 促销活动]** 菜单，然后单击 **[!UICONTROL 创建营销活动]**.

1. 在 **[!UICONTROL 属性]** 选择促销活动执行类型：已计划或API触发。 在 [本页](../campaigns/create-campaign.md#campaigntype).

1. 在 **[!UICONTROL 操作]** ，选择 **[!UICONTROL 应用程序内消息]** 和 **[!UICONTROL 应用程序界面]** 之前已为应用程序内消息配置。 然后，单击 **[!UICONTROL 创建]**.

   了解有关 [本页](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. 从 **[!UICONTROL 属性]** ，输入 **[!UICONTROL 标题]** 和 **[!UICONTROL 描述]** 描述。

1. 要为应用程序内消息分配自定义或核心数据使用标签，请选择 **[!UICONTROL 管理访问权限]**. [了解详情](../administration/object-based-access.md)。

1. 单击 **[!UICONTROL 选择受众]** 按钮，以从可用的Adobe Experience Platform区段列表中定义要定位的受众。 [了解详情](../segment/about-segments.md)。

   ![](assets/in_app_create_2.png)

1. 在 **[!UICONTROL 身份命名空间]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解详情](../event/about-creating.md#select-the-namespace)。

1. 单击 **[!UICONTROL 编辑触发器]** 选择将触发消息的事件和标准：

   1. 单击 **添加条件** 您希望触发器考虑多个事件或条件时，请执行以下操作。
   1. 选择事件的链接方式，例如选择 **[!UICONTROL 和]** 如果您愿意 **both** 触发器为true，以便显示或选择消息 **[!UICONTROL 或]** 如果您希望在 **e** 触发器是真的。
   1. 单击 **[!UICONTROL 创建组]** 将触发器分组在一起。

   ![](assets/in_app_create_3.png)

1. 选择应用程序内消息处于活动状态时触发的频率。 可以使用以下选项：

   * **[!UICONTROL 每次]**:在 **[!UICONTROL 移动设备应用程序触发器]** 下拉列表。
   * **[!UICONTROL 一次]**:仅当在 **[!UICONTROL 移动设备应用程序触发器]** 下拉列表。
   * **[!UICONTROL 点进之前]**:在 **[!UICONTROL 移动设备应用程序触发器]** 下拉列表，直到SDK通过“已单击”操作发送interact事件。
   * **[!UICONTROL X次数]**:显示此消息X时间。

1. 如果需要，请选择 **[!UICONTROL 每周时间]** 或 **[!UICONTROL 时间]** 将显示应用程序内消息。

1. 营销活动设计为在特定日期或定期频率执行。 了解如何配置 **[!UICONTROL 计划]** 在 [此部分](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. 您现在可以使用 **[!UICONTROL 编辑内容]** 按钮。 [了解详情](design-in-app.md)

   ![](assets/in_app_create_4.png)

>[!ENDTABS]

## 操作方法视频{#video}

以下视频演示如何在营销活动中创建、配置和发布应用程序内消息。

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**相关主题：**

* [设计应用程序内消息](design-in-app.md)
* [测试并发送应用程序内消息](send-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
* [应用程序内配置](inapp-configuration.md)