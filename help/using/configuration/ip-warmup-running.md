---
solution: Journey Optimizer
product: journey optimizer
title: 运行IP预热计划
description: 了解如何运行和监控IP预热计划
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、池、组、子域、可投放性
hide: true
hidefromtoc: true
source-git-commit: dc1eeb3c199e7db2fc152b682404a547e2ae56c7
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 1%

---

# 运行IP预热计划 {#ip-warmup-running}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [IP预热入门](ip-warmup-gs.md)
* [创建IP预热活动](ip-warmup-campaign.md)
* [创建IP预热计划](ip-warmup-plan.md)
* **[运行IP预热计划](ip-warmup-running.md)**

>[!ENDSHADEBOX]

## 定义阶段 {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="选择要排除的营销活动受众"
>abstract="从要从当前阶段排除的其他营销活动中选择受众。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="选择要排除的域组"
>abstract="选择要从当前阶段排除的域。"

您需要将活动与阶段级别的受众关联，并根据需要为与单个创意/活动关联的所有运行打开某些设置

在阶段级别，系统会确保提取之前定向的+新用户档案；在迭代级别，系统会确保每次运行都具有唯一的用户档案，并且计数与计划中所列的计数相匹配

1. 对于每个阶段，选择要与IP预热计划的此阶段关联的活动。

   ![](assets/ip-warmup-plan-select-campaign.png)

   请注意以下事项：

   * 仅限具有的促销活动 **[!UICONTROL IP预热计划激活]** 选项已启用 <!--and live?--> 可供选择。 [了解详情](#create-ip-warmup-campaign)

   * 您必须选择与为当前IP预热计划选择的活动使用相同曲面的活动。

   * 您不能选择已在其他IP预热营销活动中使用的营销活动。

1. 对于每个阶段，将应用以下内容：

   * **[!UICONTROL 配置文件排除]**  — 始终排除该阶段上一次运行的用户档案。 例如，如果在运行#1，Leo在前6300位目标用户中被覆盖，系统将自动确保Leo在运行#2不会收到邮件。

   * **[!UICONTROL 排除的活动受众]**  — 从其他受众中选择受众 <!--executed/live?-->要从当前阶段排除的营销活动。

     例如，您可能正在执行一个阶段，并且由于任何原因必须拆分该阶段。 在这种情况下，在阶段2中，您要将阶段1中使用的营销活动包含在此部分中，以便在阶段2中，不包括先前来自阶段1的联系人员。 这不仅可以应用于同一IP预热计划中的营销活动，还可以应用于其他IP预热计划。

   * **[!UICONTROL 排除的域组]**  — 选择要从该阶段中排除的域，例如Gmail。 <!--??-->

     运行IP预热几天后，您意识到某个域的ISP信誉表明hotmail不好，您希望通过ISP解决该问题，但不希望停止IP预热计划。 在这种情况下，您可以将域组hotmail置于排除的类别中。

     >[!NOTE]
     >
     >域排除需要一个未执行的阶段，因此您可能必须拆分正在运行的阶段才能添加排除项。 同样，如果域组不是OOTB域组，则可能必须在Excel中创建域组，然后上载并排除该域组。

   ![](assets/ip-warmup-plan-phase-1.png)

1. 如果需要，可以添加阶段 — 该阶段将在当前最后一个阶段之后添加。 使用 **[!UICONTROL 删除阶段]** 按钮以删除任何不需要的阶段。

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >无法撤消 **[!UICONTROL 删除]** 操作。
   >
   >如果从IP预热计划中删除所有阶段，我们建议重新上传计划。

## 定义运行 {#define-runs}

1. 为每次运行选择计划。 <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. 选择结束时间，这基本上意味着我们可以在该窗口内执行预热活动，以防受众作业出现任何延迟。 如果未指定，我们将在启动时尝试但失败。 如果提供了结束时间，我们将在该窗口之间执行运行。

1. 激活每次运行。 确保调度的时间足够早，以允许运行分段作业。 <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >每次运行必须在实际发送时间之前至少12小时激活。 否则，可能无法完成分段。 <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. 如果活动执行尚未开始，则可以停止运行。<!--why?-->

   活动开始执行后， **[!UICONTROL 停止]** 按钮将变为不可用。 <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. 要添加运行，请选择 **[!UICONTROL 在下方添加运行]** 从三个圆点图标。

   ![](assets/ip-warmup-plan-run-more-actions.png)

1. 在任何时候，如果您希望使用从特定运行开始的不同营销活动，请选择 **[!UICONTROL 拆分为新阶段选项]** 从三个圆点图标。 为当前阶段的剩余运行创建一个新阶段。 按照以下步骤操作 [以上](#define-phases) 以定义新阶段。

   例如，如果为运行#4选择此选项，则#4运行#8将移至新阶段。

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

## 监控计划

运行可以具有以下状态<!--TBC with Medha-->：

* **[!UICONTROL 已完成]**:
* **[!UICONTROL 失败]**:
* **[!UICONTROL 已取消]**：在开始执行营销活动之前，您已停止运行。

优点 :

* 营销活动级别将继续显示具有与今天类似功能的报表。 但IP预热计划还可用作执行多少等内容的单个位置的综合报告。

* 可在单个位置管理和查看IP热量的进展情况。

* 在创意/营销活动级别整合报表，因为某个阶段的所有报表都在运行