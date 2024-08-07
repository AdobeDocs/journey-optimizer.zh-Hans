---
product: journey optimizer
title: setDays
description: 了解函数setDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setDays，函数，表达式，历程
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 12%

---

# setDays {#setDays}

仅设置日期时间或日期时间的日期。 例如，如果您要等到月份的某一天，则可以强制该天。

## 类别

日期

## 函数语法

`setDays(<parameter>)`

## 参数

| 参数 | 类型 |
|--- |--- |
| 日期时间 | dateTime |
| 不考虑时区的日期时间 | dateTimeOnly |
| 天数 | 整数 |

## 签名和返回的类型

`setDays(<dateTime>,<days>)`

返回日期时间。

`setDays(<dateTimeOnly>,<days>)`

返回不考虑时区的日期时间。

## 示例

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

返回2023-12-25T01:11:00Z。

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`
