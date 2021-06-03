---
title: 函数库
description: 函数库
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# 对象函数 {#objects}

![](../../assets/do-not-localize/badge.png)

## 为null{#isNull}

`isNull`函数确定对象引用是否不存在。

**格式**

```sql
{%= isNull(object) %}
```

**示例**

以下操作会检查人员的家庭地址是否不存在。

```sql
{%= isNull(person.homeAddress) %}
```

## 不为空{#isNotNull}

`isNotNull`函数确定对象引用是否存在。

**格式**

```sql
{%= isNotNull(object) %}
```

**示例**

以下操作会检查人员的家庭地址是否存在。

```sql
{%= isNotNull(person.homeAddress) %}
```
