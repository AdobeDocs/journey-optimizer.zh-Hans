---
product: journey optimizer
title: toInteger
description: 了解函数toInteger
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toInteger，函数，表达式，历程
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 13%

---

# toInteger {#toInteger}

将参数值转换为整数。

## 类别

转化

## 函数语法

`toInteger(<parameter>)`

## 参数

| 参数 | 描述 |
|--- |--- |
| 字符串 | 将字符串值转换为整数 |
| dateTime | 将日期转换为毫秒数（纪元毫秒） |
| 小数 | 通过删除小数部分转换为整数(示例：1.5变为1) |
| 布尔 | 如果为true，则将布尔值转换为1；如果为false，则将布尔值转换为0 |

## 签名和返回类型

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

返回整数。

## 示例

`toInteger("4")`

返回4。
