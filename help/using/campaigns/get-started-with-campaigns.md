---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动快速入门
description: 了解 Journey Optimizer 中营销活动的更多信息
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 营销活动、操作方法、入门、optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 98%

---

# 营销活动快速入门 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="营销活动计划"
>abstract="默认情况下，营销活动在手动激活时开始，并在发送消息一次后立即结束。您可以灵活地设置特定日期和时间以发送消息。此外，还可以为定期操作营销活动指定结束日期。在操作触发器中，您还可以配置消息发送频率以满足您的偏好。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="营销活动开始"
>abstract="指定应发送消息的日期和时间。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="营销活动结束"
>abstract="指定应停止执行周期性营销活动的时间。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="营销活动操作触发器"
>abstract="定义营销活动消息的发送频率。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="速率控制"
>abstract="通过指定所需的速率限制为您的营销活动设置速率控制。此功能对于防止下游系统（如登陆页面或客户服务平台）过载尤为实用。"

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="创建营销活动"
>abstract="借助 **Adobe Journey Optimizer**，可使用各种渠道向特定受众投放一次性内容。使用历程时，操作将按顺序执行。借助营销活动，可同时执行诸多操作：立即执行或根据指定计划执行。"

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="营销活动"
>abstract="创建营销活动，以跨各种渠道向特定受众投放一次性内容。在创建营销活动之前，请确保您已准备好渠道配置和 Adobe Experience Platform 受众以供使用。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="营销活动类型"
>abstract="选择营销活动的类型。可用渠道根据所选类型而不同。<br>**计划的营销活动**（操作营销活动）– 非常适合简单的一次性批量通信，您可以计划在某个特定的时间执行。<br>**API 触发的营销活动** – 通过 API 调用激活该功能，能够直接从外部系统自动发送基于事件的消息。<br>**编排的营销活动** – 提供一个可视化的拖放式画布，用于设计和自动化复杂、多步骤的营销工作流，包括从受众细分到跨渠道的个性化消息投放。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="营销活动"
>abstract="创建您的分段流程，设计跨渠道消息并规划营销活动。支持的渠道：电子邮件、短信、推送通知。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="营销活动"
>abstract="提供单次或重复的出站投放或持续的入站操作。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="营销活动"
>abstract="提供单次或重复的出站事务性操作。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="营销活动"
>abstract="向目标受众投放个性化营销通信。支持的渠道：电子邮件、短信、推送通知。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="营销活动"
>abstract="向单个轮廓或轮廓集投放事务性通信。支持的渠道：电子邮件、短信、推送通知。"

Adobe Journey Optimizer 赋能您跨多个渠道向特定受众传递针对性的单次内容。通过营销活动，您可以同步执行协调的营销行动，在恰当时机向受众传递精准信息。

本指南提供清晰的路线图，帮助您理解营销活动基础概念，根据实际用例选择合适的营销活动类型，并自信地设计出能提供有影响力的客户体验的营销活动。

## 什么是营销活动？

**营销活动**&#x200B;是通过一个或多个渠道向特定受众传递内容的协调营销行动。与历程中操作按顺序执行不同，营销活动的操作会同时执行——无论是即时启动还是按预设计划进行。

使用[!DNL Journey Optimizer]营销活动可以：

* 向目标受众区段投放&#x200B;**一次性或周期性内容**
* 跨电子邮件、推送、短信、应用程序内、web 等执行&#x200B;**协调的多渠道通信**
* 通过 API 调用触发&#x200B;**自动响应**，以实现事件驱动的实时消息传递
* 使用可视化编排工具设计&#x200B;**复杂的营销工作流**

![](assets/gs-campaigns.png)

➡️**准备好开始构建了吗？**&#x200B;[在几分钟内创建您的第一个营销活动](create-campaign.md)。

## 选择您的营销活动类型 {#campaign-types}

**在开始构建**&#x200B;之前，请务必了解哪种类型的营销活动适合您的用例。 Adobe Journey Optimizer 支持三种营销活动类型，每种类型针对不同的场景和激活机制而设计：

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB 编排的营销活动]

**何时使用：**&#x200B;复杂的多步骤营销工作流

**编排的营销活动**&#x200B;提供可视化拖放式画布，用于设计和自动化复杂的营销工作流。从受众细分到跨渠道个性化消息推送，所有操作都在一个兼顾效率与管控的直观环境中完成。

