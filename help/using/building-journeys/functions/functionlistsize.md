---
product: journey optimizer
title: listSize
description: 了解函数listSize
feature: Journeys
role: Developer
level: Experienced
keywords: listSize，函数，表达式，历程
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 11%

---

# listSize {#listSize}

计算列表中的元素数。

## 类别

列表

## 函数语法

`listSize(<parameters>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要处理的列表。 对于listObject，它必须是字段引用。 listObject不能包含null对象。 |

## 签名和返回的类型

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

返回整数。

`listSize(<listObject>)`

## 示例

`listSize([10,2,3])`

返回3。

`listSize(@event{my_event.productListItems})`

返回给定对象数组（listObject类型）中的对象数。
