---
product: journey optimizer
title: in
description: 瞭解中的函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: in，函式，運算式，歷程
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 18%

---

# in {#in}

檢查第一個引數值是否在清單中。 檢查會透過每個引數值上的「等於」來執行。 如果找到引數值，則會傳回true，否則會傳回false。

型別 `<expression>` 必須與清單專案相符。 作為提醒，清單的專案型別必須彼此相符。

## 类别

列表

## 函式語法

`in(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 字符串 | 字符串 |
| 布尔值 | 布尔型 |
| 整数 | 整数 |
| 小數 | 小數 |
| 持續時間 | 持續時間 |
| 日期時間 | 日期時間 |
| DateTimeOnly | DateTimeOnly |
| 列表 | listString |
| 列表 | listBoolean |
| 列表 | listInteger |
| 列表 | listDecimal |
| 列表 | listDuration |
| 列表 | listDateTime |
| 列表 | listDateTimeOnly |
| 列表 | listDateOnly |

## 簽章和傳回的型別

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

傳回布林值。

## 示例

`in(4,[4,5,3,4])`

傳回true。

`in(8,[4,5,3,4])`

傳回false。

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
