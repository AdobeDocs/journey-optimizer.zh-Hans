---
solution: Journey Optimizer
product: journey optimizer
title: 历程报告
description: 了解如何使用历程报告中的数据
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="限量发布版" type="Informative"
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 1%

---

# 监控您的自定义操作 {#reporting}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_custom_actions_monitor"
>title="监控您的自定义操作"
>abstract="通过&#x200B;**[!UICONTROL 自定义操作]**&#x200B;报告页面，您可以跟踪历程对第三方系统发起的API调用的性能和可靠性。"

>[!AVAILABILITY]
>
>自定义操作报表当前仅适用于一组组织（限量发布）。

**[!UICONTROL 自定义操作]**&#x200B;报告页面允许您监视从历程到第三方系统的API调用的可靠性和性能。 这些报告可帮助您快速识别可能影响投放的集成问题、延迟瓶颈或限制/上限限制。

“自定义操作”报表页面的功能与Journey Optimizer中的其他实时报表类似。 有关仪表板功能的详细信息，请参阅[本文档](../reports/report-cja-manage.md)。

要访问&#x200B;**[!UICONTROL 自定义操作]**&#x200B;报告页面，请从您的![](assets/do-not-localize/Smock_Monitoring_18_N.svg)操作&#x200B;**[!UICONTROL 主页中单击]**。

![](assets/monitor-1.png)

➡️ [了解有关如何配置自定义操作的更多信息](../action/about-custom-action-configuration.md)

## KPI {#kpis}

![](assets/monitor-2.png)

**[!UICONTROL 自定义操作]**&#x200B;关键绩效指标(KPI)用作集中式仪表板，提供自定义操作调用的运行状况和可靠性的综合视图。 这些指标允许您评估性能、发现瓶颈并确保与外部系统的稳定集成。

+++ 了解有关自定义操作KPI的更多信息

* **[!UICONTROL 成功的调用]**：返回有效响应且无错误的HTTP调用总数。

* **[!UICONTROL 4xx/5xx错误]**：由于客户端(4xx)或服务器端(5xx)错误，突出显示配置问题或终结点故障而失败的调用数。

* **[!UICONTROL 超时]**：因超出最大响应时间而失败的调用数。 这有助于显示外部端点的滞后或性能问题。

* **[!UICONTROL 上限调用]**：由于上限限制而被阻止的调用数，可确保下游系统不会过载。

* **[!UICONTROL 平均RPS]**：在所选时间范围内，自定义操作每秒处理的请求数。

+++

## 呼叫加班 {#calls}

![](assets/monitor-3.png)

**[!UICONTROL 超时呼叫]**&#x200B;图表显示了在为报告选择的时段内的HTTP呼叫KPI趋势。 时间序列的粒度取决于所选的时间范围。 例如：

* 对于7天的报告，每个数据点都将显示一天的KPI。
* 如果您选择1天时间范围，该图表将显示每小时的KPI。
* 如果您选择1小时时间范围，该图表将显示每分钟的KPI。

➡️[有关HTTP调用量度的说明，请参阅KPI部分](#kpis)

## 呼叫细分 {#breakdown}

![](assets/monitor-4.png)

**[!UICONTROL 调用细分]**&#x200B;表提供了HTTP调用量度的层次细分，从顶级的每个端点的总体量度，到使用每个端点的每个自定义操作的量度，再到底层依赖这些量度的历程。

➡️[有关HTTP调用量度的说明，请参阅KPI部分](#kpis)


