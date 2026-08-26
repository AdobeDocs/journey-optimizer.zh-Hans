---
solution: Journey Optimizer
product: journey optimizer
title: AI助手中的C2PA元数据
description: 了解Adobe Journey Optimizer如何自动将C2PA元数据应用于使用AI Assistant生成或编辑的图像，以及这对于您的内容意味着什么。
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
source-git-commit: cf5370872104972b3e49d544b09ab48858484da6
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 3%

---

# AI助手中的C2PA元数据 {#generative-content-credentials}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解哪些AI Assistant操作附加了C2PA元数据、这对于合并了多个创作AI源的图像意味着什么，以及当内容在应用程序之间移动时将会发生什么情况。

>[!ENDSHADEBOX]

>[!INFO]
>
>围绕创新型人工智能透明度的新法律正在出现，Adobe正在努力满足跨司法辖区的适用要求。 C2PA元数据是Adobe用于满足这些法规要求的源工具。

C2PA元数据是持久的、不可见的元数据，记录一段内容的创建或编辑方式。 当您在Adobe Journey Optimizer中使用AI助手通过创作AI工具生成或编辑图像时，C2PA元数据会自动附加到该图像，您无需执行任何操作。

## 附加C2PA元数据的操作 {#cc-workflows}

下表总结了根据AI Assistant中执行的图像操作附加C2PA元数据的时间。

| 操作 | 描述 | 是否附加C2PA元数据？ | 用例示例 |
| --- | --- | --- | --- |
| **生成图像** | 从文本提示、参考图像创建新图像，或生成类似图像 | 一直。 图像是由创成式人工智能生成的，因此它总是带有新的C2PA元数据。 | 从描述所需视觉效果的文本提示生成电子邮件促销活动的横幅图像。 |
| **裁切图像**（居中裁切或智能裁切） | 根据请求的尺寸调整图像 | 仅当源图像已具有C2PA元数据时。 裁剪会重新创建图像的像素，这些像素通常会擦除该C2PA元数据，因此AI Assistant在裁剪之前会从源图像读取这些像素，然后重新构建这些像素，并将其重新附加到裁剪的结果。 裁剪本身不会添加新的创作AI操作，而是保留现有操作。 | 生成的横幅图像会被裁剪以适合网页：通过裁剪保留C2PA元数据。</br> 用作推送通知背景的上传库存照片会被裁剪以适合屏幕：由于库存照片不执行创作AI操作，因此不会创建C2PA元数据。 |
| **添加文本叠加** | 在背景图像上渲染生成的文本 | 仅当背景图像已具有C2PA元数据时。 渲染叠加时，将从背景加上文本生成新图像，这通常会擦除该C2PA元数据，因此AI Assistant会预先从背景图像读取该元数据，然后重新构建该元数据并将其重新附加到结果。 叠加步骤不会添加新的创作AI操作。 | 促销标题被呈现为在登陆页生成的背景图像上的文本叠加：来自背景图像的C2PA元数据被保留。 |
| **覆盖图像** | 将两个或多个图像组合在一起 | 如果任何源图像具有C2PA元数据，则组合图像携带所有源图像，并合并到单个C2PA元数据中。 合成从源中生成一个新图像，通常会擦除这些C2PA元数据，因此AI Assistant在合成之前读取每个C2PA元数据，然后构建一个合并的C2PA元数据，其中列出每个有助于创作AI操作的源。 | 生成的产品图像与为电子邮件标题生成的背景合成：结果携带反映两个生成AI源的C2PA元数据。<br> 将两张上传的品牌照片合成一个拼贴：由于两个来源都不执行创作AI操作，因此不会创建C2PA元数据。 |

## 内容类型及其范围 {#cc-content-types}

* **图像**：已覆盖。 当使用创作AI生成图像时，附加C2PA元数据，并通过AI助手执行的裁剪、文本叠加和图像叠加操作来保留C2PA元数据。
* **文本**：不适用。 AI Assistant的纯文本输出（如副本生成、翻译和品牌对齐建议）不需要C2PA元数据。

## 内容移动时发生的情况 {#cc-content-moves}

C2PA元数据随图像文件一起传输。 从Adobe Journey Optimizer下载或导出使用创作AI生成或编辑的图像时，将保留其C2PA元数据。 [了解有关C2PA元数据的更多信息](https://helpx.adobe.com/cn/firefly/using/content-credentials.html){target="_blank"}。

将图像引入内容的某些方法(例如从PDF或从嵌入(base64)源中提取图像)可能不会保留原始C2PA元数据。 在这些情况下，无法从源中读取C2PA元数据，并且不会为结果创建任何元数据。

## 其他资源

* [Adobe Experience Cloud创作AI用户准则](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}
* [护栏和限制](gs-generative.md#generative-guardrails)
* [创作AI内容透明度](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency#related-links)