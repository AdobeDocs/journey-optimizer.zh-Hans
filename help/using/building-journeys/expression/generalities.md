---
product: Journey Optimizer
title: 语法
description: 了解高级表达式编辑器
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 5%

---

# 高级表达式编辑器语法 {#syntax}

## 括号和表达式优先级{#parentheses-and-expression-priority}

括号可用于使复杂表达式更易读。 _(&lt;expression>)_ 等于 _&lt;expression>_. 括号还可用于定义评估顺序和关联性。

表达式将从左到右进行计算。 必须应用算术运算符的相关性：乘数和分区优先于加减。 要限定特定顺序，必须添加括号以限定操作。 例如：

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| 表达式 | 评估 |
|--- |--- |
| `4 + 2 * 10` | <ul><li>“*”优先于“+”：2 * 10评估→ 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>括号会更改优先级：(4 + 2)评估→ 6</li><li> 6 * 10 → 60</li></ul> |

## 区分大小写{#case-sensitivity}

以下是不同的区分大小写规则：

* 所有运算符（和或等） 应该写成小写。 例如， _`<expression1>`和`<expression2>`_ 是有效的表达式，而 _`<expression1>`和`<expression2>`_ 不是。
* 所有函数名称都区分大小写。 例如， _inSegment()_ 有效，而函数 _INSEGMENT()_ 不是。
* 字段引用和常量值区分大小写：它们不是语言的内置元素（与运算符和函数相反），而是由最终用户创作的。

## 返回的表达式类型{#returned-expression-type}

根据使用的上下文，表达式编辑器可以返回不同的值。

| 高级表达式编辑器用法 | 应返回的表达式类型 |
|--- |--- |
| 条件（数据源条件、日期条件） | 布尔 |
| 自定义计时器 | dateTimeOnly |
| 操作参数映射 | 任何 |
