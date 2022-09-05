---
title: 创建内容实验
description: 了解如何在营销活动中创建内容实验
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 6068060e66f75a7727f4a0fdae580c11542fa13b
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 4%

---

# 创建内容体验 {#content-experiment}

>[!AVAILABILITY]
>
>的 **内容实验** 功能当前仅适用于一组组织（有限可用性）。 有关更多信息，请与您的 Adobe 代表联系。

使用Journey Optimizer内容实验定义多种投放处理方式。 兴趣的受众被随机分配给每个治疗，以便确定哪个治疗在兴趣量度方面表现最佳。 您可以选择更改电子邮件的内容、主题或发件人。

>[!NOTE]
>
>在开始内容实验之前，请确保为自定义数据集设置了报表配置。 有关详细信息，请参阅[此部分](reporting-configuration.md)。

在以下示例中，投放目标已被拆分为两个组，每个组分别占目标群体的45%，而拒绝组为10%，他们将不会收到投放。

目标受众中的每个人都将收到一封电子邮件的一个版本，其主题行为以下两个版本之一：

* 一个是直接向新收藏集和图像促销10%的优惠。
* 另一个只是在广告中宣传特惠，而没有指定任何图像的10%的优惠。

此处的目标是根据收到的实验，查看收件人是否将与电子邮件进行交互。 因此，我们将选择 **[!UICONTROL Email Opens]** 作为此内容实验中的主要目标量度。

![](assets/content_experiment.png)

## 创建营销活动 {#campaign-experiment}

1. 从 **[!UICONTROL Campaigns]** 页面，单击 **[!UICONTROL Create campaign]**.

   ![](assets/content_experiment_1.png)

1. 选择 **[!UICONTROL Email]** 然后 **[!UICONTROL Surface]** 要用于此投放。 有关更多信息，请参阅 [通道曲面](../configuration/channel-surfaces.md) 页面。

   ![](assets/content_experiment_2.png)

1. 单击 **[!UICONTROL Create]**。

1. 设置 **[!UICONTROL Properties]** 投放内容：
   * **[!UICONTROL Title]**
   * **[!UICONTROL Description]**
   * **[!UICONTROL Category]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. 要开始内容实验，请将 **[!UICONTROL Content experiment]** 选项。 的 **[!UICONTROL Content experiment]** 菜单。

   ![](assets/content_experiment_3.png)

1. 设置 **[!UICONTROL Audience]** 和 **[!UICONTROL Schedule]** 参数。 [了解详情](create-campaign.md)

1. 单击 **[!UICONTROL Edit content]** 开始个性化您的 **[!UICONTROL Treatments]**.

   ![](assets/content_experiment_4.png)

## 创建您的治疗方案 {#treatment-experiment}

1. 从 **[!UICONTROL Edit content]** 窗口，添加 **[!UICONTROL Subject line]** ，然后单击 **[!UICONTROL Save]**.

   对于此处理，我们直接在主题行中指定选件。

   ![](assets/content_experiment_5.png)

1. 单击 **[!UICONTROL Email designer]** 以开始个性化投放。

   ![](assets/content_experiment_6.png)

1. 设计电子邮件后，单击 **[!UICONTROL Save]** 然后回到 **[!UICONTROL Edit content]** 窗口创建B。

1. 从 **[!UICONTROL More actions]** 按钮，单击 **[!UICONTROL Duplicate]**.

   您还可以选择从头开始单击 **[!UICONTROL Content experiment]** 按钮以访问高级选项，然后 **[!UICONTROL Add treatment]**.

   ![](assets/content_experiment_7.png)

1. 更改 **[!UICONTROL Title]** 以便更好地区分他们。

   ![](assets/content_experiment_8.png)

1. 选择链接到新创建的电子邮件投放 **[!UICONTROL Treatment]**.

1. 添加 **[!UICONTROL Subject line]** 投放。

   对于此处理方式，我们选择不在 **[!UICONTROL Subject line]**.

   ![](assets/content_experiment_9.png)

1. 单击 **[!UICONTROL Email designer]** 以根据需要进一步个性化B级投放。

