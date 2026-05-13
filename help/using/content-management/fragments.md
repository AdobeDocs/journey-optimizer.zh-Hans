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
TQID: https://experienceleague.adobe.com/2XVXr3MjYnD-7o0C2ARXQ8j3sJOFfJfvjfCEZdkV50I
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a653cc2e-bc85-4353-a306-399e5b247978id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: c6e980f5-2d4f-494f-beef-186b9ecf1513id: d595a60b-bcf5-4a63-a189-66a0be755cc7id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 346
ht-degree: 21%

---

# 片段入门 {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="定义您自已的片段"
>abstract="创建和管理独立的片段，以便可在多个历程和营销活动中重用您的内容。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="创建片段"

片段是可重复使用的组件，可以在[!DNL Journey Optimizer]营销活动和历程中的一个或多个电子邮件中引用。 此功能允许您预构建多个自定义内容块，营销用户可以使用这些内容块在改进的设计过程中快速组合电子邮件内容。

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [了解如何在这些视频中管理、创作和使用片段](#video-fragments)

要充分利用片段，请执行以下操作：

* **创建您自己的片段**：从头开始创建可视化或表达式片段，或者通过将内容另存为片段来创建可视化或表达式片段。 [了解如何创建片段](create-fragments.md)。 此外，您还可以利用Journey Optimizer **Content REST API**&#x200B;管理内容片段。 有关详细信息，请参阅[Journey Optimizer API文档](https://developer.adobe.com/journey-optimizer-apis/references/content){target="_blank"}。
* **重复使用您的片段：**&#x200B;根据需要多次在内容中使用它们。 请参阅[添加可视化片段](../email/use-visual-fragments.md)和[利用表达式片段](../personalization/use-expression-fragments.md)

## 开始前 {#fragment-prerequisites}

要创建、编辑、存档和发布片段，您需要拥有 **[!DNL Content Library Manager]** 产品配置文件中包含的 **[!DNL Manage library items]** 和&#x200B;**[发布片段]**&#x200B;的权限。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)

在此版本中，以下限制适用：

* **可视化片段**&#x200B;仅适用于电子邮件渠道。
* **表达式片段**&#x200B;不可用于应用程序内渠道。

[此部分](../start/guardrails.md#fragments-guardrails)中有更多适用于片段的护栏。

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
