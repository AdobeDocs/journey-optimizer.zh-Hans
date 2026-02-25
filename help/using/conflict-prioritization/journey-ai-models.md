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
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 4%

---

# 使用AI模型排名历程 {#journey-ai-models}

>[!AVAILABILITY]
>
>此功能当前处于“有限可用”状态。 请联系 Adobe 代表获取访问权限。

[!DNL Adobe Journey Optimizer]可帮助您控制当用户档案符合超出系统允许范围的条件时，可以输入哪些历程。 为此，您可以使用[规则集](rule-sets.md)来定义历程进入或并发的上限。 当用户档案符合条件的历程超过上限允许时，分配给每个历程的优先级将确定选择哪些历程。

您可以使用&#x200B;**AI模型**，而不是使用优先级或排名公式，来根据经过训练的模型得分动态排名历程。 您可以从UI中的&#x200B;**[!UICONTROL 业务流程排名]**&#x200B;部分创建AI模型，并在规则集中使用它们以将它们应用于历程。

有关[!DNL Journey Optimizer]中可用的AI模型类型的概述，请参阅“决策”部分中的[AI模型入门](../experience-decisioning/ranking/ai-models.md#ai-model-types)。

## 创建 AI 模型 {#create-ai-model}

>[!CAUTION]
>
>要创建、编辑或删除AI模型，您必须具有&#x200B;**管理排名策略**&#x200B;权限。 [了解详情](../administration/high-low-permissions.md#manage-ranking-strategies)

要创建历程排名的AI模型，请执行以下步骤。

1. 创建将从中收集转化事件的数据集。 [了解如何操作](../experience-decisioning/data-collection/create-dataset.md)

1. 访问&#x200B;**[!UICONTROL 业务流程排名]**&#x200B;部分，然后选择&#x200B;**[!UICONTROL AI模型]**&#x200B;选项卡。 此时将显示之前创建的AI模型列表。

1. 单击&#x200B;**[!UICONTROL 创建AI模型]**。

1. 为AI模型指定唯一名称并根据需要指定描述。

   ![包含名称和描述字段的AI模型详细信息窗格](assets/journey-model-details.png){width="80%"}

   >[!NOTE]
   >
   >排名对象是将应用排名公式的实体。 默认情况下，排名对象设置为&#x200B;**[!UICONTROL 历程]**。

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)-->

1. **[!UICONTROL 优化量度]**&#x200B;部分提供有关AI模型使用的转化事件的信息。 [!DNL Journey Optimizer]排名基于&#x200B;**转化率** （转化率=转化事件总数/展示事件总数）。 兑换率使用以下方式计算：

   * **展示事件** （显示的项目）
   * **转化事件** （导致点击或转化的项目）

   这些事件是使用Web SDK或移动SDK自动捕获的。 在[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans)概述中了解详情。

1. 选择收集转化和印象事件的数据集。 在[本节](../experience-decisioning/data-collection/create-dataset.md)中了解如何创建此类数据集。

   ![为转化和印象事件选择数据集](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >下拉列表中仅显示从与&#x200B;**[!UICONTROL 体验事件 — 建议交互]**&#x200B;字段组（以前称为mixin）关联的架构创建的数据集。

1. &#x200B;<!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->选择要用于训练AI模型的区段。

   >[!NOTE]
   >
   >您最多可以选择5个受众。

1. 保存并激活AI模型。

现在，配置规则集时，AI模型可用。

## 将AI模型分配给规则集 {#assign-ai-model-to-ruleset}

要使用AI模型为您的历程排名，您需要在公式中使用它并将此公式分配给规则集。

1. 使用您创建的AI模型创建排名公式。 [了解如何操作](journey-ranking-formulas.md#create-journey-ranking-formula)

1. 从&#x200B;**[!UICONTROL 业务规则]**&#x200B;菜单中，创建要用于历程仲裁的规则集。 [了解如何操作](rule-sets.md#Create)

1. 确保选择&#x200B;**[!UICONTROL 历程]**&#x200B;域。

1. 在规则集属性中，将&#x200B;**[!UICONTROL 排名方法]**&#x200B;设置为&#x200B;**[!UICONTROL 公式]**（而不是&#x200B;**[!UICONTROL 优先级]**）。

1. 从下拉列表中选择使用您创建的AI模型的公式。

1. 创建要添加到规则集的历程上限规则。 [了解如何操作](journey-capping.md#create-rule)

1. 保存规则集。

现在，使用AI模型的公式已分配给规则集。 然后，您可以将该规则集应用于历程。

## 将规则集应用于历程 {#assign-rule-set-to-journey}

要将规则集分配给历程，请执行以下步骤。

1. 创建或打开要为其分配规则集的历程。 [了解如何创建历程](../building-journeys/journey-gs.md)

1. 在历程属性中，从下拉列表中选择规则集。 [了解如何操作](journey-capping.md#apply-capping)。

   >[!NOTE]
   >
   >一次只能将一个规则集应用于历程。

1. 保存历程。

在应用上限时，所有使用此规则集的历程将使用AI模型根据选定的公式进行排名。
