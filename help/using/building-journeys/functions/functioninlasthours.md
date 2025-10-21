---
product: journey optimizer
title: inLastHours
description: 了解inLastHours函数
feature: Journeys
role: Developer
level: Experienced
keywords: inLastHours，函数，表达式，历程
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# inLastHours {#inLastHours}

如果给定的日期时间介于现在和现在之间 — 增量小时，则返回true。

## 类别

日期

## 函数语法

`inLastHours(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

## 签名和返回的类型

`inLastHours(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。

`inLastHours(@event{MyEvent.timestamp}, 4)`

返回真。
