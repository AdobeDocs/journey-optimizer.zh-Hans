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
source-git-commit: 1ad534b7877f0ac6c1f50e29f41af708e83b34c9
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 5%

---

# 管理活动 {#modify-stop-campaign}

活动激活后，您可以随时修改或停止它。 这些操作仅适用于具有定期执行的营销活动。

此外，您可以复制实时营销活动（执行一次或定期执行）以创建新营销活动，并存档已完成或停止的营销活动。

## 访问营销活动 {#access}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_view"
>title="营销活动列表和日程表视图"
>abstract="除了营销活动列表之外，[!DNL Journey Optimizer] 还提供营销活动的日程表视图，清晰展示营销活动的日程安排。您可以随时使用这些按钮在列表和日程表视图之间切换。"

可从&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单访问营销活动。

默认情况下，列表会显示具有&#x200B;**[!UICONTROL 草稿]**、**[!UICONTROL 计划]**&#x200B;和&#x200B;**[!UICONTROL 实时]**&#x200B;状态的所有营销活动。 要显示已停止、已完成和已存档的营销活动，您需要清除过滤器。

![](assets/create-campaign-list.png)

您还可以根据营销活动类型和渠道或创建时分配给营销活动的标记来过滤列表。 [了解如何为营销活动分配标记](create-campaign.md#create)

## 营销活动日历 {#calendar}

除了营销活动列表之外，[!DNL Journey Optimizer]还提供营销活动的日历视图，以直观的方式清晰地展示其计划。

>[!AVAILABILITY]
>
>日历视图当前仅适用于一组组织（限量发布）。 若要请求访问权限，请使用[此表单](https://forms.cloud.microsoft/r/FC49afuJVi){target=”_blank”}。
>
>此功能正在开发中。 我们欢迎您使用顶部菜单中的&#x200B;**[!UICONTROL Beta反馈]**&#x200B;按钮输入和请求。

日历显示本周安排的所有营销活动。 使用日历上方的箭头按钮在周之间导航。

![日历视图显示实时营销活动](assets/campaigns-timeline.png)

营销活动的表示方式：

* 默认情况下，日历网格会显示选定周的所有实时营销活动和计划营销活动。 其他筛选器选项可以显示已完成、已停止和已完成的激活或特定类型或渠道的激活。
* 不显示草稿营销活动。
* 跨越多天的营销活动显示在日历网格的顶部。
* 如果未指定开始时间，则使用最接近的手动激活时间将其放置在日历中。
* 营销活动显示为1小时时间跨度，但这并不反映实际的发送或完成时间。

有关营销活动的更多详细信息，请单击其可视块以打开相关详细信息。

要查看特定营销活动的详细信息，请从列表中选择该营销活动。 此时将打开一个信息窗格，其中包含有关营销活动的各种信息，例如其类型、对报告的访问权限或已分配的标记。

![打开了信息窗格的campaign列表](assets/campaign-rail.png)

## 营销活动状态和警报 {#statuses}

营销活动可以具有多种状态：

* **[!UICONTROL 草稿]**：正在编辑营销活动，尚未激活它。
* **[!UICONTROL 正在激活]**：正在激活营销活动。
* **[!UICONTROL 正在处理]** *（仅限电子邮件营销活动）*：受众导出已完成，正在发布营销活动。
* **[!UICONTROL 实时]**：营销活动已激活。
* **[!UICONTROL 已计划]**：营销活动配置为在特定开始日期激活。
* **[!UICONTROL 已停止]**：营销活动已手动停止。 您无法再激活或重用它。 [了解如何停止营销活动](modify-stop-campaign.md#stop)
* **[!UICONTROL 已完成]**：营销活动已完成。 此状态在活动激活3天后自动分配，如果活动定期执行，则在活动结束日期分配。
* **[!UICONTROL 已存档]**：营销活动已存档。 [了解如何存档营销活动](modify-stop-campaign.md#archive)

>[!NOTE]
>
>**[!UICONTROL 实时]**&#x200B;或&#x200B;**[!UICONTROL 已计划]**&#x200B;状态旁边的“打开草稿版本”图标指示营销活动的新版本已创建且尚未激活。 [了解详情](modify-stop-campaign.md#modify)。

当您的某个营销策划中发生错误时，该营销策划的状态旁边会显示一个警告图标。 单击该图标以显示有关警报的信息。 这些警报可能会在各种情况下发生，例如营销活动消息未发布或所选配置不正确时。

![](assets/campaign-alerts.png)

## 修改定期活动 {#modify}

要修改和创建定期活动的新版本，请执行以下步骤：

1. 打开营销活动，然后单击&#x200B;**[!UICONTROL 修改营销活动]**&#x200B;按钮。

1. 将创建营销活动的新版本。 您可以通过单击&#x200B;**[!UICONTROL 打开实时版本]**&#x200B;来检查实时版本。

   ![](assets/create-campaign-draft.png)

   在营销活动列表中，带有正在起草版本的激活营销活动在&#x200B;**[!UICONTROL 状态]**&#x200B;列中显示为带有特定图标。 单击此图标以打开营销策划的草稿版本。

   ![](assets/create-campaign-edit-list.png)

1. 更改准备就绪后，您可以激活营销活动的新版本（请参阅[查看和激活营销活动](create-campaign.md#review-activate)）。

   >[!IMPORTANT]
   >
   >激活草稿将替换营销活动的实时版本。

## 停止定期活动 {#stop}

要停止定期营销活动，请将其打开，然后单击&#x200B;**[!UICONTROL 停止营销活动]**&#x200B;按钮。

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>停止营销活动不会停止正在进行的发送，但它将停止计划的发送，如果发送已经在进行，则会停止下一次发生次数。

<!-- inbound campaign (inapp): can stop and resume -->

## 复制营销活动 {#duplicate}

您可以复制实时营销活动以创建新营销活动。 为此，请打开营销活动，然后单击&#x200B;**[!UICONTROL 复制]**。

![](assets/create-campaign-duplicate.png)

## 存档营销活动 {#archive}

随着时间的推移，促销活动列表不断增加，最终使浏览已完成和已停止的促销活动变得更加困难。

为防止出现这种情况，您可以存档不再需要的、已完成和已停止的营销活动。 为此，请单击省略号按钮，然后选择&#x200B;**[!UICONTROL 存档]**。

![](assets/create-campaign-archive.png)

然后，可以使用列表中的专用过滤器检索已存档的营销活动。 [了解如何访问营销活动](get-started-with-campaigns.md#access)
