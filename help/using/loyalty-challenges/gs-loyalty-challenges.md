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
source-git-commit: 7b075996eebd03f0aa812da3ece9cfebef8c65fc
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 3%

---


# 忠诚度挑战入门 {#get-started-loyalty-challenges}

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私有测试版**&#x200B;中，可能在您的环境中不可用。 请联系 Adobe 代表以获取访问权限。

忠诚度挑战让您能够为客户创建个性化的参与优惠，帮助您大规模编排忠诚度计划。 您可以设计具有特定任务和里程碑的挑战，奖励完成任务的客户，并通过Adobe Journey Optimizer渠道提供体验。

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* **忠诚度挑战入门** ◀︎**您在这里** — 快速概述和后续步骤
* [了解忠诚度挑战](get-started.md) — 功能、工作流程、先决条件
* [创建挑战](create-challenges.md) — 生成并配置挑战
* [管理挑战](manage-challenges.md) — 编辑、监视、优化

>[!ENDSHADEBOX]

## 快速概述 {#quick-overview}

使用忠诚度挑战来：

* **创建三种类型的挑战**：标准（任何任务）、条纹（重复任务）或顺序（有序任务）
* **设计挑战内容**：使用内容卡在客户设备上显示挑战
* **设置任务要求**：定义具有奖励的操作，如购买、访问或自定义事件
* **发送多渠道通知**：通过应用程序内、电子邮件和关键阶段的推送传递消息
* **跟踪性能**：通过自动生成的历程和内置报告进行监视

## 工作原理 {#how-it-works-overview}

按照以下工作流程创建忠诚度挑战：

1. **设置数据摄取** — 配置源连接器以跟踪客户操作
2. **创建挑战** — 定义类型、受众和日期
3. **添加任务** — 配置操作和奖励
4. **设计内容** — 创建内容卡和可选的消息传递
5. **发布** - Journey Optimizer自动生成并激活历程
6. **监视器** — 跟踪参与率和性能

>[!NOTE]
>
>自动生成的历程显示在历程清单中，并且可以根据需要进行自定义。 但是，直接对历程所做的更改不会同步回挑战配置。

## 先决条件 {#prerequisites-overview}

在使用忠诚度挑战之前：

* 配置Experience Platform源连接器（例如，毛细管）以摄取忠诚度事件数据
* 确保您在Journey Optimizer中具有适当的权限
* 在Experience Platform中创建目标受众

有关详细的先决条件，请参阅[了解忠诚度挑战](get-started.md#prerequisites)。

## 重要限制 {#limitations-overview}

* **无分类帐系统**：忠诚度挑战不跟踪货币值或点数余额。 Journey Optimizer调用外部忠诚度管理系统来处理点数分配。
* **仅限受众选择**：您可以选择现有受众，但无法从忠诚度挑战UI创建新受众。

## 后续步骤 {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="get-started.md">
    <img alt="了解" src="../assets/do-not-localize/learn-more-button.svg">
    </a>
    <div>
    <a href="get-started.md"><strong>了解忠诚度挑战</strong></a>
    </div>
    <p>
    <em>了解特性、工作流程和功能</em>
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
