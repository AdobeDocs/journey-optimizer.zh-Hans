---
product: experience platform
solution: Experience Platform
title: 自动优化模型
description: 了解有关自动优化模型的更多信息
feature: Ranking, Decision Management
role: User
level: Experienced
exl-id: a85de6a9-ece2-43da-8789-e4f8b0e4a0e7
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '1336'
ht-degree: 0%

---

# 自动优化模型 {#auto-optimization-model}

自动优化模型旨在提供可最大程度提高业务客户设置的回报(KPI)的优惠。 这些KPI可以采用转化率、收入等形式。 目前，自动优化侧重于优化优惠点击次数，并将优惠转化作为我们的目标。 自动优化是一种非个性化的功能，可根据选件的“全局”性能进行优化。

## 限制 {#limitations}

使用自动优化模型进行决策管理时受以下限制：

* 自动优化模型不适用于批量决策API。
* 构建模型所需的反馈必须作为体验事件发送。 它不应自动发送到 [!DNL Journey Optimizer] 渠道。

## 术语 {#terminology}

讨论自动优化时，以下术语将会很有用：

* **多臂老虎机**：A [多臂老虎机](https://en.wikipedia.org/wiki/Multi-armed_bandit){target="_blank"} 优化方法平衡了探索性学习与对该学习的利用。

* **汤姆逊采样**：汤普森采样是一种用于在线决策问题的算法，其中采取的操作是按顺序执行的，必须在利用已知的最大即时性能和投资积累可能提高未来性能的新信息之间取得平衡。 [了解详情](#thompson-sampling)

* [**Beta分布**](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"}: Set of continuous [probability distributions](https://en.wikipedia.org/wiki/Probability_distribution){target="_blank"} defined on the interval [0, 1] [parameterized](https://en.wikipedia.org/wiki/Statistical_parameter){target="_blank"} by two positive [shape parameters](https://en.wikipedia.org/wiki/Shape_parameter){target="_blank"}.

## 汤普森采样 {#thompson-sampling}

基于自动优化的算法是 **汤普森采样**. 在本节中，我们讨论了汤普森采样背后的直觉。

[汤普森采样](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}贝叶斯盗贼是一种解决多臂盗贼问题的贝叶斯方法。  其基本思想是将每个优惠的平均奖励??视为一个 **随机变量** 利用我们目前所收集的数据，更新我们对平均奖励的“信念”。 这个“信念”在数学上用一个 **后验概率分布**  — 本质上是一个平均奖励值的范围，以及奖励对每个报价具有该值的可能性（或概率）。 那么，对于每一个决定，我们都会做 **从每个后验奖励分布中取一个点** 并选择其采样奖励值最高的优惠。

下图说明了此过程，我们有3种不同的选件。 起初，我们没有从数据中获得任何证据，我们假定所有报价都具有统一的后验报酬分布。 我们从每个优惠的后验奖励分布中抽取一个样本。 从选件2的分布中选择的示例具有最高值。 以下示例为 **探索**. 显示选件2后，我们收集任何潜在奖励（例如转化/无转化），并使用贝叶斯定理更新选件2的后验分布，如下所述。  我们继续此过程，并在每次显示优惠并收集奖励时更新后验分布。 在第二个数字中，选中的选件3 — 尽管选件1的平均奖励最高（其后验奖励分布最靠右），但是从每个分布中抽样过程导致我们选择了一个明显次优的选件3。 通过这样做，我们为自己提供了进一步了解Offer 3真实奖励分配情况的机会。

当收集到更多的样本时，置信度增加，并且获得对可能的奖励的更准确的估计（对应于更窄的奖励分布）。 在有更多证据的情况下更新我们的信念的过程被称为 **贝叶斯推理**.

最终，如果一个选件（例如选件1）是明确的入选者，则其后奖励分配将与其他选件分开。 此时，对于每个决策，从选件1中抽样得到的奖励可能是最高的，我们将以更高的概率来选择它。 这是 **开发**  — 我们坚信报价1是最佳报价，因此选择它是为了获得最大回报。

![](../assets/ai-ranking-thompson-sampling.png)

**图1**： *对于每项决策，我们都会从后验回报分布中取一个分数。 将选择具有最高样本值（转化率）的选件。 在初始阶段，所有选件均具有均匀分布，因为我们没有任何证据表明来自数据的选件转换率。 随着样本量的增加，后验分布越来越窄，精度也越来越高。 最终，每次都将选择转化率最高的选件。*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**技术详细信息**

要计算/更新分配，我们使用 **Bayes定理**. 对于每个选件 ***i***，我们要计算它们的***P(??i | 数据)***，即对于每个选件 ***i***，奖励值出现的概率 **??i** 根据我们目前为该选件收集的数据，

根据贝叶斯定理：

***后验概率=概率*先验***

此 **先验概率** 是对产生输出的概率的初步猜测。 在收集了一些证据之后，这种概率被称为 **后验概率**. 

自动优化旨在考虑二进制奖励（单击/不单击）。 在这种情况下，可能性表示来自N个审判的成功数量，并以 **二项式分布**. 对于某些似然函数，如果您选择某个先验分布，则后验分布与先验分布相同。 这样的前一个则称为 **共轭验前**. 这种先验使后验分布的计算变得非常简单。 此 **Beta分布** Beta分布采用两个参数： ***α*** 和 ***β***. 这些参数可以看作是成功和失败的计数，其平均值由以下公式给出：

![](../assets/ai-ranking-beta-distribution.png)

如上所述的Likelihood函数由二项式分布建模，其中s是成功（转化），f是失败（无转化），q是 [随机变量](https://en.wikipedia.org/wiki/Random_variable){target="_blank"} with a [beta distribution](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"}.

验前分布采用Beta分布建模，验后分布采用以下形式：

![](../assets/ai-ranking-posterior-distribution.svg)

计算后验的方法为将成功和失败数添加到现有参数中 ***α***， ***β***.

对于自动优化，如上面的示例所示，我们以先验分布开始 ***Beta(1， 1)*** （均匀分布）对于所有选件，在给定选件获得成功和失败后，后验会成为带参数的Beta分布 ***(s+α， f+β)*** 为了那个报价。
+++

**相关主题**：

要更深入地了解汤普森采样，请阅读以下研究论文：
* [Thompson抽样方法的实证分析](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target="_blank"}
* [多臂强盗问题的Thompson抽样分析](https://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target="_blank"}

## 冷启动问题 {#cold-start}

向营销活动添加新选件，并且没有有关新选件转化率的可用数据时，会出现“冷启动”问题。 在此期间，我们必须想出一个策略，确定选择此新选件的频率，以便将性能下降降至最低，同时收集有关此新选件转化率的信息。 有多种解决方案可以解决此问题。 关键是在探索这一新提议与不牺牲开采之间找到平衡。 目前，我们使用“均匀分布”作为新选件的转化率（先验分布）的初始猜测。 基本上，我们给所有的转化率值赋予相同的发生概率。


![](../assets/ai-ranking-cold-start-strategies.png)

**图2**： *以包含3个选件的营销活动为例。 在营销活动处于实时状态时，选件4会添加到营销活动中。 最初，我们没有关于选件4的转化率的数据，因此我们必须处理冷启动问题。 我们使用均匀分布作为我们关于选件4转化率的初步猜测，同时我们收集此新选件的数据。 如 [汤普森采样](#thompson-sampling) 部分，为了选择将向用户显示的选件，我们从选件的后验奖励分布中采样点，并选择具有最高采样值的选件。 在上例中，我们选择了选件4，并且随后根据所收集的奖励更新了此选件的后验分布，如 [汤普森采样](#thompson-sampling) 部分。*

## 提升测量 {#lift}

“提升”是用于衡量在排名服务中部署的任何策略与基线策略（仅随机提供选件）相比的表现。

例如，如果我们有兴趣衡量用于排名服务的汤普森采样(TS)策略的性能，并且KPI是转化率(CVR)，则TS策略相对于基线策略的“提升”定义为：

![](../assets/ai-ranking-lift.png)
