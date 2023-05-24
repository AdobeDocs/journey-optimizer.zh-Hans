---
product: journey optimizer
title: now
description: 立即瞭解函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 現在，函式，運算式，歷程
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 16%

---

# now {#now}

以日期時間格式傳回目前日期。 如需資料型別的詳細資訊，請參閱 [此頁面](../expression/data-types.md).

## 类别

日期

## 函式語法

`now(<parameter>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| 字符串 |  |

## 簽章和傳回型別

`now()`

`now("<timeZone id>")`

傳回日期時間。

## 示例

`now()`

傳回2019-06-03T06:30Z。

`toString(now())`

傳回「2019-06-03T06:30Z」

`now("Europe/Paris")`

傳回2019-06-03T08:30+02:00。
