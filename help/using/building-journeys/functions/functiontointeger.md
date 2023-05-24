---
product: journey optimizer
title: toInteger
description: 瞭解函式toInteger
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toInteger，函式，運算式，歷程
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 13%

---

# toInteger {#toInteger}

將引數值轉換為整數。

## 类别

转化

## 函式語法

`toInteger(<parameter>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| 字符串 | 將字串值轉換為整數 |
| dateTime | 將日期轉換為毫秒數（紀元毫秒） |
| 小數 | 透過移除小數部分轉換為整數（範例： 1.5變為1） |
| 布尔 | 將布林值轉換為1 （如果為true）、0 （如果為false） |

## 簽章和傳回型別

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

傳回整數。

## 示例

`toInteger("4")`

傳回4。
