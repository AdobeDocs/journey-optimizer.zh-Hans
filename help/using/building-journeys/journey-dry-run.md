---
solution: Journey Optimizer
product: journey optimizer
title: 历程试运行
description: 了解如何在练习模式下发布历程
feature: Journeys
role: User
level: Intermediate
keywords: 发布，历程，实时，有效性，检查
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/a7qFw84obtkCRDmiqMxQNgvqhI4b6t5suROeF7ZPh1I
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 1413
ht-degree: 13%

---

# 历程试运行 {#journey-dry-run}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何在练习模式下发布历程，以使用实际生产数据测试该历程，而无需联系实际客户或更新配置文件，以便您可以在设计上线前验证设计。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="试运行模式"
>abstract="当前历程处于试运行状态。 历程试运行是 [!DNL Adobe Journey Optimizer] 中的一种特殊历程发布模式，使历程设计人员能够在不接触真实客户或更新轮廓信息的前提下，使用真实生产数据对历程进行测试。  此功能有助于历程设计人员在正式发布前验证历程设计和受众定位，从而增强信心。"


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="以试运行模式发布历程"
>abstract="试运行是 [!DNL Adobe Journey Optimizer] 提供的一种特殊历程发布模式，允许历程设计人员使用真实的生产数据测试历程。 历程设计完成后，可通过试运行验证其功能是否正常，并确保各步骤配置正确。 通过此发布模式，您可以对历程进行冒烟测试，而无需向任何轮廓发送通信。"

历程试运行是 [!DNL Adobe Journey Optimizer] 中的一种特殊历程发布模式，使历程设计人员能够在不接触真实客户或更新轮廓信息的前提下，使用真实生产数据对历程进行测试。  此功能有助于历程设计人员在正式发布前验证历程设计和受众定位，从而增强信心。

