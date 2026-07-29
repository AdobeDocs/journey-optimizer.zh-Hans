---
solution: Journey Optimizer
product: journey optimizer
title: 忠诚度挑战入门
description: 了解如何在Adobe Journey Optimizer中创建和管理忠诚度挑战，以构建引人入胜的奖励忠诚度计划。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
feature_v2: []
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 82fd2e225b54a2c47081303b230ab66fc2149022
workflow-type: tm+mt
source-wordcount: 964
ht-degree: 13%

---

# 开始应对忠诚度挑战 {#get-started-loyalty-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_inventory"
>title="忠诚度挑战"
>abstract="通过忠诚度挑战您可以创建极具吸引力的游戏化的忠诚度计划，以推动客户行为，深化品牌关系。 构建奖励客户特定行为的挑战——从购买和写评论，到参与社交媒体和引荐好友。"

>[!AVAILABILITY]
>
>Journey Optimizer忠诚度目前不适用于Healthcare Shield和Privacy and Security Shield客户。 Healthcare Shield和Privacy and Security Shield客户的可用性将在未来功能准备就绪时更新。

## 概述 {#overview}

通过忠诚度挑战您可以创建极具吸引力的游戏化的忠诚度计划，以推动客户行为，深化品牌关系。 构建奖励客户特定行为的挑战——从购买和写评论，到参与社交媒体和引荐好友。

通过忠诚度挑战，您可以：

* **设计灵活的挑战类型**：创建符合业务目标的标准、连续或连续挑战
* **策略性地配置奖励**：在任务里程碑或完全完成时提供点数以保持参与
* **个性化体验**：使用内容卡和多渠道消息传递创建沉浸式品牌体验
* **无缝集成**：与现有的忠诚度提供商联系并利用Experience Platform数据
* **自动跟踪**：通过自动生成的历程（无需自定义开发）监控客户进度
* **衡量绩效**：使用内置的报告功能板跟踪项目KPI、挑战结果和任务级指标

![](assets/challenges-gs.png)

您可以创建以下类型的挑战体验：

* **标准挑战**：客户以任意顺序完成任意指定数量的任务。 如果您希望灵活地选择完成路径并使用多个路径，请使用此类型。\
  *示例：“夏季健康挑战” — 完成5项任务中的3项：购买健康产品、在社交媒体上分享、推荐朋友、撰写评论或参加虚拟活动*

* **连续挑战**：客户连续多次完成同一任务。 使用此类型鼓励随着时间的推移出现一致、重复的行为。\
  *示例：“咖啡爱好者周” — 连续7天购买咖啡产品以解锁免费饮品奖励*

* **连续挑战**：客户按定义的顺序完成任务。 使用此类型引导客户完成特定历程或载入流程。\
  *示例：“新成员历程” — 注册电子邮件→进行首次购买→撰写产品评论→推荐朋友（按此确切顺序完成）*

* **提出您自己的数据挑战**（可用性受限）：挑战框架（任务和奖励）是从您的“忠诚度挑战”数据集成中组合而成的。 您可以像配置任何其他挑战类型一样配置“设置”、“内容”和“消息”。

