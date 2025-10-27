---
solution: Journey Optimizer
product: Journey Optimizer
title: Adobe Journey Optimizer中的AI功能
description: Adobe Journey Optimizer中的AI功能
hide: true
hidefromtoc: true
source-git-commit: 2b377fea2f54c15d04fd0fc16633951c58598580
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 4%

---

# Adobe Journey Optimizer中的AI功能{#section-overview}

Adobe Journey Optimizer利用人工智能和机器学习的强大功能，转变您创建、优化和交付客户体验的方式。 从跨渠道生成个性化内容到预测吸引客户的最佳时间，AI功能可简化您的工作流并最大化影响。 本节探讨了AI支持的功能如何协同工作，帮助您做出更明智的决策、自动化复杂的任务并创建真正引起受众共鸣的体验。 无论您是利用创作AI进行内容创建、使用预测模型进行决策，还是优化发送时间以实现更好的参与，您都可以发现实用的工具和策略以充分发挥AI在客户历程编排中的潜力。

## AI支持的功能

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hans)

用于内容生成的 AI 助手

利用创新型人工智能在电子邮件、短信、推送通知、网页和登陆页面中创建和个性化内容。

[浏览AI助手](ai-assistant-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hans)

发送时间优化

使用人工智能根据历史行为预测发送消息的最佳时间并最大化客户参与。

[了解发送时间优化](../using/building-journeys/send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hans)

适用于Decisioning的AI模型

创建自动优化和个性化优化模型，以便为客户提供排名和最佳优惠。

[发现AI模型](ai-models-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg?lang=zh-Hans)

AI助理产品知识

使用对话式人工智能获得关于Adobe Journey Optimizer的即时答案和运营见解。

[使用 AI 助手](../using/start/ai-assistant.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hans)

使用AI进行内容试验

生成多个内容变体并运行实验以识别对受众表现最佳的内容。

[了解AI试验](../using/content-management/generative-experimentation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg?lang=zh-Hans)

客户人工智能集成

与Adobe智能服务集成以预测客户行为并在您的旅程中使用流失和转化分数。

[探索智能服务](../using/building-journeys/ai-services-overview.md)
:::

::::


## 其他资源

- **[品牌协调度评分](../using/content-management/brands-score.md)** — 使用AI支持的评分评估AI生成的内容与品牌准则的协调程度。
- **[实验加速器](../using/content-management/experiment-accelerator-gs.md)** — 通过AI驱动的见解和推荐加快内容实验过程。
- **[AI支持的API](../using/configuration/ajo-apis.md)** — 通过API以编程方式访问Journey Optimizer的AI和机器学习功能。

## 常见问题

+++**使用AI功能需要哪些权限？**

要使用AI助手生成内容，必须向用户授予&#x200B;**生成内容**&#x200B;权限。 此权限通过权限产品中的AI助手资源分配。 要使用AI Assistant获取产品知识和操作见解，用户必须同意Adobe Experience Cloud创作AI用户准则。

[了解有关权限的更多信息](../using/administration/ootb-permissions.md)

+++

+++**哪些渠道支持AI助手内容生成？**

用于内容生成的AI助手可用于&#x200B;**电子邮件**、**推送**、**短信**&#x200B;和&#x200B;**Web**&#x200B;渠道。 它当前不适用于直邮、内容卡、LINE或WhatsApp渠道。

+++

+++**使用AI助手的最佳实践是什么？**

- **使用明确定义的提示** — 生成的内容的质量受营销目标和提示的严重影响。 要明确具体。
- **上传品牌资产** — 提供PDF、JPEG、PNG或ZIP格式（最大50MB）的品牌资产，以便获得准确的品牌内内容。
- **使用自定义模板** — 利用最多8到10个图像的特定于品牌的电子邮件模板以获得最佳结果。
- **提供反馈** — 使用拇指向上、拇指向下或标记图标报告有问题的输出以帮助优化模型。
- **每代仅使用一个品牌资产** — 虽然您可以上传多个资产，但每个特定代仅使用一个品牌资产。

[了解有关AI Assistant护栏的更多信息](../using/content-management/gs-generative.md#generative-guardrails)

+++

+++**优化发送时间的最佳实践是什么？**

- **等待30天** — 在启用发送时间优化之前使用电子邮件和推送操作至少30天，以确保充分的数据收集。
- **选择最佳等待时间** — 为获得最佳结果，将最大等待时间设置为6-24小时。 较短的持续时间会限制优化潜力；较长的持续时间可能会导致消息过期。
- **针对正确的量度进行优化** — 对于电子邮件，针对驱动操作时的点击次数或针对信息内容打开次数进行优化。 推送消息始终针对打开次数进行优化。
- **避免发送对时间敏感的邮件** — 请勿将发送时间优化用于紧急操作邮件，如订单确认、密码重置或航班通知。 最适合营销通信，如促销活动和新闻稿。
- **计划早上发送推送消息** — 为避免夜间通知，请计划早上持续时间较短的批量推送发送消息（例如，上午9点发送，等待时间为8小时）。

[了解有关发送时间优化的更多信息](../using/building-journeys/send-time-optimization.md)

+++

+++**发送时间优化的限制是什么？**

- **渠道** — 仅适用于历程中的电子邮件和推送通知渠道。 在营销活动中或自定义操作中不可用。
- **可用性** — 必须由Adobe客户关怀团队或您的Adobe代表启用。
- **培训期** — 在使用前需要至少30天的历史电子邮件或推送数据。
- **模型训练** — 模型最初每周使用过去16周的数据进行训练，然后每月重新训练。
- **探索与优化** - 5%的消息接收随机探索发送时间；95%的消息接收优化的发送时间。

+++

+++**在Decisioning中，AI模型有哪些限制？**

- **最大AI模型** — 每个组织最多5个AI排名模型。
- **数据集要求** — 对于自动优化模型，在过去14天内至少2个选件必须具有100个以上的显示事件和5个以上的点击事件。
- **反馈事件** — 必须作为体验事件发送；不能在Journey Optimizer渠道中自动收集。
- **API限制** — 自动优化模型不适用于批量决策API（仅限决策管理）。

[了解有关 AI 模型的更多信息](../using/experience-decisioning/ranking/ai-models.md)

+++

+++**哪些护栏适用于AI支持的决策？**

| 组件 | 限制 |
|-----------|-------|
| AI排名模型 | 每个组织5个 |
| 决策请求(使用Edge分段基于代码) | 每秒 1,500 |
| 决策请求(基于代码，不使用Edge分段) | 每秒 5,000 |
| 项目集合 | 共计10,000 |
| 每个收藏集的优惠项目 | 500 |
| 每个决策策略的选择策略 | 10 |
| 每个决策策略返回的优惠项目 | 30 |
| 资格规则+排名公式 | 10,000个合并项 |
| 每个规则的配置文件属性 | 25 |
| 每个规则的上下文数据属性 | 30 |

[详细了解Decisioning护栏](../using/experience-decisioning/decisioning-guardrails.md)

+++

+++**要使用AI功能，是否需要同意任何条款？**

是，在Journey Optimizer中使用AI助手之前，您必须同意[Adobe Experience Cloud Generative AI用户准则](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)。 有关更多信息，请与Adobe代表联系。 此外，Adobe还将Content Credentials应用于Firefly生成的资源，作为其致力于在生成性人工智能使用方面实现透明度的工作的一部分。

+++

+++**AI生成的内容是否始终准确？**

不会。创作AI内容可能并不总是准确的。 始终检查AI生成的输出的准确性，并确保它们适合您的用例。 使用提供的评级工具分享反馈，以帮助工程师优化模型。

+++

