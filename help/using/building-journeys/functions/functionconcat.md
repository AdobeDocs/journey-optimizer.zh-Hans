---
product: journey optimizer
title: concat
description: 瞭解函式內容
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: concat，函式，運算式，歷程
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

---

# concat {#concat}

串連兩個字串引數或字串清單。

## 类别

字符串

## 函式語法

`concat(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|------------------|
| 列表 | listString |
| 字符串 | 字符串 |

## 簽章和傳回的型別

`concat(<string>,<string>)`

`concat(<listString>)`

傳回字串。

## 示例

`concat("Hello","World")`

傳回「HelloWorld」。

`concat(["Hello"," ","World"])`

傳回「Hello World」。
