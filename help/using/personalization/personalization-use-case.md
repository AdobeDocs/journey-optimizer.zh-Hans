---
title: 个性化用例
description: 个性化用例
translation-type: tm+mt
source-git-commit: 274086b4479a482ceb8e79e56d554f7d7b6cf545
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---


# 个性化用例{#personalization-use-case}

![](../assets/do-not-localize/badge.png)

在此用例中，您将在一条推送通知消息中了解如何使用多种类型的个性化。 将使用三种类型的个性化：

* 用户档案:基于用户档案字段的消息个性化
* 优惠决策：基于优惠决策变量的个性化
* 上下文：基于旅程中的情境数据的个性化

此示例的目标是在每次更新事件订单时将客户推送到Journey Optimizer。 随后向客户发送推送通知，其中包含订单信息和个性化优惠。

对于此用例，需要以下先决条件：

* 创建和设计推送通知消息，无需发布。 请参阅此[部分](../create-message.md)。
* 配置订单事件，包括订单编号、状态和物料名称。 请参阅此[部分](../event/about-events.md)。
* 创建决定(以前称为“优惠活动”)，请参阅此[部分](../offers/offer-activities/create-offer-activities.md)。

## 第1步 — 在用户档案上添加个性化

1. 单击&#x200B;**[!UICONTROL Message]**&#x200B;菜单，然后选择您的消息。

   ![](assets/perso-uc.png)

1. 单击&#x200B;**标题**&#x200B;字段。

   ![](assets/perso-uc2.png)

1. 在主题中键入内容并添加用户档案个性化。 使用搜索栏可查找用户档案的名字字段。 在主题文本中，将光标放在要插入个性化字段的位置，然后单击&#x200B;**+**&#x200B;图标。 单击&#x200B;**保存**。

   ![](assets/perso-uc3.png)

   >[!NOTE]
   >
   >留在草稿中。 请勿发布。

## 第2步 — 创建旅程

1. 单击&#x200B;**[!UICONTROL Journeys]**&#x200B;菜单并创建新旅程。

   ![](assets/perso-uc4.png)

1. 添加您的条目事件、**消息**&#x200B;和&#x200B;**结束**&#x200B;活动。

   ![](assets/perso-uc5.png)

1. 在&#x200B;**消息**&#x200B;活动中，选择之前创建的消息。 单击&#x200B;**确定**。

   ![](assets/perso-uc6.png)

   系统会显示一条消息，通知您已将登入事件数据和旅程属性传递给该消息。

   ![](assets/perso-uc7.png)

   >[!NOTE]
   >
   >此时将显示一条警告图标。 这是因为消息尚未发布。

## 第3步 — 在情境数据上添加个性化

1. 在&#x200B;**Message**&#x200B;活动中，单击&#x200B;**打开消息**&#x200B;图标。 消息将在新选项卡中打开。

   ![](assets/perso-uc8.png)

1. 单击&#x200B;**标题**&#x200B;字段。

   ![](assets/perso-uc9.png)

1. 选择&#x200B;**Context**&#x200B;类别。 此项目仅在旅程将情境数据传递到消息时才可用。 单击&#x200B;**Journey Orchestration**。 将显示以下上下文信息：

   * **事件**:此类别会重新对位于旅程中“消息”活动之前的事件中 **** 的所有字段进行分组。
   * **历程属性**:与给定用户档案的旅程相关的技术字段，例如旅程ID或遇到的特定错误。请参阅[Journey Orchestration文档](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/syntax/journey-properties.html#building-advanced-conditions-journeys)。

   ![](assets/perso-uc10.png)

1. 展开&#x200B;**事件**&#x200B;项，并查找与事件相关的订单编号字段。 您还可以使用搜索框。 单击&#x200B;**+**&#x200B;图标以在主题文本中插入个性化字段。 单击&#x200B;**保存**。

   ![](assets/perso-uc11.png)

1. 现在单击&#x200B;**Body**&#x200B;字段。

   ![](assets/perso-uc12.png)

1. 键入消息并插入&#x200B;**Context**&#x200B;类别中的订单项名称和订单进度。

   ![](assets/perso-uc13.png)

1. 从下拉列表中，选择&#x200B;**优惠决定**&#x200B;以插入offer decisioning变量。 选择放置位置并单击决定旁的&#x200B;**+**&#x200B;图标(以前称为“优惠活动”)，将其添加到正文中。

   ![](assets/perso-uc14.png)

1. 单击“validate”（验证）以确保没有错误，然后单击“**保存**”。

   ![](assets/perso-uc15.png)

1. 现在，发布消息。

   ![](assets/perso-uc16.png)

## 第4步 — 测试并发布旅程

1. 再次开启旅程。 如果旅程已打开，请确保刷新页面。 消息发布后，您会发现旅程中没有错误。 单击&#x200B;**Test**&#x200B;按钮，然后单击&#x200B;**触发事件**。

   ![](assets/perso-uc17.png)

1. 输入要在测试中传递的不同值。 测试模式仅适用于测试用户档案。 用户档案标识符需要与测试用户档案对应。 单击&#x200B;**发送**。

   ![](assets/perso-uc18.png)

   推送通知将发送并显示在测试用户档案的移动电话上。

   ![](assets/perso-uc19.png)

1. 确认没有错误并发布旅程。

