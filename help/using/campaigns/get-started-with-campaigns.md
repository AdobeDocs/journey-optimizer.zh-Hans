---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动快速入门
description: 了解 Journey Optimizer 中营销活动的更多信息
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 营销活动、操作方法、入门、optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 5821bc3f3c6e81ae1ae7389bbca1bdcec11cc805
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 69%

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
>abstract="指定所需的速率限制，为您的营销活动设置速率控制。此功能对于防止登陆页面或客户关怀平台等下游系统过载特别有用。"

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
>abstract="选择营销活动的类型。 可用渠道因所选类型而异。 <br>**计划的营销活动** （操作营销活动） — 非常适合于安排在特定时间运行的简单、一次性批量通信。<br>**API触发的营销活动** — 通过API调用激活，支持直接从外部系统自动发送基于事件的消息。<br>**编排的营销活动** — 提供可视、拖放式画布以设计和自动化复杂的多步骤营销工作流，从受众分段到跨渠道的个性化消息投放。"

使用 Journey Optimizer 营销活动通过各种渠道向特定受众投放一次性内容。使用历程时，操作将按顺序执行。借助营销活动，可同时执行诸多操作：立即执行或根据指定计划执行。

![](assets/gs-campaigns.png)

您可以在Journey Optimizer中创建不同类型的营销活动。 支持的渠道和用例因营销活动类型而异。 下面列出了这些类型。

* **操作营销活动**

  利用操作营销活动（或计划营销活动），可以针对营销用例（如促销优惠、参与营销活动、公告、法律声明或策略更新）进行简单的临时批量通信。 在此页面[上了解有关行动促销活动功能、用例和支持的渠道](create-campaign.md)的更多信息。

* **API 触发的营销活动**

  API触发的营销活动允许营销通信在适当的时间联系受众，或允许向个人发送交易/运营消息，如密码重置，其中需求可能涉及个性化，不仅使用用户档案属性，还涉及触发器中的实时上下文数据，即REST API有效负载。 在此页面[上了解有关API触发的营销活动功能、用例和受支持的渠道](api-triggered-campaigns.md)的更多信息。

* **精心策划的营销活动**

  Adobe Journey Optimizer 中的营销活动编排功能旨在为品牌发起的跨渠道复杂营销活动提供支持，从而帮助您大规模提高参与度、收入和客户忠诚度。

  跨渠道营销至关重要，而精心设计的营销活动可以让这项工作变得流畅一体。借助可视化的拖放界面，您可以设计和自动化跨多个渠道的复杂营销工作流程，从分段到消息投放。一切都在为速度、控制和效率而构建的直观环境中进行。 在此页面[上详细了解协调的营销活动功能、用例和受支持的渠道](../orchestrated/gs-orchestrated-campaigns.md)。

## 先决条件 {#prerequisites}

在创建营销活动之前，请确保已查看以下先决条件。

### 权限

营销活动仅适用于具有下列相应权限的用户。[进一步了解 Journey Optimizer 内置角色](../administration/ootb-product-profiles.md)

>[!BEGINTABS]

>[!TAB 操作营销活动]

营销活动管理员
营销活动审批者
营销活动经理
营销活动查看者

>[!TAB API 触发的营销活动]

营销活动管理员
营销活动审批者
营销活动经理
营销活动查看者

>[!TAB 精心策划的营销活动]

精心策划营销活动的管理员
精心策划营销活动的审批者
精心策划营销活动的经理
精心策划营销活动的查看者

>[!ENDTABS]

如果您无法访问营销活动功能，请联系管理员申请必要的权限。

+++了解如何分配活动相关角色

1. 要将角色分配给 [!DNL Permissions] 产品中的用户，请导航至&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡，然后相应地选择一个内置营销活动相关&#x200B;**[!UICONTROL 角色]**（如前文所描述）。

1. 在&#x200B;**[!UICONTROL 用户]**&#x200B;选项卡中，单击&#x200B;**[!UICONTROL 添加用户]**。

1. 输入您的用户名或电子邮件地址，或从列表中选择用户并单击&#x200B;**[!UICONTROL 保存]**。

   如果之前没有创建用户，请参阅[有关添加用户的文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/ui/users)。

随后，您的用户将收到一封重定向到您的实例的电子邮件。

+++

### 受众

在创建营销活动之前，需要设置受众。[受众快速入门](../audience/about-audiences.md)。

### 渠道配置

要选择渠道，必须创建并提供相应的渠道配置（即预设）。[了解如何设置渠道配置](../configuration/channel-surfaces.md)。

## 让我们深入探究

现在您已了解 [!DNL Journey Optimizer] 中的营销活动，接下来请深入了解这些文档部分，开始创建您的第一个营销活动。

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="操作营销活动" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">操作营销活动</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="短信" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API 触发的营销活动</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="推送" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">精心策划的营销活动</a></td>
</tr></table>
