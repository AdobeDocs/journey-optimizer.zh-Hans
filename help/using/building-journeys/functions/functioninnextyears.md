---
product: journey optimizer
title: inNextYears
description: 了解函数inNextYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextYears，函数，表达式，历程
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextYears {#inNextYears}

如果给定的日期或日期时间介于现在和现在+增量年之间，则返回true。

## 类别

日期

## 函数语法

`inNextYears(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

## 签名和返回的类型

`inNextYears(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

返回真。
