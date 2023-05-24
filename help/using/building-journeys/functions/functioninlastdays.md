---
product: journey optimizer
title: inLastDays
description: 瞭解函式inLastDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays，函式，運算式，歷程
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastDays {#inLastDays}

如果指定的日期或日期時間介於現在和現在 — 差異天數之間，則傳回true。

## 类别

日期

## 函式語法

`inLastDays(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整数 |

## 簽章和傳回型別

`inLastDays(<dateTime>,<integer>)`

傳回布林值。

## 示例

`inLastDays(toDateTime('2019-12-12T01:11:00Z'), 4)`

傳回true。
