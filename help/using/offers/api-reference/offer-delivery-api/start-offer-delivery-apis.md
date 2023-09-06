---
title: 优惠投放 API 入门
description: 了解可用于提供个性化优惠的API的更多信息。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: ccc3ad2b186a64b9859a5cc529fe0aefa736fc00
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 4%

---

# 优惠投放 API 入门 {#about-decisioning-apis}

您可以使用以下任一方式交付优惠： **决策** 或 **边缘决策** API。 此外， **批量决策** API允许您在一次调用中将选件交付给给定受众中的所有配置文件。 受众中每个用户档案的选件内容都放在Adobe Experience Platform数据集中，可用于自定义批量工作流。

在此页面中，您可以找到随提供的有关特定功能的信息。 **决策** 和 **边缘决策** API。 虽然这两种方法都允许您向客户提供选件，但我们建议使用 **边缘决策** API适用于入站用例，并确保提高平台的延迟和吞吐量。


有关如何使用API的更多信息，请参阅以下章节：
* [Decisioning API](decisioning-api.md)
* [Edge Decisioning API](edge-decisioning-api.md)
* [Batch Decisioning API](batch-decisioning-api.md)

## Edge Decisioning API功能 {#edge}

**体验事件和决策请求的独特请求**

借助Edge Decisioning API，您可以将体验事件本身与决策请求一起发送到一个请求中，而不是发送两个不同的请求。

例如，如果客户访问您的网站，则请求将包括体验事件（客户对页面的访问），并获取选件以填充所访问的页面。

**将上下文数据存储到Adobe Experience Platform**

上下文数据是指您仅在需要恢复选件时知道的数据。 例如，所购买物品的颜色、购买时的天气等。

使用Edge Decisioning API请求传递上下文数据时，数据会存储在Adobe Experience Platform配置文件中，以便将来重复使用。

>[!NOTE]
>
>为了存储上下文数据，您需要配置专用的XDM架构。

## 决策API功能 {#decisioning}

以下列出的功能仅在Decisioning API中可用。 如果您需要利用其中一个应用程序来满足您的要求，请使用Decisioning API。 否则，我们建议使用Edge Decisioning API。

* **体验事件**：利用体验事件构建决策规则。
* **选件内容和特征**：您可以选择不使用专用选项返回选件的内容和特征。
* **优惠元数据**：启用一个选项以返回选件的元数据。
* **合并策略**：在请求中使用与沙盒关联的合并策略不同的合并策略。
* **决策事件和频率封顶**：阻止将决策事件计数为所发生的任何频率上限。
* **复制建议**：启用一个不删除重复建议的选项。
