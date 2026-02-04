---
solution: Journey Optimizer
product: journey optimizer
title: 忠诚度挑战入门
description: 了解如何在Adobe Journey Optimizer中创建和管理忠诚度挑战，以构建引人入胜的忠诚度计划。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人测试版" type="Informative"
source-git-commit: f41c1ed8a2d9e74b9d8fe97e0bf9e565d326aec6
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 1%

---


# 忠诚度挑战入门 {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* **忠诚度挑战入门** ◀︎**您在这里** — 概述、工作流程、先决条件
* [访问和管理忠诚度挑战](access-loyalty-challenges.md) — 库存、挑战和任务管理
* [创建挑战](create-challenges.md) — 生成并配置挑战
* [创建任务](create-tasks.md) — 定义挑战任务

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

## 工作原理 {#how-it-works}

按照以下工作流程创建和启动忠诚度挑战：

1. **设置数据摄取** — 配置Experience Platform源连接器（如毛细连接器）以摄取跟踪客户操作和进度的忠诚度事件数据。 此数据支持挑战跟踪和任务完成。

1. **选择目标受众** — 通过从Adobe Experience Platform中选择受众，定义哪些客户可以参与您的挑战。

1. **创建挑战** — 定义基本挑战属性，包括名称、类型（标准、条纹或顺序）和日期范围。

1. **添加任务** — 定义客户必须完成的特定操作，包括任务类型（购买、支出、访问、参与、自定义事件）、数量、产品过滤器和奖励。

1. **设计内容卡** — 使用客户设备上显示的Journey Optimizer内容卡创建挑战的可视化表示形式。 内容卡显示挑战信息、进度和奖励。

1. **配置消息**（可选） — 为关键生命周期阶段（启动、进行中和完成）设置多渠道消息（应用程序内、电子邮件、推送）。

1. **发布历程** - Journey Optimizer会自动为您遇到的挑战生成历程。 导航到历程清单并发布自动生成的历程，以便客户能够看到难题。

有关详细的分步说明，请参阅[创建挑战](create-challenges.md)。

## 先决条件 {#prerequisites}

在使用忠诚度挑战之前，请确保您具有：

+++数据摄取设置

忠诚度挑战依赖于通过Experience Platform源连接器摄取的数据来跟踪客户进度和任务完成。

1. **配置支持的源连接器**：目前，毛细管连接器通常可用。 计划在未来版本中使用其他连接器。

1. **验证数据摄取**：确保忠诚度事件和客户数据流入Experience Platform并在Journey Optimizer中可用。 验证数据架构包含用于跟踪客户操作和进度的必要字段。

有关详细说明，请参阅：

* [Experience Platform源文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/home)
* [在Journey Optimizer中配置源连接器](../start/get-started-sources.md)

+++

+++所需的权限

要使用“忠诚度挑战”，您需要在Journey Optimizer中拥有适当的权限。 所需的权限包括：

* 访问&#x200B;**[!UICONTROL 忠诚度挑战(Beta)]**&#x200B;功能
* 创建和管理历程的权限
* 创建和管理内容卡的权限
* 创建和管理受众权限

如果您无法访问此功能或需要其他权限，请与您的管理员联系。

+++

+++目标受众

定义一个目标受众，指定哪些客户有资格参与您的忠诚度挑战。 您可以选择现有受众，也可以直接从挑战创建界面中创建新受众。 [了解如何使用受众](../audience/about-audiences.md)。

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
