---
title: 设计应用程序内内容
description: 了解如何在Journey Optimizer中设计应用程序内内容
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内、消息、设计、格式
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 0c32248d13c08a98e9298ddc932aa2e547ab2acd
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 5%

---

# 设计应用程序内内容 {#design-content}

您可以编辑应用程序内内容以配置体验选项：

* 在 **[!UICONTROL 营销活动]**，来自 **[!UICONTROL 操作]** 菜单，要配置消息内容，请单击 **[!UICONTROL 编辑内容]** 按钮。

  ![](assets/edit-in-app-content.png)

* 在 **[!UICONTROL 历程]**，通过应用程序内消息的高级菜单 **[!UICONTROL 操作]**，您可以使用来开始设计内容 **[!UICONTROL 编辑内容]** 按钮。

  ![](assets/design_inapp_journey.png)

此 **[!UICONTROL 高级格式化]** 切换可激活其他选项以自定义体验。

创建应用程序内消息，并定义其内容并对其进行个性化后，即可查看和激活该消息。 然后，将根据营销活动计划发送通知。 请参阅[此页面](send-in-app.md)以了解详情。

## 消息布局 {#message-layout}

从 **[!UICONTROL 消息布局]** 部分，根据您的消息传送需求从四个不同的布局选项中选择一个。

![](assets/in_app_content_1.png)

* **[!UICONTROL 全屏]**：此类型的布局会覆盖受众设备的整个屏幕。

  此选项支持媒体（图像、视频）、文本和按钮组件。

* **[!UICONTROL 模态]**：此布局显示在大型警报样式窗口中，背景中仍可看到您的应用程序。

  此选项支持媒体（图像、视频）、文本和按钮组件。

* **[!UICONTROL 横幅]**：此类型的布局显示为本机操作系统警报消息。

  您只能添加 **[!UICONTROL 页眉]** 和 **[!UICONTROL 正文]** 到您的消息中。

* **[!UICONTROL 自定义]**：利用自定义消息模式，可直接导入和编辑其中一个预配置的HTML消息。

   * 选择 **[!UICONTROL 撰写]** 输入或粘贴原始HTML代码。

     使用左窗格以利用Journey Optimizer个性化功能。 有关详细信息，请参阅[此部分](../personalization/personalize.md)。

   * 选择 **[!UICONTROL 导入]** 导入包含HTML内容的HTML或.zip文件。

## “内容”选项卡 {#content-tab}

从 **内容** 选项卡上，您可以定义并个性化：通知的内容和样式 **关闭** 按钮。 您还可以向应用程序内通知添加媒体，并在此选项卡中添加操作按钮。

### “关闭”按钮 {#close-button}

![](assets/in_app_content_2.png)

选择 **[!UICONTROL 样式]** 的 **[!UICONTROL “关闭”按钮]**.

可用的样式包括：

* **[!UICONTROL 简单]**
* **[!UICONTROL 圆形]**
* **[!UICONTROL 自定义图像]** 从媒体URL或您的资产中。

+++更多高级格式选项

如果 **[!UICONTROL 高级格式模式]** 打开，您可以检查 **[!UICONTROL 颜色]** 选项以选择按钮的颜色和不透明度。

+++

### 媒体 {#add-media}

此 **[!UICONTROL 媒体]** 字段允许您将媒体添加到应用程序内消息，从而为最终用户创造有趣的体验。

![](assets/in_app_content_3.png)

键入您的媒体URL或单击 **[!UICONTROL 选择资源]** 图标，用于将存储在资产库中的资产直接添加到应用程序内消息。 [了解有关资产管理的更多信息](../email/assets-essentials.md).
您还可以添加 **[!UICONTROL 替换文本]** 用于屏幕阅读应用程序。

+++更多高级格式选项

如果 **[!UICONTROL 高级格式模式]** 打开，您可以自定义 **[!UICONTROL 最大高度]** 和 **[!UICONTROL 最大宽度]** 您的媒体的。

+++

### 页眉和正文 {#title-body}

