---
solution: Journey Optimizer
product: journey optimizer
title: 在Journey Optimizer中从头开始设计内容
description: 了解如何从头开始设计内容
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 内容，编辑器，电子邮件，开始
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 4ce8573aa76ceae807d404e736b2d780f687aa56
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 从头开始设计内容 {#content-from-scratch}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="添加结构组件"
>abstract="结构组件定义电子邮件的版面。拖放 **结构** 组件，以开始设计电子邮件内容。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="添加结构组件"
>abstract="结构组件定义登陆页面的版面。拖放 **结构** 组件，以开始设计登陆页面的内容。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="添加结构组件"
>abstract="结构组件定义片段的版面。拖放 **结构** 组件，以开始设计片段的内容。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="添加结构组件"
>abstract="结构组件定义模板的版面。拖放 **结构** 组件来开始设计模板的内容。"


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="定义电子邮件列"
>abstract="Email Designer允许您通过选择列结构轻松定义电子邮件的布局。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="定义登陆页面列"
>abstract="通过设计器，您可以通过选择列结构轻松定义登陆页面的布局。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="定义片段列"
>abstract="设计器允许您通过选择列结构轻松定义片段的布局。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="定义模板列"
>abstract="Designer允许您通过选择列结构轻松定义模板的布局。"


使用Adobe Journey Optimizer Designer轻松定义内容的结构。 通过通过简单的拖放操作添加和移动结构元素，您可以在几秒内设计内容的形状。

要开始构建内容，请执行以下步骤：

1. 从Designer主页中，选择 **[!UICONTROL 从头开始设计]** 选项。

   ![](assets/email_designer.png)

1. 通过拖放开始设计内容 **[!UICONTROL 结构]** 到画布中以定义电子邮件的布局。

   >[!NOTE]
   >
   >堆叠列与所有电子邮件程序不兼容。 不支持时，不会堆叠列。

   <!--Once placed in the email, you cannot move nor remove your components unless there is already a content component or a fragment placed inside. This is not true in AJO - TBC?-->

1. 添加任意数量的 **[!UICONTROL 结构]** 根据需要，在右侧的专用窗格中编辑其设置。

   ![](assets/email_designer_structure_components.png)

   选择 **[!UICONTROL n:n列]** 组件来定义所选的列数（在3到10之间）。 您还可以通过在每列底部移动箭头来定义每列的宽度。

   >[!NOTE]
   >
   >每个列大小不能低于结构组件总宽度的10%。 无法删除不为空的列。

1. 展开 **[!UICONTROL 内容]** ，并将所需数量的元素添加到一个或多个结构组件中。 [了解有关内容组件的更多信息](content-components.md)

1. 可使用 **[!UICONTROL 设置]** 或 **[!UICONTROL 样式]** 选项卡。 例如，您可以更改每个组件的文本样式、内边距或边距。 [了解有关对齐和填充的更多信息](alignment-and-padding.md)

   ![](assets/email_designer_structure_component.png)

1. 从 **[!UICONTROL 资产选取器]**，您可以直接选择存储在 **[!UICONTROL 资产库]**. [了解有关资产管理的更多信息](assets-essentials.md)

   双击包含您的资产的文件夹。 将它们拖放到结构组件中。

   ![](assets/email_designer_asset_picker.png)

1. 插入个性化字段以根据用户档案属性、区段成员关系、上下文属性等自定义您的内容。 [了解有关内容个性化的更多信息](../personalization/personalize.md)

   ![](assets/email_designer_personalization.png)

1. 单击 **[!UICONTROL 启用条件内容]** 以根据条件规则添加动态内容并将内容调整为目标用户档案。 [动态内容入门](../personalization/get-started-dynamic-content.md)

   ![](assets/email_designer_dynamic-content.png)

1. 单击 **[!UICONTROL 链接]** 选项卡，以显示要跟踪的内容的所有URL。 您可以修改 **[!UICONTROL 跟踪类型]** 或 **[!UICONTROL 标签]** 添加 **[!UICONTROL 标记]** （如果需要）。 [了解有关链接和跟踪的更多信息](message-tracking.md)

   ![](assets/email_designer_links.png)

1. 如果需要，您可以通过单击 **[!UICONTROL 切换到代码编辑器]** 从顶部 **更多** 按钮。 [了解有关代码编辑器的更多信息](code-content.md)

   ![](assets/email_designer_switch-to-code.png)

   >[!CAUTION]
   >
   >切换到代码编辑器后，无法还原到此内容的可视设计器。

1. 内容准备就绪后，单击 **[!UICONTROL 模拟内容]** 按钮来检查渲染。 您可以选择桌面视图或移动设备视图。 [了解有关预览电子邮件的更多信息](preview.md)

   ![](assets/email_designer_simulate_content.png)

1. 内容准备就绪后，单击 **[!UICONTROL 保存]**.

