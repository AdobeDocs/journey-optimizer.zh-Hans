---
product: journey optimizer
title: toDateOnly
description: 瞭解函式toDateOnly
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly，函式，運算式，歷程
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 10%

---

# toDateOnly{#toDateOnly}

將引數轉換為dateOnly型別值。 若要進一步瞭解資料型別，請參閱此 [區段](../expression/data-types.md).

## 类别

转化

## 函式語法

`toDateOnly(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 以「YYYY-MM-DD」（XDM格式）表示日期的字串表示法。 也支援ISO-8601格式：僅限 **完整日期** 已考慮零件(請參閱 [RFC 3339,5.6節](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | 字符串 |
| 日期時間 | dateTime |
| 沒有時區的日期時間 | dateTimeOnly |
| 紀元的整數值（以毫秒為單位） | 整数 |

## 簽章和傳回的型別

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

傳回dateOnly型別值。

## 示例

`toDateOnly("2016-08-18")`

`toDateOnly("2016-08-18T00:00:00.000Z")`

`toDateOnly("2016-08-18T00:00:00")`

所有傳回表示2016-08-18的dateOnly物件。

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

傳回dateOnly。
