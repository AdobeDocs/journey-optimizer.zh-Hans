---
solution: Journey Optimizer
product: journey optimizer
title: 有关集成的常见问题解答
description: 有关Journey Optimizer与消息中的外部数据和内容集成的常见问题解答。
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: 集成，常见问题解答，外部数据，个性化
hide: true
source-git-commit: e4c298fb1c47501920a27a93b43878327b6c5861
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 2%

---

# 有关集成的常见问题解答 {#vendor-integration-faq}

>[!BEGINSHADEBOX]

目录：

* [使用集成](integrations.md)
* [供应商集成入门](vendor-integration-gs.md)
* [可用的供应商](vendor-integration.md)
* **[常见问题解答](vendor-integration-faq.md)**

>[!ENDSHADEBOX]

以下是有关Adobe Journey Optimizer中&#x200B;**集成**&#x200B;的常见问题解答。


## 快速入门

+++ 集成在Journey Optimizer中做什么？

它将外部数据源连接到Journey Optimizer，以便您可以将内容和数据从第三方系统拉入到营销活动和历程中，并使用该数据个性化消息。

➡️ [了解有关集成概述的更多信息](integrations.md)

+++

+++ 谁配置集成，以及谁在内容中使用集成？

管理员创建和激活技术配置（**[!UICONTROL 配置]** > **[!UICONTROL 集成]** > **[!UICONTROL 管理]** > **[!UICONTROL 创建集成]**）。 营销人员在文本或HTML组件中使用&#x200B;**[!UICONTROL 添加个性化]**，打开&#x200B;**[!UICONTROL 集成]**，选择活动集成，并映射属性。

➡️ [了解有关管理员和营销人员工作流的更多信息](integrations.md)

+++

+++ 我该如何作为管理员在UI中创建或管理集成？

转到左侧菜单中的&#x200B;**[!UICONTROL 配置]**&#x200B;部分，从&#x200B;**[!UICONTROL 集成]**&#x200B;卡中打开&#x200B;**[!UICONTROL 管理]**，然后选择&#x200B;**[!UICONTROL 创建集成]**。

