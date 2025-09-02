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
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 99%

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
>abstract="**计划的营销活动**&#x200B;会立即或在指定日期执行&#x200B;，其旨在发送市场营销类型的消息。**API 触发的**&#x200B;营销活动使用 API 调用来执行 。它们旨在发送营销性消息（需要用户同意的推广消息）或事务性消息（非商业消息，在特定上下文中，也可以发送到已取消订阅的轮廓）。"

使用 Journey Optimizer 营销活动通过各种渠道向特定受众投放一次性内容。使用历程时，操作将按顺序执行。借助营销活动，可同时执行诸多操作：立即执行或根据指定计划执行。

![](assets/gs-campaigns.png)

您可以在 Journey Optimizer 中创建不同类型的营销活动：

* **操作营销活动**

  通过“操作营销活动”（或“计划营销活动”），可以针对营销用例（如促销产品建议、参与性营销活动、公告、法律声明或政策更新）进行简单的临时批量通信。

* **API 触发的营销活动**

  通过“API 触发的营销活动”，您可以在正确的时间将营销通信传达给受众，或者允许将事务性/运营消息发送给个人（如密码重置），其中需求可能涉及个性化，不仅会使用轮廓属性，还会用到触发器中的实时上下文数据（即 REST API 有效负载）。

* **精心策划的营销活动**

  Adobe Journey Optimizer 中的营销活动编排功能旨在为品牌发起的跨渠道复杂营销活动提供支持，从而帮助您大规模提高参与度、收入和客户忠诚度。

  跨渠道营销至关重要，而精心设计的营销活动可以让这项工作变得流畅一体。借助可视化的拖放界面，您可以设计和自动化跨多个渠道的复杂营销工作流程，从分段到消息投放。您可以在直观的环境中进行一切操作，从而提升速度、控制力和效率。

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
