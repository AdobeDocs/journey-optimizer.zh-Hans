---
solution: Journey Optimizer
product: journey optimizer
title: 用户界面
description: 进一步了解 Journey Optimizer 用户界面
feature: Overview
topic: Content Management
role: User
level: Intermediate
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 33%

---


# 搜索、过滤、组织 {#search-filter-organize}

## 搜索{#unified-search}

在 Adobe Journey Optimizer 界面的任何地方，使用顶部中央位置的 Adobe Experience Cloud 统一搜索功能在沙盒中查找资产、历程和数据集等等。

开始输入内容以显示排名靠前的结果。与输入的关键词有关的帮助文章也会显示在结果中。

![](assets/unified-search.png)

按 **Enter** 键访问所有结果并按业务对象进行筛选。

![](assets/search-and-filter.png)

## 筛选器列表{#filter-lists}

在大多数列表中，可使用搜索栏查找特定项目并定义筛选条件。

单击列表左上角的筛选图标即可访问筛选器。利用过滤器菜单，可根据不同的条件筛选显示的元素：您可以选择仅显示特定类型或状态的元素、您创建的元素或最近30天内修改的元素。 选项因上下文不同而异。

此外，您还可以使用统一标记来根据分配给对象的标记来筛选列表。 目前，标记可用于历程和营销活动。 [了解如何使用标记](#tags)

>[!NOTE]
>
>请注意，显示的列可以使用列表右上角的配置按钮进行个性化设置。为每个用户保存个性化设置。

在列表中，您可以对每个元素执行基本操作。例如，您可以删除项目或制作项目副本。

![](assets/journey4.png)

## 使用统一的标记 {#tags}

使用Adobe Experience Platform [统一标记](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html)，您可以轻松地对Journey Optimizer历程和促销活动进行分类，以改进从列表中的搜索。

>[!AVAILABILITY]
>
>统一标记当前处于测试阶段。 文档和功能可能会发生变化。

## 向对象添加标记

的 **标记** 字段，在 [历程](../building-journeys/journey-gs.md#change-properties) 或 [营销活动](../campaigns/create-campaign.md#create) 属性，用于为对象定义标记。 您可以选择现有标记，也可以创建新标记。

开始键入所需标记的名称，然后从列表中选择该名称。 如果不可用，请单击 **创建** 以创建并添加新受众。 您可以根据需要定义任意数量的标记。

![](assets/tags1.png)

定义的标记列表显示在 **标记** 字段。

>[!NOTE]
>
> 标记区分大小写
> 
> 如果您复制或创建历程或营销策划的新版本，则会保留标记。

## 标记过滤

历程和营销活动列表显示一个专用列，以便您能够轻松地将标记可视化。

过滤器还仅可用于显示具有特定标记的历程或营销活动。

![](assets/tags2.png)

您可以在任何类型的历程或营销策划（实时、草稿等）中添加或删除标记。 为此，请单击 **更多操作** 图标，然后选择 **编辑标记**.

![](assets/tags3.png)

## 管理标记

管理员可以删除标记，并使用 **标记** 菜单，下 **管理**. 在 [统一标记文档](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/ui/managing-tags.html).

>[!NOTE]
>
> 直接从 **[!UICONTROL 标记]** 字段会自动添加到内置的“未分类”类别中。
