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
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---


# 访问忠诚度挑战 {#access-loyalty-challenges}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md) — 概述、工作流程、先决条件
* **访问忠诚度挑战** ◀︎**您位于此处** — 清点和筛选
* [创建挑战](create-challenges.md) — 生成并配置挑战
* [管理挑战](manage-challenges.md) — 编辑、监视、优化

>[!ENDSHADEBOX]

## 访问忠诚度挑战清单 {#access-inventory}

要了解忠诚度挑战，请执行以下操作：

1. 在Adobe Journey Optimizer的&#x200B;**[!UICONTROL 客户历程]**&#x200B;部分下的左侧导航菜单中选择&#x200B;**[!UICONTROL 忠诚度挑战]**。

2. 此时将显示“忠诚度挑战”页面，其中包含两个选项卡：
   * **[!UICONTROL 挑战]**：查看和管理所有忠诚度挑战
   * **[!UICONTROL 任务]**：查看和管理所有可在不同挑战中重用的任务

默认情况下，**[!UICONTROL 挑战]**&#x200B;选项卡处于选中状态，显示组织中的所有现有挑战。

## “挑战”选项卡 {#challenges-tab}

“挑战”选项卡按上次修改日期显示所有挑战，最近修改的挑战显示在最前。

### 了解挑战清单 {#inventory-overview}

“挑战”清单显示了所有挑战，并提供了以下信息：

* **[!UICONTROL 质询名称]**：您分配给质询的名称
* **[!UICONTROL 状态]**：质询的当前状态（请参阅下面的状态描述）
* **[!UICONTROL 类型]**：质询类型（标准、条纹或顺序）
* **[!UICONTROL 开始日期]**：质询生效时
* **[!UICONTROL 结束日期]**：质询过期时间
* **[!UICONTROL 创建者]**：创建质询的用户
* **[!UICONTROL 上次修改时间]**：上次修改的日期和时间
* **[!UICONTROL 标记]**：应用于组织挑战的任何标记

### 质询状态 {#challenge-statuses}

挑战可能具有以下状态：

* **[!UICONTROL 草稿]**：正在创建或编辑挑战，但尚未发布
* **[!UICONTROL 已计划]**：已发布挑战，并计划在以后的某个日期开始
* **[!UICONTROL 实时]**：挑战当前处于活动状态并且可供目标受众使用
* **[!UICONTROL 已完成]**：质询已超过其结束日期，或所有目标均已实现
* **[!UICONTROL 已停止]**：在完成前已手动停止挑战
* **[!UICONTROL 已存档]**：已存档质询以进行组织

### 搜索和过滤挑战 {#search-challenges}

使用搜索功能可按名称或描述快速查找特定挑战。

您还可以应用过滤器根据特定条件缩小质询列表。 您可以合并多个筛选器以优化搜索。

您可以按任务的当前状态、类型、开始或结束日期或您为组织应用的标记来筛选任务。

### 针对挑战采取行动 {#inventory-actions}

在“挑战”选项卡中，您可以对挑战执行快速操作：

* **查看质询详细信息**：选择质询名称以打开其详细信息页面
* **编辑质询**：选择更多操作菜单（三个圆点），然后选择&#x200B;**[!UICONTROL 编辑]**
* **复制挑战**：选择“更多操作”菜单，然后选择&#x200B;**[!UICONTROL 复制]**
* **停止实时质询**：选择“更多操作”菜单，然后选择&#x200B;**[!UICONTROL 停止]**
* **存档挑战**：选择“更多操作”菜单，然后选择&#x200B;**[!UICONTROL 存档]**
* **删除草稿质询**：选择更多操作菜单，然后选择&#x200B;**[!UICONTROL 删除]**（仅适用于草稿）

### 创建新的挑战 {#create-from-inventory}

从“挑战”选项卡创建新的挑战：

1. 选择右上角的&#x200B;**[!UICONTROL 创建挑战]**。

2. 挑战创建工作流开始。

有关详细说明，请参阅[创建挑战](create-challenges.md)。

## “任务”选项卡 {#tasks-tab}

“任务”选项卡显示所有可用于多个挑战的可重用任务。 在创建或编辑任何挑战时，可以选择此处创建的任务。

### 了解任务清单 {#tasks-inventory-overview}

“任务”清单显示所有任务，其信息如下：

* **[!UICONTROL 任务名称]**：分配给任务的名称
* **[!UICONTROL 任务类型]**：操作类型（购买、支出金额、访问、参与、自定义事件）
* **[!UICONTROL 描述]**：任务要求的简要描述
* **[!UICONTROL 创建者]**：创建任务的用户
* **[!UICONTROL 上次修改时间]**：上次修改的日期和时间
* **[!UICONTROL 用于挑战]**：当前使用此任务的挑战数

### 从“任务”选项卡创建任务 {#create-tasks-from-tab}

您可以通过两种方式创建任务：

1. **从“任务”选项卡** （建议用于可重用任务）：
   * 导航到&#x200B;**[!UICONTROL 任务]**&#x200B;选项卡
   * 选择&#x200B;**[!UICONTROL 创建任务]**
   * 配置任务属性（名称、类型、数量、产品过滤器、奖励）
   * 保存任务以使其可用于任何挑战

2. **创建挑战时** （针对挑战特定的任务）：
   * 在创建挑战期间，在“任务”部分中选择&#x200B;**[!UICONTROL 添加任务]**
   * 选择&#x200B;**[!UICONTROL 创建新任务]**&#x200B;或从现有任务中选择
   * 通过这种方式创建的任务也会保存到Tasks清单中，并且可重复使用

>[!TIP]
>
>当您计划跨多个挑战使用同一任务时，建议从“任务”选项卡创建任务。 这样可以确保一致性，并更容易集中更新任务定义。

### 对任务执行操作 {#tasks-actions}

在“任务”选项卡中，您可以对任务执行操作：

* **查看任务详细信息**：选择任务名称以查看完整配置
* **编辑任务**：选择更多操作菜单（三个圆点），然后选择&#x200B;**[!UICONTROL 编辑]**
* **复制任务**：选择“更多操作”菜单，然后选择&#x200B;**[!UICONTROL 复制]**
* **删除任务**：选择“更多操作”菜单，然后选择&#x200B;**[!UICONTROL 删除]**（仅当未在任何活动挑战中使用时）
* **查看使用情况**：查看当前使用该任务的挑战

## 后续步骤 {#next-steps}

现在您已知道如何访问和浏览忠诚度挑战清单：

* [创建挑战](create-challenges.md) — 了解如何构建您的第一个挑战
* [管理挑战](manage-challenges.md) — 了解如何编辑和监控挑战
