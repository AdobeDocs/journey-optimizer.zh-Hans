---
product: experience platform
solution: Experience Platform
title: 创建 AI 模型
description: 了解如何创建AI模型来对优惠进行排名
feature: Ranking, Decision Management
role: User
level: Intermediate
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 15%

---

# 构建AI模型 {#create-ai-models}

[!DNL Journey Optimizer]允许您创建&#x200B;**AI模型**，以根据您的业务目标对优惠进行排名。

>[!CAUTION]
>
>要创建、编辑或删除AI模型，您必须具有&#x200B;**管理排名策略**&#x200B;权限。 [了解详情](../../administration/high-low-permissions.md#manage-ranking-strategies)

## 创建 AI 模型 {#create-ranking-strategy}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_metric"
>title="优化量度"
>abstract="[!DNL Journey Optimizer] 根据&#x200B;**转化率**&#x200B;对产品建议进行排名（转化率 = 转化事件总数/展示事件总数）。转化率使用两种类型的量度来计算：**展示事件**（显示的产品建议）和&#x200B;**转化事件**（通即通过电子邮件或网站点击的产品建议）。这些事件是使用已提供的 Web SDK 或 Mobile SDK 自动捕获的。"

要创建AI模型，请执行以下步骤：

1. 创建将从中收集转化事件的数据集。 [了解如何操作](../data-collection/create-dataset.md)

1. 导航到&#x200B;**[!UICONTROL 决策]** > **[!UICONTROL 策略设置]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL AI模型]**。

   ![](../assets/ai-model-list.png)

   将列出迄今为止创建的所有AI模型。

1. 单击&#x200B;**[!UICONTROL 创建AI模型]**&#x200B;按钮。

1. 为AI模型指定唯一名称并根据需要指定描述。

1. 选择要创建的AI模型类型：

   * **[!UICONTROL 自动优化]**&#x200B;根据过去的选件性能优化选件。 [了解详情](auto-optimization-model.md)
   * **[!UICONTROL 个性化优化]**&#x200B;根据受众和优惠表现优化和个性化优惠。 [了解详情](personalized-optimization-model.md)

   ![](../assets/ai-model-types.png)

1. **[!UICONTROL 优化量度]**&#x200B;部分提供有关AI模型用于计算优惠排名的转化事件的信息。

   [!DNL Journey Optimizer] 根据&#x200B;**转化率**&#x200B;对产品建议进行排名（转化率 = 转化事件总数/展示事件总数）。转化率使用两种类型的量度进行计算：
   * **展示事件** （显示的优惠）
   * **转化事件** （通过电子邮件或Web导致点击的选件）。

   这些事件是使用Web SDK或提供的Mobile SDK自动捕获的。 在[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans)概述中了解详情。

+++ 正在自定义[!DNL Customer Journey Analytics]量度上优化模型

   >[!NOTE]
   >
   >此功能仅适用于具有管理员权限的[!DNL Customer Journey Analytics]客户。
   >
   >在开始之前，请确保已将Journey Optimizer与Customer Journey Analytics集成，以便将Journey Optimizer数据集导出到默认数据视图。 [了解如何在 [!DNL Customer Journey Analytics]](../../reports/cja-ajo.md)中利用 [!DNL Journey Optmizer] 数据

   **[!UICONTROL 个性化优化]**&#x200B;模型是一种AI模型，它允许您定义业务目标，并利用客户数据来训练面向业务的模型以提供个性化优惠并最大化KPI。

   默认情况下，个性化优化模型使用&#x200B;**优惠点击次数**&#x200B;作为优化量度。 如果您正在使用[!DNL Customer Journey Analytics]，[!DNL Decisioning]允许您利用自己的自定义量度来优化您的模型。

   为此，请选择&#x200B;**[!UICONTROL 个性化优化]**&#x200B;模型类型并展开&#x200B;**[!UICONTROL 转化事件]**&#x200B;下拉列表。 默认[!DNL Customer Journey Analytics] [数据视图](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-dataviews/data-views){target="_blank"}中的所有量度都会显示在列表中。 选择要优化模型的量度。

   ![](../assets/ai-model-custom-metrics.png){width=85%}

   >[!NOTE]
   >
   >默认情况下，[!DNL Customer Journey Analytics]中的量度使用“最后接触”归因模型，该模型将100%的点数分配给转化前最近发生的接触点。
   >
   >虽然可以修改归因模型，但并非所有的归因模型都适合用于人工智能模型优化。 我们建议仔细选择与您的优化目标一致的归因模型，以确保模型准确性和性能。
   >
   >有关可用归因模型及其使用指南的更多详细信息，请参阅[[!DNL Customer Journey Analytics] 文档](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-dataviews/component-settings/attribution){target="_blank"}

+++

1. 选择收集转化和印象事件的数据集。 在[本节](../data-collection/create-dataset.md)中了解如何创建此类数据集。

   ![](../assets/ai-model-datasets.png){width=85%}

   >[!CAUTION]
   >
   >下拉列表中仅显示从与&#x200B;**[!UICONTROL 体验事件 — 建议交互]**&#x200B;字段组（以前称为mixin）关联的架构创建的数据集。

1. 如果您正在创建&#x200B;**[!UICONTROL 个性化优化]** AI模型，请选择要用于训练AI模型的区段。

   <!--➡️ [Discover this feature in video](#video)-->

   >[!NOTE]
   >
   >您最多可以选择5个受众。

1. 保存并激活AI模型。

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

现在，每次显示和/或单击优惠时，您都希望&#x200B;**[!UICONTROL 体验事件 — 建议交互]**&#x200B;字段组使用[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=zh-Hans#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"}或Mobile SDK自动捕获相应的事件。

为了能够在事件类型（显示优惠或单击优惠）中发送，您必须为发送到Adobe Experience Platform的体验事件中的每个事件类型设置正确的值。 [了解如何操作](../data-collection/schema-requirement.md)

<!--
## How-to video {#video}

Learn how to create a personalized optimization model and how to apply it to a decision.

>[!VIDEO](https://video.tv.adobe.com/v/3445961?quality=12&captions=chi_hans)-->
