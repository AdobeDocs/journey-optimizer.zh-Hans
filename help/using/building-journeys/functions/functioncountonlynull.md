---
product: journey optimizer
title: countOnlyNull
description: 了解函数countOnlyNull
feature: Journeys
role: Engineer
level: Experienced
keywords: countOnlyNull，函数，表达式，历程
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# countOnlyNull {#countOnlyNull}

计算列表中的空值的数量。

请注意，此函数不支持参数`<listObject>`。

## 类别

聚合

## 函数语法

`countOnlyNull(<listAny>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly |

## 签名和返回的类型

`countOnlyNull(<listAny>)`

返回整数。

## 示例

`countOnlyNull([10,2,10,null])`

返回1。
