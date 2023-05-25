---
product: journey optimizer
title: substr
description: 了解函数substr
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: substr，函数，表达式，历程
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# substr {#substr}

返回字符串表达式在开始索引和结束索引之间的子字符串。 如果未定义结束索引，则它介于开始索引和结束索引之间。

## 类别

字符串

## 函数语法

`substr(<parameters>)`

## 参数

| 参数 | 类型 |
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
