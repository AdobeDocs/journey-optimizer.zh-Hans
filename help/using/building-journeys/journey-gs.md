---
solution: Journey Optimizer
product: journey optimizer
title: 创建您的第一个历程
description: 使用 [!DNL Adobe Journey Optimizer]构建您的第一个历程的关键步骤
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 历程，第一，开始，快速入门，受众，事件，操作
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/7zNDOi2SUTyttgR6I1iOYQb61ejxpqLYznweU8alnPw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
  - id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 1481
ht-degree: 13%

---

# 创建您的第一个历程 {#jo-quick-start}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解在Adobe Journey Optimizer中构建第一个历程的关键步骤，从定义登录受众或事件，到添加操作并将其实时发布。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="创建历程"
>abstract="**[!DNL Adobe Journey Optimizer]** 利用存储在事件或数据源中的上下文数据构建实时编排用例。"

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="历程"
>abstract="客户历程可提供个性化且符合上下文的体验。 通过 Journey Optimizer，可用存储在事件或数据源中的上下文数据构建实时编排用例。 **概述**&#x200B;选项卡显示一个仪表板，其中包含与您的历程相关的关键量度。 **浏览**&#x200B;选项卡显示现有历程的列表。"

[!DNL Adobe Journey Optimizer]包括全渠道编排画布，允许营销人员协调营销外联与一对一客户参与。 利用用户界面，可轻松地将活动从面板拖放到画布中以构建历程。 此历程用户界面在[此页面](journey-ui.md)中有详细介绍。

![历程画布示例](assets/journey38.png)

此页面上详细描述了创建历程的主要步骤。 其简化如下：

![历程创建步骤：创建、设计、测试和发布](assets/journey-creation-process.png)

在本指南中，您将执行以下操作：

* 定义历程入口点 — 受众区段或实时事件
* 跨渠道添加消息操作 — 电子邮件、推送、短信、应用程序内、Web、基于代码的体验、内容卡等。 [查看支持的渠道](journey-action.md)
* 在激活之前使用测试用户档案测试您的历程
* 发布您的历程并监控其性能

构建多步骤客户历程，实时启动跨渠道交互、优惠和消息序列。 此方法确保客户根据其行为和相关业务信号在最佳时刻参与。

<!--
>[!TIP]
>
>Not sure whether to use a journey or a campaign? [Learn how to choose the right approach](../start/journeys-vs-campaigns.md).
-->

## 开始之前 {#prerequisites}

构建之前需要配置的内容取决于历程的触发方式。 大多数历程都从以下两个入口点之一开始：

* **基于受众的条目** — 历程在计划时间针对定义的一组配置文件运行。 在构建历程之前，在Adobe Experience Platform中[创建受众](../audience/about-audiences.md)。 如果您不熟悉Journey Optimizer，那么建议您从这里开始。

* **基于事件的条目** — 当个人执行操作（如购买或注册）时，将实时触发历程。 [配置事件](../event/about-events.md)以定义触发器及其携带的数据。

**不确定要使用哪个入口点？** 下表将最常见的用例映射到正确的开始活动。

| 入口点 | 使用时间…… | 配置文件输入 |
|---|---|---|
| **[读取受众](read-audience.md)** | 您希望向一组已定义的配置文件（新闻稿、促销活动、入门培训系列）发送计划或定期消息。 | 一次或按计划从批量受众获取所有用户档案。 |
| **[受众资格](audience-qualification-events.md)** | 当用户档案进入或退出受众时，您需要实时做出反应（忠诚度级别升级、流失风险标记）。 | 一次一个配置文件，只要他们在流受众中符合条件。 |
| **单一事件** | 配置文件操作会触发即时响应（购买确认、表单提交、应用程序登录）。 | 一次一个配置文件，实时。 |
| **[商业活动](../event/about-creating-business.md)** | 一个非用户档案事件会同时影响多个人员（航班取消、库存补充、突发新闻警报）。 | 通过自动读取受众步骤，查看与事件关联的所有用户档案。 |

以下元素是可选的，但根据用例的不同，这些元素可能是必需的：

* **数据源** — 要使用来自外部系统的数据扩充历程条件或个性化，请设置[数据源](../datasource/about-data-sources.md)。

* **自定义操作** — 如果您通过第三方系统而不是内置渠道传递消息，请配置[自定义操作](../action/action.md)。

>[!NOTE]
>
>* 如果您是负责技术设置（事件、数据源和操作）的数据工程师，请参阅[此部分](../configuration/about-data-sources-events-actions.md)。
>
>* 在[此页面](../start/guardrails.md)上详细介绍了历程护栏和限制。

## 创建历程 {#jo-build}

要创建多步历程，请执行以下步骤：

1. 在“历程管理”菜单部分中，单击&#x200B;**[!UICONTROL 历程]**。

1. 单击&#x200B;**[!UICONTROL 创建历程]**&#x200B;按钮以创建新旅程。

