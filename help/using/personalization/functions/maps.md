---
title: 映射函数库
description: 映射函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 5%

---

# 映射函数{#maps}

在个性化中使用映射函数，以便更轻松地与映射交互。

## 获取{#get}

的 `get` 函数用于检索给定键值的映射值。

**格式**

```sql
{%= get(map, string) %}
```

**示例**

以下操作将获取键的标识映射值 `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## 键{#keys}

的 `keys` 函数用于检索给定映射的所有键。

**格式**

```sql
{%= keys(map) %}
```

**示例**

以下操作将获取映射的所有键值 `identityMap`.

```sql
{%= keys(identityMap) %}
```

## 值{#values}

的 `values` 函数检索给定映射的所有值。

**格式**

```sql
{%= values(map) %}
```

**示例**

以下操作将获取映射的所有值 `identityMap`.

```sql
{%= values(identityMap) %}
```
