---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动入门
description: 了解 Journey Optimizer 中营销活动的更多信息
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 营销活动、操作方法、入门、optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 68%

---

# 营销活动入门 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="营销活动计划"
>abstract="默认情况下，营销活动在手动激活时开始，并在发送消息一次后立即结束。您可以灵活地设置特定日期和时间以发送消息。此外，您还可以为循环操作营销活动指定结束日期。 在操作触发器中，您还可以配置消息发送频率以满足您的偏好。"

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
>title="节流速率控制"
>abstract="节流速率控制"

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
>abstract="立即执行或在指定日期执行&#x200B;**计划的营销活动**，其旨在发送市场营销类型的消息。使用 API 调用执行 **API 触发的**&#x200B;活动。它们旨在发送营销性消息（需要用户同意的推广消息）或事务性消息（非商业消息，在特定上下文中，也可以发送到已取消订阅的轮廓）。"

使用 Journey Optimizer 营销活动通过各种渠道向特定受众投放一次性内容。使用历程时，操作将按顺序执行。借助营销活动，可同时执行诸多操作：立即执行或根据指定计划执行。

![](assets/gs-campaigns.png)

您可以在Journey Optimizer中创建不同类型的营销活动：

* **操作营销活动**

  利用操作营销活动（或计划营销活动），可以针对营销用例（如促销优惠、参与营销活动、公告、法律声明或策略更新）进行简单的临时批量通信。

* **API触发的营销活动**

  API触发的营销活动允许营销通信在适当的时间联系受众，或允许向个人发送交易/运营消息，如密码重置，其中需求可能涉及个性化，不仅使用用户档案属性，还涉及触发器中的实时上下文数据，即REST API有效负载。

<!--* **Orchestrated campaigns**

    Campaign Orchestration in Adobe Journey Optimizer powers sophisticated, brand-initiated marketing campaigns across channels, helping you drive engagement, revenue, and customer loyalty at scale.

    While cross-channel marketing is essential, orchestrated campaigns make it seamless. With a visual, drag-and-drop interface, you can design and automate complex marketing workflows, from segmentation to message delivery, across multiple channels. Everything happens in one intuitive environment, built for speed, control, and efficiency.-->

## 开始前 {#campaign-prerequisites}

在[!DNL Journey Optimizer]中开始创建您的第一个营销活动之前，请检查以下先决条件：

1. **您需要适当的权限**。营销活动仅适用于有权访问与营销活动相关的&#x200B;**[!UICONTROL 产品配置文件]**&#x200B;的用户，例如Campaign管理员、Campaign审批者、Campaign经理和/或Campaign查看器。 如果您无法访问营销活动，则必须扩展您的权限。

   +++了解如何分配营销活动相关角色

   1. 要将角色分配给 [!DNL Permissions] 产品中的用户，请导航至&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡，然后选择一个内置的营销活动&#x200B;**[!UICONTROL 角色]**：营销活动管理员、营销活动审批者、营销活动经理或营销活动查看者。

   1. 在&#x200B;**[!UICONTROL 用户]**&#x200B;选项卡中，单击&#x200B;**[!UICONTROL 添加用户]**。

   1. 输入您的用户名或电子邮件地址，或从列表中选择用户并单击&#x200B;**[!UICONTROL 保存]**。

      如果之前没有创建用户，请参阅[有关添加用户的文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/access-control/ui/users)。

   随后，您的用户将收到一封重定向到您的实例的电子邮件。

   +++

1. **您需要有受众**。在创建营销活动之前，需要设置受众。[开始使用受众](../audience/about-audiences.md)。

1. **您需要一个渠道配置**。要选择渠道，必须创建并提供相应的渠道配置（即预设）。[了解如何设置渠道配置](../configuration/channel-surfaces.md)。

## 让我们深入探究

现在您已了解[!DNL Journey Optimizer]中的营销活动，接下来该深入了解这些文档部分，以开始创建您的第一个营销活动。

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="操作营销活动" src="assets/do-not-localize/gs-action-campaign.png" width="50%"></a><br/><a href="create-campaign.md">操作营销活动</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="短信" src="assets/do-not-localize/gs-api-triggered-campaign.png" width="50%"></a><br/><a href="api-triggered-campaigns.md">API触发的营销活动</a></td>
</tr></table>

<!--
<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="action campaigns" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Action campaigns</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API triggered campaigns</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrated campaigns</a></td>
</tr></table>-->
