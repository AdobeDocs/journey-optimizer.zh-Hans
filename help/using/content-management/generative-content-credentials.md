---
solution: Journey Optimizer
product: journey optimizer
title: Content Credentials在人工智能助理
description: 了解Adobe Journey Optimizer如何自动将Content Credentials应用于使用AI助手生成或编辑的图像，以及这对于您的内容意味着什么。
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
hide: true
source-git-commit: 556502a5c45ad920827785a9950bc5f7bbc4ca8f
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# Content Credentials在人工智能助理 {#generative-content-credentials}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解哪些AI Assistant操作附加了Content Credentials，这对于合并了多个创作AI源的图像意味着什么，以及当内容在应用程序之间移动时将会发生什么。

>[!ENDSHADEBOX]

>[!INFO]
>
>围绕创新型人工智能透明度的新法律正在出现，Adobe正在努力满足跨司法辖区的适用要求。 Content Credentials是Adobe用于满足这些法律要求的来源工具。

Content Credentials是持久的不可见元数据，记录一段内容的创建或编辑方式。 当您在Adobe Journey Optimizer中使用AI助手通过创作AI工具生成或编辑图像时，Content Credentials会自动附加到该图像，而您无需执行任何操作。

## 附加Content Credentials的操作 {#cc-workflows}

下表总结了根据在AI Assistant中执行的图像操作附加Content Credentials的时间。

| 操作 | 描述 | Content Credentials有联系吗？ | 用例示例 |
| --- | --- | --- | --- |
| **生成图像** | 从文本提示、参考图像创建新图像，或生成类似图像 | 一直。 图像是创新型人工智能生成的，因此总是带有新鲜的Content Credential。 | 从描述所需视觉效果的文本提示生成电子邮件促销活动的横幅图像。 |
| **裁切图像**（居中裁切或智能裁切） | 根据请求的尺寸调整图像 | 仅当源图像已具有Content Credential时。 裁切会重新创建图像的像素，这些像素通常会擦除该Content Credential，因此AI Assistant在裁切之前会从源图像读取该像素，然后重新构建该像素，并将其重新附加到裁切的结果。 裁剪本身不会添加新的创作AI操作，而是保留现有操作。 | 生成的横幅图像会被裁剪以适合网页：Content Credential会通过裁剪保留。</br> 用作推送通知背景的上传库存照片会被裁剪以适合屏幕：由于库存照片不执行创作AI操作，因此不会创建任何Content Credential。 |
| **添加文本叠加** | 在背景图像上渲染生成的文本 | 仅当背景图像已具有Content Credential时。 渲染叠加时，将从背景加上文本生成新图像，文本通常会擦除该Content Credential，因此AI Assistant会预先从背景图像读取叠加图，然后重新构建叠加图并将其重新附加到结果。 叠加步骤不会添加新的创作AI操作。 | 促销标题在登陆页生成的背景图像上呈现为文本叠加：保留背景图像中的Content Credential。 |
| **覆盖图像** | 将两个或多个图像组合在一起 | 如果任何源图像具有Content Credential，则合并的图像将承载所有这些源图像，并合并到单个Content Credential中。 合成操作会从源中生成一个新图像，该图像通常可以擦除这些Content Credentials，因此AI助手在合成之前读取每个源图像，然后构建一个组合Content Credential，其中列出每个有助于生成式AI操作的源。 | 生成的产品图像与为电子邮件标题生成的背景合成：结果携带反映两个生成AI源的Content Credential。<br> 将两张上传的品牌照片合成一个拼贴：由于两个来源都不执行创作AI操作，因此不会创建任何Content Credential。 |

## 内容类型及其范围 {#cc-content-types}

* **图像**：已覆盖。 当使用创作AI生成图像时，会附加Content Credentials，并通过由AI助手执行的裁切、文本叠加和图像叠加操作来保留。
* **文本**：不适用。 AI Assistant的纯文本输出（如副本生成、翻译和品牌对齐建议）不需要Content Credentials。

## 内容移动时发生的情况 {#cc-content-moves}

Content Credentials将随图像文件一起运行。 从Adobe Journey Optimizer下载或导出使用创作AI生成或编辑的图像时，将保留其Content Credentials。 [进一步了解Content Credentials](https://helpx.adobe.com/cn/firefly/using/content-credentials.html){target="_blank"}。

将图像引入内容的某些方法(例如从PDF或从嵌入(base64)源中提取图像)可能无法保留原始Content Credential。 在这些情况下，无法从源中读取任何Content Credential，并且不会为结果创建任何内容。

## 其他资源

* [Adobe Content Credentials](https://helpx.adobe.com/cn/firefly/using/content-credentials.html){target="_blank"}：了解有关Content Credentials如何跨Adobe产品工作的更多信息。
* [Adobe Experience Cloud创作AI用户准则](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [护栏和限制](gs-generative.md#generative-guardrails)
