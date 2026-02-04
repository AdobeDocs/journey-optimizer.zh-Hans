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
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---


# 忠诚度挑战入门 {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* **忠诚度挑战入门** ◀︎**您在这里** — 概述、工作流程、先决条件
* [访问忠诚度挑战](access-loyalty-challenges.md) — 清点和筛选
* [创建挑战](create-challenges.md) — 生成并配置挑战
* [创建任务](create-tasks.md) — 定义挑战任务
* [管理挑战](manage-challenges.md) — 编辑、监视、优化

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私有测试版**&#x200B;中，可能在您的环境中不可用。 要请求获取访问权限，请联系您的Adobe代表。 了解有关[可用性标签](../rn/releases.md#availability-labels)的更多信息。

## 概述 {#overview}

“忠诚度挑战”为大规模创建忠诚度计划提供了一个完整的解决方案，范围从定义任务和里程碑到跨渠道交付内容和跟踪绩效。

您可以创建三种类型的挑战体验：

* **标准挑战**：客户以任意顺序完成任意指定数量的任务
* **连续挑战**：客户连续多次完成同一任务
* **连续挑战**：客户按定义的顺序完成任务

借助“忠诚度挑战”，您可以配置奖励、在关键生命周期阶段发送多渠道通知以及通过自动生成的历程监控绩效 — 同时保持与外部忠诚度管理系统的集成。

<!-- SCREENSHOT: High-level diagram showing Loyalty Challenges architecture with: Data ingestion from source connectors -> Challenge creation in JO -> Content cards & messaging -> Customer device -> Journey tracking -->

## 工作原理 {#how-it-works}

<!-- SCHEMA: Visual workflow diagram showing the 8 steps in the loyalty challenge creation process with icons for each step -->

按照以下工作流程创建和启动忠诚度挑战：

1. **设置数据摄取** — 配置Experience Platform源连接器（如毛细连接器）以摄取跟踪客户操作和进度的忠诚度事件数据。 此数据支持挑战跟踪和任务完成。

1. **创建挑战** — 定义基本挑战属性，包括名称、类型（标准、条纹或顺序）、受众和日期范围。 有关详细步骤，请参阅[创建挑战](create-challenges.md)。

1. **添加任务** — 定义客户必须完成的特定操作，包括任务类型（购买、支出、访问、参与、自定义事件）、数量、产品过滤器和奖励。 有关详细说明，请参阅[创建任务](create-tasks.md)。

1. **设计内容卡** — 使用客户设备上显示的Journey Optimizer [内容卡](../content-card/get-started-content-card.md)创建挑战的可视化表示形式。 内容卡显示挑战信息、进度和奖励。

1. **配置消息传送**（可选） — 为关键生命周期阶段（启动、进行中和完成）设置多渠道消息（[应用程序内](../in-app/get-started-in-app.md)、[电子邮件](../email/get-started-email.md)、[推送](../push/get-started-push.md)）。

1. **审核并发布** — 使用[测试用户档案](../test-approve/test-profiles.md)测试您的挑战，然后发布该挑战以将其提供给您的目标受众。

1. **激活历程** — 当您发布挑战时，Journey Optimizer会自动创建处于草稿状态的[历程](../building-journeys/journey-gs.md)，以协调内容卡交付和消息传送。 导航到历程清单，找到自动生成的历程（名为“挑战： [挑战名称]”），然后[激活它](../building-journeys/publishing-the-journey.md)，以使您的客户能够查看挑战。

1. **监控绩效** — 通过内置报告和历程画布跟踪参与率、完成率、奖励分发和消息参与。 有关监控详细信息，请参阅[管理挑战](manage-challenges.md)。

## 先决条件 {#prerequisites}

在使用忠诚度挑战之前，请确保您具有：

+++数据摄取设置

忠诚度挑战依赖于通过Experience Platform源连接器摄取的数据来跟踪客户进度和任务完成。

1. **配置支持的源连接器**：目前，毛细管连接器通常可用。 计划在未来版本中使用其他连接器。

1. **验证数据摄取**：确保忠诚度事件和客户数据流入Experience Platform并在Journey Optimizer中可用。 验证数据架构包含用于跟踪客户操作和进度的必要字段。

有关详细说明，请参阅：

* [Experience Platform源文档](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home)
* [在Journey Optimizer中配置源连接器](../start/get-started-sources.md)

+++

+++所需的权限

要使用“忠诚度挑战”，您需要在Journey Optimizer中拥有适当的权限。 所需的权限包括：

* 访问&#x200B;**[!UICONTROL 忠诚度挑战]**&#x200B;功能
* 创建和管理历程的权限
* 创建和管理内容卡的权限
* 创建和管理受众权限

如果您无法访问此功能或需要其他权限，请与您的管理员联系。

+++

+++目标受众

在创建挑战之前，请在Experience Platform中创建目标受众。 这些受众定义哪些客户有资格参与您的忠诚度挑战。 有关如何创建受众的详细信息，请参阅[受众入门](../audience/about-audiences.md)。

+++

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
    </p>
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
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
    <!--<img alt="Tasks" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-tasks.md"><strong>创建任务</strong></a>
    </div>
    <p>
    <em>为挑战定义操作和奖励</em>
    </p>
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
    </p>
  </td>
</tr>
</table>
