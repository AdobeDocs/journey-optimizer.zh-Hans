---
title: 导入或编码电子邮件
description: 了解如何导入电子邮件内容或对电子邮件进行编码
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 52011299-0c65-49c3-9edd-ba7bed5d7205
source-git-commit: b43e3432ede1d4985e0a6b57b57c5efc3cf60c50
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 9%

---

# 导入或编码电子邮件内容 {#existing-content}

Journey Optimizer允许您导入现有HTML内容以设计电子邮件。 此内容可以是原始HTML代码，也可以是现有HTML文件或zip文件夹中的内容。

要对HTML内容进行编码或导入现有内容，请执行以下步骤：

1. [创建消息](create-message.md)

1. 打开 **[!UICONTROL Email Designer]** 从 **[!UICONTROL Edit Content]** 中。

   ![](assets/import-html_1.png)

1. 选择 **[!UICONTROL Code your own]** 或 **[!UICONTROL Import HTML]**。有关后续步骤，请参阅以下各节。

## 编码您自己的 {#import-raw-html-code}

使用 **[!UICONTROL Code your own]** 模式导入原始HTML和/或编码电子邮件内容。 此方法需要HTML技能。

>[!CAUTION]
>
> 图像来源 [Adobe Experience Manager Assets Essentials](assets-essentials.md) 使用此方法时无法引用。 您的HTML代码中引用的图像必须存储到公共位置。

1. 在Email Designer主页中，选择 **[!UICONTROL Code your own]**.

   ![](assets/code-your-own.png)

1. 输入或粘贴原始HTML代码。

1. 使用左窗格可利用 [!DNL Journey Optimizer] 个性化功能。 如需详细信息，请参阅[此部分](../personalization/personalize.md)。

   ![](assets/code-editor.png)

1. 如果要打开Email Designer以从新设计开始发送电子邮件，请选择 **[!UICONTROL Change your design]** 中。

   ![](assets/code-editor-change-design.png)

1. 单击 **[!UICONTROL Preview]** 按钮以使用测试用户档案检查消息设计和个性化。 如需详细信息，请参阅[此部分](preview.md)。

   ![](assets/code-editor-preview.png)

1. 代码准备就绪后，单击 **[!UICONTROL Save]** 然后返回消息创建屏幕以完成消息。

   ![](assets/code-editor-save.png)

## 导入HTML {#import-html-content-from-file}

您可以在电子邮件设计器中导入HTML内容。 此内容可以是：

* 安 **HTML文件** 带有合并样式表，
* A **.zip文件夹** 使用HTML文件、样式表(.css)和图像。

   >[!NOTE]
   >
   >.zip文件结构没有限制。 但是，引用必须是相对的，并且与.zip文件夹的树结构相匹配。

要导入包含HTML内容的文件，请执行以下步骤：

1. 在Email Designer主页中，选择 **[!UICONTROL Import HTML]**.

   ![](assets/import-html_2.png)

1. 拖放包含您的HTML内容的HTML或.zip文件。

1. 上传HTML内容后，您可以利用Email Designer功能编辑和预览电子邮件。 [在本节中了解详情](create-email-content.md)。

   ![](assets/html-imported.png)
