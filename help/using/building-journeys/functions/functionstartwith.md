---
product: journey optimizer
title: startWith
description: 了解函数startWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWith，函数，表达式，历程
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# startWith {#startWith}

如果第二个参数是第一个参数的前缀，则返回true。

## 类别

字符串

## 函数语法

`startWith(<parameters>)`

## 参数

| 参数 | 类型 |
|-------------|--------|
| 字符串 | 字符串 |
| 前缀 | 字符串 |

## 签名和返回的类型

`startWith(<string>,<string>)`

返回布尔值。

## 示例

`startWith("Hello World", "Hello")`

返回真。

`startWith("Hello World", "World")`

返回假。
