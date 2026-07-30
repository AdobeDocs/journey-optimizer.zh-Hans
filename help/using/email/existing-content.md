---
solution: Journey Optimizer
product: journey optimizer
title: 导入电子邮件内容
description: 了解如何导入电子邮件内容
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: 电子邮件，导入，内容， html， zip， css
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
TQID: https://experienceleague.adobe.com/R0Csd9gbvY-iyW81G-clHoXozEBYWBfjb0y9PWq4zZA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 27%

---

# 导入电子邮件内容 {#existing-content}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何以HTML文件或.zip文件夹的形式导入现有HTML内容，以及如何转换现有内容，以便使用Email Designer对其进行编辑和个性化。

>[!ENDSHADEBOX]

[!DNL Journey Optimizer]允许您导入现有HTML内容以设计电子邮件。 相关的内容可以是：

* 包含合并样式表的&#x200B;**HTML文件**；
* **.zip文件夹**，包括HTML文件、样式表(.css)和图像。

  >[!NOTE]
  >
  >具体的 .zip 文件结构没有任何限制。 但是，引用必须是相对的，并且适合.zip文件夹的树结构。


>[!TIP]
>
>如果您有图像设计（JPEG或PNG）而不是HTML文件，则可以使用[图像到HTML转换器](../content-management/image-to-html.md)，通过AI自动将它们转换为可编辑的HTML电子邮件模板。

要导入包含 HTML 内容的文件，请执行以下步骤：

1. 从电子邮件Designer主页中，选择&#x200B;**[!UICONTROL 导入HTML]**。

   ![](assets/import-html_2.png)

1. 拖放包含 HTML 内容的 HTML 或 .zip 文件，然后单击&#x200B;**[!UICONTROL 导入]**。

   ![](assets/html-imported_2.png)

1. 上传HTML内容后，您的内容将处于&#x200B;**[!UICONTROL 兼容模式]**。

   在此模式下，您只能对文本进行个性化，向内容添加链接或包含资源。

1. 若要利用Email Designer内容组件，请访问&#x200B;**[!UICONTROL HTML converter]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 转换]**。

   ![](assets/html-imported.png)

   >[!NOTE]
   >
   > 在HTML文件中使用`<table>`标记作为第一层可能会导致样式丢失，包括顶层标记中的背景和宽度设置。

1. 您现在可以根据需要使用Email Designer功能个性化导入的文件。 [了解详情](content-from-scratch.md)

## 操作方法视频 {#video}

了解如何导入现有 HTML 内容、调整设计、添加镜像页面和取消订阅链接，以及如何对内容进行编码。

>[!VIDEO](https://video.tv.adobe.com/v/3421908?captions=chi_hans&quality=12)
