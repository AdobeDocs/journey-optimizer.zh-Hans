---
solution: Journey Optimizer
product: journey optimizer
title: 修改或停止营销活动
description: 了解如何在Journey Optimizer中修改、停止或复制实时营销活动
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 管理营销活动、状态、计划、访问、优化器
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: b9630c922ff67b0a402af5f950ee4e5a442bb1b1
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 1%

---

# 管理活动 {#modify-stop-campaign}

活动激活后，您可以随时修改或停止它。 这些操作仅适用于具有定期执行的营销活动。

此外，您可以复制实时营销活动（执行一次或定期执行）以创建新营销活动，并存档已完成或停止的营销活动。

## 访问活动 {#access}

营销活动可从以下位置访问： **[!UICONTROL 营销活动]** 菜单。

默认情况下，列表会显示所有具有 **[!UICONTROL 草稿]**， **[!UICONTROL 已计划]**、和 **[!UICONTROL 实时]** 状态。 要显示已停止、已完成和已存档的营销活动，您需要清除过滤器。

![](assets/create-campaign-list.png)

此外，您可以根据营销活动类型和渠道，或根据创建营销活动时分配给营销活动的标记来过滤列表。 [了解如何为营销活动分配标记](create-campaign.md#create)

## 营销活动状态和警报 {#statuses}

营销活动可以具有多种状态：

* **[!UICONTROL 草稿]**：正在编辑营销活动，尚未激活它。
* **[!UICONTROL 激活]**：正在激活营销活动。
* **[!UICONTROL 正在处理]** *（仅限电子邮件营销活动）*：受众导出已完成，营销活动正在发布中。
* **[!UICONTROL 实时]**：营销活动已激活。
* **[!UICONTROL 已计划]**：将营销活动配置为在特定的开始日期激活。
* **[!UICONTROL 已停止]**：营销活动已手动停止。 您无法再激活或重用它。 [了解如何停止营销活动](modify-stop-campaign.md#stop)
* **[!UICONTROL 已完成]**：营销活动结束。 此状态在活动激活3天后自动分配，如果活动定期执行，则在活动结束日期分配。
* **[!UICONTROL 已存档]**：营销活动已存档。 [了解如何存档营销活动](modify-stop-campaign.md#archive)

>[!NOTE]
>
>旁边的“打开草稿版本”图标 **[!UICONTROL 实时]** 或 **[!UICONTROL 已计划]** 状态表示已创建营销活动的新版本，但尚未激活。 [了解详情](modify-stop-campaign.md#modify)。

当您的某个营销策划中发生错误时，该营销策划的状态旁边会显示一个警告图标。 单击该图标以显示有关警报的信息。 这些警报可能会在各种情况下发生，例如营销活动消息未发布或所选表面不正确时。

![](assets/campaign-alerts.png)

## 修改定期活动 {#modify}

要修改和创建定期活动的新版本，请执行以下步骤：

1. 打开活动，然后单击 **[!UICONTROL 修改营销活动]** 按钮。

1. 将创建营销活动的新版本。 您可以通过单击查看实时版本 **[!UICONTROL 打开实时版本]**.

   ![](assets/create-campaign-draft.png)

   在营销活动列表中，带有正在起草版本的激活营销活动在中带有特定图标 **[!UICONTROL 状态]** 列。 单击此图标以打开营销策划的草稿版本。

   ![](assets/create-campaign-edit-list.png)

1. 更改准备就绪后，您可以激活营销活动的新版本(请参阅 [查看和激活营销活动](create-campaign.md#review-activate))。

   >[!IMPORTANT]
   >
   >激活草稿将替换营销活动的实时版本。

## 停止定期活动 {#stop}

要停止定期营销活动，请将其打开，然后单击 **[!UICONTROL 停止营销活动]** 按钮。

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>停止营销活动不会停止正在进行的发送，但它将停止计划的发送，如果发送已经在进行，则会停止下一次发生。

<!-- inbound campaign (inapp): can stop and resume -->

## 复制营销活动 {#duplicate}

您可以复制实时营销活动以创建新营销活动。 为此，请打开营销策划，然后单击 **[!UICONTROL 复制]**.

![](assets/create-campaign-duplicate.png)

## 存档营销活动 {#archive}

随着时间的推移，促销活动列表不断增加，最终使浏览已完成和已停止的促销活动变得更加困难。

为防止出现这种情况，您可以存档不再需要的、已完成和已停止的营销活动。 为此，请单击省略号按钮，然后选择 **[!UICONTROL 存档]**.

![](assets/create-campaign-archive.png)

然后，可以使用列表中的专用过滤器检索已存档的营销活动。 [了解如何访问营销活动](get-started-with-campaigns.md#access)
