---
title: 决策管理事件关键信息
description: 进一步了解每个决策管理事件发送的关键信息。
feature: 优惠
topic: 集成
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 91%

---

# 决策管理事件关键信息 {#events-key-information}

做出决策时发送的每个事件都包含四项关键数据点，您可以利用这些数据点进行分析和报告。

![](../../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**：后备优惠的名称和 ID（如果未选择个性化优惠），
* **[!UICONTROL Placement]**：用于投放优惠的投放位置的名称、ID 和渠道，
* **[!UICONTROL Selections]**：为用户档案选择的优惠的名称和 ID，
* **[!UICONTROL Activity]**：决策（以前称为优惠活动）的名称和 ID。

此外，您还可以利用 **[!UICONTROL identityMap]** 和 **[!UICONTROL Timestamp]** 字段检索有关用户档案的信息和投放优惠的时间。

有关随每项决策发送的所有 XDM 字段的更多信息，请参阅[此小节](xdm-fields.md)。
