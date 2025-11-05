---
product: journey optimizer
title: 数学函数
description: 了解数学函数
feature: Journeys
role: Developer
level: Experienced
keywords: 数学，函数，表达式，历程，计算，数字
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 7%

---

# 数学函数 {#math-functions}

数学函数为历程表达式中的数值计算提供基本的数学运算。 利用这些函数，可以对数据执行精确的数字计算和转换。

当您需要执行以下操作时，请使用数学函数：

* 生成用于测试、取样或随机化([random](#random))的随机值
* 将小数位四舍五入到最接近的整数，以便显示更干净的数据([round](#round))
* 对数值字段执行数学计算
* 转换数值以实现业务逻辑和决策

数学函数处理十进制和整数类型，自动管理类型转换以确保历程表达式中的结果准确。

## random {#random}

生成一个介于0和1之间的随机数。

+++句法

`random()`

+++

+++签名和返回的类型

`random()`

返回小数。

+++

## round {#round}

返回与参数最接近的整数值，并将四舍五入设置为正无限。

+++句法

`round(<parameters>)`

+++

+++参数

* 小数
* 整数

+++

+++签名和返回的类型

`round(<decimal>)`

`round(<integer>)`

返回整数。

+++

+++示例

`round(3.14)`

返回3。

`round(3.54)`

返回4。

`round(-3.14)`

返回–3。

`round(3)`

返回3。

+++

