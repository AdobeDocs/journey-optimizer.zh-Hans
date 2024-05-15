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
source-git-commit: 644e0959ee0d0ec8ee0c4ec54c3bcd1cc3c4dda9
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 54%

---

# AI 助手入门 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="AI 助手"
>abstract="在精心设计并个性化设置投放后，您可使用 AI 助手来增强您的内容。此功能使您通过描述要生成的东西即可微调内容，从而简化个性化和改善内容的过程。"


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="使用AI助手定义上下文"
>abstract="要将所选内容用作内容生成的输入，请激活 **使用原始内容** 切换。 还可上传品牌资源以将其用作来源。如果不使用所选内容，则必须上传并选择品牌资源。"


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe 生成式 AI 条款"
>abstract="您必须同意 Adobe Experience Cloud 生成式 AI 用户准则才能使用此功能。您向此功能提供的任何提示、上下文或补充信息或其他输入都必须与特定的上下文关联，这些特定的上下文可包括您的品牌宣传材料、网站内容、数据、此类数据的架构、模板或其他可信文档，并且不得包含任何个人信息（个人信息包括任何可追溯回具体个人的信息）。您应检查此功能产生的任何输出是否准确，并确保它适合您的用例"
>additional-url="https://www.adobe.com/cn/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Adobe 生成式 AI 用户准则"

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
