---
solution: Journey Optimizer
product: journey optimizer
title: 使用Journey Optimizer创建编排的营销活动
description: 了解如何使用Adobe Journey Optimizer创建编排的活动
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 7f535b87e415ae9191199b34476adb5c977b66e9
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 17%

---


# 创建精心策划的营销活动 {#create-first-campaign}

+++ 目录

| 欢迎使用编排的营销活动 | 启动您的第一个编排的营销活动 | 查询数据库  | 编排的营销活动活动 |
|---|---|---|---|
| [开始使用编排的营销活动](gs-orchestrated-campaigns.md)<br/><br/>[配置步骤](configuration-steps.md)<br/><br/>[创建编排的营销活动的关键步骤](gs-campaign-creation.md) | [创建协调的营销活动](create-orchestrated-campaign.md)<br/><br/>[协调活动](orchestrate-activities.md)<br/><br/>[发送包含协调的营销活动的消息](send-messages.md)<br/><br/>[开始并监视营销活动](start-monitor-campaigns.md)<br/><br/>[报告](reporting-campaigns.md) | [使用查询Modeler](orchestrated-query-modeler.md)<br/><br/>[生成您的第一个查询](build-query.md)<br/><br/>[编辑表达式](edit-expressions.md) | [开始使用活动](activities/about-activities.md)<br/><br/>活动：<br/>[And-join](activities/and-join.md) - [生成受众](activities/build-audience.md) - [更改维度](activities/change-dimension.md) - [组合](activities/combine.md) - [重复数据删除](activities/deduplication.md) - [扩充](activities/enrichment.md) - [分支](activities/fork.md) - [协调](activities/reconciliation.md) - [拆分](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="协同营销活动列表"
>abstract="**多步骤**&#x200B;选项卡列出了所有的协同营销活动。单击协同营销活动的名称即可对其进行编辑。使用&#x200B;**创建协同营销活动**&#x200B;按钮，添加新的协同营销活动。"

## 创建营销活动

要创建编排的营销活动，请执行以下步骤：

1. 要创建&#x200B;**编排的营销活动**，请浏览到&#x200B;**营销活动**&#x200B;菜单。

1. 单击屏幕右上角的&#x200B;**[!UICONTROL 创建编排的营销活动]**&#x200B;按钮。

1. 在编排的营销活动&#x200B;**属性**&#x200B;对话框中，选择要用于创建编排的营销活动的模板（也可以使用默认的内置模板）。 [了解有关编排的活动模板的更多信息](#campaign-templates)。

1. 输入编排的营销活动的标签。 此外，我们强烈建议您在屏幕的&#x200B;**[!UICONTROL 其他选项]**&#x200B;部分的专用字段中向编排的活动添加描述。

1. 展开&#x200B;**[!UICONTROL 其他选项]**&#x200B;部分，为编排的活动配置更多设置。

1. 单击&#x200B;**[!UICONTROL 创建编排的营销活动]**&#x200B;按钮以确认创建编排的营销活动。

现在，您的编排活动已创建并可在工作流列表中使用。 您现在可以访问其可视画布并开始添加、配置和编排其将执行的任务。 [了解如何编排已编排的营销活动](orchestrate-activities.md)。

## 配置Campaign设置

新管理员设置>架构、执行字段和合并策略概述。 [了解详情](configuration-steps.md)

## 使用协同营销活动模板 {#campaign-templates}

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_for_campaign"
>title="协同营销活动模板"
>abstract="协同营销活动模板包含预先配置的设置和活动，可重复用于创建新的协同营销活动。"

>[!CONTEXTUALHELP]
>id="ajo_workflow_template_creation_properties"
>title="协同营销活动属性"
>abstract="协同营销活动模板包含预先配置的设置和活动，可重复用于创建新的协同营销活动。在此屏幕中，输入协同营销活动模板的标签并配置其设置，例如其内部名称、文件夹和执行文件夹、时区和主管组。"

协同营销活动模板包含预先配置的设置和活动，可重复用于创建新的协同营销活动。创建编排的活动时，您可以从编排的活动属性中选择编排的活动模板。 默认情况下，会提供一个空模板。

您可以从现有的编排活动创建模板，或从头开始创建新模板。 这两种方法详见下文。

>[!BEGINTABS]

>[!TAB 从现有编排的活动创建模板]

要从现有的编排活动创建编排的活动模板，请执行以下步骤：

1. 打开&#x200B;**促销活动**&#x200B;菜单，然后浏览到编排的促销活动以另存为模板。
1. 单击编排的营销活动名称右侧的三个圆点，然后选择&#x200B;**复制为模板**。
1. 在弹出窗口中，确认创建模板。
1. 在编排的活动模板画布中，根据需要检查、添加和配置活动。
1. 从&#x200B;**设置**&#x200B;按钮浏览到设置以更改编排的活动模板的名称，然后输入描述。
1. 选择模板的&#x200B;**文件夹**&#x200B;和&#x200B;**执行文件夹**。 文件夹是保存编排的活动模板的位置。 执行文件夹是保存基于此模板创建的编排的营销活动的文件夹。
1. 保存更改。

现在，模板列表中提供了编排的活动模板。 您可以基于此模板创建编排的营销活动。 此编排的营销活动将预配置模板中定义的设置和活动。


>[!TAB 从头开始创建模板]


要从头开始创建编排的活动模板，请执行以下步骤：

1. 打开&#x200B;**Campaign**&#x200B;菜单并浏览到&#x200B;**模板**&#x200B;选项卡。 您可以查看可用的编排活动模板列表。
1. 单击屏幕右上角的&#x200B;**[!UICONTROL 创建模板]**&#x200B;按钮。
1. 输入标签并打开附加选项，以输入编排的活动模板的描述。
1. 选择模板的文件夹和执行文件夹。 文件夹是保存编排的活动模板的位置。 执行文件夹是保存基于此模板创建的编排的营销活动的文件夹。
1. 单击&#x200B;**创建**&#x200B;按钮确认您的设置。
1. 在编排的活动模板画布中，根据需要添加和配置活动。

   ![](assets/wf-template-activities.png){zoomable="yes"}

1. 保存更改。

现在，模板列表中提供了编排的活动模板。 您可以基于此模板创建编排的营销活动。 此编排的营销活动将预配置模板中定义的设置和活动。

>[!ENDTABS]
