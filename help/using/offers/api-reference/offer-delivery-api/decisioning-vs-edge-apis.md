---
title: 决策和Edge决策API
description: 决策管理是服务和UI程序的集合，使营销人员能够使用业务逻辑和决策规则跨渠道和应用程序创建和提供最终用户个性化选件体验。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: dc56f2dc461a11c9706b3572ccd4b9e0feb6f055
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 1%

---

# 决策和Edge决策API {#about-decisioning-apis}

您可以使用 **决策** 或 **Edge Decisioning** API。

在本页中，您将找到有关每个API可用特定功能的信息。 虽然这两种方法都允许您向客户交付选件，但我们建议您使用 **Edge Decisioning** 尽可能针对入站用例使用API，并确保平台上的延迟和吞吐量得到改善。

|  | 请求数/秒 | 延迟 |
|---|---|---|
| 决策API | 2000年 | &lt;500 毫秒 |
| Edge Decisioning API | 5000 | &lt;250 毫秒 |

有关如何使用API的更多信息，请参阅以下章节：
* [决策API](decisioning-api.md)
* [Edge Decisioning API](edge-decisioning-api.md)

## Edge Decisioning API功能 {#edge}

**对体验事件和决策请求的独特请求**

借助Edge Decisioning API，您可以在一个请求中发送体验事件本身以及决策请求，而不是发送两个不同的请求。

例如，如果客户访问您的网站，则请求将包含体验事件（客户对页面的访问），并获取回选件以填充访问的页面。

**将上下文数据存储到Adobe Experience Platform**

上下文数据是指您仅在希望返回选件时才知道的数据。 例如，购买文章的颜色、购买时的天气等。

通过Edge Decisioning API请求传递上下文数据时，数据会存储到Adobe Experience Platform配置文件中，以便将来重复使用。

>[!NOTE]
>
>要存储上下文数据，您需要配置专用XDM架构。

## 决策API功能 {#decisioning}

以下列出的功能仅适用于Decisioning API。 如果您需要利用其中一个解决方案来满足您的要求，请使用决策API。 否则，我们建议使用Edge Decisioning API。

* **体验事件**:利用体验事件构建决策规则。
* **选件内容和特性**:您可以选择不使用专用选项返回选件的内容和特征。
* **选件元数据**:启用一个选项以返回选件的元数据。
* **合并策略**:在您的请求中使用与沙盒关联的合并策略。
* **决策事件和频率上限**:块决策事件不会被发生的任何频率上限计数。
* **重复命题**:启用不删除重复命题的选项。
