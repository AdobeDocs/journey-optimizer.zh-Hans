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
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '1014'
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

一旦您拥有 [创建了IP预热计划](ip-warmup-plan.md) 并上传与可投放性顾问一起准备的文件，您可以定义阶段并在计划中运行。

每个阶段对应于由多次运行组成的时段，您可以为该时段分配一个营销活动。

对于每次运行，您都拥有一定数量的收件人，并安排执行此运行的时间。

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

1. 在 **[!UICONTROL 配置文件排除]** 部分中，您可以看到始终排除该阶段先前运行的用户档案。 例如，如果在Run #1中，某个用户档案涵盖了被定位的前4800人，则系统将自动确保该用户档案不会在Run #2中收到电子邮件。

1. 从 **[!UICONTROL 排除的活动受众]** 部分，从其他部分选择受众 <!--executed/live?-->要从当前阶段排除的营销活动。

   ![](assets/ip-warmup-plan-exclude-campaigns.png)

   例如，在执行阶段1时，必须 [拆分](#split-phase) 不管怎么说。 因此，您可以排除阶段1中使用的营销活动，以便之前从阶段1联系的用户档案不包括到阶段2。 您还可以从其他IP预热计划中排除营销活动。

1. 从 **[!UICONTROL 排除的域组]** 部分中，选择要从该阶段中排除的域。

   ![](assets/ip-warmup-plan-exclude-domains.png)

   例如，运行IP预热几天后，您意识到某个域的ISP信誉(即Adobe)不佳，您希望在不停止IP预热计划的情况下解决该问题。 在这种情况下，您可以排除Adobe域组。

   >[!NOTE]
   >
   >域排除需要一个未执行的阶段，因此您可能必须拆分正在运行的阶段才能添加排除项。 同样，如果域组不是OOTB域组，则需要将此域组添加到Excel文件中，将其上传，然后排除该域。

   ![](assets/ip-warmup-plan-phase-1.png)

1. 如果需要，可以添加阶段。 它将在当前最后一个阶段后添加。

1. 使用 **[!UICONTROL 删除阶段]** 按钮以删除任何不需要的阶段。

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >无法撤消 **[!UICONTROL 删除]** 操作。
   >
   >如果从IP预热计划中删除所有阶段，我们建议重新上传计划。

## 定义运行 {#define-runs}

1. 为每次运行选择计划。 <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. 或者，选择一个窗口，万一受众分段作业执行出现任何延迟，可以在其中执行IP预热活动。 如果未指定结束时间，则会在开始时间尝试执行，如果未完成分段，则执行将失败。

1. 激活每次运行。 确保调度的时间足够早，以允许运行分段作业。 <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >每次运行必须在实际发送时间之前至少12小时激活。 否则，可能无法完成分段。 <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

   <!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. 如果活动执行尚未开始，则可以停止运行。<!--why?-->

   >[!NOTE]
   >
   >活动开始执行后， **[!UICONTROL 停止]** 按钮将变为不可用。 <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. 要添加运行，请选择 **[!UICONTROL 在下方添加运行]** 从三个圆点图标。

   ![](assets/ip-warmup-plan-run-more-actions.png)

## 拆分阶段 {#split-phase}

在任何时候，如果您希望使用从特定运行开始的不同营销活动，请选择 **[!UICONTROL 拆分为新阶段选项]** 从三个圆点图标。

为当前阶段的剩余运行创建一个新阶段。 按照以下步骤操作 [以上](#define-phases) 以定义新阶段。

例如，如果为Run #4选择此选项，则Runs #4 to #8将移动到新阶段。

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

## 将计划标记为已完成 {#mark-as-completed}

如果您的计划执行得不够好，或者您要删除它以创建另一个计划，则可以将其标记为已完成。

要执行此操作，请单击 **[!UICONTROL 更多]** IP预热计划右上角的按钮，然后选择 **[!UICONTROL 标记为已完成]**.

![](assets/ip-warmup-plan-mark-completed.png)

仅当计划中的所有运行都位于以下位置时，此选项才可用 **[!UICONTROL 已成功]** 或 **[!UICONTROL 草稿]** 状态。 无法运行 **[!UICONTROL 实时]**.

中列出了不同的运行状态 [本节](#monitor-plan).

## 监控计划 {#monitor-plan}

要衡量计划的影响，您可以使用报表检查IP预热营销活动的效果。 了解有关营销活动电子邮件的更多信息 [实时报告](../reports/campaign-live-report.md#email-live) 和 [全局报告](../reports/campaign-global-report.md##email-global).

IP预热计划本身也可用作单个位置的整合报告。 您可以检查元素，例如 **[!UICONTROL 实时]** 或 **[!UICONTROL 已成功]** 会针对每个阶段运行，并查看IP预热计划的进展情况。

运行可以具有以下状态：

* **[!UICONTROL 草稿]** ：每当创建运行时，无论是何时 [上传新计划](ip-warmup-plan.md) 或 [添加运行](#define-runs) 在用户界面中，它采用 **[!UICONTROL 草稿]** 状态。
* **[!UICONTROL 实时]**：无论何时激活运行，都会使用 **[!UICONTROL 实时]** 状态。
* **[!UICONTROL 已成功]**<!--TBC-->：此运行的营销活动执行已完成。 <!--i.e. campaign execution has started, no error happened and emails have reached users? to check with Sid-->
* **[!UICONTROL 已取消]**： a **[!UICONTROL 实时]** 已使用 **[!UICONTROL 停止]** 按钮。 仅当活动执行尚未启动时，此按钮才可用。 [了解详情](#define-runs)
* **[!UICONTROL 失败]**：系统遇到错误，或用于当前阶段的营销活动已停止<!--what should the user do in that case?-->.
