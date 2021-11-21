---
product: adobe campaign
title: listSize
description: 了解函数listSize
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 34%

---

# listSize {#listSize}

计算列表中的元素数。

## 类别

列表

## 函数语法

`listSize(<parameters>)`

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

## 签名和返回类型

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

`listSize(<listPoint>)`

返回整数。

## 示例

`listSize([10,2,3])`

返回3。
