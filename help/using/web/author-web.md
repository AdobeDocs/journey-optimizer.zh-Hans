---
title: 创建 Web 页面
description: 了解如何在Journey Optimizer中创作网页并编辑其内容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1623'
ht-degree: 14%

---

# 创建 Web 页面 {#author-web}

一旦 [添加了web操作](create-web.md#create-web-campaign) 对于您的营销活动，您可以使用web设计器编辑网站的内容。

在 [!DNL Journey Optimizer], Web创作由 **Adobe Experience Cloud Visual Helper** chrome浏览器扩展。 [了解详情](web-prerequisites.md#visual-authoring-prerequisites)

>[!CAUTION]
>
>在 [!DNL Journey Optimizer] 用户界面，请确保遵循 [此部分](web-prerequisites.md).

[在此视频中了解如何创作Web营销活动](#video)

## 编辑网页内容 {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="确认要编辑的 URL"
>abstract="确认特定网页的 URL，用于编辑将应用到上面定义的 Web 表面的内容。网页必须使用 Adobe Experience Platform Web SDK 实施。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans" text="了解详情"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="输入 URL 以进行编辑"
>abstract="输入特定网页的 URL，用于编辑将应用到与规则匹配的所有页面上的内容。网页必须使用 Adobe Experience Platform Web SDK 实施。"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans" text="了解详情"

要开始创作Web营销活动，请执行以下步骤。

1. 从 **[!UICONTROL 操作]** 选项卡 [营销活动](create-web.md#create-web-campaign)，选择 **[!UICONTROL 编辑内容]**.<!--change screen with rule-->

   ![](assets/web-campaign-edit-content.png)

1. 如果您创建的页面与规则匹配，则必须输入与此规则匹配的任何URL:更改将应用于与规则匹配的所有页面。 此时会显示页面内容。

   >[!NOTE]
   >
   >如果您输入单个URL作为Web界面，则要个性化的URL已经填充。

   ![](assets/web-edit-enter-url.png)

   >[!CAUTION]
   >
   >网页必须包含 [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hans){target="_blank"}. [了解详情](web-prerequisites.md#implementation-prerequisites)

1. 单击 **[!UICONTROL 编辑网页]** 以开始创作。 此时将显示Web设计器。

   ![](assets/web-designer.png)

   >[!NOTE]
   >
   >如果尝试加载加载失败的网站，则会显示一条消息，建议您安装 [Visual Editing Helper浏览器扩展](#install-visual-editing-helper). 请参阅 [此部分](web-prerequisites.md#troubleshooting).

1. 从画布中选择任何元素，如图像、按钮、段落、文本、容器、标题、链接等。 [了解详情](#content-components)

1. 使用:

   * 用于编辑其内容、布局、插入链接或个性化等的上下文菜单。

      ![](assets/web-designer-contextual-bar.png)

   * 用于编辑、复制、删除或隐藏每个元素的右侧面板顶部的图标。

      ![](assets/web-designer-right-panel-icons.png)

   * 根据所选元素动态更改的右侧面板。 例如，您可以编辑元素的背景、排版规则、边框、大小、位置、间距、效果或内联样式。

      ![](assets/web-designer-right-panel.png)

>[!NOTE]
>
>Web内容设计器与电子邮件设计器大体相似。 了解详情 [设计内容 [!DNL Journey Optimizer]](../email/get-started-email-design.md).

## 使用组件 {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="将组件添加到网页"
>abstract="可将许多组件添加到网页，然后根据需要编辑这些组件。"

1. 从 **[!UICONTROL 组件]** 在左侧的窗格中，选择一个项目。 您可以将以下组件添加到网页中，并根据需要对其进行编辑：

   * [除法器](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [图像](../email/content-components.md#image)
   * 标题 — 使用此组件与使用 **[!UICONTROL 文本]** 组件。 [了解详情](../email/content-components.md#text)
   * 段落 — 使用此组件与使用 **[!UICONTROL 文本]** 组件。 [了解详情](../email/content-components.md#text)
   * 链接
   * [优惠决策](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. 将鼠标悬停在页面中，然后单击 **[!UICONTROL 此项前插入]** 或 **[!UICONTROL 此项后插入]** 按钮将组件附加到页面上的现有元素。

   ![](assets/web-designer-insert-components.png)

   >[!NOTE]
   >
   >要取消选择组件，请单击 **[!UICONTROL ESC]** 按钮。

1. 根据需要直接在页面内容中编辑组件。

   ![](assets/web-designer-edit-header.png)

1. 从右侧的上下文窗格中调整显示的样式，如背景、文本颜色、边框、大小、位置等。  — 具体取决于选定的组件。

   ![](assets/web-designer-header-style.png)

## 添加个性化和选件

要添加个性化，请选择一个容器，然后从显示的上下文菜单栏中选择个性化图标。 使用表达式编辑器添加更改。 [了解详情](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

使用 **[!UICONTROL 优惠决策]** 插入组件 [选件](../offers/get-started/starting-offer-decisioning.md) 到您的网页中。 该过程与 [向电子邮件添加选件](../email/add-offers-email.md). 它将利用决策管理来选择最佳选件，以提供给您的客户。

![](assets/web-designer-offer.png)

## 管理修改 {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="轻松管理所有更改"
>abstract="使用此窗格，您可以浏览和管理您添加到网页的所有调整和样式。"

您可以轻松管理您添加到网页的所有组件、调整和样式。

1. 选择 **[!UICONTROL 修改]** 图标以在左侧显示相应的窗格。

   ![](assets/web-designer-modifications-pane.png)

1. 您可以查看对页面所做的每项更改。

1. 选择不需要的修改并单击删除图标以将其删除。

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >删除某个操作时请务必小心，因为该操作可能会影响后续操作。

1. 使用 **[!UICONTROL 更多操作]** 按钮 **[!UICONTROL 修改]** 窗格以同时删除所有修改。

   ![](assets/web-designer-delete-modifications.png)

1. 从 **[!UICONTROL 更多操作]** 菜单，您也只能删除无效的修改，即被其他更改覆盖的更改。 例如，如果修改文本的颜色，然后删除该文本，则颜色修改将无效，因为该文本不再存在。

1. 您还可以使用 **[!UICONTROL 撤消/重做]** 按钮。

   ![](assets/web-designer-undo-redo.png)

   单击并按住按钮可在 **[!UICONTROL 撤消]** 和 **[!UICONTROL 重做]** 选项。 然后，单击按钮本身以应用所需的操作。

## 使用点击跟踪 {#use-click-tracing}

Web设计器中的这项功能允许您选择网站的任何元素并跟踪该元素的点击。

营销活动上线后，您可以检查营销活动Web报表中每个元素的点击次数。 此信息对于改善网站用户体验非常有用。 例如，如果 [网站报告](../reports/campaign-global-report.md#web-tab) 显示许多用户单击的某个元素实际上不可点击，您可能想要添加指向该元素的链接。

1. 在页面中选择一个元素，然后选择 **[!UICONTROL 单击跟踪元素]** 中。

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >可以选择任何项目（无论是否可点击）。

1. 相应的跟踪操作会自动显示在 **[!UICONTROL 点击跟踪]** 窗格。

   ![](assets/web-designer-click-track-pane.png)

1. 添加有意义的标签以管理所有跟踪的元素并在报表中轻松查找它们。 的 **[!UICONTROL CSS选择器]** 字段中显示了用于查找选定元素的信息。

1. 重复上述步骤，以根据需要选择任意数量的其他元素进行点击跟踪。 相应的操作都列在左窗格中。

   ![](assets/web-designer-click-tracking-actions.png)

1. 要删除元素上的点击跟踪，请选择相应的删除图标。

活动活动后，即可查看营销活动报表 **[!UICONTROL Web]** 选项卡来比较展示次数、点击率和按元素的点击次数。 [了解详情](../reports/campaign-global-report.md#web-tab)

## 在Web设计器中导航 {#navigate-web-designer}

### 使用痕迹导航 {#breadcrumbs}

1. 从画布中选择任意元素。

1. 单击 **[!UICONTROL 展开/折叠痕迹导航]** 按钮来快速显示有关选定元素的信息。

   ![](assets/web-designer-breadcrumbs.png)

1. 将鼠标悬停在痕迹导航上时，编辑器中会高亮显示相应的元素。

1. 使用它，您可以轻松导航到可视编辑器中的任何父元素、同级元素或子元素。

### 交换到浏览模式 {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="使用浏览模式"
>abstract="在此模式下，您可以从要个性化的选定表面导航到确切的页面。"

您可以从默认 **[!UICONTROL 设计]** 模式 **[!UICONTROL 浏览]** 模式。

![](assets/web-designer-browse-mode.png)

从 **[!UICONTROL 浏览]** 模式下，您可以从要个性化的选定表面导航到确切的页面。

当处理身份验证后或特定URL开头不可用的页面时，此插件特别有用。 例如，您将能够进行身份验证，导航到帐户页面或购物车页面，然后切换回 **[!UICONTROL 设计]** 模式来执行对所需页面所做的更改。

### 更改设备大小 {#change-device-size}

您可以将Web设计器显示的设备大小更改为预定义的大小，例如 **[!UICONTROL 平板电脑]** 或 **[!UICONTROL 移动设备横向]**，或通过输入所需的像素数定义自定义大小。

您还可以将缩放焦点从25%更改为400%。

![](assets/web-designer-device.png)

更改设备大小的功能专为在各种设备、窗口和屏幕大小上均能正常呈现的响应式网站而设计。 响应式网站自动调整和适应任意屏幕大小，包括台式机、笔记本电脑、平板电脑或手机。

>[!CAUTION]
>
>您可以编辑具有特定设备大小的Web体验。 但是，只要选择器相同，这些更改就会应用于所有大小和设备，而不仅仅是您正在使用的设备大小。 同样，在普通桌面视图中编辑体验时，会将更改应用于所有屏幕大小，而不仅仅是桌面视图。
>
>目前， [!DNL Journey Optimizer] 不支持特定于设备大小的页面更改。 这意味着，例如，如果您有一个单独的移动设备网站，且网站结构各不相同，则应在其他营销活动中对移动设备网站进行特定更改。

## 测试Web营销活动 {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="预览 Web 体验"
>abstract="模拟您将获得的 Web 体验。"

要显示已修改的Web体验的预览，请执行以下步骤。

>[!CAUTION]
>
>您必须具有测试用户档案，以模拟将向他们提供哪些选件。 了解如何 [创建测试用户档案](../segment/creating-test-profiles.md).

1. 从Web营销活动编辑内容屏幕中，选择 **[!UICONTROL 模拟内容]**.

   <!--![](assets/web-designer-simulate.png)-->

   ![](assets/web-campaign-simulate.png)

1. 单击 **[!UICONTROL 管理测试用户档案]** 选择一个或多个测试用户档案。
1. 将显示已修改网页的预览。

   ![](assets/web-designer-preview.png)

1. 您还可以在默认浏览器中打开测试URL，或复制测试URL以将其粘贴到任何浏览器中。 这样，您就可以与团队和利益相关方共享该链接，在营销活动开始之前，他们将能够在任何浏览器中预览新的Web体验。

   >[!NOTE]
   >
   >复制测试URL时，显示的内容是在中生成内容模拟时用于测试用户档案的个性化内容 [!DNL Journey Optimizer].

## 操作方法视频{#video}

以下视频演示如何在 [!DNL Journey Optimizer] 营销活动。

>[!VIDEO](https://video.tv.adobe.com/v/3418803/?quality=12&learn=on)
