---
product: journey optimizer
title: countWithNull
description: 了解函数countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull，函数，表达式，历程
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 30%

---

# countWithNull {#countWithNull}

计算列表的所有元素，包括null值。

## 类别

聚合

## 函数语法

`countWithNull(<listAny>)`

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

`countWithNull(<listAny>)`

返回一个整数。

## 示例

`countWithNull([10,2,10,null])`

返回4。
