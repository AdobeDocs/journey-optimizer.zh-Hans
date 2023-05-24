---
product: journey optimizer
title: inNextMonths
description: 瞭解函式inNextMonths
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextMonths，函式，運算式，歷程
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextMonths {#inNextMonths}

如果指定的日期或日期時間介於現在和現在+差異月份之間，則傳回true。

## 类别

日期

## 函式語法

`inNextMonths(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整数 |

## 簽章和傳回型別

`inNextMonths(<dateTime>,<integer>)`

傳回布林值。

## 示例

`inNextMonths(toDateTime('2020-01-12T01:11:00Z'), 4)`

傳回true。
