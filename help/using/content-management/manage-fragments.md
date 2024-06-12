---
solution: Journey Optimizer
product: journey optimizer
title: 管理片段
description: 了解如何管理您的内容片段
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 1fc708e1-a993-4a2a-809c-c5dc08a4bae1
source-git-commit: 4f238177485ccc5ab53b48488dd1f2084d34d684
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 2%

---

# 管理片段 {#manage-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="新片段状态"
>abstract="从 **草稿** 和 **实时** Journey Optimizer 6月版本中引入了状态，在此版本之前创建的所有片段均具有“草稿”状态，即使它们在历程或营销活动中使用。 如果您对这些片段进行了任何更改，则需要发布它们以使它们“处于活动状态”，并将更改传播到关联的营销活动和历程。 您还需要创建新历程/营销活动版本并进行发布。"

要管理片段，请从访问片段列表 **[!UICONTROL 内容管理]** > **[!UICONTROL 片段]** 左侧菜单。

![](assets/fragment-list.png)

在当前沙盒中创建的所有片段 —  [从 **[!UICONTROL 片段]** 菜单](#create-fragments)，使用 [另存为片段](#save-as-fragment) 选项 — 将显示。

您可以按以下项筛选片段：

* 类型： **[!UICONTROL 可视化]** 或 **[!UICONTROL 表达式]**
* 标记
* 创建或修改日期

您可以选择显示所有片段，或仅显示当前用户创建或修改的项目。

您还可以显示 **[!UICONTROL 已存档]** 片段。 [了解详情](#archive-fragments)

![](assets/fragment-list-filters.png)

从 **[!UICONTROL 更多操作]** 按钮进行以下操作：

* 复制片段。

* 使用 **[!UICONTROL 浏览引用]** 选项，用于查看使用它的历程、营销策划或模板。 [了解详情](#explore-references)

* 将片段存档。 [了解详情](#archive-fragments)

* 编辑片段的 [标记](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## 编辑片段 {#edit-fragments}

要编辑片段，请执行以下步骤。

1. 单击以下位置中的所需项目： **[!UICONTROL 片段]** 列表。
1. 从片段属性中，您可以 [浏览引用](#explore-references)， [管理其访问权限](../administration/object-based-access.md)，并更新片段详细信息，包括 [标记](../start/search-filter-categorize.md#tags).

   ![](../email/assets/fragment-edit-content.png)

1. 选择相应的按钮以编辑内容，就像从头开始创建片段时所做的那样。 [了解详情](#create-from-scratch)

>[!NOTE]
>
>在编辑片段时，更改将自动传播到该片段使用的所有内容，但中使用的内容除外 **[!UICONTROL 实时]** 历程或营销活动。 您还可以中断来自原始片段的继承。 在中了解详情 [向您的电子邮件添加可视化片段](../email/use-visual-fragments.md#break-inheritance) 和 [利用表达式片段](../personalization/use-expression-fragments.md#break-inheritance) 部分。

## 探索引用 {#explore-references}

您可以显示当前使用片段的历程、营销活动和内容模板列表。

要执行此操作，请选择 **[!UICONTROL 浏览引用]** 来自 **[!UICONTROL 更多操作]** 菜单或片段属性屏幕中的菜单的操作工具栏。

![](assets/fragment-explore-references.png)

选择一个选项卡，可在历程、营销活动、模板和片段之间切换。 您可以查看其状态，然后单击名称以重定向到引用片段的相应项目。

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>如果片段用在历程、营销策划或模板中，且标签阻止您访问片段，您将在选定选项卡顶部看到一条警报消息。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)

## 存档片段 {#archive-fragments}

您可以从不再与您的品牌相关的项目中清理片段列表。

要执行此操作，请单击 **[!UICONTROL 更多操作]** 按钮选择所需片段旁边的 **[!UICONTROL 存档]**. 它会从片段列表中消失，从而阻止用户在未来电子邮件或模板中使用它。

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>如果存档内容中使用的片段， <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->该内容将不会受到影响。

要取消存档片段，请在 **[!UICONTROL 已存档]** 项并选择 **[!UICONTROL 取消存档]** 从 **[!UICONTROL 更多操作]** 菜单。 现在可以再次从片段列表中访问，并可用于任何电子邮件或模板。

![](assets/fragment-list-unarchive.png)
