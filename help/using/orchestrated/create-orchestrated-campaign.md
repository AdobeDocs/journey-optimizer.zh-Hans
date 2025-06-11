---
solution: Journey Optimizer
product: journey optimizer
title: 使用Journey Optimizer创建和计划编排的营销活动
description: 了解如何使用Adobe Journey Optimizer创建编排的活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 435b4a7eee9428c7f0efeb62c72b39c0e2aaabba
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 13%

---


# 创建和计划编排的营销活动 {#create-first-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="协同营销活动列表"
>abstract="**编排**&#x200B;选项卡列出了所有编排的营销活动。 单击协同营销活动的名称即可对其进行编辑。使用&#x200B;**创建协同营销活动**&#x200B;按钮，添加新的协同营销活动。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库  | 编排的营销活动活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md) | [创建编排营销活动的关键步骤](gs-campaign-creation.md)<br/><br/><b>[创建和计划营销活动](create-orchestrated-campaign.md)</b><br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[发送包含编排营销活动的消息](send-messages.md)<br/><br/>[开始和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[And-join](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

正在进行文档

>[!ENDSHADEBOX]

## 创建营销活动 {#create}

要创建编排的营销活动，请执行以下步骤：

1. 浏览到&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，选择&#x200B;**[!UICONTROL 业务流程]**&#x200B;选项卡，然后选择&#x200B;**[!UICONTROL 创建营销活动]**。

   ![](assets/inventory-create.png)

1. 输入编排的营销活动的名称。 此外，我们强烈建议您在专用字段中添加描述。

1. （可选）使用&#x200B;**标记**&#x200B;字段将Adobe Experience Platform统一标记分配给您编排的营销活动。 这样，您就可以轻松地对营销活动进行分类，并改进营销活动列表中的搜索。[了解如何使用标记](../start/search-filter-categorize.md#tags)。

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;按钮进行确认。


现在，您的编排活动已创建并在活动列表中可用。 您可以随时通过单击促销活动画布中的![促销活动设置图标](assets/do-not-localize/campaign-settings.svg)图标来更改这些属性。


## 计划营销活动 {#schedule}

默认情况下，编排的营销活动在手动激活后开始，并在执行活动后立即结束。

如果不想在活动激活后立即执行编排的活动，则可以指定活动应执行的日期和时间。 您还可以根据各种条件以固定频率执行营销活动。

要配置营销活动计划，请打开编排的营销活动，然后单击&#x200B;**[!UICONTROL 尽快]**&#x200B;按钮。

![](assets/create-schedule.png)

<!--In the Execution frequency field, select 

time zone

daily, weekly, monthly
several times a day based on specific hours or periodically

recurring frequencies (all except as soon and once)
preview launch times
validity period

>[!NOTE]
>
>When scheduling campaigns in [!DNL Adobe Journey Optimizer], ensure your start date/time aligns with the desired first delivery. For recurring campaigns, if the initial scheduled time has already passed, the campaigns will roll over to the next available time slot according to their recurrence rules.

## Work with orchestrated campaign templates {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="Orchestrated campaign templates"
>abstract="Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaign."

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="Orchestrated campaign properties"
>abstract="Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaigns. In this screen, enter the label of the orchestrated campaign template and configure its settings such as its internal name, folder and execution folders, timezone, and supervisor group."

Orchestrated campaign templates contain pre-configured settings and activities which can be reused for creating new orchestrated campaigns. You can select the template of your orchestrated campaign from the orchestrated campaign properties, when creating an orchestrated campaign. An empty template is provided by default.

You can create a template from an existing orchestrated campaign, or create a new template from scratch. Both methods are detailed below.

>[!BEGINTABS]

>[!TAB Create a template from an existing orchestrated campaign]

To create an orchestrated campaign template from an existing orchestrated campaign, follow these steps:

1. Open to the **Campaign** menu and browse to the orchestrated campaign to save as a template.
1. Click the three dots on the right of the name of the orchestrated campaign, and choose **Copy as template**.
1. In the popup window, confirm the template creation.
1. In the orchestrated campaign template canvas, check, add, and configure the activities as needed.
1. Browse to the settings, from the **Settings** button, to change the name of the orchestrated campaign template, and enter a description.
1. Select the **folder** and **execution folder** of the template. The folder is the location where the orchestrated campaign template is saved. The execution folder is the folder where orchestrated campaigns created based on this template are saved.
1. Save your changes. 

The orchestrated campaign template is now available in the template list. You can create an orchestrated campaign based on this template. This orchestrated campaign will be pre-configured with the settings and activities defined in the template.


>[!TAB Create a template from scratch]


To create an orchestrated campaign template from scratch, follow these steps:

1. Open to the **Campaign** menu and browse to the **Templates** tab. You can see the list of available orchestrated campaign templates.
1. Click the **[!UICONTROL Create template]** button in the upper-right corner of the screen.
1. Enter the label and open the additional options to enter a description of your orchestrated campaign template.
1. Select the folder and execution folder of the template. The folder is the location where the orchestrated campaign template is saved. The execution folder is the folder where orchestrated campaigns created based on this template are saved.
1. Click the **Create** button to confirm your settings.
1. In the orchestrated campaign template canvas, add and configure the activities as needed.

     ![](assets/wf-template-activities.png){zoomable="yes"}

1. Save your changes. 

The orchestrated campaign template is now available in the template list. You can create an orchestrated campaign based on this template. This orchestrated campaign will be pre-configured with the settings and activities defined in the template.

>[!ENDTABS]






## Next steps {#next}

Once your campaign configuration and content are ready, you can review and activate it. [Learn more](review-activate-campaign.md)

-->