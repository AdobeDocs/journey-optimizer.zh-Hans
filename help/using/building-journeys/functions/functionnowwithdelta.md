---
product: journey optimizer
title: nowWithDelta
description: 瞭解nowWithDelta函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: nowWithDelta，函式，運算式，歷程
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 7%

---

# nowWithDelta {#nowWithDelta}

傳回包含位移的目前日期時間。 如果指定了時區識別碼，則會套用時區位移。 如需資料型別的詳細資訊，請參閱 [此頁面](../expression/data-types.md).

## 类别

日期

## 函式語法

`nowWithDelta(<parameters>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| delta | 正整數或負整數 |
| 日期部分 | 年、月、日、小時、分鐘或秒作為字串 |
| 時區id | 時區值的字串表示。 如需詳細資訊，請參閱 [資料型別](../expression/data-types.md). 時區ID必須是字串常數。 它不能是欄位參考或運算式。 |

## 簽章和傳回型別

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

傳回日期時間。

## 示例

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

傳回2小時前的日期時間。
