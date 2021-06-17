---
title: 对象函数库
description: 对象函数库
feature: 个性化
topic: 个性化
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 10%

---

# 对象函数 {#objects}

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
