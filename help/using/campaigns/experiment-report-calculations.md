---
title: 实验报表中使用的统计计算
description: 进一步了解运行实验报告时使用的统计计算
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta" type="Informitive"
exl-id: b3336381-bc73-4c8f-938f-f10fe37305b0
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 3%

---

# 实验报表中的统计计算 {#experiment-report-calculations}

>[!BEGINSHADEBOX]

您将在本文档中找到的内容：

* [内容体验入门](get-started-experiment.md)
* [创建内容体验](content-experiment.md)
* [了解统计计算](experiment-calculations.md)
* [配置实验报表](reporting-configuration.md)
* **[实验报表中的统计计算](experiment-report-calculations.md)**

>[!ENDSHADEBOX]

本页记录了Adobe Journey Optimizer促销活动实验报表中使用的详细统计计算。

请注意，本页面面向技术用户。

## 转化率

转化率或 **均值**,μ<sub>ν</sub> 每次治疗 `ν` 在实验中，定义为量度总和与分配给该量度的用户档案数之比，N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

给，Y<sub>iν</sub> 是每个用户档案的目标量度值 `i`，已分配给给定变体 *ν*. 当目标量度是“唯一”量度时，即是执行特定操作的用户档案数量的计数，此量度将显示为转化率，并以百分比格式设置。 当量度是“计数”或“总值”量度（例如，电子邮件打开次数、收入）时，该量度的平均估计值会显示为“每个用户档案的计数”或“每个用户档案的值”。

根据需要，将样本标准偏差与表达式一起使用：

![](assets/statistical_2.png){width="225" align="center"}

## 提升 {#lift}

变体之间的提升度  *ν*、和控制变量  *ν<sub>0</sub>* 是转化率中的相对“增量”，定义为以下计算方式，其中各个转化率如上所述。 以百分比形式显示。

![](assets/statistical_3.png){width="125" align="center"}

</br>

## 针对个人治疗的任意有效置信区间

“历程实验”面板可针对实验中的个别处理显示“任何时候有效”的置信区间（置信序列）。

单个变体的置信度序列 `ν` 是Adobe使用的统计方法的核心。 您可以在 [本页](https://doi.org/10.48550/arXiv.2103.06476) (复制自 [沃比 — 史密斯等])。

如果您有兴趣估计目标参数 `ψ` 例如实验中变体的转化率、“固定时间”置信区间(CI)序列与时均置信序列(CS)之间的二分法可概括如下：

![](assets/statistical_4.png){width="500" align="center"}

对于常规置信区间，概率保证目标参数位于值范围内。C.A.D.C.D.C.D.C.D.C.D.C.D.C.D.C.D.C.D.C.D.C.D.D.C.D.C.D.T.D.T.D.T.D.T.D.D.D.D.D.C.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.D.T.T.D.<sub>n</sub> 仅在 `n` (其中 `n` 是示例数)。 相反，对于置信序列，我们保证始终/所有样本量的值 `t`，则目标参数的“true”值位于范围内。

这具有一些深层含义，对于在线测试非常重要：

* 当有新数据时，可以选择更新CS。
* 实验可以持续地监控、自适应地停止或持续。
* I类错误在所有停止时间（包括与数据相关的时间）都受到控制。

Adobe使用渐近置信序列，该序列用于具有平均估计的单个变体 `μ` 具有以下形式：

![](assets/statistical_5.png){width="300" align="center"}

执行:

* `N` 是该变体的单位数。
* `σ` 是标准偏差的样本估计值（如上所定义）。
* `α` 是I类错误的所需级别（或误覆盖概率）。 此值始终设置为0.05。
* ρ<sup>2</sup> 是调节CS最紧的样本大小的常量。 Adobe选择了ρ的普适值<sup>2</sup> = 10<sup>-2.8</sup>，适用于在线实验中看到的转化率类型。

## 置信度 {#confidence}

Adobe使用的置信度是“任何时候有效”的置信度，该置信度是通过反转平均处理效果的置信度序列来获得的。

确切地说，在两个样本中 *t* 测试两个变体之间的差异，在 *p*&#x200B;值，以及不同值的置信区间。 比如，任何时候都有效 *p*-value可通过反转平均处理效果估算器的（任何有效的）置信序列来获得：

![](assets/statistical_6.png){width="200" align="center"}

这里， *E* 是一种期待。 使用的估计器是逆倾向加权(IPW)估计器。 考虑N = N<sub>0</sub> +N<sub>1</sub> 件数，每个件数的变量分配 `i` 由A标记<sub>i</sub>=0,1（如果设备已分配给变体） `ν`=0,1。 如果为用户分配了固定概率（倾向）π<sub>0</sub>,(1-π)<sub>0</sub>)，其结果量度为Y<sub>i</sub>，则平均处理效果的IPW估算器为：

![](assets/statistical_12.png){width="400" align="center"}

注意到 *f* 是影响函数，沃比 — 史密斯等 显示此估算器的置信序列为：

![](assets/statistical_7.png){width="500" align="center"}

用经验估计代替分配概率：π<sub>0</sub> = N<sub>0</sub>/N，方差项可以用单个样本平均估计μ来表示<sub>0,1</sub> 和标准偏差估计，σ<sub>0,1</sub> 为：

![](assets/statistical_8.png){width="500" align="center"}

接下来，回想一下，对于测试统计量z=(μ)的常规假设检验<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>)之间 `p`-values和置信区间：

![](assets/statistical_9.png){width="500" align="center"}

where `Φ` 是标准正态的累积分布。 适用于任何有效时间 `p`-values，假定上述平均处理效果的置信序列，我们可以反转此关系：

![](assets/statistical_10.png){width="600" align="center"}

最后， **任何有效置信度** 为：

![](assets/statistical_11.png){width="200" align="center"}

## 宣布实验为结论

对于双臂实验，Journey Optimizer实验面板会显示一条消息，说明实验是 **结论** 当任何有效置信度超过95%时(即任何有效时间 `p`-value低于5%)。

当存在两个以上变体时，应用Bonferonni校正来控制系列误差率。 为了在 `K` 治疗和单基线（对照）治疗 `K-1` 独立假设检验。 Bonferonni修正意味着，如果在任何有效时，我们拒绝控制与给定变量具有相等手段的零假设 `p`-value（上面定义）低于阈值 `α/(K-1)`.

## 性能最佳的手臂

当宣布实验结果时，显示性能最佳的臂。 这是性能最佳（平均值或转化率最高）的臂，在Set（包括控制）和所有具有 `p` — 值低于Bonferonni阈值。
