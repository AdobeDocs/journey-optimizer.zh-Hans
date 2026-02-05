---
solution: Journey Optimizer
product: journey optimizer
title: 内容优化入门
description: 了解如何使用内容优化在您的营销活动和历程中提供个性化和优化的内容。
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: 优化、定位、实验、A/B测试、活动、历程、个性化
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: 8dba26f29fda47d0b953d80656aa0f0b6fe294a9
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 8%

---

# 内容优化入门 {#message-optimization}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_optimization"
>title="内容优化"
>abstract="通过Journey Optimizer中的内容优化，您可以测试内容的不同版本并确定表现最佳的版本。 您可以使用定位向特定区段提供个性化内容，或者使用试验来测试多个变体，或者将这两种方法结合使用以实现复杂的优化策略。"

内容优化使您拥有多种工具，可在适当的时间向适当的受众传达恰当的信息。 通过将数据驱动型洞察与强大的个性化功能相结合，您可以最大限度地提高营销活动和历程的参与度和转化率。

内容优化在[营销活动](../campaigns/create-campaign.md)和[历程](../building-journeys/journey-gs.md)中均可用，使您能够在所有客户接触点中应用相同的优化策略。

➡️ [在此视频中了解如何在营销活动中利用内容优化](#video)

## 优化功能 {#capabilities}

通过Journey Optimizer中的内容优化，您可以：

* [使用定位](optimization-targeting.md)根据配置文件属性、上下文数据或受众成员资格向特定受众区段提供个性化内容。

* [运行实验](optimization-experimentation.md)以测试多个内容变体并根据您的成功量度确定表现最佳的变体。

* [将这两种方法结合使用](optimization-combination.md)以创建完善的优化策略，从中测试每个目标区段的不同变体。

## 定位与试验 {#targeting-vs-experimentation}

了解定位和试验之间的区别可帮助您为目标选择正确的优化方法。

**定位**&#x200B;使用确定性规则，根据已知的配置文件属性、上下文或受众成员资格向特定区段提供个性化内容。 它可确保将正确的信息传达给正确的受众。

**试验**&#x200B;使用随机分配测试多个内容变体并发现表现最佳的变体。 它有助于您通过数据驱动测试了解哪些内容最能引起受众的共鸣。

下表总结了主要差异：

| 功能 | 定位 | 试验 |
|--------|-----------|-----------------|
| **分配方法** | 确定性 — 基于规则 | 随机 — 基于流量分配 |
| **基于** | 配置文件属性、上下文、受众 | 随机分布 |
| **用例** | 将相关内容交付给已知区段 | 发现哪些内容表现最佳 |
| **示例** | 按位置显示不同的促销活动 | 测试2主题行，以查看哪些主题行获得了更多打开 |
| **最适合** | 大规模Personalization | 优化和学习 |

![](../campaigns/assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## 常见使用案例 {#use-cases}

以下是内容优化可以帮助您获得更好结果的一些典型方案：

定位：

* **地理定位** — 根据客户所在位置发送特定于位置的选件。 例如，在较冷地区推广冬季外套，在较温暖的气候中推广泳衣。

* **设备优化** — 提供特定于设备的内容，例如针对桌面用户的桌面优化布局和针对智能手机用户的移动设备优化布局。

试验：

* **A/B测试** — 测试不同的电子邮件主题行、call-to-action按钮或促销优惠，以找出哪些内容促进转化最多。

* **生命周期营销** — 测试新客户的不同入门培训消息与现有客户的保留期优惠。

组合：

* **高级分段** — 按忠诚度级别定位客户，并在每个级别内测试不同的奖励消息，以最大化所有区段的参与度。

## 快速入门 {#get-started}

要开始优化内容，请执行以下操作：

1. **创建营销活动或历程**：设置您的[营销活动](../campaigns/create-campaign.md)或[历程](../building-journeys/journey-gs.md)，并添加至少一个操作。

1. **选择您的优化方法**：
   * [使用定位](optimization-targeting.md)为特定区段个性化内容。
   * [使用试验](optimization-experimentation.md)测试多个变体。
   * [合并两者](optimization-combination.md)以实现高级优化。

1. **定义您的内容**：为您的优化策略创建不同的内容变体。

1. **激活和监视**：启动优化的活动或历程并在[报告](../reports/campaign-global-report-cja.md)中跟踪性能。

## 工作原理 {#how-it-works}

在您的历程或营销活动上线后，将根据您定义的标准评估用户档案。 根据这些评估，每个用户档案都会收到最合适的内容版本：

1. **配置文件评估** — 当配置文件进入您的活动或历程时，Journey Optimizer会评估其属性和上下文。

1. **内容分配** — 基于您的优化配置：
   * 对于&#x200B;**定位**，符合特定条件的配置文件将收到相应的个性化内容。
   * 对于&#x200B;**试验**，会根据流量分配设置将配置文件随机分配给不同的内容变体。
   * 对于&#x200B;**组合**，配置文件首先与定位规则匹配，然后随机分配给该区段的其中一个试验变体。

1. **性能跟踪** - Journey Optimizer自动跟踪参与指标和转化数据，以帮助您识别哪些内容表现最佳。

## 操作方法视频 {#video}

了解如何在操作中或API触发的营销活动中利用内容优化。 您将了解如何定位子受众、按位置创建消息变体、启用备用内容以及在单个营销活动中运行多个实验。本教程还介绍如何管理多渠道营销活动，同时保持消息的一致性。

>[!VIDEO](https://video.tv.adobe.com/v/3470378?captions=chi_hans&quality=12)

**相关主题**

* [创建营销活动](../campaigns/create-campaign.md)
* [创建历程](../building-journeys/journey-gs.md)
* [内容试验](../content-management/get-started-experiment.md)
