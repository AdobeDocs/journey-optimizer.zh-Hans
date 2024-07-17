---
title: 设计应用程序内内容
description: 了解如何在Journey Optimizer中设计应用程序内内容
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内、消息、设计、格式
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1154'
ht-degree: 28%

---

# 设计应用程序内内容 {#design-content}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_content"
>title="定义应用程序内内容"
>abstract="自定义应用程序内消息的内容和样式。您还可以添加媒体和操作按钮，提升消息的吸引力和有效性。"

您可以编辑应用程序内内容以配置体验选项：

* 在&#x200B;**[!UICONTROL 营销活动]**&#x200B;中，从&#x200B;**[!UICONTROL 操作]**&#x200B;菜单中，要配置消息内容，请单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮。

  ![](assets/edit-in-app-content.png)

* 在&#x200B;**[!UICONTROL 历程]**&#x200B;中，从应用程序内&#x200B;**[!UICONTROL 操作]**&#x200B;的高级菜单中，可以使用&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮开始设计内容。

  ![](assets/design_inapp_journey.png)

**[!UICONTROL 高级格式]**&#x200B;切换可激活其他选项以自定义体验。

创建应用程序内消息，并定义其内容并对其进行个性化后，即可查看和激活该消息。 然后，将根据营销活动计划发送通知。 请参阅[此页面](send-in-app.md)以了解详情。

## 消息布局 {#message-layout}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_message_layout"
>title="定义应用程序内内容"
>abstract="消息版面为您提供了常用模板来构建消息。自定义版面提供了用于上传或撰写自定义 HTML 消息的选项。"

从&#x200B;**[!UICONTROL 消息布局]**&#x200B;部分中，根据您的消息传送需求选择四个不同的布局选项之一。

![](assets/in_app_web_design_1.png)

* **[!UICONTROL 全屏]**：此类型的布局覆盖受众设备的整个屏幕。

  此选项支持媒体（图像、视频）、文本和按钮组件。

* **[!UICONTROL 模式]**：此布局显示在大型警报样式窗口中，背景中仍可看到您的应用程序。

  此选项支持媒体（图像、视频）、文本和按钮组件。

* **[!UICONTROL 横幅]**：此类型的布局显示为本机操作系统警报消息。

  您只能向消息添加&#x200B;**[!UICONTROL 标头]**&#x200B;和&#x200B;**[!UICONTROL 正文]**。

* **[!UICONTROL 自定义]**：自定义消息模式允许您直接导入和编辑预配置的HTML消息之一。

   * 选择&#x200B;**[!UICONTROL 撰写]**&#x200B;以输入或粘贴原始HTML代码。

     使用左窗格以利用Journey Optimizer个性化功能。 有关详细信息，请参阅[此部分](../personalization/personalize.md)。

   * 选择&#x200B;**[!UICONTROL 导入]**&#x200B;以导入包含HTML内容的HTML或.zip文件。

## “内容”选项卡 {#content-tab}

从&#x200B;**Content**&#x200B;选项卡，您可以定义并个性化通知的内容和&#x200B;**关闭**&#x200B;按钮的样式。 您还可以向应用程序内通知添加媒体，并在此选项卡中添加操作按钮。

### “关闭”按钮 {#close-button}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_close"
>title="选择“关闭”按钮的样式。"
>abstract="关闭按钮部分包含用于选择消息关闭按钮变体的选项以及用于上传自定义图像的选项。"

![](assets/in_app_web_design_2.png)

选择&#x200B;**[!UICONTROL 关闭按钮]**&#x200B;的&#x200B;**[!UICONTROL 样式]**。

可用的样式包括：

* **[!UICONTROL 简单]**
* **[!UICONTROL 圆]**
* 来自媒体URL或您的Assets的&#x200B;**[!UICONTROL 自定义图像]**。

+++更多高级格式选项

如果&#x200B;**[!UICONTROL 高级格式模式]**&#x200B;已打开，则可以选中&#x200B;**[!UICONTROL 颜色]**&#x200B;选项来选择按钮的颜色和不透明度。

+++

### 媒体 {#add-media}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_media"
>title="将媒体添加到应用程序内消息中，为最终用户创造引人入胜的体验。"
>abstract="提供内容的直接链接或使用资源选择器在 Asset Essentials 中选取媒体以添加到消息中。"

**[!UICONTROL Media]**&#x200B;字段允许您向应用程序内消息添加媒体，从而为最终用户创造引人入胜的体验。

![](assets/in_app_web_design_3.png)

键入您的媒体URL或单击&#x200B;**[!UICONTROL 选择Assets]**&#x200B;图标，直接将存储在Assets库中的资源添加到应用程序内消息中。 [了解有关资产管理的更多信息](../content-management/assets.md)。
您还可以为屏幕阅读应用程序添加**[!UICONTROL 替换文本]**。

+++更多高级格式选项

如果&#x200B;**[!UICONTROL 高级格式模式]**&#x200B;已打开，您可以自定义媒体的&#x200B;**[!UICONTROL 最大高度]**&#x200B;和&#x200B;**[!UICONTROL 最大宽度]**。

+++

