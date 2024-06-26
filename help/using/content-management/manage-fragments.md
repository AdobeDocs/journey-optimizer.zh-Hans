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
source-git-commit: 8ca75a149db65ee65bf28fe6c0688ee18488fcec
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 管理片段 {#manage-fragments}

要管理片段，请从访问片段列表 **[!UICONTROL 内容管理]** > **[!UICONTROL 片段]** 左侧菜单。

在当前沙盒中创建的所有片段 —  [从 **[!UICONTROL 片段]** 菜单](#create-fragments)，使用 [另存为片段](#save-as-fragment) 选项 — 将显示。

![](assets/fragment-list-filters.png)

您可以按以下项筛选片段：

* 状态（草稿或实时）
* 类型（可视化或表达式）
* 创建或修改日期
* 状态（已存档或未存档）
* 标记

您还可以选择显示所有片段，或仅显示当前用户创建或修改的项目。

从 **[!UICONTROL 更多操作]** 按钮进行以下操作：

* 复制片段。
* 使用 **[!UICONTROL 浏览引用]** 选项，用于查看使用它的历程、营销策划或模板。 [了解详情](#explore-references)
* 将片段存档。 [了解详情](#archive-fragments)
* 编辑片段的标记 [了解如何使用统一标记](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## 片段状态

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="新的片段状态"
>abstract="由于在 Journey Optimizer 6 月版中引入了&#x200B;**草稿**&#x200B;和&#x200B;**实时**&#x200B;状态，因此在此版本之前创建的所有片段都具有“草稿”状态，即使它们用于历程或活动中。如果您对这些片段进行任何更改，则需要发布片段以使其“生效”，并将更改传播到相关的活动和历程。您还需要创建一个新的历程/活动版本并发布它。发布需要用户权限。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="了解有关内容片段权限的更多信息"

>[!AVAILABILITY]
>
> 请注意，片段状态在Journey Optimizer 6月发布后的几天内逐步推出。 虽然某些用户将可以立即访问，但其他用户在环境中使用它之前可能会遇到延迟。 如果您的环境中尚未提供此增强功能，请注意，片段不需要 **实时** 将在您的历程和营销活动中使用。

片段可以具有多种状态：

* **[!UICONTROL 草稿]**：片段正在编辑且未获得批准。

* **[!UICONTROL 实时]**：片段已获得批准并处于活动状态。 [了解如何发布片段](../content-management/create-fragments.md#publish)

  在编辑实时片段时，其状态旁边会显示一个特定图标。 单击此图标可打开片段的草稿版本。

* **[!UICONTROL 发布]**：片段已获得批准并正在发布。
* **[!UICONTROL 已存档]**：片段已存档。 [了解如何存档片段](#archive-fragments)

>[!CAUTION]
>
>由于在 Journey Optimizer 6 月版中引入了&#x200B;**草稿**&#x200B;和&#x200B;**实时**&#x200B;状态，因此在此版本之前创建的所有片段都具有“草稿”状态，即使它们用于历程或活动中。如果您对这些片段进行任何更改，则需要发布片段以使其“生效”，并将更改传播到相关的活动和历程。您还需要创建一个新的历程/活动版本并发布它。发布需要用户权限。

## 编辑片段 {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="活动中的片段更新"
>abstract="如果您发布对片段所做的更改，则此营销活动不会更新。 它需要发布新版本，以便可以支持片段更新功能。"

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="历程中的片段更新"
>abstract="如果您发布对片段所做的更改，则不会更新此历程。 它需要发布新版本，以便可以支持片段更新功能。"

要编辑片段，请执行以下步骤。

1. 从单击所需的片段 **[!UICONTROL 片段]** 列表。

1. 片段属性将打开，并预览其内容。

1. 如果正在编辑的片段具有 **实时** 状态，单击 **修改** 按钮以创建片段的草稿版本。 片段的当前版本将继续处于活动状态，直到您发布草稿版本。

1. 对片段进行所需的更改。 要编辑其内容，请单击 **编辑** 按钮后，可编辑您的内容，就像从头开始创建片段时所做的那样。 [了解如何创建片段](#create-from-scratch)

   >[!NOTE]
   >
   >编辑表达式片段时，您可以删除任何个性化字段，但无法向片段内容添加新个性化字段。 如果要添加个性化字段，请复制片段以创建新片段。

   您还可以通过选择 **资源管理器引用** 选项。 [了解详情](#explore-references)

   ![](assets/fragment-edit.png)

1. 更改准备就绪后，单击 **Publish** 按钮以使您的修改处于活动状态。

在编辑片段时，更改会自动传播到使用该片段的所有内容，包括实时历程和营销活动，但已中断原始片段继承的内容除外。 了解如何在中中断继承 [向您的电子邮件添加可视化片段](../email/use-visual-fragments.md#break-inheritance) 和 [利用表达式片段](../personalization/use-expression-fragments.md#break-inheritance) 部分。

>[!AVAILABILITY]
>
>请注意，在Journey Optimizer 6月发布后的几天内，实时历程和营销活动中的片段更改传播正在逐步推出。 虽然某些用户将可以立即访问，但其他用户在环境中使用它之前可能会遇到延迟。 如果您的环境中尚未提供此增强功能，则您的更改将不会传播到实时历程或营销活动中使用的内容。

## 探索引用 {#explore-references}

您可以显示当前使用片段的历程、营销活动和内容模板列表。 要执行此操作，请选择 **[!UICONTROL 浏览引用]** 来自 **[!UICONTROL 更多操作]** 菜单或片段属性屏幕中的菜单的操作工具栏。

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
