---
solution: Journey Optimizer
product: journey optimizer
title: 运行 IP 预热计划
description: 了解如何运行和监控IP预热计划
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP、组、子域、可投放性
exl-id: 752ffd7f-09c2-4aa3-a067-2dbe0634709c
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '2530'
ht-degree: 11%

---

# 执行 IP 预热计划 {#ip-warmup-running}

在您[创建IP预热计划](ip-warmup-plan.md)并上传与可投放性顾问准备的文件后，您可以定义计划中的阶段并运行。

每个阶段都由若干您为其分配单个营销活动的运行组成。

## 定义阶段 {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="排除营销活动受众"
>abstract="选择营销活动以从当前阶段排除其受众。这可以防止之前联系过的个人资料再次成为目标；只有那些通过历程收到过通信的人才会被排除。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="排除域组"
>abstract="选择要从当前阶段排除的域。域排除需要非执行阶段，因此，您可能必须拆分正在运行的阶段才能添加排除。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-execution.html#split-phase" text="拆分阶段"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_phases"
>title="定义计划的阶段"
>abstract="每个阶段都由若干您为其分配单个营销活动的运行组成。"

<!--You need to associate the campaign and audience at phase level and turns on some settings as needed for all runs associated with a single creative/campaign

At phase level, system ensures that previously targeted + new profiles are picked up AND at iteration level, system ensures that each run is having unique profiles and the count matches what is stated in plan-->

<!--![](assets/ip-warmup-plan-phase-1.png)-->

1. 选择要与IP预热计划第一阶段关联的营销活动。

   >[!NOTE]
   >
   >您不能选择已在另一个IP预热计划中使用的营销活动。 但是，同一IP预热计划的一个或多个阶段中可以使用相同的活动。

   ![](assets/ip-warmup-plan-select-campaign.png)

   >[!IMPORTANT]
   >
   >* 只有启用了&#x200B;**[!UICONTROL IP预热计划激活]**&#x200B;选项的营销活动才可供选择。 [了解详情](#create-ip-warmup-campaign)
   >
   >* 只有使用与所选IP预热计划相同配置的营销活动才可供选择。

