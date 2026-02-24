---
solution: Journey Optimizer
product: Journey Optimizer
title: 设置消息和历程上限规则
description: 设置消息和历程上限规则
redpen-status: CREATED_||_2025-08-11_20-28-34
exl-id: 630e252a-aab2-4a27-ad46-d4dbfbc3f3a4
source-git-commit: 9e23162373564e7866af115ee2cd706527336e4a
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 38%

---

# 设置消息和历程上限规则{#section-overview}

上限规则是[冲突管理和优先处理](../using/conflict-prioritization/gs-conflict-prioritization.md)的一部分 — 它们有助于确保客户获得适当的通信量而不会感到不知所措。 在应用规则之前，请使用[冲突检测工具](../using/conflict-prioritization/conflicts.md)来识别重叠的历程和营销活动。 当多个通信符合同一个用户档案的资格时，[优先级分数](../using/conflict-prioritization/priority-scores.md)将确定最先传递的消息。

您可以设置发送消息的频率（频率上限）、用户档案可以进入的历程数（历程上限）以及消息被阻止的时间（免打扰时间）的限制。 规则将分组到&#x200B;**规则集**&#x200B;中，并应用于营销活动或历程。 有关来自外部系统的程序化控制，请参阅[上限API](../using/configuration/capping.md)。

## 设置消息和历程上限规则

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hans)

使用规则集

了解如何创建、管理和激活规则集，以控制 Adobe Journey Optimizer 中的消息频率和历程进入规则。

[探索规则集](../using/conflict-prioritization/rule-sets.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hans)

历程上限和仲裁

了解如何设置历程进入和并发上限，设置历程的优先级并监控排除项，以防止过度通信。

[了解历程上限](../using/conflict-prioritization/journey-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hans)

按渠道设置频率上限

了解如何创建并应用特定于渠道的频率上限规则，以优化消息投放并避免过度通信。

[设置频率上限](../using/conflict-prioritization/channel-capping.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg?lang=zh-Hans)

设置免打扰时间

定义基于时间的电子邮件、短信、推送和WhatsApp排除项，以便在特定时间段内不发送消息 — 尊重客户的偏好和合规性。

[设置免打扰时间](../using/conflict-prioritization/quiet-hours.md)
:::

::::

## 其他资源

- **[开始冲突管理和优先化](../using/conflict-prioritization/gs-conflict-prioritization.md)** — 冲突检测、优先级分数和规则集概述。
- **[识别潜在冲突](../using/conflict-prioritization/conflicts.md)** — 在应用上限规则之前检测重叠的历程和营销活动。
- **[分配优先级得分](../using/conflict-prioritization/priority-scores.md)** — 控制当某个用户档案符合多个通信的条件时，优先采用哪个历程或营销活动。
