---
product: journey optimizer
title: inNextDays
description: 瞭解函式inNextDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextDays，函式，運算式，歷程
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextDays {#inNextDays}

如果指定的日期或日期時間介於現在和現在+差異天數之間，則傳回true。

## 类别

日期

## 函式語法

`inNextDays(<dateTime>,<delta>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整数 |

## 簽章和傳回型別

`inNextDays(<dateTime>,<integer>)`

傳回布林值。

## 示例

`inNextDays(toDateTime('2010-12-12T01:11:00Z'), 4)`

傳回true。
