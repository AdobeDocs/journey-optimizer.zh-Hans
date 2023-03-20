---
solution: Journey Optimizer
product: journey optimizer
title: 创建内容实验
description: 了解如何在营销活动中创建内容实验
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
keywords: 内容，实验，多个，受众，处理
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
badge: label="Beta" type="Informitive"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 5%

---

# 创建内容体验 {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="内容体验"
>abstract="您可以选择更改投放内容、主题或发件人，以定义多种投放处理方式并确定适合受众的最佳组合。"

>[!BEGINSHADEBOX]

您将在本文档中找到的内容：

* [内容体验入门](get-started-experiment.md)
* **[创建内容体验](content-experiment.md)**
* [了解统计计算](experiment-calculations.md)
* [配置实验报表](reporting-configuration.md)
* [实验报表中的统计计算](experiment-report-calculations.md)

>[!ENDSHADEBOX]

Journey Optimizer内容实验允许您定义多种交付处理方式，以便衡量哪种交付处理方式对目标受众的效果最佳。 您可以选择更改投放内容、主题或发件人。 兴趣的受众随机分配给每个治疗，以确定哪个治疗在指定量度方面效果最佳。

>[!NOTE]
>
>在开始内容实验之前，请确保为自定义数据集设置了报表配置。 有关详细信息，请参阅[此部分](reporting-configuration.md)。

在以下示例中，投放目标已被拆分为两个组，每个组分别占目标群体的45%，而拒绝组为10%，他们将不会收到投放。

目标受众中的每个人都将收到一封电子邮件的一个版本，其主题行为以下两个版本之一：

* 一个是直接向新收藏集和图像促销10%的优惠。
* 另一个只是在广告中宣传特惠，而没有指定任何图像的10%的优惠。

此处的目标是根据收到的实验，查看收件人是否将与电子邮件进行交互。 因此，我们将选择 **[!UICONTROL 电子邮件打开次数]** 作为此内容实验中的主要目标量度。

![](assets/content_experiment.png)

## 创建营销活动 {#campaign-experiment}

1. 从 **[!UICONTROL 促销活动]** 页面，单击 **[!UICONTROL 创建营销活动]**.

   ![](assets/content_experiment_1.png)

1. 选择您的渠道，然后选择 **[!UICONTROL 曲面]** 要用于此投放，请单击 **[!UICONTROL 创建]**. 有关更多信息，请参阅 [通道曲面](../configuration/channel-surfaces.md) 页面。

   ![](assets/content_experiment_2.png)

1. 设置 **[!UICONTROL 属性]** 投放内容：
   * **[!UICONTROL 名称]**
   * **[!UICONTROL 描述]**

1. 定义要定位的受众。 为此，请单击 **[!UICONTROL 选择受众]** 按钮以显示可用的Adobe Experience Platform区段列表。 [了解有关区段的更多信息](../segment/about-segments.md)

   在 **[!UICONTROL 身份命名空间]** 字段中，选择要用于识别选定区段中个人的命名空间。 [了解详情](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. 在 **[!UICONTROL 操作跟踪]** 部分，指定是否要跟踪收件人对投放的反应：您可以跟踪点击和/或打开次数。

   一旦执行了营销活动，即可从营销活动报表访问跟踪结果。

1. 要在特定日期或定期频率执行营销活动，请配置 **[!UICONTROL 计划]** 中。 [了解详情](create-campaign.md)

1. 单击 **[!UICONTROL 编辑内容]** 以开始个性化投放。 [了解详情](../email/content-from-scratch.md)

   ![](assets/content_experiment_17.png)

1. 从 **[!UICONTROL 编辑内容]** 窗口，开始个性化处理A。

   对于此处理方式，我们将直接在主题行中指定特殊选件并添加个性化。

   ![](assets/content_experiment_5.png)

## 配置内容实验 {#configure-experiment}

1. 在您的投放进行个性化后，从Campaign摘要页面，单击 **[!UICONTROL 创建实验]** 以开始配置内容实验。

   ![](assets/content_experiment_3.png)

1. 选择 **[!UICONTROL 成功量度]** 你想为你的实验设定。

   对于我们的实验，我们选择 **[!UICONTROL 电子邮件打开]** 以测试收件人在促销代码位于主题行中时是否会打开其电子邮件。

   ![](assets/content_experiment_11.png)

1. 单击 **[!UICONTROL 添加治疗]** 以创造所需数量的新治疗。

   ![](assets/content_experiment_8.png)

1. 更改 **[!UICONTROL 标题]** 以便更好地区分他们。

1. 选择添加 **[!UICONTROL 维持]** 组到您的投放。 此群组将不会从此营销策划接收任何内容。

   打开切换栏将自动获取您群体的10%，您可以根据需要调整此百分比。

   ![](assets/content_experiment_12.png)

1. 然后，您可以选择为每个 **[!UICONTROL 治疗]** 或者只是打开 **[!UICONTROL 均匀分配]** 切换栏。

   ![](assets/content_experiment_13.png)

1. 单击 **[!UICONTROL 创建]** 设置配置时。

## 设计您的处理方法 {#treatment-experiment}

1. 从 **[!UICONTROL 编辑内容]** 窗口中，选择您的治疗B以更改内容。

   在此，我们选择不在 **[!UICONTROL 主题行]**.

   ![](assets/content_experiment_18.png)

1. 单击 **[!UICONTROL 编辑电子邮件正文]** 进一步个性化你的治疗B。

   ![](assets/content_experiment_9.png)

1. 设计理疗后，单击 **[!UICONTROL 更多操作]** 要访问与您的治疗相关的选项，请执行以下操作： **[!UICONTROL 重命名]**, **[!UICONTROL 复制]** 和 **[!UICONTROL 删除]**.

   ![](assets/content_experiment_7.png)

1. 如果需要，请访问 **[!UICONTROL 实验设置]** 菜单来更改您的处理配置。

   ![](assets/content_experiment_19.png)

1. 定义消息内容后，单击 **[!UICONTROL 模拟内容]** 按钮以控制投放的呈现，并使用测试用户档案检查个性化设置。 [了解详情](../email/preview.md)

1. 在内容实验准备就绪后，从Campaign摘要页面中，您可以单击 **[!UICONTROL 查看以激活]** 以显示营销活动摘要。 如果有任何参数不正确或缺失，则会显示警报。

   ![](assets/content_experiment_15.png)

1. 检查营销活动配置是否正确，然后单击 **[!UICONTROL 激活]** 启动它。

   ![](assets/content_experiment_14.png)

在配置实验和营销活动后，您可以使用营销活动报表跟踪投放成功与否。

## 目标报告 {#objectives-global}

>[!AVAILABILITY]
>
>内容实验功能当前仅适用于一组组织（有限可用性）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/performance_report.gif)

