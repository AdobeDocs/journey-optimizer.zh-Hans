---
product: journey optimizer
title: concat
description: 了解函数连接
feature: Journeys
role: Engineer
level: Experienced
keywords: concat，函数，表达式，历程
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

---

# concat {#concat}

连接两个字符串参数或一个字符串列表。

## 类别

字符串

## 函数语法

`concat(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 列表 | listString |
| 字符串 | 字符串 |

## 签名和返回的类型

`concat(<string>,<string>)`

`concat(<listString>)`

返回字符串。

## 示例

`concat("Hello","World")`

返回“HelloWorld”。

`concat(["Hello"," ","World"])`

返回“Hello World”。
