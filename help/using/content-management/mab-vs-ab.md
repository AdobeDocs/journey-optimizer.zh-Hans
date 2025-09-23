---
title: 试验报告中使用的统计计算
description: 详细了解A/B测试与多臂老虎机
feature: A/B Testing, Experimentation
role: User
level: Experienced
source-git-commit: 397fad9c95e0c11c0496ab5c9adfb6f8169de4f6
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 2%

---

# A/B与多臂老虎机试验 {#mab-vs-ab}

<!--
>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Experiment type"
>abstract="Experiment type determines how traffic is allocated between treatments during your test. Choose the method that best aligns with your goals:</br>
>
>* **A/B Experiment**: Splits traffic as you define between treatments and measures performance until results are statistically significant. Best for learning which treatment performs better in a controlled comparison.
>
>* **Multi-armed Bandit**: Shifts traffic toward higher-performing treatments as data is collected, balancing speed and optimization. Useful when you want to maximize conversions during the experiment.
>
>* **Bring your own Multi-armed Bandit**: Use your own algorithm to decide traffic allocation, giving you flexibility if you have a custom model or strategy."
-->

本页详细比较了&#x200B;**A/B**&#x200B;和&#x200B;**多臂老虎机**&#x200B;实验，说明了它们各自的优势、局限性以及每种方法最有效的方案。

## A/B {#ab-test}

传统的A/B试验包括在各处理之间平均分配流量，并保持此分配，直到试验结束。 一旦达到统计显着性，就识别获胜处理并随后对其进行缩放。

### 优点

传统A/B试验的关键优势包括：

* **统计严格**

  固定设计提供了明确定义的错误率和置信区间。

  假设检验框架（例如95%置信度）更易于应用和解释。

  适当支持的实验可降低误报的可能性。

* **简单性**

  方法简单明了，设计和执行都非常方便。

  结果可明确传达给非技术利益相关者。

* **综合数据收集**

  每种处理方法都能获得充分的暴露，从而不仅能够分析入选的变体，还能分析表现不佳的替代品。

  这些补充信息可为长期战略决策提供信息。

* **偏置控制**

  固定分配会降低偏见的易感性，例如“赢家的诅咒”或向均值的回归。

### 限制

传统A/B试验的主要局限性包括：

* **机会成本**

  很大一部分流量被引向低等治疗方式，可能会降低测试期间的转化率或收入。

  在试验结束之前，无法实施入选处理。

* **固定持续时间要求**

  测试通常必须按预先指定的时间范围运行，即使外部条件（如季节性、市场变化、中途变化）也是如此。

  实验适应性有限。

## 多臂老虎机 {#mab-experiment}

多臂老虎机算法使用自适应分配：随着证据的积累，更多流量被引向性能更好的处理。 目的是最大化实验期间的累计回报，而不是只关注最终结果。

### 优点

多臂老虎机方法的主要优势是：

* **更快的优化**

  有前途的治疗方法会更早获得优先考虑，从而改善测试期间的整体性能。

* **适应性**

  随着数据的收集，分配会不断更新，这使得多臂老虎机适用于动态环境。

* **机会成本降低**

  不良治疗措施被迅速淘汰，从而最大限度地减少浪费的流量。

* **适用于连续测试**

  对于正在进行的实验或流量代价高昂的上下文有效。

### 限制

多臂老虎机方法的主要局限性包括：

* **较弱的统计保证**

  传统的假设检验方法应用起来比较困难，而阻止规则则比较不清晰。

* **透明度降低**

  自适应分配可能很难向利益相关者解释。

* **有关处理表现不佳的信息有限**

  弱疗法的暴露量极小，限制了诊断insight的应用。

* **实现复杂性**

  需要高级算法和基础架构，而且存在更大的错误配置可能性。

## 何时使用A/B与多臂老虎机

| 方案 | 推荐的方法 |
|-|-|
| 您正在运行探索性或研究驱动测试 | A/B |
| 您正在运行始终运行的营销活动，例如广告、推荐 | 多臂老虎机 |
| 要在测试期间最大限度地提高转化率 | 多臂老虎机 |
| 你需要清晰自信的洞察力 | A/B |
| 您需要快速适应，例如季节转移 | 多臂老虎机 |
| 您的流量有限，希望快速优化投资回报 | 多臂老虎机 |
| 您的流量较大，可以承受较慢的学习时间 | A/B |
| 利益相关者需要明确的决策点 | A/B |

