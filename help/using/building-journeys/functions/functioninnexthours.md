---
product: journey optimizer
title: inNextHours
description: 了解inNextHours的函数
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inNextHours {#inNextHours}

如果给定的日期或dateTime介于现在和现在+增量小时之间，则返回true。

## 类别

日期

## 函数语法

`inNextHours(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 三角洲 | 整数 |

## 签名和返回类型

`inNextHours(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inNextHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

返回true。
