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
source-git-commit: 267d1850cbe30b1078f3b5b5bd228364bb63edd6
workflow-type: ht
source-wordcount: '602'
ht-degree: 100%

---

# AI 助手入门 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="AI 助手"
>abstract="完成投放的定制和个性化后，您可以使用 AI 助手增强内容。借助此功能，您可以描述要生成的内容来进行微调，从而简化个性化和内容改进的过程。"


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="使用 AI 助手定义上下文"
>abstract="要将所选内容用作内容生成的输入，请打开&#x200B;**使用原始内容**&#x200B;开关。您还可以上传品牌资源，以将其用作源。如果不使用选定内容，则必须上传和选择品牌资源。"


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe 生成式 AI 术语"
>abstract="是否能访问此功能取决于您是否同意遵守 Adobe Experience Cloud 生成式 AI 用户指南。请检查此功能产生的任何输出是否准确，并确保它适合您的用例。"
>additional-url="https://www.adobe.com/cn/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Adobe 生成式 AI 用户指南"

>[!BEGINSHADEBOX]

**目录**

* AI 助手入门
* [使用 AI 助手生成电子邮件](generative-email.md)
* [使用 AI 助手生成短信](generative-sms.md)
* [使用 AI 助手进行推送生成](generative-push.md)
* [使用 AI 助手进行内容试验](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Adobe Journey Optimizer 中的 AI 助手目前仅作为 Beta 版供部分用户使用。

Adobe Journey Optimizer 中的 AI 助手由 Azure OpenAI 提供支持，为文本和图像提供主动的内容变体建议。这可用于电子邮件、推送和短信渠道。这项新功能可用于快速的文本和图像生成。通过 Adobe Firefly 管理图像生成。

使用 Journey Optimizer 中的 AI 助手，尝试使用不同的主标题和图像来优化消息的影响。生成多个变体并构建试验，从而进行比较。利用 Journey Optimizer 内容试验，您可以定义多种消息处理方式，以衡量哪种方式最适合您的目标受众。您可以选择更改投放内容或主题。消息受众将随机分配给每个处理方式，以确定在指定的量度下哪个处理效果最佳。在[此部分](../content-management/content-experiment.md)中详细了解内容试验。

## 护栏和限制 {#generative-guardrails}

下面列出了在 Journey Optimizer 中使用 AI 助手生成电子邮件的一般准则：

* 生成的内容的质量在很大程度上受您定义的营销目标/提示的影响。使用为 GenAI 模型明确定义的提示以准确解释。 
* 上传品牌资源以提供准确的品牌相关内容。否则，内容基于公开可用的信息。上传的内容可以是以下格式：PDF、JPEG、PNG 或 ZIP 文件（具有支持的文件格式）。
* 上传的品牌资源的最大大小为 50 MB。可以上传较大的文件或大量的图像，但处理时间会增加。
* 使用 Adobe Campaign 创作的电子邮件模板，最好是[内置电子邮件模板](../email/use-email-templates.md)，用于创建电子邮件内容的特定于品牌的模板或自定义模板。建议使用最多包含 8 至 10 张图像的电子邮件模板。
* 选择变体时，请确保使用拇指竖起、拇指朝下或标记图标报告任何有问题的输出。
* 您对 AI 助手的使用受 Adobe Experience Cloud 生成式 AI 用户指南的约束。[了解详情](https://www.adobe.com/cn/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

以下限制适用于 Journey Optimizer 中的 AI 助手：

* 支持的语言只有英语。
* 仅适用于电子邮件、推送和短信渠道。
* GenAI 内容可能并不总是准确的：请分享您的反馈，以便我们的工程师可以优化模型。
* 您可以上传多个品牌资源，但对于每个具体的生成操作仅可使用一个资源。

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
