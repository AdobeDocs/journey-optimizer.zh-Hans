---
product: adobe campaign
title: toDateOnly
description: 了解函数toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: cca94d15da5473aa9890c67af7971f2e745d261e
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 9%

---

# toDateOnly{#toDateOnly}

将参数转换为dateOnly类型值。 要了解有关数据类型的更多信息，请参阅此 [部分](../expression/data-types.md).

## 类别

转化

## 函数语法

`toDateOnly(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 日期的字符串表示形式为“YYYY-MM-DD”（XDM格式）。 还支持ISO-8601格式：仅 **全日期** 考虑部件(请参阅 [RFC 3339，第5.6节](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | 字符串 |
| 日期时间 | dateTime |
| 不带时区的日期时间 | dateTimeOnly |
| 以毫秒为单位的纪元整数值 | 整数 |

## 签名和返回的类型

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

返回dateOnly类型值。

## 示例

`toDateOnly("2016-08-18")`

`toDateOnly("2016-08-18T00:00:00.000Z")`

`toDateOnly("2016-08-18T00:00:00")`

所有变量都返回表示2016-08-18的dateOnly对象。

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

返回dateOnly。
