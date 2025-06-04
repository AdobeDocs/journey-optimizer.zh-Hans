---
solution: Journey Optimizer
product: journey optimizer
title: 配置协同营销活动设置
description: 了解如何使用Adobe Journey Optimizer配置编排的活动设置
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: a9bb3782-a4d1-43fe-ae2a-aef3f17ba588
source-git-commit: 7f535b87e415ae9191199b34476adb5c977b66e9
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 26%

---

# 配置协同营销活动设置 {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="协同营销活动属性"
>abstract="在此屏幕中，选择要用于创建协同营销活动的模板并指定标签。展开&#x200B;**其他选项**&#x200B;部分以配置更多设置，例如协同营销活动内部名称、其文件夹、时区和主管组。强烈建议选择一个主管组，以便如果出错，可提醒操作员。"

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库  | 编排的营销活动活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建协调的营销活动](create-orchestrated-campaign.md)<br/><br/>[协调活动](orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](send-messages.md)<br/><br/>[开始并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用查询Modeler](orchestrated-query-modeler.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[And-join](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

在画布中创建编排的活动或编排编排的活动活动时，您可以访问与编排的活动相关的高级设置。 例如，您可以为编排的活动设置特定时区，管理编排的活动在出错时的行为方式，或管理应清除编排的活动历史记录的延迟。

这些设置是在创建编排活动时选择的模板中预先配置的，但可以根据需要对此特定编排活动进行编辑。

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## 协同营销活动属性 {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="协同营销活动属性"
>abstract="此部分提供了创建协同营销活动时也可访问的通用协同营销活动属性。您可以选择要用于创建协同营销活动的模板并指定标签。展开“其他选项”部分以配置特定设置，例如协同营销活动存储文件夹或时区。"

**[!UICONTROL 属性]**&#x200B;部分提供了通用设置，可在创建编排的活动时配置这些设置。 要访问现有编排营销活动的属性，请单击编排营销活动画布上方操作栏中可用的&#x200B;**[!UICONTROL 设置]**&#x200B;按钮。


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


这些属性包括：

* 列表中显示的编排促销活动的&#x200B;**[!UICONTROL 标签]**。
* 编排的营销活动的&#x200B;**[!UICONTROL 内部名称]**。
* 应保存编排营销活动的&#x200B;**[!UICONTROL 文件夹]**。
* 要在编排的所有营销活动中使用的默认&#x200B;**[!UICONTROL 时区]**。 默认情况下，编排的营销活动的时区就是为当前营销活动操作员定义的时区。
可能的值包括：
   * **服务器时区**&#x200B;以使用Adobe Experience Platform组织的时区
   * **操作员时区**，使用执行编排活动的操作员的时区
   * **数据库的时区**&#x200B;以使用数据库服务器的时区
   * 特定时区
* 当编排的活动失败时，属于&#x200B;**[!UICONTROL 主管]**&#x200B;字段中所选操作员组的操作员将收到电子邮件通知。
* 您还可以输入编排的营销活动的&#x200B;**[!UICONTROL 描述]**。

## 分段设置  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="分段设置"
>abstract="在此部分中，您可以选择协同营销活动中目标轮廓的定位维度，并选择保留两次执行之间的工作流结果。此选项只应用于测试目的，且不得在生产环境中的协同营销活动内启用。"

* **[!UICONTROL 定向维度]**：选择要用于定向用户档案的定向维度：收件人、合同受益人、操作员、订阅者等。

* **[!UICONTROL 保留两次执行之间的临时人口结果]**：默认情况下，仅保留编排的活动的最后一次执行的工作表。 以前执行的工作表由技术精心安排的活动清除，该活动每天运行。

  如果启用此选项，则即使在执行编排的活动之后，也会保留工作表。 您可以将其用于测试目的，因此必须&#x200B;**仅**&#x200B;用于开发或暂存环境。 在生产编排的活动中，绝不能对其进行检查。

## 执行设置  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="执行设置"
>abstract="在此部分中，您可以配置与多步骤营销活动执行相关的设置，例如协同营销活动历史记录的保留天数。"

* **[!UICONTROL 历史记录（以天为单位）]**：指定必须清除历史记录的天数。 历史记录包含与编排的活动相关的元素：日志、任务、事件（链接到编排的活动操作的技术对象）。 现成可用的编排活动模板的默认值为30天。 清除历史记录由数据库清理技术编排的活动执行，默认情况下，每天都会执行该活动

  >[!IMPORTANT]
  >
  >如果将&#x200B;**[!UICONTROL 历史记录（天）]**&#x200B;字段保留为空，其值将被视为“1”，这表示历史记录将在 1 天后清除。

* **[!UICONTROL 默认关联性]**：如果您的安装包含多个协调的活动服务器，请使用此字段指定将在其中执行协调活动的服务器。 这强制在特定服务器上执行该编排的营销活动。 您可以选择任何现有的关联名称，但请确保不使用空格或标点符号。 如果使用不同的服务器，请指定不同的名称（用逗号分隔）。

  >[!IMPORTANT]
  >
  >如果此字段中定义的值在任何服务器上不存在，则编排的营销活动将保持挂起状态。


* **[!UICONTROL 将SQL查询保存到日志]**：选中此选项可将workflmulti-step campaignow中的SQL查询保存到日志中。 此功能是为高级用户保留的。它适用于包含定向活动（如&#x200B;**[!UICONTROL 构建受众]**）的编排营销活动。 启用此选项后，在协调的活动执行期间发送到数据库的SQL查询将显示在协调的活动日志中，允许您分析这些查询以优化查询或诊断问题。

## 错误管理设置  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="错误管理设置"
>abstract="在此部分中，您可以定义协同营销活动在执行期间应如何管理错误。您可以选择暂停流程、忽略一定数量的错误或停止协同营销活动执行。"

* **[!UICONTROL 错误管理]**：此字段允许您定义在编排的营销活动任务出现错误时要执行的操作。 有三种可能的选项：

   * **[!UICONTROL 暂停进程]**：编排的活动自动暂停，其状态更改为&#x200B;**[!UICONTROL 失败]**。 问题解决后，使用&#x200B;**[!UICONTROL 恢复]**&#x200B;按钮恢复编排的营销活动。
   * **[!UICONTROL 忽略]**：触发错误的任务状态更改为&#x200B;**[!UICONTROL 失败]**，但编排的活动会保留&#x200B;**[!UICONTROL 已启动]**&#x200B;状态。<!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL 中止进程]**：编排的活动自动停止，其状态更改为&#x200B;**[!UICONTROL 失败]**。 问题解决后，使用&#x200B;**[!UICONTROL 开始]**&#x200B;按钮重新启动编排的营销活动。

* **[!UICONTROL 连续错误]**：在&#x200B;**[!UICONTROL 如果出现错误]**&#x200B;字段中选择&#x200B;**[!UICONTROL 忽略]**&#x200B;值时，此字段将变为可用。 您可以指定在流程停止前可忽略的错误的数量。一旦达到此数量，编排的营销活动状态将更改为&#x200B;**[!UICONTROL 失败]**。 如果此字段的值为0，则无论错误数量如何，编排的营销活动都不会停止。


