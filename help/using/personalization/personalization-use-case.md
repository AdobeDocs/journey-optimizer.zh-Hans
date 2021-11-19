---
title: 个性化用例&冒号；订单状态通知
description: 了解如何使用用户档案、选件决策和上下文信息对消息进行个性化
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: daf5c6021a3efc8852b989fb602380c369758ead
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---

# 个性化用例：订单状态通知 {#personalization-use-case}

在此用例中，您将看到如何在单个推送通知消息中使用多种类型的个性化。 将使用三种类型的个性化：

* **用户档案**:基于用户档案字段的消息个性化
* **优惠决策**:基于offer decisioning变量进行个性化
* **上下文**:基于历程中的情境数据进行个性化

此示例的目标是将事件推送到 [!DNL Journey Optimizer] 每次更新客户订单时。 随后，系统会向客户发送推送通知，其中包含有关订单的信息和个性化优惠。

对于此用例，需要满足以下先决条件：

* 创建和设计推送通知消息，而不发布。 请参阅 [部分](../create-message.md).
* 配置订单事件，包括订单编号、状态和物料名称。 请参阅 [部分](../event/about-events.md).
* 创建决策（以前称为“选件活动”），请参阅 [部分](../offers/offer-activities/create-offer-activities.md).

## 第1步 — 在用户档案中添加个性化

1. 单击 **[!UICONTROL Message]** ，然后选择您的消息。

   ![](assets/perso-uc.png)

1. 单击 **标题** 字段。

   ![](assets/perso-uc2.png)

1. 键入主题并添加个性化用户档案。 使用搜索栏查找用户档案的名字字段。 在主题文本中，将光标放在要插入个性化字段的位置，然后单击 **+** 图标。 单击&#x200B;**保存**。

   ![](assets/perso-uc3.png)

   >[!NOTE]
   >
   >留言稿。 尚未发布。

## 第2步 — 创建历程

1. 单击 **[!UICONTROL Journeys]** 菜单，并创建新历程。

   ![](assets/perso-uc4.png)

1. 添加您的登入事件， **消息** 和 **结束** 活动。

   ![](assets/perso-uc5.png)

1. 在 **消息** 活动，选择之前创建的消息。 单击 **确定**.

   ![](assets/perso-uc6.png)

   将显示一条消息，通知您条目事件数据和历程属性已传递到消息。

   ![](assets/perso-uc7.png)

   >[!NOTE]
   >
   >此时将显示一条警告图标的消息。 这是因为消息尚未发布。

## 步骤3 — 基于上下文数据添加个性化

1. 从 **消息** 活动，单击 **打开消息** 图标。 此时将在新选项卡中打开消息。

   ![](assets/perso-uc8.png)

1. 单击 **标题** 字段。

   ![](assets/perso-uc9.png)

1. 选择 **上下文** 类别。 仅当历程将上下文数据传递到消息时，此项目才可用。 单击 **Journey Orchestration**. 将显示以下上下文信息：

   * **事件**:此类别会重组置于之前事件的所有字段 **消息** 活动。
   * **历程属性**:与给定用户档案的历程相关的技术字段，例如历程ID或遇到的特定错误。 在 [Journey Orchestration文档](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. 展开 **事件** ，并查找与事件相关的订单编号字段。 您还可以使用搜索框。 单击 **+** 图标，以在主题文本中插入个性化字段。 单击&#x200B;**保存**。

   ![](assets/perso-uc11.png)

1. 现在，单击 **正文** 字段。

   ![](assets/perso-uc12.png)

1. 键入消息并插入，从 **上下文** 类别、订单项目名称和订单进度。

   ![](assets/perso-uc13.png)

1. 从下拉菜单中，选择 **优惠决策** 插入offer decisioning变量。 选择版面并单击 **+** 图标（以前称为“选件活动”），将其添加到主体中。

   ![](assets/perso-uc14.png)

1. 单击“验证”以确保没有错误，然后单击 **保存**.

   ![](assets/perso-uc15.png)

1. 现在，发布消息。

   ![](assets/perso-uc16.png)

## 第4步 — 测试和发布历程

1. 再次打开历程。 如果历程已打开，请确保刷新页面。 现在，消息已发布，您可以看到历程中没有错误。 单击 **测试** 按钮，然后单击 **触发事件**.

   ![](assets/perso-uc17.png)

1. 输入测试中要传递的不同值。 测试模式仅适用于测试用户档案。 用户档案标识符需要与测试用户档案对应。 单击 **发送**.

   ![](assets/perso-uc18.png)

   推送通知将发送并显示在测试用户档案的手机上。

   ![](assets/perso-uc19.png)

1. 确认没有错误并发布历程。
