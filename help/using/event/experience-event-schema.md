---
title: 关于历程事件的ExperienceEvent架构
description: 了解旅程事件的ExperienceEvent模式
feature: Schemas
topic: Administration
role: Admin
level: Intermediate
exl-id: f19749c4-d683-4db6-bede-9360b9610eef
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 1%

---

# 关于ExperienceEvent架构(适用于 [!DNL Journey Optimizer] 事件 {#about-experienceevent-schemas}

[!DNL Journey Optimizer] 事件是通过流摄取发送到Adobe Experience Platform的XDM体验事件。

因此，为设置事件的重要先决条件 [!DNL Journey Optimizer] 您应该熟悉Adobe Experience Platform的体验数据模型（或XDM）、如何构建XDM体验事件架构，以及如何将XDM格式的数据流式传输到Adobe Experience Platform。

## 架构要求 [!DNL Journey Optimizer] 事件  {#schema-requirements}

设置事件的第一步 [!DNL Journey Optimizer] 是为了确保您定义了用于表示事件的XDM架构，并创建了一个数据集，用于记录Adobe Experience Platform上该事件的实例。 并非完全需要为事件创建一个数据集，但将事件发送到特定数据集将允许您维护用户的事件历史记录以供将来参考和分析，因此始终都是一个好主意。 如果您还没有适用于事件的架构和数据集，则可以在Adobe Experience Platform Web界面中完成这两项任务。

![](../assets/schema1.png)

将用于 [!DNL Journey Optimizer] 事件应满足以下要求：

* 架构必须是XDM ExperienceEvent类的。

   ![](../assets/schema2.png)

* 对于系统生成的事件，架构必须包含Orchestration eventID字段组。 [!DNL Journey Optimizer] 使用此字段标识历程中使用的事件。

   ![](../assets/schema3.png)

* 声明用于标识事件主题的标识字段。 如果未指定身份，则可以使用身份映射。 不建议采取此做法。

   ![](../assets/schema4.png)

* 如果希望此数据稍后在历程中可供查找，请标记配置文件的架构和数据集。

   ![](../assets/schema5.png)

   ![](../assets/schema6.png)

* 您可以随时包含数据字段，以捕获要随事件一起包含的任何其他上下文数据，例如有关用户、从中生成事件的设备的信息、位置，或与事件相关的任何其他有意义的环境。

   ![](../assets/schema7.png)

   ![](../assets/schema8.png)

## 利用架构关系{#leverage_schema_relationships}

Adobe Experience Platform允许您定义架构之间的关系，以便将一个数据集用作另一个数据集的查询表。

假设您的品牌数据模型有一个用于捕获购买的架构。 您还具有产品目录的架构。 您可以在购买架构中捕获产品ID，并使用关系从产品目录中查找更完整的产品详细信息。 例如，这样，您便可以为购买笔记本电脑的所有客户创建一个区段，而无需明确列出所有笔记本电脑ID或捕获事务系统中的每个产品详细信息。

要定义关系，您需要在源架构中具有专用字段，在此例中为购买架构中的产品ID字段。 此字段需要引用目标架构中的产品ID字段。 必须为用户档案启用源表和目标表，并且目标架构必须将该通用字段定义为其主标识。

以下是为将产品ID定义为主标识的用户档案启用的产品目录架构。

![](../assets/schema9.png)

以下是产品ID字段中定义的关系的购买架构。

![](../assets/schema10.png)

>[!NOTE]
>
>在 [Experience Platform文档](https://experienceleague.adobe.com/docs/platform-learn/tutorials/schemas/configure-relationships-between-schemas.html?lang=en).

在Journey Optimizer中，您随后可以利用链接表中的所有字段：

* 在配置业务或统一事件时， [了解更多](../event/experience-event-schema.md#unitary_event_configuration)
* 在历程中使用条件时， [了解更多](../event/experience-event-schema.md#journey_conditions_using_event_context)
* 在消息个性化中， [了解更多](../event/experience-event-schema.md#message_personalization)
* 在自定义操作个性化中， [了解更多](../event/experience-event-schema.md#custom_action_personalization_with_journey_event_context)

### 事件配置{#unitary_event_configuration}

关联的架构字段在统一和业务事件配置中可用：

* 浏览事件配置屏幕中的事件架构字段时。
* 定义系统生成事件的条件时。

![](../assets/schema11.png)

链接的字段不可用：

* 在事件键公式中
* 事件id条件（基于规则的事件）中

要了解如何配置单一事件，请参阅 [页面](../event/about-creating.md).

### 历程使用事件上下文的条件{#journey_conditions_using_event_context}

您可以使用来自查找表的数据来构建条件（表达式编辑器），该查询表链接到历程中使用的事件。

在历程中添加条件，编辑表达式并在表达式编辑器中展开事件节点。

![](../assets/schema12.png)

要了解如何定义旅程条件，请参阅 [页面](../building-journeys/condition-activity.md).

### 邮件个性化{#message_personalization}

个性化消息时，可使用链接的字段。 相关字段显示在从历程传递到消息的上下文中。

![](../assets/schema14.png)

要了解如何使用上下文历程信息个性化消息，请参阅此 [页面](../personalization/personalization-use-case.md).

### 使用历程事件上下文自定义操作个性化{#custom_action_personalization_with_journey_event_context}

配置历程自定义操作活动的操作参数时，可以使用链接的字段。

![](../assets/schema13.png)

要了解如何使用自定义操作，请参阅 [页面](../building-journeys/using-custom-actions.md).
