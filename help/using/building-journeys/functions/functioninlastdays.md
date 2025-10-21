---
product: journey optimizer
title: inLastDays
description: 了解函数inLastDays
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastDays，函数，表达式，历程
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 19%

---

# inLastDays {#inLastDays}

如果给定的dateTime介于现在和现在之间 — 增量天，则返回true。

## 类别

日期

## 函数语法

`inLastDays(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

## 签名和返回的类型

`inLastDays(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。
