---
product: journey optimizer
title: toString
description: 了解函数toString
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toString，函数，表达式，历程
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---

# toString {#toString}

根据类型将参数值转换为字符串值。 有关数据类型的详细信息，请参阅 [此页面](../expression/data-types.md).

## 类别

转化

## 函数语法

`toString(<parameter>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| dateTime | 将日期转换为UTC日期格式 |
| dateTimeOnly | 将日期转换为UTC日期格式 |
| 持续时间 | 转换为字符串形式的相应毫秒数 |
| 整数 | 转换为值的字符串表示形式（1变为“1”） |
| 小数 | 转换为值的字符串表示形式（1.5变为“1.5”） |
| 布尔 | 将布尔值转换为“true”（如果为true），“false”（如果为false） |

## 签名和返回的类型

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

返回字符串。

## 示例

`toString(4)`

返回“4”。

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

返回给定dateOnly字段（XDM日期字段）的字符串表示形式，例如“2023-08-18”。

`toString(toDuration(1520))`

返回“PT1.52S”。
