---
solution: Journey Optimizer
product: journey optimizer
title: Integrate Journey Optimizer with external systems
description: Learn the best practices when integrating Journey Optimizer with external systems
feature: Integrations
role: User
level: Beginner
keywords: external, API, optimizer, capping
exl-id: 27859689-dc61-4f7a-b942-431cdf244455
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '1834'
ht-degree: 23%

---

# 与外部系统集成 {#external-systems}

This page presents the different guardrails provided by Journey Optimizer when integrating an external system, as well as best practices: how to optimize the protection of your external system using the capping API, how to configure journey timeout, and how retries work.

Journey Optimizer allows you to configure connections to external systems via [custom data sources](../datasource/about-data-sources.md) and [custom actions](../action/action.md). This allows you, for example, to enrich your journeys with data coming from an external reservation system, or send messages using a third-party system such as Epsilon or Facebook.

When integrating an external system, you can encounter several issues, the system can be slow, can stop responding, or it might not be able to handle a large volume. Journey Optimizer offers several guardrails to protect your system from over-loading.

All external systems are different in terms of performance. You need to adapt the configuration to your use cases.

When Journey Optimizer executes a call to an external API, the technical guardrails are executed as follows:

1. Capping or throttling rules are applied: if the maximum rate is reached, remaining calls are discarded or queued.

1. Timeout and retry: if the capping or throttling rule is fulfilled, Journey Optimizer tries to perform the call until the end of the timeout duration is reached.

>[!TIP]
>
>We recommend leaving at least a one-minute buffer between the external API&#39;s token expiration period and your Journey Optimizer [`cacheDuration` setting](../datasource/external-data-sources.md#custom-authentication-access-token), especially under heavy workloads, to avoid expiration mismatches and 401 errors.

## Capping &amp; throttling APIs {#capping}

### About capping &amp; throttling apis

在配置数据源或操作时，您需要建立与系统的连接，以检索要在历程中使用的其他信息，或者发送消息或 API 调用。

历程 API 支持每秒最多 5,000 个事件，但某些外部系统或 API 的吞吐量可能不同。 To prevent overloading these systems, you can use the **Capping** and **Throttling** APIs to limit the number of events sent per second.

每次按历程执行 API 调用时，它都会通过 API 引擎。 If the limit set in the API is reached, the call is either rejected if you are using the Capping API, or queued for up to 6 hours and processed as soon as possible in the order they were received if you are using the Throttling API.

For example, let&#39;s say that you have defined a capping or throttling rule of 200 calls per second for your external system. 在 10 个不同历程中，系统由自定义操作调用。 如果一个历程每秒收到 300 个调用，则将使用 200 个可用的位置，并丢弃剩余的 100 个调用或将它们排入队列。 由于超出了最大使用率，因此其他 9 个历程将没有任何位置。 此粒度有助于避免使外部系统出现过载和崩溃。

>[!IMPORTANT]
>
>**上限规则**&#x200B;在沙盒级别针对特定端点（调用的 URL）配置，但在全局范围内应用于该沙盒的所有历程。 Capping is available on both data sources and custom actions.
>
>**限制规则**&#x200B;仅在生产沙盒上针对特定端点配置，但在全局范围内应用于所有沙盒中的所有历程。 只能为每个组织使用一个限制配置。 Throttling is only available on custom actions.
>
>The **maxCallsCount** value has to be greater than 1.

For more information on how to work with the APIs, refer to these sections:

* [API 上限](capping.md)
* [API 限制](throttling.md)

