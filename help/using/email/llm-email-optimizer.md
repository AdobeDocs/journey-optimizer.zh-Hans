---
title: 优化AI收件箱的电子邮件文本
description: 在Journey Optimizer中优化电子邮件的纯文本层，以便AI辅助收件箱客户可以在使用AI优化的电子邮件Designer中总结邮件或提取意图时使用您的优惠和CTA。
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: 0c2f95ce-28a0-480c-9829-b7e4975b6340
hide: true
source-git-commit: 434480b9ea30ab456e97c2cf281adb1253b8f73d
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 1%

---

# 优化AI收件箱的电子邮件文本 {#email-text-optimizer}

[!DNL Adobe Journey Optimizer]附带电子邮件渠道功能，可帮助您构建邮件的特定版本以改进AI辅助收件箱体验，例如[!DNL Apple Intelligence]中的[!DNL Google Gemini]和[!DNL Gmail]，以便他们能够更准确地回答问题并根据您的内容总结邮件，从而获得更好的结果。

您可以使用此功能来优化消息的专用文本版本，以便AI辅助收件箱体验更有可能显示您想要的选件、行动要求和详细信息，而不是精简自动生成文本或不相关的上下文。

## 工作原理 {#how-it-works}

收件人在AI辅助收件箱体验中可能会问的典型问题是&#x200B;*此电子邮件是关于什么的？*&#x200B;或&#x200B;*这些选件是什么？*。

* 这些AI助理提供的答案可能是简短的总结（例如，消息为促销，提及VIP早期访问和促销，并包含指向产品类别的链接），但仍然忽略了营销人员关心的目标，因为助理从他们实际看到的任何文本中推断出的内容 — 不一定是您打算看到的完整故事。

* 此外，助理可以主动搜索与品牌相关的折扣或优惠券，并将它们折叠到答案中，这样用户就不会再只查看您的消息实际承诺的内容。 这种行为对最终用户很有用，但是对于需要答案来跟踪发送中真实术语的营销人员，这种行为会稀释他们的控制权。

为防止出现这些问题，[!DNL Journey Optimizer]创建了邮件的附加文本版本，以便优惠券、折扣范围、行动号召和其他优先级显示在清晰的线性副本的前面。

>[!NOTE]
>
>此专用文本版本与消息的默认或自定义纯文本版本不同。 [了解详情](text-version-email.md)

目标是让收件箱AI为您定义的优惠和操作提供基础摘要和问答，而不是依赖简单的默认文本部分或不相关的Web结果。

