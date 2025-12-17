---
title: 开始使用Decisioning API
description: 了解如何开始使用Decisioning API以编程方式管理决策项并提供个性化优惠。
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7a4b5d4e-9c1d-4f3a-b8e9-1d5f6e7a8c3a
version: Journey Orchestration
source-git-commit: e46ab0637a0fa4a2b4b8b6ff3b8ab3eb5d38e0f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 4%

---

# Decisioning API开发人员指南 {#decisioning-api-developer-guide}

Decisioning API允许您以编程方式创建和管理用于向客户提供个性化优惠的组件。 这些RESTful API为决策项、选择策略、资格规则和其他决策组件提供完整的CRUD（创建、读取、更新、删除）操作。

## 身份验证 {#authentication}

在使用Decisioning API之前，您必须设置身份验证以访问API端点。 有关分步说明，请参阅[Journey Optimizer身份验证指南](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}。

## 可用的API操作 {#available-operations}

Decisioning API为决策组件提供全面的管理功能。 可以使用以下操作类别：

* **决策项** — 创建、读取、更新、删除和列出决策项，这些决策项表示要交付给客户的优惠或内容。

  ➡️ [了解如何管理决策项](decisions-items/create.md)

* **项目集合** — 将决策项目组织到集合中，以便使用资格规则更轻松地管理和定位。

  ➡️ [了解如何管理项目集合](items-collections/create.md)

* **选择策略** — 定义在多个项目符合交付条件时如何选择和排名决策项目。

  ➡️ [了解如何管理选择策略](selection-strategies/create.md)

* **资格规则** — 设置条件以确定哪些配置文件有资格接收特定决策项目。

  ➡️ [了解如何管理资格规则](eligibility-rules/create.md)

* **排名公式** — 创建自定义排名逻辑以确定决策项的显示顺序。

  ➡️ [了解如何管理排名公式](ranking-formulas/create.md)

* **投放位置** — 定义决策项可在体验中显示的位置或上下文。

  ➡️ [了解如何管理投放位置](exd-placements/create.md)

## 后续步骤 {#next-steps}

现在，您已了解Decisioning API的基础知识，可以继续特定操作了：

* [创建决策项](decisions-items/create.md)
* [列出决策项目](decisions-items/decision-items-list.md)
* [创建选择策略](selection-strategies/create.md)
* [创建资格规则](eligibility-rules/create.md)

有关在营销活动和历程中使用决策的更多信息，请参阅[决策文档](../gs-experience-decisioning.md)。
