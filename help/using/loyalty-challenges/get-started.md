---
solution: Journey Optimizer
product: journey optimizer
title: 忠诚度挑战入门
description: 了解如何在Adobe Journey Optimizer中创建和管理忠诚度挑战，以创建吸引人的忠诚度计划。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人测试版" type="Informative"
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%

---


# 忠诚度挑战入门 {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* **忠诚度挑战入门** ◀︎**您在这里** — 概述、工作流程、先决条件
* [访问忠诚度挑战](access-loyalty-challenges.md) — 清点和筛选
* [创建挑战](create-challenges.md) — 生成并配置挑战
* [管理挑战](manage-challenges.md) — 编辑、监视、优化

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_challenges_overview"
>title="关于忠诚度挑战"
>abstract="忠诚度挑战让您能够创建个性化的参与优惠，以激励客户完成特定操作并获得奖励。"

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私有测试版**&#x200B;中，可能在您的环境中不可用。 请联系 Adobe 代表以获取访问权限。

## 概述 {#overview}

“忠诚度挑战”为大规模创建忠诚度计划提供了一个完整的解决方案，范围从定义任务和里程碑到跨渠道交付内容和跟踪绩效。 您可以创建三种类型的挑战体验，配置奖励，在关键生命周期阶段发送多渠道通知，并通过自动生成的历程监控绩效，同时保持与外部忠诚度管理系统的集成。

## 主要功能 {#key-capabilities}

使用忠诚度挑战来：

* **创建三种类型的挑战**：
   * **Standard**：客户以任何顺序完成任意数量的任务以获取奖励
   * **条纹**：客户连续多次完成同一任务
   * **顺序**：客户按特定顺序完成任务

* **设计挑战内容**：使用Journey Optimizer内容卡创建客户设备上挑战的可视化呈现形式。 内容卡显示挑战信息、进度和奖励。

* **设置任务要求**：定义客户必须执行哪些操作才能获得奖励，包括：
   * 任务类型（购买、支出金额、访问、参与度、自定义事件）
   * 数量要求
   * 使用SKU、类别或属性的产品包含/排除项
   * 自定义属性和条件

* **配置奖励**：定义客户在完成任务时（渐进式奖励）或完成整个挑战（最终奖励）后获得的奖励。

* **发送多渠道通知**：在关键阶段跨多个渠道（应用程序内、电子邮件、推送）投放消息：
   * **启动项**：挑战开始时
   * **正在进行**：客户正在处理时
   * **完成**：客户完成挑战时

* **跟踪性能**：监视自动生成的历程并通过内置报告审查质询性能。

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

### 目标受众 {#target-audiences}

在创建挑战之前，请在Experience Platform中创建目标受众。 您可以选择现有受众，但无法从忠诚度挑战UI创建新受众。

## 重要限制 {#limitations}

* **无分类帐系统**：忠诚度挑战不跟踪货币值或点数余额。 当客户完成挑战并获得奖励时，Journey Optimizer会调用您的外部忠诚度管理系统来处理积分分配。

* **仅限受众选择**：您可以选择现有受众，但无法从忠诚度挑战UI创建新受众。

## 后续步骤 {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>访问忠诚度挑战</strong></a>
    </div>
    <p>
    <em>了解如何访问清单和筛选挑战</em>
    <p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>创建挑战</strong></a>
    </div>
    <p>
    <em>生成并配置您的第一个忠诚度挑战</em>
    <p>
  </td>
  <td>
    <a href="manage-challenges.md">
    <!--<img alt="Manage" src="../assets/do-not-localize/monitor-button.svg">-->
    </a>
    <div>
    <a href="manage-challenges.md"><strong>管理挑战</strong></a>
    </div>
    <p>
    <em>编辑、监控和优化挑战</em>
    <p>
  </td>
</tr>
</table>
