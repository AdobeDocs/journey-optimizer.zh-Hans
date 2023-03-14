---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动入门
description: 详细了解Journey Optimizer中的促销活动
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 营销活动、如何、开始、优化器
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 8b1bf0b0469c1efc5194dae56ddddd9f05dbf722
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 12%

---

# 营销活动入门 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="营销活动"
>abstract="创建营销活动，以通过各种渠道向特定区段投放一次性内容。 在创建营销活动之前，请确保您具有可供使用的渠道界面（即消息预设）和Adobe Experience Platform区段。"

使用 Journey Optimizer 营销活动通过各种渠道向特定区段投放一次性内容。使用历程时，操作将按顺序执行。 借助营销活动，可同时执行诸多操作：立即执行或根据指定计划执行。

您可以创建两种类型的营销活动：

* **计划的活动** 允许针对营销用例（如促销优惠、参与促销活动、公告、法律声明或策略更新）进行简单的临时批量通信。
* **API触发的营销活动** 允许使用REST API发送简单的交易/操作消息（密码重置、购物车放弃等），其中需求可能涉及使用用户档案属性和有效负荷中的上下文数据进行个性化。

创建活动的主要步骤如下：

![](assets/create-campaign-process.png)

➡️ [在视频中发现此功能](#video)

## 开始前 {#campaign-prerequisites}

在Journey Optimizer中开始创建您的第一个营销活动之前，请检查以下先决条件：

1. **您需要适当的权限**. 营销活动仅适用于有权访问与营销活动相关的用户 **[!UICONTROL 产品配置文件]** 例如Campaign管理员、Campaign批准者、Campaign经理和/或Campaign查看者。

   如果您无法访问营销活动，则必须扩展您的权限。 如果您有权访问 [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"} 对于您的组织，请执行以下步骤。 如果不能，请联系您的Journey Optimizer管理员。

   +++了解如何分配营销活动权限

   要分配相应的 **[!UICONTROL 产品配置文件]** 对您的用户：

   1. 起始日期 [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}，选择 [!DNL Adobe Experience Platform] 产品。

   1. 浏览至 **[!UICONTROL 产品配置文件]** 选项卡，选择与活动相关的内置营销活动之一 **[!UICONTROL 产品配置文件]**：Campaign管理员、Campaign审批者、Campaign经理或Campaign查看者。

      有关Journey Optimizer促销活动的更多信息 **[!UICONTROL 产品配置文件]** 和 **[!UICONTROL 权限]**， [请参阅此页面](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. 单击 **[!UICONTROL 添加用户]** 将选定的分配给您的用户 **[!UICONTROL 产品配置文件]**.

      ![](assets/do-not-localize/admin_2.png)

   1. 键入您的用户名、组或电子邮件地址，然后单击 **[!UICONTROL 保存]**.
   您的用户现在可以访问 **[!UICONTROL 营销活动]**.

+++

1. **您需要一个受众**. 在创建营销活动之前，需要提供受众区段。 了解有关受众创建的更多信息 [本页内容](../segment/about-segments.md).
1. **您需要渠道界面**. 要能够选择渠道，您必须已创建相应的渠道界面（即预设）并且可用。 了解有关渠道界面的更多信息 [本页内容](../configuration/channel-surfaces.md).

## 操作方法视频 {#video}

了解如何创建您的第一个营销活动。

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
