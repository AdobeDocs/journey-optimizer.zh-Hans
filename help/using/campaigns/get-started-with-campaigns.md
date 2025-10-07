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
source-git-commit: 801b90201c3ffcbfb7b038abac2bf99209a14c7a
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 60%

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
>abstract="选择营销活动的类型。可用渠道根据所选类型而不同。<br>**计划的营销活动**（操作营销活动）– 非常适合简单的一次性批量通信，您可以计划在某个特定的时间执行。<br>**API 触发的营销活动** – 通过 API 调用激活该功能，能够直接从外部系统自动发送基于事件的消息。<br>**编排的营销活动** – 提供一个可视化的拖放式画布，用于设计和自动化复杂、多步骤的营销工作流，包括从受众分段到跨渠道的个性化消息投放。"

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

使用[!DNL Journey Optimizer]营销活动跨多个渠道向特定受众投放一次性内容。 与旅程不同（旅程分步执行操作），营销活动同时执行操作 — 立即执行或按定义的计划执行。

![](assets/gs-campaigns.png)

## 营销活动类型

[!DNL Journey Optimizer]支持三种营销活动类型。 每种类型适合不同的用例，并支持不同的渠道。

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB 精心策划的营销活动]

**精心策划的营销活动**&#x200B;跨渠道推动由品牌发起的复杂营销活动，帮助您大规模提高参与度、收入和客户忠诚度。

跨渠道营销至关重要，而精心设计的营销活动可以让这项工作变得流畅一体。借助可视化的拖放界面，您可以设计和自动化跨多个渠道的复杂营销工作流程，从分段到消息投放。您可以在直观的环境中进行一切操作，从而提升速度、控制力和效率。

➡️ [了解如何使用编排的营销活动](../orchestrated/gs-orchestrated-campaigns.md)。

>[!TAB 操作营销活动（或计划的营销活动）]

**操作营销活动**（也称为计划营销活动）允许进行简单的临时批处理通信。

* **已计划 — 营销** — 对于营销用例，如促销优惠、参与活动、公告、法律声明或策略更新。 需要选择加入收件人。
* **已计划 — 事务性** — 与营销活动不同，事务性活动不需要收件人选择加入。 此类别用于与中断、紧急情况、取消相关的通信。 支持的渠道：电子邮件、短信、推送通知。

➡️ [了解如何使用操作营销活动](create-campaign.md)

>[!TAB API 触发的营销活动]

**API触发的营销活动**&#x200B;允许您使用API调用触发营销活动的执行。 在需要个性化时，这些通信可以发送，其中不仅包括密码重置配置文件属性，还包括触发器中的实时上下文数据（即REST API有效负载）。

* **API触发 — 营销** — 向目标受众发送个性化营销通信。
* **API触发 — 事务性** — 在个人执行的操作（如密码重置请求、购物车购买等）之后发送消息。

➡️ [了解如何使用API触发的营销活动](api-triggered-campaigns.md)


>[!ENDTABS]

## 按营销活动类型显示的受支持渠道 {#channels}

下表显示了不同促销活动类型中每个渠道的可用性，说明了支持这些渠道的位置。

| 渠道 | 操作（营销） | 操作（事务性） | API触发（营销） | API触发（事务性） | 已编排 |
|----------------------|---------------------|-------------------------|----------------------------|--------------------------------|--------------|
| 电子邮件 | ✅ | ✅ | ✅ | ✅ | ✅ |
| 短信 | ✅ | ✅ | ✅ | ✅ | ✅ |
| 推送通知 | ✅ | ✅ | ✅ | ✅ | ✅ |
| 应用程序内 | ✅ | — | — | — | — |
| 直邮 | ✅ | — | — | — | — |
| Web | ✅ | — | — | — | — |
| 基于代码的费用 | ✅ | — | — | — | — |
| 内容卡 | ✅ | — | — | — | — |
| WhatsApp | ✅ | — | — | — | — |
| 线形图 | ✅ | — | — | — | — |

## 先决条件 {#prerequisites}

在使用营销活动之前，请确保已查看以下先决条件。

* **受众**&#x200B;受众需要在创建营销活动之前可用。 [受众快速入门](../audience/about-audiences.md)。

* **渠道配置** — 要能够选择渠道，您必须已创建相应的渠道配置（即预设）并且可用。 [了解如何设置渠道配置](../configuration/channel-surfaces.md)。

* **权限** — 营销活动仅适用于具有下列相应权限的用户。 如果您无法访问Campaign功能，请联系您的管理员以请求必要的权限。 [进一步了解 Journey Optimizer 内置角色](../administration/ootb-product-profiles.md)

  | 营销活动类型 | 权限 |
  |----------------------------|----------------------------------------------------------------------------|
  | **操作营销活动** | Campaign管理员<br>Campaign审批者<br>Campaign管理员<br>Campaign查看器 |
  | **API 触发的营销活动** | Campaign管理员<br>Campaign审批者<br>Campaign管理员<br>Campaign查看器 |
  | **精心策划的营销活动** | 协调的活动管理员<br>协调的活动审批者<br>协调的活动管理员<br>协调的活动查看器 |

  +++了解如何分配营销活动相关角色

   1. 要将角色分配给 [!DNL Permissions] 产品中的用户，请导航至&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡，然后相应地选择一个内置营销活动相关&#x200B;**[!UICONTROL 角色]**（如前文所描述）。

   1. 在&#x200B;**[!UICONTROL 用户]**&#x200B;选项卡中，单击&#x200B;**[!UICONTROL 添加用户]**。

   1. 输入您的用户名或电子邮件地址，或从列表中选择用户并单击&#x200B;**[!UICONTROL 保存]**。

      如果之前没有创建用户，请参阅[有关添加用户的文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/ui/users)。

  随后，您的用户将收到一封重定向到您的实例的电子邮件。

  +++

## 让我们深入探究

现在您已了解 [!DNL Journey Optimizer] 中的营销活动，接下来请深入了解这些文档部分，开始创建您的第一个营销活动。

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="操作营销活动" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">操作营销活动</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="短信" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API 触发的营销活动</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="推送" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">精心策划的营销活动</a></td>
</tr></table>