1. 编辑历程的配置窗格以定义历程的名称并设置其属性。 了解如何在[此页面](journey-properties.md)上设置历程的属性。

   >[!TIP]
   >
   >**我应该选择哪种历程类型？** 如果您是Journey Optimizer的新用户，请使用&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动从基于受众的历程开始 — 它不需要预先配置事件，并且是熟悉画布的最简单方法。 对于事件触发的实时体验（例如，对购买或表单提交作出反应），首先配置事件并使用基于事件的条目。 准备好更深入了吗？ [发现所有历程类型及其进入规则](entry-management.md#types-of-journeys)。

   ![具有设置和配置选项的历程属性面板](assets/jo-properties.png)

然后，您可以开始设计历程。

## 设计旅程 {#jo-design}

历程设计器允许您使用直观的拖放界面构建多步历程。 左侧面板中的活动分为三类： **事件**、**编排**&#x200B;和&#x200B;**操作**。 有关画布及其控件的完整概述，请参阅[此页面](using-the-journey-designer.md)。

![带有活动面板和画布的历程设计器界面](assets/journey38.png)

请按照以下步骤设计您的旅程：

1. **添加入口点** — 将事件或&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动从调色板拖动到画布上。 此属性定义用户档案如何进入历程：实时单独（基于事件）或一次性从定义的受众（基于受众）进入所有历程。

   ![读取用于选择目标受众的受众活动配置](assets/read-segment.png)

1. **添加消息操作** — 从调色板的&#x200B;**[!UICONTROL 操作]**&#x200B;部分，将渠道操作拖动到画布上，以将消息发送到流经历程的用户档案。 操作适用于电子邮件、推送通知、短信等。

1. **添加编排活动** — 使用&#x200B;**[!UICONTROL 条件]**&#x200B;活动根据用户档案属性或行为将历程分支为多个路径。 使用&#x200B;**[!UICONTROL 等待]**&#x200B;活动在步骤之间引入时间延迟。

>[!TIP]
>
>对于具有多个阶段或多个接触点的历程，请考虑将端到端流中断为与&#x200B;**[!UICONTROL 跳转]**&#x200B;活动连接的较小子历程。 这降低了复杂性，并使每个子历程更容易独立测试。 在[设计策略：小型子历程](jump.md#jump-strategy)中了解更多信息。

## 测试历程 {#jo-test}

构建历程后，请在发布之前对其进行测试。 Journey Optimizer提供了&#x200B;**测试模式**，以便在测试配置文件在历程中移动时查看它们，并在激活之前检测潜在的错误。 运行快速测试可确保历程正确运行，以便您能够放心地发布它们。 在本节[&#128279;](testing-the-journey.md)中了解如何测试您的历程

您还可以在&#x200B;**练习**&#x200B;中执行您的历程。 历程试运行是 Adobe Journey Optimizer 中的一种特殊历程发布模式，使历程设计人员能够在不接触真实客户或更新轮廓信息的前提下，使用真实生产数据对历程进行测试。 此功能有助于历程设计人员在正式发布前验证历程设计和受众定位，从而增强信心。 在本节[&#128279;](journey-dry-run.md)中了解如何在练习模式下发布历程。

## 发布历程 {#jo-pub}

您必须发布历程以激活它，并使其可供新配置文件进入该历程。 在发布历程之前，请验证其是否有效并且没有错误。 您无法发布包含错误的历程。 在此[部分](publish-journey.md)中了解有关历程发布的更多信息。

![包含受众、条件和操作的完整历程流](assets/jo-journeyuc2_32bis.png)

发布后，您可以使用专用的报告工具监控旅程，以衡量旅程的有效性。

![历程分析报告，显示性能指标和统计数据](assets/jo-dynamic_report_journey_12.png)

在此[部分](../reports/live-report.md)中了解有关历程报告的更多信息。

## 常见使用案例 {#use-cases}

不确定从哪里开始？ 以下是历程可发挥最大价值的三种典型方案：

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
      <a href="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank">
        <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px">
      </a>
      <div><strong>欢迎系列</strong><br/>注册后，使用一系列消息自动载入新用户，引导他们浏览您的产品或服务。</div>
    </td>
    <td>
      <a href="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank">
        <img src="../assets/do-not-localize/icon-campaign.svg" width="35px">
      </a>
      <div><strong>放弃购买</strong><br/>通过发送包含个性化内容的及时提醒，重新吸引未完成购买的客户。</div>
    </td>
    <td>
      <a href="jo-use-cases.md">
        <img src="../assets/do-not-localize/icon-content.svg" width="35px">
      </a>
      <div><strong>重新参与</strong><br/>根据非活动用户最后的已知行为，重新吸引具有定向优惠或更新的非活动用户。</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="jo-use-cases.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
  </tr>
</table>

## 其他资源

* **[历程类型和配置文件条目](entry-management.md)** — 了解所有历程类型（单一事件、业务事件、读取受众、受众资格）以及配置文件如何输入、重新输入和流过历程。
* **[历程设计器概述](using-the-journey-designer.md)** — 掌握历程画布界面以设计和编排客户历程。
* **[历程活动](about-journey-activities.md)** — 发现所有可用的活动，包括事件、操作和编排组件。
* **[测试历程](testing-the-journey.md)** — 了解如何在发布到生产环境之前使用测试模式测试您的历程。
* **[发布历程](publish-journey.md)** — 了解历程发布流程以及如何管理实时历程。
* **[历程报表](report-journey.md)** — 使用详细的指标和见解跟踪和分析旅程表现。
* **[历程疑难解答](troubleshooting.md)** — 查找常见历程问题的解决方案和调试的最佳实践。
* **[历程教程](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"}** — 浏览有关历程构建和最佳实践的分步视频教程。

