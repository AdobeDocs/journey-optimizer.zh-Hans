---
solution: Journey Optimizer
product: journey optimizer
title: 创建片段
description: 了解如何创建片段以在Journey Optimizer营销活动和历程中重用内容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 83997271d16e15fb0d7ccdd21aa8ac8b8221a0d5
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 1%

---


# 从头开始创建片段 {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="选择可视类型"
>abstract="创建独立的可视化片段，以使您的内容可在历程或营销活动中的电子邮件或内容模板中重用。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html" text="向您的电子邮件添加可视化片段"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="选择表达式类型"
>abstract="创建一个独立的表达式片段，以使您的内容可在多个历程和营销活动中重复使用。 使用个性化编辑器时，您可以利用在当前沙盒上创建的所有表达式片段。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html" text="利用表达式片段"

片段是从以下位置创建的 **[!UICONTROL 片段]** 左侧菜单。 此外，在设计内容时，您还可以将现有内容的一部分另存为片段。 [了解如何操作](#save-as-fragment)

保存后，您的片段即可用于历程、营销策划或模板。 您现在可以在中构建任何内容时使用此片段 [!DNL Journey Optimizer]. 请参阅 [添加可视片段](../email/use-visual-fragments.md) 和 [利用表达式片段](../personalization/use-expression-fragments.md)

要从头开始创建片段，请执行以下步骤。

1. [访问片段列表](#access-manage-fragments) 通过 **[!UICONTROL 内容管理]** > **[!UICONTROL 片段]** 左侧菜单。

1. 选择 **[!UICONTROL 创建片段]**.

1. 填写片段详细信息，即名称和描述（如果需要）。

   ![](assets/fragment-details.png)

1. 从中选择或创建Adobe Experience Platform标记 **[!UICONTROL 标记]** 用于对片段进行分类以改进搜索的字段。 [了解详情](../start/search-filter-categorize.md#tags)

1. 选择片段类型： [可视片段](#create-visual-fragment) 或 [表达片段](#create-expression-fragment).

   >[!NOTE]
   >
   >当前仅可视片段使用 **电子邮件** 支持渠道。

1. 如果要创建表达式片段，请选择要使用的代码类型： **[!UICONTROL HTML]**， **[!UICONTROL JSON]** 或 **[!UICONTROL 文本]**.

   ![](assets/fragment-expression-type.png)

1. 要为片段分配自定义或核心数据使用标签，请选择 **[!UICONTROL 管理访问权限]**. [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md).

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 此 [电子邮件设计工具](../email/get-started-email-design.md) 或者会打开个性化编辑器，具体取决于您创建的片段类型。

   * 对于可视化片段，请根据需要编辑您的内容，就像处理历程或营销活动中的任何电子邮件一样。

     >[!NOTE]
     >
     >您可以添加个性化字段和动态内容，但片段中不支持上下文属性。

     ![](assets/fragment-designer.png)

   * 对于表达式片段，请使用 [!DNL Journey Optimizer] 具有所有个性化和创作功能的个性化编辑器，用于构建片段内容。 [了解详情](../personalization/personalization-build-expressions.md)

     ![](assets/fragment-expression-editor.png)

1. 片段准备就绪后，单击 **[!UICONTROL 保存]**.

片段将添加到 [片段列表](#access-manage-fragments). 现在，在中构建任何内容时，均可使用该功能 [!DNL Journey Optimizer] 电子邮件设计器或个性化编辑器。

* [了解如何使用可视化片段](../email/use-visual-fragments.md)
* [了解如何使用表达式片段](../personalization/use-expression-fragments.md)
