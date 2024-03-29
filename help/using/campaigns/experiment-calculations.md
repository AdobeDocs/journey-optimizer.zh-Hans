---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer试验使用的统计计算
description: 了解有关运行实验时使用的统计计算的更多信息
feature: Experimentation
topic: Content Management
role: User
level: Experienced
keywords: 内容，实验，统计，计算
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 1490ac2efd39c6bf9b6ca97e682750463e9f054d
workflow-type: tm+mt
source-wordcount: '1067'
ht-degree: 0%

---

# 了解统计计算 {#experiment-calculations}

本文介绍了在Adobe Journey Optimizer中运行实验时使用的统计计算。

试验用途 [高级统计方法](../campaigns/assets/confidence_sequence_technical_details.pdf) 以计算 **置信序列** 和 **置信度**，您可在需要时运行试验并持续监控结果。

本文介绍了试验的工作原理，并直观地介绍了Adobe的 **任何时间有效的置信序列**.

对于专家用户，技术详细信息和参考资料详见 [此页面](../campaigns/assets/confidence_sequence_technical_details.pdf).

## 统计测试和控制错误 {#statistical-testing}

在运行试验时，您试图确定两个群体之间是否存在差异，以及该差异是否由偶然性引起。

通常有两种假设：

* 该 **空假设验证** 也就是说对治疗没有影响
* 该 **替代假设验证** 意思是治疗有作用

在统计意义上，目标是尝试评估证据的力量以拒绝零假设。 需要注意的一点是，统计学意义是用来判断治疗方案出现差异的可能性，而不是成功的可能性。 这就是为何要结合使用统计显着性与 **提升**.

有效的试验需要考虑可能导致不正确推断的不同类型的错误。

![](assets/technote_1.png)

上表说明了错误的不同类型：

* **误报（I类错误）**：是对null假设的错误拒绝，但实际上它是true。 在在线实验的背景下，这意味着我们错误地得出每种处理的结果量度各不相同，尽管它们相同。
  </br>在运行试验之前，我们通常会选择一个阈值 `\alpha`. 实验运行后， `p-value` 是经过计算的，我们拒绝 `null if p < \alpha`.选择一个 `/alpha` 基于得到错误答案的后果，例如，在临床试验中，某人的生命可能会受到影响，你可能会决定 `\alpha = 0.005`. 在线实验中常用的阈值为 `\alpha = 0.05`，这意味着从长远来看，我们预计每100个实验中会有5个误报。

* **误报（II类错误）**：表示我们未能拒绝null假设验证，尽管它为false。 对于实验，这意味着我们不拒绝空假设，但实际上它是不一样的。 为了控制这种类型的错误，我们通常需要在我们的实验中拥有足够的用户来保证一定的功率，定义为 `1 - \beta`（即1减去II型错误的概率）。

大多数统计推断技术都要求您根据希望确定的影响大小和错误容差(`\alpha` 和 `\beta`)。 但是，Adobe Journey Optimizer的方法旨在允许您持续查看结果，无论您的样本量有多大。

## Adobe的统计方法：任何时间有效的置信序列

A **置信序列** 是a的顺序模拟 **置信区间**，例如，如果您重复试验一百次，并计算每个进入试验新用户的平均指标估计值及其相关的95%置信序列。 95%置信度序列将包括您运行的100次实验中的95次实验中量度的真实值。 每个试验只能计算一次95%置信区间，以提供相同的95%覆盖率保证；而不是针对每个新用户。 因此，通过使用置信序列，您可以连续监控实验，而不会增加误报错误率。

单个试验的置信序列和置信区间之间的差异如下面的动画所示：

![](assets/technote_2.gif)

**置信序列** 将试验的焦点转移到估计而不是假设检验，即专注于精确估计治疗之间的手段差异，而不是是否拒绝基于统计显着性阈值的零假设。

然而，以类似的方式，把两者 `p-values`，或 **置信度**、和 **置信度间隔**，这其中也有一个关系 **置信序列** 任何时间有效 `p-values`或任意时间的有效置信度。 鉴于置信度等量的熟悉程度，Adobe提供了以下两点 **置信序列** 以及随时有效的信任度。

理论基础 **置信序列** 来自对随机变量的序列的研究，这些随机变量被称为“马丁格勒”。 下面是专家阅读的一些主要结果，但实践者的经验很清楚：

>[!NOTE]
>
>置信序列可以解释为置信区间的安全序列类似项。 通过使用置信区间，您只能在达到预先确定的样本大小后解释试验。 但是，通过使用置信序列，您可以随时查看并解释试验中的数据，并安全地停止或继续试验。 对应的Any Time Valid Confidence，或 `p-value`，也可在任何时候安全解释。

需要注意的是，由于置信序列是“任何时间有效的”，因此它们比在相同样本量下使用的固定水平域方法更保守。 置信序列的范围通常比置信区间计算大，而任何时间的有效置信度都将小于固定视域置信度计算。 这种保守主义的好处是，你可以随时安全地解读结果。

## 宣布试验具有结论性

![](assets/experimentation_report_2.png)

每次查看试验报告时，Adobe都会分析到目前为止在试验中积累的数据，并将在至少一个治疗的随时有效置信度超过95%阈值时宣布试验具有“结论性”。

此时，报表屏幕顶部将突出显示执行效果最佳的处理（基于转化率或配置文件标准化量度值），并在表格报表中以星号指示。 在此确定时，只考虑置信度大于95%以及基准值的处理。

当存在两个以上的处理时，使用Bonferroni校正链接对多个比较问题进行校正，并控制基于族的错误率。 在这种情况下，也有可能存在置信度大于95%且置信区间重叠的多个处理。 在这种情况下，Adobe Journey Optimizer将声明转化率（或配置文件规范化的量度值）最高的的那一个是最佳绩效者。
