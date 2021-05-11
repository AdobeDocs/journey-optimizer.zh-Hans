---
title: 函数库
description: 函数库
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# 对象函数{#objects}

![](../../assets/do-not-localize/badge.png)

## 为null

`isNull`函数确定对象引用是否不存在。

**格式**

```sql
isNull({OBJECT})
```

**示例**

以下PQL查询会检查人员的住宅地址是否不存在。

```sql
isNull(person.homeAddress)
```

## 不为null

`isNotNull`函数确定是否存在对象引用。

**格式**

```sql
isNotNull({OBJECT})
```

**示例**

以下PQL查询将检查人员的住宅地址是否存在。

```sql
isNotNull(person.homeAddress)
```
