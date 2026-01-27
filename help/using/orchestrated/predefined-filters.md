---
solution: Journey Optimizer
product: journey optimizer
title: 使用预定义过滤器
description: 了解如何在编排的营销活动中保存、应用和管理预定义过滤器
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 11%

---


# 使用预定义过滤器 {#predefined-filters}

预定义过滤器是已保存的规则，您可以在规则生成器中重复使用。 使用它们可避免重建常见查询，并标准化跨编排的营销活动的定位逻辑。

您可以将预定义过滤器标记为收藏、与其他用户共享以及添加参数，以便在应用过滤器时编辑选定的字段。

## 创建预定义过滤器 {#create}

保存规则生成器中的自定义筛选条件，以便将来使用。 执行以下步骤：

1. 打开规则生成器并定义您的过滤条件。[了解如何生成规则](../orchestrated/build-query.md)

1. 可选：若要在使用筛选器时使某些字段可编辑，请选择该字段并打开&#x200B;**[!UICONTROL 设置为参数]**。 应用过滤器时，只能编辑这些字段。

   ![](assets/predefined-filter-parameter-enable.png)

1. 若要保存筛选器，请单击&#x200B;**[!UICONTROL 选择或保存筛选器]**，然后选择&#x200B;**[!UICONTROL 另存为筛选器]**。

   ![](assets/predefined-filter-save.png)

1. 输入筛选器的标签和说明，然后单击&#x200B;**[!UICONTROL 保存]**。

   * 如需将过滤器保存为收藏，请开启&#x200B;**[!UICONTROL 收藏过滤器]**&#x200B;选项。有关详细信息，请参阅[此部分](#fav-filter)。
   * 要使其他用户能够访问该筛选器，请启用&#x200B;**[!UICONTROL 共享筛选器]**&#x200B;选项。 有关详细信息，请参阅[此部分](#share-filter)。

   ![](assets/predefined-filter-save-name.png)

您的自定义筛选器现在可在&#x200B;**预定义筛选器**&#x200B;列表中使用。

## 在规则中使用预定义过滤器 {#apply}

在规则生成器中定义查询时，可以使用预定义过滤器。

1. 在&#x200B;**[!UICONTROL 规则属性]**&#x200B;窗格中，单击&#x200B;**[!UICONTROL 选择或保存筛选器]**。

1. 选择&#x200B;**[!UICONTROL 选择预定义过滤器]**&#x200B;并选择过滤器。 如果已将某个预定义过滤器添加到收藏夹，则也可以直接从列表中选择该过滤器。

   ![](assets/predefined-filter-apply.png)

   >[!IMPORTANT]
   >
   >选择预定义过滤器会将画布中已构建的规则替换为所选过滤器。

1. 该过滤器将在画布中打开。 根据需要继续编辑条件。

   ![](assets/predefined-filter-added.png)

   如果所选过滤器包含参数，则只能编辑标记为参数的字段。 它们显示在&#x200B;**[!UICONTROL 规则属性]**&#x200B;窗格旁边的窗格中。

   ![](assets/predefined-filter-parameter-apply.png)

   要编辑预定义过滤器本身，请单击![省略号按钮](assets/do-not-localize/rule-builder-icon-more.svg)并选择&#x200B;**[!UICONTROL 切换到规则版本]**。 所有更改仅应用于您正在构建的当前规则。 不修改预定义过滤器。

   ![](assets/predefined-filter-parameter-edit.png)

## 将过滤器另存为收藏夹 {#fav-filter}

创建预定义过滤器时，请启用&#x200B;**[!UICONTROL 收藏夹过滤器]**&#x200B;选项，以在收藏夹中查看此预定义过滤器。

将筛选器另存为收藏后，该筛选器会显示在筛选器列表的&#x200B;**[!UICONTROL 收藏的筛选器]**&#x200B;部分，如下所示：

![收藏过滤器部分](assets/predefined-filter-favorites.png)

## 共享预定义过滤器 {#share-filter}

默认情况下，您创建的预定义过滤器是私有的，仅对您可见。 要使组织中的其他操作员能够访问某个筛选器，请启用&#x200B;**[!UICONTROL 共享筛选器]**&#x200B;选项。

![共享筛选器选项](assets/predefined-filter-shared.png)

共享过滤器会显示在适用于所有用户的预定义过滤器列表中，从而允许他们在自己的规则中使用这些过滤器。

## 管理预定义过滤器 {#manage-predefined-filter}

要编辑或删除预定义过滤器，请执行以下步骤：

1. 使用规则生成中的&#x200B;**[!UICONTROL 选择或保存筛选器]**&#x200B;按钮打开预定义筛选器列表。

1. 选择筛选器旁边的![省略号按钮](assets/do-not-localize/rule-builder-icon-more.svg)并选择所需的操作。

![](assets/predefined-filters-edit.png)
