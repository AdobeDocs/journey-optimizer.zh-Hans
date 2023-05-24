---
product: journey optimizer
title: startWith
description: 瞭解函式startWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWith，函式，運算式，歷程
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# startWith {#startWith}

如果第二個引數是第一個引數的前置詞，則傳回true。

## 类别

字符串

## 函式語法

`startWith(<parameters>)`

## 参数

| 参数 | 类型 |
|-------------|--------|
| 字符串 | 字符串 |
| 前置詞 | 字符串 |

## 簽章和傳回的型別

`startWith(<string>,<string>)`

傳回布林值。

## 示例

`startWith("Hello World", "Hello")`

傳回true。

`startWith("Hello World", "World")`

傳回false。
