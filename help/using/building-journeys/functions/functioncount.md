---
product: journey optimizer
title: count
description: 瞭解函式計數
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: count，計數， function，運算式， journey
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: ad113c0414b20ac2f758ad06a44315b24a3d3d0c
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 28%

---

# count {#count}

計算清單的元素而不考慮null值。

## 类别

聚合

## 函式語法

`count(<listAny>)`

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

## 簽章和傳回型別

`count(<listAny>)`

傳回整數。

## 示例

`count([10,2,10,null])`

傳回3。