>[!TIP]
>您还可以使用[CX同事历程技能](../start/ajo-coworker-skills.md#loyalty-challenge-management)中的&#x200B;**忠诚度挑战管理**&#x200B;创建和管理忠诚度挑战，并使用自然语言提示更快地创建挑战。

➡️ [观看功能概述](#video)

## 工作原理 {#how-it-works}

忠诚度挑战的使用涉及三个广泛的阶段 — 设置、执行和衡量 — 通常在管理员和从业者角色之间共享。

**1. 设置您的程序** *（管理员）*

在提出挑战之前，管理员配置计划基础：奖励提供者、将客户操作映射到任务完成的事件定义、产品清单和排除列表。 [了解如何配置忠诚度挑战](loyalty-admin.md)。

**2. 作者和启动挑战** *（从业者）*

营销人员通过选择类型（标准、条纹、顺序或自带数据）、配置设置（受众、计划、规则）以及定义任务和奖励来创建挑战。 他们可以选择使用&#x200B;**内容卡**&#x200B;或&#x200B;**基于代码的体验**&#x200B;在面向成员的界面上显示质询，并为质询生命周期中的关键时刻设置渠道通知。 配置完毕后，他们发布挑战，生成自动构建的历程，然后发布该历程以让挑战生效。 [了解如何创建挑战](create-challenges.md)。

**3. 监视性能** *（从业者/分析师）*

挑战提出后，内置的报告功能板将提供挑战级别的量度：受众funnel表现、任务完成率、奖励发放和收入影响。 AI支持的分析引擎还会提供上下文建议，以帮助优化程序性能。 [了解忠诚度报告](loyalty-reporting.md)。

## 先决条件 {#prerequisites}

在使用忠诚度挑战之前，请确保您具有：

+++所需的权限

要使用“忠诚度挑战”，您必须分配到“忠诚度”角色。 在Prod沙盒中，管理员、从业人员和分析人员可以使用默认角色。 对于非生产沙盒，您的管理员必须创建一个具有所需忠诚度权限的自定义角色。

如果您无法访问此功能或需要其他权限，请与您的管理员联系。 [了解如何配置忠诚度挑战权限](loyalty-permissions.md)。

+++

+++配置忠诚度计划（管理员）

管理员在&#x200B;**[!UICONTROL 忠诚度配置]**&#x200B;菜单中配置奖励提供者、事件定义、产品清单、排除项和全局设置。 仅创建挑战的营销人员不需要访问此菜单。 [了解如何配置忠诚度挑战](loyalty-admin.md)

如果在左侧导航中看不到&#x200B;**[!UICONTROL 忠诚度配置]**&#x200B;菜单，请联系您的管理员。

+++

+++目标受众

在创建挑战之前，请确保所需的目标受众存在于Adobe Experience Platform中。 在挑战配置过程中，您将选择受众，该受众定义哪些客户有资格参与。 [了解如何使用受众](../audience/about-audiences.md)。

+++

## 让我们深入探究 {#lets-dive-deeper}

现在您已经了解了忠诚度挑战及其工作方式，接下来该深入了解详细信息。 浏览以下主题以访问该界面，创建您的第一个挑战，并定义您的客户将完成的任务。

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
      <img alt="访问" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>访问并管理挑战和任务</strong></a>
    </div>
    <p>
    <em>了解如何访问清单并管理挑战和任务</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="创建" src="assets/do-not-localize/icon-challenge.png" width="200"/>
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
      <img alt="任务" src="assets/do-not-localize/icon-task.png" width="200"/>
    </a>
    <div>
    <a href="create-tasks.md"><strong>创建任务</strong></a>
    </div>
    <p>
    <em>了解如何定义客户为应对挑战而完成的任务</em>
    </p>
  </td>
  <td>
    <a href="loyalty-reporting.md">
      <img alt="报告" src="assets/do-not-localize/icon-reporting.png" width="200"/>
    </a>
    <div>
    <a href="loyalty-reporting.md"><strong>监控性能</strong></a>
    </div>
    <p>
    <em>使用内置功能板跟踪计划KPI、挑战结果和任务量度</em>
    </p>
  </td>
  <!--
    <a href="loyalty-admin.md"><strong>Configure the loyalty program</strong></a>
  <td>
    <a href="loyalty-admin.md">
    <em>Set up reward providers, event definitions, and org settings for fulfillment</em>
    </a>
    <div>
-->
    <a href="loyalty-admin.md"><strong>配置忠诚度挑战</strong></a>
    </div>
    <p>
    <em>设置奖励提供者、事件定义和组织设置</em>
    </p>
  </td>
</tr>
</table>

## API 参考 {#api-reference}

若要以编程方式管理忠诚度挑战，请使用[忠诚度挑战API](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}。 该API允许您通过REST端点创建、更新和管理挑战和任务。

## 操作方法视频 {#video}

**刚开始应对忠诚度挑战？** 观看此概述，了解功能和优势：

>[!VIDEO](https://video.tv.adobe.com/v/3496441?quality=12)

