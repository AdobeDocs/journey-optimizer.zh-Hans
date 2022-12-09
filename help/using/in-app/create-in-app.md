---
title: 创建应用程序内通知
description: 了解如何在Journey Optimizer中创建应用程序内消息
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# 创建应用程序内消息 {#create-in-app}

## 创建营销活动和应用程序内消息{#create-in-app-in-a-campaign}

要创建应用程序内消息，请执行以下步骤：

1. 访问 **[!UICONTROL Campaigns]** 菜单，然后单击 **[!UICONTROL Create campaign]**.

1. 在 **[!UICONTROL Properties]** 部分，指定您希望何时执行营销活动。

1. 在 **[!UICONTROL Actions]** ，选择 **[!UICONTROL In-app message]** 和 **[!UICONTROL App surface]** 之前已为应用程序内消息配置。 然后，单击 **[!UICONTROL Create]**.

   [了解有关应用程序内配置的更多信息](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. 从 **[!UICONTROL Properties]** ，编辑营销活动的 **[!UICONTROL Title]** 和 **[!UICONTROL Description]**.

1. 要为登陆页面分配自定义或核心数据使用标签，请选择 **[!UICONTROL Manage access]**. [了解更多](../administration/object-based-access.md).

1. 单击 **[!UICONTROL Select audience]** 按钮，以从可用Adobe Experience Platform区段列表中定义要定位的受众。 [了解更多](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. 在 **[!UICONTROL Identity namespace]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解更多](../event/about-creating.md#select-the-namespace).

1. 选择应用程序内消息处于活动状态时触发的频率：

   * **[!UICONTROL Show every time]**:在 **[!UICONTROL Mobile app trigger]** 下拉列表。
   * **[!UICONTROL Show once]**:仅当在 **[!UICONTROL Mobile app trigger]** 下拉列表。
   * **[!UICONTROL Show until click through]**:在 **[!UICONTROL Mobile app trigger]** 下拉列表，直到SDK通过“已单击”操作发送interact事件。

1. 从 **[!UICONTROL Mobile app trigger]** 下拉列表中，选择将触发消息的事件和标准：

   1. 从左下拉菜单中，选择触发消息所需的事件。
   1. 从右下拉菜单中，选择选定事件所需的验证。
   1. 单击 **[!UICONTROL Add]** 按钮。 然后，重复上述步骤。
   1. 选择事件的链接方式，例如选择 **[!UICONTROL And]** 如果您愿意 **both** 触发器为true，以便显示或选择消息 **[!UICONTROL Or]** 如果您希望在 **e** 触发器是真的。

   ![](assets/in_app_create_3.png)

1. 从 **[!UICONTROL Mobile app trigger]**
下拉菜单。

   通过选择触发器，您可以选择显示应用程序内消息的用户操作。

   ![](assets/in_app_create_3.png)

1. 营销活动设计为在特定日期或定期频率执行。 了解如何配置 **[!UICONTROL Schedule]** 在 [此部分](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. 您现在可以使用 **[!UICONTROL Edit content]** 按钮。

   ![](assets/in_app_create_4.png)

## 发送应用程序内消息{#in-app-send}

### 在设备上预览 {#preview-device}

您可以在特定设备中预览应用程序内通知。

1. 单击 **[!UICONTROL Preview on device]**.

   ![](assets/in_app_create_6.png)

1. 从 **[!UICONTROL Connect to device]** 窗口，单击 **[!UICONTROL Start]**.

1. 键入 **[!UICONTROL Base URL]** ，单击 **[!UICONTROL Next]**.

   ![](assets/in_app_create_7.png)

1. 使用设备扫描二维码并输入显示的PIN码。

现在，您可以直接在设备上触发应用程序内消息，以便在实际设备上预览和查看消息。

### 查看并激活应用程序内通知{#in-app-review}

创建应用程序内消息并定义其内容并进行个性化后，您便可以查看并激活该消息。

要执行此操作，请执行以下步骤：

1. 使用 **[!UICONTROL Review to activate]** 按钮以显示消息摘要。

   摘要允许您根据需要修改营销活动，并检查是否有参数不正确或缺失。

   ![](assets/in_app_create_5.png)

1. 检查营销活动配置是否正确，然后单击 **[!UICONTROL Activate]**.

您的营销活动现已激活。 营销活动中配置的应用程序内通知将立即发送，或在指定的日期发送。

发送后，您可以在营销活动报表中衡量应用程序内消息的影响。 有关报告的更多信息，请参阅 [此部分](inapp-report.md).

**相关主题：**

* [设计应用程序内消息](design-in-app.md)
* [应用程序内报表](inapp-report.md)
* [应用程序内配置](inapp-configuration.md)
