---
product: journey optimizer
title: count
description: 了解函数计数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 计数，函数，表达式，历程
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---

# count {#count}

计算列表的元素，而不考虑null值。

## 类别

聚合

## 函数语法

`count(<listAny>)`

`count(<listObject>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要处理的列表。 对于listObject，它必须是字段引用。 listObject不能包含null对象。 |

## 签名和返回的类型

`count(<listAny>)`

返回整数。

## 示例

`count([10,2,10,null])`

返回3。

`count(@event{my_event.productListItems})`

返回给定对象数组（listObject类型）中的对象数。 备注： listObject不能包含null对象
