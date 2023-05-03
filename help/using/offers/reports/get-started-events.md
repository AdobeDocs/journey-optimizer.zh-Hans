---
title: 使用决策管理事件
description: 了解如何在 Adobe Experience Platform 中创建“决策管理”报告。
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: a6a892ec20dfeb6879bef2f4c2eb4a0f8f54885f
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 47%

---

# 决策管理事件入门 {#monitor-offer-events}

每次使用“决策管理”为给定用户档案做出决策时，与这些事件相关的信息都会被自动发送到 Adobe Experience Platform。

这样，您就可以洞察您的决策，例如，知道向给定用户档案展示了哪个选件。 您可以将这些数据导出以将其分析到您自己的报表系统中，或利用Adobe Experience Platform [查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=zh-Hans) 与其他工具结合使用，以增强分析和报告功能。

## 数据集中可用的关键信息 {#key-information}

做出决策时发送的每个事件都包含四个关键数据点，您可以利用这些数据点进行分析和报告：

![](../assets/events-dataset-preview.png)

* **[!UICONTROL 回退]**:如果未选择个性化选件，则备用选件的名称和ID
* **[!UICONTROL 版面]**:用于交付选件的版面的名称、ID和渠道，
* **[!UICONTROL 选择]**:为配置文件选择的选件的名称和ID，
* **[!UICONTROL 活动]**:决策的名称和ID。

此外，您还可以利用 **[!UICONTROL identityMap]** 和 **[!UICONTROL 时间戳]** 字段，以检索有关用户档案和选件交付时间的信息。

有关随每项决策发送的所有 XDM 字段的更多信息，请参阅[此小节](xdm-fields.md)。

## 访问数据集 {#access-datasets}

可从 Adobe Experience Platform **[!UICONTROL 数据集]**&#x200B;菜单访问包含“决策管理”事件的数据集。在为每个实例进行预配时会自动创建一个数据集。

![](../assets/events-datasets-list.png)

这些数据集基于 **[!UICONTROL ODE DecisionEvents]** 架构，包含从“决策管理”向 Adobe Experience Platform 发送信息所需的所有 XDM 字段。

>[!NOTE]
>
>请注意，ODE DecisionEvents 数据集是&#x200B;**非用户档案数据集**，这意味着它们不能被引入到 Experience Platform 中以供实时客户档案使用。
