---
product: experience platform
solution: Experience Platform
title: 创建数据集以收集事件
description: 了解如何创建数据集以收集事件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 10%

---

# 创建数据集以收集事件 {#create-dataset}

要收集体验事件，您首先需要创建一个将发送这些事件的数据集。

首先，创建将在数据集中使用的架构：

1. 从 **[!UICONTROL 数据管理]** 菜单，选择 **[!UICONTROL 架构]** 然后转到 **[!UICONTROL 浏览]** 选项卡。

1. 单击 **[!UICONTROL 创建架构]** 选择 **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >在 [XDM系统概述文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en){target="_blank"}.

1. 从 **[!UICONTROL 字段组]** 部分，选择 **[!UICONTROL 添加]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. 在 **[!UICONTROL 搜索]** 字段中，键入“建议交互”。

1. 选择 **[!UICONTROL 体验事件 — 建议交互]** 字段组，单击 **[!UICONTROL 添加字段组]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >将在数据集中使用的架构必须具有 **[!UICONTROL 体验事件 — 建议交互]** 与其关联的字段组。 否则，您将无法在排名策略中使用它。

1. 键入名称并保存架构。

>[!NOTE]
>
>了解有关在 [架构组合的基础知识](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target="_blank"}.

现在，您可以使用此架构创建数据集。 为此，请执行以下步骤：

1. 从 **[!UICONTROL 数据管理]** 菜单，选择 **[!UICONTROL 数据集]** 然后转到 **[!UICONTROL 浏览]** 选项卡。

1. 单击 **[!UICONTROL 创建数据集]** 选择 **[!UICONTROL 从架构创建数据集]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 从列表中选择之前创建的架构，然后单击 **[!UICONTROL 下一个]**.

1. 为 **[!UICONTROL 名称]** 字段，单击 **[!UICONTROL 完成]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>现在可以选择此数据集来在 [创建排名策略](#create-ranking-strategy).
