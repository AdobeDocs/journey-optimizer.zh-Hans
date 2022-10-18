---
product: journey optimizer
title: inNextMonths
description: 了解NextMonths中的函数
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inNextMonths {#inNextMonths}

如果给定的日期或dateTime介于现在和现在+增量月之间，则返回true。

## 类别

日期

## 函数语法

`inNextMonths(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 三角洲 | 整数 |

## 签名和返回类型

`inNextMonths(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inNextMonths(toDateTime('2020-01-12T01:11:00Z'), 4)`

返回true。
