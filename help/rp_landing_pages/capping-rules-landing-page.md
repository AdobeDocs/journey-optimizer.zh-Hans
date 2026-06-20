---
solution: Journey Optimizer
product: Journey Optimizer
title: 设置消息和历程上限规则
description: 设置消息和历程上限规则
redpen-status: CREATED_||_2025-08-11_20-28-34
exl-id: 630e252a-aab2-4a27-ad46-d4dbfbc3f3a4
source-git-commit: 0a2c384faea70dcbc9b99596740e375d85b2bc64
workflow-type: ht
source-wordcount: '292'
ht-degree: 100%

---

# 设置消息和历程上限规则{#section-overview}

上限规则属于[冲突管理与优先级排序](../using/conflict-prioritization/gs-conflict-prioritization.md)的组成部分，有助于确保客户收到适当数量的通信内容，而不会感到应接不暇。在应用规则之前，请使用[冲突检测工具](../using/conflict-prioritization/conflicts.md)来识别重叠的历程和营销活动。当多个沟通内容同时符合同一轮廓的条件时，[优先级分数](../using/conflict-prioritization/priority-scores.md)将决定哪条消息优先发送。

您可以限制消息发送的频率（频率上限）、一个轮廓可以进入多少个历程（历程上限）以及何时屏蔽消息（静默时段）。规则被分组到&#x200B;**规则集** 中，并应用于营销活动或历程。如需通过外部系统进行编程控制，请参阅[上限 API](../using/configuration/capping.md)。

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

为电子邮件、短信、推送和 WhatsApp 定义基于时间的排除规则，确保在特定时间段内不发送任何消息——从而尊重客户偏好并确保合规性。

[设置免打扰时间](../using/conflict-prioritization/quiet-hours.md)
:::

::::

## 其他资源

- **[冲突管理与优先级排序入门](../using/conflict-prioritization/gs-conflict-prioritization.md)** – 冲突检测、优先级分数和规则集概览。
- **[识别潜在冲突](../using/conflict-prioritization/conflicts.md)** - 在应用上限规则之前检测重叠的历程和营销活动。
- **[分配优先级分数](../using/conflict-prioritization/priority-scores.md)** - 当一个轮廓同时符合多个沟通条件时，控制哪个历程或营销活动优先。
