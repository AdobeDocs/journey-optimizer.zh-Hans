---
solution: Journey Optimizer
product: journey optimizer
title: 时区管理
description: 了解时区管理
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: 时区，属性，历程，条件，时间，日期，自定义
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: fec6b15db9f8e6b2a07b55bc9e8fc4d9cb0d73d7
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 2%

---

# 时区管理 {#timezone_management}

您可以在中定义时区 [属性](../building-journeys/journey-properties.md#timezone) 你旅程的一部分。

要访问历程属性，请单击屏幕右上角的铅笔图标。

此时区将用于包含时间元素的历程的每个活动，例如：

* [时间条件](../building-journeys/condition-activity.md#time_condition)
* [日期条件](../building-journeys/condition-activity.md#date_condition)
* [自定义等待](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

您可以选择 [固定时区](#fixed-timezone) 或选择使用时区 [在用户配置文件中定义](#timezone-from-profiles).

## 定义固定时区 {#fixed-timezone}

时区也可以固定。 清除预定义的时区并从下拉列表中选择一个时区。 如果您使用固定时区，则所有进入旅程的个人都将使用相同的时区。

为此，请在 **[!UICONTROL 历程属性]** 窗格，选择时区。

![](assets/journey72.png)

## 使用配置文件定义历程时区 {#timezone-from-profiles}

如果历程的进入事件具有命名空间，这意味着历程可以访问Adobe Experience Platform的实时客户个人资料服务，则您可能希望使用在个人资料级别定义的时区。 为此，请在中 **属性**，检查 **在等待和条件中使用配置文件时区**. 默认情况下不选中此选项。

如果为用户档案定义了时区，则历程将检索并使用它。 如果未指定，则使用的时区将是时区字段中定义的时区。

![](assets/journey73.png)

>[!NOTE]
>
>配置文件时区与 **时区** 字段存在于 **偏好设置详细信息** 字段组。

## 在表达式中使用时区 {#timezone-in-expressions}

历程的开始和结束日期无法链接到特定时区。 它们会自动关联到实例的时区。
