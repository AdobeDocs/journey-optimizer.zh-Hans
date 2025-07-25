---
title: 决策护栏和限制
description: 详细了解Decisioning护栏和限制。
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: 58f4fdf8ec3cdb609efebf5b8713f6b770ef5414
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 18%

---

# 决策护栏和限制 {#decisioning-guardrails}

要确保优化使用决策，请牢记以下护栏和限制。

[此部分](../start/guardrails.md)中提供了[!DNL Journey Optimizer]护栏和限制的完整列表。

## 决策请求 {#decision-requests}

| 护栏 | 限制 |
| ------- | ------- |
| 使用Edge分段功能的基于代码的体验API请求，其中包含决策策略 | 1500 |
| 具有不使用Edge分段的决策策略的基于代码的体验API请求 | 5000 |

## 物料集合 {#item-collections}

| 护栏 | 限制 |
| ------- | ------- |
| 项目集合 | 10K |
| 每个项目收藏集的优惠项目总数 | 500 |

## 决策策略 {#decision-policy}

| 护栏 | 限制 |
| ------- | ------- |
| 每个决策策略的选择策略和手动项目数 | 10 |
| 每个决策策略返回的最大优惠项目 | 30 |

## 资格规则 {#eligibility-rules}

| 护栏 | 限制 |
| ------- | ------- |
| 决策规则和排名公式总数 | 10K总和 |
| 每条规则的配置文件属性最大数量 | 25 |
| 每个规则的上下文数据属性的最大数量 | 30 |
| pql规则的最大大小 | 15K (UTF-8) |
| 最大嵌套级别数 | 30 |

## 排名公式 {#ranking-formulas}

| 护栏 | 限制 |
| ------- | ------- |
| 排名公式PQL的最大大小 | 8K (UTF-8) |
| 配置文件属性的最大数量 | 25 |
| 上下文数据属性的最大数量 | 30 |
| 最大嵌套级别数 | 30 |

## 其他  {#others}

| 护栏 | 限制 |
| ------- | ------- |
| 每个优惠目录架构的自定义属性数 | 100 |
| 选件项目总数 | 10K |
| 投放位置总数 | 1K |
| AI排名模型 | 5 |
| 频率规则 — 每个选件的上限规则的最大数量 | 10 |
