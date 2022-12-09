---
title: 设计应用程序内内容
description: 了解如何在Journey Optimizer中设计应用程序内内容
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# 设计应用程序内内容 {#design-content}

您可以编辑应用程序内内容以配置体验选项，包括消息布局和显示、文本和按钮选项。

要配置消息内容，请单击 **[!UICONTROL Edit content]** 按钮，然后使用屏幕右侧部分的选项来设计应用程序内消息内容。

![](assets/edit-in-app-content.png)

的 **[!UICONTROL Advanced formatting]** 切换可激活其他选项以自定义体验。

创建应用程序内消息并定义其内容并进行个性化后，您便可以查看并激活该消息。 然后，将根据促销活动计划发送通知。 在 [本页](create-in-app.md#in-app-send).

## 消息布局 {#message-layout}

从 **[!UICONTROL Message Layout]** ，请从四个不同的布局选项中选择一个，具体选项取决于您的消息传送需求。

![](assets/in_app_content_1.png)

* **[!UICONTROL Fullscreen]**:此类布局会覆盖受众设备的整个屏幕。

   它支持媒体（图像、视频）、文本和按钮组件。

* **[!UICONTROL Modal]**:此布局显示在大型警报样式窗口中，背景中仍可看到您的应用程序。

   它支持媒体（图像、视频）、文本和按钮组件。

* **[!UICONTROL Banner]**:此类型的布局显示为本机操作系统警报消息。

   您只能添加 **[!UICONTROL Header]** 和 **[!UICONTROL Body]** 的URL。

* **[!UICONTROL Custom]**:自定义消息模式允许您直接导入和编辑预配置的HTML消息之一。

   * 选择 **[!UICONTROL Compose]** 输入或粘贴原始HTML代码。

      使用左窗格可利用Journey Optimizer个性化功能。 有关更多信息，请参阅 [此部分](../personalization/personalize.md).

   * 选择 **[!UICONTROL Import]** 导入包含HTML内容的HTML或.zip文件。

## “内容”选项卡 {#content-tab}

从 **内容** 选项卡，您可以定义和个性化：通知的内容和 **关闭** 按钮。 您还可以向应用程序内通知添加媒体，并从此选项卡添加操作按钮。

### “关闭”按钮 {#close-button}

![](assets/in_app_content_2.png)

选择 **[!UICONTROL Style]** 您的 **[!UICONTROL Close button]**.

可用的样式包括：

* **[!UICONTROL Simple]**
* **[!UICONTROL Circle]**
* **[!UICONTROL Custom image]** 从媒体URL或您的资产。

+++更多具有高级格式的选项

如果 **[!UICONTROL Advanced formatting mode]** 已打开，您可以检查 **[!UICONTROL Color]** 选项来选择按钮的颜色和不透明度。

+++

### 媒体 {#add-media}

的 **[!UICONTROL Media]** 字段允许您向应用程序内消息中添加媒体，从而为最终用户创建引人入胜的体验。

![](assets/in_app_content_3.png)

键入您的媒体URL，或单击 **[!UICONTROL Select Assets]** 图标，可直接将存储在资产库中的资产添加到应用程序内消息。 [了解有关资产管理的更多信息](../email/assets-essentials.md).
您还可以添加 **[!UICONTROL Alternative text]** 屏幕读取应用程序。

+++更多具有高级格式的选项

如果 **[!UICONTROL Advanced formatting mode]** 已打开，您可以自定义 **[!UICONTROL Max height]** 和 **[!UICONTROL Max width]** 你的媒体。

+++

### 标题和正文 {#title-body}

要撰写消息，请在 **[!UICONTROL Header]** 和 **[!UICONTROL Body]** 字段。

![](assets/in_app_content_4.png)

使用 **[!UICONTROL Personalization]** 图标以添加个性化。 在Adobe Journey Optimizer表达式编辑器中了解有关个性化的更多信息 [在此部分中](../personalization/personalize.md).

+++更多具有高级格式的选项

如果 **[!UICONTROL Advanced formatting mode]** 已打开，您可以 **[!UICONTROL Header]** 和 **[!UICONTROL Body]**:

* the **[!UICONTROL Font]**
* the **[!UICONTROL Pt size]**
* the **[!UICONTROL Font Color]**
* the **[!UICONTROL Alignment]**
+++

### 按钮 {#add-buttons}

为用户添加按钮以与应用程序内消息进行交互。

![](assets/in_app_content_5.png)

要个性化您的按钮，请执行以下操作：

1. 编辑按钮#1文本（主）字段。 您还可以使用 **[!UICONTROL Personalization]** 图标来定义内容和个性化数据。

1. 选择 **[!UICONTROL Interact event]** 定义用户与按钮交互后按钮的操作。

1. 在 **[!UICONTROL Target]** 字段。

1. 要添加多个按钮，请单击 **[!UICONTROL Add button]**.

+++更多具有高级格式的选项

如果 **[!UICONTROL Advanced formatting mode]** 已打开，您可以 **[!UICONTROL Buttons]**:

* the **[!UICONTROL Font]**
* the **[!UICONTROL Pt size]**
* the **[!UICONTROL Font Color]**
* the **[!UICONTROL Alignment]**
* the **[!UICONTROL Button style]**
* the **[!UICONTROL Radius]**
* the **[!UICONTROL Button color]**

+++

## “设置”选项卡 {#settings-tab}

从 **设置** 选项卡，您可以定义消息布局并预览应用程序内消息。 您还可以访问高级格式选项。

### 预览 {#preview-tab}

![](assets/in_app_content_6.png)

的 **[!UICONTROL App Preview]** 用于在应用程序内消息后添加背景：

* 来自URL链接的媒体。

* 资产库中的资产。

* 背景颜色。

### 布局 {#layout-options}

![](assets/in_app_content_7.png)

的 **[!UICONTROL Background image]** 字段，可向应用程序内消息添加背景：

* 来自URL链接的媒体。

* 背景颜色。

### 消息 {#message-tab}

![](assets/in_app_content_8.png)

默认启用的UI接管选项允许您使应用程序内消息背景变暗，以强调对内容的关注。

+++更多具有高级格式的选项

如果 **[!UICONTROL Advanced formatting mode]** 启用后，您可以使用以下选项进一步个性化您的消息：

* **[!UICONTROL Customize gestures]**:允许您自定义用户轻扫交互的内容。 如果选择“取消”，则可以添加自定义交互事件和/或目标目标。

* **[!UICONTROL Customize UI takeover]**:用于选择要在背景中显示的颜色及其不透明度。

* **[!UICONTROL Customize size]**:允许您调整应用程序内通知的宽度和高度。

* **[!UICONTROL Customize position]**:允许您自定义应用程序内消息在用户屏幕上的位置。 您可以更改“垂直”和“水平”对齐方式。

* **[!UICONTROL Customize animation]**:允许您自定义显示和取消动画，例如，如果您的应用程序内通知从用户设备的左侧或顶部显示。

* **[!UICONTROL Message round corner]**:允许您通过更改 **[!UICONTROL Corner radius]**.

+++

**相关主题：**

* [创建应用程序内消息](create-in-app.md)
* [应用程序内报表](inapp-report.md)
* [应用程序内配置](inapp-configuration.md)
