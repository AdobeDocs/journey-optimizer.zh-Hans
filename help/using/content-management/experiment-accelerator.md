---
solution: Journey Optimizer
product: journey optimizer
title: Experimentation Accelerator
description: 提高有效开展试验并产生见解的能力
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: 内容，实验，多个，受众，处理
hide: true
hidefromtoc: true
source-git-commit: e4d5631701c5c270af7aec931f6b98a567b4ed29
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 1%

---

# Experimentation Accelerator入门 {#content-experiment}

>[!BEGINSHADEBOX]

* **[开始使用Experimentation Accelerator](experiment-accelerator.md)**
* [实验选项卡](experiment-accelerator-monitor.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
> Experimentation Accelerator目前处于测试阶段，各项功能正在逐步推出。

**Experimentation Accelerator**&#x200B;是一个功能强大的工具，旨在简化和增强试验流程。 通过与Adobe Target和Adobe Journey Optimizer集成，它提供了一个用于管理、分析和优化试验的集中平台。 Experimentation Accelerator利用AI驱动的洞察和自适应测试，使您能够做出数据驱动型决策、改进营销策略并取得可衡量的结果。

主要优势包括：

* **更快的试验**：使用随时间调整的模型运行自适应、始终开启的测试。

* **Unified Platform**：在一个位置管理Adobe Target和Journey Optimizer的所有试验。

* **AI驱动的分析**：自动显示关键发现、性能驱动因素和新机会。

* **更智能的定位**：使用行为和内容数据优先考虑高影响力的实验。

* **KPI监控**：跨试验跟踪提升度、收入和置信度等量度。

* **无缝Collaboration**：通过实时警报轻松共享结果和管理团队角色。

在[创建和配置实验](content-experiment.md)并将营销活动或历程发送到配置文件后，您可以访问&#x200B;**[!UICONTROL Experimentation Accelerator]**&#x200B;以深入了解实验的执行情况。

要访问&#x200B;**[!UICONTROL Experimentation Accelerator]**，请执行以下操作：

* 从左侧菜单中选择&#x200B;**[!UICONTROL 试验]**&#x200B;下拉菜单中的&#x200B;**[!UICONTROL Experimentation Accelerator]**。

* 或者，从应用程序切换器中选择&#x200B;**[!UICONTROL Experimentation Accelerator]**。

请注意，仅具有Target许可证的用户只能通过应用程序切换器访问它。

<!--
<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="Overview" href="experiment-accelerator-overview.md" src="assets/do-not-localize/experiments-2.jpeg">
<div align="center"><p><strong><a href="experiment-accelerator-overview.md">Overview</a></strong></p></div></td>
<td><img alt="Experiments" href="experiment-accelerator-monitor.md" src="assets/do-not-localize/experiment-overview.jpeg">
<div align="center"><p><strong><a href="experiment-accelerator-monitor.md">Experiments</a></strong></p></div></td>
<td><img alt="Metrics" href="experiment-accelerator-metrics.md" src="assets/do-not-localize/experiment-metrics.png">
<div align="center"><p><strong><a href="experiment-accelerator-metrics.md">Metrics</a></strong></p></div></td>
</tr></table>
-->

## 什么是A/B测试？

A/B测试是比较两个或更多版本的东西以确定哪个版本比定义的目标表现更好的过程。

参与者会被随机分配给一个称为变体的版本，并会跟踪他们的行为。 结果将显示一个版本在统计上是否优于其他版本。

## 关键术语

| 术语 | 定义 |
|-|-|
| 控件 | 用作比较基准的原始版本。 |
| 变体或处理 | 已创建新版本以针对控件进行测试。 |
| 假设验证 | 预测哪些变化将产生更好的结果，以及为什么。 |
| 样本量 | 测试中包含的个人或会话数。 |
| 统计显着性 | 衡量结果的置信度，其结果并非由随机随机偶然性引起。 |
| 提升 | 与控制组相比，变体的百分比改善或降低。 |
| 主要量度 | 用于确定测试成功与否的主要衡量标准。 |
| 次要量度 | 支持提供其他insight或帮助监控意外影响的指标。 |
| 置信区间 | 真实效果可能下降的估计范围。 |
| 区段 | 独立分析的特定受众子集（例如，新用户、移动访客）。 |

## 运行试验的最佳实践

* **从明确的假设开始**

  一个强有力的假设包括您正在更改的内容、您预期发生的情况以及原因。
示例： _我们相信更改X将由于Z而增加Y。_

* **定义有意义的成功量度**

  选择与您更宽泛的目标一致的量度。 避免使用看起来良好但未反映实际影响的“虚名”量度。

* **一次测试一个更改（如果可能）**

  隔离变量使得更易于准确地解释结果。 如果一次测试多个更改，您可能不知道导致该效果的原因。

* **让测试运行足够长**

  过早的结论可能会产生误导。 等待统计上显着的样本量后再采取行动。

* **了解外部因素**

  季节性、假期以及您环境中的其他更改可能会扭曲结果。 记录任何可能影响测试期间行为的内容。

* **认真使用分段**

  按受众区段划分结果可揭示隐藏的模式，但避免过度解释小样本大小。

* **文档并共享学习内容**

  清楚地记录测试的内容、原因以及您学到的内容。 这有助于建立机构知识，防止重复错误。

## 常用量度

| 量度 | 衡量标准 | 使用时间 |
|-|-|-|
| 转化率 | 完成所需操作的用户的百分比 | 对于跟踪目标驱动型体验的成功非常有用 |
| 点进率(CTR) | 点击特定元素的用户百分比 | 指示体验的吸引力 |
| 参与率 | 用户与体验的交互级别 | 适合衡量兴趣或关注 |
| 跳出率 | 快速离开而不执行操作的用户的百分比 | 可能表示不合适或混淆体验 |
| 页面逗留时间 | 用户在体验的特定部分上花费的时间 | 可以反映兴趣深度或复杂性 |
| 每位访客带来的收入(RPV) | 每个用户获得的平均收入 | 通常用于以商业为中心的实验 |
| 保留率 | 随着时间的推移返回或保持参与的用户百分比 | 对长期价值评估很有用 |

## 怎样做一个好的实验？

一个好的实验不只产生一个胜利，它产生一个明确、可操作的学习。
以下是要查找的内容：

&amp;amp；check； **统计置信度**：变量之间的差异不太可能是偶然造成的。
&amp;amp；check； **与目标的对齐方式**：主要量度反映了向业务目标迈进的有意义的进展。
&amp;amp；check； **次要影响**：对相关量度没有显着的负面影响。
&amp;amp；check； **可扩展性**：结果可以为将来的决策提供信息或推广到其他领域。
&amp;amp；check； **Clarity**：结果的原因被合理地隔离和理解。

试验不仅仅是寻找“最佳”版本，它还包括通过测试和迭代来构建知识。 如果一切顺利，实验将揭示推动更明智决策、更佳用户体验和改进结果的洞察力。

>[!BEGINSHADEBOX]

**示例：**

* **公司**：连锁酒店
* **假设验证**：如果在主页上使用更紧急的语言，将导致更多预订。
   * **控件**：原始版本
   * **变体**：已添加具有紧急性的新版本
   * **主要指标**：预订率
   * **辅助量度**：跳出率、网站逗留时间
* **结果**：变体使预订率提升了14%，且其他量度没有负变化。
* **操作**：考虑推出该变体并运行后续实验以在其他领域测试类似的方法。

>[!ENDSHADEBOX]
