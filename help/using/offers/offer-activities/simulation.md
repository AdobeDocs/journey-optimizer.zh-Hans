---
title: 创建模拟
description: 了解如何创建模拟
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: null
source-git-commit: bad206b6c9b48241dbbd7758a331d602fac466b4
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# 创建模拟

## 关于模拟

要验证决策逻辑，您可以模拟哪些选件将交付到给定版面的测试用户档案。

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

这样，您就可以测试和优化各种版本的选件，而不会对目标收件人产生任何影响。

>[!NOTE]
>
>此功能模拟对 [!DNL Decisions] API。 了解详情 [使用决策API提供优惠](../api-reference/decisions-api/deliver-offers.md).

要访问此功能，请选择 **[!UICONTROL Simulation]** 选项卡 **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** 菜单。

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## 选择测试用户档案

首先，您需要选择要用于模拟的测试用户档案。

1. 单击 **[!UICONTROL Manage profile]**。

   ![](../../assets/offers_simulation-manage-profile.png)

1. 选择要用于标识测试用户档案的身份命名空间。 在本例中，我们将使用 **电子邮件** 命名空间。

   >[!NOTE]
   >
   >标识命名空间定义标识符的上下文，如电子邮件地址或CRM ID。 进一步了解Adobe Experience Platform身份命名空间 [在此部分中](../../get-started-identity.md){target=&quot;_blank&quot;}。

1. 输入标识值并单击 **[!UICONTROL View]** 列出可用的用户档案。

   ![](../../assets/offers_simulation-add-profile.png)

1. 如果要测试不同的用户档案数据，请添加其他用户档案，并保存您的选择。

   ![](../../assets/offers_simulation-save-profiles.png)

1. 添加后，所有用户档案都会列在 **[!UICONTROL Test profile]**. 您可以在保存的测试用户档案之间切换，以显示每个选定用户档案的结果。

   ![](../../assets/offers_simulation-saved-profiles.png)

1. 您可以单击 **[!UICONTROL Profile details]** 链接以显示所选的用户档案数据。

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## 添加决策作用域

现在，选择要在测试用户档案上模拟的选件决策。

1. 选择 **[!UICONTROL Add decision scope]**。

   ![](../../assets/offers_simulation-add-decision.png)

1. 从列表中选择版面。

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. 将显示可用的决策。

   * 您可以使用搜索字段来优化选择。
   * 您可以单击 **[!UICONTROL Open offer decisions]** 链接以打开您创建的所有决策的列表。 了解详情 [决策](create-offer-activities.md).

   选择您选择的决策并单击 **[!UICONTROL Add]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. 您刚刚定义的决策范围将显示在主工作区中。

   您可以调整要请求的选件数量。 例如，如果您选择2，则此决策范围将显示2个最佳选件。

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >您最多可以请求30个选件。

1. 重复上述步骤，以根据需要添加任意数量的决策。

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >即使您定义多个决策范围，也只会模拟一个API请求。
   >
   >默认情况下，所有重复数据消除标志都启用模拟功能，这意味着决策引擎允许重复数据，因此可以在多个决策中提出相同的建议。 了解 [!DNL Decisions] 中的API请求属性 [此部分](../api-reference/decisions-api/deliver-offers.md).

## 查看模拟结果

添加决策范围并选择测试用户档案后，即可查看结果。

1. 单击 **[!UICONTROL View results]**。

   ![](../../assets/offers_simulation-view-results.png)

1. 将根据为每个决策选择的用户档案显示最佳的可用选件。

   选择选件以显示其详细信息。

   ![](../../assets/offers_simulation-offer-details.png)

1. 从列表中选择其他用户档案以显示其他测试用户档案的选件决策结果。

1. 您可以根据需要多次添加、删除或更新决策范围。

>[!NOTE]
>
>每次更改用户档案或更新决策范围时，您都需要使用 **[!UICONTROL View results]** 按钮。

<!--Questions

* Is it recommended to first select profiles or first add decision scopes?
* What does Request offer changes?
* Nothing displays when I click View results? Can't see any score...
* What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
* What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
* Is there a way to create relevant test profiles?
* Error on Profile details link.
* Is there a tutorial planned to be released?
* Why still a big red frame when no profile is found?

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->