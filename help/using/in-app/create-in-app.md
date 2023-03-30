---
title: 创建应用程序内通知
description: 了解如何在Journey Optimizer中创建应用程序内消息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内，消息，创建，开始
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 1af9a3adeb6727e965e61434b0ed2c41ff3d4911
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 创建应用程序内消息 {#create-in-app}

应用程序内消息是在营销活动的上下文中创建的。

要创建应用程序内消息，请执行以下步骤：

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


## 操作方法视频{#video}

以下视频演示如何在营销活动中创建、配置和发布应用程序内消息。

>[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)


**相关主题：**

* [设计应用程序内消息](design-in-app.md)
* [测试并发送应用程序内消息](send-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
* [应用程序内配置](inapp-configuration.md)