---
title: 时区管理
description: 了解时区管理
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 2%

---

# 时区管理 {#timezone_management}

您可以在 [属性](../building-journeys/journey-gs.md#change-properties) 你的旅程。

要访问“属性”，请单击屏幕右上方的铅笔图标。

此时区将用于历程中包含时间元素的每个活动，例如：

* [时间条件](../building-journeys/condition-activity.md#time_condition)
* [日期条件](../building-journeys/condition-activity.md#date_condition)
* [自定义等待](../building-journeys/wait-activity.md#custom)
* [修复了日期等待](../building-journeys/wait-activity.md#fixed_date)

您可以选择时区，也可以选择使用用户配置文件中定义的时区。

>[!NOTE]
>
>配置文件时区适用于 **timeZone** 字段 **首选项详细信息** 字段组。

## 定义固定时区 {#fixed-timezone}

时区也可以固定。 清除预定义的时区，然后从下拉列表中选择一个时区。 如果您使用固定时区，则进入历程的所有个人都将使用相同的时区。

为此，请在 **[!UICONTROL Journey Properties]** 窗格，选择时区。

![](../assets/journey72.png)

## 使用用户档案定义旅程时区 {#timezone-from-profiles}

如果历程的登入事件具有命名空间，即历程可以访问Adobe Experience Platform的实时客户资料服务，则会使用在历程中流动的个人资料中指定的时区预定义时区。

如果在Adobe Experience Platform配置文件中定义了时区，则可以在历程中进行检索。

如果个人的用户档案不包含时区，则检索到的时区将是时区字段中定义的时区。

为此，请在 **[!UICONTROL Properties]**，勾选 **[!UICONTROL Use Profile timezone in waits and conditions]**.

![](../assets/journey73.png)

## 在表达式中使用时区 {#timezone-in-expressions}

历程的开始日期和结束日期不能链接到特定时区。 它们会自动关联到实例的时区。
