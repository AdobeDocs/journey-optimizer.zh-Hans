---
product: journey optimizer
title: countOnlyNull
description: 瞭解函式countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull，函式，運算式，歷程
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 30%

---

# countOnlyNull {#countOnlyNull}

計算清單中null值的數量。

## 类别

聚合

## 函式語法

`countOnlyNull(<listAny>)`

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

`countOnlyNull(<listAny>)`

傳回整數。

## 示例

`countOnlyNull([10,2,10,null])`

傳回1。
