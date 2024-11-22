---
title: Publish和管理基于代码的体验
description: 了解如何在Journey Optimizer中发布和停止基于代码的体验
feature: Code-based Experiences
topic: Content Management
role: User
level: Experienced
source-git-commit: bf0a6fa496a08348be16896a7f2313882eb97c06
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 1%

---

# 管理基于代码的体验 {#publish-code-based}

## 让基于代码的体验上线 {#code-based-experience-live}

>[!IMPORTANT]
>
> 如果您的营销活动受批准政策的约束，则需要请求批准才能激活基于代码的体验。 [了解详情](../test-approve/gs-approval.md)

定义基于代码的体验并根据需要使用[基于代码的编辑器](create-code-based.md#edit-code)编辑内容后，您可以激活历程或营销活动以使更改对受众可见。

您还可以在基于代码的体验内容上线之前对其进行预览。 [了解详情](test-code-based.md)

>[!NOTE]
>
>如果您激活基于代码的历程/营销活动，影响的页面与另一个已上线的历程或营销活动相同，则所有更改将应用于您的内容。
>
>如果多个基于代码的历程或营销活动更新了内容的相同元素，则优先级最高的历程/营销活动优先。

一旦您的基于代码的历程或营销活动上线，您的应用程序实施团队将负责发出显式API或SDK调用，以获取选定[基于代码的体验配置](code-based-configuration.md)中定义的表面的内容。 在[本节](code-based-implementation-samples.md)中了解关于不同客户实施的更多信息。

### Publish基于代码的历程 {#publish-code-based-journey}

要在历程中实时提供基于代码的体验，请执行以下步骤。

1. 验证您的历程是否有效并且没有错误。 [了解详情](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)

1. 在历程中，选择位于右上角的下拉菜单中的&#x200B;**[!UICONTROL Publish]**&#x200B;选项。

   ![](assets/code-based-journey-publish.png)

   >[!NOTE]
   >
   >在[本节](../building-journeys/publishing-the-journey.md)中了解有关发布历程的更多信息。

您的基于代码的历程处于&#x200B;**[!UICONTROL 实时]**&#x200B;状态，现在对所选受众可见。 历程的每个收件人都可以看到您的修改。

>[!NOTE]
>
>单击&#x200B;**[!UICONTROL Publish]**&#x200B;后，最多可能需要15分钟才能使更改生效。

### 激活基于代码的营销活动 {#activate-code-based-campaign}

1. 从基于代码的营销活动中，选择&#x200B;**[!UICONTROL 审阅以激活]**。

   ![](assets/code-based-campaign-review.png)

1. 检查并编辑内容、属性、配置、受众和计划（如果需要）。

1. 选择&#x200B;**[!UICONTROL 激活]**。

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >在[此部分](../campaigns/review-activate-campaign.md)中了解关于激活营销活动的更多信息。

您的基于代码的营销活动处于&#x200B;**[!UICONTROL 实时]**&#x200B;状态，现在对所选受众可见。 营销活动的每个收件人都可以看到您向内容添加的修改。

>[!NOTE]
>
>单击&#x200B;**[!UICONTROL 激活]**&#x200B;后，最多可能需要15分钟才能使更改生效。
>
>如果您为基于代码的营销活动定义了计划，则在到达开始日期和时间之前，该计划的状态为&#x200B;**[!UICONTROL 已计划]**。

## 停止基于代码的历程或营销活动 {#stop-code-based-experience}

当基于代码的体验处于实时状态时，您可以停止它以防止受众看到您的修改。 请按照以下步骤操作。

1. 从相应的列表中选择实时历程或营销策划。

1. 根据您的具体情况执行相关操作：

   * 从营销活动顶部菜单中，选择&#x200B;**[!UICONTROL 停止营销活动]**。

     ![](assets/code-based-campaign-stop.png)

   * 从历程顶部菜单中，单击&#x200B;**[!UICONTROL 更多]**&#x200B;按钮，然后选择&#x200B;**[!UICONTROL 停止]**。

     ![](assets/code-based-journey-stop.png)

1. 您添加的修改将不再对您定义的受众可见。

>[!NOTE]
>
>停止基于代码的历程或营销活动后，您将无法再次编辑或激活它。 您只能复制它并激活复制的历程/营销策划。

<!--Reporting TBC

## Check the code-based experience reports {#check-code-based-reports}

Once your code-based experience is live, you can check the **[!UICONTROL Code-based]** tab of the  [Journey report](../reports/journey-global-report-cja.md#web-cja) and [Campaign report](../reports/campaign-global-report-cja.md#web) to compare elements such as the number of experiences delivered to your audience, and the number of engagements with your content.-->

<!--## Code-based reports

You can access code-based journey or campaign reports from the summary screen.

Global reports display events that occurred at least two hours ago and cover events over a selected time period. In comparison, Live reports focus on events that took place within the past 24 hours, with a minimum time interval of two minutes from the event occurrence.

### Code-based live report {#live-report-code-based}

From your campaign **[!UICONTROL Live report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages. [Learn more on live report](../reports/campaign-live-report.md)

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your code-based experiences, such as:

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**:  total number of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (impressions, unique impressions and interactions) for the last 24 hours.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.
+++

### Code-based global report {#global-report-code-based}

Code-based campaign global report can be accessed directly from your journey or campaign with the **[!UICONTROL View report]** button. [Learn more on global report](../reports/campaign-global-report-cja.md)

From your Campaign **[!UICONTROL Global report]**, the **[!UICONTROL Code-based experience]** tab details the main information relative to your apps or web pages.

![](assets/code-based-campaign-global-report.png)

Add image TBC

+++Learn more on the different metrics and widgets available for the Code-based experience report.

The **[!UICONTROL Code-based experience performance]** KPIs detail the main information relative to your visitors' engagement with your experiences, such as:

* **[!UICONTROL Unique impressions]**: number of unique users to whom the experience was delivered.

* **[!UICONTROL Impressions]**: total number of experiences delivered to all users.

* **[!UICONTROL Interactions]**: percentage of engagements with your app/page. This includes any actions taken by the users, such as clicks or any other interactions.

The **[!UICONTROL Code-based experience summary]** graph shows the evolution of your experiences (unique impressions, impressions and interactions) for the concerned period.

TBC: The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.
+++

-->

