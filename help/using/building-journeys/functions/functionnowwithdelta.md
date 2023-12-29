---
product: journey optimizer
title: nowWithDelta
description: 了解函数nowWithDelta
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: nowWithDelta，函数，表达式，历程
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

---

# nowWithDelta {#nowWithDelta}

返回包含偏移量的当前日期时间。 如果指定了时区ID，将应用时区偏移。 有关数据类型的详细信息，请参阅 [此页面](../expression/data-types.md).

## 类别

日期

## 函数语法

`nowWithDelta(<parameters>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| 增量 | 正或负整数值 |
| 日期部分 | 年、月、日、小时、分钟或秒 |
| 时区id | 时区值的字符串表示形式。 有关更多信息，请参阅 [数据类型](../expression/data-types.md). 时区ID必须是字符串常量。 它不能是字段引用，也不能是表达式。 |

## 签名和返回的类型

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

返回日期时间。

## 示例

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

返回2小时前的dateTime。
