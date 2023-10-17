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
source-git-commit: 5ac3797db8115180094cc97f06ec330839a7a5ff
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 35%

---

# 个性化入门{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="个性化体验"
>abstract="借助 **Adobe Journey Optimizer**，可利用您拥有的特定收件人相关数据和信息，让您的消息适合每个特定收件人。该信息可以是特定收件人的名字、兴趣、居住地、购买的物品等。"


发现 [!DNL Adobe Journey Optimizer] 个性化功能，利用您拥有的关于每个特定收件人的数据和信息，根据他们调整您的消息。 该信息可以是特定收件人的名字、兴趣、居住地、购买的物品等。

➡️ [在这些视频中了解如何个性化消息](#video-perso)
➡️ [探索利用个性化的用例](personalization-use-case.md)

## 使用专用语法构建个性化表达式 {#syntax}

[!DNL Journey Optimizer] 使用 **内嵌** 基于Handlebars的简单个性化语法，允许您创建内容由双大括号括起来的表达式 **{{}}**. 您可以在同一内容或字段中添加多个表达式，而不受限制。了解详情，请参阅 [个性化语法](personalization-syntax.md).

**示例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

在处理消息（电子邮件和推送）时，Journey Optimizer会使用Experience Platform数据库中包含的数据替换表达式：  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` 会变成“Hello John Doe”。

## 利用用户档案数据将消息个性化 {#data}

个性化基于 Adobe Experience Platform 中定义的 **XDM Individual Profile** 架构管理的用户档案数据。了解详情，请参阅 [Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}.

>[!CAUTION]
>此 **XDM个人资料** 架构是唯一可用于在中个性化内容的架构 [!DNL Journey Optimizer].

此外，您还可以利用 **计算属性** 使您的内容个性化。 计算属性基于提取到Adobe Experience Platform中的支持配置文件的体验事件数据集，并充当存储在客户配置文件中总结各个行为事件的汇总数据点 [了解如何使用计算属性](../audience/computed-attributes.md)

## 在不同上下文中添加个性化 {#contexts}

[!DNL Journey Optimizer] 允许您以几种不同的方式将消息的内容和显示个性化。 详细了解可在其中执行个性化的上下文 [本节](personalization-contexts.md).

## 使用表达式编辑器 {#editor}

[!DNL Journey Optimizer] 提供了一个表达式编辑器，您可以在其中选择、排列、自定义和验证所有数据，以便为您的内容创建自定义的个性化设置。

提供了多种工具来帮助构建个性化内容（辅助函数、预定义表达式库、受欢迎的属性……）

了解有关 [!DNL Journey Optimizer] 中的表达式编辑器 [本节](personalization-build-expressions.md)

## 操作说明视频{#video-perso}

了解如何使用历程中的情境式事件信息来对消息进行个性化。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

了解如何在消息中添加基于用户档案的个性化推送，以及如何将受众会员资格用作个性化块的先决条件。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

