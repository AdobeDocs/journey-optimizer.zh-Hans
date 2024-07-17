---
title: 对象函数库
description: 对象函数库
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 19%

---

# 对象函数 {#objects}

## 为空{#isNull}

`isNull`函数确定对象引用是否不存在。

**语法**

```sql
{%= isNull(object) %}
```

**示例**

以下操作检查人员的家庭地址是否不存在。

```sql
{%= isNull(person.homeAddress) %}
```

## 不为空{#isNotNull}

`isNotNull`函数确定是否存在对象引用。

**语法**

```sql
{%= isNotNull(object) %}
```

**示例**

以下操作检查人员的家庭地址是否存在。

```sql
{%= isNotNull(person.homeAddress) %}
```
