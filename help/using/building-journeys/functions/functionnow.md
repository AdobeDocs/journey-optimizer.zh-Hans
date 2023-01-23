---
product: journey optimizer
title: now
description: 立即了解该函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 现在，函数，表达式，旅程
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 16%

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
