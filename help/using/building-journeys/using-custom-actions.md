---
solution: Journey Optimizer
product: journey optimizer
title: 使用自定义操作
description: 了解如何使用自定义操作
feature: Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 操作，自定义， API，历程，配置，服务
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 25%

---

# 使用自定义操作 {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="自定义操作"
>abstract="通过自定义操作，您可以配置第三方系统的连接以发送消息或 API 调用。可以使用任何提供商的任何服务配置操作，这些服务可以通过具有 JSON 格式有效负载的 REST API 调用。"

通过自定义操作，您可以配置第三方系统的连接以发送消息或 API 调用。可以使用任何提供商的任何服务配置操作，这些服务可以通过具有 JSON 格式有效负载的 REST API 调用。

## 同意和数据治理 {#privacy}

在Journey Optimizer中，您可以将数据治理和同意策略应用于自定义操作，以防止将特定字段导出到第三方系统，或排除未同意接收电子邮件、推送或短信通信的客户。 有关更多信息，请参阅以下页面：

* [数据治理](../action/action-privacy.md).
* [同意](../action/consent.md).

## URL 配置

的配置窗格 **自定义操作** 活动显示为自定义操作配置的URL配置参数和身份验证参数。 您不能在历程中设置URL的静态部分，而应在自定义操作的全局配置中设置。 [了解详情](../action/about-custom-action-configuration.md)。

### 动态路径

如果URL包含动态路径，请在 **[!UICONTROL 路径]** 字段。

要连接字段和纯文本字符串，请使用高级表达式编辑器中的字符串函数或加号(+)。 将纯文本字符串用单引号(&#39;)或双引号(&#39;&#39;)括起来。 [了解详情](expression/expressionadvanced.md)。

下表显示了一个配置示例：

| 字段 | 值 |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| 路径 | `The id of marketingCampaign + '/messages'` |

连接的URL具有以下形式：

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### 标头和查询参数 {#headers}

此 **[!UICONTROL URL配置]** 部分显示动态标题和查询参数字段，但不显示常量字段。 在操作配置屏幕中，动态标头和查询参数字段被定义为变量。 [了解详情](../action/about-custom-action-configuration.md#url-configuration)

要指定动态标题和查询参数字段的值，请在字段内或铅笔图标上单击，然后选择所需的字段。

![](assets/journey-dynamicheaderfield.png)

## 操作参数

在 **[!UICONTROL 操作参数]** 部分中，您将看到消息参数定义为 _&quot;Variable&quot;_. 对于这些参数，您可以定义从何处获取此信息（例如：事件、数据源）、手动传递值或针对高级用例使用高级表达式编辑器。 高级用例可以是数据操作和其他功能使用。 请参阅此 [页面](expression/expressionadvanced.md).

**相关主题**

[配置操作](../action/about-custom-action-configuration.md)
