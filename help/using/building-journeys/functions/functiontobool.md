---
product: journey optimizer
title: toBool
description: 了解toBool函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: tobool，函数，表达式，历程
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 11%

---

# toBool {#toBool}

根据参数值的类型，将其转换为布尔值。

* 从字符串：尝试将字符串值转换为布尔值，如果字符串值为“true”，则从“true”；否则从“false”
* 从数值：如果数值不等于0，则为真，否则为假

## 类别

转化

## 函数语法

`toBool(<parameter>)`

## 参数

* 十进制
* 布尔
* 字符串
* 整数

## 签名和返回的类型

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

返回布尔值。

## 示例

`toBool("true")`

`toBool(1)`

返回真。

`toBool("this is not a boolean")`

返回假。
