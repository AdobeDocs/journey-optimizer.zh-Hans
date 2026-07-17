---
solution: Journey Optimizer
product: journey optimizer
title: 监测忠诚度挑战表现
description: 了解如何使用“忠诚度挑战”报表功能板跟踪Adobe Journey Optimizer中的挑战表现和见解。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: 762afe791cc1fa826b7a9f35f6f54591590bab7c
workflow-type: tm+mt
source-wordcount: 592
ht-degree: 4%

---

# 监测忠诚度挑战表现 {#loyalty-reporting}

>[!BEGINSHADEBOX]

**目录**

[忠诚度挑战入门](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**创建和管理挑战**

* [访问和管理挑战和任务](access-loyalty-challenges.md)
* [创建挑战](create-challenges.md)
* [创建任务](create-tasks.md)
* **监视忠诚度挑战表现** ◀︎**您在这里**

</td>
<td style="vertical-align:top;">

**配置并集成**

* [配置忠诚度挑战](loyalty-admin.md)
* [奖励定义指南](reward-definition-guide.md)
* [Event Transformer指南](event-transformer-guide.md)
* [忠诚度数据和数据集](loyalty-data-and-datasets.md)
* [忠诚度挑战API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](../rn/releases.md)。

使用“忠诚度挑战”报表可查看您的挑战的执行情况。 查看哪些人正在注册、哪些人正在完成挑战，以及您的项目产生了多少收入 — 所有这些都在一个位置完成。 数据来自Adobe Customer Journey Analytics。

要打开报告仪表板，请转到Journey Optimizer中的&#x200B;**[!UICONTROL 忠诚度挑战(Beta)]**，并在左侧导航中选择&#x200B;**[!UICONTROL 忠诚度报告]**。

报表界面有两个选项卡：

* **[报告](#reports-view)**：您面临的挑战的数字和图表。
* **[分析](#insights-cards)**：当前值得您关注的卡片。

## “报表”视图 {#reports-view}

**报告**&#x200B;选项卡概述了您的项目在选定期间的运行情况。 使用页面顶部的日期选取器并选择&#x200B;**[!UICONTROL 应用筛选器]**&#x200B;按钮以更改报告时段并查看更新的数字和图表。

![](assets/reporting-challenge-key.png)

**关键量度**&#x200B;区域一览即可显示四个数字。 每个量度还会显示与上一时段相比的百分比变化。

* **忠诚度会员**：期间有多少忠诚度会员处于活动状态。
* **挑战赛注册**：会员注册挑战赛的次数。
* **收入**：与质询活动关联的总收入。
* **平均完成率**：至少完成一项质询的已注册成员的百分比。

右侧的&#x200B;**最新见解**&#x200B;面板显示您的项目的最新人工智能生成的见解。 选择&#x200B;**[!UICONTROL 查看全部]**&#x200B;以打开完整的&#x200B;**分析**&#x200B;选项卡。

在关键量度下，**挑战**&#x200B;部分为您提供了两个挑战活动视图。

![](assets/reporting-challenge-challenges.png)

* **挑战参与**：一个时间线，其中显示了该期间开始、正在进行和完成的挑战的成员数量。
* **挑战报告**：包含类型、任务、状态和注册号等详细信息的所有挑战列表。 使用搜索栏查找特定质询。 选择挑战以查看其包含参与趋势和性能详细信息的完整报告。

  +++挑战报告示例

  ![](assets/reporting-challenge-report.png)

  +++

## “分析”选项卡 {#insights-cards}

**Insights**&#x200B;选项卡显示AI生成的卡片，该卡片标记忠诚度计划中的异常、趋势和机会。 每张卡片都代表一个观察结果，并根据观察结果与当前项目数据的对比程度进行排名。

![](assets/reporting-insights.png)

右上角的&#x200B;**上次抓取时间**&#x200B;时间戳显示insight引擎上次处理您的程序数据的时间。

### 信息卡操作 {#insight-card-actions}

每个信息卡都有一个包含两个操作的![](assets/do-not-localize/Smock_More_18_N.svg)菜单：

* **解除**：从分析列表中永久删除该卡。
* **暂停**：暂时隐藏卡片。 选择暂停&#x200B;**1天**、**3天**&#x200B;或&#x200B;**7天**。 在暂停时段结束后，卡会重新显示。

<!--
### Priority badges {#insight-badges}

Each card has a priority badge — **High**, **Medium**, or **Low** — based on how significant the underlying signal is relative to your current program data. These levels are relative: there are always a few **High** cards, even in a quiet week. **High** means "most relevant right now", not that a fixed threshold was crossed.
-->

### 类别标记 {#insight-category-tags}

每个卡片都带有一个&#x200B;**类别标记**，用于标识insight与程序相关的部分。

| 类别 | 涵盖的内容 |
| --- | --- |
| **计划范围** | 忠诚度计划的整体状况和性能 |
| **层级** | 各成员层之间的收益率、变动和分布 |
| **挑战** | 特定挑战或跨挑战的活动、完成率和异常 |
| **产品** | 产品目录性能，包括视图、赎回和目录级别的趋势 |
| **成员生命周期** | 成员如何在注册、参与和流失阶段取得进展 |
| **趋势** | 基于时间的模式，如每周周期、季节性尖峰或趋势逆转 |
