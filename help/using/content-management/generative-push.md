---
solution: Journey Optimizer
product: journey optimizer
title: 使用AI助手生成推送
description: 开始使用AI助手生成推送内容
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta 版" type="Informative"
hide: true
hidefromtoc: true
exl-id: a9f9d8af-c762-4038-8bbc-bbd519e0ef3a
source-git-commit: b62f8954e09f50896ad5e70784c5a93943617e85
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 6%

---

# 使用AI助手生成推送 {#generative-push}

>[!BEGINSHADEBOX]

**目录**

* [AI 助手入门](gs-generative.md)
* [使用 AI 助手生成电子邮件](generative-email.md)
* [使用 AI 助手生成短信](generative-sms.md)
* 使用AI助手生成推送
* [使用AI助手进行内容试验](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!NOTE]
>
>在开始使用此功能之前，请阅读相关内容 [护栏和限制](gs-generative.md#generative-guardrails).

创建消息并对消息进行个性化后，使用Adobe Journey Optimizer中的AI助手将推送通知内容提升到新的水平。

浏览以下选项卡，了解如何使用Journey Optimizer中的AI助手。

>[!BEGINTABS]

>[!TAB 完全推送生成]

在此特定示例中，了解如何使用AI Assistant发送吸引人的推送通知。

执行以下步骤：

1. 创建和配置推送通知活动后，单击 **[!UICONTROL 编辑内容]**.

   有关如何配置推送通知活动的更多信息，请参阅 [此页面](../push/create-push.md).

1. 填写 **[!UICONTROL 基本详细信息]** 您的营销活动。 完成后，单击 **[!UICONTROL 编辑内容]**.

1. 根据需要个性化您的推送通知。 [了解详情](../push/design-push.md)

1. 访问 **[!UICONTROL 显示AI助手]** 菜单。

   ![](assets/push-genai-full-1.png){zoomable=&quot;yes&quot;}

1. 启用 **[!UICONTROL 使用原始内容]** AI助手选项，用于根据您的营销活动内容、名称和选定的受众来个性化新内容。

   您的提示必须始终与特定上下文关联。

1. 通过描述您要在 **[!UICONTROL 提示]** 字段。

   如果您在制作提示时需要帮助，请访问 **[!UICONTROL 提示库]** 其中提供了多种提示性想法来改进您的营销活动。

   ![](assets/push-genai-full-2.png){zoomable=&quot;yes&quot;}

1. 选择 **[!UICONTROL 上传品牌资产]** 添加任何品牌资产，其中包含可为AI助手提供其他上下文的内容。

1. 选择要生成的字段： **[!UICONTROL 标题]** 和/或 **[!UICONTROL 消息]**.

1. 使用不同的选项定制提示：

   * **[!UICONTROL 沟通策略]**：为生成的文本选择最合适的通信样式。
   * **[!UICONTROL 语言]**：选择您希望生成内容的语言。
   * **[!UICONTROL 色调]**：电子邮件的基调应该会引起受众的共鸣。 无论您是要提供信息、好玩还是具有说服力，AI Assistant都可以相应地调整消息。

   ![](assets/push-genai-full-3.png){zoomable=&quot;yes&quot;}

1. 提示就绪后，单击 **[!UICONTROL 生成]**.

1. 浏览生成的页面 **[!UICONTROL 变体]** 并单击 **[!UICONTROL 预览]** 以查看所选变体的全屏版本。

1. 导航至 **[!UICONTROL 优化]** 内的选项 **[!UICONTROL 预览]** 用于访问其他自定义功能的窗口：

   * **[!UICONTROL 用作参考内容]**：所选变量将用作生成其他结果的参考内容。

   * **[!UICONTROL 重新短语]**： AI助手可以通过不同的方式重新声明您的消息，以使您的撰写保持新鲜，并吸引各种受众。

   * **[!UICONTROL 使用简单语言]**：利用AI Assistant简化您的语言，确保为更广泛的受众提供清晰易用的功能。

   ![](assets/push-genai-full-4.png){zoomable=&quot;yes&quot;}

1. 单击 **[!UICONTROL 选择]** 找到相应的内容后。

   您还可以为内容启用试验。 [了解详情](generative-experimentation.md)

1. 插入个性化字段，以根据用户档案数据自定义电子邮件内容。 然后，单击 **[!UICONTROL 模拟内容]** 按钮来控制渲染，并使用测试用户档案检查个性化设置。 [了解详情](../personalization/personalize.md)

定义内容、受众和计划后，便可以准备推送营销活动。 [了解详情](../campaigns/review-activate-campaign.md)

>[!TAB 文本生成]

在此特定示例中，了解如何将AI助手用于特定内容。 执行以下步骤：

1. 创建和配置推送通知活动后，单击 **[!UICONTROL 编辑内容]**.

   有关如何配置推送活动的更多信息，请参阅 [此页面](../push/create-push.md).

1. 填写 **[!UICONTROL 基本详细信息]** 您的营销活动。 完成后，单击 **[!UICONTROL 编辑内容]**.

1. 根据需要个性化您的推送通知。 [了解详情](../push/design-push.md)

1. 访问 **[!UICONTROL 显示AI助手]** 菜单旁边的 **[!UICONTROL 标题]** 或 **[!UICONTROL 消息]** 字段。

   ![](assets/push-genai-1.png){zoomable=&quot;yes&quot;}

1. 启用 **[!UICONTROL 使用参考内容]** AI助手选项，用于根据您的营销活动内容、名称和选定的受众来个性化新内容。

   您的提示必须始终与特定上下文关联。

1. 通过描述您要在 **[!UICONTROL 提示]** 字段。

   如果您在制作提示时需要帮助，请访问 **[!UICONTROL 提示库]** 其中提供了多种提示性想法来改进您的营销活动。

   ![](assets/push-genai-2.png){zoomable=&quot;yes&quot;}

1. 选择 **[!UICONTROL 上传品牌资产]** 添加任何品牌资产，其中包含可为AI助手提供其他上下文的内容。

   ![](assets/push-genai-3.png){zoomable=&quot;yes&quot;}

1. 使用不同的选项定制提示：

   * **[!UICONTROL 沟通策略]**：为生成的文本选择最合适的通信样式。
   * **[!UICONTROL 语言]**：选择您希望生成内容的语言。
   * **[!UICONTROL 色调]**：电子邮件的基调应该会引起受众的共鸣。 无论您是要提供信息、好玩还是具有说服力，AI Assistant都可以相应地调整消息。
   * **[!UICONTROL 长度]**：使用范围滑块选择内容的长度。

   ![](assets/push-genai-4.png){zoomable=&quot;yes&quot;}

1. 提示就绪后，单击 **[!UICONTROL 生成]**.

1. 浏览生成的页面 **[!UICONTROL 变体]** 并单击 **[!UICONTROL 预览]** 以查看所选变体的全屏版本。

1. 导航至 **[!UICONTROL 优化]** 内的选项 **[!UICONTROL 预览]** 用于访问其他自定义功能的窗口：

   * **[!UICONTROL 用作参考内容]**：所选变量将用作生成其他结果的参考内容。

   * **[!UICONTROL 详细]**：AI助手可以帮助您展开特定主题，提供其他详细信息以便更好地了解和参与。

   * **[!UICONTROL 总结]**：过长的信息可能会使电子邮件收件人过载。 使用AI Assistant将要点整合为清晰、简洁的摘要，以吸引注意并鼓励他们进一步阅读。

   * **[!UICONTROL 重新短语]**：AI Assistant可以通过不同的方式重新表述您的消息，保持您写作的新鲜度并吸引各种受众。

   * **[!UICONTROL 使用更简单的语言]**：利用AI Assistant简化您的语言，确保为更广泛的受众提供清晰易用的功能。

   ![](assets/push-genai-5.png){zoomable=&quot;yes&quot;}

1. 单击 **[!UICONTROL 选择]** 找到相应的内容后。

   您还可以为内容启用试验。 [了解详情](generative-experimentation.md)

1. 插入个性化字段，以根据用户档案数据自定义电子邮件内容。 然后，单击 **[!UICONTROL 模拟内容]** 按钮来控制渲染，并使用测试用户档案检查个性化设置。 [了解详情](../personalization/personalize.md)

定义内容、受众和计划后，便可以准备推送营销活动。 [了解详情](../campaigns/review-activate-campaign.md)

>[!ENDTABS]
