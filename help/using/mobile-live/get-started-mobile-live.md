---
solution: Journey Optimizer
product: journey optimizer
title: 实时活动快速入门
description: 了解如何在Journey Optimizer中发送实时活动
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: df4183e15b2907bfb669e7e2e8eb88771627dcf4
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 21%

---

# 实时活动快速入门 {#get-started-mobile-live}


实时活动是显示在设备锁定屏幕上的永久、可浏览的UI元素。 它们让您的应用程序提供实时、最新的信息，让用户在整个持续事件中都能了解最新信息，而无需他们打开应用程序或接收重复的推送通知。

>[!AVAILABILITY]
>
>Adobe Journey Optimizer中的实时活动仅与Apple iOS兼容。

与传统推送通知不同，实时活动代表&#x200B;**基于状态的参与**：实时活动不提供一次性警报，而是保持持续的、情境式的存在，并随着事件的发展动态更新。


![](assets/do-not-localize/live-activity.jpeg){width="30%" align="left"}

借助Adobe Journey Optimizer，您可以通过API触发的营销活动以编程方式远程&#x200B;**开始**、**更新**&#x200B;和&#x200B;**结束**&#x200B;实时活动 — 大规模支持个人和基于受众的用例。

实时活动只能&#x200B;**通过** API触发&#x200B;**营销活动启动**，从而允许您提供自定义有效负载并通过自己的有效负载执行所有个性化。
必须根据预期的实时活动用例选择适当的&#x200B;**API触发**&#x200B;营销活动类型：

* 为广播用例选择&#x200B;**API触发的营销** — 大规模发送的基于受众的更新：

   * 运动得分和实时活动倒计时
   * 路线上所有乘客的航班状态更新
   * 在用户区段间共享体验

* 为个别用例选择&#x200B;**API触发的事务性** — 每个用户1:1个实时更新：

   * 订单跟踪和交付进度
   * 乘坐或服务状态更新
   * 实时预订和预约确认

## 主要优点

实时活动可将移动参与从基于通知转变为基于状态，从而使品牌能够：

* 在整个高值事件中保持&#x200B;**连续存在**
* **动态更新信息**，用户不会因为重复通知而不知所措
* 提供与现实世界活动相关的&#x200B;**更丰富、更符合情境的**&#x200B;移动时刻
* 在活动交易或实时体验期间&#x200B;**提高参与度和维系率**

## 快速入门指南

完成以下步骤以在应用程序中配置和实施实时活动：

1. **[配置 Adobe Journey Optimizer](mobile-live-configuration.md)**

   通过创建移动配置来设置环境。

1. **[集成 Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   与 Adobe Experience Platform Mobile SDK 集成，可在锁屏界面和灵动岛上实现实时动态更新。

1. **[在Journey Optimizer中创建实时活动](create-mobile-live.md)**

   在Journey Optimizer中使用API触发的营销活动来启动实时活动。

1. **[跟踪营销活动](../reports/campaign-global-report-cja-activity.md)**

   开始使用内置报告衡量实时活动的影响。

## 操作方法视频

了解如何使用Adobe Journey Optimizer配置iOS Live Activities，以便在iPhone锁屏界面和Dynamic Island上提供丰富的实时更新。

>[!VIDEO](https://video.tv.adobe.com/v/3479874/?captions=chi_hans&learn=on)
