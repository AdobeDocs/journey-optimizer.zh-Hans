---
product: journey optimizer
title: toDateTime
description: 了解函数toDateTime
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateTime，函数，表达式，历程
exl-id: 2b487e60-593e-4bf7-9639-f469ba0f5cdc
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 10%

---

# toDateTime {#toDateTime}

根据参数类型将参数转换为日期时间值。

## 类别

转化

## 函数语法

`toDateTime(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| ISO-8601格式的日期时间 | 字符串 |
| 时区id | 字符串 |
| 不带时区的日期时间 | dateTimeOnly |
| 纪元的整数值（以毫秒为单位） | 整数 |

>[!NOTE]
>
>时区ID必须是字符串常量。 它不能是字段引用，也不能是表达式。 有关数据类型的详细信息，请参阅[此页面](../expression/data-types.md)。

## 签名和返回的类型

`toDateTime(<string>)`

`toDateTime(<stringified time zone id>, <dateTimeOnly>)`

`toDateTime(<integer>)`

返回&#x200B;**日期时间**。

<!--`toDateTime(<year>,<month>,<dayOfMonth>,<hour>,<minute>,<second>)`

Returns a date time with default time zone UTC.

`toDateTime(<year>,<month>,<dayOfMonth>)`
`toDateTime(<stringified timeZone>,<year>,<month>,<dayOfMonth>)`
`toDateTime(<timeZone>,<year>,<month>,<dayOfMonth>)`

Return a datetime where hour, minute and second set to 0.

`toDateTime(<stringified timeZone>,<year>,<month>,<dayOfMonth>,<hour>,<minute>,<second>)`
`toDateTime(<string>)`
`toDateTime(<string>,<integer>)`
`toDateTime(<stringified timeZone>,<dateTimeOnly)`

`toDateTime(<timeZone>,<integer>)`

Return a datetime.

-->

## 示例

`toDateTime ("2023-08-18T23:17:59.123Z")`

返回2023-08-18T23:17:59.123Z

`toDateTime(toDateTimeOnly("UTC", "2023-08-18T23:17:59.123"))`

返回2023-08-18T23:17:59.123Z

`toDateTime(1560762190189)`

返回2023-06-17T09:03:10.189Z

<!--`toDateTime ("2016-08-18T23:17:59.123", "UTC")`

Returns 2016-08-18T23:17:59.123Z.

`toDateTime("Z",2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000Z.

`toDateTime("Z",2016,8,18)`

Returns 2016-08-18T00:00:00.000Z.-->
