---
product: adobe campaign
title: toString
description: 了解函数toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: cca94d15da5473aa9890c67af7971f2e745d261e
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 7%

---

# toString {#toString}

根据参数值的类型，将其转换为字符串值。 有关数据类型的更多信息，请参阅 [本页](../expression/data-types.md).

## 类别

转化

## 函数语法

`toString(<parameter>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| dateTime | 以UTC日期格式转换日期 |
| dateTimeOnly | 以UTC日期格式转换日期 |
| 持续时间 | 转换为字符串形式的相应毫秒数 |
| 整数 | 转换为值的字符串表示形式（1变为“1”） |
| 小数 | 转换为值的字符串表示形式（1.5变为“1.5”） |
| 布尔 | 如果为true，则将布尔值转换为“true”；如果为false，则将布尔值转换为“false” |

## 签名和返回类型

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

返回给定dateOnly字段（XDM日期字段）的字符串表示形式，例如“2016-08-18”。
