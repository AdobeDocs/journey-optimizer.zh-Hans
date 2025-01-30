---
solution: Journey Optimizer
product: journey optimizer
title: 片段入门
description: 了解如何使用内容片段以在Journey Optimizer营销活动和历程中重用内容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: c30b7f4d75222db0553fbf576b90791af58cda57
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 13%

---

# 片段入门 {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="定义您自已的片段"
>abstract="创建和管理独立的片段，以便可在多个历程和营销活动中重用您的内容。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="创建片段"

片段是可重复使用的组件，可以在[!DNL Journey Optimizer]营销活动和历程中的一个或多个电子邮件中引用。 此功能允许您预构建多个自定义内容块，营销用户可以使用这些内容块在改进的设计过程中快速组合电子邮件内容。

![](../rn/assets/do-not-localize/fragments.gif)

➡️[了解如何在这些视频中管理、创作和使用片段](#video-fragments)

要充分利用片段，请执行以下操作：

* **创建您自己的片段**：从头开始创建可视化或表达式片段，或者通过将内容另存为片段来创建可视化或表达式片段。 [了解如何创建片段](#create-fragments)。 此外，您还可以利用Journey Optimizer **Content REST API**&#x200B;管理内容片段。 有关详细信息，请参阅[Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}。
* **重复使用您的片段：**&#x200B;根据需要多次在内容中使用它们。 请参阅[添加可视化片段](../email/use-visual-fragments.md)和[利用表达式片段](../personalization/use-expression-fragments.md)

## 开始前 {#fragment-prerequisites}

要创建、编辑、存档和发布片段，您需要具有&#x200B;**[!DNL Content Library Manager]**&#x200B;产品配置文件中包含的&#x200B;**[!DNL Manage library items]**&#x200B;和&#x200B;**[Publish片段]**&#x200B;权限。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)

在此版本中，以下限制适用：

* **可视化片段**&#x200B;仅适用于电子邮件渠道。
* **表达式片段**&#x200B;不可用于应用程序内渠道。

## 可视化和表达式片段 {#visual-expression}

有两种类型的片段可用：

* **可视化片段**&#x200B;是预定义的可视化块，您可以使用[电子邮件Designer](../email/get-started-email-design.md)在多个电子邮件投放中重用，或在[内容模板](../email/use-email-templates.md)中重用。
* **表达式片段**&#x200B;是预定义的表达式，可从[个性化编辑器](../personalization/personalization-build-expressions.md)中的专用条目中使用。

可从左侧菜单&#x200B;**[!UICONTROL 内容管理]** > **[!UICONTROL 片段]**&#x200B;访问所有创建的片段。 [了解如何管理片段](../content-management/manage-fragments.md)

![](assets/fragment-list.png)

## 操作方法视频 {#video-fragments}

了解如何在[!DNL Journey Optimizer]中管理、创作和使用&#x200B;**可视化片段**。

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

了解如何在[!DNL Journey Optimizer]中管理、创作和使用&#x200B;**表达式片段**。

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
