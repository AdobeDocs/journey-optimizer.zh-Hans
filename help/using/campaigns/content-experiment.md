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
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '748'
ht-degree: 6%

---

# 创建内容试验 {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="内容体验"
>abstract="您可以选择改变投放内容、主题或发件人，以便定义多种投放处理方法并确定最适合您受众的组合。"

>[!NOTE]
>
>在开始内容试验之前，请确保为自定义数据集设置了报表配置。 有关详细信息，请参阅[此部分](reporting-configuration.md)。

Journey Optimizer内容实验允许您定义多种投放处理，以衡量哪种投放处理对目标受众的效果最佳。 您可以选择更改投放内容、主题或发件人。 感兴趣的受众被随机分配给每个处理，以确定哪个处理在指定的量度方面效果最佳。

在下面的示例中，投放目标被分为两个组，每个组代表目标人口的45%，而保留组占10%，他们将不接收投放。

目标受众中的每个人都会收到一个版本的电子邮件，其主题行是以下两个版本之一：

* 其中一个直接宣传新系列和图片的10%选件。
* 另一家公司只公布了特别优惠，没有提供任何图片，也没有指定10%的折扣。

此处的目标是查看收件人是否会根据收到的试验与电子邮件交互。 因此，我们将选择 **[!UICONTROL 电子邮件打开次数]** 作为此内容试验中的主要目标量度。

![](assets/content_experiment.png)

## 创建您的营销活动 {#campaign-experiment}

1. 从 **[!UICONTROL 营销活动]** 页面，单击 **[!UICONTROL 创建营销活动]**.

   ![](assets/content_experiment_1.png)

<!--
1. In the **[!UICONTROL Properties]** section, choose your **[!UICONTROL Campaign type]**:

    * **[!UICONTROL Scheduled]**: designed to send marketing messages and can be executed immediately or at a specified date.

    * **[!UICONTROL API-Triggered]**: designed to send transactional messages, such as password reset notifications or cart abandonment reminders. 
    
        To execute an API-triggered campaign, you will need to make an API call. [Learn more](api-triggered-campaigns.md)
-->
1. 选择您的渠道，然后选择 **[!UICONTROL 表面]** 要用于此投放并单击 **[!UICONTROL 创建]**. 有关详情，请参阅 [渠道表面](../configuration/channel-surfaces.md) 页面。

   在此示例中，我们选择使用电子邮件发送营销活动。

   ![](assets/content_experiment_2.png)

1. 设置 **[!UICONTROL 属性]** 您的交付内容：
   * **[!UICONTROL 名称]**
   * **[!UICONTROL 描述]**

1. 定义要定位的受众。 要执行此操作，请单击 **[!UICONTROL 选择受众]** 按钮以显示可用Adobe Experience Platform受众的列表。 [了解有关受众的更多信息](../audience/about-audiences.md)

   在 **[!UICONTROL 身份命名空间]** 字段中，选择要使用的命名空间，以便识别所选受众中的个人。 [了解详情](get-started-experiment.md#content-experiment-work)

   ![](assets/content_experiment_16.png)

1. 在 **[!UICONTROL 操作跟踪]** 部分，指定是否要跟踪收件人对投放的反应：您可以跟踪点击和/或打开。

   执行营销活动后，即可从营销活动报表访问跟踪结果。

1. 要在特定日期或按重复频率执行活动，请配置 **[!UICONTROL 计划]** 部分。 [了解详情](create-campaign.md)

1. 单击 **[!UICONTROL 编辑内容]** 以开始个性化您的投放。

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

配置试验性和营销活动后，您可以使用Campaign报告跟踪投放的成功情况。 [了解详情](../reports/campaign-global-report.md#experimentation-report)
