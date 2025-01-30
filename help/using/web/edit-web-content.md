---
title: 编辑 Web 内容
description: 了解如何在Journey Optimizer中创作网页并编辑其内容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 503bedc30c35305537c62f9452f4a2dc07424523
workflow-type: tm+mt
source-wordcount: '1068'
ht-degree: 16%

---

# 编辑 Web 内容 {#edit-web-content}

将Web体验](create-web.md#create-web-experience)添加到历程或营销活动后，即可使用Web设计器编辑网站的内容。[

[在此视频中了解如何创作Web营销活动](#video)

在[!DNL Journey Optimizer]中，Web创作由&#x200B;**Adobe Experience Cloud Visual Helper** Chrome浏览器扩展提供支持。 [了解详情](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>要在[!DNL Journey Optimizer]用户界面中访问和创作网页，请确保遵循[本节](web-prerequisites.md)中列出的先决条件。

访问以下部分以了解有关每个主题的更多信息：

* [管理修改](manage-web-modifications.md)

* [监测 Web 活动](monitor-web-experiences.md)

## 使用 Web 设计器 {#work-with-web-designer}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="确认要编辑的 URL"
>abstract="确认特定网页的 URL，用于编辑将应用到上面定义的 Web 配置的内容。网页必须使用 Adobe Experience Platform Web SDK 实施。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans" text="了解详情"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="输入 URL 以进行编辑"
>abstract="输入特定网页的 URL，用于编辑将应用到与规则匹配的所有页面上的内容。网页必须使用 Adobe Experience Platform Web SDK 实施。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans" text="了解详情"

要开始创作Web体验，请执行以下步骤。

1. 从历程中的营销活动或Web体验活动的&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL 编辑内容]**。<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. 如果创建的页面与规则匹配，则必须输入与此规则匹配的任何URL：更改将应用于与规则匹配的所有页面。 此时将显示页面内容。

   >[!NOTE]
   >
   >如果您输入单个URL作为Web配置，则已填充要个性化的URL。

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >该网页必须包含[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"}。 [了解详情](web-prerequisites.md#implementation-prerequisites)

1. 单击&#x200B;**[!UICONTROL 编辑网页]**&#x200B;开始创作。 此时将显示Web设计器。

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >如果尝试加载无法加载的网站，则会显示一条消息，建议您安装[可视化编辑帮助程序浏览器扩展](#install-visual-editing-helper)。 请参阅[本节](web-prerequisites.md#troubleshooting)中的疑难解答提示。

1. 从画布中选择任意元素，如图像、按钮、段落、文本、容器、标题、链接等。 [了解详情](#content-components)

1. 使用：

   * 上下文菜单，用于编辑其内容、布局、插入链接或个性化等。

     ![](assets/web-designer-contextual-bar.png)

   * 右侧面板顶部的图标用于编辑、复制、删除或隐藏每个元素。

     ![](assets/web-designer-right-panel-icons.png)

   * 根据所选元素动态更改的右侧面板。 例如，您可以编辑元素的背景、排版规则、边框、大小、位置、间距、效果或内联样式。

     ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>Web内容设计器主要类似于电子邮件设计器。 了解有关[使用 [!DNL Journey Optimizer]](../email/get-started-email-design.md)设计内容的更多信息。

## 使用组件 {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="将组件添加到网页"
>abstract="可将许多组件添加到网页，然后根据需要编辑这些组件。"

1. 从左侧的&#x200B;**[!UICONTROL 组件]**&#x200B;窗格中，选择一个项。 您可以将以下组件添加到网页中，并根据需要对其进行编辑：

   * [分隔条](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [图像](../email/content-components.md#image)
   * 标题 — 使用此组件类似于在电子邮件设计器中使用&#x200B;**[!UICONTROL Text]**&#x200B;组件。 [了解详情](../email/content-components.md#text)
   * 段落 — 使用此组件类似于在电子邮件设计器中使用&#x200B;**[!UICONTROL Text]**&#x200B;组件。 [了解详情](../email/content-components.md#text)
   * 链接

   ![](assets/web-designer-components.png)

1. 将鼠标悬停在页面中并单击&#x200B;**[!UICONTROL 此项前插入]**&#x200B;或&#x200B;**[!UICONTROL 此项后插入]**&#x200B;按钮以将组件附加到页面上的现有元素。

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >要取消选择组件，请单击画布顶部显示的上下文蓝色横幅中的&#x200B;**[!UICONTROL ESC]**&#x200B;按钮。

1. 根据需要直接在页面的内容中编辑组件。

   ![](assets/web-designer-edit-header.png)

1. 调整从右侧的上下文窗格显示的样式，例如背景、文本颜色、边框、大小、位置等。  — 取决于所选的组件。

   ![](assets/web-designer-header-style.png)

## 添加个性化

要添加个性化，请选择一个容器，然后从显示的上下文菜单栏中选择个性化图标。 使用个性化编辑器添加更改。 [了解详情](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

## 在Web设计器中导航 {#navigate-web-designer}

本节详细介绍在Web设计器中导航的各种方式。 要查看和管理添加到您的Web体验的修改，请参阅[此部分](manage-web-modifications.md)。

### 使用痕迹导航 {#breadcrumbs}

1. 从画布中选择任意元素。

1. 单击屏幕左下方的&#x200B;**[!UICONTROL 展开/折叠痕迹导航]**&#x200B;按钮，可快速显示有关所选元素的信息。

   ![](assets/web-designer-breadcrumbs.png)

1. 将鼠标悬停在痕迹导航上时，编辑器中会突出显示相应的元素。

1. 使用该编辑器，您可以轻松导航到可视编辑器中的任何父元素、同级元素或子元素。

### 切换到浏览模式 {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="使用浏览模式"
>abstract="在此模式下，您可以从要个性化的选定配置导航到确切的页面。"

您可以使用专用按钮将默认&#x200B;**[!UICONTROL 设计]**&#x200B;模式交换为&#x200B;**[!UICONTROL 浏览]**&#x200B;模式。

![](assets/web-designer-browse-mode.png)

从&#x200B;**[!UICONTROL 浏览]**&#x200B;模式中，您可以导航到要个性化的选定配置中的相应页面。

在处理身份验证后的页面或在特定URL处从头开始不可用的页面时，此插件特别有用。 例如，您将能够进行身份验证，导航到您的帐户页面或购物车页面，然后切换回&#x200B;**[!UICONTROL 设计]**&#x200B;模式，以便在所需页面上执行更改。

使用&#x200B;**[!UICONTROL 浏览]**&#x200B;模式还允许您在创作单页应用程序时浏览网站的所有视图。 [了解详情](web-spa.md)

### 更改设备大小 {#change-device-size}

您可以将Web设计器显示的设备大小更改为预定义的大小，如&#x200B;**[!UICONTROL 平板电脑]**&#x200B;或&#x200B;**[!UICONTROL 移动设备横向]**，或者通过输入所需的像素数来定义自定义大小。

您还可以将缩放焦点从25%更改为400%。

![](assets/web-designer-device.png)

更改设备大小的功能专为可在各种设备、窗口和屏幕大小上呈现出良好效果的响应式网站而设计。 响应式网站会自动调整和适应任何屏幕大小，包括台式机、笔记本电脑、平板电脑或手机。

>[!CAUTION]
>
>您可以编辑具有特定设备大小的Web体验。 但是，只要选择器相同，这些更改就会应用于所有大小和设备，而不仅仅是您正在使用的设备大小。 同样，在普通桌面视图中编辑体验会将更改应用于所有屏幕大小，而不仅仅是桌面视图。
>
>当前，[!DNL Journey Optimizer]不支持特定于设备大小的页面更改。 这意味着，例如，如果您具有一个单独的移动网站并具有单独的网站结构，则您应该针对不同营销活动中的移动网站进行更改。

## 操作方法视频{#video}

以下视频说明如何在[!DNL Journey Optimizer]营销活动中使用Web设计器创作Web体验。

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)