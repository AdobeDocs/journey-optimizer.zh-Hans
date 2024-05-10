---
solution: Journey Optimizer
product: journey optimizer
title: AI 助手入门
description: 了解如何访问和使用 Journey Optimizer 的 AI 助手
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta 版" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: b62f8954e09f50896ad5e70784c5a93943617e85
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 43%

---

# AI 助手入门 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_content_generation"
>title="创建电子邮件内容"
>abstract="Adobe Journey Optimizer 中的 AI 助手可以主动为文本和图像提供内容变体建议。这可用于电子邮件、推送、短信和 Web 渠道。这项新功能可用于快速的文本和图像生成。"

>[!BEGINSHADEBOX]

**目录**

* AI 助手入门
* [使用 AI 助手生成电子邮件](generative-email.md)
* [使用 AI 助手生成短信](generative-sms.md)
* [使用AI助手生成推送](generative-push.md)
* [使用AI助手进行内容试验](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Adobe Journey Optimizer中的AI助手当前作为测试版仅向选定用户提供。

Adobe Journey Optimizer 中的 AI 助手可以主动为文本和图像提供内容变体建议。它可用于电子邮件、推送和短信渠道。 这项新功能可用于快速的文本和图像生成。通过 Adobe Firefly 管理图像生成。

使用 Journey Optimizer 中的 AI 助手，尝试使用不同的主标题和图像来优化消息的影响。生成多个变体并构建试验，从而进行比较。利用 Journey Optimizer 内容试验，您可以定义多种消息处理方式，以衡量哪种方式最适合您的目标受众。您可以选择更改投放内容或主题。消息受众将随机分配给每个处理方式，以确定在指定的量度下哪个处理效果最佳。在[此部分](../campaigns/content-experiment.md)中详细了解内容试验。

## 护栏和限制 {#generative-guardrails}

下面列出了在Journey Optimizer中使用AI助手生成电子邮件的一般准则：

* 生成的内容的质量在很大程度上受您定义的营销目标/提示的影响。 使用明确定义的提示以准确解释GenAI模型。 
* 上传品牌资产以对品牌内容保持准确。 否则，内容基于公开可用的信息。 上传的内容可以具有以下格式：PDF、JPEG、PNG或ZIP文件（具有支持的文件格式）。
* 上传的品牌资产的最大大小为50MB。 较大的文件或大量的图像可以工作，但处理时间会增加。
* 最好使用Adobe Campaign创作的电子邮件模板 [内置电子邮件模板](../email/use-email-templates.md)，用于创建电子邮件内容的特定于品牌的模板或自定义模板。 建议使用最多包含8至10张图像的电子邮件模板。
* 选择变体时，请确保使用向上缩略图、向下缩略图或标记图标报告任何有问题的输出。
* 您对AI助手的使用受Adobe Experience Cloud创作AI用户指南的约束。 [了解详情](https://www.adobe.com/cn/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

以下限制适用于Journey Optimizer中的AI助手：

* 支持的语言仅是英语。
* 仅适用于电子邮件、推送和短信渠道。
* GenAI内容可能并不总是准确的：请分享您的反馈，以便我们的工程师可以优化模型。
* 您可以上传多个品牌资产，但只能为特定世代利用一个。

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="电子邮件生成" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>电子邮件生成</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="短信生成" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>短信生成</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="推送生成" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>推送通知生成</strong></a>
</div>
<p></td>
</tr></table>
