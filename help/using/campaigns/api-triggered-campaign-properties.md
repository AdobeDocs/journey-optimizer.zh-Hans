---
solution: Journey Optimizer
product: journey optimizer
title: 定义API触发的营销活动属性
description: 了解如何定义API触发的营销活动属性。
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 营销活动， API触发， REST，优化器，消息
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 22%

---


# 定义API触发的营销活动属性 {#api-properties}

要创建新的API触发的营销活动，请执行以下步骤：

1. 浏览到&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单并选择&#x200B;**[!UICONTROL API触发]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 创建营销活动]**&#x200B;按钮并选择营销活动类型：

   * **[!UICONTROL API触发 — 营销]** — 选择此类型的API触发的营销活动向目标受众发送个性化的营销通信。

   * **[!UICONTROL API触发 — 事务型]** — 事务型营销活动旨在发送事务型消息，即在个人执行操作后发送的消息：密码重置请求、购物车购买等。

   ![](assets/api-triggered-modal.png)

1. 在&#x200B;**[!UICONTROL 属性]**&#x200B;选项卡中，输入营销活动的名称和描述。

   ![](assets/create-campaign-properties.png)

1. 使用&#x200B;**标记**&#x200B;字段将Adobe Experience Platform统一标记分配给您的营销活动。 这样，您就可以轻松地对营销活动进行分类，并改进营销活动列表中的搜索。[了解如何使用标记](../start/search-filter-categorize.md#tags)。

1. 您可以根据访问标签限制对此营销活动的访问。要对访问权限添加限制，请浏览页面顶部的&#x200B;**[!UICONTROL 管理访问权限]**&#x200B;按钮。确保仅选择您具有权限的标签。 [了解有关对象级访问控制的详细信息](../administration/object-based-access.md)。

## 后续步骤 {#next}

准备好营销活动配置和内容后，即可配置其操作。 [了解详情](api-triggered-campaign-action.md)