➡️ [在此视频中了解历程试运行](#dry-run-video)

## 主要优点 {#journey-dry-run-benefits}

历程练习通过使用真实的生产数据对客户旅程进行安全、数据驱动的测试，而无需联系客户或更改用户档案信息，从而增强了从业者的信心并促进了旅程的成功。 此功能使历程从业者能够在上线之前验证受众覆盖范围和分支逻辑，确保历程与其预期业务目标一致。

借助历程练习，您可以提前发现问题、优化定位策略以及根据实际数据（而非假设）改进旅程设计。 练习直接集成到历程画布中，可提供直观的报告和对关键绩效指标的可见性，使团队能够自信地迭代并简化审批工作流。 这提高了运营效率，降低了发布风险，并实现了更好的客户参与结果。

最终，此功能可缩短实现价值的时间并减少历程失败。

历程练习带来了：

1. **安全测试环境**：未联系处于练习模式的用户档案，确保没有发送通信或影响实时数据的风险。
1. **受众见解**：历程从业者可以预测受众在不同旅程节点上的可达性，包括基于历程条件的选择退出和排除。
1. **实时反馈**：量度直接显示在历程画布中，类似于实时报告，使历程参与者能够优化其历程设计。

## 练习执行逻辑 {#journey-dry-run-exec}

在练习期间，旅程以模拟模式运行，将以下特定行为应用于每个旅程活动而不触发实际操作：

* 不执行&#x200B;**渠道操作**&#x200B;节点，包括电子邮件、短信或推送通知。
* **自定义操作**&#x200B;在试运行期间被禁用，并且其响应设置为null。

  为了提高可读性，在执行练习期间，自定义操作和渠道活动显示为灰色。

  ![练习历程中的操作活动灰显](assets/dry-run-greyed-activities.png){width="80%"}

* 默认情况下，**数据源**（包括外部数据源）和&#x200B;**等待**&#x200B;活动在试运行期间处于禁用状态。 但是，在激活练习模式[&#128279;](#journey-dry-run-start)时，您可以更改此行为。

* 未执行&#x200B;**反应**&#x200B;节点：进入它的所有配置文件都将成功退出。 但是，以下优先级规则适用：

   * 如果&#x200B;**反应**&#x200B;节点与一个或多个并行的&#x200B;**单一事件**&#x200B;节点一起使用，则配置文件将始终通过反应事件。
   * 如果&#x200B;**反应**&#x200B;节点与一个或多个并行的&#x200B;**反应事件**&#x200B;节点一起使用，则配置文件将始终通过画布中的第一个节点（顶部的节点）。

>[!CAUTION]
>
>* 启动模拟运行的权限仅限于具有&#x200B;**[!DNL Publish journeys]**&#x200B;高级权限的用户。 停止模拟运行的权限仅限于具有&#x200B;**[!DNL Manage journeys]**&#x200B;高级权限的用户。 在[本节](../administration/permissions-overview.md)中了解有关管理[!DNL Journey Optimizer]用户访问权限的更多信息。
>
>* 在开始使用练习功能之前，[请阅读护栏和限制](#journey-dry-run-limitations)。

## 开始试运行 {#journey-dry-run-start}

您可以在任何草稿历程中使用模拟运行功能，而不会出错。

要激活试运行，请执行以下步骤：

1. 打开要测试的历程。
1. 选择&#x200B;**[!UICONTROL 练习]**&#x200B;按钮。

   ![开始历程试运行](assets/dry-run-button.png)

1. 如果要启用或禁用&#x200B;**等待**&#x200B;活动和&#x200B;**外部数据源**&#x200B;调用，请选择，并确认练习发布。

   ![确认历程试运行发布](assets/dry-run-publish.png){width="50%"}

   转换过程中出现状态消息&#x200B;**[!UICONTROL 正在激活练习]**。

1. 一旦激活，历程将进入&#x200B;**[!UICONTROL 练习]**&#x200B;模式。


## 监控练习 {#journey-dry-monitor}

启动干模式发布后，您可以可视化历程执行以及用户档案如何通过历程分支和节点进行进度。

量度直接显示在历程画布中。 在历程画布的[实时报告中，了解有关历程实时报告和量度的更多信息](report-journey.md)。

![监视历程试运行执行](assets/dry-run-metrics.png)

您还可以访问练习的&#x200B;**最近24小时报告**&#x200B;和&#x200B;**所有时间报告**。 要访问这些报告，请单击历程画布右上角的&#x200B;**查看报告**&#x200B;按钮。

![访问历程试运行执行的报告](assets/dry-run-report.png)

>[!CAUTION]
>
> 仅当练习为&#x200B;**活动**&#x200B;时，报表数据才可用。  停止后，将无法再访问报表数据。 如果需要，请使用报告上方的&#x200B;**导出**&#x200B;按钮下载报告。


## 停止练习 {#journey-dry-run-stop}

14天后，练习历程自动过渡到&#x200B;**[!UICONTROL 草稿]**&#x200B;状态。

也可以手动停止练习历程。 要取消激活“Dry run（试运行）”模式，请执行以下步骤：

1. 打开要停止的练习历程。
1. 选择&#x200B;**[!UICONTROL 关闭]**&#x200B;按钮以结束测试。
确认屏幕中提供指向过去24小时和所有时间报表的链接。

   ![停止历程试运行执行](assets/dry-run-stop.png){width="50%"}

1. 单击&#x200B;**[!UICONTROL 返回草稿]**&#x200B;以进行确认。


## 护栏和限制 {#journey-dry-run-limitations}

* 处于练习模式的配置文件将计入[可启用的配置文件](../audience/license-usage.md)
* 处于试运行模式的历程将计入实时旅程配额
* 模拟历程不会影响业务规则
  <!--* When creating a new journey version, if a previous journey version is **Live**, then the Dry run activation is not allowed on the new version.-->
* 在练习中未启用&#x200B;**跳转**&#x200B;操作。
当源历程触发到目标历程的&#x200B;**跳转**&#x200B;事件时，该跳转事件将不适用于练习历程版本。例如，如果历程的最新版本为模拟运行，而上一个版本为&#x200B;**实时**，则跳转事件将忽略模拟运行版本，仅适用于&#x200B;**实时**&#x200B;版本。

## 历程步骤事件和练习 {#journey-step-events}

历程练习生成&#x200B;**stepEvents**。 这些stepEvents具有特定标志和练习ID： `inDryRun`和`dryRunID`。

![历程试运行架构属性](assets/dry-run-attributes.png)

* 当历程处于练习模式时，`_experience.journeyOrchestration.stepEvents.inDryRun`返回`true`，对于测试或实时历程（非练习）返回`null`。
* 在练习模式下，`_experience.journeyOrchestration.stepEvents.dryRunID`返回练习实例的ID；对于测试或实时历程，它是`null`。


如果将stepEvent数据导出到&#x200B;**外部系统**，则可以使用`inDryRun`标志筛选练习执行。

在使用[!DNL Adobe Experience Platform]查询服务分析&#x200B;**历程报告量度**&#x200B;时，必须排除练习生成的步骤事件。 为此，请排除`inDryRun`为`true`的步骤事件（即仅包括`inDryRun`为`null`或`false`的事件）。

## 常见问题 {#faq}

**练习是否向真实客户发送消息？**

没有。 练习使用实际生产数据，但不联系用户档案或更新用户档案信息。 不执行渠道操作（电子邮件、短信、推送），并将禁用自定义操作并将其响应设置为`null`。

**我需要什么权限才能启动或停止试运行？**

启动练习需要&#x200B;**[!DNL Publish journeys]**&#x200B;高级权限。 停止练习需要&#x200B;**[!DNL Manage journeys]**&#x200B;高级权限。 在[权限部分](../administration/permissions-overview.md)中了解详情。

**我可以在哪些历程中试运行？**

您可以对任何没有错误的&#x200B;**[!UICONTROL 草稿]**&#x200B;历程使用试运行。

**练习持续多长时间？**

14天后，练习历程自动转换回&#x200B;**[!UICONTROL 草稿]**&#x200B;状态。 您也可以随时手动停止试运行。

**是否在试运行期间执行等待活动和外部数据源？**

默认情况下，**等待**&#x200B;活动和&#x200B;**数据源**（包括外部数据源）在试运行期间被禁用。 您可以在[激活练习模式](#journey-dry-run-start)时更改此行为。

**练习配置文件和历程是否计入我的配额？**

是的。 处于练习模式的配置文件将计入[可参与配置文件](../audience/license-usage.md)，处于练习模式的历程将计入实时历程配额。 但是，模拟历程不会影响业务规则。

**停止测试后，我是否仍可访问模拟运行报告？**

没有。 仅当练习为&#x200B;**活动**&#x200B;时，报告数据才可用。 停止后，将无法再访问数据 — 如果需要，请使用报表上方的&#x200B;**导出**&#x200B;按钮提前下载数据。

**如何从我的报表中排除练习数据？**

练习生成标记为`inDryRun`和`dryRunID`的&#x200B;**stepEvents**。 使用[!DNL Adobe Experience Platform]查询服务分析历程报告量度时，排除`inDryRun`为`true`的步骤事件（仅包括`inDryRun`为`null`或`false`的事件）。

## 操作方法视频 {#dry-run-video}

在此视频中了解如何练习您的历程。

>[!VIDEO](https://video.tv.adobe.com/v/3464681/?learn=on&enablevpops)
