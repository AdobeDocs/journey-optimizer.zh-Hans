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
source-git-commit: 8c8fb70baf66d2b48c81c6344717be18993141f8
workflow-type: tm+mt
source-wordcount: '1106'
ht-degree: 16%

---

# 历程试运行 {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="试运行模式"
>abstract="当前历程处于试运行状态。历程试运行是 Adobe Journey Optimizer 中的一种特殊历程发布模式，使历程设计人员能够在不接触真实客户或更新轮廓信息的前提下，使用真实生产数据对历程进行测试。此功能有助于历程设计人员在正式发布前验证历程设计和受众定位，从而增强信心。"


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="以试运行模式发布历程"
>abstract="试运行是 Adobe Journey Optimizer 提供的一种特殊历程发布模式，允许历程设计人员使用真实的生产数据测试历程。设计历程后，执行试运行以确认它可以正常工作并确保步骤正确无误。通过此发布模式，您可以对历程进行冒烟测试，而无需向任何轮廓发送通信。"

历程试运行是 Adobe Journey Optimizer 中的一种特殊历程发布模式，使历程设计人员能够在不接触真实客户或更新轮廓信息的前提下，使用真实生产数据对历程进行测试。此功能有助于历程设计人员在正式发布前验证历程设计和受众定位，从而增强信心。


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

  ![练习历程中的操作活动灰显](assets/dry-run-greyed-activities.png){width="80%" align="left"}

* 默认情况下，**数据源**（包括外部数据源）和&#x200B;**等待**&#x200B;活动在试运行期间处于禁用状态。 但是，在激活练习模式[时，您可以更改此行为](#journey-dry-run-start)。

* 未执行&#x200B;**反应**&#x200B;节点：进入它的所有配置文件都将成功退出。 但是，以下优先规则适用：
   * 如果&#x200B;**反应**&#x200B;节点与一个或多个并行的&#x200B;**单一事件**&#x200B;节点一起使用，则配置文件将始终通过反应事件。
   * 如果&#x200B;**反应**&#x200B;节点与一个或多个并行的&#x200B;**反应事件**&#x200B;节点一起使用，则配置文件将始终通过画布中的第一个节点（顶部的节点）。

>[!CAUTION]
>
>* 启动模拟运行的权限仅限于具有&#x200B;**[!DNL Publish journeys]**&#x200B;高级权限的用户。 停止模拟运行的权限仅限于具有&#x200B;**[!DNL Manage journeys]**&#x200B;高级权限的用户。 在[!DNL Journey Optimizer]本节[中了解有关管理](../administration/permissions-overview.md)用户访问权限的更多信息。
>
>* 在开始使用练习功能之前，[请阅读护栏和限制](#journey-dry-run-limitations)。

## 开始试运行 {#journey-dry-run-start}

您可以在任何草稿历程中使用模拟运行功能，而不会出错。

要激活试运行，请执行以下步骤：

1. 打开要测试的历程。
1. 选择&#x200B;**练习**&#x200B;按钮。

   ![开始历程试运行](assets/dry-run-button.png)

1. 如果要启用或禁用&#x200B;**等待**&#x200B;活动和&#x200B;**外部数据源**&#x200B;调用，请选择，并确认练习发布。

   ![确认历程试运行发布](assets/dry-run-publish.png){width="50%" align="left"}

   转换过程中出现状态消息&#x200B;**正在激活练习**。

1. 一旦激活，历程将进入&#x200B;**练习**&#x200B;模式。


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

14天后，练习历程自动过渡到&#x200B;**草稿**&#x200B;状态。

也可以手动停止练习历程。 要取消激活“Dry run（试运行）”模式，请执行以下步骤：

1. 打开要停止的练习历程。
1. 选择&#x200B;**关闭**按钮以结束测试。
确认屏幕中提供指向过去24小时和所有时间报表的链接。

   ![停止历程试运行执行](assets/dry-run-stop.png){width="50%" align="left"}

1. 单击&#x200B;**返回草稿**&#x200B;以进行确认。


## 护栏和限制 {#journey-dry-run-limitations}

* 处于试运行模式的配置文件将计入可参与配置文件
* 处于试运行模式的历程将计入实时旅程配额
* 模拟历程不会影响业务规则
  <!--* When creating a new journey version, if a previous journey version is **Live**, then the Dry run activation is not allowed on the new version.-->
* 在练习中未启用&#x200B;**跳转**操作。
当源历程触发到目标历程的**跳转**&#x200B;事件时，该跳转事件将不适用于练习历程版本。 例如，如果历程的最新版本为模拟运行，而上一个版本为&#x200B;**实时**，则跳转事件将忽略模拟运行版本，仅适用于&#x200B;**实时**&#x200B;版本。

## 历程步骤事件和练习 {#journey-step-events}

历程练习生成&#x200B;**stepEvents**。 这些stepEvents具有特定标志和练习ID： `inDryRun`和`dryRunID`。

![历程试运行架构属性](assets/dry-run-attributes.png)

* 如果已激活模拟运行，`_experience.journeyOrchestration.stepEvents.inDryRun`将返回`true`，否则返回`false`
* `_experience.journeyOrchestration.stepEvents.dryRunID`返回练习实例的ID


如果将stepEvent数据导出到&#x200B;**外部系统**，则可以使用`inDryRun`标志筛选练习执行。

使用Adobe Experience Platform查询服务分析&#x200B;**历程报告量度**&#x200B;时，必须排除练习生成的步骤事件。 要执行此操作，请将`inDryRun`标志设置为`false`。

