---
title: 在历程中创建应用程序内通知
description: 了解如何在Journey Optimizer中创建应用程序内消息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内，消息，创建，开始
hide: true
hidefromtoc: true
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 2%

---

# 在历程中创建应用程序内消息 {#create-in-app-journey}

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

## 应用程序内活动限制 {#in-app-activity-limitations}

* 此功能当前不适用于医疗保健客户。

* 个性化只能包含配置文件属性。

* 应用程序内显示已绑定到历程生命周期，这意味着当某个用户档案的历程结束时，该历程中的所有应用程序内消息将停止为该用户档案显示。 这意味着您无法直接从历程活动中停止应用程序内活动。 你必须结束那段旅程。
* 应用程序内显示与历程的生命周期相关联，这意味着当某个特定用户配置文件的历程完成后，该历程中的所有应用程序内消息将不再为该用户档案显示。 因此，无法直接从历程活动中停止应用程序内消息。 相反，您需要结束整个历程，以阻止应用程序内消息显示到用户档案。

* 使用此功能，您将无法 **[!UICONTROL 反应]** 活动来对应用程序内打开或单击做出响应。

* 从用户配置文件在画布中到达应用程序内活动时到用户开始看到该应用程序内消息时，会出现激活延迟。 此延迟可介于15分钟到1小时之间。

**相关主题：**

* [设计应用程序内消息](design-in-app.md)
* [测试并发送应用程序内消息](send-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
* [应用程序内配置](inapp-configuration.md)