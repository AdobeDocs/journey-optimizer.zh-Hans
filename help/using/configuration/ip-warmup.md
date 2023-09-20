---
solution: Journey Optimizer
product: journey optimizer
title: 实施IP预热计划
description: 了解如何实施IP预热计划
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、池、组、子域、可投放性
hide: true
hidefromtoc: true
source-git-commit: 1ac68f1b3a9657ce71a653011ab92fb817ca80b0
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 2%

---

# 实施IP预热计划 {#ip-warmup}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!AVAILABILITY]
>
>IP预热功能目前仅作为测试版提供给部分用户。 要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

替换为 [!DNL Journey Optimizer]，您可以按照最佳可投放性实践以标准化且高效的方式直接从用户界面执行IP预热工作流。

>[!CAUTION]
>
>此功能仅适用于电子邮件渠道。

使用新平台发送电子邮件时，Internet服务提供商(ISP)会怀疑无法识别的IP地址。 如果突然发送大量电子邮件，ISP通常会将其标记为垃圾邮件。

要避免被标记为垃圾邮件，您可以使用IP预热计划功能逐步增加发送量。 通过管理菜单中的新选项，可更顺利地执行操作，而不是创建复杂的历程。 这应该可以确保启动阶段的顺利发展，并帮助您降低地址无效的总比率。

>[!NOTE]
>
>在中了解更多有关利用IP预热提高您的电子邮件声誉的信息 [可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html).

<!--
Here are the main steps:

1. You get a deliverability plan from the deliverability consulting team.

