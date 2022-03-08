---
product: adobe campaign
title: toString
description: 了解函数toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

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
