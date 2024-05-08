---
title: 在Experience Decisioning中利用上下文数据
description: 了解如何在Experience Decisioning中利用上下文数据
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="有限发布版"
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# 在Experience Decisioning中利用上下文数据 {#context}

借助Experience Decisioning，您可以利用Adobe Experience Platform中提供的任何信息来执行各种操作，例如创建 [决策规则](rules.md) 或 [排名公式](ranking.md). 例如，您可以设计一个决策规则，要求在发出决策请求时当前天气为≥80度。

>[!NOTE]
>
>上下文数据是在Adobe Experience Platform中定义的，在发出决策请求时发送。 它不包括历史数据。

要使用上下文数据，您首先需要定义要在Experience Decisioning中可用的数据。 完成后，此数据将无缝集成到中的Experience Decisioning **[!UICONTROL 上下文数据]** 选项卡创建决策规则时可用。 您还可以在编辑排名公式时利用数据。

![](assets/decision-rules-context.png)

使用Adobe Experience Platform数据馈送Experience Decisioning的步骤如下：

1. 创建 **体验事件架构**  Adobe Experience Platform及其关联的 **数据集**. [了解如何创建架构](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. 创建新的Adobe Experience Platform数据流：

   1. 导航至 **[!UICONTROL 数据流]** 菜单并选择 **[!UICONTROL 新建数据流]**.

   1. 在 **[!UICONTROL 事件架构]** 从下拉列表中，选择之前创建的Experience Event架构，然后单击 **[!UICONTROL 保存]**.

      ![](assets/decision-rule-context-datastream.png)

   1. 单击 **[!UICONTROL 添加服务]** 并选择“Adobe Experience Platform”作为服务。 在 **[!UICONTROL 事件数据集]** 下拉列表中，选择之前创建的事件数据集，并启用 **[!UICONTROL Adobe Journey Optimizer]** 选项。

      ![](assets/decision-rules-context-datastream-service.png)

保存数据流后，所选数据集的信息将自动获取并集成到Experience Decisioning中，通常在大约24小时内变为可用。

有关如何使用Adobe Experience Platform的进一步指导，请探索以下资源：

* [体验数据模型(XDM)架构](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [数据集](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [数据流](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
