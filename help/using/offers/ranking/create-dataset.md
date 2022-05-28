---
product: experience platform
solution: Experience Platform
title: 创建数据集以收集事件
description: 了解如何创建数据集以收集事件
feature: Ranking Formulas
role: User
level: Intermediate
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 7%

---

# 创建数据集以收集事件 {#create-dataset}

在创建AI模型之前，您需要创建一个数据集，以收集转化事件。 首先，创建将在数据集中使用的架构：

1. 从 **[!UICONTROL Data Management]** 菜单，选择 **[!UICONTROL Schema]**，转到 **[!UICONTROL Browse]** 选项卡，单击 **[!UICONTROL Create schema]**.

   ![](../assets/ai-ranking-create-schema.png)

1. 选择 **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    在 [XDM系统概述文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans).


1. 在 **[!UICONTROL Search]** 字段中，键入“建议交互”并选择 **[!UICONTROL Experience Event - Proposition Interactions]** 字段组。

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    将在数据集中使用的架构必须具有 **[!UICONTROL Experience Event - Proposition Interactions]** 与其关联的字段组。 否则，您将无法在排名策略中使用它。

1. 单击 **[!UICONTROL Add field groups]**。

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >字段组以前称为mixin。

1. 键入名称并保存架构。<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    了解有关在 [架构组合的基础知识](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas).

现在，您可以使用此架构创建数据集。 为此，请执行以下步骤：

1. 从 **[!UICONTROL Data Management]** 菜单，选择 **[!UICONTROL Datasets]**，转到 **[!UICONTROL Browse]** 选项卡，单击 **[!UICONTROL Create dataset]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. 选择 **[!UICONTROL Create dataset from schema]**。

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 从列表中选择之前创建的架构。

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. 单击 **[!UICONTROL Next]**。

1. 为 **[!UICONTROL Name]** 字段，单击 **[!UICONTROL Finish]**.

   ![](../assets/ai-ranking-dataset-name.png)

现在，可以选择数据集以在 [创建排名策略](#create-ranking-strategy).