要撰写消息，请在 **[!UICONTROL 页眉]** 和 **[!UICONTROL 正文]** 字段。

![](assets/in_app_content_4.png)

使用 **[!UICONTROL 个性化]** 图标以添加个性化。 了解有关Adobe Journey Optimizer表达式编辑器中个性化的更多信息 [在此部分中](../personalization/personalize.md).

+++更多高级格式选项

如果 **[!UICONTROL 高级格式模式]** 已打开，您可以为 **[!UICONTROL 页眉]** 和 **[!UICONTROL 正文]**：

* 该 **[!UICONTROL 字体]**
* 该 **[!UICONTROL Pt大小]**
* 该 **[!UICONTROL 字体颜色]**
* 该 **[!UICONTROL 对齐方式]**
+++

### 按钮 {#add-buttons}

添加按钮以方便用户与应用程序内消息进行交互。

![](assets/in_app_content_5.png)

要个性化您的按钮，请执行以下操作：

1. 编辑按钮#1文本（主）字段。 您也可以使用 **[!UICONTROL 个性化]** 图标来定义内容和个性化数据。

1. 选择您的 **[!UICONTROL Interact事件]** 用于定义用户与按钮交互后按钮的操作。

1. 在“ ”中输入您的Web URL或深层链接 **[!UICONTROL Target]** 字段。

1. 要添加多个按钮，请单击 **[!UICONTROL “添加”按钮]**.

+++更多高级格式选项

如果 **[!UICONTROL 高级格式模式]** 已打开，您可以为 **[!UICONTROL 按钮]**：

* 该 **[!UICONTROL 字体]**
* 该 **[!UICONTROL Pt大小]**
* 该 **[!UICONTROL 字体颜色]**
* 该 **[!UICONTROL 对齐方式]**
* 该 **[!UICONTROL 按钮样式]**
* 该 **[!UICONTROL 半径]**
* 该 **[!UICONTROL 按钮颜色]**

+++

## “设置”选项卡 {#settings-tab}

从 **设置** 选项卡，您可以定义消息布局并预览应用程序内消息。 您还可以访问高级格式设置选项。

### 预览 {#preview-tab}

![](assets/in_app_content_6.png)

此 **[!UICONTROL 应用程序预览]** 允许您在应用程序内消息后添加背景：

* URL链接中的媒体。

* 资产库中的资产。

* 背景颜色。

### 版式 {#layout-options}

![](assets/in_app_content_7.png)

此 **[!UICONTROL 背景图像]** 字段用于向应用程序内消息添加背景：

* URL链接中的媒体。

* 背景颜色。

### 消息 {#message-tab}

![](assets/in_app_content_8.png)

默认情况下，启用了UI接管选项，该选项允许您使应用程序内消息背后的背景变暗，以强调对内容的关注。

+++更多高级格式选项

如果 **[!UICONTROL 高级格式模式]** 开，您可以使用以下选项进一步个性化您的消息：

* **[!UICONTROL 自定义手势]**：用于自定义用户轻扫交互的内容。 如果选择了“消除”，则可以添加自定义交互事件和/或目标目标。

* **[!UICONTROL 自定义UI接管]**：用于选择要在背景中显示的颜色及其不透明度。

* **[!UICONTROL 自定义大小]**：用于调整应用程序内通知的宽度和高度。

* **[!UICONTROL 自定义位置]**：用于自定义应用程序内消息在用户屏幕上的位置。 您可以更改垂直对齐和水平对齐。

* **[!UICONTROL 自定义动画]**：允许您自定义显示和解除动画，例如，如果您的应用程序内通知从用户设备的左侧或顶部显示。

* **[!UICONTROL 消息转角]**：用于通过更改 **[!UICONTROL 圆角半径]**.

+++

**相关主题：**

* [创建应用程序内消息](create-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
* [应用程序内配置](inapp-configuration.md)

## 操作方法视频{#video}

以下视频介绍了如何创作和测试应用程序内消息。

>[!VIDEO](https://video.tv.adobe.com/v/3410471?quality=12&learn=on)