A detailed description of the APIs is available in [Adobe Journey Optimizer APIs documentation](https://developer.adobe.com/journey-optimizer-apis/references/journeys-throttling)

### 数据源和自定义操作容量 {#capacity}

对于&#x200B;**外部数据源**，每秒的最大调用数限制为 15。 如果超出此限制，则会根据所使用的 API，丢弃或排入任何其他调用。 联系 Adobe 以将端点包含在允许列表中，这样可以增加专用外部数据源的此限制，但对于公共外部数据源不可以这样操作。 * [了解如何配置数据源](../datasource/about-data-sources.md)。

>[!NOTE]
>
>如果数据源使用的自定义身份验证的端点与数据源使用的端点不同，您需要联系 Adobe 以将该端点也包含在允许列表中。

对于&#x200B;**自定义操作**，您需要评估外部 API 的容量。 例如，如果Journey Optimizer每秒发送1000次调用，而您的系统仅支持每秒200次调用，则您需要定义上限或限制配置，以便您的系统不会饱和。 [了解如何配置操作](../action/action.md)

>[!NOTE]
>
>由于现在支持响应，因此您应该对外部数据源用例使用自定义操作而不是数据源。 有关回应的详细信息，请参阅此[部分](../action/action-response.md)

## 响应缓慢的端点 {#response-time}

当端点的响应时间大于0.75秒时，其自定义操作调用通过专用的&#x200B;**慢速自定义操作服务**&#x200B;而不是默认服务进行路由。

此自定义操作缓慢服务每30秒应用150,000次调用的上限限制。 该限制使用滑动窗口执行，滑动窗口可在该30秒周期内的任何毫秒内开始。 窗口一旦满，则会拒绝其他调用，并出现上限错误。 系统不会等待下一个固定间隔，而是在达到30秒阈值后立即开始设置上限。

由于慢速端点可能会导致管道中所有排队操作出现延迟，因此建议不要为自定义操作配置响应速度较慢的端点。 将此类操作路由到慢速服务有助于保护整体系统性能，并防止其他自定义操作增加延迟。

## 超时和重试 {#timeout}

如果满足上限或限制规则，则应用超时规则。

在每个历程中，您可以定义超时持续时间。 这允许您在调用外部系统时设置最大持续时间。 超时持续时间在历程的属性中配置。 请参见[此页面](../building-journeys/journey-properties.md#timeout_and_error)。

此超时对于所有外部调用（自定义操作和自定义数据源中的外部API调用）都是全局的。 默认情况下，设置为30秒。

在定义的超时持续时间内，Journey Optimizer会尝试调用外部系统。 在第一次调用后，最多可以执行三次重试，直到达到超时持续时间结束为止。 无法更改重试次数。

每次重试使用一个插槽。 如果您的限制为每秒100次调用，并且每个调用需要重试两次，则速率降至每秒30次调用（每个调用使用3个插槽：第一次调用和两次重试）。

超时持续时间值取决于用例。 如果您希望快速发送消息（例如，在客户端进入商店时），则您不希望设置较长的超时。 此外，超时时间越长，放入队列中的项目就越多。 This can greatly impact performance. If Journey Optimizer performs 1000 calls per seconds, keeping 5 or 15 seconds of data can quickly overwhelm the system.

Let&#39;s take an example for a timeout of 5 seconds.

* The first call lasts less than 5 seconds: the call is successful, no retry is performed.
* The first call lasts longer 5 seconds: the call is canceled and there is no retry. It is counted as a timeout error in reporting.
* The first call fails after 2 seconds (the external system returns an error): 3 seconds are left for retries, if capping slots are available.
   * If one of the three retries is successful before the end of the 5 seconds, the call is performed, and there is no error.
   * If the end of the timeout duration is reached during the retries, the call is canceled and counted as a timeout error in reporting.

## 常见问题 {#faq}

You will find below Frequently Asked Questions about integrating Journey Optimizer with external systems.

需要更多信息？ 使用本页底部的反馈选项提出问题，或通过 [Adobe Journey Optimizer 社区](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=zh-hans){target="_blank"}进行联系。

+++ How can I configure a capping or throttling rule? Is there a default rule?

To create capping or throttling rules, please refer to [this section](../configuration/external-systems.md#capping). By default, there is no throttling rule but a capping limit of 300,000 calls over one minute defined for all custom actions, per host and per sandbox. “每台主机”限制适用于域级别（例如，example.com）。 此限制是根据客户使用情况设置的，用于保护自定义操作所针对的外部端点。 如果需要，您可以通过我们的“上限/限制 API”定义较大的上限或限制来覆盖此设置。 Refer to [this page](../action/about-custom-action-configuration.md) for more details on how to request capping increases.

+++

+++ How many retries are performed? Can I change the number of retries or define a minimum wait period between retries?

For a given call, a maximum of three retries can be performed after the first call, until the end of timeout duration is reached. The number of retries and the time between each retry cannot be changed. 请参阅[此小节](../configuration/external-systems.md#timeout)。

+++

+++ Where can I configure the timeout? Is there a maximum value?

在每个历程中，您可以定义超时持续时间。 超时持续时间在历程的属性中配置。 Timeout duration must be between 1 second and 30 seconds. Refer to [this section](../configuration/external-systems.md#timeout) and [this page](../building-journeys/journey-properties.md#timeout_and_error).

+++

+++ 什么是出口代理？我应何时使用它？

出口代理为从Journey Optimizer **自定义操作**&#x200B;到外部系统的出站调用提供&#x200B;**静态IP地址**。 当您的第三方端点需要IP时使用它。

**重要信息：**&#x200B;出口代理不控制吞吐量、速率限制或并发连接数。 要管理呼叫量和连接限制，请使用[上限API](capping.md)或[限制API](throttling.md)。

**为以下对象使用出口代理：**
* 在第三方防火墙或端点上列入允许列表静态IP

**对以下对象使用上限/限制API：**
* 限制每秒API调用的数量
* 控制到端点的并发连接
* 保护外部系统避免过载

如果您需要使用静态IP进行Adobe，请联系列入允许列表为您的组织启用出口代理。

+++

+++ 使用自定义操作时，Journey Optimizer打开的最大连接数是多少？

启用IP代理并在目标端点上定义限制配置后，连接数基于速率（这些是估计值，不保证数量）：

* 200至2000年c/s：50个连接
* 2000至3000年：75次连接
* 3000到4000之间：100个连接
* 4000至5000之间：125次连接

如果端点上未定义限制配置，则Journey Optimizer的引擎将设计为按比例放大，并且可能会获得大量连接（超过2,000个）。 为了获得有限数量的连接，客户需要使用限制配置。

+++
