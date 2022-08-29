---
title: 营销活动入门
description: 进一步了解 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: d747cc9a4d065ea9110cb8065c113326959e2a41
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 4%

---

# 营销活动入门 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="营销活动"
>abstract="创建营销活动，以便跨各种渠道将一次性内容交付到特定区段。 在创建营销活动之前，请确保已准备好渠道界面（即消息预设）和Adobe Experience Platform区段以供使用。"

使用Journey Optimizer促销活动通过各种渠道向特定区段交付一次性内容。 使用历程时，设计会按顺序执行操作。 对于营销活动，可同时执行（立即执行）或根据指定的计划执行（即）操作。

创建促销活动以发送简单的临时批量通信，以用于营销用例，如促销优惠、参与促销活动、公告、法律声明或策略更新。

➡️ [在视频中发现此功能](#video)

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

## 开始前 {#campaign-prerequisites}

在Journey Optimizer中开始创建您的第一个营销活动之前，请查看以下先决条件：

1. **您需要适当的权限**. 营销活动仅供有权访问与营销活动相关的营销活动的用户使用 **[!UICONTROL Product profile]** 例如，促销活动管理员、促销活动审批者、促销活动管理器和/或促销活动查看器。 如果您无法访问营销活动，则必须扩展您的权限。 如果您有权访问 [Adobe Admin Console](https://adminconsole.adobe.com/)为您的组织{target=&quot;_blank&quot;}，请按照以下步骤操作。 如果没有，请联系您的Journey Optimizer管理员。

+++了解如何分配营销活动权限

要分配对应的 **[!UICONTROL Product profile]** 对您的用户：

1. 从 [!DNL Admin console]，选择 [!DNL Adobe Experience Platform] 产品。

1. 从 **[!UICONTROL Product profile]** 选项卡，选择与内置营销活动相关的 **[!UICONTROL Product profile]**:促销活动管理员、促销活动审批者、促销活动管理器或促销活动查看者。

   有关Journey Optimizer促销活动的更多信息 **[!UICONTROL Product profiles]** 和 **[!UICONTROL Permissions]**, [请参阅此页面](../administration/ootb-product-profiles.md).

   ![](assets/do-not-localize/admin_1.png)

1. 单击 **[!UICONTROL Add user]** 要将选定的 **[!UICONTROL Product profile]**.

   ![](assets/do-not-localize/admin_2.png)

1. 键入您的用户名、组或电子邮件地址，然后单击 **[!UICONTROL Save]**.

您的用户现在将能够访问 **[!UICONTROL Campaigns]**.

+++

1. **您需要受众**. 在创建营销活动之前，需要提供受众区段。 了解有关受众创建的更多信息 [本页](../segment/about-segments.md).
1. **你需要一个通道表面**. 要选择通道，必须创建并提供相应的通道曲面。 了解有关渠道曲面（即预设）的更多信息 [本页](../configuration/channel-surfaces.md)

## 访问活动 {#access}

营销活动可从 **[!UICONTROL Campaigns]** 菜单。

默认情况下，列表会显示 **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]**&#x200B;和 **[!UICONTROL Live]** 状态。 要显示已停止、已完成和已存档的营销活动，您需要清除过滤器。

![](assets/create-campaign-list.png)

## 营销活动状态 {#statuses}

营销活动可以有多种状态：

* **[!UICONTROL Draft]**:营销活动正在编辑，尚未激活。
* **[!UICONTROL Activating]**:营销活动正在激活。
* **[!UICONTROL Live]**:营销活动已激活。
* **[!UICONTROL Scheduled]**:营销活动已配置为在特定开始日期激活。
* **[!UICONTROL Stopped]**:营销活动已手动停止。 您无法再激活或重复使用它(请参阅 [停止营销活动](modify-stop-campaign.md#stop))
* **[!UICONTROL Completed]**:营销活动已完成。 此状态在营销活动激活3天后自动分配，如果营销活动定期执行，则在营销活动结束日期自动分配。
* **[!UICONTROL Archived]**:营销活动已存档。

>[!NOTE]
>
>位于 **[!UICONTROL Live]** 或 **[!UICONTROL Scheduled]** 状态表示营销活动的新版本已创建且尚未激活(请参阅 [修改营销活动](modify-stop-campaign.md#modify))。

## 操作方法视频 {#video}

了解如何创建您的第一个营销活动。

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
