---
product: journey optimizer
title: inLastMonths
description: 了解inLastMonths函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastMonths，函数，表达式，历程
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastMonths {#inLastMonths}

如果给定的日期或日期时间介于现在和现在之间 — 增量月份，则返回true。

## 类别

日期

## 函数语法

`inLastMonths(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

## 签名和返回的类型

`inLastMonths(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。
