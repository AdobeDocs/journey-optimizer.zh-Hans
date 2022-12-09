---
product: journey optimizer
title: inLastYears
description: 了解LastYears中的函数
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 0%

---

# inLastYears {#inLastYears}

如果给定的日期或dateTime介于现在和现在之间 — 增量年，则返回true。

## 类别

日期

## 函数语法

`inLastYears(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 三角洲 | 整数 |

## 签名和返回类型

`inLastYears(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

返回true。
