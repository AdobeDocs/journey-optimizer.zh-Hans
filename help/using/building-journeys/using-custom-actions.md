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
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Sw-hR0cfAG8Lk8YbhJKj53UqG-er2bC3-7Ijih0PF44
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: e0eb8757-182f-49f3-94a4-1587d16f5094id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 20%

---

# 使用自定义操作 {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="自定义操作"
>abstract="通过自定义操作，您可以配置第三方系统的连接以发送消息或 API 调用。 可以使用任何提供商的任何服务配置操作，这些服务可以通过具有 JSON 格式有效负载的 REST API 调用。"

使用自定义操作启用与第三方系统的连接，以发送消息或API调用。 可以使用任何提供商的任何服务配置操作，这些服务可以通过具有 JSON 格式有效负载的 REST API 调用。

在[此部分](../action/action.md)中了解自定义操作的详细信息。

了解如何在[此页面](../action/about-custom-action-configuration.md)上创建和配置自定义操作。

了解如何在[此页面](../action/action-response.md)上使用自定义操作的API调用响应进行个性化。

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

![具有动态参数映射的自定义操作URL配置](assets/journey-custom-action-url.png)

### 标头和查询参数 {#headers}

**[!UICONTROL URL配置]**&#x200B;部分显示动态标头和查询参数字段，但不显示常量字段。 在操作配置屏幕中，动态标头和查询参数字段被定义为变量。 [了解详情](../action/about-custom-action-configuration.md#url-configuration)

要指定动态标题和查询参数字段的值，请在字段内或铅笔图标上单击，然后选择所需字段。

自定义操作中的![动态标头字段配置](assets/journey-dynamicheaderfield.png)

## 操作参数

在&#x200B;**[!UICONTROL 操作参数]**&#x200B;部分中，您将看到定义为&#x200B;_&quot;变量&quot;_&#x200B;的消息参数。 对于这些参数，您可以定义从何处获取此信息（例如：事件、数据源）、手动传递值或针对高级用例使用高级表达式编辑器。 高级用例可以是数据操作和其他功能使用。 请参见[此页面](expression/expressionadvanced.md)。

