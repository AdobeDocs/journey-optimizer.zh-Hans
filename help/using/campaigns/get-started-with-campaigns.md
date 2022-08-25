---
title: 营销活动入门
description: 进一步了解 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---

# 营销活动入门 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="营销活动"
>abstract="通过促销活动，您可以跨多个渠道向特定区段交付一次性内容。 在创建新营销活动之前，请确保已准备好渠道界面（即消息预设）和Adobe Experience Platform区段以供使用。"

## 关于营销活动 {#about}

>[!IMPORTANT]
>
>此功能仅适用于具有促销活动相关产品用户档案（如促销活动管理员、促销活动审批者、促销活动管理器和/或促销活动查看者）访问权限的用户。 有关如何分配产品配置文件的更多信息，请参阅 [本页](../administration/permissions.md).

营销活动允许您使用多个渠道向特定区段交付一次性内容。 与设计按顺序执行操作的历程不同，营销活动可以同时执行操作（立即执行，也可以按指定的计划执行）。

这样，您就可以发送简单的临时批量通信，以用于营销用例，如促销优惠、参与活动、公告、法律声明或策略更新。

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

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