的 **[!UICONTROL 目标]** 选项卡，通过定位一个特定量度来优化投放报表。

的 **[!UICONTROL 目标]** 已列出，链接到 **[!UICONTROL 数据集]** 定义与系统的连接以检索其他信息。 内置列表 **[!UICONTROL 目标]** 可用，但您可以通过添加新来添加自己的 **[!UICONTROL 数据集]**. 有关详细过程，请参阅此 [部分](reporting-configuration.md).

选择要定位的目标后，这两个 **[!UICONTROL 性能概述]** 和 **[!UICONTROL 营销活动目标]** 小组件将提供您交付性能的详细摘要。

使用 **[!UICONTROL 营销活动目标]** 小组件中，您还可以选择将主要目标与其他量度进行比较。

请注意，如果需要，可以调整每个小组件的大小并将其删除。 有关此内容的更多信息，请参阅此内容 [部分](../reports/global-report.md#modify-dashboard).

## 实验报表 {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="成功指标"
>abstract="成功量度的总值（之前在创建实验时选择的量度）除以用户档案数。"

>[!AVAILABILITY]
>
>内容实验功能当前仅适用于一组组织（有限可用性）。 有关更多信息，请与您的 Adobe 代表联系。

![](assets/experimentation_report_3.png)

从营销策划 **[!UICONTROL 全局报告]**, **[!UICONTROL 实验]** 选项卡详细列出了与每个变体的执行方式以及是否存在最佳执行者相关的主要信息。

请注意，定义最佳表演可能需要一些时间，它将由此图标表示 ![](assets/experimentation_report_1.png).

的 **[!UICONTROL 实验结果]** 小组件详细介绍每个变体的性能。 您可以通过从 **[!UICONTROL 基线]** 下拉菜单。 最佳待遇将用星形图标表示。

下表显示了以下量度：

* **[!UICONTROL 用户档案]**:针对此治疗的用户档案数。

* **[!UICONTROL 独特出站点击]**:出站渠道的总点击次数。

* **[!UICONTROL 每个用户档案的计数]**:实验目标量度的总值除以用户档案数。

* **[!UICONTROL 置信区间]**:基线与最佳处理之间性能差异的百分比。 [了解详情](../campaigns/experiment-calculations.md#confidence-intervals)。

* **[!UICONTROL 平均提升度]**:给定治疗相对于基准线的转化率提高的百分比。 [了解详情](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL 置信度]**:有证据表明，给定治疗与基准治疗相同。 [了解详情](../campaigns/experiment-calculations.md#understand-confidence)

要深入了解这些结果以及如何解释它们，请参阅 [本页](../campaigns/get-started-experiment.md#interpret-results).
