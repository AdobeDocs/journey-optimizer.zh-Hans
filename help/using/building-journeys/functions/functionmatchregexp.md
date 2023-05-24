---
product: journey optimizer
title: matchRegExp
description: 瞭解函式matchRegExp
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: matchRegExp，函式，運算式，歷程
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 17%

---

# matchRegExp {#matchRegExp}

如果第一個引數中的字串符合第二個引數中的規則運算式，則傳回true。 如需詳細資訊，請參閱 [此頁面](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## 类别

字符串

## 函式語法

`matchRegExp(<parameters>)`

## 参数

| 参数 | 类型 |
|--- |--- |
| 字符串 | 字符串 |
| regexp | 字符串 |

## 簽章和傳回的型別

`matchRegExp(<string>,<string>)`

傳回布林值。

## 示例

`matchRegExp("username@adobe.com", "*adobe")`

傳回true。
