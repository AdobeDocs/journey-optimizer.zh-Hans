---
title: 决策管理事件关键信息
description: 进一步了解每个决策管理事件发送的关键信息。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 07be59e8-e994-4854-8089-25614d005dbe
source-git-commit: 2d859a5dab19a419d424acefd17d254473c00818
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 85%

---

# 决策管理事件关键信息 {#events-key-information}

做出决策时发送的每个事件都包含四项关键数据点，您可以利用这些数据点进行分析和报告。

![](../../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**：后备优惠的名称和 ID（如果未选择个性化优惠），
* **[!UICONTROL Placement]**：用于投放优惠的投放位置的名称、ID 和渠道，
* **[!UICONTROL Selections]**：为用户档案选择的优惠的名称和 ID，
* **[!UICONTROL Activity]**:决策的名称和ID。

此外，您还可以利用 **[!UICONTROL identityMap]** 和 **[!UICONTROL Timestamp]** 字段检索有关用户档案的信息和投放优惠的时间。

有关随每项决策发送的所有 XDM 字段的更多信息，请参阅[此小节](xdm-fields.md)。