➡️ [了解有关创建集成的更多信息](integrations.md#configure)

+++

+++ 集成的常见用例有哪些？

示例包括忠诚度系统中的奖励积分、产品价格信息、推荐引擎中的推荐以及物流更新（如投放状态）。

➡️ [了解有关第三方系统示例数据的更多信息](integrations.md)

➡️ [了解有关供应商集成示例的更多信息](vendor-integration.md)

+++

## 配置

+++ 如何以管理员身份在高级别配置集成？

请提供名称和描述、API端点URL（可以选择包含路径变量）、路径模板值、**[!UICONTROL GET]**&#x200B;或&#x200B;**[!UICONTROL POST]**、可选标头和查询参数、身份验证方法、策略设置（例如超时和可选缓存或重试）、映射字段的示例JSON响应，然后运行&#x200B;**[!UICONTROL 发送测试连接]**&#x200B;和&#x200B;**[!UICONTROL 激活]**（如果有效）。

➡️ [了解有关集成配置的更多信息](integrations.md#configure)

+++

+++ 支持哪些身份验证类型？

这些身份验证类型可用： **[!UICONTROL 无身份验证]**、**[!UICONTROL API密钥]**、**[!UICONTROL 基本身份验证]**&#x200B;和&#x200B;**[!UICONTROL OAuth 2.0]**（在适用的情况下，带有OAuth的有效负载配置）。

➡️ [了解有关身份验证类型的更多信息](integrations.md#configure)

+++

+++ 响应有效负载步骤用于什么？

粘贴示例JSON响应，以便系统检测数据类型，并且您可以选择在消息中公开哪些字段进行个性化。 您可以限制营销人员在创作期间可用的字段。

➡️ [了解有关响应有效负载映射的更多信息](integrations.md#configure)

+++

+++ 营销人员如何向消息添加集成？

在营销活动或历程内容中，对文本或HTML组件使用&#x200B;**[!UICONTROL 添加个性化]**，转到&#x200B;**[!UICONTROL 集成]**，选择集成，然后保存。 利用个性化编辑器中的Pills模式，您可以将值映射到配置中的变量（例如URL中的标头或查询参数或路径变量）。

➡️ [了解有关集成个性化的更多信息](integrations.md#personalization)

+++

## 功能和用例

+++ 我可以在历程和营销活动中使用集成吗？

可以。 在当前产品限制内，该功能可用于&#x200B;**出站**&#x200B;渠道（例如电子邮件、短信和推送）的历程和营销活动。

➡️ [了解有关历程和营销活动的更多信息](integrations.md#limitations)

+++

+++ 我可以在可重用片段中使用集成吗？

集成功能在片段中是&#x200B;**不支持**。 在产品支持的营销活动和历程消息内容中使用集成。

➡️ [了解有关片段和Beta版限制的更多信息](integrations.md#limitations)

+++

## 限制

+++ 哪些渠道支持集成？

支持&#x200B;**出站**&#x200B;渠道（例如电子邮件、短信和推送）。

➡️ [了解有关受支持渠道的更多信息](integrations.md#limitations)

+++

+++ 支持哪些API响应格式？

对于API调用响应，字段映射支持&#x200B;**JSON**。 原始二进制图像输出和非JSON格式不适用于此工作流。

➡️ [了解有关JSON和响应格式的更多信息](integrations.md#limitations)

+++

+++ 我可以连接到哪些API模式？

支持针对特定内容的&#x200B;**检索** API。 此集成模型不支持&#x200B;**列表** API（宽列表或分页模式）。

➡️ [了解有关检索与列出API的更多信息](integrations.md#limitations)

+++

## 权限和相关功能

+++ 配置集成需要什么权限？

配置是&#x200B;**[!UICONTROL 配置]** > **[!UICONTROL 集成]**&#x200B;下的管理员工作流。 确切的权限名称取决于贵组织的Admin Console和Journey Optimizer产品配置文件。 请与管理员或Adobe代表确认。

➡️ [了解有关集成配置位置的更多信息](integrations.md#configure)

+++

+++ 集成是否会取代Experience Platform源的Adobe Journey Optimizer连接器？

不是。 **集成**&#x200B;用于您从API驱动的消息内容中的个性化字段。 **源**&#x200B;和其他数据摄取功能有不同的用途（例如，批量数据摄取和配置文件扩充）。 将每种功能用于其目标范围。

➡️ [了解更多有关集成的用途](integrations.md)

➡️ [了解有关Experience Platform源的更多信息](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=zh-Hans){target="_blank"}

+++

## 故障排除

+++ 为什么测试连接失败或保持无效？

验证端点URL、HTTP方法、路径模板、标头和查询参数、身份验证以及策略超时。 调整后使用&#x200B;**[!UICONTROL 发送测试连接]**。 对于有效负载问题，请确保示例反映有效的JSON，并且所选字段与API返回的内容匹配。

➡️ [了解有关测试连接和负载验证的更多信息](integrations.md#configure)

+++

+++ 为什么营销人员在选取器中看不到我的集成？

集成必须在成功测试后&#x200B;**激活**。 当营销人员打开&#x200B;**[!UICONTROL 集成]**&#x200B;时，仅显示活动的集成。 如果集成仍处于草稿或非活动状态，请先完成激活。

➡️ [了解有关测试连接和激活的更多信息](integrations.md#configure)

+++

## 第三方供应商

+++ 哪些供应商示例可用，以及谁负责保护API？

您可以与公开兼容API端点的任何第三方平台集成。 **说明性**&#x200B;供应商模式和配置示例可帮助您为兼容的API建模。 保护端点的责任在于第三方平台和您的团队。

➡️ [了解有关供应商集成过程的更多信息](vendor-integration.md)

+++
