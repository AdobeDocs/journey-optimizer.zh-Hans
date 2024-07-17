---
product: journey optimizer
title: distinctCountWithNull
description: 了解函数distinctCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull，函数，表达式，历程
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# distinctCountWithNull {#distinctCountWithNull}

计算不同值（包括空值）的数量。

请注意，此函数不支持参数`<listObject>`。

## 类别

聚合

## 函数语法

`distinctCountWithNull(<listAny>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly |

## 签名和返回的类型

`distinctCountWithNull(<listAny>)`

返回整数。

## 示例

`distinctCountWithNull([10,2,10,null])`

返回3。
