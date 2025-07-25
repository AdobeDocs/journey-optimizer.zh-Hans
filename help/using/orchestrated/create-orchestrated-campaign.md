---
solution: Journey Optimizer
product: journey optimizer
title: 使用 Journey Optimizer 创建和计划精心策划的营销活动
description: 了解如何使用 Adobe Journey Optimizer 创建和计划精心策划的营销活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 4461d3fdf6e61b7d2593027250dce65bba5fbd77
workflow-type: tm+mt
source-wordcount: '1232'
ht-degree: 84%

---


# 创建和计划精心策划的营销活动 {#create-first-campaign}

+++ 目录

| 欢迎了解精心策划的营销活动 | 启动第一个精心策划的营销活动 | 查询数据库 | 精心策划的营销活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>创建和管理关系架构和数据集：</br> <ul><li>[架构和数据集入门](gs-schemas.md)</li><li>[手动架构](manual-schema.md)</li><li>[文件上载架构](file-upload-schema.md)</li><li>[摄取数据](ingest-data.md)</li></ul>[访问和管理编排的营销活动](access-manage-orchestrated-campaigns.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | <b>[创建和计划营销活动](create-orchestrated-campaign.md)</b><br/><br/>[精心策划活动](orchestrate-activities.md)<br/><br/>[启动和监控营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用规则生成器](orchestrated-rule-builder.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md)<br/><br/>[重定向](retarget.md) | [活动快速入门](activities/about-activities.md)<br/><br/>活动：<br/>[并行汇聚](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [渠道活动](activities/channels.md) - [合并](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分叉](activities/fork.md) - [协调](activities/reconciliation.md) - [保存受众](activities/save-audience.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++
<br/>

>[!BEGINSHADEBOX]

</br>

此页面上的内容不是最终内容，可能会发生变化。

>[!ENDSHADEBOX]

在 [!DNL Adobe Journey Optimizer] 中创建精心策划的营销活动，并配置其执行计划以控制其启动时间和运行频率。进行选择以立即启动营销活动、在指定日期和时间启动，或使用灵活的计划选项（如按每日、每周或每月的频率）定期执行。

## 创建营销活动 {#create}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="编排式营销活动列表"
>abstract="**编排**&#x200B;标签页列出了所有编排式营销活动。单击协同营销活动的名称即可对其进行编辑。使用&#x200B;**创建协同营销活动**&#x200B;按钮，添加新的协同营销活动。"

要创建精心策划的营销活动，请执行以下步骤：

1. 浏览到&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单并选择&#x200B;**[!UICONTROL 业务流程]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 创建营销活动]**&#x200B;按钮并选择&#x200B;**[!UICONTROL 业务流程 — 营销]**&#x200B;营销活动类型。

   ![](assets/create-modal.png)

1. 定义营销活动属性。 为此，请单击促销活动名称旁边的![促销活动设置图标](assets/do-not-localize/campaign-settings.svg)按钮。

   ![](assets/inventory-create.png)

   1. 输入营销活动的&#x200B;**[!UICONTROL 名称]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

   1. 为您的营销活动选择&#x200B;**[!UICONTROL 合并策略]**。

      在[!DNL Adobe Experience Platform]中，每个受众都与特定的合并策略绑定，该策略定义如何组合配置文件信息以形成合并的配置文件。 在读取受众活动中选择合并策略时，只有基于同一合并策略的受众才可用。 默认情况下，系统使用默认合并策略，但您可以根据需要更改它。 有关合并策略的更多信息，请参阅[Adobe Experience Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/merge-policies/overview){target="_blank"}。

   1. 使用&#x200B;**[!UICONTROL 标记]**&#x200B;字段将Adobe Experience Platform统一标记分配给您的营销活动。 这样，您就可以轻松地对营销活动进行分类，并改进精心策划的营销活动列表中的搜索。[了解如何使用标记](../start/search-filter-categorize.md#tags)。

   1. 单击&#x200B;**[!UICONTROL 保存]**。

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

默认情况下，精心策划的营销活动需手动激活启动，并在所有关联活动执行完毕后自动结束。若需延迟执行或定期运行营销活动，您可为营销活动自定义执行计划。

在计划精心策划的营销活动时，请遵循以下最佳实践以确保实现最佳性能与预期效果：

* 精心策划的营销活动的执行间隔不应低于 15 分钟，否则可能影响系统整体性能并导致数据库阻塞。
* 若需在精心策划的营销活动中发送一次性消息，您可将执行频率设置为&#x200B;**一次**。
* 若需在精心策划的营销活动中发送定期消息，需使用&#x200B;**计划**&#x200B;选项并设置执行频率。定期投放活动不支持自定义计划。

要配置活动计划，请执行以下步骤：

1. 打开营销活动，然后单击&#x200B;**[!UICONTROL 尽快]**&#x200B;按钮。

   ![](assets/create-schedule.png)

1. 选择营销活动的执行频率，然后配置可用选项。设置因所选频率而异：

   +++一次

   在指定的日期和时间运行营销活动一次。

   * **[!UICONTROL 日期]**：选择应执行营销活动的日期。
   * **[!UICONTROL 时间]**：选择应执行营销活动的特定时间。

+++

   +++每日

   每天或在选定的日期运行营销活动。

   * **[!UICONTROL 每日重复]**：选择营销活动的运行频率：
      * **[!UICONTROL 每天]**：在一周的每一天（包括周末）执行营销活动。
      * **[!UICONTROL 工作日]**：仅在星期一到星期五执行营销活动。
      * **[!UICONTROL 在特定时间段内]**：在定义的日期范围内（例如，从 7 月 1 日至 7 月 15 日）每天执行营销活动。在此时间段范围之外，不会运行营销活动。
      * **[!UICONTROL 在每周的选定日期]**：仅在每周的指定日期（例如，周一、周三、周五）执行营销活动。

   * **[!UICONTROL 开始时间]**：定义每天执行营销活动的时间。

+++

   +++一天多次

   在同一天内多次运行营销活动。您可以选择特定时间或设置周期频率。

   * **[!UICONTROL 选定小时]**：选择营销活动运行的特定时间，并配置其每日重复频率（在一周的每一天或某些天执行）。
   * **[!UICONTROL 定期]**：选择每 n 分钟或每 n 小时运行营销活动一次。您还可以定义一天内允许执行的时间范围。

+++

   +++每周

   以周为频率运行营销活动，并提供特定日期选项。

   * **[!UICONTROL 频率]**：选择营销活动的运行频率（例如，每周、每两周）。
   * **[!UICONTROL 从某日开始]**：选择开始重复运行的日期。
   * **[!UICONTROL 每日重复]**：选择在一周中的特定日期执行（例如，每个星期一和星期四）。
   * **[!UICONTROL 开始时间]**：设置营销活动在选定日期的执行时间。

+++

   +++每月

   以月为频率运行营销活动，并提供特定日期选项。

   * **[!UICONTROL 每月重复]**：选择营销活动是每月运行还是仅在特定月份运行。
   * **[!UICONTROL 每日重复]**：
      * **[!UICONTROL 每天]**：在每月的每个日历日（包括周末）执行营销活动。
      * **[!UICONTROL 每月的最后一天]**：仅在每月的最后一个日历日（如 1 月 31 日、2 月 28/29 日）执行营销活动。
      * **[!UICONTROL 每月的特定日期（例如，第 15 日）]**：在指定的日期（例如，每个月的第 15 日）执行营销活动。
      * **[!UICONTROL 每周的第一天/最后一天或第 n 天]**（例如，第一个星期一）：在指定的工作日（例如，每周的第 15 日）执行营销活动。
      * **[!UICONTROL 每周的选定日期]**：在指定日期执行营销活动。

   * **[!UICONTROL 开始时间]**：设置营销活动的执行时间。

+++

1. 使用&#x200B;**[!UICONTROL 有效期]**&#x200B;设置，定义特定的开始和结束日期，将营销活动的执行限制在有限的时间范围内。

1. 对于定期计划，请单击&#x200B;**[!UICONTROL 预览启动时间]**&#x200B;按钮，根据当前配置预览即将执行的确切日期和时间。这有助于在激活之前验证计划，并确保营销活动按预期运行。

>[!NOTE]
>
>在 [!DNL Adobe Journey Optimizer] 中计划营销活动时，请确保开始日期/时间与所需的首次投放时间一致。对于定期营销活动，如果计划的首次时间已过，则营销活动将根据定期规则滚动到下一个可用时间段。

在下方的示例中，活动配置为从 2025 年 10 月 1 日至 2026 年 1 月 1 日每天运行两次，运行时间为早上 9 点和凌晨 12 点。

![调度程序配置为在早上 9 点和凌晨 12 点每天运行营销活动两次](assets/scheduler-sample.png){width="50%" align="left"}

## 后续步骤 {#next}

配置营销活动设置和计划后，您就可以开始精心策划将要执行的不同任务。[了解如何精心策划营销活动](../orchestrated/orchestrate-activities.md)
