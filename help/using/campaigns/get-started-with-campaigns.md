---
solution: Journey Optimizer
product: journey optimizer
title: 营销活动入门
description: 进一步了解 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 营销活动入门 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="促销活动"
>abstract="创建营销活动，以便跨各种渠道将一次性内容交付到特定区段。 在创建营销活动之前，请确保已准备好渠道界面（即消息预设）和Adobe Experience Platform区段以供使用。"

使用Journey Optimizer促销活动，通过各种渠道将一次性内容交付到特定区段。 使用历程时，将依次执行操作。 对于营销活动，可同时执行（立即执行）或根据指定的计划执行（即）操作。

您可以创建两种类型的营销活动：

* **计划促销活动** 允许针对促销用例（如促销优惠、参与促销活动、公告、法律声明或策略更新）进行简单的临时批量通信。
* **API触发的营销活动** 允许使用REST API（密码重置、卡放弃等）的简单事务/操作消息，其中需要使用用户档案属性和有效负载的上下文数据进行个性化。

创建营销活动的主要步骤如下：

![](assets/create-campaign-process.png)

➡️ [在视频中发现此功能](#video)

## 开始之前 {#campaign-prerequisites}

在Journey Optimizer中开始创建您的第一个营销活动之前，请检查以下先决条件：

1. **您需要适当的权限**. 营销活动仅供有权访问与营销活动相关的营销活动的用户使用 **[!UICONTROL Product profile]** 例如，促销活动管理员、促销活动审批者、促销活动管理器和/或促销活动查看器。

   如果您无法访问营销活动，则必须扩展您的权限。 如果您有权访问 [Adobe Admin Console](https://adminconsole.adobe.com/)为您的组织{target=&quot;_blank&quot;}，请按照以下步骤操作。 如果没有，请联系您的Journey Optimizer管理员。

   +++了解如何分配营销活动权限

   要分配对应的 **[!UICONTROL Product profile]** 对您的用户：

   1. 从 [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}，选择 [!DNL Adobe Experience Platform] 产品。

   1. 浏览到 **[!UICONTROL Product profile]** 选项卡，选择与内置营销活动相关的其中一个 **[!UICONTROL Product profile]**:促销活动管理员、促销活动审批者、促销活动管理器或促销活动查看者。

      有关Journey Optimizer促销活动的更多信息 **[!UICONTROL Product profiles]** 和 **[!UICONTROL Permissions]**, [请参阅此页面](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. 单击 **[!UICONTROL Add user]** 要将选定的 **[!UICONTROL Product profile]**.

      ![](assets/do-not-localize/admin_2.png)

   1. 键入您的用户名、组或电子邮件地址，然后单击 **[!UICONTROL Save]**.
   您的用户现在可以访问 **[!UICONTROL Campaigns]**.

+++

1. **您需要受众**. 在创建营销活动之前，需要提供受众区段。 了解有关受众创建的更多信息 [本页](../segment/about-segments.md).
1. **你需要一个通道表面**. 要选择渠道，必须创建并提供相应的渠道表面（即预设）。 进一步了解渠道曲面 [本页](../configuration/channel-surfaces.md).

## 操作方法视频 {#video}

了解如何创建您的第一个营销活动。

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
