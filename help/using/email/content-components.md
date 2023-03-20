---
solution: Journey Optimizer
product: journey optimizer
title: 使用电子邮件设计器内容组件
description: 了解如何在电子邮件中使用内容组件
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 组件，电子邮件设计器，编辑器，电子邮件
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: 08d842a877ed52349eef5a901aaf9c75187c69d3
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 1%

---

# 使用Email Designer内容组件 {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="关于内容组件"
>abstract="内容组件是空内容占位符，您可以使用这些占位符创建电子邮件的布局。"

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="关于内容组件"
>abstract="内容组件是空内容占位符，您可以使用这些占位符创建登陆页面的布局。"

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="关于内容组件"
>abstract="内容组件是空内容占位符，您可以使用它们创建片段的布局。"

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="关于内容组件"
>abstract="内容组件是空内容占位符，您可以使用这些占位符创建模板的布局。"

创建电子邮件内容时， **[!UICONTROL 内容组件]** 允许您使用原始组件进一步个性化电子邮件，一旦将原始组件放入电子邮件中，即可对其进行编辑。

您可以在一个或多个结构组件中添加所需数量的内容组件，这些组件可定义电子邮件的布局。

## 添加内容组件 {#add-content-components}

要向电子邮件中添加内容组件并根据需要对其进行调整，请执行以下步骤。

1. 在Email Designer中，使用现有内容或拖放 **[!UICONTROL 结构部件]** ，以定义电子邮件的布局。 [了解如何操作](content-from-scratch.md)

1. 访问 **[!UICONTROL 内容组件]** 部分，从Email Designer左窗格中选择相应的按钮。

   ![](assets/email_designer_content_components.png)

1. 将您选择的内容组件拖放到相关结构组件中。

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >可以将多个组件添加到单个结构组件中，并添加到结构组件的每一列中。

