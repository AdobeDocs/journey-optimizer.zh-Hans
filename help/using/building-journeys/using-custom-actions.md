---
solution: Journey Optimizer
product: journey optimizer
title: 使用自定义操作
description: 了解如何使用自定义操作
feature: Journeys, Actions, Custom Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 操作，自定义， API，历程，配置，服务
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 20%

---

# 使用自定义操作 {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="自定义操作"
>abstract="通过自定义操作，您可以配置第三方系统的连接以发送消息或 API 调用。可以使用任何提供商的任何服务配置操作，这些服务可以通过具有 JSON 格式有效负载的 REST API 调用。"

使用自定义操作启用与第三方系统的连接，以发送消息或API调用。 可以使用任何提供商的任何服务配置操作，这些服务可以通过具有 JSON 格式有效负载的 REST API 调用。

在[此部分](../action/action.md)中了解自定义操作的详细信息。

了解如何在[此页面](../action/about-custom-action-configuration.md)上创建和配置自定义操作。

## 同意和数据治理 {#privacy}

在Journey Optimizer中，您可以将数据治理和同意策略应用于自定义操作，以防止将特定字段导出到第三方系统，或排除未同意接收电子邮件、推送或短信通信的客户。 有关更多信息，请参阅以下页面：

* [数据管理](../action/action-privacy.md)。
* [同意](../action/consent.md)。

## URL 配置

**自定义操作**&#x200B;活动的配置窗格显示针对自定义操作配置的URL配置参数和身份验证参数。 您无法在历程中设置URL的静态部分，但可以在自定义操作的全局配置中设置。 [了解详情](../action/about-custom-action-configuration.md)。

### 动态路径

如果URL包含动态路径，请在&#x200B;**[!UICONTROL 路径]**&#x200B;字段中指定路径。

要连接字段和纯文本字符串，请使用高级表达式编辑器中的字符串函数或加号(+)。 将纯文本字符串用单引号(&#39;)或双引号(&#39;&#39;)括起来。 [了解详情](expression/expressionadvanced.md)。

下表显示了一个配置示例：

| 字段 | 值 |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| 路径 | `The _id + '/messages'` |

连接的URL具有以下形式：

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;ID>`/messages`

![](assets/journey-custom-action-url.png)

### 标头和查询参数 {#headers}

**[!UICONTROL URL配置]**&#x200B;部分显示动态标头和查询参数字段，但不显示常量字段。 在操作配置屏幕中，动态标头和查询参数字段被定义为变量。 [了解详情](../action/about-custom-action-configuration.md#url-configuration)

要指定动态标题和查询参数字段的值，请在字段内或铅笔图标上单击，然后选择所需字段。

![](assets/journey-dynamicheaderfield.png)

## 操作参数

在&#x200B;**[!UICONTROL 操作参数]**&#x200B;部分中，您将看到定义为&#x200B;_&quot;变量&quot;_&#x200B;的消息参数。 对于这些参数，您可以定义从何处获取此信息（例如：事件、数据源）、手动传递值或针对高级用例使用高级表达式编辑器。 高级用例可以是数据操作和其他功能使用。 请参阅此[页面](expression/expressionadvanced.md)。

