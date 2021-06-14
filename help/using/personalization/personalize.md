---
title: 在 Journey Optimizer 中个性化内容
description: 个性化入门
feature: 个性化
topic: 个性化
role: Data Engineer
level: Beginner
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 50%

---

# 个性化入门{#add-personalization}

![](../assets/do-not-localize/badge.png)

探索历程优化个性化功能，通过利用您拥有的关于他/她的数据和信息，将消息调整为适合每个特定收件人的。 这可以是他的名字、兴趣、居住地、购买的东西等。

Journey Optimizer 使用基于 Handlebars 的 **inline** 简单个性化语法，允许您创建内容由双重大括号 **{{}}** 括起来的表达式。您可以在同一内容或字段中添加多个表达式，而不受限制。请参阅[个性化语法](personalization-syntax.md)，以了解更多信息。

个性化基于 Adobe Experience Platform 中定义的 **XDM Individual Profile** 架构管理的用户档案数据。有关详细信息，请参阅 [Adobe Experience Platform Data Model (XDM) 文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans)。

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
