---
solution: Journey Optimizer
product: journey optimizer
title: 吞吐量的性能附加功能 — （推送）单一 — 消息投放
description: 了解如何在Adobe Journey Optimizer中配置和使用性能加载项实现吞吐量 — （推送）单一 — 消息投放。
feature: Push
topic: Content Management
role: User
level: Intermediate
exl-id: 2d0677ad-41c8-4299-a7c8-0e4f8a1716f7
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 3%

---


# 吞吐量的性能附加功能 — （推送）单一 — 消息投放 {#performance-add-on-for-throughput-push-unitary-mes}

>[!AVAILABILITY]
>
>此功能可从&#x200B;**AJO26.7** (2026-07-27)获得。

## 概述 {#overview}

Adobe Journey Optimizer引入了&#x200B;**吞吐量性能附加功能 — （推送）单一 — 消息交付**，使组织能够跨推送渠道提供更相关、更个性化的客户体验。

本页介绍如何在营销活动和历程中配置和使用此功能。

## 先决条件 {#prerequisites}

开始之前：

* 您有权访问Adobe Journey Optimizer，并拥有所需的&#x200B;**推送**&#x200B;权限。
* 已配置推送渠道表面。 请参阅[配置推送渠道](../configuration/channel-surfaces.md)。

## 工作原理 {#how-it-works}

吞吐量的性能插件 — （推送）单一 — 消息投放直接与AJO执行引擎集成。 当用户档案到达历程或营销活动中的推送操作时，该功能会在发送时应用配置的参数。

主要功能：

* **配置文件级个性化** — 使用配置文件和上下文属性根据收件人调整设置。
* **历程和营销活动支持** — 在编排的历程和一次性营销活动中都有效。
* **实时量度** — 结果显示在[推送报告](../reports/push-report.md)中。

## 配置用于吞吐量的性能加载项 {#configure}

1. 在AJO左侧菜单中，导航到&#x200B;**渠道** > **推送配置**。
1. 选择或创建渠道配置。
1. 在&#x200B;**的**&#x200B;性能加载项部分中，启用该功能。
1. 设置所需的参数。
1. 单击&#x200B;**保存**。

>[!NOTE]
>
>配置更改适用于新历程执行。 正在进行的历程不受影响。

## 相关主题 {#related-topics}

* [推送入门](get-started-push.md)
* [创建推送通知](create-push.md)
* [AJO26.7发行说明](../rn/release-notes.md)
