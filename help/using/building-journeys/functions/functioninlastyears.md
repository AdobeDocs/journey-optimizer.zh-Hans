---
product: journey optimizer
title: inLastYears
description: 了解函数inLastYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastYears，函数，表达式，历程
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastYears {#inLastYears}

如果给定的日期或日期时间介于现在和现在之间 — 增量年，则返回true。

## 类别

日期

## 函数语法

`inLastYears(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

## 签名和返回的类型

`inLastYears(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。
