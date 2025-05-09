---
product: journey optimizer
title: toDateOnly
description: 了解函数toDateOnly
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly，函数，表达式，历程
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 1af75a0e6bfc2c3b9c565c3190f46d137a68d32e
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 10%

---

# toDateOnly{#toDateOnly}

将参数转换为dateOnly类型值。 要了解有关数据类型的更多信息，请参阅此[部分](../expression/data-types.md)。

## 类别

转化

## 函数语法

`toDateOnly(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 以“YYYY-MM-DD”形式表示的日期的字符串（XDM格式）。 还支持ISO-8601格式：仅考虑&#x200B;**完整日期**&#x200B;部分（请参阅[RFC 3339，第5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6)节） | 字符串 |
| 日期时间 | dateTime |
| 不带时区的日期时间 | dateTimeOnly |
| 纪元的整数值（以毫秒为单位） | 整数 |

## 签名和返回的类型

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

返回dateOnly类型值。

## 示例

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

所有参数都返回表示2023-08-18的dateOnly对象。

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

返回dateOnly。