个性化处理后，即可开始配置内容实验。

## 配置内容实验 {#configure-experiment}

1. 当这两个投放都进行了个性化后， **[!UICONTROL Edit content]** 窗口，选择 **[!UICONTROL Configure content experiment]**.

   ![](assets/content_experiment_10.png)

1. 选择要为实验设置的目标。

   对于我们的实验，我们选择 **[!UICONTROL Email open]** 以测试收件人在促销代码位于主题行中时是否会打开其电子邮件。

   ![](assets/content_experiment_11.png)

1. 选择添加 **[!UICONTROL Holdout]** 组到您的投放。 此群组将不会从此营销策划接收任何内容。

   打开切换栏将自动获取您群体的10%，您可以根据需要调整此百分比。

   ![](assets/content_experiment_12.png)

1. 然后，您可以选择为每个 **[!UICONTROL Treatment]** 或者只是打开 **[!UICONTROL Distribute evenly]** 切换栏。

   ![](assets/content_experiment_13.png)

1. 单击 **[!UICONTROL Save]** 设置配置时。

1. 内容实验准备就绪后，您可以单击 **[!UICONTROL Review to activate]** 以显示营销活动摘要。 如果有任何参数不正确或缺失，则会显示警报。

   ![](assets/content_experiment_15.png)

1. 检查营销活动配置是否正确，然后单击 **[!UICONTROL Activate]** 启动它。

   ![](assets/content_experiment_14.png)

在配置实验和营销活动后，您可以使用营销活动报表跟踪投放成功与否。

## 目标报告 {#objectives-global}

>[!AVAILABILITY]
>
>内容实验功能当前仅适用于一组组织（有限可用性）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/performance_report.gif)

的 **[!UICONTROL Objectives]** 选项卡，通过定位一个特定量度来优化投放报表。

的 **[!UICONTROL Objectives]** 已列出，链接到 **[!UICONTROL Datasets]** 定义与系统的连接以检索其他信息。 内置列表 **[!UICONTROL Objectives]** 可用，但您可以通过添加新来添加自己的 **[!UICONTROL Dataset]**. 有关详细过程，请参阅此 [部分](reporting-configuration.md).

选择要定位的目标后，这两个 **[!UICONTROL Performance overview]** 和 **[!UICONTROL Campaign objective]** 小组件将提供您交付性能的详细摘要。

使用 **[!UICONTROL Campaign objective]** 小组件中，您还可以选择将主要目标与其他量度进行比较。

请注意，如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的更多信息，请参阅此内容 [部分](../reports/global-report.md#modify-dashboard).

## 实验报表 {#experimentation-global}

>[!AVAILABILITY]
>
>内容实验功能当前仅适用于一组组织（有限可用性）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/experimentation_report_3.png)

从营销策划 **[!UICONTROL Global report]**, **[!UICONTROL Experimentation]** 选项卡详细列出了与每个变体的执行方式以及是否存在最佳执行者相关的主要信息。

请注意，定义最佳表演可能需要一些时间，它将由此图标表示 ![](assets/experimentation_report_1.png).

的 **[!UICONTROL Experiment result]** 小组件详细介绍每个变体的性能。 您可以通过从 **[!UICONTROL Baseline]** 下拉菜单。 最佳待遇将用星形图标表示。

下表显示了以下量度：

* **[!UICONTROL Profiles]**:针对此治疗的用户档案数。

* **[!UICONTROL Unique outbound clicks]**:出站渠道的总点击次数。

* **[!UICONTROL Count per profile]**:实验目标量度的总值除以用户档案数。

* **[!UICONTROL Confidence interval]**:基线与最佳处理之间性能差异的百分比。 [了解详情](../campaigns/experiment-calculations.md#confidence-intervals)。

* **[!UICONTROL Average lift]**:给定治疗相对于基准线的转化率提高的百分比。 [了解详情](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confidence]**:有证据表明，给定治疗与基准治疗相同。 [了解详情](../campaigns/experiment-calculations.md#understand-confidence)

要深入了解这些结果以及如何解释它们，请参阅 [本页](../campaigns/get-started-experiment.md#interpret-results).
