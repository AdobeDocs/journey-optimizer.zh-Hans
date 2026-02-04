---
solution: Journey Optimizer
product: journey optimizer
title: 访问忠诚度挑战
description: 了解如何在Adobe Journey Optimizer中访问、搜索和过滤忠诚度挑战。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人测试版" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---


# 访问忠诚度挑战 {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md) — 概述、工作流程、先决条件
* **访问忠诚度挑战** ◀︎**您位于此处** — 清点和筛选
* [创建挑战](create-challenges.md) — 生成并配置挑战
* [创建任务](create-tasks.md) — 定义挑战任务
* [管理挑战](manage-challenges.md) — 编辑、监视、优化

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私有测试版**&#x200B;中，可能在您的环境中不可用。 要请求获取访问权限，请联系您的Adobe代表。 了解有关[可用性标签](../rn/releases.md#availability-labels)的更多信息。

## 访问忠诚度挑战清单 {#access-inventory}

<!-- SCREENSHOT: Journey Optimizer main menu showing "Loyalty challenges" under "Customer journeys" section -->

要访问忠诚度挑战，请导航到Journey Optimizer并选择&#x200B;**[!UICONTROL 客户历程]**&#x200B;部分下的&#x200B;**[!UICONTROL 忠诚度挑战]**。

<!-- SCREENSHOT: Loyalty Challenges landing page showing the two tabs: Challenges and Tasks -->

此时将显示“忠诚度挑战”页面，其中包含两个选项卡：

* **[!UICONTROL 挑战]**：查看和管理所有忠诚度挑战

* **[!UICONTROL 任务]**：查看和管理所有可在不同挑战中重用的任务

## 挑战清单 {#challenges-tab}

<!-- SCREENSHOT: Challenges tab showing the inventory table with columns: Challenge name, Status, Type, Start date, End date, Created by, Last modified, Tags -->

“挑战”选项卡按上次修改日期显示所有挑战，最近修改的挑战显示在最前。 将显示以下信息：

* **[!UICONTROL 质询名称]**：您分配给质询的名称
* **[!UICONTROL 状态]**：质询的当前状态（请参阅下面的状态描述）
* **[!UICONTROL 类型]**：质询类型（标准、条纹或顺序）
* **[!UICONTROL 开始日期]**：质询生效时
* **[!UICONTROL 结束日期]**：质询过期时间
* **[!UICONTROL 创建者]**：创建质询的用户
* **[!UICONTROL 上次修改时间]**：上次修改的日期和时间
* **[!UICONTROL 标记]**：应用于组织挑战的任何标记

### 质询状态 {#challenge-statuses}

<!-- VISUAL: Status badges showing different challenge statuses with color coding: Draft (gray), Scheduled (blue), Live (green), Completed (gray), Stopped (red), Archived (gray) -->

显示的挑战具有不同的状态，指示其在生命周期中的当前状态：

* **草稿**：正在创建或编辑挑战
* **已计划**：挑战已发布，将在开始日期生效
* **实时**：挑战正在进行，客户可以参加
* **已完成**：挑战结束日期已错过或目标已实现
* **已停止**：在完成前已手动停止挑战
* **已存档**：已存档质询以进行组织

有关状态转换和挑战生命周期的详细信息，请参阅[挑战生命周期](manage-challenges.md#challenge-lifecycle)。

### 搜索和过滤挑战 {#search-challenges}

<!-- SCREENSHOT: Search bar and filter panel showing available filters (status, type, dates, tags) with an example of active filters applied -->

您可以使用搜索和筛选器快速找到挑战：

**搜索：**

* 使用搜索栏，通过输入质询名称或描述的关键字来查找质询。 在您键入内容时，搜索将实时更新结果。

**筛选器：**

* 应用一个或多个筛选器以缩小结果范围：
   * **状态**：按质询状态筛选（草稿、已计划、实时、已完成、已停止、已存档）
   * **类型**：按质询类型筛选（标准、条纹、顺序）
   * **日期**：按开始日期或结束日期范围筛选
   * **标记**：按应用于挑战的标记进行筛选

您可以同时合并多个过滤器。 例如，筛选标记为“Summer2024”的Live Standard挑战，以快速找到活动的季节性活动。

要清除筛选器，请选择&#x200B;**[!UICONTROL 全部清除]**&#x200B;或删除单个筛选器。

### 针对挑战采取行动 {#inventory-actions}

<!-- SCREENSHOT: More actions menu (three dots) expanded showing options: Edit, Duplicate, Stop, Archive, Delete -->

在“挑战”选项卡中，您可以对挑战执行快速操作：

* **查看质询详细信息**：选择质询名称以打开其详细信息页面
* **编辑挑战**：选择&#x200B;**[!UICONTROL 更多操作]**&#x200B;菜单（三个圆点），然后选择&#x200B;**[!UICONTROL 编辑]**
* **复制挑战**：选择&#x200B;**[!UICONTROL 更多操作]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 复制]**
* **停止实时质询**：选择&#x200B;**[!UICONTROL 更多操作]**&#x200B;菜单并选择&#x200B;**[!UICONTROL 停止]**
* **存档挑战**：选择&#x200B;**[!UICONTROL 更多操作]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 存档]**
* **删除草稿质询**：选择&#x200B;**[!UICONTROL 更多操作]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 删除]**（仅适用于草稿）

有关创建后管理挑战的详细信息，包括编辑限制、复制策略、性能监控和疑难解答，请参阅[管理挑战](manage-challenges.md)。

## 任务清单 {#tasks-tab}

<!-- SCREENSHOT: Tasks tab showing the inventory table with columns: Task name, Task type, Description, Created by, Last modified, Used in challenges -->

“任务”选项卡显示所有可用于多个挑战的可重用任务。 在创建或编辑任何挑战时，可以选择此处创建的任务。

任务清单显示以下信息：

* **[!UICONTROL 任务名称]**：分配给任务的名称
* **[!UICONTROL 任务类型]**：操作类型（购买、支出金额、访问、参与、自定义事件）
* **[!UICONTROL 描述]**：任务要求的简要描述
* **[!UICONTROL 创建者]**：创建任务的用户
* **[!UICONTROL 上次修改时间]**：上次修改的日期和时间
* **[!UICONTROL 用于挑战]**：当前使用此任务的挑战数

### 对任务执行操作 {#tasks-actions}

在“任务”选项卡中，您可以对任务执行操作：

* **查看任务详细信息**：选择任务名称以查看完整配置
* **编辑任务**：选择&#x200B;**[!UICONTROL 更多操作]**&#x200B;菜单（三个圆点），然后选择&#x200B;**[!UICONTROL 编辑]**
* **复制任务**：选择&#x200B;**[!UICONTROL 更多操作]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL 复制]**
* **删除任务**：选择&#x200B;**[!UICONTROL 更多操作]**&#x200B;菜单并选择&#x200B;**[!UICONTROL 删除]**（仅当未在任何活动挑战中使用时）
* **查看使用情况**：查看当前使用该任务的挑战

## 后续步骤 {#next-steps}

现在您已知道如何访问和浏览忠诚度挑战清单：

* [创建挑战](create-challenges.md) — 了解如何构建第一个挑战并配置任务
* [创建任务](create-tasks.md) — 了解如何为挑战定义可重用的任务
* [管理挑战](manage-challenges.md) — 了解如何编辑、监控和优化挑战
