---
product: journey optimizer
title: distinct
description: 瞭解不同的函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinct，不同，函式，運算式，歷程
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 6%

---

# distinct {#distinct}

傳回給定清單的不同值或物件。 會忽略Null專案。

>[!NOTE]
>
>如果目標清單是listObject，則此函式只能用於自訂動作運算式。

## 类别

列表

## 函式語法

`distinct(<parameters>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 |
| keyAttributeName | 字符串 | 此引數是選用引數，僅適用於listObject。 如果未提供引數，如果所有屬性的值都相同，則會將物件視為重複。 否則，如果給定的屬性具有相同的值，則會將物件視為重複。 |

## 簽章和傳回的型別

`distinct(<listInteger>)`

傳回整數清單。

`distinct(<listDecimal>)`

傳回小數點清單。

`distinct(<listString>)`

傳回字串清單。

`distinct(<listDateTimeOnly>)`

傳回日期時間清單，不考慮時區。

`distinct(<listDateTime>)`

傳回日期時間清單。

`distinct(<listDateOnly>)`

傳回日期清單。

`distinct(<listBoolean>)`

傳回布林值清單。

`distinct(<listDuration>)`

傳回持續時間清單。

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

傳回物件清單。


## 示例

`distinct([10,2,10,null])`

返回结果 `[10, 2]`.
