---
solution: Journey Optimizer
product: journey optimizer
title: 添加个性化优惠
description: 了解如何向消息添加个性化优惠
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 优惠、决策、电子邮件、个性化、决策
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 1%

---

# 添加个性化优惠 {#deliver-personalized-offers}

In [!DNL Journey Optimizer] 在电子邮件中，您可以插入将利用决策管理引擎的决策，以便选择向客户提供的最佳优惠。

例如，您可以添加一个决策，该决策将在您的电子邮件中显示一个特殊的折扣优惠，该优惠将因收件人的忠诚度级别而异。

>[!IMPORTANT]
>
>如果对历程消息中使用的优惠决策进行了更改，则需要取消发布历程并重新发布它。  这将确保将更改纳入历程的消息中，并且消息与最新更新一致。

* 有关如何创建和管理优惠的更多信息，请参阅 [本节](../offers/get-started/starting-offer-decisioning.md).
* 对于 **完整的端到端示例** 显示如何配置优惠、在决策中使用优惠以及在电子邮件中利用此决策、签出 [本节](../offers/offers-e2e.md#insert-decision-in-email).

➡️ [在此视频中了解如何添加优惠作为个性化](#video-offers)

## 在电子邮件中插入决策 {#insert-offers}

>[!CAUTION]
>
>在开始之前，您必须 [定义优惠决策](../offers/offer-activities/create-offer-activities.md).

要在电子邮件中插入决策，请执行以下步骤：

1. 创建电子邮件，然后打开Email Designer以配置其内容。

1. 添加 **[!UICONTROL 优惠决策]** 内容组件。

   ![](assets/deliver-offer-component.png)

   了解如何在中使用内容组件 [本节](content-components.md).

1. 此 **[!UICONTROL 优惠决策]** 选项卡显示在右侧面板中。 单击 **[!UICONTROL 选择优惠决策]**：

   1. 在显示的窗口中，选择与要显示的选件对应的版面。

      [版面](../offers/offer-library/creating-placements.md) 是用于展示优惠的容器。 在本例中，我们将使用“电子邮件顶部图像”投放位置。 此版面已在选件库中创建，用于显示位于消息顶部的图像类型选件。

   1. 将显示与所选投放位置匹配的决策。 选择要在内容组件中使用的决策，然后单击 **[!UICONTROL 添加]**.

      >[!NOTE]
      >
      >列表中仅显示与所选投放位置兼容的决策。 在此示例中，只有一个选件活动与“电子邮件顶部图像”投放位置匹配。

      ![](assets/deliver-offer-placement.png)

决策现已添加到组件中。 保存更改后，在历程中发送消息时，您的优惠可随时显示给相关用户档案。

>[!NOTE]
>
>当您更新消息中直接或间接引用的优惠、后备优惠、优惠收藏集或优惠决策时，更新会自动反映在相应的消息中。

## 在电子邮件中预览优惠 {#preview-offers-in-email}

您可以使用预览作为添加到电子邮件决策一部分的不同优惠 **[!UICONTROL 选件]** 部分或内容组件箭头。

![](assets/deliver-offer-preview.png)

要在客户配置文件中显示作为决策一部分的不同优惠，请执行以下步骤。

>[!NOTE]
>
>您需要具有测试用户档案才能预览消息。 了解如何 [创建测试用户档案](../audience/creating-test-profiles.md).

1. 选择要用于预览选件的测试配置文件：

   1. 单击 **[!UICONTROL “模拟内容”按钮]** 按钮，然后选择命名空间以从中标识测试用户档案 **[!UICONTROL 身份命名空间]** 字段。

      >[!NOTE]
      >
      >在此示例中，我们使用 **电子邮件** 命名空间。 了解有关Adobe Experience Platform身份命名空间的更多信息 [在此部分中](../audience/get-started-identity.md).

   1. 在 **[!UICONTROL 标识值]** 字段中，输入用于标识测试用户档案的值。 在此示例中，输入测试用户档案的电子邮件地址。

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

   1. 添加其他用户档案，以便根据用户档案数据测试消息的不同变体。

      ![](assets/deliver-offer-test-profiles.png)

1. 单击 **[!UICONTROL 预览]** 选项卡，测试您的消息，然后选择测试用户档案。 将显示与所选用户档案（女性）对应的优惠。

   ![](assets/deliver-offer-test-profile-female-preview.png)

   您可以选择其他测试用户档案来预览消息每个变体的电子邮件内容。 在消息内容中，将显示与选定测试用户档案（现为男性）对应的选件。

详细了解在中查看消息预览的详细步骤 [本节](#preview-your-messages).

## 操作方法视频{#video-offers}

了解如何在中向消息添加决策管理组件 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
