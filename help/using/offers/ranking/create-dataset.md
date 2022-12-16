---
product: experience platform
solution: Experience Platform
title: 创建数据集以收集事件
description: 了解如何创建数据集以收集事件
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 16%

---

# 创建数据集以收集事件 {#create-dataset}

在创建AI模型之前，您需要创建一个数据集，以收集转化事件。 首先，创建将在数据集中使用的架构：

1. 从 **[!UICONTROL 数据管理]** 菜单，选择 **[!UICONTROL 架构]**，转到 **[!UICONTROL 浏览]** 选项卡，单击 **[!UICONTROL 创建架构]**.

   ![](../assets/ai-ranking-create-schema.png)

1. 选择 **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >在 [XDM 系统概述文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh_Hans){target=&quot;_blank&quot;}中了解关于 XDM 架构和字段组的更多信息。

1. 从 **[!UICONTROL 字段组]** 部分，选择 **[!UICONTROL 添加]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. 在 **[!UICONTROL 搜索]** 字段中，键入“建议交互”并选择 **[!UICONTROL 体验事件 — 建议交互]** 字段组。

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >将在数据集中使用的架构必须具有 **[!UICONTROL 体验事件 — 建议交互]** 与其关联的字段组。 否则，您将无法在排名策略中使用它。

1. 单击 **[!UICONTROL 添加字段组]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >字段组以前称为mixin。

1. 键入名称并保存架构。

>[!NOTE]
>
>了解有关在 [架构组合的基础知识](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target=&quot;_blank&quot;}。

现在，您可以使用此架构创建数据集。 为此，请执行以下步骤：

1. 从 **[!UICONTROL 数据管理]** 菜单，选择 **[!UICONTROL 数据集]**，转到 **[!UICONTROL 浏览]** 选项卡，单击 **[!UICONTROL 创建数据集]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. 选择 **[!UICONTROL 从架构创建数据集]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. 从列表中选择之前创建的架构。

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. 单击&#x200B;**[!UICONTROL 下一步]**。

1. 为 **[!UICONTROL 名称]** 字段，单击 **[!UICONTROL 完成]**.

   ![](../assets/ai-ranking-dataset-name.png)

现在，可以选择数据集以在 [创建排名策略](#create-ranking-strategy).
