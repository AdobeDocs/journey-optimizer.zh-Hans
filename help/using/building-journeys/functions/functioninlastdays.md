---
product: adobe campaign
title: inLastDays
description: 了解LastDays中的函数
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inLastDays {#inLastDays}

如果给定的日期或dateTime介于现在和现在之间 — 增量天数，则返回true。

## 类别

日期

## 函数语法

`inLastDays(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 三角洲 | 整数 |

## 签名和返回类型

`inLastDays(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inLastDays(toDateTime('2019-12-12T01:11:00Z'), 4)`

返回true。
