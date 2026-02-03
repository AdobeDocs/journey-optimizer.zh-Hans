---
solution: Journey Optimizer
product: journey optimizer
title: 了解忠诚度挑战
description: 了解Adobe Journey Optimizer中的忠诚度挑战特性、工作流程和功能。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人测试版" type="Informative"
source-git-commit: 419c7b3913ca4da50c69ed36ffc1a8c8520607b4
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 2%

---


# 了解忠诚度挑战 {#understand-loyalty-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="关于忠诚度挑战"
>abstract="忠诚度挑战让您能够创建个性化的参与优惠，以激励客户完成特定操作并获得奖励。"

忠诚度挑战让您能够设计和部署个性化的参与优惠，以激励客户完成特定操作并获得奖励。

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](gs-loyalty-challenges.md) — 快速概述和后续步骤
* **了解忠诚度挑战** ◀︎**您在这里** — 功能、工作流程、先决条件
* [创建挑战](create-challenges.md) — 生成并配置挑战
* [管理挑战](manage-challenges.md) — 编辑、监视、优化

>[!ENDSHADEBOX]

## 概述 {#overview}

“忠诚度挑战”为大规模创建忠诚度计划提供了一个完整的解决方案，范围从定义任务和里程碑到跨渠道交付内容和跟踪绩效。 您可以创建三种类型的挑战体验，配置奖励，在关键生命周期阶段发送多渠道通知，并通过自动生成的历程监控绩效，同时保持与外部忠诚度管理系统的集成。

## 工作原理 {#how-it-works}

按照以下工作流程创建和启动忠诚度挑战：

1. **设置数据摄取** — 配置Experience Platform源连接器（如Chariceline）以摄取跟踪客户操作和进度的忠诚度事件数据。

2. **创建挑战** — 定义基本挑战属性，包括名称、类型（标准、条纹或顺序）、受众和日期范围。

3. **添加任务** — 定义客户必须完成的特定操作，包括任务类型（购买、支出、访问等）、数量、产品过滤器和奖励。

4. **设计内容卡** — 使用客户设备上显示的Journey Optimizer内容卡创建挑战的可视化表示形式。

5. **配置消息**（可选） — 为关键阶段（启动、进行中和完成）设置多渠道消息（应用程序内、电子邮件、推送）。

6. **审核并发布** — 使用测试配置文件测试您的挑战，然后发布该挑战以供您的目标受众使用。

7. **自动生成的历程** — 发布时，Journey Optimizer会自动创建一个历程，以协调内容卡交付和消息传递。

8. **激活历程** — 自动生成的历程将在您的挑战开始日期激活，并管理所有客户交互。

9. **监控绩效** — 通过内置报告和历程画布跟踪参与率、完成率、奖励分发和消息参与。

>[!NOTE]
>
>自动生成的历程显示在历程清单中，并且可以根据需要进行自定义。 但是，直接对历程所做的更改不会同步回挑战配置。

## 主要功能 {#key-capabilities}

使用忠诚度挑战来：

* **创建三种类型的挑战**：
   * **Standard**：客户完成任意数量的任务即可获得奖励。
   * **条纹**：客户多次完成同一任务。
   * **顺序**：客户按特定顺序完成任务。

* **设计挑战内容**：使用Journey Optimizer内容卡创建客户设备上挑战的可视化呈现形式。 内容卡在客户设备上显示挑战信息、进度和奖励。

* **设置任务要求**：定义客户必须执行哪些操作才能获得奖励，包括：
   * 任务类型（购买、支出金额、访问等）
   * 数量要求
   * 使用SKU的产品包含/排除项
   * 自定义属性和条件

* **配置奖励**：定义客户在完成任务或完成整个挑战后获得的奖励

* **发送通知**：在关键阶段跨多个渠道（应用程序内、电子邮件、推送）投放消息：
   * **启动项**：挑战开始时
   * **正在进行**：客户正在处理时
   * **完成**：客户完成挑战时

* **跟踪性能**：监视自动生成的历程并审查质询性能

### 重要限制 {#limitations}

* **无分类帐系统**：忠诚度挑战不跟踪货币值或点数余额。 当客户完成挑战并获得奖励时，Journey Optimizer会调用您的外部忠诚度管理系统来处理积分分配。

* **仅限受众选择**：您可以选择现有受众，但无法从忠诚度挑战UI创建新受众。

## 先决条件 {#prerequisites}

在使用忠诚度挑战之前，请确保您具有：

### 数据摄取设置 {#data-ingestion}

忠诚度挑战依赖于通过Experience Platform源连接器摄取的数据来跟踪客户进度和任务完成。

1. **配置支持的源连接器**：目前，毛细管连接器通常可用。 已计划添加其他连接器。

2. **验证数据摄取**：确保忠诚度事件和客户数据流入Experience Platform并在Journey Optimizer中可用。

有关详细说明，请参阅：

* [Experience Platform源文档](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [在Journey Optimizer中配置源连接器](../start/get-started-sources.md)

### 所需的权限 {#required-permissions}

要使用“忠诚度挑战”，您需要在Journey Optimizer中拥有适当的权限。 如果无法访问该功能，请与管理员联系。

## 访问忠诚度挑战 {#access}

要了解忠诚度挑战，请执行以下操作：

1. 在Adobe Journey Optimizer的左侧导航菜单中选择&#x200B;**[!UICONTROL 忠诚度挑战]**。

2. “忠诚度挑战”清单显示了所有现有挑战，并提供了如下信息：
   * 质询名称和描述
   * 状态（草稿、实时、已停止等）
   * 挑战类型（标准、条纹、顺序）
   * 开始和结束日期
   * 上次修改日期

3. 选择&#x200B;**[!UICONTROL 创建质询]**&#x200B;以开始创建新质询。

### 搜索和过滤挑战 {#search-filter}

使用搜索和筛选功能快速查找特定难题：

* **搜索**：在搜索字段中输入质询名称或关键字
* **按状态筛选**：草稿、已计划、实时、已完成、已停止或已存档
* **按类型筛选**：标准、连续或顺序挑战
* **按日期过滤**：特定日期范围内的挑战
* **按标记过滤**：应用了特定标记的挑战

## 后续步骤 {#next-steps}

现在您已经了解了忠诚度挑战，了解如何创建您的第一个挑战：

* [创建挑战](create-challenges.md)
* [管理挑战](manage-challenges.md)
