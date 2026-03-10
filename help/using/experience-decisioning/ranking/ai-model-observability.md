---
solution: Journey Optimizer
product: Journey Optimizer
title: AI模型监测
description: 监测AI排名模型的运行状况、培训状态和个性化优化模型的性能
feature: Ranking, Decisioning
topic: Artificial Intelligence
role: User
level: Intermediate
version: Journey Orchestration
source-git-commit: e329c221fa714747d50495e466d02e75bed2967c
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 2%

---

# 监控您的AI模型 {#ai-model-observability}

无论您是营销人员、数据科学家还是决策管理员，了解您的个性化优化模型的表现和行为方式都可以帮助您使用AI为每个客户选择最佳选件。

为此，您可以直接在[!DNL Journey Optimizer]中监视AI模型的运行状况、培训状态和演变。

这让您清楚地了解模型是否正常工作、模型上次培训的时间、培训期间发生的情况、模型如何推动业务成果（例如，转化或收入），以及模型不工作时进行故障排除<!-- (for example, unexpected decision item count, training data date range, or insufficient events)-->。

>[!AVAILABILITY]
>
>当前，仅对[个性化优化](personalized-optimization-model.md)模型支持此功能。

➡️ [通过观看视频了解此功能](#video)

## 查看培训状态 {#from-ai-model-list}

一旦模型设置为实时，它就会进入持续的生命周期：收集数据并定期重新训练模型以优化选件排名。 您可以在AI模型列表中检查个性化优化模型的训练状态。

1. 转到&#x200B;**[!UICONTROL 决策]** > **[!UICONTROL 策略设置]** > **[!UICONTROL AI模型]**&#x200B;以打开AI模型清单。

1. 您可以查看所有可用的AI模型及其状态。

1. 对于个性化优化类型的每个&#x200B;**[!UICONTROL Live]** AI模型，有两列可让您看到：
   * 上次训练作业运行时间（**[!UICONTROL 上次训练时间]**），并且
   * 每个模型是否已成功训练（**[!UICONTROL 训练结果]**）。

   ![](../assets/ai-model-list-training.png)

   这使您能够快速识别需要进一步调查或故障排除的模型。

## 访问模型状态报表 {#access-ai-model-details}

从列表中单击进入个性化优化AI模型。 从该位置，您可以查看以下列出的元素：

* **[!UICONTROL 当前部署的模型]** — 此部分显示当前部署的模型、其部署时间、它使用的数据的日期范围、包含并个性化的决策项（选件）的数量，以及当前跨子模型的流量分配<!-- (random exploration, new offer booster?, contextual bandit, neural network)-->。

  ![](../assets/ai-model-deployed-model.png)

  在此示例中，该模型被训练在五个决策项上，并且模型具有足够的流量来针对三个决策项开发个性化预测。 其余两个决策项目是随机提供的。

  您还可以看到该模型当前将40%的流量分配给个性化神经网络，40%的流量分配给上下文老虎机，20%的流量分配给随机探索。

* **[!UICONTROL 上次培训作业]** — 此部分显示上次培训作业的状态、运行时间以及所有错误消息。 [了解有关错误状态的更多信息](#check-for-error-states)

  ![](../assets/ai-model-last-training-job.png)

  在此示例中，您可以观察到，已部署的模型与预期的培训作业匹配。

* **[!UICONTROL 属性]** — 此部分显示模型的属性，例如使用的数据集、优化量度和用于训练个性化优化模型的受众。

  ![](../assets/ai-model-properties.png)

  单击&#x200B;**[!UICONTROL 编辑属性]**&#x200B;以修改这些元素。 您将被重定向到创建AI模型屏幕。 [了解详情](create-ai-models.md)

* **[!DNL Model performance]** — 此部分显示随时间变化的模型每个分支的性能，例如每个子模型的流量分配和转化率。 您可以在&#x200B;**最近7天**&#x200B;和&#x200B;**最近30天**&#x200B;之间切换。 提升度和统计重要性是指示模型是否实际改善了营销结果的关键指标。

  ![](../assets/ai-model-performance.png)

  在此示例中，您可以看到在过去30天内，个性化子模型的转化率提升了60%以上，而且这种提升在统计上是显着的，这意味着此AI模型正对您的业务产生重大影响。

* **[!UICONTROL 随时间变化的模型流量分配]** — 此部分显示模型随时间的演变。 首次部署模型时，100%的流量是随机的，因为尚未收集选件数据。 在第一次重新训练后，流量通常会转向个性化胳膊。

  ![](../assets/ai-model-trafic-allocation.png)

  在此示例中，您可以看到随着模型的重新训练，流量分配已从100%随机探索转变为神经网络和上下文盗用型流量。

## 了解训练错误 {#check-for-error-states}

要查看上次训练作业失败的个性化优化AI模型的错误详细信息，请执行以下步骤。

1. 从列表中单击进入模型。 将显示模型状态详细信息。

   ![](../assets/ai-model-no-model-deployed.png){width="95%"}

   在此示例中，您可以看到由于上一个训练作业失败，未部署任何模型。

   >[!NOTE]
   >
   >当未部署模型时，使用统一的随机流量分配提供决策请求。

1. 查看&#x200B;**[!UICONTROL 上次训练作业]**&#x200B;部分中的错误详细信息。

   ![](../assets/ai-model-training-job-failed.png){width="70%"}

   当为此模型选择的数据集内没有反馈事件时，训练作业通常会失败。 这意味着您需要填充数据集或选择具有适当转化事件的新数据集。

1. 您可以检查在模型的&#x200B;**[!UICONTROL 属性]**&#x200B;中选择的数据集。 单击&#x200B;**[!UICONTROL 编辑属性]**&#x200B;以选择另一个数据集。 [了解详情](create-ai-models.md)

   ![](../assets/ai-model-properties-edit-dataset.png){align="left" width="45%"}

## 常见问题 {#faq}

+++ 我可以监控哪些AI模型？

当前仅支持[个性化优化](personalized-optimization-model.md)模型的AI模型监视。 其他排名模型类型尚未公开模型状态报表。
+++

+++ 为什么我的模特培训工作失败了？

当为模型选择的数据集没有或只有很少的反馈（转化）事件时，培训作业通常会失败。 查看&#x200B;**[!UICONTROL 上次训练作业]**&#x200B;部分以了解错误详细信息，然后查看模型的&#x200B;**[!UICONTROL 属性]**&#x200B;以确认数据集和优化量度。 使用正确的事件填充该数据集，或[选择包含相应转化数据的其他数据集](create-ai-models.md)。
+++

+++ AI模型监测与营销活动和历程报告有何关系？

AI模型监测与活动或历程报告不同。 单个AI模型可以跨多个营销活动或多个历程使用，并且营销活动或历程报表不显示用于给定投放的模型。 使用AI模型状态监视来了解和监视模型本身；将[活动报告](../../reports/campaign-global-report-cja.md)和[历程报告](../../reports/journey-global-report-cja.md)用于投放级别的量度。
+++

+++ 我的优化量度是一个连续量度（如收入或订单值），而不是二进制量度（如点击次数或转化次数）。 如何解释报告的转化率和转化率值？

当使用连续量度（如收入或订单值）时，该模型尝试预测与给定优惠呈现相关的估计值（而不是转换概率）。 报告的“转化”值是与每个模型栏中记录的选件显示关联的总收入（或订单值）。 报告的“转化率”是转化值除以显示值，在连续量度的情况下可能超过100%。
+++

+++ 提升度的重要性是什么？

提升度重要性是报告的提升度与随机探索的统计意义。 显着性使用比例差异的卡方检验进行计算，该结果与两个人口比例的Z检验的显着性计算相同。
+++

+++ 什么是模型基尼指数？ 基尼指数的“好”值是多少？

模型基尼指数（也称为基尼系数）是模型预测能力的离线度量。 模型基尼指数介于0（无预测能力）到1（完美预测每个客户每个选件的转化或量度值）之间。 没有通用的“好”基尼指数值，因为不同的决策用例导致不同的用户行为，从而不同的模型结果。 在同一用例中，基尼指数值越高表示模型质量越高。
+++

+++ 基尼指数是如何计算的？

每个模型臂的基尼指数的计算方式各不相同，具体取决于优化量度是二进制还是连续：

**二进制优化量度**（例如点击次数、订购次数）：基尼指数是根据接收方操作特性(ROC)曲线的曲线(AUC)下的面积计算的，通常称为ROC AUC或简称为AUC。 ROC AUC的范围从0.5（具有零预测能力的随机模型）到1.0（完美预测能力）。 使用公式Gini = 2 x (ROC AUC) - 1将ROC AUC转换为基尼指数。

**连续优化量度**（例如收入、订单值）：基尼指数的计算基于与模型的累积预测正值相对于群体中累积真实正值关联的Lorenz曲线下的区域。 Lorenz曲线下方的面积介于0.0（完美预测能力）到0.5（零预测能力的随机模型）之间。 使用公式Gini = 1 - 2 x (Lorenz AUC)将Lorenz AUC转换为Gini索引。
+++

+++ 衡量模型质量的更好指标是基尼指数还是提升/提升显着性？

通常情况下，模型质量的在线测量，如升程和升程显着性，被认为是测量模型质量的“黄金标准”方法。 据报告，基尼指数为评估决策模型的客户数据科学团队提供额外的数据点。
+++

<!--
## Understanding statuses and errors {#statuses-errors}

* **Success** – The latest training job completed successfully. The model is trained and deployed for ranking.
* **Failed** – The latest training job failed (for example, no events in the datasets). The UI shows an error message and a request ID; use these when troubleshooting or contacting support.
* **In progress** – A training job is running. Some metrics may be temporarily unavailable until it finishes.
* **Pending** – No result yet (for example, model recently activated or settings recently changed).

If no model has been successfully deployed yet, the "currently deployed model" section and some performance fields will be empty or show the initial-state messaging.-->

## 操作方法视频 {#video}

了解如何在[!DNL Journey Optimizer]中监视您的AI排名模型并解释培训状态和表现。

>[!VIDEO](https://video.tv.adobe.com/v/3479859?captions=chi_hans&quality=12)

## 相关文档 {#related}

* [关于 AI 模型](ai-models.md)
* [个性化优化模型](personalized-optimization-model.md)
* [创建 AI 模型](create-ai-models.md)
* [创建数据集以收集事件](../data-collection/create-dataset.md)
