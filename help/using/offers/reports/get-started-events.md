---
title: 决策管理事件入门
description: 了解如何在Adobe Experience Platform中创建决策管理报告。
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 57%

---

# 决策管理事件入门 {#monitor-offer-events}

每次决策管理部门对给定的用户档案做出决策时，与这些事件相关的信息都会自动发送到Adobe Experience Platform。

因此您可以导出这些数据，然后将其导入您自己的报告系统中进行分析。您还可以将 Adobe Experience Platform [查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=zh-Hans)与其他工具结合使用，以增强分析和报告。

包含决策管理事件的数据集可从Adobe Experience Platform访问 **[!UICONTROL Datasets]** 菜单。 在为每个实例进行预配时会自动创建一个数据集。

![](../assets/events-datasets-list.png)

这些数据集基于 **[!UICONTROL ODE DecisionEvents]** 架构，其中包含从决策管理向Adobe Experience Platform发送信息所需的所有XDM字段。

>[!NOTE]
>
>请注意，ODE DecisionEvents 数据集是&#x200B;**非用户档案数据集**，这意味着它们不能被引入到 Experience Platform 中以供实时客户档案使用。

**相关主题：**

* [决策管理事件关键信息](../reports/key-information.md)
* [访问事件 XDM 字段](../reports/xdm-fields.md)
