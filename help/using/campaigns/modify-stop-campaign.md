---
solution: Journey Optimizer
product: journey optimizer
title: 修改或停止营销活动
description: 了解如何在Journey Optimizer中修改、停止或复制实时营销活动
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 管理营销活动、状态、计划、访问、优化器
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---

# 管理活动 {#modify-stop-campaign}

活动激活后，您可以随时修改或停止它。 这些操作仅适用于具有定期执行的营销活动。

此外，您可以复制实时营销活动（执行一次或循环执行）以创建新营销活动，并存档已完成或停止的营销活动。

## 访问活动 {#access}

营销活动可从以下网址访问： **[!UICONTROL 营销活动]** 菜单。

默认情况下，列表会显示所有促销活动，其中 **[!UICONTROL 草稿]**， **[!UICONTROL 已计划]**、和 **[!UICONTROL 实时]** 状态。 要显示已停止、已完成和已存档的营销活动，您需要清除过滤器。

![](assets/create-campaign-list.png)

此外，您可以根据促销活动类型和渠道，或根据创建促销活动时分配给促销活动的标记来筛选列表。 [了解如何将标记分配给活动](create-campaign.md#create)

## 营销活动状态 {#statuses}

营销活动可以具有多种状态：

* **[!UICONTROL 草稿]**：正在编辑营销活动，尚未激活它。
* **[!UICONTROL 激活]**：正在激活营销活动。
* **[!UICONTROL 实时]**：营销活动已激活。
* **[!UICONTROL 已计划]**：营销活动配置为在特定的开始日期激活。
* **[!UICONTROL 已停止]**：营销活动已手动停止。 您无法再激活或重用它。 [了解如何停止营销活动](modify-stop-campaign.md#stop)
* **[!UICONTROL 已完成]**：营销活动结束。 此状态在营销活动激活3天后自动分配，如果活动定期执行，则在营销活动结束日期分配。
* **[!UICONTROL 已存档]**：营销活动已存档。 [了解如何存档活动](modify-stop-campaign.md#archive)

>[!NOTE]
>
>旁边的“打开草稿版本”图标 **[!UICONTROL 实时]** 或 **[!UICONTROL 已计划]** 状态表示已创建新版本的营销活动，但尚未激活。 [了解详情](modify-stop-campaign.md#modify)。

## 修改定期活动 {#modify}

要修改和创建循环活动的新版本，请执行以下步骤：

1. 打开营销策划，然后单击 **[!UICONTROL 修改营销活动]** 按钮。

1. 将创建营销活动的新版本。 您可以通过单击来检查实时版本 **[!UICONTROL 打开实时版本]**.

   ![](assets/create-campaign-draft.png)

   在营销活动列表中，带有正在起草版本的已激活营销活动在中带有特定图标 **[!UICONTROL 状态]** 列。 单击此图标以打开营销策划的草稿版本。

   ![](assets/create-campaign-edit-list.png)

1. 在更改准备就绪后，您可以激活营销活动的新版本(请参阅 [查看并激活营销活动](create-campaign.md#review-activate))。

   >[!IMPORTANT]
   >
   >激活草稿将替换营销活动的实时版本。

## 停止定期活动 {#stop}

要停止定期营销活动，请将其打开，然后单击 **[!UICONTROL 停止营销活动]** 按钮。

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>停止营销活动不会停止正在进行的发送，但它将停止计划的发送，如果发送已经在进行，则停止下一次发送。

<!-- inbound campaign (inapp): can stop and resume -->

## 复制营销活动 {#duplicate}

您可以复制实时营销活动以创建新营销活动。 为此，请打开营销策划，然后单击 **[!UICONTROL 复制]**.

![](assets/create-campaign-duplicate.png)

## 存档营销活动 {#archive}

随着时间的推移，促销活动列表不断增加，最终使浏览已完成和已停止的促销活动变得更加困难。

要防止出现这种情况，您可以存档您不再需要的已完成和已停止的营销活动。 为此，请单击省略号按钮，然后选择 **[!UICONTROL 存档]**.

![](assets/create-campaign-archive.png)

然后，可以使用列表中的专用过滤器检索已存档的营销活动。 [了解如何访问营销活动](get-started-with-campaigns.md#access)
