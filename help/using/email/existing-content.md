---
solution: Journey Optimizer
product: journey optimizer
title: 导入电子邮件内容
description: 了解如何导入电子邮件内容
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 电子邮件，导入，内容， html， zip， css
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 33%

---

# 导入电子邮件内容 {#existing-content}

[!DNL Journey Optimizer] 用于导入现有HTML内容以设计电子邮件。 相关的内容可以是：

* An **HTML文件** 合并样式表；
* A **.zip文件夹** 包括HTML文件、样式表(.css)和图像。

  >[!NOTE]
  >
  >具体的 .zip 文件结构没有任何限制。但是，引用必须是相对的，并且适合.zip文件夹的树结构。

要导入包含 HTML 内容的文件，请执行以下步骤：

1. 从Email Designer主页中，选择 **[!UICONTROL 导入HTML]**.

   ![](assets/import-html_2.png)

1. 拖放包含 HTML 内容的 HTML 或 .zip 文件，然后单击&#x200B;**[!UICONTROL 导入]**。

   ![](assets/html-imported_2.png)

1. 上传HTML内容后，您的内容将位于 **[!UICONTROL 兼容模式]**.

   在此模式下，您只能对文本进行个性化，向内容添加链接或包含资源。

1. 为了能够利用Email Designer内容组件，请访问 **[!UICONTROL HTML转换器]** 选项卡，然后单击 **[!UICONTROL 转换]**.

   ![](assets/html-imported.png)

   >[!NOTE]
   >
   > 使用 `<table>` 将标签作为HTML文件中的第一层可能会导致样式丢失，包括顶层标签中的背景和宽度设置。

1. 现在，您可以根据需要使用Email Designer功能个性化导入的文件 [了解详情](content-from-scratch.md).

## 操作方法视频 {#video}

了解如何导入现有 HTML 内容、调整设计、添加镜像页面和取消订阅链接，以及如何对内容进行编码。

>[!VIDEO](https://video.tv.adobe.com/v/334102?quality=12)
