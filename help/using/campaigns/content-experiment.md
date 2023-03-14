---
solution: Journey Optimizer
product: journey optimizer
title: 创建内容试验
description: 了解如何在营销活动中创建内容试验
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: 内容，试验，多个，受众，处理
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
badge: label="Beta" type="Informational"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 5%

---

# 创建内容体验 {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="内容体验"
>abstract="您可以选择更改投放内容、主题或发件人，以定义多个投放处理并确定适合受众的最佳组合。"

>[!BEGINSHADEBOX]

您将在本文档中找到以下内容：

* [内容体验入门](get-started-experiment.md)
* **[创建内容体验](content-experiment.md)**
* [了解统计计算](experiment-calculations.md)
* [配置实验报表](reporting-configuration.md)
* [实验报表中的统计计算](experiment-report-calculations.md)

>[!ENDSHADEBOX]

Journey Optimizer内容实验允许您定义多种投放处理，以衡量哪种投放处理对目标受众的效果最佳。 您可以选择更改投放内容、主题或发件人。 感兴趣的受众被随机分配给每个处理，以确定哪个处理在指定的量度方面效果最佳。

>[!NOTE]
>
>在开始内容试验之前，请确保为自定义数据集设置了报表配置。 有关详细信息，请参阅[此部分](reporting-configuration.md)。

在下面的示例中，投放目标被分为两个组，每个组代表目标人口的45%，而保留组占10%，他们将不接收投放。

目标受众中的每个人都会收到一个版本的电子邮件，其主题行是以下两个版本之一：

* 其中一个直接宣传新系列和图片的10%选件。
* 另一家公司只公布了特别优惠，没有提供任何图片，也没有指定10%的折扣。

此处的目标是查看收件人是否会根据收到的试验与电子邮件交互。 因此，我们将选择 **[!UICONTROL 电子邮件打开次数]** 作为此内容试验中的主要目标量度。

![](assets/content_experiment.png)

## 创建您的营销活动 {#campaign-experiment}

1. 从 **[!UICONTROL 营销活动]** 页面，单击 **[!UICONTROL 创建营销活动]**.

   ![](assets/content_experiment_1.png)

1. 选择您的渠道，然后选择 **[!UICONTROL 表面]** 要用于此投放并单击 **[!UICONTROL 创建]**. 有关详情，请参阅 [渠道表面](../configuration/channel-surfaces.md) 页面。

   ![](assets/content_experiment_2.png)

1. 设置 **[!UICONTROL 属性]** 您的交付内容：
   * **[!UICONTROL 名称]**
   * **[!UICONTROL 说明]**

