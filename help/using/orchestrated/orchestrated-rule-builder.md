---
solution: Journey Optimizer
product: journey optimizer
title: 使用规则生成器
description: 了解如何为编排的活动创建规则
exl-id: fb7a0eb2-b2ff-49fa-af1f-f1c10f219b00
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 69%

---


# 使用规则生成器 {#orchestrated-rule-builder}

精心策划的营销活动附带规则生成器，可简化根据各种标准筛选数据库的过程。规则生成器可高效处理极其复杂的长查询，提供更强的灵活性与精准度。

它还支持在条件中使用预定义过滤器，让您能轻松优化查询，同时借助高级表达式和运算符实现全面的受众目标选择与细分策略。

## 访问规则生成器 {#access}

在需要定义规则以筛选数据的每个上下文中，都可以使用规则生成器。

| 使用情况 | 示例 |
|  ---  |  ---  |
| **构建受众**：使用&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动指定要在编排的营销活动中定位的群体，并轻松创建根据您的需求定制的新受众。 [了解如何生成受众](../orchestrated/activities/build-audience.md) | ![显示如何访问受众创建界面的图像](assets/query-access-audience.png){width="200" align="center" zoomable="yes"} |
| **在营销活动画布中创建条件**：使用&#x200B;**[!UICONTROL 拆分]**&#x200B;活动在营销活动画布中应用规则，以满足您的特定要求。[了解如何使用“拆分”活动](../orchestrated/activities/split.md) | ![显示如何访问工作流自定义选项的图像](assets/query-access-split.png){width="200" align="center" zoomable="yes"} |
| **创建高级过滤器**：生成规则以过滤列表中显示的数据，如促销活动日志或定向维度。 | ![显示如何自定义列表过滤器的图像](assets/query-access-advanced-filters.png){width="200" align="center" zoomable="yes"} |

## 规则生成器界面 {#interface}

规则生成器提供了一个中央画布用于生成查询，并提供一个显示规则详情的属性窗格。

![显示规则生成器界面的图像](assets/rule-builder-interface.png)

* **中央画布**&#x200B;是添加和组合各类组件以生成规则的操作区域。[了解如何生成规则](../orchestrated/build-query.md)

* **[!UICONTROL 规则属性]**&#x200B;窗格提供有关规则的信息。它支持执行各种操作来检查规则，确保其符合您的需求。

  在生成查询以创建受众时，会显示此窗格。[了解如何检查和验证您的查询](build-query.md#check-and-validate-your-query)

## 使用预定义过滤器

通过预定义过滤器，您可以重用规则生成器中保存的查询，包括带有参数的版本。 有关保存、应用和管理预定义过滤器的完整演练，请参阅[使用预定义过滤器](predefined-filters.md)。