1. 为当前阶段选择营销策划后，将显示排除用户档案、营销策划受众和域组的部分。

   >[!NOTE]
   >
   >一旦激活运行，除非您[将运行](#split-phase)拆分为新阶段，否则无法再修改排除项。

   1. 从&#x200B;**[!UICONTROL 排除的域组]**&#x200B;部分，选择要从该阶段排除的域。

      >[!NOTE]
      >
      >域排除需要一个未执行的阶段，因此您可能需要[拆分正在运行的阶段](#split-phase)以添加排除项。

      ![](assets/ip-warmup-plan-exclude-domains.png)

      例如，运行IP预热几天后，您意识到您在域(例如Adobe)的ISP信誉不佳，您希望在不停止IP预热计划的情况下解决该问题。 在这种情况下，您可以排除Adobe域组。

      >[!NOTE]
      >
      >您只能排除已添加到[IP预热计划模板](ip-warmup-plan.md#prepare-file)的自定义域组。 如果不是这种情况，请使用要排除的自定义域组更新模板，然后[重新上载计划](#re-upload-plan)。

   1. 从用于排除用户档案的&#x200B;**[!UICONTROL 营销活动]**&#x200B;部分中，选择要从当前阶段中排除的受众的营销活动。

      ![](assets/ip-warmup-plan-exclude-campaigns.png)

      例如，在执行阶段1时，出于任何原因，您必须[拆分它](#split-phase)。 因此，您可以排除阶段1中使用的营销活动，以便之前在第1阶段联系的用户档案不包括在第2阶段中。 您还可以从其他IP预热计划中排除营销活动。

   1. 从排除用户档案的&#x200B;**[!UICONTROL 历程]**&#x200B;部分中，选择包含要从当前阶段中排除的受众的历程。

+++ 要使用用于排除用户档案选项的历程，您需要在AJO消息反馈事件和AJO实体记录架构之间建立关系。

      1. 创建将用作以下步骤的标识类型的自定义&#x200B;**命名空间**。

      1. 访问Adobe Experience Platform，从&#x200B;**架构**&#x200B;菜单中，选择&#x200B;**AJO实体记录架构**，并将&#x200B;**_id**&#x200B;字段设置为主标识，然后选择之前创建的命名空间作为&#x200B;**标识命名空间**。

      1. 从&#x200B;**架构**&#x200B;菜单中，选择&#x200B;**AJO消息反馈事件架构**，并导航到&#x200B;**_messageID**&#x200B;字段。 选择&#x200B;**添加关系**，然后选择&#x200B;**AJO实体记录架构**&#x200B;作为&#x200B;**引用架构**，选择您之前创建的命名空间作为&#x200B;**引用身份命名空间**。
+++

   1. 在&#x200B;**[!UICONTROL 以前运行中定向的用户档案]**&#x200B;部分中，您可以看到始终排除该阶段以前运行中的用户档案。 例如，如果在Run #1中，某个用户档案涵盖了被定位的前4800人，则系统将自动确保该用户档案不会在Run #2中收到电子邮件。

      >[!NOTE]
      >
      >此分区不可编辑。

1. 如果需要，您可以使用&#x200B;**[!UICONTROL 替换]**&#x200B;按钮替换营销活动。 您还可以使用&#x200B;**[!UICONTROL 清除]**&#x200B;按钮&#x200B;**[!UICONTROL 清除]**&#x200B;选定的营销活动。 此操作不仅会清除营销活动，还会清除其他阶段级别属性，例如域组排除、营销活动、历程排除等。 清除后，您可以立即或稍后选择新的营销策划。

   ![](assets/ip-warmup-plan-replace-campaign.png)

   >[!NOTE]
   >
   >只有在激活该阶段的第一次运行之前，才能执行此操作。 一旦激活某个运行，便无法替换该活动，除非您[将该运行](#split-phase)拆分为新阶段。

1. 如果需要，可以添加阶段。 它将在最后一个阶段后添加。

   ![](assets/ip-warmup-plan-add-phase.png)

1. 使用&#x200B;**[!UICONTROL 删除阶段]**&#x200B;按钮删除任何不需要的阶段。 仅当某个阶段未执行任何运行时，此操作才可用。<!--Once a run is executed, deletion is not allowed.-->

   >[!CAUTION]
   >
   >无法撤消&#x200B;**[!UICONTROL 删除阶段]**&#x200B;操作。

   ![](assets/ip-warmup-plan-delete-phase.png)

   >[!NOTE]
   >
   >如果从IP预热计划中删除所有阶段，建议重新上传计划。 [了解详情](#re-upload-plan)

## 定义运行 {#define-runs}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_run"
>title="定义每次运行"
>abstract="为所有阶段定义并激活每次运行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_last_engagement"
>title="按参与过滤"
>abstract="此列是一个过滤器，它仅针对例如在过去 20 天内与您的品牌有过互动的用户。您还可以通过&#x200B;**编辑运行**&#x200B;选项更改此设置。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_retry"
>title="设置时间范围"
>abstract="您可以定义一个时间范围，在此期间，如果分段作业有任何延迟，则可以执行 IP 预热营销活动。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_pause"
>title="因受众错误取消运行"
>abstract="在为某次运行评估受众后，如果合格的轮廓比作为目标的轮廓少，则选择此选项可取消此次运行。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_qualified"
>title="查看合格的轮廓"
>abstract="此列显示合格的轮廓数。为某次运行评估受众后，如果作为目标的轮廓比合格的轮廓多，则除非启用了&#x200B;**因错误取消已激活的运行**&#x200B;选项，否则仍执行该运行。如果启用了该选项，则取消该运行。"

1. 为每次运行选择一个计划，以确保在指定的时间执行它。

   ![](assets/ip-warmup-plan-send-time.png)

1. 或者，您可以定义一个时间范围，以在[受众评估](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"}出现任何延迟时执行IP预热活动。 为此，请单击左上角计划名称旁边的“属性”图标，然后使用&#x200B;**[!UICONTROL 重试运行时间]**&#x200B;下拉列表选择持续时间 — 最多240分钟（4小时）。

   >[!NOTE]
   >
   >在定义的时间窗口结束前，每30分钟进行一次重试。

   ![](assets/ip-warmup-plan-retry-run-time.png)

   例如，如果在指定日期的早上9点设置发送时间，并选择120分钟作为重试运行时间，则对于受众评估中的任何意外延迟，允许运行的时间窗口为2小时（上午9点到上午11点）。

   >[!NOTE]
   >
   >如果未指定时间窗口，则在发送时尝试运行，如果未完成受众评估，则运行将失败。

1. 如果需要，请从“更多操作”图标中选择&#x200B;**[!UICONTROL 编辑运行]**。 您可以在此更新每列的地址数。 例如，您还可以更新&#x200B;**[!UICONTROL 上次参与]**&#x200B;字段以仅定向过去20天内与您的品牌互动的用户。

   >[!NOTE]
   >
   >建议咨询您的可投放性专家，修改这些数字。

   ![](assets/ip-warmup-plan-edit-run.png)

   >[!NOTE]
   >
   >如果不希望将任何参与期应用于运行，请在&#x200B;**[!UICONTROL 上次参与]**&#x200B;字段中输入0。

1. 选择&#x200B;**[!UICONTROL 发生错误时取消激活的运行]**&#x200B;选项，以便在评估受众运行后，如果合格的配置文件少于目标配置文件，则取消该运行。 在这种情况下，该运行采用&#x200B;**[!UICONTROL 失败]**&#x200B;状态。

   ![](assets/ip-warmup-plan-pause.png)

1. **[!UICONTROL 激活]**&#x200B;运行。 [了解详情](#activate-run)

1. 此运行的状态将更改为&#x200B;**[!UICONTROL Live]**，这意味着系统已接受计划运行的请求。

   >[!NOTE]
   >
   >[此部分](#monitor-plan)中列出了不同的运行状态。

1. 如果活动执行尚未开始，您可以取消实时运行。 此操作实际上会取消运行计划 — 它不会停止发送。

   ![](assets/ip-warmup-plan-stop-run.png)

1. 要复制任何草稿、实时或已完成的运行，请选择&#x200B;**[!UICONTROL 复制运行]**。 复制后，将显示“编辑运行”菜单，使用户能够根据需要调整&#x200B;**[!UICONTROL 目标配置文件总数]**&#x200B;和&#x200B;**[!UICONTROL 发送时间]**。

   ![](assets/ip-warmup-duplicate.png)

## 激活运行 {#activate-run}

要激活运行，请选择&#x200B;**[!UICONTROL 激活]**&#x200B;按钮。 然后，您可以每天激活下一个运行。

当同时运行多个IP预热计划（均针对相同的IP池和域）时，预测潜在的后果至关重要。 例如，如果ISP强制实施每天100封电子邮件的限制，则针对同一域运行多个计划可能会超过此阈值。

请确保您计划了足够的时间以允许执行[受众评估](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#how-segmentation-works){target="_blank"}。

![](assets/ip-warmup-plan-activate.png)

>[!CAUTION]
>
>每次运行必须在实际发送时间之前至少12小时激活。 否则，可能无法完成受众评估。

在激活运行时，会自动创建多个受众。

* 如果激活阶段的第一次运行：

   * 为排除的营销活动受众（如果有）创建[受众](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html){target="_blank"}，其命名约定如下： `<warmupName>-Phase<phaseNo>-Audience Exclusion `。

   * 使用以下命名约定为排除的域组（如果有）创建受众： `<warmupName>-Phase<phaseNo>-Domain Exclusion`。

   * 为排除的历程受众（如果有）创建另一个受众，其命名约定如下： `<warmupName>-Phase<phaseNo>-Journey Audience Exclusion`。

  >[!NOTE]
  >
  >将预热计划标记为完成之后，将清理受众。
  >
  >如果排除的营销活动受众、排除的历程受众或后续阶段的域组没有变化，则系统不会创建新受众。

* 激活任何运行时：

   * 为最后一个参与过滤器创建另一个受众，其命名约定如下： `<warmupName>-Phase<phaseNo>_Run<runNo>-Engagement Filter`。

     >[!NOTE]
     >
     >将预热计划标记为完成之后，会清理受众。
     >
     >如果后续阶段的最后一个参与过滤器没有变化，则系统不会创建新受众。

   * 已创建[受众组合](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=zh-Hans){target="_blank"}，该组合对应于将向其发送营销活动的受众，其命名约定如下： `<warmupName>-Phase<phaseNo>-Run<runNo>`。

     >[!NOTE]
     >
     >每次运行都会创建一个新的受众组合。 如果限制为10个，则同时使用已发布的受众组合运行多个营销活动、历程和IP预热计划的用户必须提前计划，以保持在此限制范围内进行并行操作。
     >
     >在激活下一个迭代时，将清除受众合成（以及因此产生的输出受众）。

   * 使用以下命名约定创建输出受众： `IP Warmup Audience-<warmupName>-Phase<phaseNo>-Run<runNo>`。

<!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

<!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

<!--Upon activation, when the segment evaluation happens, more segments will be created by the IP warmup service and will be leveraged in an audience composition and a new audience will be created for each run splitted into the different selected domains.-->

## 监控计划 {#monitor-plan}

要成功执行IP预热计划，您需要每天监视报告、激活运行并检查其状态。

### 使用“高亮”部分 {#highlights}

为阶段激活第一次运行后，将显示&#x200B;**[!UICONTROL 高亮]**&#x200B;部分。

它提供了当前运行和即将运行的快速概述。 在此部分中，您还可以编辑和激活下次运行。

![](assets/ip-warmup-plan-highlights.png)

### 检查运行状态 {#run-statuses}

IP预热计划本身就是单个位置的整合报告。 您可以检查每个阶段运行的&#x200B;**[!UICONTROL Live]**&#x200B;或&#x200B;**[!UICONTROL Completed]**&#x200B;等元素，并查看IP预热计划的进展情况。

>[!NOTE]
>
>作为最佳实践，建议每天监控IP预热计划。

运行可以具有以下状态：

* **[!UICONTROL 草稿]** ：每当创建运行时，在[创建新计划](ip-warmup-plan.md)或从用户界面[添加运行](#define-runs)时，它都会采用&#x200B;**[!UICONTROL 草稿]**&#x200B;状态。
* **[!UICONTROL 实时]**：无论何时激活运行，它都会处于&#x200B;**[!UICONTROL 实时]**&#x200B;状态。 这意味着系统已接受计划运行的请求，而不是发送已开始。 在此阶段，您可以通过单击表中的&#x200B;**[!UICONTROL 查看状态]**&#x200B;按钮来观察实时运行的状态。 这样，您就可以跟踪实际符合条件的定向用户档案的数量。
* **[!UICONTROL 已完成]**：此运行的营销活动执行已完成。 您可以通过单击表中的&#x200B;**[!UICONTROL 查看报告]**&#x200B;按钮来访问详细的运行报告。 使用此选项，您可以跟踪运行的电子邮件投放状态，包括特定于域组的划分，以便增强监控。 请注意，与其关联的Campaign将设置为“已停止”。[了解详情](#reports)
* **[!UICONTROL 已取消]**：已使用&#x200B;**[!UICONTROL 取消]**&#x200B;按钮取消了&#x200B;**[!UICONTROL 实时]**&#x200B;运行。[了解详情](#define-runs)
* **[!UICONTROL 失败]**：系统遇到错误，或用于当前阶段的营销活动已停止，或者您已启用&#x200B;**[!UICONTROL 如果出现错误，请取消激活的运行]**&#x200B;选项，但出现错误。 如果某个运行失败，您可以计划第二天再次运行。

### 使用报表 {#reports}

一般来说，要衡量计划的影响，您可以使用[!DNL Journey Optimizer]活动报告来检查IP预热活动的效果。 为此，对于每个已完成的运行，您可以单击&#x200B;**[!UICONTROL 查看报表]**&#x200B;按钮。 了解有关营销活动电子邮件[实时报告](../reports/campaign-live-report.md#email-live)和[全局报告](../reports/campaign-global-report.md#email-global)的更多信息。

![](assets/ip-warmup-plan-reports.png)

您还可以从[促销活动菜单](../campaigns/modify-stop-campaign.md#access)访问报告，因为您的计划可能使用不同的促销活动。


## 管理您的计划 {#manage-plan}

在任何时候，如果IP预热计划未按预期执行，您可以执行以下操作。

### 拆分阶段 {#split-phase}

如果要添加从特定运行开始的新阶段，请从“更多操作”图标中选择&#x200B;**[!UICONTROL 拆分运行到新阶段]**&#x200B;选项。

![](assets/ip-warmup-plan-run-split-run.png)

为当前阶段的剩余运行创建一个新阶段。

例如，如果为Run #4选择此选项，则Runs #4 to #8将移动到当前阶段之后的新阶段。

按照以上[步骤](#define-phases)定义新阶段。

* 您可以为该新阶段使用&#x200B;**[!UICONTROL 替换]**&#x200B;或&#x200B;**[!UICONTROL 清除]**&#x200B;选项。

* 您还可以排除上一个营销活动或表现不佳的域。 在[本节](#define-phases)中了解详情。

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

### 重新上传IP预热计划 {#re-upload-plan}

如果您的IP预热计划未按预期执行（例如，如果您发现某些ISP将您的邮件标记为垃圾邮件），则可以要求可投放性专家设置另一个IP预热计划文件，并使用相应的按钮重新上传它。

![](assets/ip-warmup-re-upload-plan.png)

以前执行的所有运行都将为只读。 新计划显示在第一个计划下。

按照以上[步骤](#define-phases)从新计划定义阶段。

>[!NOTE]
>
>IP预热计划的详细信息将根据新上传的文件而更改。 先前执行的运行（无论其[状态](#monitor-plan)如何）不受影响。

让我们举一个例子：

* 在最初的IP预热计划中，阶段2运行了9次。

* 已执行4个运行（无论失败、完成还是已取消<!--as long as a run has been attempted, it is an executed run-->）。

* 如果重新上传新计划，则运行前4次的阶段2将进入只读模式。

* 其余5次运行（处于草稿状态）将移至新阶段（第3阶段），该阶段会根据新上传的计划显示。

### 将计划标记为已完成 {#mark-as-completed}

如果您的IP已使用所需的卷进行热处理，或者您的计划执行得不够好，或者您想删除它以创建另一个卷，您可以将其标记为已完成。

为此，请单击IP预热计划右上角的&#x200B;**[!UICONTROL 更多]**&#x200B;按钮，然后选择&#x200B;**[!UICONTROL 标记为已完成]**。

![](assets/ip-warmup-plan-mark-completed.png)

仅当计划中的所有运行处于&#x200B;**[!UICONTROL 已完成]**&#x200B;或&#x200B;**[!UICONTROL 草稿]**&#x200B;状态时，此选项才可用。 如果运行是&#x200B;**[!UICONTROL Live]**，则该选项将显示为灰色。

[此部分](#monitor-plan)中列出了不同的运行状态。

