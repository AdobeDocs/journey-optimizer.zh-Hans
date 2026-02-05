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
mini-toc-levels: 2
source-git-commit: f50cc244f6d5ec8b38844e8240e72502ddfe3ae0
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 1%

---


# 忠诚度挑战入门 {#get-started-loyalty-challenges}

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私有测试版**&#x200B;中，可能在您的环境中不可用。 要请求获取访问权限，请联系您的Adobe代表。 了解有关[可用性标签](../rn/releases.md#availability-labels)的更多信息。

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* **忠诚度挑战入门** ◀︎**您在这里** — 概述、工作流程、先决条件
* [访问和管理挑战和任务](access-loyalty-challenges.md) — 清点、挑战和任务管理
* [创建挑战](create-challenges.md) — 生成并配置挑战
* [创建任务](create-tasks.md) — 定义挑战任务

>[!ENDSHADEBOX]

## 概述 {#overview}

忠诚度挑战使您能够创建引人入胜的游戏化忠诚度计划，以推动客户行为并深化品牌关系。 构建奖励客户特定行为的挑战 — 从购买和撰写评论到参与社交媒体和反向链接好友。

通过忠诚度挑战，您可以：

* **设计灵活的挑战类型**：创建符合业务目标的标准、连续或连续挑战
* **策略性地配置奖励**：在任务里程碑或完全完成时提供点数以保持参与
* **个性化体验**：使用内容卡和多渠道消息传递创建沉浸式品牌体验
* **无缝集成**：与现有的忠诚度提供商联系并利用Experience Platform数据
* **自动跟踪**：通过自动生成的历程（无需自定义开发）监控客户进度

![](assets/challenges-gs.png)

您可以创建三种类型的挑战体验：

* **标准挑战**：客户以任意顺序完成任意指定数量的任务。 如果您希望灵活地选择完成路径并使用多个路径，请使用此类型。\
  *示例：“夏季健康挑战” — 完成5项任务中的3项：购买健康产品、在社交媒体上分享、推荐朋友、撰写评论或参加虚拟活动*

* **连续挑战**：客户连续多次完成同一任务。 使用此类型鼓励随着时间的推移出现一致、重复的行为。\
  *示例：“咖啡爱好者周” — 连续7天购买咖啡产品以解锁免费饮品奖励*

* **连续挑战**：客户按定义的顺序完成任务。 使用此类型引导客户完成特定历程或载入流程。\
  *示例：“新成员历程” — 注册电子邮件→进行首次购买→撰写产品评论→推荐朋友（按此确切顺序完成）*

## 工作原理 {#how-it-works}

按照以下工作流程创建和启动忠诚度挑战：

1. **设置数据摄取** — 配置Experience Platform源连接器（如[毛细连接器](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/home#loyalty)）以摄取跟踪客户操作和进度的忠诚度事件数据。 此数据支持挑战跟踪和任务完成。

1. **创建挑战** — 定义基本挑战属性，包括名称、类型（标准、条纹或顺序）和日期范围。

1. **添加任务** — 定义客户必须完成的特定操作，包括任务类型（购买、支出）、数量、产品过滤器和奖励。

1. **设计内容卡** — 使用客户设备上显示的Journey Optimizer内容卡创建挑战的可视化表示形式。 内容卡显示挑战信息、进度和奖励。

1. **配置消息**（可选） — 为关键生命周期阶段（启动、进行中和完成）设置多渠道消息（应用程序内、电子邮件、推送）。

1. **选择目标受众** — 通过从Adobe Experience Platform中选择受众，定义哪些客户可以参与您的挑战。

1. **发布历程** - Journey Optimizer会自动为您遇到的挑战生成历程。 导航到历程清单并发布自动生成的历程，以便客户能够看到难题。

有关详细的分步说明，请参阅[创建挑战](create-challenges.md)。

## 先决条件 {#prerequisites}

在使用忠诚度挑战之前，请确保您具有：

+++数据摄取设置

忠诚度挑战依赖于通过Experience Platform源连接器摄取的数据来跟踪客户进度和任务完成。

在启动之前，请配置支持的源连接器。 目前，毛细管连接器可用。 计划在未来版本中使用其他连接器。 [了解忠诚度源连接器](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/sources/home#loyalty)。

+++

<!--+++Required permissions

To use Loyalty Challenges, you need appropriate permissions in Journey Optimizer. Required permissions include:

TBD

Contact your administrator if you cannot access the feature or need additional permissions.

+++-->

+++目标受众

在创建挑战之前，请确保所需的目标受众存在于Adobe Experience Platform中。 在挑战配置过程中，您将选择受众，该受众定义哪些客户有资格参与。 [了解如何使用受众](../audience/about-audiences.md)。

+++

## 后续步骤 {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>访问和管理挑战和任务</strong></a>
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
    <em>了解如何生成和配置您的第一个忠诚度挑战</em>
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
    <em>了解如何配置客户为应对挑战而完成的操作</em>
    </p>
  </td>
</tr>
</table>
