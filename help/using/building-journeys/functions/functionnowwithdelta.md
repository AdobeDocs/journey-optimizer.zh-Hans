---
product: journey optimizer
title: nowWithDelta
description: 了解函数nowWithDelta
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# nowWithDelta {#nowWithDelta}

返回包含偏移的当前日期时间。 如果指定了时区ID，则将应用时区偏移。 有关数据类型的更多信息，请参阅 [本页](../expression/data-types.md).

## 类别

日期

## 函数语法

`nowWithDelta(<parameters>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| 三角洲 | 正整数或负整数值 |
| 日期部分 | 年、月、日、小时、分钟或秒（字符串） |
| 时区id | 时区值的字符串表示形式。 有关更多信息，请参阅 [数据类型](../expression/data-types.md). 时区ID必须是字符串常量。 它不能是字段引用或表达式。 |

## 签名和返回类型

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

返回dateTime。

## 示例

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

返回恰好2小时前的dateTime。
