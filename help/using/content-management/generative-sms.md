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
source-wordcount: '889'
ht-degree: 8%

---

# 使用 AI 助手生成短信 {#generative-sms}

>[!BEGINSHADEBOX]

**目录**

* [AI 助手入门](gs-generative.md)
* [使用 AI 助手生成电子邮件](generative-email.md)
* 使用 AI 助手生成短信
* [使用AI助手生成推送](generative-push.md)
* [使用AI助手进行内容试验](generative-experimentation.md)

>[!ENDSHADEBOX]

根据受众的偏好对短信消息进行精心设计和定制后，可在Journey Optimizer中提升与AI助理的通信。

此资源提供了有见地的建议，可优化您的内容，帮助您的消息引起共鸣并促进最大程度的参与。

浏览以下选项卡，了解如何使用Journey Optimizer中的AI助手。

>[!NOTE]
>
>在开始使用此功能之前，请阅读相关内容 [护栏和限制](gs-generative.md#generative-guardrails).

>[!BEGINTABS]

>[!TAB 完整短信生成]

1. 创建和配置短信营销活动后，单击 **[!UICONTROL 编辑内容]**.

   有关如何配置短信促销活动的更多信息，请参阅 [此页面](../sms/create-sms.md).

1. 填写 **[!UICONTROL 基本详细信息]** 您的营销活动。 完成后，单击 **[!UICONTROL 编辑内容]**.

1. 根据需要个性化短信消息。 [了解详情](../sms/create-sms.md)

1. 访问 **[!UICONTROL 显示AI助手]** 菜单。

   ![](assets/sms-genai-1.png){zoomable=&quot;yes&quot;}

1. 启用 **[!UICONTROL 使用原始内容]** AI助手选项，用于根据您的营销活动内容、名称和选定的受众来个性化新内容。

   您的提示必须始终与特定上下文关联。

1. 通过描述您要在 **[!UICONTROL 提示]** 字段。

   如果您在制作提示时需要帮助，请访问 **[!UICONTROL 提示库]** 其中提供了多种提示性想法来改进您的营销活动。

   ![](assets/sms-genai-2.png){zoomable=&quot;yes&quot;}

1. 选择 **[!UICONTROL 上传品牌资产]** 添加任何品牌资产，其中包含可为AI助手提供其他上下文的内容。

1. 使用不同的选项定制提示：

   * **[!UICONTROL 沟通策略]**：为生成的文本选择所需的通信方法。
   * **[!UICONTROL 语言]**：选择变体内容的语言。
   * **[!UICONTROL 色调]**：确保文本适合您的受众和用途。
   * **[!UICONTROL 长度]**：使用范围滑块选择内容的长度。

   ![](assets/sms-genai-3.png){zoomable=&quot;yes&quot;}

1. 提示就绪后，单击 **[!UICONTROL 生成]**.

1. 浏览生成的页面 **[!UICONTROL 变体]** 并单击 **[!UICONTROL 预览]** 以查看所选变体的全屏版本。

1. 导航至 **[!UICONTROL 优化]** 内的选项 **[!UICONTROL 预览]** 窗口访问其他自定义功能并微调变体到您的首选项：

   * **[!UICONTROL 用作参考内容]**：所选变量将用作生成其他结果的参考内容。

   * **[!UICONTROL 重新短语]**：AI Assistant可以通过不同的方式重新表述您的消息，保持您写作的新鲜度并吸引各种受众。

   * **[!UICONTROL 使用更简单的语言]**：利用AI Assistant简化您的语言，确保为更广泛的受众提供清晰易用的功能。

   ![](assets/sms-genai-4.png){zoomable=&quot;yes&quot;}

1. 单击 **[!UICONTROL 选择]** 找到相应的内容后。

   您还可以为内容启用试验。 [了解详情](generative-experimentation.md)

1. 插入个性化字段，以根据用户档案数据自定义短信内容。 [详细了解内容个性化](../personalization/personalize.md)

1. 定义消息内容后，单击 **[!UICONTROL 模拟内容]** 按钮来控制渲染，并使用测试用户档案检查个性化设置。 [了解详情](../personalization/personalize.md)

定义内容、受众和计划后，便可以准备短信营销活动。 [了解详情](../campaigns/review-activate-campaign.md)

>[!TAB 文本生成]

1. 创建和配置短信营销活动后，单击 **[!UICONTROL 编辑内容]**.

   有关如何配置短信促销活动的更多信息，请参阅 [此页面](../sms/create-sms.md).

1. 填写 **[!UICONTROL 基本详细信息]** 您的营销活动。 完成后，单击 **[!UICONTROL 编辑内容]**.

1. 根据需要个性化短信消息。 [了解详情](../sms/create-sms.md)

1. 访问 **[!UICONTROL 使用AI助手编辑文本]** 菜单旁边的 **[!UICONTROL 消息]** 字段。

   ![](assets/sms-text-genai-1.png){zoomable=&quot;yes&quot;}

1. 启用 **[!UICONTROL 使用参考内容]** AI助手选项，用于根据您的营销活动内容、名称和选定的受众来个性化新内容。

   您的提示必须始终与特定上下文关联。

1. 通过描述您要在 **[!UICONTROL 提示]** 字段。

   如果您在制作提示时需要帮助，请访问 **[!UICONTROL 提示库]** 其中提供了多种提示性想法来改进您的营销活动。

   ![](assets/sms-text-genai-1.png){zoomable=&quot;yes&quot;}

1. 选择 **[!UICONTROL 上传品牌资产]** 添加任何品牌资产，其中包含可为AI助手提供其他上下文的内容。

1. 使用不同的选项定制提示：

   * **[!UICONTROL 沟通策略]**：为生成的文本选择所需的通信方法。
   * **[!UICONTROL 语言]**：选择变体内容的语言。
   * **[!UICONTROL 色调]**：确保文本适合您的受众和用途。
   * **[!UICONTROL 长度]**：使用范围滑块选择内容的长度。

   ![](assets/sms-text-genai-3.png){zoomable=&quot;yes&quot;}

1. 提示就绪后，单击 **[!UICONTROL 生成]**.

1. 浏览生成的页面 **[!UICONTROL 变体]** 并单击 **[!UICONTROL 预览]** 以查看所选变体的全屏版本。

1. 导航至 **[!UICONTROL 优化]** 内的选项 **[!UICONTROL 预览]** 窗口访问其他自定义功能并微调变体到您的首选项：

   * **[!UICONTROL 用作参考内容]**：所选变量将用作生成其他结果的参考内容。

   * **[!UICONTROL 重新短语]**：AI Assistant可以通过不同的方式重新表述您的消息，保持您写作的新鲜度并吸引各种受众。

   * **[!UICONTROL 使用更简单的语言]**：利用AI Assistant简化您的语言，确保为更广泛的受众提供清晰易用的功能。

   ![](assets/sms-text-genai-4.png){zoomable=&quot;yes&quot;}

1. 单击 **[!UICONTROL 选择]** 找到相应的内容后。

   您还可以为内容启用试验。 [了解详情](generative-experimentation.md)

1. 插入个性化字段，以根据用户档案数据自定义短信内容。 [详细了解内容个性化](../personalization/personalize.md)

1. 定义消息内容后，单击 **[!UICONTROL 模拟内容]** 按钮来控制渲染，并使用测试用户档案检查个性化设置。

定义内容、受众和计划后，便可以准备短信营销活动。 [了解详情](../campaigns/review-activate-campaign.md)

>[!ENDTABS]
