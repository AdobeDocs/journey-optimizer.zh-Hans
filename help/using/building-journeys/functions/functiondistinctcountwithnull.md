---
product: journey optimizer
title: distinctCountWithNull
description: 瞭解函式distinctCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull，函式，運算式，歷程
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 22%

---

# distinctCountWithNull {#distinctCountWithNull}

計算包括null值的不同值數目。

>[!NOTE]
>
>如果目標清單是listObject，則此函式只能用於自訂動作運算式。

## 类别

聚合

## 函式語法

`distinctCountWithNull(<listAny>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 列表 | listString |
| 列表 | listBoolean |
| 列表 | listInteger |
| 列表 | listDecimal |
| 列表 | listDuration |
| 列表 | listDateTime |
| 列表 | listDateTimeOnly |
| 列表 | listDateOnly |

## 簽章和傳回的型別

`distinctCountWithNull(<listAny>)`

傳回整數。

## 示例

`distinctCountWithNull([10,2,10,null])`

傳回3。
