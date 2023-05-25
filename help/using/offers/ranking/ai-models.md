---
product: experience platform
solution: Experience Platform
title: AI模型入门
description: 了解允许对优惠进行排名的AI模型
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 4f331eff73991c32682ba2c1ca5f6b7341a561e1
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 4%

---

# AI模型入门 {#ai-models}

[!DNL Journey Optimizer] 允许您使用经过训练的模型系统，对要针对给定用户档案显示的选件进行排名。

此功能使您能够创建不同的 **AI模型** 基于您的业务目标。 在决策中使用这些基于目标的不同策略，经过训练的模型系统将帮助您了解不同的AI模型如何影响您的目标。

例如，您可以为电子邮件渠道选择一个AI模型，为推送渠道选择另一个模型。 对于每个渠道，经过训练的模型系统将利用多个数据点来确定在给定投放位置应首先显示哪个优惠，而不是考虑优惠的优先级得分或 [排名公式](create-ranking-formulas.md).

>[!IMPORTANT]
>
>目前，Journey Optimizer创作渠道不支持排名模型。

## AI 模型类型 {#ai-model-types}

中提供了两种类型的AI模型 [!DNL Journey Optimizer]：

* **自动优化模型** 旨在提供可最大程度提高业务客户回报(KPI)的优惠。 这些KPI可以是转化率、收入等形式。 目前，自动优化侧重于优化优惠点击，并将优惠转化作为我们的目标。 自动优化是非个性化的，并根据选件的“全局”性能进行优化。 [了解详情](auto-optimization-model.md)

* **个性化优化模型** 允许您定义业务目标，并利用客户数据来培训面向业务的模型，以提供个性化优惠并最大化KPI。 [了解详情](personalized-optimization-model.md)

## 创建AI模型 {#create-ai-model}

创建并使用AI模型的主要步骤如下：

1. 创建将从中收集转化和印象事件的数据集。 [了解详情](../data-collection/create-dataset.md)

1. 创建一个AI模型，该模型将利用来自数据集的事件对选件进行排名。 [了解详情](create-ranking-strategies.md)

1. 配置选件架构以自动捕获事件。 [了解详情](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >排名模型要求将反馈事件作为体验事件发送以便收集。 [了解有关决策管理数据收集的更多信息](../data-collection/data-collection.md)

1. 将AI模型分配给决策中的投放位置，以排名符合条件的优惠。 [了解详情](../offer-activities/configure-offer-selection.md)
