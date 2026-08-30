---
solution: Journey Optimizer
product: journey optimizer
title: 电子邮件和登陆页Designer中的C2PA元数据
description: 了解已附加到图像的C2PA元数据在Adobe Journey Optimizer中的电子邮件和登陆页设计器中移动时会发生什么情况。
feature: Content Management
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
source-git-commit: 47e95cbc3716e650492e9cda4a4fddbe61f56ffd
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---


# 电子邮件和登陆页Designer中的C2PA元数据 {#c2pa-email-landing-page-designer}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解已附加到图像的C2PA元数据在Adobe Journey Optimizer中的电子邮件和登陆页设计器中移动时发生了什么情况。

>[!ENDSHADEBOX]

>[!INFO]
>
>围绕创新型人工智能透明度的新法律正在出现，Adobe正在努力满足跨司法辖区的适用要求。 C2PA元数据是Adobe用于满足这些法规要求的源工具。

电子邮件和登陆页设计器本身不会生成或编辑图像。 它引用了在其他Adobe工具（如生成内容、Adobe Express或Firefly）或合作伙伴模型中已使用创作AI生成或编辑的图像。 构建、发布和发送时，已附加到这些图像的C2PA元数据将保留不变。

## 在生成和发送时，将保留C2PA元数据 {#c2pa-preserved}

下表总结了使用电子邮件和登陆页设计器构建和发送内容的每个步骤对C2PA元数据的影响。

| 操作 | 发生什么情况 | 是否保留C2PA元数据？ | 示例 |
| --- | --- | --- | --- |
| **将图像插入模板** | 设计器会为已在其他位置使用创作AI生成或编辑的图像添加引用，例如生成内容、Adobe Express、Firefly或合作伙伴模型。 不会更改图像文件本身。 | 是，未更改 | Firefly生成的横幅将插入到电子邮件模板中。 |
| **调整大小、重新定位或添加替换文本** | 仅显示模板的HTML更改中的属性。 图像文件未重新编码。 | 是，未更改 | 调整图像大小以适合移动布局和给定的替换文本。 |
| **发布** | 发布电子邮件或登陆页面，并存储图像以进行交付。 | 是，未更改 | 发布营销活动，并存储其图像以供发送。 |
| **发送电子邮件或查看登陆页面** | 图像会传送到收件人的收件箱或显示在实时页面上。 | 是，未更改 | 收件人打开电子邮件并下载图像；凭据仍与原始凭据匹配。 |

## 内容类型及其范围 {#c2pa-content-types}

* **图像**：已覆盖。 如上所示，已附加到图像的C2PA元数据在插入、调整、发布和交付时会保留。
* **视频、音频、文本**：不适用。 电子邮件和登陆页设计器不会使用创作AI生成或编辑这些内容类型。

## 内容移动时发生的情况 {#c2pa-content-moves}

C2PA元数据在Adobe Journey Optimizer中的电子邮件和登陆页设计器中随图像一起移动，从您的编辑器到存储区，再到收件人的收件箱或实时页面。 在以上任何步骤中，都不会创建、更改或删除任何凭据。

如果图像不带有创作AI C2PA元数据，则由于它不是使用创作AI生成或编辑的，因此此处不会显示凭据。 这是正常情况，而不是错误。

## 检查凭据 {#c2pa-checking-credential}

尚无法直接在电子邮件或登陆页面设计器中检查Content Credential。

## 其他资源

* [生成内容中的C2PA元数据](generative-c2pa-metadata.md)
* [创作AI内容透明度](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency)
