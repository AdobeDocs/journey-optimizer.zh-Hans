---
product: journey optimizer
title: now
description: 立即了解该函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 现在，函数，表达式，历程
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 14%

---

# now {#now}

以日期时间格式返回当前日期。 有关数据类型的详细信息，请参阅[此页面](../expression/data-types.md)。

## 类别

日期

## 函数语法

`now(<parameter>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| 字符串 |  |

## 签名和返回的类型

`now()`

`now("<timeZone id>")`

返回日期时间。

## 示例

`now()`

返回2023-06-03T06:30Z。

`toString(now())`

返回“2023-06-03T06:30Z”

`now("Europe/Paris")`

返回2023-06-03T08:30+02:00。
