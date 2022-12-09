---
title: 决策管理入门
description: 了解Adobe Journey Optimizer如何帮助您在适当的时间向客户发送适当的选件
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# 关于决策管理 {#about-decision-management}

使用 [!DNL Journey Optimizer] 以在适当的时间跨所有接触点为客户提供最佳选件和体验。 设计完成后，即可使用个性化优惠定位受众。

决策管理通过集中的营销选件库和决策引擎（该引擎将规则和约束应用于由Adobe Experience Platform创建的丰富实时用户档案，以帮助您在适当的时间向客户发送正确的选件），使个性化变得轻松。

决策管理功能包含两个主要组件：

* 的 **集中化优惠库** 在该界面中，您可以创建和管理构成选件的不同元素，并定义其规则和约束。
* 的 **优惠决策引擎** 它可利用Adobe Experience Platform数据和实时客户配置文件，以及选件库，以选择要将选件交付到的正确时间、客户和渠道。

![](../assets/architecture.png)

优点包括：

* 通过跨多个渠道提供个性化优惠，改进了营销活动效果，
* 改进了工作流：营销团队可以通过创建单个投放并更改模板不同部分的选件来改进工作流程，而不是创建多个投放或营销活动，
* 控制选件在营销活动和客户中显示的次数。

➡️ [在这些视频中了解有关决策管理的更多信息](#video)


>[!NOTE]
>
>如果您是 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target=&quot;_blank&quot;}用户正在利用 **Offer Decisioning** 应用程序服务中，本节中介绍的所有决策管理功能也适用于您。

## 关于优惠和决策 {#about-offers-and-decisions}

安 **选件** 由内容、资格规则和约束组成，这些规则和约束定义了向客户呈现资格的条件。

它是使用 **选件库**，提供了一个中央选件目录，您可以将资格规则和约束与多段内容关联以创建和发布选件(请参阅 [选件库用户界面](../get-started/user-interface.md))。

![](../assets/offer_structure.png)

使用选件扩充了选件库后，您可以将选件集成到 **决策**.

决策是选件的容器，将利用选件决策引擎以根据投放的目标选择要交付的最佳选件。

## 常见用例 {#common-use-cases}

通过决策管理功能和与Adobe Experience Platform的集成，您可以涵盖多个用例，以帮助您提高客户参与度和转化率。

* 根据Adobe Experience Platform中的数据，在您的网站主页上显示与访问客户的兴趣点匹配的选件。

   ![](../assets/website.png)

* 如果客户在您的某家商店附近走动，则会向他们发送推送通知，提醒他们可根据其属性（忠诚度、性别、以前的购买……）提供的优惠。

   ![](../assets/push_sample.png)

* 在联系您的支持团队时，决策管理还可帮助您增强客户的体验。 决策管理API允许您在呼叫中心座席的门户中显示有关客户已赎回和下一最佳优惠的信息。

   ![](../../assets/do-not-localize/call-center.png)

## 授予对决策管理的访问权限 {#granting-acess-to-decision-management}

访问和使用决策功能的权限可使用 [Adobe Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}。

要授予对决策管理功能的访问权限，您需要创建 **[!UICONTROL Product profile]** 并为用户分配相应的权限。 了解有关管理的更多信息 [!DNL Journey Optimizer] 用户和权限 [此部分](../../administration/permissions.md).

特定于决策管理的权限列在 [此部分](../../administration/high-low-permissions.md#decisions-permissions).

## 术语表 {#glossary}

您可以在下面找到使用决策管理时要使用的主要概念的列表。

* **上限** 或 **频度上限**:上限用作定义选件显示次数的约束。 有两种类型的上限，在合并的目标受众中可建议选件多少次（也称为“总上限”），以及可向同一最终用户（也称为“配置文件上限”）建议选件多少次。

* **收藏集**:收藏集是基于营销人员定义的预定义条件（如选件的类别）的选件子集。

* **决策**:决策包含通知选件选择的逻辑。

* **决策规则**:决策规则是添加到个性化选件并应用于用户档案以确定资格的限制。

* **合格选件**:符合条件的选件符合上游定义的限制，这些限制可以始终如一地提供给用户档案。

* **决策管理**:允许您使用业务逻辑和决策规则跨渠道和应用程序创建和提供最终用户个性化选件体验。

* **后备优惠**:备用选件是当最终用户不符合收藏集中任何个性化选件的资格时显示的默认选件。

* **选件**:选件是营销消息，其中可能包含与其关联的规则，以指定有资格查看选件的用户。

* **选件库**:选件库是一个中央库，用于管理个性化和回退选件、决策规则和决策。

* **个性化优惠**:个性化优惠是基于资格规则和限制的可自定义营销消息。

* **版面**:版面是指向最终用户显示选件的位置和上下文。

* **优先级**:优先级用于对满足所有限制（如资格、日历和上限）的选件进行排名。

* **表示**:表示法是指渠道使用的信息，如显示选件的位置或语言。

## 操作方法视频{#video}

>[!NOTE]
>
>这些视频适用于基于Adobe Experience Platform构建的Offer Decisioning应用程序服务，并且不特定于 [!DNL Adobe Journey Optimizer]. 但是，它们为在 [!DNL Journey Optimizer].

### 什么是决策管理？ {#what-is-offer-decisioning}

以下视频介绍了决策管理的关键功能、架构和用例：

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### 定义和管理选件 {#use-offer-decisioning}

以下视频演示了如何使用决策管理来定义和管理优惠并利用实时客户数据。

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


