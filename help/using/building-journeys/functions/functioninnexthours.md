---
product: journey optimizer
title: inNextHours
description: 了解inNextHours函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextHours，函数，表达式，历程
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextHours {#inNextHours}

如果给定的日期或日期时间介于现在和现在+增量小时数之间，则返回true。

## 类别

日期

## 函数语法

`inNextHours(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| delta | 整数 |

## 签名和返回类型

`inNextHours(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inNextHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

返回真。
