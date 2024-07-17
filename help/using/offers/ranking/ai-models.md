---
product: experience platform
solution: Experience Platform
title: AI模型入门
description: 了解允许对优惠进行排名的AI模型
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 260b9ec0a70526ac37da444e183fc1d01b97b22b
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 14%

---

# AI模型入门 {#ai-models}

[!DNL Journey Optimizer]允许您使用经过训练的模型系统，对要针对给定配置文件显示的选件进行排名。

此功能允许您根据业务目标创建不同的&#x200B;**AI模型**。 在决策中使用这些不同的基于目标的策略，训练有素的模型系统将帮助您了解不同的AI模型如何影响您的目标。

例如，您可以为电子邮件渠道选择一个AI模型，为推送渠道选择另一个模型。 对于每个渠道，经过训练的模型系统将利用多个数据点来确定在给定投放位置应首先显示哪个优惠，而不是考虑优惠的优先级得分或[排名公式](create-ranking-formulas.md)。

>[!IMPORTANT]
>
>目前，Journey Optimizer创作渠道不支持排名模型。

## AI 模型类型  {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="选择模型类型"
>abstract="选择您要创建的 AI 模型类型：**自动优化**&#x200B;可以根据过去的性能表现优化选件，而&#x200B;**个性化优化**&#x200B;则可以根据受众和选件性能来对选件进行优化和个性化。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="创建 AI 模型"

[!DNL Journey Optimizer]中提供了两种类型的AI模型：

* **自动优化模型**&#x200B;旨在提供可最大化业务客户端设置的回报(KPI)的优惠。 这些KPI可以采用转化率、收入等形式。 目前，自动优化侧重于优化优惠点击次数，并将优惠转化作为我们的目标。 自动优化是一种非个性化的功能，可根据选件的“全局”性能进行优化。 [了解详情](auto-optimization-model.md)

* **个性化优化模型**&#x200B;允许您定义业务目标，并利用客户数据来训练面向业务的模型以提供个性化优惠并最大化KPI。 [了解详情](personalized-optimization-model.md)

## 创建AI模型 {#create-ai-model}

创建和使用AI模型的主要步骤如下：

1. 创建将从中收集转化和印象事件的数据集。 [了解详情](../data-collection/create-dataset.md)

1. 创建一个AI模型，该模型将利用数据集中的事件对选件进行排名。 [了解详情](create-ranking-strategies.md)

1. 配置选件架构以自动捕获事件。 [了解详情](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >排名模型要求将反馈事件作为体验事件发送以便进行收集。 [了解有关决策管理数据收集的更多信息](../data-collection/data-collection.md)

1. 将AI模型分配给决策中的投放位置，为符合条件的优惠排名。 [了解详情](../offer-activities/configure-offer-selection.md)
