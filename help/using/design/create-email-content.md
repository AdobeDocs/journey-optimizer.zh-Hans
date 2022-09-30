---
title: 在Journey Optimizer中设计电子邮件
description: 了解如何从头开始设计电子邮件内容
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 9593ea40853221e0eec45f30f7635d8a116b03c1
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# 从零开始 {#create-email-content}

>[!CONTEXTUALHELP]
>id="ac_structure_components_email"
>title="关于结构组件"
>abstract="结构组件可定义电子邮件的布局。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_landing_page"
>title="关于结构组件"
>abstract="结构组件可定义登陆页面的布局。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_fragment"
>title="关于结构组件"
>abstract="结构组件定义片段的布局。"

>[!CONTEXTUALHELP]
>id="ac_structure_components_template"
>title="关于结构组件"
>abstract="结构组件定义模板的布局。"


>[!CONTEXTUALHELP]
>id="ac_edition_columns_email"
>title="定义电子邮件列"
>abstract="Email Designer允许您通过定义列结构轻松定义电子邮件的布局。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_landing_page"
>title="定义登陆页面列"
>abstract="Email Designer允许您通过定义列结构轻松定义登陆页面的布局。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_fragment"
>title="定义片段列"
>abstract="Email Designer允许您通过定义列结构轻松定义片段的布局。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns_template"
>title="定义模板列"
>abstract="Email Designer允许您通过定义列结构轻松定义模板的布局。"


通过Email Designer，可轻松定义电子邮件的结构。 通过通过简单的拖放操作添加和移动结构元素，您可以在几秒内设计电子邮件的形状。

要开始使用电子邮件设计器构建电子邮件内容，请执行以下步骤：

1. 从Email Designer主页中，选择 **[!UICONTROL 从头开始设计]** 选项。

   ![](assets/email_designer.png)

1. 通过拖放开始设计电子邮件内容 **[!UICONTROL 结构部件]** 定义电子邮件的布局。

   >[!NOTE]
   >
   >请注意，列堆叠与所有电子邮件程序不兼容。 不支持时，不会堆叠列。
   >
   >将组件放入电子邮件中后，除非内部已放置内容组件或片段，否则将无法移动或删除组件。

   ![](assets/email_designer_2.png)

1. 添加任意数量的 **[!UICONTROL 结构部件]** 根据需要。

   选择 **[!UICONTROL n:n列]** 组件来定义所选的列数（在3到10之间）。 您还可以通过在每列底部移动箭头来定义每列的宽度。

   >[!NOTE]
   >
   >每个列大小不能低于结构组件总宽度的10%。 无法删除不为空的列。

1. 从 **[!UICONTROL 内容组件]** 下拉列表中，您可以添加任意数量的 **[!UICONTROL 内容组件]** 根据您在结构组件中的需要。 [了解有关内容组件的更多信息](content-components.md).

   ![](assets/email_designer_3.png)

1. 每个组件都可通过 **[!UICONTROL 组件设置]** 中。 例如，您可以更改组件的文本样式、内边距或边距。 [了解有关对齐和填充的更多信息](adjusting-vertical-alignment-and-padding.md).

   ![](assets/email_designer_4.png)

1. 从 **[!UICONTROL 资产选取器]**，则可以直接在 **[!UICONTROL 资产库]** 电子邮件。 [了解有关资产管理的更多信息](assets-essentials.md).

   双击包含您的资产的文件夹，然后将要添加的资产拖放到电子邮件中。

   ![](assets/email_designer_5.png)

1. 添加个性化字段以自定义用户档案数据的内容。 [了解有关内容个性化的更多信息](../personalization/personalize.md).

   ![](assets/email_designer_6.png)

1. 添加动态内容以根据条件规则将内容调整为目标用户档案。 [动态内容入门](../personalization/get-started-dynamic-content.md).

   ![](assets/email_designer_dynamic-content.png)

1. 在 **[!UICONTROL 链接]** 选项卡，检查要跟踪的内容的所有URL列表。 您可以修改 **[!UICONTROL 跟踪类型]**, **[!UICONTROL 标签]** 和 **[!UICONTROL 标记]** （如果需要）。

   ![](assets/email_designer_7.png)

   >[!NOTE]
   >
   >了解有关 [本页](message-tracking.md).

1. 如果需要，您可以切换到代码编辑器，以通过单击 **[!UICONTROL 切换到代码编辑器]** 中。 有关代码编辑器的更多信息，请参阅 [本页](code-content.md#).

   >[!NOTE]
   >
   >切换到代码编辑器后，您将无法对此电子邮件使用可视设计器。

   ![](assets/email_designer_26.png)

1. 单击 **[!UICONTROL 显示预览]** 以检查电子邮件渲染。 您可以选择桌面视图或移动设备视图。

   有关如何预览电子邮件的更多信息，请参阅 [本页](preview.md).

   ![](assets/email_designer_8.png)

1. 准备好电子邮件后，单击 **[!UICONTROL 保存并关闭]**.

