---
product: journey optimizer
title: replaceAll
description: 了解函数replaceAll
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: replaceAll，函数，表达式，历程
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---

# replaceAll {#replaceAll}

使用基字符串中的替换字符串替换匹配目标字符串的所有匹配项。

例如，替换操作从字符串的开头到结尾进行，将字符串“aaa”中的“aa”替换为“b”将导致“ba”而不是“ab”。

## 类别

字符串

## 函数语法

`replaceAll(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|--------------|
| 基础 | 字符串 |
| Target | 字符串（正则表达式） |
| 替换 | 字符串 |

## 签名和返回的类型

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

返回字符串。

## 示例{#example}

`replaceAll("Hello World", "l", "x")`

返回“Hexxo Worxd”。

由于目标参数是RegExp，因此根据要替换的字符串，您可能需要转义某些字符。 请参阅中的示例 [此页面](../functions/functionreplace.md#example_2).
