---
solution: Journey Optimizer
product: journey optimizer
title: 管理忠诚度挑战
description: 了解如何在Adobe Journey Optimizer中管理、监控和优化忠诚度挑战。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人测试版" type="Informative"
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---


# 管理挑战 {#manage-challenges}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md) — 概述、工作流程、先决条件
* [访问忠诚度挑战](access-loyalty-challenges.md) — 清点和筛选
* [创建挑战](create-challenges.md) — 生成并配置挑战
* [创建任务](create-tasks.md) — 定义挑战任务
* **管理挑战** ◀︎**您在这里** — 编辑、监视、优化

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私有测试版**&#x200B;中，可能在您的环境中不可用。 要请求获取访问权限，请联系您的Adobe代表。 了解有关[可用性标签](../rn/releases.md#availability-labels)的更多信息。

## 管理挑战 {#manage-challenges-section}

### 挑战生命周期 {#challenge-lifecycle}

<!-- VISUAL: Flowchart diagram showing challenge lifecycle with status transitions: Draft → Scheduled → Live → Completed/Stopped/Archived -->

挑战在其生命周期中会经历不同的状态：

* **草稿**：正在创建或编辑质询，尚不可供客户使用
* **已发布**：挑战处于活动状态，已创建关联的历程。

### 编辑挑战 {#edit-challenges}

您可以通过在“挑战”清单中打开挑战来编辑挑战。 编辑行为因质询状态而异：

**草稿挑战**：您拥有完整的编辑功能。 可以不受限制地修改所有属性、任务、内容和消息。

**已发布的挑战**：当您打开已发布的挑战进行编辑时，首先需要将其还原为草稿状态。

* 直接对自动生成历程所做的任何自定义都将丢失
* 挑战将返回草稿状态
* 进行更改后，必须再次保存并发布挑战
* 您必须重新激活关联的历程，才能将更新的挑战提供给客户

>[!IMPORTANT]
>
>无法撤消将已发布的挑战还原为草稿。 在继续之前，请考虑对活动历程的影响。

### 重复的挑战 {#duplicate-challenges}

复制挑战会创建一个包含所有任务、内容和消息传送的精确副本，使您能够快速创建新版本，而无需从头开始。

要复制挑战：

1. 导航到&#x200B;**[!UICONTROL 挑战]**&#x200B;选项卡，并找到要复制的挑战。

1. 选择该质询旁边的![](assets/do-not-localize/Smock_More_18_N.svg)图标，然后选择&#x200B;**[!UICONTROL 复制]**。

1. 创建质询的副本。 打开重复的质询并修改必要的属性。

1. 保存重复的质询并生成关联的历程。

### 监控性能 {#monitor-performance}

<!-- SCREENSHOT: Challenge Performance tab showing key metrics dashboard with participation, completion, reward, and engagement metrics -->

通过关键量度跟踪挑战表现：

* **参与率量度**：
   * 注册：加入挑战的客户数量
   * 积极参加者：目前参与该挑战的客户
* **完成指标**：
   * 完成率：完成挑战的已注册客户的百分比
   * 平均完成时间：完成所有任务所用的平均时间
* **奖励量度**：
   * 已分配的奖励总计：所有已给予的奖励的总值
   * 按类型列出的奖励：按奖励类别列出的奖励细目
* **参与量度**：
   * 内容卡展示次数：质询内容卡显示的次数
   * 消息投放：在所有渠道中成功发送的消息计数

要访问性能数据，请执行以下操作：

1. 导航到“忠诚度挑战”清单中的&#x200B;**[!UICONTROL 挑战]**&#x200B;选项卡。

1. 选择要监视的挑战。

1. 打开&#x200B;**[!UICONTROL 性能]**&#x200B;选项卡以查看实时量度和分析。

<!-- SCREENSHOT: Journey report showing challenge performance data with graphs and tables -->

您还可以在[自动生成的历程报告](../reports/journey-global-report-cja.md)中访问详细的性能数据，这些数据提供了其他见解和历史趋势。

## 管理任务 {#manage-tasks}

任务是可重复使用的组件，可以跨多个挑战使用。 有效地管理任务可确保忠诚度计划的一致性，并使集中更新任务定义更容易。 在一个挑战中创建的任务可以在其他挑战中重复使用，从而减少重复和维护标准化。

### 编辑任务 {#edit-tasks}

您可以从任务清单中编辑现有任务。 请考虑以下事项：

* **未用于活动挑战中的任务**：可以自由编辑 — 所有属性都可以修改而不会受到影响
* **在实时挑战中使用的任务**：请务必谨慎，因为更改会影响使用该任务的所有挑战 — 修改将立即应用于所有引用挑战

要编辑任务，请执行以下操作：

1. 导航到“忠诚度挑战”清单中的&#x200B;**[!UICONTROL 任务]**&#x200B;选项卡。

1. 找到要编辑的任务。

1. 选择任务名称以在编辑模式下将其打开。

1. 根据需要修改任务属性：
   * 更新任务名称或描述
   * 更改活动类型或属性
   * 调整合格物料和排除项
   * 修改数量或金额需求

1. 保存更改。

>[!WARNING]
>
>在编辑实时挑战中积极使用的任务时，请考虑使用新版本创建重复项而不是修改原始项。 这样可防止对活动挑战进行意外更改，并允许您在应用修改之前对其进行测试。

### 删除任务 {#delete-tasks}

仅当任务当前未在任何挑战中使用时，才能将其删除。 删除任务之前：

* 检查任务清单中的挑战&#x200B;**[!UICONTROL 计数中的]**&#x200B;使用次数
* 确保没有草稿、计划或实时挑战引用任务

要删除任务，请执行以下操作：

1. 导航到“忠诚度挑战”清单中的&#x200B;**[!UICONTROL 任务]**&#x200B;选项卡。

1. 找到要删除的任务。

1. 验证挑战&#x200B;**[!UICONTROL 计数中使用的]**&#x200B;是否显示0。 如果计数大于0，则在删除之前必须先从所有挑战中移除该任务。

1. 选择任务旁边的![](assets/do-not-localize/Smock_More_18_N.svg)图标。

1. 选择&#x200B;**[!UICONTROL 删除]**。

1. 在对话框中确认删除。

>[!NOTE]
>
>如果任务用于任何挑战（草稿、已计划或实时），则必须先将其从所有挑战中移除，然后才能将其删除。 请考虑存档或复制任务，而不是删除它们（如果将来可能需要）。
