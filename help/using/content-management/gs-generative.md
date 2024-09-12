---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer Content Accelerator中的AI Assistant入门
description: 了解如何在Journey Optimizer Content Accelerator中访问和使用AI Assistant
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 9de2f498e104d316491e6061cbd851b2eb506036
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 42%

---

# AI Assistant内容加速器入门 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Journey Optimizer中用于内容加速的AI助手"
>abstract="完成投放的定制和个性化后，您可以使用Journey Optimizer中的AI Assistant for Content Acceleration来增强内容。 借助此功能，您可以描述要生成的内容来进行微调，从而简化个性化和内容改进的过程。"

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="上传品牌资源"
>abstract="使用上传品牌资产菜单，可添加任何品牌资产，其中包含可为Journey Optimizer中的AI助手提供用于Content Acceleration的附加上下文的内容，或选择之前上传的资产。 此选项确保 AI 助手能够获取所有必要材料，以加强其功能和相关性。"

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe 生成式 AI 术语"
>abstract="是否能访问此功能取决于您是否同意遵守 Adobe Experience Cloud 生成式 AI 用户指南。请检查此功能产生的任何输出是否准确，并确保它适合您的用例。"
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe 生成式 AI 用户指南"

>[!INFO]
>
>使用[我们的实时功能预览](https://experienceleague.adobe.com/en/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}，亲身体验亲身体验各种功能，让您亲身体验各种功能并充分了解其功能。


Adobe Journey Optimizer中的用于Content Acceleration的AI助手由Microsoft Azure OpenAI和Adobe Firefly提供支持，为文本和图像提供主动内容变体建议。 这可用于电子邮件、推送和短信渠道。这项新功能可用于快速的文本和图像生成。通过 Adobe Firefly 管理图像生成。

使用用于Content Acceleration的Adobe Journey Optimizer中的AI助手，通过尝试使用不同的主标题和图像来优化消息的影响。 生成多个变体并构建试验，从而进行比较。利用 Journey Optimizer 内容试验，您可以定义多种消息处理方式，以衡量哪种方式最适合您的目标受众。您可以选择更改投放内容或主题。消息受众将随机分配给每个处理方式，以确定在指定的量度下哪个处理效果最佳。在[此部分](../content-management/content-experiment.md)中详细了解内容试验。

>[!IMPORTANT]
>
>* 在开始使用此功能之前，请阅读相关的[护栏和限制](#generative-guardrails)。
>
>
>* 您必须同意[用户协议](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}，然后才能在Adobe Journey Optimizer中使用AI助手进行内容加速。 有关更多信息，请与您的 Adobe 代表联系。

## 访问AI Assistant内容加速器 {#generative-access}

要访问Adobe Journey Optimizer中的用于内容加速功能的AI助手，需要向用户授予&#x200B;**生成内容**&#x200B;权限。 [了解详情](../administration/permissions.md)

+++  了解如何分配与内容生成相关的权限

1. 在&#x200B;**权限**&#x200B;产品中，转到&#x200B;**角色**&#x200B;选项卡并选择所需的&#x200B;**角色**。

1. 单击&#x200B;**编辑**&#x200B;修改权限。

1. 添加&#x200B;**AI助手**&#x200B;资源，然后从下拉菜单中选择&#x200B;**生成内容**。

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. 单击&#x200B;**保存**&#x200B;以应用更改。

   已分配给此角色的任何用户都将自动更新其权限。

1. 要将此角色分配给新用户，请导航到&#x200B;**角色**&#x200B;仪表板中的&#x200B;**用户**&#x200B;选项卡，然后单击&#x200B;**添加用户**。

1. 输入用户名、电子邮件地址或从列表中选择，然后单击&#x200B;**保存**。

1. 如果之前未创建用户，请参阅[此文档](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/users)。

用户将收到一封电子邮件，其中包含访问实例的说明。

+++

## 护栏和限制 {#generative-guardrails}

下面列出了在Adobe Journey Optimizer中使用AI助手进行内容加速以生成电子邮件的一般准则：

* 生成的内容的质量在很大程度上受您定义的营销目标/提示的影响。使用为 GenAI 模型明确定义的提示以准确解释。 
* 上传品牌资源以提供准确的品牌相关内容。否则，内容基于公开可用的信息。上传的内容可以是以下格式：PDF、JPEG、PNG 或 ZIP 文件（具有支持的文件格式）。
* 上传的品牌资源的最大大小为 50 MB。可以上传较大的文件或大量的图像，但处理时间会增加。
* 使用特定于品牌或自定义的模板，在Adobe Journey Optimizer中使用AI助手创建电子邮件内容以加速Content。 建议使用最多包含8至10个图像的电子邮件模板。
* 选择变体时，请确保使用拇指竖起、拇指朝下或标记图标报告任何有问题的输出。
* 您对 AI 助手的使用受 Adobe Experience Cloud 生成式 AI 用户指南的约束。[了解详情](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* 作为Adobe承诺在媒体创建中使用创新型人工智能工具时提高透明度的一部分，Adobe将在下载或导出内容或项目包含Firefly生成的资源时应用Content credentials。 [了解详情](https://helpx.adobe.com/firefly/using/content-credentials.html)

以下限制适用于Adobe Journey Optimizer中用于Content Acceleration的AI助手：

* 支持的语言仅是英语。 非英文输入内容可能会产生不一致或错误的结果。 非英文答复引起的问题目前不予处理或改进。
* 仅适用于电子邮件、推送、Web和短信渠道。
* GenAI 内容可能并不总是准确的：请分享您的反馈，以便我们的工程师可以优化模型。
* 您可以上传多个品牌资源，但对于每个具体的生成操作仅可使用一个资源。


## AI助手内容生成功能 {#generative-features}


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
<td>
<a href="generative-web.md">
<img alt="Web生成" src="assets/do-not-localize/web-genai.jpeg">
</a>
<div><a href="generative-web.md"><strong>网页生成</strong>
</div>
<p>
</td>
</tr></table>
