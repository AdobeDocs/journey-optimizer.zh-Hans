---
product: journey optimizer
title: toString
description: 瞭解函式toString
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toString，函式，運算式，歷程
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 8%

---

# toString {#toString}

根據其型別，將引數值轉換為字串值。 如需資料型別的詳細資訊，請參閱 [此頁面](../expression/data-types.md).

## 类别

转化

## 函式語法

`toString(<parameter>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| dateTime | 將日期轉換為UTC日期格式 |
| dateTimeOnly | 將日期轉換為UTC日期格式 |
| 持續時間 | 轉換為字串形式的對應毫秒數 |
| 整数 | 轉換為值的字串表示法（1會變成「1」） |
| 小數 | 轉換為值的字串表示法（1.5變成&quot;1.5&quot;） |
| 布尔 | 將布林值轉換為&#39;true&#39; （如果為true）、&#39;false&#39; （如果為false） |

## 簽章和傳回型別

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

傳回字串。

## 示例

`toString(4)`

傳回「4」。

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

傳回指定dateOnly欄位（XDM日期欄位）的字串表示法，例如「2016-08-18」。
