---
product: journey optimizer
title: inNextDays
description: 了解函数inNextDays
feature: Journeys
role: Developer
level: Experienced
keywords: inNextDays，函数，表达式，历程
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextDays {#inNextDays}

如果给定的日期或日期时间介于现在和现在+增量天之间，则返回true。

## 类别

日期

## 函数语法

`inNextDays(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

## 签名和返回的类型

`inNextDays(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

返回真。
