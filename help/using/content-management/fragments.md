---
solution: Journey Optimizer
product: journey optimizer
title: 开始使用片段
description: 了解如何使用内容片段以在Journey Optimizer营销活动和历程中重用内容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: 08f12adf384b98dfa1d69cbc2d684c3bf58d31fa
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 2%

---

# 开始使用片段 {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="定义您自己的片段"
>abstract="创建和管理独立片段，以使您的内容可在多个历程和营销活动中重复使用。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="创建片段"

片段是可重复使用的组件，可在其中一个或多个电子邮件中引用 [!DNL Journey Optimizer] 营销活动和历程。 此功能允许预先构建多个自定义内容块，营销用户可以使用这些内容块在改进的设计过程中快速组合电子邮件内容。

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [在这些视频中了解如何管理、创作和使用片段](#video-fragments)

要充分利用片段，请执行以下操作：

* **创建您自己的片段**：从头开始创建可视化或表达式片段，或者通过将内容另存为片段来创建可视化或表达式片段。 [了解如何创建片段](#create-fragments). 此外，您还可以利用Journey Optimizer **内容REST API** 以管理内容片段。 有关详细信息，请参见 [Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.
* **重用您的片段：** 您可以根据需要在内容中多次使用它们。 请参阅 [添加可视片段](../email/use-visual-fragments.md) 和 [利用表达式片段](../personalization/use-expression-fragments.md)

## 开始前 {#fragment-prerequisites}

>[!NOTE]
>
>要创建、编辑和存档片段，您必须具有 **[!DNL Manage library items]** 权限包含在 **[!DNL Content Library Manager]** 产品配置文件。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)

在此版本中，以下限制适用：

* **可视化片段** 仅适用于电子邮件渠道。
* **表达式片段** 不可用于应用程序内渠道。

## 可视化和表达式片段 {#visual-expression}

提供了两种类型的片段：

* **可视化片段** 是预定义的可视化块，您可以使用它在多个电子邮件投放中重用 [电子邮件设计工具](../email/get-started-email-design.md)，或在 [内容模板](../email/use-email-templates.md).
* **表达式片段** 是预定义的表达式，可从中的专用条目访问 [个性化编辑器](../personalization/personalization-build-expressions.md).


所有片段都可从以下位置访问： **[!UICONTROL 内容管理]** > **[!UICONTROL 片段]**  左侧菜单。

![](assets/fragment-list.png)

## 操作方法视频 {#video-fragments}

了解如何在中管理、创作和使用可视化片段 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

了解如何在中管理、创作和使用表达式片段 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
