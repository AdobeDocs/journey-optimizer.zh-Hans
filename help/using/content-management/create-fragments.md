---
solution: Journey Optimizer
product: journey optimizer
title: 创建片段
description: 了解如何创建片段以在Journey Optimizer营销活动和历程中重用内容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: da3ffe9c-a244-4246-b4b5-a3a1d0508676
source-git-commit: c843ca5bda10aa5f3ee8a676630d78c5ec092b14
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 13%

---

# 创建片段 {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="选择可视类型"
>abstract="创建独立的可视片段，以便可在历程或营销活动的电子邮件中或内容模板中重用您的内容。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html?lang=zh-Hans" text="将可视片段添加到电子邮件"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="选择表达式类型"
>abstract="创建独立的表达式片段，以便可在多个历程和营销活动中重用您的内容。在使用个性化编辑器时，可利用已在当前沙盒上创建的所有表达式片段。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html?lang=zh-Hans" text="利用表达式片段"

片段可以从头开始创建 **[!UICONTROL 片段]** 左侧菜单。 此外，在设计内容时，您还可以将现有内容的一部分另存为片段。 [了解如何操作](#save-as-fragment)

保存后，您的片段即可用于历程、营销策划或模板。 在历程和营销活动中构建任何内容时，您可以使用此片段。 请参阅 [添加可视片段](../email/use-visual-fragments.md) 和 [利用表达式片段](../personalization/use-expression-fragments.md)

要创建片段，请执行以下步骤。

## 定义片段的属性 {#properties}

1. 通过访问片段列表 **[!UICONTROL 内容管理]** > **[!UICONTROL 片段]** 左侧菜单。

1. 选择 **[!UICONTROL 创建片段]** 并填写片段名称和描述（如果需要）。

   ![](assets/fragment-details.png)

1. 从中选择或创建Adobe Experience Platform标记 **[!UICONTROL 标记]** 用于对片段进行分类以改进搜索的字段。 [了解如何使用统一标记](../start/search-filter-categorize.md#tags)

1. 选择片段类型： **可视片段** 或 **表达片段**. [了解有关可视化和表达式片段的更多信息](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >目前，可视化片段可用于 **电子邮件** 仅限渠道。

1. 如果要创建表达式片段，请选择要使用的代码类型： **[!UICONTROL HTML]**， **[!UICONTROL JSON]** 或 **[!UICONTROL 文本]**.

   ![](assets/fragment-expression-type.png)

1. 要为片段分配自定义或核心数据使用标签，请单击 **[!UICONTROL 管理访问权限]** 按钮来打开屏幕。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md).

1. 单击 **[!UICONTROL 创建]** 以设计片段的内容。

## 设计片段内容 {#content}

配置片段的属性后，电子邮件设计器或个性化编辑器将打开，具体取决于您创建的片段类型。

* 对于可视化片段，请根据需要编辑您的内容，就像处理历程或营销活动中的任何电子邮件一样。 [了解详情](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

* 对于表达式片段，请使用 [!DNL Journey Optimizer] 具有所有个性化和创作功能的个性化编辑器，用于构建片段内容。 [了解详情](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

内容准备就绪后，单击 **保存** 按钮。 片段随即会创建，并使用添加到片段列表中 **草稿** 状态。 您可以预览并发布它，使其在历程和营销活动中可用。

>[!NOTE]
>
>片段发布在Journey Optimizer 6月发布后的几天内逐步推出。 虽然某些用户将可以立即访问，但其他用户在环境中使用它之前可能会遇到延迟。 如果您的环境中尚未提供此增强功能，请注意，在您的历程和营销活动中使用片段不需要发布片段。

## 预览和发布片段 {#publish}

>[!NOTE]
>
>要发布片段，您必须具有 **发布片段** 相关权限。 [了解有关权限的更多信息](../administration/ootb-permissions.md)

如果您的片段已准备好上线，您可以预览和发布它以使其可在您的历程和营销活动中使用。 为此，请执行以下步骤：

1. 设计其内容后返回片段创建屏幕，或从片段列表中将其打开。

1. 片段的预览位于 **标记** 字段，用于检查其渲染。 如果您需要进行任何更改，请单击 **编辑** 按钮来打开电子邮件设计器或个性化编辑器，具体取决于片段类型。

   ![](assets/fragment-preview.png)

1. 单击 **Publish** 按钮以发布片段。

   如果片段在实时历程或营销策划中使用，将打开消息以通知您。 单击 **查看更多** 用于访问引用它的历程和/或营销活动列表的链接。 [了解如何浏览片段的引用](../content-management/manage-fragments.md#explore-references)

   单击 **确认** 以在使用该片段的实时历程/营销活动中发布并更新该片段。

   ![](assets/fragment-publish.png){width="70%" align="center"}

片段现在为 **实时**，并在中构建任何内容时变得可用 [!DNL Journey Optimizer] 电子邮件设计工具或个性化编辑器：

* [了解如何使用可视化片段](../email/use-visual-fragments.md)
* [了解如何使用表达式片段](../personalization/use-expression-fragments.md)
