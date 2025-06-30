---
product: experience platform
solution: Experience Platform
title: AI模型入门
description: 了解允许对优惠进行排名的AI模型
feature: Ranking, Decision Management
role: User
level: Intermediate
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 18%

---

# AI模型入门 {#ai-models}

[!DNL Journey Optimizer]允许您使用经过训练的模型系统，对要针对给定配置文件显示的选件进行排名。

此功能允许您根据业务目标创建不同的&#x200B;**AI模型**。 在决策中使用这些不同的基于目标的策略，训练有素的模型系统将帮助您了解不同的AI模型如何影响您的目标。

<!--For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.-->

## AI 模型类型 {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_type"
>title="选择模型类型"
>abstract="选择您要创建的 AI 模型类型：**自动优化**&#x200B;可以根据过去的性能表现优化产品建议，而&#x200B;**个性化优化**&#x200B;则可以根据受众和产品建议性能来对产品建议进行优化和个性化。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="创建 AI 模型"

[!DNL Journey Optimizer]中提供了两种类型的AI模型：

* **自动优化模型**&#x200B;旨在提供可最大化业务客户端设置的回报(KPI)的优惠。 这些KPI可以采用转化率、收入等形式。 目前，自动优化侧重于优化优惠点击次数，并将优惠转化作为我们的目标。 自动优化是一种非个性化的功能，可根据选件的“全局”性能进行优化。 [了解详情](auto-optimization-model.md)

* **个性化优化模型**&#x200B;允许您定义业务目标，并利用客户数据来训练面向业务的模型以提供个性化优惠并最大化KPI。 [了解详情](personalized-optimization-model.md)

## 构建AI模型 {#create-ai-model}

能够创建和使用AI模型的主要步骤如下：

1. 创建将从中收集转化和印象事件的数据集。 [了解详情](../data-collection/create-dataset.md)

1. 创建一个AI模型，该模型将利用数据集中的事件对选件进行排名。 [了解详情](create-ai-models.md)

1. 配置选件架构以自动捕获事件。 [了解详情](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >排名模型要求将反馈事件作为体验事件发送以便进行收集。 [了解有关Decisioning数据收集的更多信息](../data-collection/data-collection.md)

1. 将AI模型分配给选择策略来对符合条件的优惠进行排名。 [了解详情](../selection-strategies.md#select-ranking-method)
