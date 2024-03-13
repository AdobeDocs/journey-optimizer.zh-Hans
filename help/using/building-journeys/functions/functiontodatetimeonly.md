---
product: journey optimizer
title: toDateTimeOnly
description: 了解函数toDateTime
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateTimeOnly，函数，表达式，历程
exl-id: db54c119-5080-403a-b254-43645be6b4a8
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 14%

---

# toDateTimeOnly{#toDateTimeOnly}

将参数值转换为仅日期时间值。

## 类别

转化

## 函数语法

`toDateTimeOnly(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| ISO-8601或“YYYY-MM-DD”格式的日期时间（XDM日期格式） | 字符串 |
| 日期时间 | dateTime |

## 签名和返回的类型

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`
<!--`toDateTimeOnly(<integer>,<integer>,<integer>)`
`toDateTimeOnly(<integer>,<integer>,<integer>,<integer>,<integer>,<integer>)`-->

返回不考虑时区的日期时间。

## 示例

`toDateTimeOnly ("2023-08-18")`

返回表示2023-08-18T00的日期时间:00:00.000

`toDateTimeOnly(now())`

<!--`toDateTimeOnly(2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000.

`toDateTimeOnly(2016,8,18)`

Returns 2016-08-18T00:00:00.000.-->
