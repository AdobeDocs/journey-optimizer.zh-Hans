---
product: adobe campaign
title: now
description: 立即了解该函数
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# now {#now}

以日期时间格式返回当前日期。 有关数据类型的更多信息，请参阅 [本页](../expression/data-types.md).

## 类别

日期

## 函数语法

`now(<parameter>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| 字符串 |  |

## 签名和返回类型

`now()`

`now("<timeZone id>")`

返回dateTime。

## 示例

`now()`

返回2019-06-03T06:30Z。

`toString(now())`

返回“2019-06-03T06:30Z”

`now("Europe/Paris")`

返回2019-06-03T08:30+02:00。
