---
solution: Journey Optimizer
product: journey optimizer
title: 发布历程
description: 了解如何发布历程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 发布，历程，实时，有效性，检查
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 42%

---

# 发布您的历程 {#publishing-the-journey}

您必须发布历程以激活它，并使其可供新配置文件进入历程。 在发布历程之前，请验证其是否有效并且没有错误。 您无法发布包含错误的历程。

➡️ [通过观看视频了解此功能](#video)

## 发布过程 {#journey-publication}

发布历程的步骤详述如下：

1. 在发布历程之前，请验证其是否有效并且没有错误。 您无法发布包含错误的历程。

   * 了解如何在[此页面](testing-the-journey.md)上测试您的历程。
   * 在[本节](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)中了解如何解决您的旅程错误。

1. 要发布历程，请单击右上角下拉菜单中的&#x200B;**[!UICONTROL 发布]**&#x200B;选项。

   >[!NOTE]
   >
   > 如果您的历程受审批策略的约束，则必须请求审批以发布历程。 [了解详情](../test-approve/gs-approval.md)

   ![](assets/journeyuc1_18.png)

发布历程时，它处于&#x200B;**只读**&#x200B;模式。 在只读模式下，您只能修改活动标签和描述、历程名称和历程描述。 如果您需要对已发布的历程进行额外的修改，请创建历程的[新版本](journey-ui.md#journey-versions)。

当您停止历程时，历程将永久停止。 流经历程的所有个人将永久停止，并且历程将停止允许新条目。 如果您需要再次运行历程，请复制它并发布新历程。

>[!IMPORTANT]
>
>如果对历程消息中使用的优惠决策进行了更改，则需要取消发布该历程并重新发布。 这可确保将更改纳入历程的消息中，并且消息与最新更新一致。

## 历程版本 {#journey-versions}

在历程列表中，所有历程版本在显示时都带有版本号。搜索历程时，当应用程序首次打开时，最新版本会显示在列表顶部。然后，您可以定义所需的排序方式，应用程序会将其保留为用户首选项。历程的版本也显示在历程版本界面的顶部，位于画布上方。

![](assets/journeyversions1.png)

>[!NOTE]
>
>通常，对于历程的所有活动版本，同一历程中无法同时存在多个用户档案。 如果启用了重新进入，则用户档案可以重新进入历程，但只有在完全退出该历程的上一个实例后才能重新进入历程。[了解详情](entry-management.md)。

### 创建历程的新版本 {#journey-create-new-version}

如果您需要修改到实时历程，请创建历程的新版本。 要创建现有历程的新版本，请执行以下步骤：

1. 打开实时历程的最新版本，单击&#x200B;**[!UICONTROL 创建新版本]**&#x200B;并确认。

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能从历程的最新版本创建新版本。

1. 进行修改，单击&#x200B;**[!UICONTROL 发布]**&#x200B;并确认。

从历程发布的那一刻起，个人将开始转入历程的最新版本。已进入先前版本的用户将停留在该版本中，直到完成该历程。如果稍后重新进入同一历程，则将进入最新版本。

可以逐个单独停止历程版本。历程的所有版本具有相同的名称。

当您发布新版本的历程时，先前版本会自动结束并切换到&#x200B;**已关闭**&#x200B;状态。无法再进入该历程。即使您停止了最新版本，先前版本仍会保持关闭状态。


>[!NOTE]
>
>特定护栏和限制适用于历程的版本控制。 请参阅[此页面](../start/guardrails.md#journey-versions-journey-versions-g)以了解详情。


## 操作说明视频 {#video}

在此视频中了解如何发布历程：

>[!VIDEO](https://video.tv.adobe.com/v/3424998?quality=12)