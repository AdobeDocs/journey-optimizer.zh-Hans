---
title: 创建基于代码的体验
description: 了解如何在Journey Optimizer中创建基于代码的体验
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 8%

---

# 创建基于代码的体验 {#create-code-based}

在[!DNL Journey Optimizer]中，您可以在历程或营销策划中创建基于代码的体验。

## 通过历程或营销活动添加基于代码的体验 {#create-code-based-experience}

要通过历程或营销活动开始构建基于代码的体验，请执行以下步骤。

>[!BEGINTABS]

>[!TAB 向历程添加基于代码的体验]

要向历程添加基于&#x200B;**代码的体验**&#x200B;活动，请执行以下步骤：

1. [创建历程](../building-journeys/journey-gs.md)。

1. 通过[事件](../building-journeys/general-events.md)或[读取受众](../building-journeys/read-audience.md)活动开始您的历程。

1. 从调色板的&#x200B;**[!UICONTROL 操作]**&#x200B;部分拖放基于&#x200B;**[!UICONTROL 代码的体验]**&#x200B;活动。

   ![](assets/code-based-activity-journey.png)

   >[!NOTE]
   >
   >由于&#x200B;**基于代码的体验**&#x200B;是入站体验活动，因此它附带3天&#x200B;**等待**&#x200B;活动。 [了解详情](../building-journeys/wait-activity.md#auto-wait-node)

1. 为您的消息输入&#x200B;**[!UICONTROL 标签]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 选择或创建要使用的基于代码的体验配置。 [了解详情](code-based-configuration.md)

   ![](assets/code-based-activity-config.png)

   >[!NOTE]
   >
   >当您使用同一渠道配置执行多个基于代码的体验操作时，如果最终用户符合多个操作的条件，则历程的&#x200B;**[!UICONTROL 优先级分数]**&#x200B;将决定向最终用户交付的内容。 [了解有关优先级分数的更多信息](../conflict-prioritization/priority-scores.md)

1. 选择&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮，然后根据需要使用个性化编辑器编辑您的内容。 [了解详情](#edit-code)

   您还可以使用现有内容模板作为代码内容的基础。 请注意，根据预先选择的渠道配置，可供选择的模板将范围限定为HTML或JSON。 [了解如何使用内容模板](../content-management/use-content-templates.md)

1. 如有必要，请通过拖放其他操作或事件来完成旅程流程。 [了解详情](../building-journeys/about-journey-activities.md)

1. 一旦您的代码库体验准备就绪，即可完成配置并发布历程以激活它。 [了解详情](../building-journeys/publishing-the-journey.md)

有关如何配置历程的详细信息，请参阅[此页面](../building-journeys/journey-gs.md)。

>[!TAB 创建基于代码的体验活动]

要通过营销活动开始构建&#x200B;**基于代码的体验**，请执行以下步骤。

1. 创建营销策划。 [了解详情](../campaigns/create-campaign.md)

1. 选择&#x200B;**计划 — 营销**&#x200B;营销活动类型。

1. 完成步骤以创建营销活动，如营销活动属性、[受众](../audience/about-audiences.md)和[计划](../campaigns/create-campaign.md#schedule)。 有关如何配置营销活动的详细信息，请参阅[此页面](../campaigns/get-started-with-campaigns.md)。

1. 选择&#x200B;**[!UICONTROL 基于代码的体验]**&#x200B;操作。

1. 选择或创建要使用的基于代码的体验配置。 [了解详情](code-based-configuration.md)

   ![](assets/code-based-campaign-surface.png)

   >[!NOTE]
   >
   >当您使用同一渠道配置执行多个基于代码的体验操作时，如果最终用户符合多个操作的条件，则促销活动的&#x200B;**[!UICONTROL 优先级得分]**&#x200B;将决定向最终用户交付的内容。 [了解有关优先级分数的更多信息](../conflict-prioritization/priority-scores.md)

1. 使用个性化编辑器，根据需要编辑您的内容。 [了解详情](#edit-code)

   您还可以使用现有内容模板作为代码内容的基础。 请注意，根据预先选择的渠道配置，可供选择的模板将范围限定为HTML或JSON。 [了解如何使用内容模板](../content-management/use-content-templates.md)

   <!--![](assets/code-based-campaign-edit-content.png)-->

有关如何配置营销活动的详细信息，请参阅[此页面](../campaigns/get-started-with-campaigns.md)。

➡️ [在此视频中了解如何创建基于代码的体验营销活动](#video)

>[!ENDTABS]

## 编辑代码内容 {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="使用个性化编辑器"
>abstract="插入和编辑要作为此基于代码的体验操作的一部分提供的代码。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/content-management/personalization/personalization-build-expressions" text="使用个性化编辑器"

要编辑基于代码的体验的内容，请执行以下步骤。

1. 从历程活动或营销活动版本屏幕中，选择&#x200B;**[!UICONTROL 编辑代码]**。

   ![](assets/code-based-campaign-edit-code.png)

   >[!NOTE]
   >
   >如果您使用基于代码的体验内容模板以及预定义的可编辑表单字段，则无需打开个性化编辑器即可管理这些字段的内容。 [了解详情](code-based-form-fields.md)

1. [个性化编辑器](../personalization/personalization-build-expressions.md)打开。 它是一个非可视化体验创建界面，允许您创作代码。

1. 您可以将创作模式从HTML切换到JSON，反之亦然。

   ![](assets/code-based-campaign-code-editor.png)

   >[!CAUTION]
   >
   >更改创作模式将导致当前代码全部丢失，因此，请确保在开始创作之前切换模式。

1. 根据需要输入代码。 您可以利用[!DNL Journey Optimizer]个性化编辑器及其所有个性化和创作功能。 [了解详情](../personalization/personalization-build-expressions.md)

1. 您可以根据需要添加HTML或JSON表达式片段。 [了解如何操作](../personalization/use-expression-fragments.md)

   您还可以将部分代码内容另存为片段。 [了解如何操作](../content-management/fragments.md#save-as-expression-fragment)

1. 通过基于代码的体验，您可以使用“决策”功能。 从左栏中选择&#x200B;**[!UICONTROL 决策策略]**&#x200B;图标，然后单击&#x200B;**[!UICONTROL 添加决策策略]**。 [了解详情](../experience-decisioning/create-decision.md#add-decision)

   ![](assets/code-based-campaign-create-decision.png)

   <!--![](../experience-decisioning/assets/decision-code-based-create.png)-->

   在历程或营销活动版本屏幕中，您还可以直接添加决策策略，而无需打开个性化编辑器。 使用右边栏上的专用图标显示&#x200B;**[!UICONTROL 决策]**&#x200B;部分。

   <!--![](assets/code-based-campaign-show-decisioning.png)-->

   有关创建决策策略的详细步骤，请参见[此部分](../experience-decisioning/create-decision.md#add-decision)。

1. 单击&#x200B;**[!UICONTROL 保存并关闭]**&#x200B;以确认更改。

现在，一旦您的开发人员进行API或SDK调用以获取渠道配置中定义的表面的内容，更改就会应用于您的网页或应用程序。

## 操作说明视频{#video}

以下视频介绍了如何创建基于代码的体验营销活动、配置其属性、测试并发布它。

>[!VIDEO](https://video.tv.adobe.com/v/3449463/?quality=12&learn=on&captions=chi_hans)
