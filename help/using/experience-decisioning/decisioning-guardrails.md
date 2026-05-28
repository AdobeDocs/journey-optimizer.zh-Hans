---
title: 决策护栏和限制
description: 详细了解Decisioning护栏和限制。
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/oTljriepwffzR-LIAc2kWjTQx9Oj0QMgJpbghkSEsmY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: e42070c4cc1dde06786c4075b1e6e45e8c323c12
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 16%

---

# 决策护栏和限制 {#decisioning-guardrails}

要确保优化使用决策，请牢记以下护栏和限制。

[此部分](../start/guardrails.md)中提供了[!DNL Journey Optimizer]护栏和限制的完整列表。

## 决策请求 {#decision-requests}

| 护栏 | 限制 |
| ------- | ------- |
| 使用Edge分段功能的基于代码的体验API请求，其中包含决策策略 | 1500 |
| 具有不使用Edge分段的决策策略的基于代码的体验API请求 | 5000 |
| 每个Edge决策请求的最大表面URI数 | 30 |

## 决策项 {#decision-items}

| 护栏 | 限制 |
| ------- | ------- |
| 决策项目总数 | 10K |
| 包含属性的项目的最大大小(1KB)，最多30个属性 | 1KB |
| 频率规则 — 每个决策项的最大上限规则数 | 10 |
| 每个决策项目的AEM内容片段的最大数量 | 5 |

## 物料集合 {#item-collections}

| 护栏 | 限制 |
| ------- | ------- |
| 项目集合 | 10K |
| 每个收藏集的决策项目总数 | 500 |

## 决策策略 {#decision-policy}

| 护栏 | 限制 |
| ------- | ------- |
| 每个决策策略的选择策略和手动项目数 | 10 |
| 每个决策策略返回的最大决策项目数 | 30 |
| 每封电子邮件的最大决策策略数 | 10 |

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

## 其他 {#others}

| 护栏 | 限制 |
| ------- | ------- |
| 每个项目目录架构的自定义属性数 | 100 |
| 投放位置总数 | 1K |
| AI排名模型 | 5 |

## 配置 {#configurations}

Decisioning支持的配置总数不能超过20,000。

总配置计数是沙盒中存在的[上限规则](items.md#capping)的总数。
