---
solution: Journey Optimizer
product: journey optimizer
title: 在编排的营销活动中添加个性化
description: 了解如何使用用户档案属性、工作表中的目标属性以及扩充收集数组，个性化编排的营销活动消息。
exl-id: c4a91e2b-6f08-4d1a-9e3b-2f8f5a0d1c62
version: Campaign Orchestration
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: e0a12bd7971c778378f9905cf93653792f38509d
workflow-type: tm+mt
source-wordcount: 477
ht-degree: 0%

---

# 在编排的营销活动中添加个性化 {#add-personalization}

在您[在画布上编排活动](orchestrate-activities.md)并添加渠道活动后，您可以在电子邮件、短信或其他渠道编辑器中个性化消息内容。

编排营销活动中的Personalization的工作方式与其他[!DNL Journey Optimizer]营销活动或历程类似，不同之处与&#x200B;**工作表**&#x200B;相关联：通过定位和扩充画布上的活动计算出的属性，而不仅仅是来自配置文件存储的数据。

## 访问个性化编辑器 {#access}

1. 打开您的编排的营销活动并添加渠道活动。 [了解如何添加渠道活动](activities/channels.md#add)

1. 配置渠道活动，然后打开&#x200B;**[!UICONTROL 内容]**&#x200B;选项卡并编辑消息。

1. 在消息编辑器中，使用个性化编辑器将属性插入到内容中。

要预览和测试渠道活动中的个性化内容，请参阅[检查和测试您的内容](activities/channels.md#simulate-content-test-profiles)。

## 配置文件和目标属性 {#attributes}

打开个性化编辑器时，两个主文件夹包含可用于个性化的属性：

* **[!UICONTROL 轮廓属性]**

  来自[!DNL Adobe Experience Platform]的配置文件相关数据：用户配置文件中捕获的名称、电子邮件地址、位置和其他特征。

* **[!UICONTROL Target属性]**（仅限编排的营销活动）

  在活动画布上从工作表中计算的属性。 此文件夹有两个子文件夹：

   * **`<Targeting dimension>`**（例如，收件人或购买） — 与营销活动中定位的维度相关的属性。

   * **`Enrichment`** — 通过&#x200B;**[!UICONTROL 扩充]**&#x200B;活动（关系链接、收集的行、聚合）添加的数据。 在1:N **[!UICONTROL 收集数据]**&#x200B;扩充后，您将同时获得编号行和集合数组。 [了解如何使用扩充集合数据](#enrichment-collections)

有关[!DNL Journey Optimizer]中个性化编辑器的详细概述，请参阅[个性化入门](../personalization/personalize.md)。

## 使用扩充收集数据 {#enrichment-collections}

当您配置具有1:N链接和&#x200B;**[!UICONTROL 收集数据]**&#x200B;的&#x200B;**[!UICONTROL 扩充]**&#x200B;活动时，扩充属性在以下两种形式的&#x200B;**[!UICONTROL 目标属性] > [!UICONTROL 扩充]**&#x200B;下可用：

* **拼合的行** — 每个检索的行有一个字段（例如，**Purchase 1**、**Purchase 2**、**Purchase 3**），每个字段均具有您在链接上选择的属性（如价格或产品）。 当您需要单独固定插槽（例如`target.enrichment.purchase1.price`）时使用它们。

* **集合数组** — 一个数组，用于所有收集的行，该数组从链接标签命名（例如，**购买**）。 当您需要处理完整的记录集时，请使用此项 — 使用[数组函数](#array-functions)。

![](assets/enrichment-target-attributes-picker.png)

要标识集合数组中的flattend行，请在表达式编辑器中插入属性并读取生成的路径。 集合数组是路径为&#x200B;**plural** （例如`purchases`）并且具有&#x200B;**无行号** （`purchase1`、`purchase2`等）的条目。

| 您需要 | 表达式编辑器中的路径 |
| --- | --- |
| **一个已收集的行** | **编号** — 例如`target.enrichment.purchase1.price` |
| **完整的收藏集** | **Plural和unnumbered** — 例如`target.enrichment.purchases.price` |

您可以将[!DNL Journey Optimizer]中的其他位置使用的相同[数组和列表函数](../personalization/functions/arrays-list.md)应用于扩充集合，引用`target.enrichment.<label>`。

例如，在主题行中，您可能会显示存在多少已收集的购买以及第一个项目的价格：

```sql
Hello number of Items: {%= count(target.enrichment.purchases.price) %} , Name of first item: {%= head(target.enrichment.purchases.product) %}
```

➡️ [了解如何在画布上配置收藏集扩充](activities/enrichment.md#collection-personalization)
