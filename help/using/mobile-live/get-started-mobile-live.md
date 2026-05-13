---
solution: Journey Optimizer
product: journey optimizer
title: 实时活动快速入门
description: 了解如何在 Journey Optimizer 中发送实时活动
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
TQID: https://experienceleague.adobe.com/IB00r0QSfCthvgvyqubGwsaUoiJKBL-E96duLn4R5i0
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 421
ht-degree: 100%

---

# 实时活动快速入门 {#get-started-mobile-live}


实时活动是在设备锁屏上持久显示、一目了然的 UI 元素。 它们使您的应用程序能够提供实时、最新的信息，让用户在事件的进行过程中随时了解情况，而无需打开应用程序或接收重复的推送通知。

>[!AVAILABILITY]
>
>Adobe Journey Optimizer 中的实时活动仅与 Apple iOS 兼容。

与传统推送通知不同，实时活动体现的是&#x200B;**基于状态的参与**：它不是发送一次性的提醒，而是保持持续的、上下文相关的存在，并随着事件的发展动态更新。


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="锁屏界面和灵动岛上的 iOS 实时活动" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>主要优点</strong></p>
<p>实时活动使移动端的用户参与从基于通知的模式转向基于状态的模式，从而使品牌能够：</p>
<ul>
<li>在高价值事件期间，维持锁屏界面上的<strong>持续呈现</strong></li>
<li><strong>动态更新信息</strong>，避免因重复通知给用户带来困扰</li>
<li>提供与现实事件相关联的<strong>更丰富、更符合上下文的</strong>移动端体验</li>
<li>在进行中的事务或实时体验过程中，<strong>提高参与度和留存率</strong></li>
</ul>
</td>
</tr>
</table>

借助 Adobe Journey Optimizer，您可以通过 API 触发的营销活动以编程方式远程&#x200B;**启动**、**更新**&#x200B;和&#x200B;**结束**&#x200B;实时活动，大规模地同时支持个体级和基于受众的用例。

实时活动&#x200B;**只能**&#x200B;通过 **API 触发的**营销活动启动，让您可以提供自定义负载并通过自己的负载执行所有个性化设置。
必须根据预期的实时活动用例选择适当的 **API 触发的**&#x200B;营销活动类型：

* 对于广播类用例（即大规模发送基于受众的更新），请选择 **API 触发的营销**：

   * 体育比分和实时活动倒计时
   * 面向某条航线上所有乘客的航班状态更新
   * 跨用户区段的共同体验

* 对于个体用例，请选择 **API 触发的事务性** – 每个用户 1:1 次实时更新：

   * 订单跟踪和投放进度
   * 行程或服务状态更新
   * 实时预订和预约确认

## 快速入门指南

请完成以下步骤，在应用程序中配置和实施实时活动：

1. **[配置 Adobe Journey Optimizer](mobile-live-configuration.md)**

   通过创建移动配置来设置环境。

1. **[集成 Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   与 Adobe Experience Platform Mobile SDK 集成，可在锁屏界面和灵动岛上实现实时动态更新。

1. **[在 Journey Optimizer 中创建实时活动](create-mobile-live.md)**

   在 Journey Optimizer 中使用 API 触发的营销活动来启动实时活动。

1. **[跟踪营销活动](../reports/campaign-global-report-cja-activity.md)**

   使用内置报告，开始衡量实时活动的影响。

## 操作说明视频

了解如何使用 Adobe Journey Optimizer 配置 iOS 实时活动，以便在 iPhone 锁屏界面和灵动岛上提供丰富的实时更新。

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
