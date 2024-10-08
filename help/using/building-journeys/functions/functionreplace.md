---
product: journey optimizer
title: replace
description: 了解函数替换
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 替换，函数，表达式，历程
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 11%

---

# replace {#replace}

使用基本字符串中的替换字符串替换匹配目标字符串的第一个匹配项。

例如，替换操作从字符串的开头到结尾进行，将字符串“aaa”中的“aa”替换为“b”将导致“ba”而不是“ab”。

## 类别

字符串

## 函数语法

`replace(<parameters>)`

## 参数

| 参数 | 类型 |
|-----------|--------------|
| 基础 | 字符串 |
| 目标 | 字符串(RegExp) |
| 替换 | 字符串 |

## 签名和返回的类型

`replace(<base>,<target>,<replacement>)`

返回字符串。

## 示例 1

`replace("Hello World", "l", "x")`

返回“Hexlo World”。

## 示例 2 {#example_2}

由于target参数是RegExp，因此根据要替换的字符串，您可能需要转义某些字符。 示例如下：

* 要计算的字符串：`|OFFER_A|OFFER_B`
* 由配置文件属性`#{ExperiencePlatform.myFieldGroup.profile.myOffers}`提供
* 要替换的字符串： `|OFFER_A`
* 字符串替换为： `''`
* 您需要在`|`字符之前添加`\\`。

表达式为：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

返回的字符串是： `|OFFER_B`

您还可以构建要替换给定属性的字符串：

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
