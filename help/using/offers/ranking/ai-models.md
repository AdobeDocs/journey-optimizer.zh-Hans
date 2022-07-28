---
product: experience platform
solution: Experience Platform
title: AI模型快速入门
description: 了解允许对优惠进行排名的AI模型
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 3%

---

# AI模型快速入门 {#ai-models}

[!DNL Journey Optimizer] 允许您使用经过培训的模型系统对选件进行排名，以显示给定的用户档案。

此功能允许您创建不同的 **AI模型** 基于您的业务目标。 在决策中使用这些基于目标的不同策略，经过培训的模型系统将帮助您了解不同的AI模型如何影响您的目标。

例如，您可以为电子邮件渠道选择一个AI模型，为推送渠道选择另一个AI模型。 对于每个渠道，经过培训的模型系统将利用多个数据点来确定在给定投放中应首先显示哪个选件，而不是考虑选件的优先级分数或 [排名公式](create-ranking-formulas.md).

## AI模型类型 {#ai-model-types}

在 [!DNL Journey Optimizer]:

* **自动优化模型** 旨在提供由业务客户设定的可最大化回报(KPI)的选件。 这些关键绩效指标可以是转化率、收入等形式。 此时，自动优化将重点放在通过选件转化作为我们的目标来优化选件点击量。 自动优化是非个性化的，并会根据选件的“全局”性能进行优化。 [了解详情](auto-optimization-model.md)

* **个性化模型** 允许您定义业务目标并利用客户数据来培训面向业务的模型，以提供个性化优惠并最大化KPI。 [了解详情](personalized-optimization-model.md)

>[!CAUTION]
>
>目前，只有选定用户才能提前使用个性化优化模型。

## 创建AI模型 {#create-ai-model}

创建和使用AI模型的主要步骤如下：

1. 创建将收集转化和展示事件的数据集。 [了解详情](create-dataset.md)
1. 创建一个AI模型，以利用数据集中的事件对选件进行排名。 [了解详情](create-ranking-strategies.md)
1. 配置选件架构以自动捕获事件。 [了解详情](schema-requirement.md)
1. 将AI模型分配给决策中的版面，以对符合条件的选件进行排名。 [了解详情](../offer-activities/configure-offer-selection.md)
