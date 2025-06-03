---
solution: Journey Optimizer
product: journey optimizer
title: 关于 Adobe Experience Platform 受众
description: 了解如何使用 Adobe Experience Platform 受众
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 3ec496ba-7555-49e2-992c-403c33302a90
source-git-commit: b6fe3fec0c64983fc2317027a5748a0d44c18469
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 3%

---

# 使用受众扩充属性 {#enrichment}

当定位通过组合工作流、自定义（CSV文件）受众或联合受众组合生成的受众时，您可以使用这些受众中的扩充属性来构建历程并个性化消息。

>[!NOTE]
>
>在2024年10月1日之前通过CSV文件自定义上传创建的受众不符合个性化条件。 要使用这些受众中的属性并充分利用此功能，请重新创建并重新上传在此日期之前导入的任何外部CSV受众。
>
>同意策略不支持扩充属性。 因此，任何同意策略规则都应仅基于在配置文件中找到的属性。

您可以使用受众的扩充属性执行以下操作：

* **根据利用目标受众的扩充属性的规则，在历程中创建多个路径**。 为此，请使用[读取受众](../building-journeys/read-audience.md)活动定位受众，然后根据受众的扩充属性在[条件](../building-journeys/condition-activity.md)活动中创建规则。

  ![](assets/audience-enrichment-attribute-condition.png){width="70%" zoomable="yes"}

* 通过在个性化编辑器中添加来自目标受众的扩充属性，在历程或营销活动中&#x200B;**个性化您的消息**。 [了解如何使用个性化编辑器](../personalization/personalization-build-expressions.md)

  ![](assets/audience-enrichment-attribute-perso.png){width="70%" zoomable="yes"}

>[!IMPORTANT]
>
>要使用通过组合工作流创建的受众中的扩充属性，请确保将这些属性添加到“ExperiencePlatform”数据Source中的字段组。
>
>+++ 了解如何将扩充属性添加到字段组>
>
>1. 导航到“管理”>“配置”>“数据源”。
>1. 选择“Experience Platform”并创建或编辑字段组。
>1. 在架构选择器中，选择相应的架构。 架构的名称将遵循以下格式：“audienceId的架构：”+受众的ID。 您可以在受众库中的受众详细信息屏幕上找到受众ID。
>1. 打开字段选择器，查找要添加的扩充属性，然后选中这些属性旁边的复选框。
>1. 保存更改。
>1. 将扩充属性添加到字段组后，您可以在Journey Optimizer中以上列出的位置使用它们。
>
>有关数据源的详细信息，请参阅以下部分：
>
>* [使用Adobe Experience Platform数据源](../datasource/adobe-experience-platform-data-source.md)
>* [配置数据源](../datasource/configure-data-sources.md)
>
>+++







+++ 什么是扩充属性？

扩充属性是额外的上下文属性，特定于受众。 它们与用户档案无关，通常用于个性化目的。

扩充属性通过受众构成中的扩充活动或自定义上传过程链接到受众。

+++

+++ 在Journey Optimizer中，可在何处使用扩充属性？

可在以下方面利用受众组合中的扩充属性。 [了解如何使用受众扩充属性](#enrichment)

* 条件活动(历程)
* 自定义操作属性(历程)
* 消息个性化(历程和营销活动)

+++

+++ 如何在历程中启用扩充属性？

要使用通过组合工作流创建的受众中的扩充属性，请确保将这些属性添加到“ExperiencePlatform”数据Source中的字段组。 有关如何向字段组添加扩充属性的信息，请参阅[此部分](#enrichment)

+++

+++ 扩充属性值是否在历程开始后更新？

当前不支持。 即使在等待或事件节点之后，扩充属性值仍与历程开始时相同。

+++
