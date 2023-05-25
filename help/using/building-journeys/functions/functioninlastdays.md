---
product: journey optimizer
title: inLastDays
description: 了解inLastDays函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays，函数，表达式，历程
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastDays {#inLastDays}

如果给定的日期或日期时间介于现在和现在之间 — 增量天，则返回true。

## 类别

日期

## 函数语法

`inLastDays(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| delta | 整数 |

## 签名和返回类型

`inLastDays(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inLastDays(toDateTime('2019-12-12T01:11:00Z'), 4)`

返回真。
