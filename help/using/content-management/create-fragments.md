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
source-git-commit: c3513c087a05f2258e00fd4d80fdb23bedfd9188
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 14%

---

# 创建片段 {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="选择可视类型"
>abstract="创建独立的可视片段，以便可在历程或营销活动的电子邮件中或内容模板中重用您的内容。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments" text="将可视片段添加到电子邮件"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="选择表达式类型"
>abstract="创建独立的表达式片段，以便可在多个历程和营销活动中重用您的内容。在使用个性化编辑器时，可利用已在当前沙盒上创建的所有表达式片段。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/content-management/personalization/personalization-build-expressions" text="使用个性化编辑器"

可以从左侧菜单&#x200B;**[!UICONTROL 片段]**&#x200B;从头开始创建片段。 此外，在设计内容时，您还可以将现有内容的一部分另存为片段。 [了解如何操作](#save-as-fragment)

保存后，您的片段即可用于历程、营销策划或模板。 在历程和营销活动中构建任何内容时，您可以使用此片段。 请参阅[添加可视片段](../email/use-visual-fragments.md)和[利用表达式片段](../personalization/use-expression-fragments.md)。

要创建片段，请执行以下步骤。

## 定义片段的属性 {#properties}

1. 通过&#x200B;**[!UICONTROL 内容管理]** > **[!UICONTROL 片段]**&#x200B;左侧菜单访问片段列表。

1. 选择&#x200B;**[!UICONTROL 创建片段]**&#x200B;并填写片段名称和描述（如果需要）。

   ![](assets/fragment-details.png)

1. 从&#x200B;**[!UICONTROL 标记]**&#x200B;字段中选择或创建Adobe Experience Platform标记可对片段进行分类，以改进搜索。 [了解如何使用统一标记](../start/search-filter-categorize.md#tags)

1. 选择片段类型： **可视化片段**&#x200B;或&#x200B;**表达式片段**。 [了解详情](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >当前，可视化片段仅可用于&#x200B;**电子邮件**&#x200B;渠道。

1. 如果要创建表达式片段，请选择要使用的代码类型：**[!UICONTROL HTML]**、**[!UICONTROL JSON]**&#x200B;或&#x200B;**[!UICONTROL 文本]**。

   ![](assets/fragment-expression-type.png)

1. 要为片段分配自定义或核心数据使用标签，请单击屏幕上方的&#x200B;**[!UICONTROL 管理访问权限]**&#x200B;按钮。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)。

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;以设计片段的内容。

## 设计片段内容 {#content}

配置片段的属性后，会根据您创建的片段类型打开Email Designer或个性化编辑器。

* 对于可视化片段，请根据需要编辑您的内容，就像处理历程或营销活动中的任何电子邮件一样。 [了解详情](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

  要快速应用符合您的品牌和设计的特定样式，您可以将[主题](../email/apply-email-themes.md)应用于片段。

  ![](assets/fragment-themes.png)

  >[!CAUTION]
  >
  >片段在主题模式和经典模式之间不交叉兼容。 要在要应用主题的内容中使用片段，必须在主题模式下创建此片段。 [了解有关主题的更多信息](../email/apply-email-themes.md)

* 对于表达式片段，利用[!DNL Journey Optimizer]个性化编辑器及其所有个性化和创作功能来构建片段内容。 [了解详情](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

内容就绪后，单击&#x200B;**[!UICONTROL 保存]**&#x200B;按钮。

>[!NOTE]
>
>可视片段不能超过100KB。 表达式片段不能超过200KB。

已创建片段并将其添加到状态为&#x200B;**[!UICONTROL 草稿]**&#x200B;的片段列表。 您可以预览并发布它，使其在历程和营销活动中可用。

## 预览和发布片段 {#publish}

>[!NOTE]
>
>要发布片段，您必须具有[发布片段](../administration/ootb-product-profiles.md#content-library-manager)用户权限。

如果您的片段已准备好上线，您可以预览和发布它以使其可在您的历程和营销活动中使用。 要实现此目的，请执行以下步骤。

1. 设计其内容后返回片段创建屏幕，或从片段列表中将其打开。

1. 片段预览位于&#x200B;**[!UICONTROL 标记]**&#x200B;字段下，允许检查其渲染。 如果需要执行任何更改，请单击屏幕上方的&#x200B;**[!UICONTROL 编辑]**&#x200B;按钮以打开电子邮件Designer或个性化编辑器，具体取决于片段类型。 [了解详情](manage-fragments.md#edit-fragments)

   ![](assets/fragment-preview.png)

1. 单击右上角的&#x200B;**[!UICONTROL 发布]**&#x200B;按钮发布片段。

1. 如果片段在实时历程或营销策划中使用，将打开一条消息通知您。 单击&#x200B;**[!UICONTROL 查看更多]**&#x200B;链接可访问引用它的历程和/或营销活动列表。 [了解如何浏览片段的引用](../content-management/manage-fragments.md#explore-references)

   ![](assets/fragment-publish.png){width="70%" align="center"}

   单击&#x200B;**[!UICONTROL 确认]**&#x200B;以发布片段，并在使用该片段的实时历程/营销活动中更新它。

片段现在为&#x200B;**[!UICONTROL 实时]**，在[!DNL Journey Optimizer] Email Designer或个性化编辑器中构建任何内容时都可用。

* [了解如何使用可视化片段](../email/use-visual-fragments.md)
* [了解如何使用表达式片段](../personalization/use-expression-fragments.md)
