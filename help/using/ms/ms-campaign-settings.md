---
solution: Journey Optimizer
product: journey optimizer
title: 配置多步营销活动设置
description: 了解如何使用Adobe Journey Optimizer配置多步营销活动设置
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 7%

---


# 配置多步营销活动设置 {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="多步骤营销活动属性"
>abstract="在此屏幕中，选择要用于创建多步骤营销活动的模板并指定标签。 展开&#x200B;**其他选项**&#x200B;部分以配置更多设置，如多步骤营销活动内部名称、其文件夹、时区和主管组。 强烈建议选择一个主管组，以便如果出错，可提醒操作员。"

在画布中创建多步骤营销活动或编排多步骤营销活动时，您可以访问与多步骤营销活动相关的高级设置。 例如，您可以为多步骤营销活动设置特定时区，管理多步骤营销活动在出现错误时的行为方式，或管理应清除多步骤营销活动历史记录的延迟。

这些设置是在创建多步骤营销活动时选择的模板中预先配置的，但可视需要为此特定的多步骤营销活动进行编辑。

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## 多步骤营销活动属性 {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="多步骤营销活动属性"
>abstract="本节提供创建多步骤营销活动时也可以访问的通用多步骤营销活动属性。 您可以选择要用于创建多步骤营销活动的模板并指定标签。 展开其他选项部分以配置特定设置，例如存储文件夹或时区的多步营销活动。"

**[!UICONTROL 属性]**&#x200B;部分提供了通用设置，可在创建多步骤营销活动时配置这些设置。 要访问现有多步骤营销活动的属性，请单击多步骤营销活动画布上方操作栏中可用的&#x200B;**[!UICONTROL 设置]**&#x200B;按钮。


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


这些属性包括：

* 列表中显示的多步营销活动的&#x200B;**[!UICONTROL 标签]**。
* 多步骤营销活动的&#x200B;**[!UICONTROL 内部名称]**。
* 应保存多步骤营销活动的&#x200B;**[!UICONTROL 文件夹]**。
* 要在所有多步骤营销活动中使用的默认&#x200B;**[!UICONTROL 时区]**。 默认情况下，多步骤营销活动的时区就是为当前营销活动操作员定义的时区。
可能的值包括：
   * **服务器时区**&#x200B;以使用Adobe Experience Platform组织的时区
   * **操作员时区**，使用执行多步骤活动的操作员的时区
   * **数据库的时区**&#x200B;以使用数据库服务器的时区
   * 特定时区
* 当多步骤营销活动失败时，将通过电子邮件通知属于&#x200B;**[!UICONTROL 主管]**&#x200B;字段中所选操作员组的操作员。
* 您还可以输入多步骤营销活动的&#x200B;**[!UICONTROL 描述]**。

## 分段设置  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="分段设置"
>abstract="在此部分中，您可以选择定向维度在多步营销活动中定向用户档案，并选择在两个执行之间保留工作流结果。 此选项应仅用于测试目的，不得在生产多步骤活动中启用。"

* **[!UICONTROL 定向维度]**：选择要用于定向用户档案的定向维度：收件人、合同受益人、操作员、订阅者等。

* **[!UICONTROL 保留两次执行之间的临时人口结果]**：默认情况下，仅保留多步骤活动的最后一次执行的工作表。 以前执行的工作表由每天运行的多步技术活动清除。

  如果启用此选项，则即使在执行多步骤活动后，也会保留工作表。 您可以将其用于测试目的，因此必须&#x200B;**仅**&#x200B;用于开发或暂存环境。 在生产多步骤活动中绝不能对其进行检查。

## 执行设置  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="执行设置"
>abstract="在此部分中，您可以配置与工作流执行相关的设置，例如多步营销活动历史记录的保留天数。"

* **[!UICONTROL 历史记录（以天为单位）]**：指定必须清除历史记录的天数。 历史记录包含与多步骤活动相关的元素：日志、任务、事件（链接到多步骤活动操作的技术对象）。 现成的多步营销活动模板的默认值为30天。 清除历史记录由数据库清理技术多步骤活动执行，默认情况下，每天都会执行该活动

  >[!IMPORTANT]
  >
  >如果将&#x200B;**[!UICONTROL 历史记录（天）]**&#x200B;字段保留为空，其值将被视为“1”，这表示历史记录将在 1 天后清除。

* **[!UICONTROL 默认关联性]**：如果您的安装包含多个多步骤营销活动服务器，请使用此字段指定将在其中执行多步骤营销活动的服务器。 这强制在特定服务器上执行该多步营销活动。 您可以选择任何现有的关联名称，但请确保不使用空格或标点符号。 如果使用不同的服务器，请指定不同的名称（用逗号分隔）。

  >[!IMPORTANT]
  >
  >如果此字段中定义的值在任何服务器上不存在，则多步骤营销活动将保持挂起状态。


* **[!UICONTROL 将SQL查询保存到日志]**：选中此选项可将workflmulti-step campaignow中的SQL查询保存到日志中。 此功能是为高级用户保留的。它适用于包含定向活动（如&#x200B;**[!UICONTROL 构建受众]**）的多步营销活动。 启用此选项后，在多步骤活动执行期间发送到数据库的SQL查询将显示在多步骤活动的日志中，以便您分析这些查询以优化查询或诊断问题。

## 错误管理设置  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="错误管理设置"
>abstract="在此部分中，您可以定义多步骤营销活动在执行期间应如何管理错误。 您可以选择暂停流程、忽略特定数量的错误或停止多步骤营销活动执行。"

* **[!UICONTROL 错误管理]**：此字段允许您定义多步骤营销活动任务出现错误时要执行的操作。 有三种可能的选项：

   * **[!UICONTROL 暂停进程]**：多步骤营销活动自动暂停，其状态更改为&#x200B;**[!UICONTROL 失败]**。 问题解决后，使用&#x200B;**[!UICONTROL 恢复]**&#x200B;按钮恢复多步骤营销活动。
   * **[!UICONTROL 忽略]**：触发错误的任务状态更改为&#x200B;**[!UICONTROL 失败]**，但多步骤营销活动会保留&#x200B;**[!UICONTROL 已启动]**&#x200B;状态。<!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL 中止进程]**：多步骤营销活动自动停止，其状态更改为&#x200B;**[!UICONTROL 失败]**。 问题解决后，使用&#x200B;**[!UICONTROL 开始]**&#x200B;按钮重新启动多步骤营销活动。

* **[!UICONTROL 连续错误]**：在&#x200B;**[!UICONTROL 如果出现错误]**&#x200B;字段中选择&#x200B;**[!UICONTROL 忽略]**&#x200B;值时，此字段将变为可用。 您可以指定在流程停止前可忽略的错误的数量。一旦达到此数量，多步骤营销活动状态将更改为&#x200B;**[!UICONTROL 失败]**。 如果此字段的值为0，则无论错误数量如何，多步骤营销活动都不会停止。

## 初始化脚本 {#initialization-script}

**初始化脚本**&#x200B;允许您初始化变量或修改活动属性。 单击&#x200B;**编辑代码**&#x200B;按钮并键入要执行的代码片段。 执行多步骤营销活动时，将调用脚本。 请参阅与[事件变量](event-variables.md)相关的部分。

