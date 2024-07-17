---
solution: Journey Optimizer
product: journey optimizer
title: 在 Journey Optimizer 中个性化内容
description: 个性化入门。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: 表达式、编辑器、开始、个性化
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 35%

---

# 个性化入门{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="个性化体验"
>abstract="借助 **Adobe Journey Optimizer**，可利用您拥有的特定收件人相关数据和信息，让您的消息适合每个特定收件人。该信息可以是特定收件人的名字、兴趣、居住地、购买的物品等。"

发现[!DNL Adobe Journey Optimizer]个性化功能，利用您拥有的关于每个特定收件人的数据和信息根据他们调整您的邮件。 该信息可以是特定收件人的名字、兴趣、居住地、购买的物品等。

➡️[了解如何在这些视频中个性化邮件](#video-perso)
➡️[探索利用个性化的用例](personalization-use-case.md)

## 使用专用语法构建个性化表达式 {#syntax}

[!DNL Journey Optimizer]使用基于Handlebars的&#x200B;**inline**&#x200B;简单个性化语法，该语法允许您创建内容由双大括号&#x200B;**{{}}**&#x200B;括起来的表达式。 您可以在同一内容或字段中添加多个表达式，而不受限制。[了解有关个性化语法的更多信息](personalization-syntax.md)。

**示例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

在处理消息（电子邮件和推送）时，Journey Optimizer将表达式替换为Experience Platform数据库中包含的数据： `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`变为“Hello John Doe”。

## 利用用户档案数据将消息个性化 {#data}

个性化基于 Adobe Experience Platform 中定义的 **XDM Individual Profile** 架构管理的用户档案数据。请参阅[Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}以了解详情。

>[!CAUTION]
>**XDM Individual Profile**&#x200B;架构是唯一可用于个性化[!DNL Journey Optimizer]中内容的架构。

此外，您还可以利用&#x200B;**计算属性**&#x200B;来个性化您的内容。 计算属性基于摄取到Adobe Experience Platform中的启用配置文件的体验事件数据集，并作为客户配置文件中存储的汇总数据点，汇总各个行为事件[了解如何使用计算属性](../audience/computed-attributes.md)

## 使用个性化编辑器 {#editor}

[!DNL Journey Optimizer]提供了一个个性化编辑器，您可以在其中选择、排列、自定义和验证所有数据，以便为您的内容创建自定义个性化。 有多种工具可帮助您构建个性化内容，例如：Felper函数、预定义表达式库、受欢迎的属性等。

* [了解如何使用个性化编辑器](personalization-build-expressions.md)
* [了解可在何处执行个性化](personalization-contexts.md)。

## 操作说明视频{#video-perso}

了解如何使用历程中的情境式事件信息来对消息进行个性化。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

了解如何在消息中添加基于用户档案的个性化推送，以及如何将受众会员资格用作个性化块的先决条件。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

