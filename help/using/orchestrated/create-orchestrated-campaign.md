---
solution: Journey Optimizer
product: journey optimizer
title: 使用Journey Optimizer创建和计划编排的营销活动
description: 了解如何使用Adobe Journey Optimizer创建和计划编排的营销活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 779c90f0be57749a63da103d18cc642106c5f837
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 11%

---


# 创建并安排编排式营销活动的执行时间 {#create-first-campaign}

+++ 目录

| 欢迎使用编排的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | <b>[创建和计划营销活动](create-orchestrated-campaign.md)</b><br/><br/>[编排活动](orchestrate-activities.md)<br/><br/>[启动并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重新定位](retarget.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[并加入](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++
<br/>

>[!BEGINSHADEBOX]

正在进行文档

>[!ENDSHADEBOX]

在[!DNL Adobe Journey Optimizer]中创建编排的营销活动，并配置其执行计划以控制其启动时间和运行频率。 选择在特定的日期和时间立即启动促销活动，或者使用灵活的计划选项（如每天、每周或每月频率）定期启动促销活动。

## 创建营销活动 {#create}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="编排式营销活动列表"
>abstract="**编排**&#x200B;标签页列出了所有编排式营销活动。单击协同营销活动的名称即可对其进行编辑。使用&#x200B;**创建协同营销活动**&#x200B;按钮，添加新的协同营销活动。"

要创建编排的营销活动，请执行以下步骤：

1. 转到&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，选择&#x200B;**[!UICONTROL 业务流程]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。

   ![](assets/inventory-create.png)

1. 输入营销活动的名称和描述。

1. *（可选）*&#x200B;使用&#x200B;**[!UICONTROL 标记]**&#x200B;字段将Adobe Experience Platform统一标记分配给您的营销活动。 这使您能够轻松地对它们进行分类，并从编排的营销活动列表中改进搜索。 [了解如何使用标记](../start/search-filter-categorize.md#tags)。

1. 单击&#x200B;**[!UICONTROL 创建]**。

现在，您的编排活动已创建并显示在编排的活动列表中。 您可以随时通过单击促销活动画布中的![促销活动设置图标](assets/do-not-localize/campaign-settings.svg)图标来更新这些属性。

## 计划营销活动 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="调度程序"
>abstract="作为营销活动经理，您可以将活动设定为在特定时间自动启动，从而实现营销沟通的精准时机控制和精确的受众定位。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="调度程序有效期"
>abstract="可定义调度程序的有效期。它可为永久（默认），也可一直有效至特定日期。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="调度程序选项"
>abstract="定义调度程序的频率。可在特定时刻执行它、每天、每周或每月执行它一次或多次。"

默认情况下，编排的营销活动在手动激活时开始，并在执行其关联活动后结束。 如果您希望延迟执行或定期运行该活动，则可以为该活动定义计划。

在计划编排的营销活动时，请考虑以下最佳实践，以确保最佳性能和预期行为：

* 请勿将编排好的营销活动安排为每15分钟运行一次以上，因为它可能会影响整体系统性能，并在数据库中创建块。
* 如果要在编排的营销活动中发送一次性消息，可将其设置为运行&#x200B;**一次**。
* 如果要在编排的活动中发送定期消息，则需要使用&#x200B;**计划**&#x200B;选项并设置执行频率。 循环投放活动不允许您定义计划。

要配置活动计划，请执行以下步骤：

1. 打开营销活动，然后单击&#x200B;**[!UICONTROL 尽快]**&#x200B;按钮。

   ![](assets/create-schedule.png)

1. 选择活动的执行频率，然后配置可用选项。 设置因所选频率而异：

   +++一次

   在指定的日期和时间运行一次营销活动。

   * **[!UICONTROL 日期]**：选择应执行营销活动的日期。
   * **[!UICONTROL 时间]**：选择应执行营销活动的特定时间。

   +++

   +++每日

   在每天或选定的日期运行活动。

   * **[!UICONTROL 每日重复周期]**：选择营销活动运行的频率：
      * **[!UICONTROL 每天]**：在一周的每一天（包括周末）执行营销活动。
      * **[!UICONTROL 工作日]**：仅在星期一到星期五执行营销活动。
      * **[!UICONTROL 在特定时间段内]**：在定义的日期范围内（例如，从7月1日至7月15日）每天执行营销活动。 营销活动不会在此范围之外运行。
      * **[!UICONTROL 在每周的选定日期]**：仅在每周的指定日期（例如，周一、周三、周五）执行营销活动。

   * **[!UICONTROL 开始时间]**：定义每天应执行营销活动的时间。

   +++

   +++一天几次

   在同一天内多次运行活动。 您可以选择特定时间或设置周期频率。

   * **[!UICONTROL 选定的小时数]**：选择营销活动应运行的特定时间，并配置其每日重复周期（在一周的每一天或某些天执行）。
   * **[!UICONTROL 定期]**：选择每n分钟或每小时运行一次营销活动。 您还可以在允许执行的一天内定义时间范围。

   +++

   +++每周

   每周运行一次该营销活动，并提供指定日期的选项。

   * **[!UICONTROL 频率]**：选择营销活动的运行频率（例如，每周、每两周）。
   * **[!UICONTROL 从日期]**&#x200B;开始：选择循环开始的日期。
   * **[!UICONTROL 每日重复]**：选择一周中的特定日期执行（例如，每个星期一和星期四）。
   * **[!UICONTROL 开始时间]**：设置活动在选定日期应执行的时间。

   +++

   +++每月

   每月运行一次营销活动，并包含指定日期的选项。

   * **[!UICONTROL 每月重复]**：选择营销活动是每月运行还是仅在特定月份运行。
   * **[!UICONTROL 每日重复周期]**：
      * **[!UICONTROL 每天]**：在每月每个日历日（包括周末）执行营销活动。
      * **[!UICONTROL 每月的最后一天]**：仅在每月的最后一个日历日（如1月31日、2月28/29日）执行营销活动。
      * **[!UICONTROL 当月的特定日期（例如，15日）]**：在指定的日期（例如，每个月的15日）执行营销活动。
      * **[!UICONTROL 一周的第一天/最后一天]**（例如，第一个星期一）：      在指定的工作日（例如，每周的15日）执行营销活动。
      * **[!UICONTROL 每周的选定日期]**：在指定日期执行营销活动。

   * **[!UICONTROL 开始时间]**：设置活动应执行的时间。

   +++

1. 使用&#x200B;**[!UICONTROL 有效期]**&#x200B;设置定义特定的开始和结束日期，将营销活动的执行限制在有限的时间范围内。

1. 对于定期计划，请单击&#x200B;**[!UICONTROL 预览启动时间]**&#x200B;按钮以根据当前配置预览即将执行的确切日期和时间。 这有助于在激活之前验证计划，并确保活动按预期运行。

>[!NOTE]
>
>在[!DNL Adobe Journey Optimizer]中计划营销活动时，请确保您的开始日期/时间与所需的首次投放一致。 对于定期活动，如果已超过初始计划时间，则活动将根据定期规则滚动到下一个可用时间段。

在下方的示例中，将活动配置为从2025年10月1日至2026年1月1日，编排的活动每天在早上9点和12点运行两次。

![调度程序配置为在早上9点和12点每天运行两次活动](assets/scheduler-sample.png){width="50%" align="left"}

## 后续步骤 {#next}

配置营销活动设置和计划后，您就可以开始编排将执行的不同任务。 [了解如何编排营销活动](../orchestrated/orchestrate-activities.md)
