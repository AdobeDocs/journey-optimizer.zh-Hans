---
title: 映射函数库
description: 映射函数库
feature: 个性化
topic: 个性化
role: Data Engineer
level: Experienced
source-git-commit: e3b7e80b72e6be71d5b38cd5507d20ad2e8ca8d4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 7%

---

# 映射函数{#maps}

在个性化中使用映射函数，以便更轻松地与映射交互。

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