>[!IMPORTANT]
>
>确切的AI助手行为取决于收件箱提供商和模型版本。 在发送电子邮件后，外部AI客户端提供的答案和摘要可能会错误、不完整或与Web结果混杂在一起。
>
>为AI收件箱优化电子邮件文本功能仅在Journey Optimizer中生成专用文本版本；它无法保证第三方助理如何解释或显示消息。 详细了解第三方收件箱AI[的](#inbox-ai-risks)限制和风险。

## 推荐用例 {#use-cases}

<!--
* **Critical details only in images** — Offers, promo codes, or deadlines shown in banners or graphics are invisible in plain text. Use the optimizer (and manual edits) so the same facts appear as text, improving extraction by AI summaries and text-only clients.
-->

* **密集或零碎的自动生成的文本** — 当默认纯文本难以扫描时，优化可以生成更清晰的线性叙述，其中具有明确的选件和链接。

* **控制收件箱问答** — 如果您希望收件人询问助理&#x200B;*电子邮件内容*&#x200B;或&#x200B;*选件内容*，则功能强大的ai收件箱版本可减少部分摘要并避免依赖与已批准副本无关的Web补充答案。

## 针对AI收件箱体验进行优化 {#optimize-with-ai}

>[!IMPORTANT]
>
>在使用此功能之前，请阅读相关的[风险和限制](#inbox-ai-risks)。
>
>要访问此功能，您必须同意用户协议，该协议在您第一次在[!DNL Journey Optimizer]中使用创作AI时显示。 有关详细信息，请阅读[Adobe Experience Cloud Generative AI用户准则](https://www.adobe.com/cn/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}。

要优化带有[!DNL Journey Optimizer]的AI收件箱的电子邮件的纯文本版本，请执行以下步骤。

1. 在[向Designer发送电子邮件](content-from-scratch.md)中打开您的电子邮件（来自营销活动、历程或模板，具体取决于您的工作流）。

1. 单击&#x200B;**[!UICONTROL 针对AI收件箱进行优化]**&#x200B;按钮可生成一个改进版本，该版本突出显示了用于AI辅助阅读和摘要的关键信息。

   电子邮件Designer中的![为AI收件箱优化](assets/optimize-for-ai-button.png){zoomable="yes" width="80%"}按钮

1. 如果这是您在[!DNL Journey Optimizer]中第一次使用创作AI，将要求您同意用户协议。 若要了解更多信息，请查看[Adobe Generative AI用户准则](https://www.adobe.com/cn/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}。

   ![Journey Optimizer中的Generative AI用户协议对话框](assets/optimize-ai-inbox-agreement.png){width=50%}

   单击&#x200B;**[!UICONTROL 同意]**&#x200B;以继续。

1. 将显示生成的版本。

   ![已为AI收件箱优化生成的版本](assets/optimize-ai-inbox-output.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >**为AI收件箱优化电子邮件文本**&#x200B;不会更改您的HTML设计、布局或图像。

1. 要对自动生成的内容进行更改，请选择&#x200B;**[!UICONTROL 启用编辑]**&#x200B;切换开关，并根据需要手动编辑内容。

1. 一旦对您的版本满意，请单击&#x200B;**[!UICONTROL 优化电子邮件]**&#x200B;按钮进行确认。

1. 您的电子邮件现在已成功针对AI收件箱进行优化。

1. 要访问或编辑优化版本，请单击&#x200B;**[!UICONTROL 已为AI收件箱优化]**&#x200B;按钮。

   电子邮件Designer中的![重新优化按钮](assets/optimize-ai-inbox-optimized-button.png){zoomable="yes" width="80%"}

1. 此时会显示优化版本。 您可以&#x200B;**[!UICONTROL 删除优化]**&#x200B;或单击&#x200B;**[!UICONTROL 重新优化]**&#x200B;以生成新版本。

   电子邮件Designer中的![以前优化的版本](assets/optimize-ai-inbox-optimized-version.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >如果您对原始HTML内容进行了更改，则需要重新优化人工智能收件箱版本。

## 第三方收件箱人工智能的风险和限制 {#inbox-ai-risks}

“针对AI收件箱优化电子邮件”功能可帮助您准备电子邮件的版本，以了解邮箱提供商处理您[!DNL Journey Optimizer]发送的方式。 它不控制这些提供商的产品。 在传递邮件后，[!DNL Gmail]、[!DNL Apple] Mail、[!DNL Outlook]或其他客户端中的任何AI功能都将按照其条款、模型和策略运行，而不是Adobe的运行。

* **不可预测的演示文稿** — 摘要、通知模糊和对话式回答可能会忽略选件、错误地陈述价格或日期、将内容与不相关的Web结果合并，或者以不再匹配您批准的副本的方式进行转述。 供应商更新模型或UI时行为会发生更改，恕不另行通知。

* **无法保证与HTML的等同性** — 依赖预览或助理答案的收件人可能永远不会看到您的HTML完整设计、图像或法律页脚。 他们认为，这条信息“说”的内容可能只来自于人工智能生成的简短摘要。

* **隐私、合规性和数据使用** — 收件箱AI可以根据提供商的隐私政策、保留和区域规则，处理提供商基础架构上的邮件内容。 受管控行业中的组织应评估收件人使用此类功能是否会影响其义务，而不管电子邮件是如何在[!DNL Journey Optimizer]中创作的。

* **品牌和法律曝光度** — 不正确或不完整的AI摘要仍可能会导致客户对促销活动、条款或选择退出语言产生混淆或争议。 **针对AI收件箱优化电子邮件**&#x200B;不能确保第三方模型能够忠实地重现电子邮件的优化版本。

* **[!UICONTROL 在]**&#x200B;中针对AI收件箱进行优化[!DNL Journey Optimizer] — Email Designer中的创作时间控件与最终用户收件箱助理不同。 发送之前请始终查看生成的纯文本。

## 相关主题 {#related-topics}

* [电子邮件设计快速入门](get-started-email-design.md)
* 若要更广泛地了解Adobe的生成功能，请参阅[开始使用AI助手来创建内容](../content-management/gs-generative.md)。