**非常适合：**&#x200B;多步骤客户互动计划、复杂细分与目标选择策略、跨渠道营销活动编排、品牌发起的大规模营销，以及含多重决策点的高级工作流程自动化。

➡️[了解编排的营销活动](../orchestrated/gs-orchestrated-campaigns.md)

>[!TAB 操作营销活动（已计划）]

**何时使用：**&#x200B;简单的计划性批量通信

**操作营销活动**（也称为计划营销活动）非常适合于在特定时间执行的简单、一次性或周期性批量通信。

**两个类别：**

* **营销型** – 促销优惠、互动活动、公告通知、法律声明或政策更新。需要收件人选择加入。
* **交易型** – 服务中断、紧急通知、取消告知。无需选择启用。

**非常适合：**&#x200B;面向客户区段的月度简报、时效性促销公告、季节性营销活动、产品发布通讯，以及服务中断通知。

➡️[了解操作营销活动](create-campaign.md)

>[!TAB API 触发的营销活动]

**何时使用：**&#x200B;与外部系统集成的实时事件驱动型消息推送

**API 触发的营销活动** – 通过 API 调用激活，支持直接从外部系统触发自动化消息推送。此类营销活动支持使用轮廓属性及 API 负载中的实时上下文数据进行个性化定制。

**两个类别：**

* **营销型** – 针对目标受众的个性化营销信息。
* **交易型** – 基于个体行为触发的消息（密码重置、购物车购买等）

**非常适合：**&#x200B;密码重置确认、购物车弃单挽回、订单确认和物流更新、帐户活动通知以及实时个性化推荐。

➡️[了解 API 触发的营销活动](api-triggered-campaigns.md)

>[!ENDTABS]

>[!NOTE]
>
>不确定选择哪种类型？ 从&#x200B;**操作营销活动**（计划性批量通信）或 **API 触发的营销活动**（实时消息推送）开始——它们涵盖了大多数常见用例。

## 先决条件 {#prerequisites}

在使用营销活动之前，请确保已完成以下准备工作：

* **受众** – 创建营销活动前，受众必须在 Adobe Experience Platform 中准备就绪。[受众快速入门→](../audience/about-audiences.md)

* **渠道配置** – 渠道配置（预设）必须预先创建，并确保您计划使用的渠道已就绪。[设置渠道配置→](../configuration/channel-surfaces.md)

* **权限** – 您需要根据营销活动类型获得相应的权限。若您无法访问营销活动功能，请联系您的管理员。[了解内置角色→](../administration/ootb-product-profiles.md)

  +++营销活动权限列表

  | 营销活动类型 | 权限 |
  |-------------|---------------|
  | **操作营销活动**&#x200B;和&#x200B;**API触发的营销活动** | 营销活动管理员<br>营销活动审批者<br>营销活动经理<br>营销活动查看者 |
  | **编排的营销活动** | 编排的营销活动的管理员<br>编排的营销活动的审批者<br>编排的营销活动的经理<br>编排的营销活动的查看者 |

  +++

  +++如何分配营销活动权限

   1. 在 [!DNL Permissions] 产品中导航至&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡，选择一个内置的与营销活动相关的&#x200B;**[!UICONTROL 角色]**。

   1. 在&#x200B;**[!UICONTROL 用户]**&#x200B;选项卡中，单击&#x200B;**[!UICONTROL 添加用户]**。

   1. 输入您的用户名或电子邮件地址，或从列表中选择用户并单击&#x200B;**[!UICONTROL 保存]**。

  如果之前没有创建用户，请参阅[有关添加用户的文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/ui/users){target="_blank"}。

  随后，您的用户将收到一封重定向到您的实例的电子邮件。

  +++

## 您的营销活动创建工作流 {#workflow}

构建成功的营销活动须遵循清晰、可重复的流程。 以下是您的分步工作流：

+++1.规划您的营销活动

在开始之前，请明确您的目标：

