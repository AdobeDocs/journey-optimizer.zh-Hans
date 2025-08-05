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
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 74%

---

# 营销活动快速入门 {#get-started-campaigns}

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

您可以在 Journey Optimizer 中创建不同类型的营销活动：

* **操作营销活动**

  通过“操作营销活动”（或“计划营销活动”），可以针对营销用例（如促销产品建议、参与性营销活动、公告、法律声明或政策更新）进行简单的临时批量通信。

* **API 触发的营销活动**

  通过“API 触发的营销活动”，您可以在正确的时间将营销通信传达给受众，或者允许将事务性/运营消息发送给个人（如密码重置），其中需求可能涉及个性化，不仅会使用轮廓属性，还会用到触发器中的实时上下文数据（即 REST API 有效负载）。

* **编排的营销活动**

  Adobe Journey Optimizer中的营销活动编排支持由品牌发起的各种渠道的复杂营销活动，从而帮助您大规模提高参与度、收入和客户忠诚度。

  虽然跨渠道营销至关重要，但精心设计的营销活动可以无缝进行。 借助可视化拖放界面，您可以跨多个渠道设计和自动化从分段到消息投放在内的复杂营销工作流。 一切都在为速度、控制和效率而构建的直观环境中进行。

## 先决条件 {#prerequisites}

在创建营销活动之前，请确保已查看了以下先决条件。

### 权限

营销活动仅适用于具有下列相应权限的用户。 [了解有关Journey Optimizer内置角色的更多信息](../administration/ootb-product-profiles.md)

>[!BEGINTABS]

>[!TAB 操作营销活动]

Campaign管理员
Campaign审批者
营销活动管理器
营销活动查看器

>[!TAB API 触发的营销活动]

Campaign管理员
Campaign审批者
营销活动管理器
营销活动查看器

>[!TAB 编排的营销活动]

编排的Campaign管理员
编排的活动审批者
编排的活动管理器
编排的活动查看器

>[!ENDTABS]

如果您无法访问Campaign功能，请联系您的管理员以请求必要的权限。

+++了解如何分配营销活动相关角色

1. 要向[!DNL Permissions]产品中的用户分配角色，请导航到&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡，然后选择上面详细介绍的内置营销活动相关&#x200B;**[!UICONTROL 角色]**&#x200B;之一。

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
