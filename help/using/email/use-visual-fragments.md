---
solution: Journey Optimizer
product: journey optimizer
title: 使用可视化片段
description: 了解如何在Journey Optimizer营销活动和历程中创建电子邮件时使用可视化片段
feature: Email Design, Fragments
topic: Content Management
role: User
level: Beginner
exl-id: 25a00f74-ed08-479c-9a5d-4185b5f3c684
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 4%

---

# 将可视片段添加到电子邮件 {#use-visual-fragments}

您可以在以下位置使用可视化片段： [电子邮件](get-started-email-design.md) 在历程或营销策划中，或在 [内容模板](../content-management/content-templates.md).

>[!NOTE]
>
>了解如何在中创建和管理片段 [本节](../content-management/fragments.md).

➡️ [在此视频中了解如何管理、创作和使用片段](../content-management/fragments.md#video-fragments)

## 使用片段 {#use-fragment}

1. 使用打开任何电子邮件或模板内容 [电子邮件设计工具](get-started-email-design.md).

1. 选择 **[!UICONTROL 片段]** 图标。

   ![](assets/fragments-in-designer.png)

1. 此时将显示在当前沙盒中创建的所有可视化片段的列表。 您可以：

   * 通过开始键入特定片段的标签来搜索该片段。
   * 按升序或降序对片段排序。
   * 更改片段的显示方式（卡片视图或列表视图）。

   >[!NOTE]
   >
   >片段按创建日期排序：最近添加的可视化片段首先显示在列表中。

1. 您可以搜索和刷新该列表。

   >[!NOTE]
   >
   >如果在编辑内容时修改或添加了某些片段，则列表将使用最新更改进行更新。

1. 将列表中的任何片段拖放到要插入它的区域。

   ![](assets/fragment-insert.png)

1. 与任何其他组件一样，您可以在内容中移动片段。

1. 选择片段以在右侧显示相应的窗格。 从该位置，您可以从内容中删除片段或复制片段。 您还可以直接从片段顶部显示的上下文菜单执行这些操作。

   ![](assets/fragment-right-pane.png)

1. 从 **[!UICONTROL 设置]** 选项卡，您可以：

   * 选择您希望片段显示的设备。
   * 需要时，在新选项卡中打开片段以对其进行编辑。 [了解详情](../content-management/fragments.md#edit-fragments)
   * 浏览引用。 [了解详情](../content-management/fragments.md#explore-references)

1. 您可以使用进一步自定义片段 **[!UICONTROL 样式]** 选项卡。

1. 如果需要，您可以使用原始片段中断继承。 [了解详情](#break-inheritance)

1. 添加所需数量的片段并 **[!UICONTROL 保存]** 您所做的更改。

## 中断继承 {#break-inheritance}

编辑可视片段时，将同步更改。 它们会自动传播到所有 **[!UICONTROL 草稿]** 历程/营销活动和包含该片段的内容模板。

>[!NOTE]
>
>更改不会传播到中使用的电子邮件 **[!UICONTROL 实时]** 历程或营销活动。

添加到电子邮件或内容模板时，片段默认进行同步。

但是，您可以中断来自原始片段的继承。 在这种情况下，片段的内容将被复制到当前设计中，并且更改不再同步。

要中断继承，请执行以下步骤：

1. 选择片段。

1. 单击上下文工具栏中的解锁图标。

   ![](assets/fragment-break-inheritance.png)

1. 该片段将成为不再链接到原始片段的独立元素。 可将其编辑为内容中的任何其他内容组件。 [了解详情](content-components.md)
