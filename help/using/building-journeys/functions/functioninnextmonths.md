---
product: journey optimizer
title: inNextMonths
description: 了解inNextMonths函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextMonths，函数，表达式，历程
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextMonths {#inNextMonths}

如果给定的日期或日期时间介于现在和现在+增量月份之间，则返回true。

## 类别

日期

## 函数语法

`inNextMonths(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期时间 | dateTime |
| 增量 | 整数 |

## 签名和返回的类型

`inNextMonths(<dateTime>,<integer>)`

返回布尔值。

## 示例

`inNextMonths(toDateTime('2020-01-12T01:11:00Z'), 4)`

返回真。
