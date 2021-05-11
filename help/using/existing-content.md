---
title: 导入或编写电子邮件
description: 了解如何导入电子邮件内容或为电子邮件编码
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 5%

---

# 导入或编码电子邮件内容{#existing-content}

![](assets/do-not-localize/badge.png)

Journey Optimizer允许您导入现有HTML内容以设计电子邮件。 此内容可以是原始HTML代码，也可以是现有HTML文件或zip文件夹中的内容。

要编写HTML内容代码或导入现有内容，请执行以下步骤：

1. [创建消息](create-message.md)

1. 从&#x200B;**[!UICONTROL Edit Content]**&#x200B;部分打开&#x200B;**[!UICONTROL Email Designer]**。

   ![](assets/import-html_1.png)

1. 选择 **[!UICONTROL Code your own]** 或 **[!UICONTROL Import HTML]**。有关后续步骤，请参阅以下各节。

## 编写您自己的{#import-raw-html-code}

使用&#x200B;**[!UICONTROL Code your own]**&#x200B;模式可导入原始HTML和/或编写电子邮件内容。 此方法需要HTML技能。

>[!CAUTION]
>
> 使用此方法时，无法引用来自[Adobe Experience Manager Assets Essentials](assets-essentials.md)的图像。 HTML代码中引用的图像必须存储到公共位置。

1. 在“电子邮件设计器”主页中，选择&#x200B;**[!UICONTROL Code your own]**。

   ![](assets/code-your-own.png)

1. 输入或粘贴原始HTML代码。

1. 使用左窗格可利用[!DNL Journey Optimizer]个性化功能。 如需详细信息，请参阅[此部分](personalization/personalize.md)。

   ![](assets/code-editor.png)

1. 如果要打开“电子邮件设计器”以从新设计中开始您的电子邮件，请从选项菜单中选择&#x200B;**[!UICONTROL Change your design]**。

   ![](assets/code-editor-change-design.png)

1. 单击&#x200B;**[!UICONTROL Preview]**&#x200B;按钮，使用测试用户档案检查消息设计和个性化。 如需详细信息，请参阅[此部分](preview.md)。

   ![](assets/code-editor-preview.png)

1. 代码准备就绪后，单击&#x200B;**[!UICONTROL Save]**，然后返回消息创建屏幕以完成消息。

   ![](assets/code-editor-save.png)


## 导入HTML {#import-html-content-from-file}

可以在电子邮件设计器中导入HTML内容。 此内容可以是：

* 带有合并样式表的&#x200B;**HTML文件**
* 包含HTML文件、样式表(.css)和图像的&#x200B;**.zip文件夹**。

   >[!NOTE]
   >
   >.zip文件结构没有限制。 但是，引用必须是相对的，并且与.zip文件夹的树结构相匹配。

要导入包含HTML内容的文件，请执行以下步骤：

1. 在“电子邮件设计器”主页中，选择&#x200B;**[!UICONTROL Import HTML]**。

   ![](assets/import-html_2.png)

1. 拖放包含HTML内容的HTML或.zip文件。

1. 上传HTML内容后，您可以利用电子邮件设计器功能编辑和预览您的电子邮件。 [在本节中了解更多信息](create-email-content.md)。

   ![](assets/html-imported.png)
