---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 决策管理护栏和限制
description: 详细了解决策管理护栏和限制。
badge: label="旧版" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: d2872bd3-42f8-4744-bb5b-41c49340098a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/teZQ3GKXJoj05ZD7bCCzKSzwLdUbgF8DXp8csDostOw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 402
ht-degree: 12%

---

# 决策管理护栏和限制 {#decision-management-guardrails}

>[!IMPORTANT]
>
>本页介绍旧版&#x200B;**决策管理**&#x200B;功能的护栏。 如果您使用的是&#x200B;**决策** — [!DNL Adobe Journey Optimizer]当前通过基于代码的体验和电子邮件渠道提供的决策功能 — 请改为参阅[决策护栏和限制](../experience-decisioning/decisioning-guardrails.md)。
>
>不确定您使用的是哪种功能？ [了解Decisioning](../experience-decisioning/gs-experience-decisioning.md)。

本页适用于仍在使用旧版决策管理系统的用户。 为确保最佳使用，请牢记以下护栏和限制。

[此部分](../start/guardrails.md)中提供了[!DNL Journey Optimizer]护栏和限制的完整列表。

## 决策请求

投放吞吐量对应于决策管理应用程序服务在指定时间段内可以投放的决策响应数。

| 护栏 | 限制 |
| ------- | ------- |
| 每秒决策API请求数 | 每个组织500个 |
| 使用Edge分段技术的每秒Edge Decisioning API请求数 | 每个组织1,500个 |
| Edge Decisioning API请求数/秒，不使用Edge分段 | 每个组织5,000 |
| 每个响应返回的优惠 | 每个决策范围最多30个，或总共100个 |
| 每个请求涉及的选件规则的最大数量 | 100 |

## 决策

| 护栏 | 限制 |
| ------- | ------- |
| 决策总数 | 10K |
| 实时决策 | 1K |
| 每个决策的投放位置 | 30 |

## 集合

| 护栏 | 限制 |
| ------- | ------- |
| 每个收藏集的优惠 | 500 |
| 集合 | 10K |
| 每个决策的收藏集 | 30 |

## 集合限定符

| 护栏 | 限制 |
| ------- | ------- |
| 每个选件或收藏集的收藏集限定符 | 20 |
| 集合限定符总数 | 1,000 |

## 产品建议

| 护栏 | 限制 |
| ------- | ------- |
| 优惠总数 | 10K |
| 每个沙盒的&#x200B;**活动**&#x200B;选件的最大数量 | 10K |
| 包括属性在内的选件的最大大小(1KB)，最多30个属性 | 1KB |
| 最大优惠呈现大小（所有版面的总计） | 1KB |

## 资格规则

| 护栏 | 限制 |
| ------- | ------- |
| 决策规则和排名公式总数 | 10K总和 |
| 每条规则的配置文件属性最大数量 | 25 |
| 每个规则的上下文数据属性的最大数量 | 30 |
| PQL规则的最大大小 | 15K (UTF-8) |
| 最大嵌套级别数 | 30 |

## 排名公式

| 护栏 | 限制 |
| ------- | ------- |
| 排名公式PQL的最大大小 | 8K (UTF-8) |
| 配置文件属性的最大数量 | 25 |
| 上下文数据属性的最大数量 | 30 |
| 最大嵌套级别数 | 30 |

## 其他

| 护栏 | 限制 |
| ------- | ------- |
| 投放位置 | 1000 |
| AI排名模型 | 5 |
| 频率上限 — 每个选件的上限规则的最大数量 | 10 |

## 配置 {#configurations}

决策管理支持的配置总数不能超过20,000。

总配置计数是沙盒中存在的[上限规则](offer-library/add-constraints.md#capping)的总数。 对于应用于所有[投放位置](offer-library/creating-placements.md)的每个上限规则，必须将规则乘以与指定选件关联的所有投放位置。
