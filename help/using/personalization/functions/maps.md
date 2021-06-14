---
title: 映射函数库
description: 映射函数库
feature: 个性化
topic: 个性化
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 7%

---

# 映射函数{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL)提供了一些函数，可简化与映射的交互。

## 获取{#get}

`get`函数用于检索给定键的映射值。

**格式**

```sql
{%= get(map, string) %}
```

**示例**

以下操作将获取键`example@example.com`的标识映射值。

```sql
{%= get(identityMap,"example@example.com") %}
```

## 键{#keys}

`keys`函数用于检索给定映射的所有键。

**格式**

```sql
{%= keys(map) %}
```

**示例**

以下操作将获取映射`identityMap`的所有键值。

```sql
{%= keys(identityMap) %}
```

## 值{#values}

`values`函数用于检索给定映射的所有值。

**格式**

```sql
{%= values(map) %}
```

**示例**

以下操作将获取映射`identityMap`的所有值。

```sql
{%= values(identityMap) %}
```
