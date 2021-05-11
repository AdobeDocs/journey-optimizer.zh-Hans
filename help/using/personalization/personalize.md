---
title: 在Journey Optimizer中个性化内容
description: 个性化入门
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 5%

---

# 入门指南 {#add-personalization}

![](../assets/do-not-localize/badge.png)

在Journey Optimizer的语境中，个性化是指利用您拥有的关于他的数据和信息，将消息定向到特定订阅者的操作。 这可以是他的名字、兴趣、居住地等。

Journey Optimizer使用基于Handlebars的&#x200B;**inline**&#x200B;简单个性化语法，它允许您创建包含多次大括号&#x200B;**{{}}**&#x200B;所包含内容的表达式。 您可以在同一内容或字段中添加多个表达式，而不受限制。 请参阅[个性化语法](personalization-syntax.md)。

个性化基于由Adobe Experience Platform中定义的&#x200B;**XDM个人用户档案**&#x200B;模式管理的用户档案数据。 有关详细信息，请参阅[Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans)。

>[!CAUTION]
>**XDM个人用户档案**&#x200B;模式是唯一可用于在Journey Optimizer中个性化内容的应用程序。

**示例：**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

在&#x200B;**消息处理**（电子邮件和推送）期间，表达式将替换为Experience Cloud平台数据库中包含的数据。

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
