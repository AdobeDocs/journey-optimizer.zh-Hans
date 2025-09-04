---
product: journey optimizer
title: countWithNull
description: 了解函数countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull，函数，表达式，历程
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# countWithNull {#countWithNull}

计算列表的所有元素，包括null值。

请注意，此函数不支持参数`<listObject>`。

## 类别

聚合

## 函数语法

`countWithNull(<listAny>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly |

## 签名和返回的类型

`countWithNull(<listAny>)`

返回整数。

## 示例

`countWithNull([10,2,10,null])`

返回4。