1. 使用 **[!UICONTROL 组件设置]** 窗格。 例如，您可以更改每个组件的文本样式、内边距或边距。 [了解有关对齐和填充的更多信息](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

## 容器 {#container}

您可以添加一个简单的容器，在其中可以添加其他内容组件。 这允许您对容器应用特定样式，该样式将与内部使用的组件不同。

例如，添加 **[!UICONTROL 容器]** 组件，然后添加 [按钮](#button) 组件。 您可以为容器使用特定背景，为按钮使用另一个背景。

![](assets/email_designer_container_component.png)

## 按钮 {#button}

使用 **[!UICONTROL 按钮]** 组件将一个或多个按钮插入到电子邮件中，并将电子邮件受众重定向到其他页面。

1. 从 **[!UICONTROL 内容组件]**，拖放 **[!UICONTROL 按钮]** 组件 **[!UICONTROL 结构部件]**.

1. 单击您新添加的按钮以个性化文本并有权访问 **[!UICONTROL 组件设置]** 在Email Designer右窗格中。

   ![](assets/email_designer_button_component.png)

1. 在 **[!UICONTROL 链接]** 字段中，添加您希望在单击按钮时重定向到的URL。

1. 选择如何通过 **[!UICONTROL Target]** 下拉列表：

   * **[!UICONTROL 无]**:在点击链接的同一帧中打开该链接（默认）。
   * **[!UICONTROL 空白]**:在新窗口或选项卡中打开链接。
   * **[!UICONTROL Self]**:在点击链接的同一帧中打开该链接。
   * **[!UICONTROL 父项]**:在父框架中打开链接。
   * **[!UICONTROL 顶部]**:在窗口的完整正文中打开链接。

   ![](assets/email_designer_button_link.png)

1. 您可以通过更改样式属性(例如 **[!UICONTROL 边框]**, **[!UICONTROL 大小]**, **[!UICONTROL 边距]**&#x200B;等。 从 **[!UICONTROL 组件设置]** 中。

## 文本 {#text}

使用 **[!UICONTROL 文本]** 组件，以在电子邮件中插入文本，并调整样式（边框、大小、内边距等） 使用 **[!UICONTROL 组件设置]** 中。

![](assets/email_designer_text_component.png)

1. 从 **[!UICONTROL 内容组件]**，拖放 **[!UICONTROL 文本]** 组件 **[!UICONTROL 结构部件]**.

1. 单击您新添加的组件以个性化文本，并有权访问 **[!UICONTROL 组件设置]** 在Email Designer的右侧窗格中。

1. 使用以下工具栏中的选项更改文本：

   ![](assets/email_designer_27.png)

   * **[!UICONTROL 更改文本样式]**:在文本中应用粗体、斜体、下划线或者直线。
   * **更改对齐方式**:在文本的左对齐、右对齐、居中对齐或两端对齐之间进行选择。
   * **[!UICONTROL 创建列表]**:在文本中添加项目符号或编号列表。
   * **[!UICONTROL 设置标题]**:在文本中最多添加6个标题级别。
   * **字体大小**:以像素为单位选择文本的字体大小。
   * **[!UICONTROL 编辑图像]**:向文本组件中添加图像或资产。 [了解有关资产管理的更多信息](assets-essentials.md)
   * **[!UICONTROL 显示源代码]**:显示文本的源代码。 无法修改。
   * **[!UICONTROL 复制]**:添加文本组件的副本。
   * **[!UICONTROL 删除]**:从电子邮件中删除选定的文本组件。
   * **[!UICONTROL 添加个性化]**:添加个性化字段以自定义用户档案数据的内容。 [了解有关内容个性化的更多信息](../personalization/personalize.md)
   * **[!UICONTROL 启用条件内容]**:添加条件内容，以将组件内容调整为目标用户档案。 [进一步了解动态内容](../personalization/get-started-dynamic-content.md)

1. 调整其他样式属性，如文本颜色、字体系列、边框、内边距、边距等。 从 **[!UICONTROL 组件设置]** 中。

## 除法器 {#divider}

使用 **[!UICONTROL 除法器]** 用于插入划分线以组织电子邮件的布局和内容的组件。

您可以调整样式属性，如 **[!UICONTROL 组件设置]** 中。

![](assets/email_designer_divider.png)

## HTML {#HTML}

使用 **[!UICONTROL HTML]** 组件来复制粘贴现有HTML的不同部分。 这样，您就可以创建免费的模块化HTML组件来重复使用某些外部内容。

1. 从 **[!UICONTROL 内容组件]**，拖放 **[!UICONTROL HTML]** 组件 **[!UICONTROL 结构部件]**.

1. 单击新添加的组件，然后选择 **[!UICONTROL 显示源代码]** 从上下文工具栏添加HTML。

   ![](assets/email_designer_html_component.png)

1. 复制并粘贴要添加到电子邮件的HTML代码，然后单击 **[!UICONTROL 保存]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>为了使外部内容与Email Designer兼容，Adobe建议从头开始创建消息，并将现有电子邮件中的内容复制到组件中。

## 图像 {#image}

使用 **[!UICONTROL 图像]** 组件将来自计算机的图像文件插入到电子邮件内容中。

1. 从 **[!UICONTROL 内容组件]**，拖放 **[!UICONTROL 图像]** 组件 **[!UICONTROL 结构部件]**.

1. 单击 **[!UICONTROL 浏览]** ，以从资产中选择图像文件。

   要了解 [!DNL Assets Essentials]，请参阅 [Adobe Experience Manager Assets Essentials文档](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target="_blank"}.

1. 单击新添加的组件，然后使用 **[!UICONTROL 组件设置]** 窗格：

   * **[!UICONTROL 图像标题]** 用于为图像定义标题。
   * **[!UICONTROL 替换文本]** 用于定义链接到图像的标题。 此属性对应于altHTML属性。

   ![](assets/email_designer_10.png)

1. 调整其他样式属性，如边距、边框等。 或添加链接，以将受众重定向到 **[!UICONTROL 组件设置]** 中。

## 社交 {#social}

使用 **[!UICONTROL 社交]** 组件将指向社交媒体页面的链接插入到电子邮件内容中。

1. 从 **[!UICONTROL 内容组件]**，拖放 **[!UICONTROL 社交]** 组件 **[!UICONTROL 结构部件]**.

1. 单击新添加的组件。

1. 在 **[!UICONTROL 社交]** 字段 **[!UICONTROL 组件设置]** 窗格，选择要添加或删除的社交媒体。

   ![](assets/email_designer_20.png)

1. 通过专用字段选择图标的大小。

1. 单击每个社交媒体图标以配置 **[!UICONTROL URL]** 受众将被重定向到的页面。

   ![](assets/email_designer_21.png)

1. 您还可以根据需要在 **[!UICONTROL 图像]** 字段。

1. 调整其他样式属性，如样式、边距、边框等。 从 **[!UICONTROL 组件设置]** 中。

## 优惠决策 {#offer-decision}

使用 **[!UICONTROL 优惠决策]** 组件。 的 [决策管理](../offers/get-started/starting-offer-decisioning.md) 引擎将选择要交付给客户的最佳选件。

了解如何在 [此部分](add-offers-email.md).

