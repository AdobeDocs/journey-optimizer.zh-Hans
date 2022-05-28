---
product: experience platform
solution: Experience Platform
title: AI模型快速入门
description: 了解允许对优惠进行排名的AI模型
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 3%

---

# AI模型快速入门 {#ai-models}

[!DNL Journey Optimizer] 允许您使用经过培训的模型系统对选件进行排名，以显示给定的用户档案。

此功能允许您创建不同的 **AI模型** 基于您的业务目标。 在决策中使用这些基于目标的不同策略，经过培训的模型系统将帮助您了解不同的AI模型如何影响您的目标。

例如，您可以为电子邮件渠道选择一个AI模型，为推送渠道选择另一个AI模型。 对于每个渠道，经过培训的模型系统将利用多个数据点来确定在给定投放中应首先显示哪个选件，而不是考虑选件的优先级分数或 [排名公式](create-ranking-formulas.md).

## AI模型类型 {#ai-model-types}

目前， [!DNL Journey Optimizer]**提供了一个AI模型， **自动优化**，可根据过去的选件性能优化选件。 此类AI模型的详细信息可在 [此部分](auto-optimization-model.md).

## 创建AI模型 {#create-ai-model}

创建和使用AI模型的主要步骤如下：

1. 创建将收集转化和展示事件的数据集。 [了解详情](create-dataset.md)
1. 创建一个AI模型，以利用数据集中的事件对选件进行排名。 [了解详情](create-ranking-strategies.md)
1. 配置选件架构以自动捕获事件。 [了解详情](schema-requirement.md)
1. 将AI模型分配给决策中的版面，以对符合条件的选件进行排名。 [了解详情](../offer-activities/configure-offer-selection.md)