1. Create a campaign - marketer [Learn more](#create-ip-warmup-campaign)

1. Your associated practitioner (customer's practitioner/ACS consultant/partner consultant) creates a IP warmup object in project and uploads a plan.

    The CSV manifests itself like below with numbers showing up with/without domain bifurcation. Below screen shows one phase (creative) with associated runs (The plan obviously has more such phases)

1. Practitioner associates the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

1. Then start to execute on every day basis by simply clicking the play button

1. Reports will continue to show up at campaign level with similar capabilities as today. NO enhancements in BETA. But the IP warmup plan also serves as a consolidated report at one single place of how many executions were done and so on

Benefits are as follows:

* No more creation of daily journeys and associated testing

* Standardization on Campaign which will be easy for practitioners too

* No more pain of creating queries, audiences and testing those as system will create the audiences. At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* Single place to manage and view how IP warm is progressing.

* Consolidated report at creative/campaign level as all runs for a phase 

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

实施IP预热计划的关键步骤如下：

* [创建IP预热活动](#create-ip-warmup-campaign)
* [定义IP预热计划](#define-ip-warmup-plan)

## 创建IP预热活动 {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="激活IP预热计划选项"
>abstract="选择IP预热计划激活选项。 活动开始后，可以将其与IP预热计划关联。"

您需要创建一个或多个启用了特定选项的营销活动，以便在IP预热计划中使用它们。 请按照以下步骤操作。

1. 创建 [曲面](channel-surfaces.md) 用于您已为预热计划标识的域和IP。

1. 创建 [营销活动](../campaigns/create-campaign.md) 并选择 [电子邮件](../email/create-email.md#create-email-journey-campaign) 操作。

1. 选择为IP预热创建的曲面。

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 从 **[!UICONTROL 计划]** 部分，选择 **[!UICONTROL IP预热计划激活]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   营销活动 [计划](../campaigns/create-campaign.md#schedule) 将由与之关联的IP预热计划驱动，这意味着该计划不再在营销策划本身中定义。

1. [激活](../campaigns/review-activate-campaign.md) 营销活动。 一旦启用，它就可以在IP预热计划中使用。

>[!NOTE]
>
>对于激活了IP预热计划的实时营销活动， **[!UICONTROL 删除]** 按钮在与IP预热计划关联之前可用。

有关如何配置营销活动的更多信息，请参阅 [此页面](../campaigns/get-started-with-campaigns.md).

## 定义IP预热计划 {#define-ip-warmup-plan}

### 管理IP预热计划 {#manage-ip-warmup-plans}

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL IP预热计划]** 菜单。 此时将显示迄今为止创建的所有IP预热计划。

   ![](assets/ip-warmup-filter-list.png)

1. 您可以对状态进行过滤。 不同的状态包括：

   * **未开始**：未发生运行
   * **进行中**：只要运行开始 <!--or is done?-->
   * **已暂停**
   * **已完成**：计划中的所有运行都已完成

1. 要删除IP预热计划，请选择 **[!UICONTROL 删除]** 图标并确认删除。

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >选定的IP预热计划将被永久删除。

### 创建IP预热计划 {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="指定IP预热计划"
>abstract="下载CSV模板，并使用IP预热阶段的数据和目标配置文件数填充该模板。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="选择营销表面"
>abstract="必须选择与要在营销策划中与IP预热计划关联的所选表面相同的表面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="设置渠道表面"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="创建IP预热活动"

>[!CAUTION]
>
>要创建、编辑和删除IP预热计划，您必须具有 **[!UICONTROL 可投放性顾问]** 许可。
<!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

当一个或多个实时营销活动具有 **[!UICONTROL IP预热计划激活]** 启用选项后，您可以将其与IP预热计划关联。

>[!CAUTION]
>
>与您的可投放性顾问合作，确保您的IP预热计划模板设置正确。 <!--TBC-->

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL IP预热计划]** 菜单，然后单击 **[!UICONTROL 创建IP预热计划]**.

   ![](assets/ip-warmup-create-plan.png)

1. 填写IP预热计划详细信息：提供名称和描述。

   ![](assets/ip-warmup-plan-details.png)

1. 选择 [曲面](channel-surfaces.md). 仅营销表面可供选择。 [了解有关电子邮件类型的更多信息](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >必须选择与要在营销策划中与IP预热计划关联的所选表面相同的表面。 [了解如何创建IP预热活动](#create-ip-warmup-campaign)

1. 上载包含IP预热计划的Excel文件<!--which formats are allowed?-->. 您可以使用可交付性团队提供的模板。<!--TBC?--> [了解详情](#upload-plan)
   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。上传的文件中定义的阶段数将自动显示，每个阶段的所有运行都将自动显示。 [了解详情](#upload-plan)

   ![](assets/ip-warmup-plan-phases.png)

### 重新上传IP预热计划 {#re-upload-plan}

您可以使用相应的按钮重新上传另一个IP预热计划。

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>IP预热计划的详细信息将根据新上传的文件而更改。 完整运行和激活的运行不受影响。

### 上载包含计划的文件 {#upload-plan}

以下是包含IP预热计划的文件示例。

![](assets/ip-warmup-sample-file.png)

每个阶段对应于由多次运行组成的时段，您将为该时段分配一个营销活动。

对于每次运行，您都拥有一定数量的收件人，您将定义执行此运行的日期。

对于要交付到的域，您可以拥有任意数量的列。 在本例中，您有三个列：Gmail、Adobe和“其他”，这意味着

其思想是在第一阶段运行更多地址，并逐步增加目标地址的数量，同时减少运行次数。

### 定义阶段 {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="选择要排除的营销活动受众"
>abstract="从要从当前阶段排除的其他营销活动中选择受众。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="选择要排除的域组"
>abstract="选择要从当前阶段排除的域。"

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

### 定义运行 {#define-runs}

1. 为每次运行选择计划。 <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. 选择结束时间，这基本上意味着我们可以在该窗口内执行预热活动，以防受众作业出现任何延迟。 如果未指定，我们将在启动时尝试但失败。 如果提供了结束时间，我们将在该窗口之间执行运行。

1. 激活每次运行。 确保调度的时间足够早，以允许运行分段作业。 <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >每次运行必须在实际发送时间之前至少12小时激活。 否则，可能无法完成分段。 <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

1. 如果活动执行尚未开始，则可以停止运行。

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

运行可以具有以下状态<!--TBC with Medha-->：

* **[!UICONTROL 已完成]**:
* **[!UICONTROL 失败]**:
* **[!UICONTROL 已取消]**：在开始执行营销活动之前，您已停止运行。

