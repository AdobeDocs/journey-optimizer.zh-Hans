---
product: adobe campaign
title: substr
description: 了解函数子字符串
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 15%

---

# substr {#substr}

返回开始索引和结束索引之间的字符串表达式的子字符串。 如果未定义结束索引，则它介于开始索引和结束索引之间。

## 类别

字符串

## 函数语法

`substr(<parameters>)`

## 参数

| 参数 | type |
|-------------|----------|
| 字符串 | 字符串 |
| beginIndex | 整数 |
| endIndex | 整数 |

## 签名和返回的类型

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

返回字符串。

## 示例

`substr("Hello World",6)`

返回“World”。

`substr("Hello World", 0, 5)`

返回“Hello”。
