---
solution: Journey Optimizer
product: journey optimizer
title: 自动生成内容变体(Beta)
description: 了解如何使用基于人工智能的模拟自动生成内容变体。
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="私人测试版" type="Informative"
hidefromtoc: true
hide: true
source-git-commit: 9155a16a0557a32c1d59b66b03fc84c5bc7b8463
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---


# 自动生成内容变体(Beta){#auto-generate-variants}

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私有测试版**&#x200B;中，可能在您的环境中不可用。 请联系 Adobe 代表以获取访问权限。

[!DNL Journey Optimizer]引入了基于人工智能的模拟，可自动生成多个变体以测试您的内容。 此功能可减少手动创建变体的需要，从而更轻松地在复杂模板中验证个性化逻辑。

在呈现内容以进行模拟或验证时，系统会分析您的内容并标识所有个性化令牌和分支规则。 它用有意义的值替换个性化令牌，提供近乎逼真的最终内容预览。

考虑具有基于&#x200B;**投资者类型**、**年龄组**、**婚姻状况**、**税务ID验证**&#x200B;和&#x200B;**地点**&#x200B;的分支逻辑的金融服务电子邮件模板。

如果不生成变体，您需要手动创建数十个变体以验证所有路径。 使用自动生成的变体，系统会生成自动覆盖这些条件的代表性变体。  每个生成的变体都会在预览窗格中渲染，准确地显示应用了哪些块和条件。

>[!NOTE]
>
>此功能的工作方式与标准模拟内容变体功能相同。 有关内容变体模拟以及关联的护栏和限制的更多信息，请参阅此章节： [模拟内容变体](../test-approve/simulate-sample-input.md)

## 生成内容变体

要为内容生成变体并预览它们，请执行以下步骤：

1. 打开您的内容并选择&#x200B;**[!UICONTROL 模拟内容]** / **[!UICONTROL 模拟内容变体]**。

   ![](assets/simulate-sample.png)

2. 单击&#x200B;**[!UICONTROL 生成]**&#x200B;按钮。

   ![](assets/simulate-generate-variant.png)

3. [!DNL Journey Optimizer]根据检测到的属性自动生成变体。

4. 在左窗格中查看生成的变体列表，然后选择变体以在预览窗格中查看其个性化呈现。
