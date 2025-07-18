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
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 28%

---

# 时区管理 {#timezone_management}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="时区"
>abstract="选择历程的时区。当使用固定时区时，对于所有进入历程的个人来说都是相同的。"


您可以在历程的[属性](../building-journeys/journey-properties.md#timezone)中定义时区。

要访问历程属性，请选择屏幕右上角的铅笔图标。

此时区将用于包含时间元素的历程的每个活动，例如：

* [时间条件](../building-journeys/condition-activity.md#time_condition)
* [日期条件](../building-journeys/condition-activity.md#date_condition)
* [自定义等待](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

您可以选择[固定时区](#fixed-timezone)或选择使用用户配置文件[&#128279;](#timezone-from-profiles)中定义的时区。

## 定义固定时区 {#fixed-timezone}

时区可以固定。 清除预定义的时区并从下拉列表中选择一个时区。 如果您使用固定时区，则所有进入旅程的个人都将使用相同的时区。

为此，请在&#x200B;**[!UICONTROL 历程属性]**&#x200B;窗格中选择时区。

![](assets/journey72.png)

## 使用轮廓时区 {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="使用轮廓时区"
>abstract="选中该框可在等待和条件活动中使用实时轮廓时区。如果已为轮廓定义了时区，则该历程将会检索并使用该时区。否则，时区将会是上面时区字段中定义的时区。"

如果历程的进入事件具有命名空间，这意味着历程可以访问Adobe Experience Platform的实时客户个人资料服务，则您可能希望使用在个人资料级别定义的时区。 为此，请在&#x200B;**属性**&#x200B;中选中&#x200B;**在等待和条件中使用配置文件时区**。 默认情况下不选中此选项。

如果已为轮廓定义了时区，则该历程将会检索并使用该时区。如果未指定，则使用的时区将是时区字段中定义的时区。

![](assets/journey73.png)

>[!NOTE]
>
>配置文件时区与&#x200B;**首选项详细信息**&#x200B;字段组中现有的&#x200B;**时区**&#x200B;字段一起使用。

## 在表达式中使用时区 {#timezone-in-expressions}

历程的开始和结束日期无法链接到特定时区。 它们会自动关联到实例的时区。
