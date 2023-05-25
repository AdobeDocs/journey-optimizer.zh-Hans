---
title: 试验报告中使用的统计计算
description: 了解有关运行试验报告时使用的统计计算的更多信息
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
source-git-commit: 64be9c41085dead10ff08711be1f39760a81ff95
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 0%

---

# 了解试验报告中的统计计算 {#experiment-report-calculations}

本页记录了Adobe Journey Optimizer中促销活动的试验报告中使用的详细统计计算。

请注意，本页面向技术用户。

## 转化率

转换率或 **平均值**， μ<sub>ν</sub> 进行每种处理 `ν` 在试验中，定义为量度总和与分配给该量度的配置文件数量的比率，N<sub>ν</sub>：

![](assets/statistical_1.png){width="125" align="center"}

给，Y<sub>iν</sub> 是每个用户档案的目标量度的值 `i`，已分配给给定变体 *ν*. 当目标量度是“唯一”量度（即，它是执行特定操作的配置文件数的计数）时，显示为转化率，并按百分比格式设置。 当指标为“计数”或“总值”指标（分别例如，电子邮件打开次数、收入）时，该指标的平均估计值显示为“每个配置文件的计数”或“每个配置文件的值”。

在需要的地方，使用样本标准差与表达式：

![](assets/statistical_2.png){width="225" align="center"}

## 提升 {#lift}

变量之间的提升  *ν*、和控制变量  *ν<sub>0</sub>* 换股价之相对“差值”，定义见下文计算，其中个别换股价定义见上文。 以百分比显示。

![](assets/statistical_3.png){width="125" align="center"}

</br>

## 单个处理的随时有效置信区间

历程试验面板显示试验中各个治疗的“随时有效”置信区间（置信序列）。

单个变量的置信序列 `ν` 是Adobe所使用的统计方法的核心。 您可以在以下位置找到其定义 [此页面](https://doi.org/10.48550/arXiv.2103.06476) (复制自 [沃德比 — 史密斯等])。

如果您有兴趣估计目标参数 `ψ` 例如，试验中变体的转化率，“固定时间”置信区间(CI)序列和时间均匀置信序列(CS)之间的二分法可概括如下：

![](assets/statistical_4.png){width="500" align="center"}

对于正则置信区间，概率保证目标参数位于值ċ范围内<sub>n</sub> 仅在的单个固定值下有效 `n` (其中 `n` 为样本数)。 相反，对于置信序列，我们保证在任何时候/所有样本大小值 `t`，则目标参数的“true”值位于边界内。

这隐含了一些对在线测试非常重要的深层含义：

* 每当有新数据可用时，可以选择更新CS。
* 可以连续监测、自适应停止或继续试验。
* I型错误会在所有停止时间（包括依赖于数据的时间）进行控制。

Adobe使用渐近置信序列，它适用于具有平均估计值的单个变体 `μ` 具有以下形式：

![](assets/statistical_5.png){width="300" align="center"}

执行:

* `N` 是该变体的单位数。
* `σ` 是标准偏差的样本估计值（定义见上文）。
* `α` 是I型错误（或误覆盖概率）的所需级别。 此值始终设置为0.05。
* ρ<sup>2</sup> 是一个常数，它调节CS最紧密的样品大小。 Adobe已选择一个ρ的通用值<sup>2</sup> = 10<sup>-2.8</sup>，适用于在线实验中显示的转化率类型。

## 置信度 {#confidence}

Adobe所用的置信度是一种“随时有效”的置信度，它是通过对平均处理效果的置信序列求逆而得到的。

更精确地说，在两个样本中 *t* 测试两个变体之间均值的差异，变体之间存在1:1的映射 *p* — 值，以及均数的置信区间。 打个比方，随时有效 *p*-value可以通过求平均处理效果估计器的（随时有效的）置信序列来得到：

![](assets/statistical_6.png){width="200" align="center"}

此处， *E* 是一种预期。 该估计器使用反倾向加权(IPW)估计器。 考虑N = N<sub>0</sub> +N<sub>1</sub> 单位，每个单位的变量分配 `i` 标记为A<sub>i</sub>=0,1表示单位已分配给变体 `ν`=0,1. 如果用户被指派为固定概率（倾向） π<sub>0</sub>，(1-π<sub>0</sub>)，其结果量度为Y<sub>i</sub>，则IPW的平均处理效果估计器为：

![](assets/statistical_12.png){width="400" align="center"}

注意到 *f* 影响函数，沃德比 — 史密斯等 结果表明，该估计器的置信序列为：

![](assets/statistical_7.png){width="500" align="center"}

用经验估计代替指派概率：π<sub>0</sub> = N<sub>0</sub>/N，方差项可以用个别样本的平均估计值μ表示<sub>0,1</sub> 和标准差估计值，σ<sub>0,1</sub> 作为：

![](assets/statistical_8.png){width="500" align="center"}

接下来，回忆一下对于具有测试统计量z = (μ)的常规假设检验<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>)两者之间存在对应关系 `p` — 值和置信区间：

![](assets/statistical_9.png){width="500" align="center"}

位置 `Φ` 是标准常数的累积分布。 无论何时有效 `p`-values，给定上面定义的平均处理效果的置信序列，我们可以反转此关系：

![](assets/statistical_10.png){width="600" align="center"}

最后， **随时有效置信度** 为：

![](assets/statistical_11.png){width="200" align="center"}

## 宣布试验具有结论性

对于双臂试验，“Journey Optimizer试验”面板会显示一条消息，说明某个试验是 **已有定论** 当随时有效置信度超过95%(即，随时有效 `p`-value小于5%)。

当存在两个以上的变量时，应用Bonferonni校正来控制族的错误率。 对于试验 `K` 治疗法，和单一基准（对照）治疗法，有 `K-1` 独立假设检验。 Bonferonni校正意味着我们拒绝空的假设，即如果任意时刻有效，控制项和给定变量具有相等均值 `p`-value（以上定义）低于阈值 `α/(K-1)`.

## 性能最佳的手臂

当一个实验被宣布为具有结论性时，显示最佳性能的臂。 这是一组具有最佳性能（最高平均或转换率）的臂，该组包括控制项，以及所有具有 `p` — 值低于Bonferonni阈值。
