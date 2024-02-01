---
product: journey optimizer
title: serializeList
description: 了解函数serializeList
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList，函数，表达式，历程
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

---

# serializeList {#serializeList}

将给定列表（除listObject之外的任何类型）转换为字符串。

## 类别

列表

## 函数语法

`serializeList(<parameters>)`

## 参数

| 参数 | 类型 | 描述 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly | 要转换为字符串的列表。 |
| 分隔符 | 字符串 | 输出字符串中每个列表元素之间的分隔符。 |
| addQuotes | 布尔 | 此参数指示输出字符串中的每个元素是否应包含引号(true)或(false)。 |

## 签名和返回的类型

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

返回字符串。

## 示例

`serializeList(["Hello","World"], " ", false)`

返回“Hello World”。

`serializeList(["Hello", "World"], ",", true)`

返回“Hello”、“World”。
