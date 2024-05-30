---
solution: Journey Optimizer
product: journey optimizer
title: 将内容另存为片段
description: 了解如何将内容另存为片段以在Journey Optimizer营销活动和历程中重用内容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 83997271d16e15fb0d7ccdd21aa8ac8b8221a0d5
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%

---

# 将内容另存为片段 {#save-as-fragment}

在中编辑内容时 [!DNL Journey Optimizer]，您可以将全部或部分内容另存为片段以供将来重用。

## 将内容另存为可视化片段 {#save-as-visual-fragment}

设计 [内容模板](content-templates.md) 或 [电子邮件](../email/get-started-email-design.md) 在营销活动或历程中，您可以将内容的一部分另存为可视化片段。 为此，请执行以下步骤。

1. 在 [电子邮件设计工具](../email/get-started-email-design.md)中，单击屏幕右上方的省略号。

1. 选择 **[!UICONTROL 另存为片段]** 从下拉菜单中。

   ![](assets/fragment-save-as.png)

1. 此 **[!UICONTROL 另存为片段]** 屏幕显示。 其中选择要包含在片段中的元素，包括个性化字段和动态内容。 请注意，片段中不支持上下文属性。

   >[!CAUTION]
   >
   >只能选取彼此相邻的部分。 您不能选择空的结构或其他片段。

   ![](assets/fragment-save-as-screen.png)

1. 单击 **[!UICONTROL 创建]**. 填写片段详细信息，即名称和描述（如果需要）。

1. 要为片段分配自定义或核心数据使用标签，请选择 **[!UICONTROL 管理访问权限]**. [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md).

1. 从中选择或创建Adobe Experience Platform标记 **标记** 用于对模板进行分类以改进搜索的字段。 [了解详情](../start/search-filter-categorize.md#tags)

1. 单击 **[!UICONTROL 创建]** 再来一次。 片段将保存到，并添加到 [片段列表](#access-manage-fragments)，可从访问 [!DNL Journey Optimizer] 专用菜单。

   它会变成一个独立的片段，可以 [已访问](#access-manage-fragments)， [已编辑](#edit-fragments) 和 [已存档](#archive-fragments) 作为该列表中的任何其他项目。

现在，您可以在构建任何 [电子邮件](../email/get-started-email-design.md) 或 [内容模板](content-templates.md) 范围 [!DNL Journey Optimizer]. [了解如何操作](../email/use-visual-fragments.md)

>[!NOTE]
>
>对该新片段所做的任何更改都不会传播到它来自的电子邮件或模板。 同样，在该电子邮件或模板中编辑原始内容时，不会修改新片段。

## 将内容另存为表达式片段 {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="另存为表达式片段"
>abstract="此 [!DNL Journey Optimizer] 个性化编辑器允许您将内容另存为表达式片段。 然后，可以使用这些表达式来构建个性化内容。"

此 [!DNL Journey Optimizer] 个性化编辑器允许您将内容另存为表达式片段。 然后，可以使用这些表达式来构建个性化内容。

要将内容另存为表达式片段，请执行以下步骤。

1. 在 [个性化编辑器](../personalization/personalization-build-expressions.md) 界面，构建表达式，然后单击 **[!UICONTROL 另存为片段]**.

1. 在右侧窗格中，输入表达式的名称和说明，以帮助用户更轻松地找到它。

   ![](assets/expression-fragment-save-as.png)

1. 单击 **[!UICONTROL 保存片段]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. 表达式片段将添加到 [片段列表](#access-manage-fragments). 您现在可以使用它来构建个性化内容。

>[!NOTE]
>
>表达式不能超过200KB。