1. 定义要定位的受众。 要执行此操作，请单击 **[!UICONTROL 选择受众]** 按钮以显示可用Adobe Experience Platform区段的列表。 [了解有关区段的更多信息](../segment/about-segments.md)

   在 **[!UICONTROL 身份命名空间]** 字段，选择要使用的命名空间，以标识所选区段中的个人。 [了解详情](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. 在 **[!UICONTROL 操作跟踪]** 部分，指定是否要跟踪收件人对投放的反应：您可以跟踪点击和/或打开。

   执行营销活动后，即可从营销活动报表访问跟踪结果。

1. 要在特定日期或按重复频率执行活动，请配置 **[!UICONTROL 计划]** 部分。 [了解详情](create-campaign.md)

1. 单击 **[!UICONTROL 编辑内容]** 以开始个性化您的投放。 [了解详情](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. 从 **[!UICONTROL 编辑内容]** 窗口，开始个性化处理A。

   对于此处理，我们将直接在主题行中指定特殊选件并添加个性化。

   ![](assets/content_experiment_5.png)

## 配置内容试验 {#configure-experiment}

1. 个性化投放后，从Campaign摘要页面，单击 **[!UICONTROL 创建试验]** 以开始配置内容试验。

   ![](assets/content_experiment_3.png)

1. 选择 **[!UICONTROL 成功量度]** 要为试验设置。

   对于我们的试验，我们选择 **[!UICONTROL 电子邮件打开]** 测试如果促销代码在主题行中，收件人是否会打开其电子邮件。

   ![](assets/content_experiment_11.png)

1. 单击 **[!UICONTROL 添加处理]** 创造所需数量的新治疗。

   ![](assets/content_experiment_8.png)

1. 更改 **[!UICONTROL 标题]** 以更好地区分他们。

1. 选择以添加 **[!UICONTROL 维持]** 分组到您的投放。 此组将不会收到此营销活动中的任何内容。

   打开切换栏将自动获取您群体的10%，您可以根据需要调整此百分比。

   ![](assets/content_experiment_12.png)

1. 然后，您可以选择为每个报表包分配精确百分比 **[!UICONTROL 处理]** 或者只需打开 **[!UICONTROL 均匀分布]** 切换栏。

   ![](assets/content_experiment_13.png)

1. 单击 **[!UICONTROL 创建]** 设置您的配置时。

## 设计您的待遇 {#treatment-experiment}

1. 从 **[!UICONTROL 编辑内容]** 窗口中，选择您的处理B以更改内容。

   在此，我们选择不在以下位置指定选件： **[!UICONTROL 主题行]**.

   ![](assets/content_experiment_18.png)

1. 单击 **[!UICONTROL 编辑电子邮件正文]** 进一步个性化您的治疗B。

   ![](assets/content_experiment_9.png)

1. 设计处理方案后，单击 **[!UICONTROL 更多操作]** 要访问与处理相关的选项，请执行以下操作： **[!UICONTROL 重命名]**， **[!UICONTROL 复制]** 和 **[!UICONTROL 删除]**.

   ![](assets/content_experiment_7.png)

1. 如果需要，访问 **[!UICONTROL 试验设置]** 菜单更改您的处理配置。

   ![](assets/content_experiment_19.png)

1. 定义消息内容后，单击 **[!UICONTROL 模拟内容]** 按钮来控制投放的呈现，并使用测试用户档案检查个性化设置。 [了解详情](../email/preview.md)

1. 当内容试验准备就绪时，您可以从Campaign摘要页面单击 **[!UICONTROL 查看以激活]** 以显示营销活动的摘要。 如果有任何参数不正确或缺失，将显示警报。

   ![](assets/content_experiment_15.png)

1. 检查营销活动是否正确配置，然后单击 **[!UICONTROL 激活]** 来启动它。

   ![](assets/content_experiment_14.png)

配置试验性和营销活动后，您可以使用Campaign报告跟踪投放的成功情况。

## 目标报表 {#objectives-global}

>[!AVAILABILITY]
>
>内容试验功能目前仅适用于一组组织（限量发布）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/performance_report.gif)

此 **[!UICONTROL 目标]** 利用Campaign报告的Tab选项卡，可通过定位一个特定指标来更好地优化投放报告。

此 **[!UICONTROL 目标]** 列表已链接到 **[!UICONTROL 数据集]** 来定义与系统的连接以检索附加信息。 内置列表 **[!UICONTROL 目标]** 可用，但您可以通过添加新的来添加您自己的 **[!UICONTROL 数据集]**. 有关详细过程，请参阅此 [部分](reporting-configuration.md).

选择完要定位的目标后，两项 **[!UICONTROL 性能概述]** 和 **[!UICONTROL 营销活动目标]** 构件将提供投放性能的详细摘要。

使用 **[!UICONTROL 营销活动目标]** 构件，您还可以选择将您的主要目标与其他指标进行比较。

请注意，如果需要，可以调整每个小部件的大小并将其删除。 有关此内容的更多信息，请参阅此 [部分](../reports/global-report.md#modify-dashboard).

## 试验报告 {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="成功指标"
>abstract="之前创建实验时选择的成功量度的总值除以配置文件数。"

>[!AVAILABILITY]
>
>内容试验功能目前仅适用于一组组织（限量发布）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/experimentation_report_3.png)

来自您的营销活动 **[!UICONTROL 全局报告]**，则 **[!UICONTROL 试验]** Tab详细列出了有关每个变体的表现以及是否有最佳表现的主要信息。

请注意，定义最佳业绩者可能需要一些时间，它将由此图标表示 ![](assets/experimentation_report_1.png).

此 **[!UICONTROL 实验结果]** 构件详细说明每个变体的性能。 通过从中选择处理方法之一，可以更改基线 **[!UICONTROL 基线]** 下拉列表。 最佳处理方式将以星形图标表示。

下表显示了以下量度：

* **[!UICONTROL 配置文件]**：针对此处理的用户档案数。

* **[!UICONTROL 独特出站点击次数]**：跨出站渠道的点击总数。

* **[!UICONTROL 每个配置文件的计数]**：试验目标指标的总值除以配置文件数。

* **[!UICONTROL 置信区间]**：基线和最佳业绩处理之间的业绩差异百分比。 [了解详情](../campaigns/experiment-calculations.md#confidence-intervals)。

* **[!UICONTROL 平均提升度]**：给定疗法的转化率比基线提高的百分比。 [了解详情](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL 置信度]**：表明给定治疗与基线治疗相同的证据。 [了解详情](../campaigns/experiment-calculations.md#understand-confidence)

要深入了解这些结果以及如何解释这些结果，请参阅 [此页面](../campaigns/get-started-experiment.md#interpret-results).
