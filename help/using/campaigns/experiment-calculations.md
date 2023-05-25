---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer试验使用的统计计算
description: 了解有关运行实验时使用的统计计算的更多信息
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
keywords: 内容，试验，统计，计算
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
badge: label="Beta" type="Informative"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 3%

---

# 了解统计计算 {#experiment-calculations}

>[!BEGINSHADEBOX]

本文档包括以下内容：

* [内容体验入门](get-started-experiment.md)
* [创建内容体验](content-experiment.md)
* **[了解统计计算](experiment-calculations.md)**
* [配置实验报表](reporting-configuration.md)
* [实验报表中的统计计算](experiment-report-calculations.md)

>[!ENDSHADEBOX]

本文介绍了在Adobe Journey Optimizer中运行试验时使用的统计计算。

试验使用高级统计方法来计算 **置信序列** 和 **置信度**，这允许您根据需要长时间运行试验并持续监控结果。

本文介绍了试验的工作原理，并直观地介绍了Adobe的 **任何时间有效的置信序列**.

对于专家用户，技术详细信息和参考资料详见 [此页面](../campaigns/assets/confidence_sequence_technical_details.pdf).

## 统计测试和控制错误 {#statistical-testing}

![](assets/technote_1.png)

如上表所示，许多统计推断方法被设计为控制两类错误：

* **误报（I类错误）**：不正确拒绝了null假设，但实际上它是true。 在在线试验的背景下，这意味着我们错误地得出结论认为，尽管结果量度在每种处理之间是相同的，但在每种处理之间是不同的。
   </br>在运行实验之前，我们通常会选择一个阈值 `\alpha`. 实验运行后， `p-value` 是经过计算的，我们拒绝 `null if p < \alpha`. 常用的阈值为 `\alpha = 0.05`，这意味着从长远来看，我们预计每100个实验中会有5个误报。

* **误报（II类错误）**：表示我们未能拒绝null假设验证，尽管它为false。 对于实验，这意味着我们并不拒绝空值假设，但实际上它是不一样的。 为了控制这种类型的错误，我们通常需要在我们的实验中拥有足够的用户来保证一定的Power，定义为 `1 - \beta`（即1减去II型错误的概率）。

大多数统计推断技术都要求您根据要确定的影响大小以及容错(`\alpha` 和 `\beta`)。 但是，Adobe Journey Optimizer的方法旨在让您能够持续查看结果，无论您的样本量有多大。

## Adobe的统计方法：任何时间的有效置信序列

A **置信序列** 是a的顺序模拟 **置信区间**，例如，如果您重复试验一百次，并为进入试验的每个新用户计算平均指标及其相关95%置信序列的估计值。 95%置信度序列将包括您运行的100次实验中的95次实验中量度的真实值。 每个试验只能计算一次95%置信区间，以提供相同的95%覆盖率保证；而不是针对每个新用户。 因此，通过使用置信序列，您可以连续监控实验，而不会增加误报错误率。

单个试验的置信序列和置信区间之间的差异如下图所示：

![](assets/technote_2.gif)

**置信序列** 将实验重心转移到估计而不是假设检验，即专注于精确估计治疗之间的手段差异，而不是是否拒绝基于统计显着性阈值的零假设。

然而，以类似的方式，把两者之间的关系 `p-values`，或 **置信度**、和 **置信区间**&#x200B;之间，也存在着一种关系 **置信序列** 任何时间有效 `p-values`或任意时间的有效置信度。 鉴于置信度等量的熟悉程度，Adobe同时提供了 **置信序列** 以及任何时候对其报告的有效信任。

论的理论基础 **置信序列** 来自对随机变量的序列的研究，这些随机变量被称为马丁格勒斯。 下面是一些专家读者的主要结果，但从业者的收获是明确的：

>[!NOTE]
>
>置信度序列可以解释为置信区间的安全序列类似项。您可以根据需要随时查看和解读试验中的数据，并安全地停止或继续试验。 相应的Any Time有效置信度，或 `p-value`，也可以安全解释。

需要注意的是，由于置信序列是“任何时间有效的”，因此在相同的样本量下，它们会比使用固定视域方法更保守。 置信序列的范围通常比置信区间计算大，而任何时间的有效置信度都比固定视域置信度计算小。 这种保守主义的好处是，你可以随时安全地解读结果。

## 宣布试验具有结论性

![](assets/experimentation_report_2.png)

每次查看试验报告时，Adobe都会分析到目前为止在试验中积累的数据，并将在至少一个处理的随时有效置信度超过95%阈值时宣布某个试验具有“结论性”。

此时，表现最佳的处理（基于转化率或配置文件规范化的量度值）将在报表屏幕顶部突出显示，并在表格报表中以星号指示。 在此确定中，只考虑置信度大于95%的治疗方法以及基线。

当存在两种以上的处理时，使用Bonferroni校正链接对多个比较问题进行校正，并控制基于系列的错误率。 在这种情况下，也有可能存在置信度大于95%且置信区间重叠的多个处理。 在这种情况下，Adobe Journey Optimizer将声明转化率（或用户档案规范化的指标值）最高的项目为绩效最佳的项目。
