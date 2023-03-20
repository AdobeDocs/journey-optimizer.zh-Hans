---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动入门
description: 进一步了解Journey Optimizer中的促销活动
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 营销活动，操作方法，开始， optimizer
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
>abstract="创建营销活动，以便跨各种渠道将一次性内容交付到特定区段。 在创建营销活动之前，请确保已准备好渠道界面（即消息预设）和Adobe Experience Platform区段以供使用。"

使用 Journey Optimizer 营销活动通过各种渠道向特定区段投放一次性内容。使用历程时，将依次执行操作。 借助营销活动，可同时执行诸多操作：立即执行或根据指定计划执行。

您可以创建两种类型的营销活动：

* **计划促销活动** 允许针对促销用例（如促销优惠、参与促销活动、公告、法律声明或策略更新）进行简单的临时批量通信。
* **API触发的营销活动** 允许使用REST API（密码重置、购物车放弃等）的简单事务/操作消息，其中需要使用用户档案属性和有效负荷中的上下文数据进行个性化。

创建营销活动的主要步骤如下：

![](assets/create-campaign-process.png)

➡️ [在视频中发现此功能](#video)

## 开始前 {#campaign-prerequisites}

在Journey Optimizer中开始创建您的第一个营销活动之前，请查看以下先决条件：

1. **您需要适当的权限**. 营销活动仅供有权访问与营销活动相关的营销活动的用户使用 **[!UICONTROL 产品配置文件]** 例如，促销活动管理员、促销活动审批者、促销活动管理器和/或促销活动查看器。

   如果您无法访问营销活动，则必须扩展您的权限。 如果您有权访问 [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"} 对于贵组织，请执行以下步骤。 如果没有，请联系您的Journey Optimizer管理员。

   +++了解如何分配营销活动权限

   要分配对应的 **[!UICONTROL 产品配置文件]** 对您的用户：

   1. 从 [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}，选择 [!DNL Adobe Experience Platform] 产品。

   1. 浏览到 **[!UICONTROL 产品配置文件]** 选项卡，选择与内置营销活动相关的其中一个 **[!UICONTROL 产品配置文件]**:促销活动管理员、促销活动审批者、促销活动管理器或促销活动查看者。

      有关Journey Optimizer促销活动的更多信息 **[!UICONTROL 产品配置文件]** 和 **[!UICONTROL 权限]**, [请参阅此页面](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. 单击 **[!UICONTROL 添加用户]** 要将选定的 **[!UICONTROL 产品配置文件]**.

      ![](assets/do-not-localize/admin_2.png)

   1. 键入您的用户名、组或电子邮件地址，然后单击 **[!UICONTROL 保存]**.
   您的用户现在可以访问 **[!UICONTROL 促销活动]**.

+++

1. **您需要受众**. 在创建营销活动之前，需要提供受众区段。 了解有关受众创建的更多信息 [本页](../segment/about-segments.md).
1. **你需要一个通道表面**. 要选择渠道，必须创建并提供相应的渠道表面（即预设）。 进一步了解渠道曲面 [本页](../configuration/channel-surfaces.md).

## 操作方法视频 {#video}

了解如何创建您的第一个营销活动。

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
