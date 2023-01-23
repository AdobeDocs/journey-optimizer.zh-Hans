---
product: journey optimizer
title: distinctCountWithNull
description: 了解distinctCountWithNull函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull，函数，表达式，历程
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 22%

---

# distinctCountWithNull {#distinctCountWithNull}

计算不同值的数量，包括空值。

>[!NOTE]
>
>如果目标列表是listObject，则此函数只能在自定义操作表达式中使用。

## 类别

聚合

## 函数语法

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

## 签名和返回的类型

`distinctCountWithNull(<listAny>)`

返回整数。

## 示例

`distinctCountWithNull([10,2,10,null])`

返回3。
