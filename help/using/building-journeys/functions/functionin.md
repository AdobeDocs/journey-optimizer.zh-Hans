---
product: journey optimizer
title: in
description: 了解中的函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: in，函数，表达式，历程
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 23%

---

# in {#in}

检查第一个参数值是否在列表中。 检查通过对每个参数值执行Equal。 如果找到参数值，则返回true；否则，返回false。

`<expression>`的类型必须与列表项匹配。 作为提醒，列表的项目类型必须匹配。

## 类别

列表

## 函数语法

`in(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 布尔值 | 布尔值 |
| 整数 | 整数 |
| 小数 | 小数 |
| 持续时间 | 持续时间 |
| 日期时间 | 日期时间 |
| DateTimeOnly | DateTimeOnly |
| 列表 | listString |
| 列表 | listBoolean |
| 列表 | listInteger |
| 列表 | listDecimal |
| 列表 | listDuration |
| 列表 | listDateTime |
| 列表 | listDateTimeOnly |
| 列表 | listDateOnly |

## 签名和返回的类型

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

返回布尔值。

## 示例

`in(4,[4,5,3,4])`

返回真。

`in(8,[4,5,3,4])`

返回假。

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