* **目标是什么？** （例如，促进转化、提高参与度、通知客户）
* **受众是谁？**（例如：在 Adobe Experience Platform 中创建或选择受众）
* **适合哪种营销活动类型？** （请参阅上面的[营销活动类型](#campaign-types)）
* **您将使用哪些渠道？** （电子邮件、推送、短信、应用程序内、web 等）→[查看各活动类型支持的渠道](../channels/gs-channels.md#channels)
* **应在何时执行？**（立即执行、计划执行或 API 触发）

+++

+++2.配置营销活动属性

设置营销活动的基础信息：

1. **命名并与描述**&#x200B;您的活动以便识别
2. **选择营销活动类型**（操作、API 触发或编排式）
3. **选择您的受众**
4. 如果使用冲突管理，请&#x200B;**设置优先级**
5. **配置计划**（适用于操作营销活动）或 API 详情（适用于 API 触发活动）

**类型专属指南：**&#x200B;[操作营销活动属性](campaign-properties.md) | [API 触发的营销活动属性](api-triggered-campaign-properties.md) | [编排的营销活动设置](../orchestrated/create-orchestrated-campaign.md)

+++

+++3.设计内容 

为受众打造有吸引力的邮件内容：

* 使用&#x200B;**电子邮件设计器**&#x200B;创建丰富的电子邮件体验
* 配置带图片和深度链接的&#x200B;**推送通知**
* 设计支持个性化的&#x200B;**短信/彩信**
* 创建&#x200B;**应用程序内**&#x200B;和&#x200B;**Web**&#x200B;体验
* 运用轮廓属性与上下文数据添加&#x200B;**个性化**&#x200B;内容

**类型专属指南：**&#x200B;[操作营销活动内容](campaign-content.md) | [API 触发的营销活动内容](api-triggered-campaign-content.md) | [编排的营销活动内容](../orchestrated/create-orchestrated-campaign.md)

+++

+++4.审查和测试

激活前务必审核您的营销活动：

* 使用测试轮廓&#x200B;**预览内容**
* **检查目标选择**&#x200B;以确保触达正确受众
* **确认计划**&#x200B;与激活设置
* 如果使用审批工作流，**请求审批**
* 使用种子列表&#x200B;**测试可投放性**

**类型专属指南：** [审查操作营销活动](review-activate-campaign.md) | [审查 API 触发的营销活动](review-activate-api-triggered-campaign.md) | [审查编排的营销活动](../orchestrated/create-orchestrated-campaign.md)

+++

+++5.激活您的营销活动

审查完成后，激活您的营销活动：

* **手动激活** – 立即或按计划时间激活
* **API 激活** – 对于 API 触发的营销活动，使用激活端点
* **审批流程** – 如果需要，请等待利益相关者审批

注意：已激活的营销活动不可编辑（您必须复制后修改）

**类型专属指南：** [激活操作营销活动](review-activate-campaign.md) | [激活 API 触发的营销活动](review-activate-api-triggered-campaign.md) | [激活编排的营销活动](../orchestrated/create-orchestrated-campaign.md)

+++

+++6.监测和分析

跟踪营销活动的执行情况：

* 查看营销活动报告和分析
* 监控送达率与参与量度
* 跟踪错误和退信情况
* 分析转化率和 ROI
* 运用洞察进行优化

**类型专属指南：** [操作促销活动报告](../reports/campaign-global-report-cja.md) | [API 触发的营销活动监控](api-triggered-campaigns.md#monitor) | [编排的营销活动分析](../orchestrated/create-orchestrated-campaign.md)

+++

## 让我们深入探究 {#get-started-types}

现在您已了解[!DNL Journey Optimizer]中的营销活动，请选择您的营销活动类型以开始：

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="操作营销活动" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">操作营销活动</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="短信" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API 触发的营销活动</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="推送" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">编排的营销活动</a></td>
</tr></table>

随着您对营销活动越来越熟悉，请探索这些强大的功能：

:::: landing-cards-container

:::
![icon](https://cdn.experienceleague.adobe.com/icons/calendar-alt.svg)

**排期与时机选择**

为特定日期/时间安排营销活动，设置重复投放，并优化发送时间以实现最佳效果。（操作和 API 触发的营销活动）

[了解排期设置](campaign-schedule.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

**速率控制**

限制消息吞吐量，以防止登陆页面或客户关怀平台等下游系统过载。 （操作和 API 触发的营销活动）

[控制速率限制](create-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

**受众目标选择**

精准定位特定的 Adobe Experience Platform 受众，并动态管理受众资格筛选。

[选择营销活动受众](campaign-audience.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg)

**审批工作流**

在营销活动开始之前实施审查和批准流程，确保内容质量与合规性。（操作和 API 触发的营销活动）

[审查和激活](review-activate-campaign.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/clock.svg)

**免打扰时间**

通过避开指定时间窗口发送消息，尊重客户偏好。（操作和 API 触发的营销活动）

[配置免打扰时间](quiet-hours.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

**优化**

使用定位规则和内容实验提供个性化内容并最大化参与度。

[优化营销活动](../content-management/gs-message-optimization.md)
:::

::::
