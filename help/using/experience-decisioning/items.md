---
title: 决策项
description: 了解如何使用决策项
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta 版"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: 50d3be8fb8ae04e1cab747f6ba4b1024c5e3ec97
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 25%

---

# 决策项 {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="管理决策项"
>abstract="通过 Journey Optimizer，可创建营销优惠（称为决策项）并将其整理到集中目录和收藏集中。目前，所有创建的决策项都会被合并到一个“优惠”目录中。在此屏幕中，您还可以使用&#x200B;**编辑架构**&#x200B;按钮访问该目录的架构，并为您的决策项创建自定义属性。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html" text="配置项目目录"

>[!BEGINSHADEBOX “您将在本文档指南中找到什么”]

* [开始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的决策项目： [配置物料目录](catalogs.md) - **[创建决策项目](items.md)** - [管理物料集合](collections.md)
* 配置项目的选择： [创建决策规则](rules.md) - [创建排名方法](ranking.md)
* [创建选择策略](selection-strategies.md)
* [创建决策策略](create-decision.md)

>[!ENDSHADEBOX]

通过 Journey Optimizer，可创建营销优惠（称为决策项）并将其整理到集中目录和收藏集中。它们由旨在精确满足您需求的标准和自定义属性组成。 此外，它们包含配置文件约束，允许您定义决策项目可以显示给谁。

在创建决策项目之前，请确保已创建 **决策规则** 如果您要设置条件以确定决策项可以显示给谁。 [了解如何创建决策规则](rules.md).

## 创建您的第一个决策项

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="定义决策项的优先级"
>abstract="如果一个配置文件符合多项的条件，则可通过优先级比较此决策项与其他决策项。较高的优先级使该项优先于其他项。"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="定义自定义属性"
>abstract="自定义属性是根据您的需求定制的特定属性，您可以将其分配给决策项。在决策项的目录架构中创建它们。只有将至少一个自定义属性添加到目录架构，才显示此部分。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html" text="配置项目目录"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="添加受众或决策规则"
>abstract="默认情况下，所有配置文件都有资格接收决策项，但您可使用受众或规则仅限特定配置文件可接收该项。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html" text="使用受众"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/selection/rules.html" text="使用决策规则"

要创建决策项目，请执行以下步骤：

1. 导航到 **[!UICONTROL Experience Decisioning]** > **[!UICONTROL 项目]**.

1. 定义决策项目的标准属性：

   1. 提供名称和描述。
   1. 指定开始日期和结束日期。 在此类日期内，项目仅由决策引擎考虑。
   1. 设置 **[!UICONTROL 优先级]** 与其他项目相比，如果配置文件符合多个项目的条件，则为决策项目。 较高的优先级使该项优先于其他项。
   1. 此 **标记** 字段用于将Adobe Experience Platform统一标记分配给决策项目。 这使您能够轻松分类这些分类并改进搜索。 [了解如何使用标记](../start/search-filter-categorize.md#tags)

   ![](assets/item-attributes.png)

   >[!NOTE]
   >
   >优先级是integer数据类型。 整数数据类型的所有属性都应包含整数值（无小数）。

1. 自定义属性是根据您的需求定制的特定属性，您可以将其分配给决策项。它们在决策项的目录架构中定义。 [了解如何使用目录](catalogs.md)

1. 定义决策项目的属性后，单击 **[!UICONTROL 下一个]** 设置物料的配置文件约束。

   默认情况下，所有用户档案都有资格接收决策项目，但您可以使用受众或规则将项目限制为仅特定用户档案，这两个解决方案都对应于不同的使用情况。 有关详细信息，请展开以下部分：

   +++使用受众与决策规则

   基本上，受众的输出是一个用户档案列表，而决策规则是在决策过程中根据请求对单个用户档案执行的函数。

   * **受众**：一方面，受众是一组Adobe Experience Platform配置文件，它们根据配置文件属性和体验事件匹配特定逻辑。 但是，选件管理不会重新计算受众，它在呈现选件时可能不是最新的。

   * **决策规则**：另一方面，决策规则基于Adobe Experience Platform中可用的数据，并确定可向谁显示选件。 在给定投放位置的优惠或决策中选择优惠后，每次做出决策时都会执行规则，从而确保每个用户档案都获得最新和最佳优惠。

+++

   ![](assets/item-constraints.png)

   * 要将决策项的呈现方式限制为一个或多个Adobe Experience Platform受众的成员，请选择 **[!UICONTROL 属于一个或多个受众的访客]** 选项，然后从左窗格添加一个或多个受众，然后使用 **[!UICONTROL 和]** / **[!UICONTROL 或]** 逻辑运算符。 [了解有关受众的更多信息](../audience/about-audiences.md).

   * 要将特定决策规则与决策项目关联，请选择 **[!UICONTROL 按规则]**，然后将所需规则从左窗格拖到中心区域。 [了解有关决策规则的更多信息](rules.md).

   在选择受众或决策规则时，您可以看到有关预计的合格用户档案的信息。 单击 **[!UICONTROL 刷新]** 以更新数据。

   >[!NOTE]
   >
   >当规则参数包含不在配置文件中的数据（如上下文数据）时，配置文件估计不可用。 例如，资格规则要求当前天气为≥80度。

1. 定义决策项的约束后，单击 **[!UICONTROL 下一个]** 以查看并保存项目。

1. 决策项目现在显示在列表中，其中包含 **[!UICONTROL 草稿]** 状态。 当它准备好呈现给配置文件时，单击省略号按钮并选择 **[!UICONTROL 批准]**.

   ![](assets/item-approve.png)

## 管理决策项

从决策项列表中，您可以编辑决策项，更改其状态(**草稿**， **已批准**， **已存档**)，复制或删除它。

要修改决策项，请打开该决策项，进行修改并保存它。

选择决策项目或单击省略号按钮可启用下面所述的操作。

* **[!UICONTROL 批准]**：将决策项目的状态设置为“已批准”。
* **[!UICONTROL 撤消审批]**：将决策项目的状态设回 **[!UICONTROL 草稿]**.
* **[!UICONTROL 复制]**：创建具有相同属性和约束的决策项。 默认情况下，新项目具有 **[!UICONTROL 草稿]** 状态。
* **[!UICONTROL 删除]**：从列表中删除决策项。

  >[!IMPORTANT]
  >
  >删除后，无法再访问决策项目及其内容。 此操作无法撤消。 如果决策项用在收藏集或决策中，则无法删除该决策项。 必须先从任何对象中删除决策项。

* **[!UICONTROL 存档]**：将决策项状态设置为 **[!UICONTROL 已存档]**. 该决策项目仍然可以从列表中获得，但您不能将其状态恢复为 **[!UICONTROL 草稿]** 或 **[!UICONTROL 已批准]**. 您只能复制或删除它。
