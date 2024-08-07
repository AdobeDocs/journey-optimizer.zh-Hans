---
solution: Journey Optimizer
product: journey optimizer
title: 使用 AI 助手生成短信
description: 开始使用AI助手生成短信内容
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta 版" type="Informative"
hide: true
hidefromtoc: true
exl-id: 5fd1cc3a-c023-4e8e-bfac-9a86bd33bbb3
source-git-commit: b62f8954e09f50896ad5e70784c5a93943617e85
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 8%

---

# 使用 AI 助手生成短信 {#generative-sms}

>[!BEGINSHADEBOX]

**目录**

* [AI 助手入门](gs-generative.md)
* [使用 AI 助手生成电子邮件](generative-email.md)
* 使用 AI 助手生成短信
* [使用 AI 助手进行推送生成](generative-push.md)
* [使用 AI 助手进行内容试验](generative-experimentation.md)

>[!ENDSHADEBOX]

根据受众的偏好对短信消息进行精心设计和定制后，可在Journey Optimizer中提升与AI助理的通信。

此资源提供了有见地的建议，可优化您的内容，帮助您的消息引起共鸣并促进最大程度的参与。

浏览以下选项卡，了解如何使用Journey Optimizer中的AI助手。

>[!NOTE]
>
>在开始使用此功能之前，请阅读相关的[护栏和限制](gs-generative.md#generative-guardrails)。

>[!BEGINTABS]

>[!TAB 完整短信生成]

1. 创建和配置短信营销活动后，单击&#x200B;**[!UICONTROL 编辑内容]**。

   有关如何配置短信促销活动的详细信息，请参阅[此页面](../sms/create-sms.md)。

1. 填写营销活动的&#x200B;**[!UICONTROL 基本详细信息]**。 完成后，单击&#x200B;**[!UICONTROL 编辑内容]**。

1. 根据需要个性化短信消息。 [了解详情](../sms/create-sms.md)

1. 访问&#x200B;**[!UICONTROL 显示AI助手]**&#x200B;菜单。

   ![](assets/sms-genai-1.png){zoomable="yes"}

1. 为AI助手启用&#x200B;**[!UICONTROL 使用原始内容]**&#x200B;选项，以根据您的营销活动内容、名称和所选受众来个性化新内容。

   您的提示必须始终与特定上下文关联。

1. 通过描述要在&#x200B;**[!UICONTROL 提示]**&#x200B;字段中生成的内容，优化内容。

   如果您在制作提示时寻求帮助，请访问&#x200B;**[!UICONTROL 提示库]**，该库提供了多种提示想法来改进促销活动。

   ![](assets/sms-genai-2.png){zoomable="yes"}

1. 选择&#x200B;**[!UICONTROL 上载品牌资产]**&#x200B;可添加任何包含可为AI助手提供其他上下文的内容的品牌资产。

1. 使用不同的选项定制提示：

   * **[!UICONTROL 通信策略]**：为生成的文本选择所需的通信方法。
   * **[!UICONTROL 语言]**：选择变体内容的语言。
   * **[!UICONTROL 色调]**：确保文本适合您的受众和用途。
   * **[!UICONTROL 长度]**：使用范围滑块选择内容的长度。

   ![](assets/sms-genai-3.png){zoomable="yes"}

1. 提示就绪后，单击&#x200B;**[!UICONTROL 生成]**。

1. 浏览生成的&#x200B;**[!UICONTROL 变体]**&#x200B;并单击&#x200B;**[!UICONTROL 预览]**&#x200B;以查看所选变体的全屏版本。

1. 导航到&#x200B;**[!UICONTROL 预览]**&#x200B;窗口中的&#x200B;**[!UICONTROL 优化]**&#x200B;选项以访问其他自定义功能并微调您的首选项变量：

   * **[!UICONTROL 用作引用内容]**：所选变量将用作用于生成其他结果的引用内容。

   * **[!UICONTROL 重述]**：AI助手可以通过不同的方式重述您的消息，使您的写作保持新鲜，并吸引各种受众。

   * **[!UICONTROL 使用更简单的语言]**：利用AI Assistant简化您的语言，确保更广大的受众拥有清晰易懂的语言。

   ![](assets/sms-genai-4.png){zoomable="yes"}

1. 找到相应的内容后，单击&#x200B;**[!UICONTROL 选择]**。

   您还可以为内容启用试验。 [了解详情](generative-experimentation.md)

1. 插入个性化字段，以根据用户档案数据自定义短信内容。 [详细了解内容个性化](../personalization/personalize.md)

1. 定义消息内容后，单击&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮以控制渲染，并使用测试用户档案检查个性化设置。 [了解详情](../personalization/personalize.md)

定义内容、受众和计划后，便可以准备短信营销活动。 [了解详情](../campaigns/review-activate-campaign.md)

>[!TAB 文本生成]

1. 创建和配置短信营销活动后，单击&#x200B;**[!UICONTROL 编辑内容]**。

   有关如何配置短信促销活动的详细信息，请参阅[此页面](../sms/create-sms.md)。

1. 填写营销活动的&#x200B;**[!UICONTROL 基本详细信息]**。 完成后，单击&#x200B;**[!UICONTROL 编辑内容]**。

1. 根据需要个性化短信消息。 [了解详情](../sms/create-sms.md)

1. 访问&#x200B;**[!UICONTROL 消息]**&#x200B;字段旁边的&#x200B;**[!UICONTROL 使用AI助手编辑文本]**&#x200B;菜单。

   ![](assets/sms-text-genai-1.png){zoomable="yes"}

1. 为AI助手启用&#x200B;**[!UICONTROL 使用引用内容]**&#x200B;选项，以根据您的营销活动内容、名称和所选受众来个性化新内容。

   您的提示必须始终与特定上下文关联。

1. 通过描述要在&#x200B;**[!UICONTROL 提示]**&#x200B;字段中生成的内容，优化内容。

   如果您在制作提示时寻求帮助，请访问&#x200B;**[!UICONTROL 提示库]**，该库提供了多种提示想法来改进促销活动。

   ![](assets/sms-text-genai-1.png){zoomable="yes"}

1. 选择&#x200B;**[!UICONTROL 上载品牌资产]**&#x200B;可添加任何包含可为AI助手提供其他上下文的内容的品牌资产。

1. 使用不同的选项定制提示：

   * **[!UICONTROL 通信策略]**：为生成的文本选择所需的通信方法。
   * **[!UICONTROL 语言]**：选择变体内容的语言。
   * **[!UICONTROL 色调]**：确保文本适合您的受众和用途。
   * **[!UICONTROL 长度]**：使用范围滑块选择内容的长度。

   ![](assets/sms-text-genai-3.png){zoomable="yes"}

1. 提示就绪后，单击&#x200B;**[!UICONTROL 生成]**。

1. 浏览生成的&#x200B;**[!UICONTROL 变体]**&#x200B;并单击&#x200B;**[!UICONTROL 预览]**&#x200B;以查看所选变体的全屏版本。

1. 导航到&#x200B;**[!UICONTROL 预览]**&#x200B;窗口中的&#x200B;**[!UICONTROL 优化]**&#x200B;选项以访问其他自定义功能并微调您的首选项变量：

   * **[!UICONTROL 用作引用内容]**：所选变量将用作用于生成其他结果的引用内容。

   * **[!UICONTROL 重述]**：AI助手可以通过不同的方式重述您的消息，使您的写作保持新鲜，并吸引各种受众。

   * **[!UICONTROL 使用更简单的语言]**：利用AI Assistant简化您的语言，确保更广大的受众拥有清晰易懂的语言。

   ![](assets/sms-text-genai-4.png){zoomable="yes"}

1. 找到相应的内容后，单击&#x200B;**[!UICONTROL 选择]**。

   您还可以为内容启用试验。 [了解详情](generative-experimentation.md)

1. 插入个性化字段，以根据用户档案数据自定义短信内容。 [详细了解内容个性化](../personalization/personalize.md)

1. 定义消息内容后，单击&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮以控制渲染，并使用测试用户档案检查个性化设置。

定义内容、受众和计划后，便可以准备短信营销活动。 [了解详情](../campaigns/review-activate-campaign.md)

>[!ENDTABS]
