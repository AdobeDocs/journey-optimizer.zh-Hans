---
product: journey optimizer
title: replaceAll
description: 瞭解函式replaceAll
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: replaceAll，函式，運算式，歷程
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---

# replaceAll {#replaceAll}

以基礎字串中的取代字串取代符合目標字串的所有專案。

取代會從字串的開頭到結尾進行，例如，將字串「aaa」中的「aa」取代為「b」將會產生「ba」而不是「ab」。

## 类别

字符串

## 函式語法

`replaceAll(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|--------------|
| 基底 | 字符串 |
| Target | 字串(RegExp) |
| 取代 | 字符串 |

## 簽章和傳回的型別

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

傳回字串。

## 示例{#example}

`replaceAll("Hello World", "l", "x")`

傳回「Hexxo Worxd」。

由於目標引數是RegExp，因此根據您要取代的字串，您可能需要逸出部分字元。 請參考中的範例 [此頁面](../functions/functionreplace.md#example_2).