### 内容 {#title-body}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_content"
>title="要撰写消息，请在“标题”和“正文”字段中输入内容。"
>abstract="可以在此处添加标题和正文文本。要包含个性化令牌，请打开个性化对话框。"

若要撰写邮件，请在&#x200B;**[!UICONTROL 标头]**&#x200B;和&#x200B;**[!UICONTROL 正文]**&#x200B;字段中输入内容。

![](assets/in_app_web_design_4.png)

使用&#x200B;**[!UICONTROL Personalization]**&#x200B;图标添加个性化。 在本节](../personalization/personalize.md)中了解有关Adobe Journey Optimizer个性化编辑器[中个性化的更多信息。

+++更多高级格式选项

如果&#x200B;**[!UICONTROL 高级格式模式]**&#x200B;已打开，则可以选择&#x200B;**[!UICONTROL 标题]**&#x200B;和&#x200B;**[!UICONTROL 正文]**：

* **[!UICONTROL 字体]**
* **[!UICONTROL Pt大小]**
* **[!UICONTROL 字体颜色]**
* **[!UICONTROL 对齐方式]**
+++

### 按钮 {#add-buttons}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_buttons"
>title="添加按钮以供用户与应用程序内消息进行交互。"
>abstract="通过此部分，可将行动号召按钮添加到消息。您可以为每个按钮包含自定文本和目标。"

添加按钮以供用户与应用程序内消息进行交互。

![](assets/in_app_web_design_5.png)

要个性化您的按钮，请执行以下操作：

1. 编辑按钮#1文本（主）字段。 您还可以使用&#x200B;**[!UICONTROL Personalization]**&#x200B;图标来定义内容和个性化数据。

1. 选择您的&#x200B;**[!UICONTROL Interact事件]**，该事件定义用户与按钮交互后的按钮操作。

1. 在&#x200B;**[!UICONTROL 目标]**&#x200B;字段中输入您的Web URL或深层链接。

1. 要添加多个按钮，请单击&#x200B;**[!UICONTROL 添加按钮]**。

+++更多高级格式选项

如果&#x200B;**[!UICONTROL 高级格式模式]**&#x200B;已打开，则可以选择&#x200B;**[!UICONTROL 按钮]**：

* **[!UICONTROL 字体]**
* **[!UICONTROL Pt大小]**
* **[!UICONTROL 字体颜色]**
* **[!UICONTROL 对齐方式]**
* **[!UICONTROL 按钮样式]**
* **[!UICONTROL 半径]**
* **[!UICONTROL 按钮颜色]**

+++

## “设置”选项卡 {#settings-tab}

在&#x200B;**设置**&#x200B;选项卡中，您可以定义消息布局并预览应用程序内消息。 您还可以访问高级格式设置选项。

### 预览 {#preview-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_preview"
>title="预览应用程序内消息。"
>abstract="这是在消息发送到设备的消息摘要时将显示的预览图像。"

>[!NOTE]
>
>预览仅适用于移动设备应用程序内消息。

![](assets/in_app_content_6.png)

**[!UICONTROL 应用程序预览]**&#x200B;允许您在应用程序内消息后添加背景：

* URL链接中的媒体。

* Assets库中的资源。

* 背景颜色。

### 布局 {#layout-options}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_layout"
>title="定义应用程序内消息的消息版面。"
>abstract="此部分允许您将背景添加到应用程序内消息。这需要启用 UI 接管。"

![](assets/in_app_web_design_6.png)

**[!UICONTROL 背景图像]**&#x200B;字段允许您向应用程序内消息添加背景：

* URL链接中的媒体。

* 背景颜色。

### 消息 {#message-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_message_advanced"
>title="定义消息高级设置。"
>abstract="此部分可让您增强应用程序内内容的个性化，特别是在启用了“高级格式化”的情况下。"

![](assets/in_app_web_design_7.png)

默认情况下，启用了UI接管选项，该选项允许您使应用程序内消息背后的背景变暗，以强调对内容的关注。

+++更多高级格式选项

如果&#x200B;**[!UICONTROL 高级格式化模式]**&#x200B;已打开，您可以使用以下选项进一步个性化您的消息：

* **[!UICONTROL 自定义手势]**：允许您自定义用户滑动交互的内容。 如果选择了“消除”，则可以添加自定义交互事件和/或目标目标。

* **[!UICONTROL 自定义UI接管]**：允许您选择要在后台显示的颜色及其不透明度。

* **[!UICONTROL 自定义大小]**：允许您调整应用内通知的宽度和高度。

* **[!UICONTROL 自定义位置]**：允许您自定义应用程序内消息在用户屏幕上的位置。 您可以更改垂直对齐和水平对齐。

* **[!UICONTROL 自定义动画]**：允许您自定义显示和取消动画，例如，如果您的应用程序内通知从用户设备的左侧或顶部显示。

* **[!UICONTROL 消息圆角]**：允许您通过更改&#x200B;**[!UICONTROL 圆角半径]**&#x200B;向应用程序内通知添加圆角。

+++

**相关主题：**

* [创建应用程序内消息](create-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
* [应用程序内配置](inapp-configuration.md)

## 操作方法视频{#video}

以下视频介绍了如何创作和测试应用程序内消息。

>[!VIDEO](https://video.tv.adobe.com/v/3410471?quality=12&learn=on)
