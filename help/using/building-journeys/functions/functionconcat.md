---
product: journey optimizer
title: concat
description: 了解函数概念
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '40'
ht-degree: 27%

---

# concat {#concat}

串联两个字符串参数或字符串列表。

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
