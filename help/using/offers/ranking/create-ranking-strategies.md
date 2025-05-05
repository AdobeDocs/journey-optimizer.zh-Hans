---
product: experience platform
solution: Experience Platform
title: 创建 AI 模型
description: 了解如何创建AI模型来对优惠进行排名
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 23%

---

# 创建 AI 模型 {#ai-rankings}

[!DNL Journey Optimizer]允许您创建&#x200B;**AI模型**，以根据您的业务目标对优惠进行排名。

>[!CAUTION]
>
>要创建、编辑或删除AI模型，您必须具有&#x200B;**管理排名策略**&#x200B;权限。 [了解详情](../../administration/high-low-permissions.md#manage-ranking-strategies)

## 创建 AI 模型 {#create-ranking-strategy}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_metric"
>title="优化量度"
>abstract="[!DNL Journey Optimizer] 根据&#x200B;**转化率**&#x200B;对产品建议进行排名（转化率 = 转化事件总数/展示事件总数）。转化率使用两种类型的量度来计算：**展示事件**（显示的产品建议）和&#x200B;**转化事件**（通即通过电子邮件或网站点击的产品建议）。这些事件是使用已提供的 Web SDK 或 Mobile SDK 自动捕获的。"

要创建AI模型，请执行以下步骤：

1. 创建将从中收集转化事件的数据集。 [了解如何操作](../data-collection/create-dataset.md)

1. 在&#x200B;**[!UICONTROL 组件]**&#x200B;菜单中，访问&#x200B;**[!UICONTROL 排名]**&#x200B;选项卡，然后选择&#x200B;**[!UICONTROL AI模型]**。

   ![](../assets/ai-ranking-list.png)

   将列出迄今为止创建的所有AI模型。

1. 单击&#x200B;**[!UICONTROL 创建AI模型]**&#x200B;按钮。

1. 为AI模型指定唯一的名称和描述，然后选择要创建的AI模型类型：

   * **[!UICONTROL 自动优化]**&#x200B;根据过去的选件性能优化选件。 [了解详情](auto-optimization-model.md)
   * **[!UICONTROL 个性化优化]**&#x200B;根据受众和优惠表现优化和个性化优惠。 [了解详情](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >**[!UICONTROL 优化量度]**&#x200B;部分提供有关AI模型用于计算优惠排名的转化事件的信息。
   >
   >[!DNL Journey Optimizer] 根据&#x200B;**转化率**&#x200B;对产品建议进行排名（转化率 = 转化事件总数/展示事件总数）。转化率使用两种类型的量度进行计算：
   >* **展示事件** （显示的优惠）
   >* **转化事件** （通过电子邮件或Web导致点击的选件）。
   >
   >这些事件是使用Web SDK或提供的Mobile SDK自动捕获的。 请在[Adobe Experience Platform Web SDK概述](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=zh-Hans)中进一步了解此信息。

1. 选择收集转化和印象事件的数据集。 了解如何在[此部分](../data-collection/create-dataset.md)中创建此类数据集。<!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >下拉列表中仅显示从与&#x200B;**[!UICONTROL 体验事件 — 建议交互]**&#x200B;字段组（以前称为mixin）关联的架构创建的数据集。

1. 如果您正在创建&#x200B;**[!UICONTROL 个性化优化]** AI模型，请选择要用于训练AI模型的区段。

   ➡️ [在视频中了解此功能](#video)

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >您最多可以选择5个受众。

1. 保存并激活AI模型。

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

现在，每次显示和/或单击优惠时，您都希望&#x200B;**[!UICONTROL 体验事件 — 建议交互]**&#x200B;字段组使用[Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=zh-Hans#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"}或Mobile SDK自动捕获相应的事件。

为了能够在事件类型（显示优惠或单击优惠）中发送，您必须为发送到Adobe Experience Platform的体验事件中的每个事件类型设置正确的值。 [了解如何操作](../data-collection/schema-requirement.md)

## 操作方法视频 {#video}

了解如何创建个性化优化模型以及如何将其应用于决策。

>[!VIDEO](https://video.tv.adobe.com/v/3419954?quality=12)
