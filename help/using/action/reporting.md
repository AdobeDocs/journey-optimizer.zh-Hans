---
solution: Journey Optimizer
product: journey optimizer
title: 监控您的自定义操作
description: 了解如何使用历程报告中的数据
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 97464b7afa07199792bd4311d0477b5bcb140d8e
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 2%

---

# 监控您的自定义操作 {#reporting}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_custom_actions_monitor"
>title="监控您的自定义操作"
>abstract="通过&#x200B;**[!UICONTROL 自定义操作]**&#x200B;报告页面，您可以跟踪历程对第三方系统发起的API调用的性能和可靠性。"

**[!UICONTROL 自定义操作]**&#x200B;报告页面允许您监视从历程到第三方系统的API调用的可靠性和性能。 这些报告可帮助您快速识别可能影响投放的集成问题、延迟瓶颈或限制/上限限制。

“自定义操作”报表页面的功能与Journey Optimizer中的其他实时报表类似。 有关仪表板功能的详细信息，请参阅[本文档](../reports/report-cja-manage.md)。

要访问&#x200B;**[!UICONTROL 自定义操作]**&#x200B;报告页面，请从您的![](assets/do-not-localize/Smock_Monitoring_18_N.svg)操作&#x200B;**[!UICONTROL 主页中单击]**。

![](assets/monitor-1.png)

➡️ [了解有关自定义操作配置的更多信息](../action/about-custom-action-configuration.md)

除了&#x200B;**[!UICONTROL 自定义操作]**&#x200B;报告页面之外，您还可以使用&#x200B;**[!DNL Adobe Experience Platform Query Service]**&#x200B;生成查询以报告自定义操作性能指标。 [此节](../reports/query-examples.md)中提供了查询示例。

## KPI {#kpis}

![](assets/monitor-2.png)

**[!UICONTROL 自定义操作]**&#x200B;关键绩效指标(KPI)用作集中式仪表板，提供自定义操作调用的运行状况和可靠性的综合视图。 这些指标允许您评估性能、发现瓶颈并确保与外部系统的稳定集成。

+++ 了解有关自定义操作KPI的更多信息

* **[!UICONTROL 成功的调用]**：返回有效响应且无错误的HTTP调用总数。

* **[!UICONTROL 4xx/5xx错误]**：由于客户端(4xx)或服务器端(5xx)错误，突出显示配置问题或终结点故障而失败的调用数。

* **[!UICONTROL 超时]**：因超出最大响应时间而失败的调用数。 这有助于显示外部端点的滞后或性能问题。

* **[!UICONTROL 上限调用]**：由于上限限制而被阻止的调用数，可确保下游系统不会过载。

* **[!UICONTROL 平均RPS]**：在所选时间范围内，自定义操作每秒处理的请求数。

* **[!UICONTROL 平均延迟]**：所有HTTP调用的平均端到端响应时间（以毫秒为单位），包括成功的调用、错误和超时。

* **[!UICONTROL 平均成功延迟]**：仅成功调用的平均端到端响应时间（以毫秒为单位），不包括失败的请求和超时。

* **[!UICONTROL 平均队列时间]**：呼叫在发送之前在执行队列中等待的平均时间（以毫秒为单位）。 这仅适用于受限制的端点，当达到吞吐量限制时，Journey Optimizer会将调用排入队列。

+++

## 随时间变化的呼叫 {#calls}

![](assets/monitor-3.png)

**[!UICONTROL 随时间变化的调用]**&#x200B;图形显示了在为报告选择的时间段内的HTTP调用KPI趋势。 时间序列的粒度取决于所选的时间范围。 例如：

* 对于7天的报告，每个数据点都将显示一天的KPI。
* 如果您选择1天时间范围，该图表将显示每小时的KPI。
* 如果您选择1小时时间范围，该图表将显示每分钟的KPI。

➡️[有关HTTP调用量度的说明，请参阅KPI部分](#kpis)

## 一段时间内的延迟 {#latency-overtime}

![](assets/monitor-6.png)

**[!UICONTROL 一段时间内的延迟]**&#x200B;图形可显示所选时段内的延迟量度趋势。 通过这个时间序列视图，您可以跟踪性能模式、识别高峰延迟时段并监视优化或系统更改随时间变化的影响。

➡️[请参阅KPI部分以获取延迟量度的说明](#kpis)


## 呼叫细分 {#breakdown}

![](assets/monitor-4.png)

**[!UICONTROL 调用细分]**&#x200B;表提供了HTTP调用量度的层次细分，从顶级的每个端点的总体量度，到使用每个端点的每个自定义操作的量度，再到底层依赖这些量度的历程。

➡️[有关HTTP调用量度的说明，请参阅KPI部分](#kpis)

## 延迟细分 {#latency-breakdown}

![](assets/monitor-5.png)

**[!UICONTROL 延迟细分]**&#x200B;表提供了自定义操作中延迟量度的详细细分。 此视图可帮助您识别哪些特定端点或操作遇到性能问题，使您能够有效地查明并解决延迟瓶颈。

➡️[请参阅KPI部分以获取延迟量度的说明](#kpis)

## 操作说明视频 {#video}

以下视频介绍了如何监控从您的旅程到第三方系统的API调用的可靠性和性能。

+++观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3479541?quality=12&learn=on)

+++
