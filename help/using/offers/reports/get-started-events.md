---
title: 决策管理事件入门
description: 了解如何在Adobe Experience Platform中创建决策管理报表。
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# 决策管理事件入门 {#monitor-offer-events}

每次决策管理针对给定的用户档案做出决策时，与这些事件相关的信息都会自动发送到Adobe Experience Platform。

这允许您将这些数据导出以将其分析到您自己的报表系统中。 您还可以利用Adobe Experience Platform [查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/home.html) 与其他工具结合使用，以增强分析和报告功能。

包含决策管理事件的数据集可从Adobe Experience Platform访问 **[!UICONTROL Datasets]** 菜单。 在为每个实例进行配置时，会自动创建一个数据集。

![](../assets/events-datasets-list.png)

这些数据集基于 **[!UICONTROL ODE DecisionEvents]** 架构，其中包含从决策管理向Adobe Experience Platform发送信息所需的所有XDM字段。

>[!NOTE]
>
>请注意，ODE DecisionEvents数据集是 **非配置文件数据集**，这意味着无法将它们摄取到Experience Platform中以供实时客户资料使用。

**相关主题：**

* [决策管理事件关键信息](../reports/key-information.md)
* [访问事件XDM字段](../reports/xdm-fields.md)
