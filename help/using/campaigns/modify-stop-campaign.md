---
solution: Journey Optimizer
product: journey optimizer
title: 修改或停止营销活动
description: 了解如何在中修改、停止或复制实时营销活动 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# 管理营销活动 {#modify-stop-campaign}

激活营销活动后，您可以随时修改或停止该营销活动。 这些操作仅适用于定期执行的营销活动。

此外，您还可以复制实时营销活动（执行一次或定期执行）以创建新营销活动，并存档已完成或已停止的营销活动。

## 访问营销活动 {#access}

营销活动可从 **[!UICONTROL Campaigns]** 菜单。

默认情况下，列表会显示 **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]**&#x200B;和 **[!UICONTROL Live]** 状态。

要显示已停止、已完成和已存档的营销活动，您需要清除过滤器。

![](assets/create-campaign-list.png)

## 营销活动状态 {#statuses}

营销活动可以有多种状态：

* **[!UICONTROL Draft]**:营销活动正在编辑，尚未激活。
* **[!UICONTROL Activating]**:营销活动正在激活。
* **[!UICONTROL Live]**:营销活动已激活。
* **[!UICONTROL Scheduled]**:营销活动配置为在特定开始日期激活。
* **[!UICONTROL Stopped]**:营销活动已手动停止。 您无法再激活或重复使用它。 [了解如何停止营销活动](modify-stop-campaign.md#stop)
* **[!UICONTROL Completed]**:营销活动已完成。 此状态在营销活动激活3天后自动分配，如果营销活动定期执行，则在营销活动结束日期自动分配。
* **[!UICONTROL Archived]**:营销活动已存档。 [了解如何存档营销活动](modify-stop-campaign.md#archive)

>[!NOTE]
>
>位于 **[!UICONTROL Live]** 或 **[!UICONTROL Scheduled]** 状态表示营销活动的新版本已创建且尚未激活。 [了解更多](modify-stop-campaign.md#modify).

## 修改定期营销活动 {#modify}

要修改和创建定期营销活动的新版本，请执行以下步骤：

1. 打开营销活动，然后单击 **[!UICONTROL Modify campaign]** 按钮。

1. 将创建营销活动的新版本。 您可以通过单击 **[!UICONTROL Open live version]**.

   ![](assets/create-campaign-draft.png)

   在营销活动列表中，正在进行草稿版本的激活的营销活动会在 **[!UICONTROL Status]** 列。 单击此图标可打开营销活动的草稿版本。

   ![](assets/create-campaign-edit-list.png)

1. 更改准备就绪后，您可以激活营销活动的新版本(请参阅 [查看和激活营销活动](create-campaign.md#review-activate))。

   >[!IMPORTANT]
   >
   >激活草稿将替换营销活动的实时版本。

## 停止定期促销活动 {#stop}

要停止定期促销活动，请将其打开，然后单击 **[!UICONTROL Stop campaign]** 按钮。

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>停止营销活动不会停止正在进行的发送，但会在发送已在进行时停止计划的发送或下一次发送。

<!-- inbound campaign (inapp): can stop and resume -->

## 复制营销活动 {#duplicate}

您可以复制实时营销活动以创建新营销活动。 要执行此操作，请打开营销活动，然后单击 **[!UICONTROL Duplicate]**.

![](assets/create-campaign-duplicate.png)

## 存档营销活动 {#archive}

随着时间的推移，营销活动列表会不断增长，最终会使浏览已完成和已停止的营销活动变得更加困难。

为防止出现这种情况，您可以存档不再需要的已完成和已停止的营销活动。 要执行此操作，请单击椭圆按钮，然后选择 **[!UICONTROL Archive]**.

![](assets/create-campaign-archive.png)

然后，可以使用列表中的专用过滤器来检索已存档的营销活动。 [了解如何访问营销活动](get-started-with-campaigns.md#access)
