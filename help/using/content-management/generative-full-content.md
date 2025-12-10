---
solution: Journey Optimizer
product: journey optimizer
title: 使用AI助手生成完整内容
description: 了解如何使用Journey Optimizer中的AI助手生成完整的内容体验。
feature: Content Assistant
topic: Artificial Intelligence
role: User
level: Beginner
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '1834'
ht-degree: 2%

---

# 使用AI助手生成完整内容 {#generative-full-content}

>[!IMPORTANT]
>
>在开始使用此功能之前，请阅读相关的[护栏和限制](gs-generative.md#generative-guardrails)。
></br>
>
>您必须同意[用户协议](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)，然后才能在Journey Optimizer中使用AI助手。 有关更多信息，请与您的 Adobe 代表联系。

使用Journey Optimizer中的AI助手在电子邮件、Web、登陆页和推送通知渠道中生成完整的内容体验。 AI Assistant通过创建与受众产生共鸣的综合内容，帮助您优化投放的影响。

## 用于电子邮件和Web渠道 {#email-web-channels}

AI助手可以为电子邮件营销活动、网页和登陆页生成完整的内容体验，并生成文本和图像。 这项强大的功能可帮助您创建引人注目的品牌内内容，这些内容可通过所有数字接触点与您的受众连接。

### 访问和配置 {#access-configure}

开始使用AI助手创建内容之前，您需要设置活动或历程并打开内容编辑器。 使用以下步骤准备工作区并访问AI助手面板。

1. 创建和配置活动或历程：
   * **电子邮件**：创建和配置电子邮件促销活动后，单击&#x200B;**[!UICONTROL 编辑内容]**。 [了解详情](../campaigns/create-campaign.md)
   * **网页**：创建和配置网页后，单击&#x200B;**[!UICONTROL 编辑网页]**。 [了解详情](../web/create-web.md)
   * **登陆页面**：创建和配置登陆页面后，单击&#x200B;**[!UICONTROL 打开设计器]**。 [了解详情](../landing-pages/create-lp.md)

1. 从右侧菜单中，选择&#x200B;**[!UICONTROL AI助手]**（或&#x200B;**[!UICONTROL 显示Web内容助手]**）。

   ![AI助手面板，显示品牌选择和提示字段](assets/full-email-1.png){zoomable="yes"}

### 生成内容 {#generate-content}

打开AI助手后，您现在可以配置生成设置，以创建与您的品牌和营销活动目标相匹配的内容。 自定义文本和图像参数、添加品牌资产并提供提示，以指导AI为您的受众生成相关变体。

1. 选择您的&#x200B;**[!UICONTROL 品牌]**&#x200B;以确保AI生成的内容与您的品牌规格一致。 [了解有关Brands的更多信息](brands.md)。

1. 通过描述要在&#x200B;**[!UICONTROL 提示]**&#x200B;字段中生成的内容，优化内容。

   如果您在制作提示时寻求帮助，请访问&#x200B;**[!UICONTROL 提示库]**，该库提供了多种提示想法来改进促销活动。 [了解有关提示最佳实践的更多信息](ai-assistant-prompting-guide.md)

   ![带有“提示库”按钮的提示字段](assets/full-email-2.png){zoomable="yes"}

1. **对于电子邮件**，您可以切换&#x200B;**[!UICONTROL 主题行]**&#x200B;和&#x200B;**[!UICONTROL 预编译标头]**&#x200B;选项以将其包含在变量生成中。

1. 使用&#x200B;**[!UICONTROL 文本设置]**&#x200B;选项定制提示：

   * **[!UICONTROL 通信策略]**：为生成的文本选择最合适的通信样式。
   * **[!UICONTROL 语言]**：选择所生成内容的语言。
   * **[!UICONTROL 音调]**：该音调应与您的受众产生共鸣。 无论您是要提供信息、好玩还是具有说服力，AI Assistant都可以相应地调整消息。

     ![显示通信策略、语言和音调选项的文本设置面板](assets/full-email-4.png){zoomable="yes"}

1. 选择您的&#x200B;**[!UICONTROL 图像设置]**：

   * **[!UICONTROL 内容类型]**：这将对可视化元素的性质进行分类，区分不同的可视化表示形式，如照片、图形或艺术品。
   * **[!UICONTROL 视觉强度]**：您可以通过调整图像的强度来控制其影响。 较低的设置(2)将产生更柔和、更克制的外观，而较高的设置(10)将使图像更生动、视觉更强大。
   * **[!UICONTROL 颜色和色调]**：图像内颜色的总体外观及其传达的情绪或气氛。
   * **[!UICONTROL 照明]**：这是指图像中的闪电，它塑造了大气层，突出了特定的元素。
   * **[!UICONTROL 合成]**：这指的是图像框架中元素的排列

     ![显示“内容类型”、“视觉强度”、“颜色和色调”、“光源”和“合成”选项的“图像设置”面板](assets/full-email-6.png){zoomable="yes"}

1. 从&#x200B;**[!UICONTROL 引用内容]**&#x200B;菜单中，单击&#x200B;**[!UICONTROL 上载文件]**&#x200B;以添加任何品牌资产，这些品牌资产包含可以提供其他上下文AI助手的内容或选择以前上载的内容。

   以前上载的文件在&#x200B;**[!UICONTROL 上载的引用内容]**&#x200B;下拉列表中可用。 只需切换您想要包含到层代中的资产。

   ![带有“上载品牌资产”按钮的“品牌资产”部分](assets/full-email-3.png){zoomable="yes"}

1. 提示就绪后，单击&#x200B;**[!UICONTROL 生成]**。

### 优化并完成 {#refine-finalize}

生成内容变体后，您可以优化结果以确保它们满足您的确切要求。 审查品牌定位、调整语调和语言，并准备内容以在您的营销活动或历程中激活。

1. 生成后，浏览&#x200B;**[!UICONTROL 变体]**。

1. 单击百分比图标可查看您的&#x200B;**[!UICONTROL 品牌一致性得分]**&#x200B;并识别与您的品牌的所有不一致性。

   了解有关[品牌一致性分数](brands-score.md)的更多信息。

   ![品牌一致性分数面板显示百分比分数](assets/full-email-7.png){zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 预览]**&#x200B;以查看所选变体的全屏版本，或单击&#x200B;**[!UICONTROL 应用]**&#x200B;以替换当前内容。

1. 导航到&#x200B;**[!UICONTROL 预览]**&#x200B;窗口中的&#x200B;**[!UICONTROL 优化]**&#x200B;选项以访问其他自定义功能：

   * **[!UICONTROL 重写]**：重写邮件，同时保留其含义。 此选项可帮助您在不更改核心消息的情况下生成替代措辞、改善流量或调整词语。

   * **[!UICONTROL 使用更简单的语言]**：利用AI Assistant简化您的语言，确保为更广泛的受众提供清晰易懂的语言。

   * **[!UICONTROL 翻译]**：简化您的语言，确保更广大的受众能够清晰地访问这些内容。

   * **[!UICONTROL 更改语调]**：调整消息语调以更好地匹配您的沟通风格，即使其更友好、更专业、更紧急或更励志。

   * **[!UICONTROL 更改沟通策略]**：根据您的目标修改消息传送方式，如创建紧急消息或强调令人兴奋的吸引力。

     ![显示选项的细化菜单](assets/full-email-5.png){zoomable="yes"}

1. 打开&#x200B;**[!UICONTROL 品牌一致性]**&#x200B;选项卡，查看内容如何与[品牌指南](brands.md)保持一致。

1. 找到相应的内容后，单击&#x200B;**[!UICONTROL 选择]**。

   您还可以为内容启用试验。 [了解详情](generative-experimentation.md)

1. 插入个性化字段以根据用户档案数据自定义您的内容。 然后，单击&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮以控制渲染，并使用测试配置文件检查个性化设置。 [了解详情](../personalization/personalize.md)

1. 查看并激活您的内容：
   * **电子邮件**：定义内容、受众和计划后，您就可以准备电子邮件促销活动。 [了解详情](../campaigns/review-activate-campaign.md)
   * **Web**：定义Web营销活动设置并根据需要编辑内容后，您可以查看和激活Web营销活动。 [了解详情](../web/create-web.md#activate-web-campaign)
   * **登陆页面**：登陆页面准备就绪后，您可以发布该登陆页面，以供在消息中使用。 [了解详情](../landing-pages/create-lp.md#publish-landing-page)

## 适用于移动渠道 {#mobile-channels}

AI Assistant还支持为移动推送通知生成内容，从而允许您为移动应用程序创建引人入胜的标题、消息和图像。 这有助于您在所有客户接触点（包括移动设备）之间保持一致、高质量的通信。


### 访问和配置 {#mobile-access-configure}

要使用AI助手进行推送通知，请首先设置推送活动并打开内容编辑器。 以下步骤将指导您准备活动和访问AI助手工具。

1. 创建和配置推送通知营销活动后，单击&#x200B;**[!UICONTROL 编辑内容]**。

   有关如何配置推送通知促销活动的详细信息，请参阅[此页面](../push/create-push.md)。

1. 填写营销活动的&#x200B;**[!UICONTROL 基本详细信息]**。 完成后，单击&#x200B;**[!UICONTROL 编辑内容]**。

1. 根据需要个性化您的推送通知。 [了解详情](../push/design-push.md)

1. 访问&#x200B;**[!UICONTROL 显示AI助手]**&#x200B;菜单。

   ![已打开带有AI助手面板的推送通知编辑器](assets/push-genai-full-1.png){zoomable="yes"}

### 生成内容 {#mobile-generate-content}

访问用于推送通知的AI Assistant后，您可以配置生成设置以创建引人注目的移动内容。 定义文本和图像偏好设置，选择品牌资产，并使用提示生成吸引移动用户的推送通知变体。

1. 为AI助手启用&#x200B;**[!UICONTROL 使用原始内容]**&#x200B;选项，以根据所选内容对新内容进行个性化设置。

1. 选择您的&#x200B;**[!UICONTROL 品牌]**&#x200B;以确保AI生成的内容与您的品牌规格一致。 [了解有关Brands的更多信息](brands.md)。

   请注意，品牌功能作为专用测试版发布，并将在未来版本中逐步向所有客户提供。

1. 通过描述要在&#x200B;**[!UICONTROL 提示]**&#x200B;字段中生成的内容，优化内容。

   如果您在制作提示时寻求帮助，请访问&#x200B;**[!UICONTROL 提示库]**，该库提供了多种提示想法来改进促销活动。

   具有提示字段和选项的![AI助手](assets/push-genai-full-2.png){zoomable="yes"}

1. 选择要生成的字段：**[!UICONTROL 标题]**、**[!UICONTROL 消息]**&#x200B;和/或&#x200B;**[!UICONTROL 图像]**。

1. 使用&#x200B;**[!UICONTROL 文本设置]**&#x200B;选项定制提示：

   * **[!UICONTROL 通信策略]**：为生成的文本选择最合适的通信样式。
   * **[!UICONTROL 语言]**：选择所生成内容的语言。
   * **[!UICONTROL 音调]**：推送通知的音调应该会与受众产生共鸣。 无论您是要提供信息、好玩还是具有说服力，AI Assistant都可以相应地调整消息。

     推送通知的![文本设置面板](assets/push-genai-full-3.png){zoomable="yes"}

1. 选择您的&#x200B;**[!UICONTROL 图像设置]**：

   * **[!UICONTROL 内容类型]**：这将对可视化元素的性质进行分类，区分不同的可视化表示形式，如照片、图形或艺术品。
   * **[!UICONTROL 视觉强度]**：您可以通过调整图像的强度来控制其影响。 较低的设置(2)将产生更柔和、更克制的外观，而较高的设置(10)将使图像更生动、视觉更强大。
   * **[!UICONTROL 颜色和色调]**：图像内颜色的总体外观及其传达的情绪或气氛。
   * **[!UICONTROL 照明]**：这是指图像中的闪电，它塑造了大气层，突出了特定的元素。
   * **[!UICONTROL 合成]**：这指的是图像框架中元素的排列

     ![推送通知的图像设置](assets/push-genai-full-5.png){zoomable="yes"}

1. 从&#x200B;**[!UICONTROL 引用内容]**&#x200B;菜单中，单击&#x200B;**[!UICONTROL 上载文件]**&#x200B;以添加任何品牌资产，这些品牌资产包含可以提供其他上下文AI助手的内容或选择以前上载的内容。

   以前上载的文件在&#x200B;**[!UICONTROL 上载的引用内容]**&#x200B;下拉列表中可用。 只需切换您想要包含到层代中的资产。

1. 提示就绪后，单击&#x200B;**[!UICONTROL 生成]**。

### 优化并完成 {#mobile-refine-finalize}

查看生成的推送通知变体后，您可以优化内容以使其更加完美。 在激活推送营销活动之前，使用优化工具调整语言和语气、验证品牌一致性及个性化内容。

1. 浏览生成的&#x200B;**[!UICONTROL 变体]**。

1. 单击百分比图标可查看您的&#x200B;**[!UICONTROL 品牌一致性得分]**&#x200B;并识别与您的品牌的所有不一致性。

   了解有关[品牌一致性分数](brands-score.md)的更多信息。

   ![生成的推送通知变体具有品牌一致性分数](assets/push-genai-full-4.png){zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 预览]**&#x200B;以查看所选变体的全屏版本，或单击&#x200B;**[!UICONTROL 应用]**&#x200B;以替换当前内容。

1. 导航到&#x200B;**[!UICONTROL 预览]**&#x200B;窗口中的&#x200B;**[!UICONTROL 优化]**&#x200B;选项以访问其他自定义功能：

   * **[!UICONTROL 用作引用内容]**：所选变量将用作用于生成其他结果的引用内容。

   * **[!UICONTROL 重写]**：重写邮件，同时保留其含义。 此选项可帮助您在不更改核心消息的情况下生成替代措辞、改善流量或调整词语。

   * **[!UICONTROL 使用更简单的语言]**：利用AI Assistant简化您的语言，确保为更广泛的受众提供清晰易懂的语言。

   * **[!UICONTROL 更改语调]**：调整消息语调以更好地匹配您的沟通风格，即使其更友好、更专业、更紧急或更励志。

   * **[!UICONTROL 更改沟通策略]**：根据您的目标修改消息传送方式，如创建紧急消息或强调令人兴奋的吸引力。

     ![优化推送通知的选项](assets/push-genai-full-6.png){zoomable="yes"}

1. 打开&#x200B;**[!UICONTROL 品牌一致性]**&#x200B;选项卡，查看内容如何与[品牌指南](brands.md)保持一致。

1. 找到相应的内容后，单击&#x200B;**[!UICONTROL 选择]**。

   您还可以为内容启用试验。 [了解详情](generative-experimentation.md)

1. 插入个性化字段以根据用户档案数据自定义推送通知内容。 然后，单击&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮以控制渲染，并使用测试配置文件检查个性化设置。 [了解详情](../personalization/personalize.md)

定义内容、受众和计划后，便可以准备推送营销活动。 [了解详情](../campaigns/review-activate-campaign.md)

## 操作方法视频 {#video}

了解如何在Journey Optimizer中使用AI助手生成完整内容体验。

>[!VIDEO](https://video.tv.adobe.com/v/3433552)
