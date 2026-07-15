---
title: 测试您的自定义渠道
description: 了解在激活之前，如何在Adobe Journey Optimizer中测试连接、模拟内容以及验证自定义渠道消息。
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 2%

---


# 测试您的自定义渠道 {#test-custom-channel}

在激活使用自定义渠道的历程或营销活动之前，请验证您的端点是否可访问、身份验证是否有效以及个性化令牌是否可以为目标用户档案正确解析。

## 从Channel Builder测试连接 {#test-connection}

当自定义渠道处于&#x200B;**[!UICONTROL 草稿]**&#x200B;状态时，请使用渠道生成器中的&#x200B;**[!UICONTROL 测试]**&#x200B;按钮向您的端点发送测试请求并验证端到端连接，然后再激活。 [了解详情](create-custom-channel.md#test-connection)

此测试确认：

* 终结点可从[!DNL Journey Optimizer]的出站IP访问。
* 配置的身份验证凭据是否有效。
* 终结点返回HTTP 2xx响应。

检查外部系统的日志，确认已收到测试请求，带有预期的标头和负载结构。

## 使用测试轮廓模拟内容 {#simulate-content}

**[!UICONTROL 模拟内容]**&#x200B;功能针对测试配置文件解析个性化表达式，以便您能够在交付任何实际消息之前检查将会发送的确切有效负载。

1. 在历程操作或营销活动版本屏幕中，单击&#x200B;**[!UICONTROL 模拟内容]**。

1. 单击&#x200B;**[!UICONTROL 添加测试配置文件]**&#x200B;并选择一个或多个配置文件。 [了解如何创建测试轮廓。](../audience/creating-test-profiles.md)

1. 在预览面板中查看已解析的有效负载。 对于每个测试配置文件，请验证：

   * 所有个性化令牌（例如`{{profile.person.name.firstName}}`）已被配置文件中的预期值替换。
   * 没有未解析的令牌剩余（显示为空字符串或文本`{{...}}`语法）。
   * 已填充必需的有效负载字段。
   * 辅助函数生成预期的格式化输出。

>[!TIP]
>
>使用表示不同受众区段的多个配置文件进行测试，以捕获边缘情况 — 例如，配置文件缺少可选属性、非拉丁字符集或个性化字段中的空值。

## 发送校样 {#send-proof}

要在激活之前验证端到端投放，请向一组测试收件人发送验证：

1. 在&#x200B;**[!UICONTROL 模拟内容]**&#x200B;面板中，切换到&#x200B;**[!UICONTROL 发送校样]**&#x200B;选项卡。

1. 添加要使用的配置文件。 您可以上载包含未在[!DNL Journey Optimizer]中定义为测试用户档案的用户档案的CSV文件。

1. 单击&#x200B;**[!UICONTROL 发送校样]**。 [!DNL Journey Optimizer]使用每个所选配置文件的个性化有效负载调用您的外部端点。

1. 检查您的外部系统，确认已收到验证负载。 对于消息渠道（例如，微信或Kakao Talk），验证消息是否显示在目标设备或消息传递应用程序上。

使用与电子邮件验证相同的验证模式显示验证结果：在发送验证之前显示必填字段、类型不匹配和架构验证错误。

了解有关在[营销活动](../campaigns/create-campaign.md#send-proof)和[历程](../building-journeys/testing-the-journey.md)中发送校样的更多信息。

## 在历程测试模式下测试 {#test-journey}

要进行端到端历程验证，请在&#x200B;**[!UICONTROL 测试模式]**&#x200B;下激活历程：

1. 在历程画布中，单击右上角区域中的&#x200B;**[!UICONTROL 测试]**。

1. 为受众触发的历程配置触发器事件或选择测试用户档案。

1. 单击&#x200B;**[!UICONTROL 触发事件]**&#x200B;或让配置文件通过&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动进入。

1. 观察画布中的流动。 当配置文件到达自定义渠道操作节点时，[!DNL Journey Optimizer]会使用个性化有效负载调用您的外部端点。

1. 检查外部系统的日志，确认已正确收到请求。

1. 完成后单击&#x200B;**[!UICONTROL 停止测试]**。

了解有关在[测试模式](../building-journeys/testing-the-journey.md)中测试历程的更多信息。

## 模拟历程 {#simulate-journey}

[!DNL Journey Optimizer]的&#x200B;**模拟**&#x200B;模式允许您使用模拟用户（类似临时个人资料的实体，不会在Adobe Experience Platform中持续存在）端到端地验证历程，而无需预先创建测试个人资料。

对于自定义渠道，模拟解析个性化表达式并呈现每个模拟用户的负载预览，因此您可以验证在内容上线之前是否可以交付正确的内容。

要使用自定义渠道模拟历程，请执行以下操作：

1. 在历程画布中，单击右上角区域中的&#x200B;**[!UICONTROL 模拟]**。

1. 手动添加模拟用户，或使用AI支持的&#x200B;**[!UICONTROL 快速模拟]**&#x200B;选项生成模拟用户。

1. 配置任何所需的进入事件，然后触发模拟用户通过历程。

1. 当模拟用户到达自定义渠道操作节点时，在预览面板中检查已解析的有效负载以确认个性化令牌和有效负载结构正确。

>[!NOTE]
>
>模拟适用于草稿和实时历程，并使用不计入用户档案配额或真实端点调用的临时模拟用户。

[了解有关历程模拟的更多信息](../building-journeys/simulate-journey-gs.md)

## 预激活核对清单 {#checklist}

在激活历程或营销策划之前，请确认以下事项：

* Channel Builder中的连接测试成功（端点可访问，身份验证有效）。
* 模拟有效负载显示所有测试配置文件的预期值。
* 有效负载中不会保留未解析的个性化令牌。
* 已填充所有必需的有效负载字段。
* 您的外部系统正确发送和接收了校样。
* 历程操作活动（如果已配置）上的错误路径可按预期处理失败方案。

测试完成后，继续激活。 [了解如何操作](create-custom-experience.md#activate)
