---
product: journey optimizer
title: inNextYears
description: 了解NextYears中的功能
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inNextYears {#inNextYears}

如果给定的日期或dateTime介于现在和现在+增量年之间，则返回true。

## 类别

日期

## 函数语法

`inNextYears(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 三角洲 | 整数 |

## 签名和返回类型

`inNextYears(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

返回true。
