---
title: 在 Journey Optimizer 中个性化内容
description: 个性化入门。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 25%

---

# 个性化入门{#add-personalization}

Discover [!DNL Adobe Journey Optimizer] 个性化功能，通过利用您拥有的有关邮件的数据和信息，使邮件适应每个特定收件人。 这可以是他们的名字、兴趣、住处、购买的东西等。

➡️ [了解如何在这些视频中个性化消息](#video-perso)
➡️ [了解利用个性化的用例](personalization-use-case.md)

## 使用专用语法构建个性化表达式 {#syntax}

[!DNL Journey Optimizer] 使用 **内嵌** 基于Handlebars的简单个性化语法，允许您创建内容由双大括号括起的表达式 **{{}}**. 您可以在同一内容或字段中添加多个表达式，而不受限制。在 [个性化语法](personalization-syntax.md).

**示例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

处理消息（电子邮件和推送）时，Journey Optimizer会将表达式替换为Experience Platform数据库中包含的数据：  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` 变成了“你好，无名氏”。

## 利用用户档案数据个性化您的消息 {#data}

个性化基于 Adobe Experience Platform 中定义的 **XDM Individual Profile** 架构管理的用户档案数据。在 [Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target=&quot;_blank&quot;}。

>[!CAUTION]
>的 **XDM个人配置文件** 架构是您唯一可以在 [!DNL Journey Optimizer].

## 在不同上下文中添加个性化 {#contexts}

[!DNL Journey Optimizer] 允许您以多种不同方式个性化内容和消息显示。 进一步了解在中可执行个性化的上下文 [此部分](personalization-contexts.md).

## 使用表达式编辑器 {#editor}

[!DNL Journey Optimizer] 提供了表达式编辑器，您可以在其中选择、排列、自定义和验证所有数据，以为内容创建自定义个性化。

有几种工具可帮助构建个性化内容（帮助程序函数、预定义表达式库、收藏集属性……）

详细了解 [!DNL Journey Optimizer] 表达式编辑器 [此部分](personalization-build-expressions.md)

## 操作说明视频{#video-perso}

了解如何使用历程中的情境式事件信息来对消息进行个性化。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

了解如何使用历程中的情境式事件信息来对消息进行个性化。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
