---
title: 在Journey Optimizer中个性化内容
description: 个性化入门
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 3%

---

# 个性化入门{#add-personalization}

![](../assets/do-not-localize/badge.png)

探索历程优化个性化功能，通过利用您拥有的关于他/她的数据和信息，将消息调整为适合每个特定收件人的。 这可以是他的名字、兴趣、居住地、购买的东西等。

Journey Optimizer使用&#x200B;**inline**&#x200B;基于Handlebars的简单个性化语法，该语法允许您创建包含双大括号&#x200B;**{}}**&#x200B;的内容的表达式。 您可以在同一内容或字段中添加多个表达式，且不受限制。 请参阅[个性化语法](personalization-syntax.md)，以了解更多信息。

个性化基于由Adobe Experience Platform中定义的&#x200B;**XDM个人配置文件**&#x200B;架构管理的配置文件数据。 有关更多信息，请参阅[Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans)。

>[!CAUTION]
>**XDM个人配置文件**&#x200B;架构是您唯一可用于在Journey Optimizer中个性化内容的架构。

**示例：**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

处理消息（电子邮件和推送）时，Journey Optimizer会将表达式替换为Experience Cloud平台数据库中包含的数据。

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
