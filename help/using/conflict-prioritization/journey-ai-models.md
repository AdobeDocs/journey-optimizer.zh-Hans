---
title: 历程仲裁人工智能模型
description: 了解如何创建并使用AI模型来排名要仲裁的历程，以便根据人工智能驱动的分数为每个用户档案选择最佳历程。
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="有限发布版" type="Informative"
hide: true
hidefromtoc: true
exl-id: 3e7c3069-b022-4709-936d-acaad56b5882
source-git-commit: a1b9d589773c168cc8ad0cfac0cd1ba178ae4bb6
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 4%

---

# 使用AI模型排名历程 {#journey-ai-models}

>[!AVAILABILITY]
>
>此功能当前处于“有限可用”状态。 请联系 Adobe 代表获取访问权限。

[!DNL Adobe Journey Optimizer]可帮助您控制当用户档案符合超出系统允许范围的条件时，可以输入哪些历程。 为此，您可以使用[规则集](rule-sets.md)来定义历程进入或并发的上限。 当用户档案符合条件的历程超过上限允许时，分配给每个历程的优先级将确定选择哪些历程。

您还可以使用排名公式中的&#x200B;**AI模型**，而不是使用优先级，以根据经过训练的模型得分动态排名历程。

## 创建 AI 模型 {#create-ai-model}

<!--Do you need specific permissions to create AI models?
>[!CAUTION]
>
>To create, edit, or delete AI models, you must have the **Manage Ranking Strategies** permission. [Learn more](../administration/high-low-permissions.md#manage-ranking-strategies)-->

要创建历程排名的AI模型，请执行以下步骤。

1. 创建将从中收集转化事件的数据集。 [了解如何操作](../experience-decisioning/data-collection/create-dataset.md)

1. 访问&#x200B;**[!UICONTROL 业务流程排名]**&#x200B;部分，然后选择&#x200B;**[!UICONTROL AI模型]**&#x200B;选项卡。 此时将显示之前创建的AI模型列表。

1. 单击&#x200B;**[!UICONTROL 创建AI模型]**。

1. 为AI模型指定唯一名称并根据需要指定描述。

   ![显示名称和描述字段的AI模型详细信息](assets/journey-model-details.png){width="85%"}

   >[!NOTE]
   >
   >排名对象是将应用排名公式的实体。 默认情况下，排名对象设置为&#x200B;**[!UICONTROL 历程]**。

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)-->

1. 在&#x200B;**[!UICONTROL 优化量度]**&#x200B;部分中，默认[!DNL Customer Journey Analytics] [数据视图](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"}中的所有量度都显示在列表中。 选择要优化模型的量度。

   ![优化指标下拉列表列出了AI模型的Customer Journey Analytics指标](assets/journey-model-metrics.png){width="70%"}

   [!DNL Journey Optimizer]排名基于&#x200B;**转化率** （转化率=转化事件总数/展示事件总数）。 兑换率使用以下方式计算：

   * **展示事件** （显示的项目）
   * **转化事件** （导致点击或转化的项目）

   这些事件是使用Web SDK或移动SDK自动捕获的。 在[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans)概述中了解详情。

1. 选择收集转化和印象事件的数据集。 在[本节](../experience-decisioning/data-collection/create-dataset.md)中了解如何创建此类数据集。

   ![为转化和印象事件选择数据集](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >下拉列表中仅显示从与&#x200B;**[!UICONTROL 体验事件 — 建议交互]**&#x200B;字段组关联的架构创建的数据集。 您最多可以选择5个数据集。

1. &#x200B;<!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->选择要用于训练AI模型的区段。

   >[!NOTE]
   >
   >您最多可以选择50个受众。

1. 保存并激活AI模型。

现在，在创建排名公式时，可以选择AI模型。

## 在公式中引用AI模型来对历程进行排名 {#reference-ai-model}

您现在可以将AI模型设置为引用，以构建排名公式，然后将公式分配给规则集并将规则集应用于历程。 要实现此目的，请执行以下步骤。

1. 创建排名公式。 [了解如何操作](journey-ranking-formulas.md#create-journey-ranking-formula)

1. 使用&#x200B;**[!UICONTROL 选择AI模型]**&#x200B;按钮选择要在公式中使用的AI模型。

   使用“选择AI模型”按钮![历程排名公式详细信息](assets/journey-formula-ai-model.png){width="80%"}

1. 在&#x200B;**[!UICONTROL 标准]**&#x200B;的至少一个部分中，定义一个条件并选择&#x200B;**[!UICONTROL AI模型得分]**&#x200B;作为排名方法。 例如，如果历程具有“促销”标记，则排名分数是AI模型分数。

   ![促销标记标准使用AI模型得分作为排名方法的排名公式示例](assets/journey-formula-ex-2.png){width="60%"}

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;以完成排名公式。

1. 现在，创建一个规则集并选择您创建的公式作为排名方法。 [了解如何操作](journey-ranking-formulas.md#assign-formula-to-ruleset)

1. 创建历程上限规则并保存规则集。

1. 将规则集应用于所需历程并保存它们。 [了解如何操作](journey-ranking-formulas.md#assign-rule-set-to-journey)

   >[!NOTE]
   >
   >一次只能将一个规则集应用于历程。

在应用cap时，使用此规则集的所有旅程将使用引用所选AI模型的公式进行排名。
