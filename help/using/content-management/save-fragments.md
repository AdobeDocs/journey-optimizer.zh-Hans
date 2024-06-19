---
solution: Journey Optimizer
product: journey optimizer
title: 将内容另存为片段
description: 了解如何将内容另存为片段以在Journey Optimizer营销活动和历程中重用内容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 70e88ea0-f2b0-4c13-8693-619741762429
source-git-commit: 893f7146b358da48153b1e6bc74b8f622028df76
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 8%

---

# 将内容另存为片段 {#save-as-fragment}

在中编辑内容时 [!DNL Journey Optimizer]，您可以将全部或部分内容另存为片段以供将来重用。 您可以将内容另存为片段 [从Email Designer](#save-as-visual-fragment)，或 [从表达式编辑器中](#save-as-expression-fragment).

## 另存为可视化片段 {#save-as-visual-fragment}

要将Email Designer的内容另存为片段，请执行以下步骤：

1. 在 [电子邮件设计工具](../email/get-started-email-design.md)中，单击屏幕右上方的省略号。

1. 选择 **[!UICONTROL 另存为片段]** 从下拉菜单中。

   ![](assets/fragment-save-as.png)

1. 此 **[!UICONTROL 另存为片段]** 屏幕显示。 其中选择要包含在片段中的元素，包括个性化字段和动态内容。 请注意，片段中不支持上下文属性。

   ![](assets/fragment-save-as-screen.png)

   >[!CAUTION]
   >
   >只能选取彼此相邻的部分。 您不能选择空的结构或其他片段。

1. 单击 **[!UICONTROL 创建]** 并填写片段名称和描述（如果需要）。

1. 要为片段分配自定义或核心数据使用标签，请单击 **[!UICONTROL 管理访问权限]** 按钮来打开屏幕。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md).

1. 从中选择或创建Adobe Experience Platform标记 **标记** 用于对模板进行分类以改进搜索的字段。 [了解详情](../start/search-filter-categorize.md#tags)

1. 单击&#x200B;**[!UICONTROL 创建]**。片段将添加到 [片段列表](#access-manage-fragments) 使用 **草稿** 状态。 它会变成一个独立的片段，可用作该列表中的任何其他可视化片段。

   >[!NOTE]
   >
   >对该新片段所做的任何更改都不会传播到它来自的电子邮件或模板。 同样，在该电子邮件或模板中编辑原始内容时，不会修改新片段。

1. 为了能够在您的历程和营销活动中使用片段，您需要让它上线。 [了解如何预览和发布片段](../content-management/create-fragments.md#publish)

>[!NOTE]
>
>片段发布在Journey Optimizer 6月发布后的几天内逐步推出。 虽然某些用户将可以立即访问，但其他用户在环境中使用它之前可能会遇到延迟。 如果您的环境中尚未提供此增强功能，请注意，在您的历程和营销活动中使用片段不需要发布片段。

## 另存为表达式片段 {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="另存为表达式片段"
>abstract="[!DNL Journey Optimizer]个性化编辑器可让您将内容另存为表达式片段。之后，这些表达式可用于构建个性化内容。"

[!DNL Journey Optimizer]个性化编辑器可让您将内容另存为表达式片段。之后，这些表达式可用于构建个性化内容。

要将内容另存为表达式片段，请执行以下步骤。

1. 在 [个性化编辑器](../personalization/personalization-build-expressions.md) 界面，构建表达式，然后单击 **[!UICONTROL 另存为片段]**.

   >[!NOTE]
   >
   >表达式不能超过200KB。

1. 在右侧窗格中，输入表达式的名称和说明，以帮助用户更轻松地找到它。

   ![](assets/expression-fragment-save-as.png)

1. 单击 **[!UICONTROL 保存片段]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. 片段将添加到 [片段列表](#access-manage-fragments) 使用 **草稿** 状态。 它会变成一个独立的片段，可用作该列表中的任何其他表达式片段。

1. 为了能够在您的历程和营销活动中使用片段，您需要让它上线。 [了解如何预览和发布片段](../content-management/create-fragments.md#publish)

>[!NOTE]
>
>片段发布在Journey Optimizer 6月发布后的几天内逐步推出。 虽然某些用户将可以立即访问，但其他用户在环境中使用它之前可能会遇到延迟。 如果您的环境中尚未提供此增强功能，请注意，在您的历程和营销活动中使用片段不需要发布片段。
