---
product: adobe campaign
title: inLastHours
description: 了解LastHours中的函数
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 17%

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
| 三角洲 | 整数 |

## 签名和返回类型

`inLastHours(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

返回true。

`inLastHours(@{MyEvent.timestamp}, 4)`

返回true。
