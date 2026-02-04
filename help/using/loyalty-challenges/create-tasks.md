---
solution: Journey Optimizer
product: journey optimizer
title: 创建任务以应对忠诚度挑战
description: 了解如何在Adobe Journey Optimizer中创建和配置忠诚度挑战任务。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人测试版" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---


# 创建任务 {#create-tasks}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md) — 概述、工作流程、先决条件
* [访问忠诚度挑战](access-loyalty-challenges.md) — 清点和筛选
* [创建挑战](create-challenges.md) — 生成并配置挑战
* **创建任务** ◀&rbrace;︎**您位于此处** — 定义挑战任务
* [管理挑战](manage-challenges.md) — 编辑、监视、优化

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私有测试版**&#x200B;中，可能在您的环境中不可用。 要请求获取访问权限，请联系您的Adobe代表。 了解有关[可用性标签](../rn/releases.md#availability-labels)的更多信息。

## 概述 {#overview}

任务定义客户在忠诚度挑战中必须完成的特定操作或里程碑以获取奖励。 您可以配置任务类型、数量、产品要求和奖励值，以创建引人入胜的个性化忠诚度体验。

每项任务都是可衡量的操作，有助于完成挑战。 任务是可重复使用的组件，可以独立创建，然后添加到一个或多个挑战，或直接在挑战中创建。

### 任务在不同挑战类型中如何工作 {#task-overview}

<!-- VISUAL: Diagram showing how task completion works differently for Standard, Streak, and Sequential challenges with examples -->

根据您的挑战类型（“标准”、“条纹”或“顺序”），客户完成任务的方式有所不同：

* **标准挑战**：客户以任意顺序完成任意指定数量的任务
* **连续挑战**：客户连续多次完成同一任务
* **连续挑战**：客户按定义的顺序完成任务

## 创建任务 {#create-task}

<!-- SCREENSHOT: Two screenshots side by side showing the two entry points: Tasks tab with "Create task" button, and challenge editor with "Add task" button -->

您可以从两个入口点创建任务。 无论从何处开始，配置过程都是相同的。

+++从任务清单

1. 导航到Journey Optimizer中的&#x200B;**[!UICONTROL 忠诚度挑战]**。

1. 选择&#x200B;**[!UICONTROL 任务]**&#x200B;选项卡。

1. 选择&#x200B;**[!UICONTROL 创建任务]**。

从清单中创建的任务将保存并可在多个难题中重复使用。

+++

+++从挑战中

1. 打开现有挑战或创建新挑战。

1. 导航到&#x200B;**[!UICONTROL 任务]**&#x200B;部分。

1. 选择&#x200B;**[!UICONTROL 添加任务]**，然后选择&#x200B;**[!UICONTROL 创建新任务]**。

通过这种方式创建的任务会自动添加到您的挑战中，并保存到Tasks清单中，以供在其他挑战中重复使用。

+++

### 定义任务属性 {#define-task-properties}

<!-- SCREENSHOT: Task properties form showing Task name and Task description fields -->

配置基本任务信息：

* **任务名称**：输入任务的描述性名称。 此名称对您和您的团队可见，但可能不会向客户显示，具体取决于您的内容卡设计。
* **任务描述**： （可选）添加有关任务目的或要求的详细信息。

### 选择客户活动 {#choose-activity}

<!-- SCREENSHOT: Activity type selection showing Purchase and Spend options with radio buttons -->

选择客户完成此任务必须执行的客户活动的类型：

* **[!UICONTROL 购买]**：客户必须购买一个或多个项目才能完成此任务
* **[!UICONTROL 支出]**：客户必须支出指定的金额才能完成此任务

选择最符合您的结果目标的客户活动。 每种活动类型都有特定的可配置属性，以便进一步定义和形成任务需求。

### 定义属性 {#define-attributes}

<!-- SCREENSHOT: Attributes form for Purchase activity showing Quantity field, Eligible items & exclusions field, and parameters icon for optional attributes -->

根据您选择的活动类型配置任务属性：

+++对于购买活动

配置以下属性：

* **数量**：输入完成此任务必须购买的项目数
* **符合条件的项目和排除项**：定义计入任务完成和不计入任务完成的项目或项目组。了解有关[定义合格项目和排除项](#eligible-items-exclusions)的更多信息

**可选属性**（通过参数图标进行配置）：

* **最小支出值金额**：设置最低采购金额要求
* **最大事务数**：限制可用于完成任务的事务数

+++

+++对于支出活动

配置以下属性：

* **金额**：输入完成任务所需的总支出金额
* **最大事务数**：指定允许满足支出要求的事务数。 如果不想限制事务数，可以从参数图标取消激活此属性
* **符合条件的项和排除项**： （可选）定义计入任务完成和不计入任务完成的项或项组。了解有关[定义合格项目和排除项](#eligible-items-exclusions)的更多信息

+++

配置所有属性后，选择&#x200B;**[!UICONTROL 创建]**&#x200B;以保存任务。 任务将保存到Tasks清单中，如果是从挑战中创建的，则会自动添加到该挑战中。

## 定义合格物料和排除项 {#eligible-items-exclusions}

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

对于采购和支出活动，您可以定义合格的物料和组，也可以排除物料和组。 这允许您定位特定的产品、类别或位置，以符合您的挑战目标。

**用例：**

* 创建一项任务，奖励购买咖啡物品的客户，但不包括清仓产品
* 将支出任务限制在特定产品类别中
* 在任务完成时排除礼品卡或促销项目

### 配置符合条件的项目 {#configure-eligible-items}

要定义符合条件的项目，请使用&#x200B;**[!UICONTROL 符合条件的任务购买仅限于以下]**&#x200B;部分：

* 输入特定的物料ID、类别或目标ID，用逗号分隔
* 示例：`SKU001, SKU002, CategoryA, StoreLocation123`
* **提示**：输入`*`使所有购买都符合条件（如果留空，则为默认行为）

### 配置排除项 {#configure-exclusions}

若要从任务中排除项目，请使用&#x200B;**[!UICONTROL 以下项目将从此任务中排除]**&#x200B;部分：

* 输入不应计入任务完成的特定项目ID、类别或目标ID
* 示例：`CLEARANCE01, GIFTCARD, SALE_CATEGORY`
* 常见排除项：销售或清仓商品、礼品卡、促销商品

>[!NOTE]
>
>排除项优先于符合条件的项目。 如果某个项目同时与符合条件的项目和一个排除项匹配，则会将该项目从任务中排除。

## 后续步骤 {#next-steps}

现在您已了解如何创建和配置任务：

* [创建挑战](create-challenges.md) — 了解如何构建完整的挑战并配置奖励
* [管理挑战](manage-challenges.md) — 了解如何编辑、监控和优化挑战
