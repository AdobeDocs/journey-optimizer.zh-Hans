---
title: 决策管理入门
description: 了解 Adobe Journey Optimizer 如何帮助您在适合的时间向客户发送合适的优惠
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: 2acb883b66e5da9c06ba1551f708bb8ab47ce343
workflow-type: ht
source-wordcount: '896'
ht-degree: 100%

---

# 决策管理入门 {#about-decision-management}

使用 [!DNL Journey Optimizer] 可在适当的时候将优质的产品和体验提供给所有接触点上的客户。设计完成后，将个性化的优惠锁定至您的受众。

决策管理通过集中的营销优惠库和决策引擎（该引擎可将规则和约束应用于 Adobe Experience Platform 创建的丰富实时轮廓）帮助您在适当的时间向客户发送合适的优惠，从而轻松实现个性化。

“决策管理”功能由两个主要组件组成：

* **集中式优惠库**&#x200B;是创建和管理组成优惠的不同元素并定义其规则和限制条件的界面。
* **优惠决策引擎**&#x200B;利用 Adobe Experience Platform 数据、实时客户轮廓和优惠库选择合适的时间、客户和渠道，以便向其提供优惠。

![](../assets/architecture.png)

其优势包括：

* 通过跨多个渠道提供个性化优惠而提升的营销活动效果，
* 改进的工作流程：营销团队可以通过创建单个投放并更改模板中不同部分的优惠来改进工作流程，而无需创建多个投放或活动，
* 控制优惠在营销活动和客户中显示的次数。

➡️ [通过这些视频了解有关决策管理的更多信息](#video)

>[!NOTE]
>
>如果您是 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=zh-Hans){target="_blank"} 用户并使用 **Offer Decisioning** 应用程序，则本节中介绍的所有决策管理功能也适合您。

## 关于优惠和决策 {#about-offers-and-decisions}

**优惠**&#x200B;由内容、合格规则和限制条件（确定向客户呈现该优惠的条件）组成。

它是使用&#x200B;**优惠库**&#x200B;创建的，这个库提供了一个集中式优惠目录，您可以将合格规则和限制条件与多个内容关联，以创建和发布优惠（请参阅[优惠库用户界面](../get-started/user-interface.md)）。

![](../assets/offer_structure.png)

在优惠库中添加优惠后，您可以将优惠整合到&#x200B;**决策**&#x200B;中。

决策是优惠的容器，它们将利用优惠决策引擎，以便根据投放目标来选择应投放的最合适的优惠。

## 常见使用案例 {#common-use-cases}

决策管理功能以及与 Adobe Experience Platform 的集成使您能够覆盖诸多使用案例，从而帮助您提高客户的参与度和转化率。

* 根据来自 Adobe Experience Platform 的数据，在您的网站主页上显示与来访客户的兴趣点相匹配的优惠。

  ![](../assets/website.png)

* 如果客户走到您的商店附近，根据他们的属性（忠诚度、性别、以前的购买记录等）向他们发送推送通知，提醒他们有可用的优惠。

  ![](../assets/push_sample.png)

* 决策管理还可帮助您提升客户在联系支持团队时的体验。决策管理 API 允许您在呼叫中心服务人员的门户中显示有关客户已兑现的优惠和下个最合适优惠的信息。

  ![](../../assets/do-not-localize/call-center.png)

## 授予对决策管理的访问权限 {#granting-acess-to-decision-management}

使用 [Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/managing/user-guide.html){target="_blank"} 管理访问和使用决策功能的权限。

要授予对决策管理功能的访问权限，您需要创建&#x200B;**[!UICONTROL 产品轮廓]**&#x200B;并为用户分配相应的权限。在[本节](../../administration/permissions.md)中了解更多关于管理 [!DNL Journey Optimizer] 用户和权限的信息。

[本节](../../administration/high-low-permissions.md#decisions-permissions)中列出了特定于决策管理的权限。

## 术语表 {#glossary}

您可以在下方找到使用决策管理时会用到的主要概念的列表。

* **上限**&#x200B;或&#x200B;**频率上限**：上限是用于定义优惠提供次数的限制。有两种类型的上限：在合并目标受众中可以提供多少次优惠（也称为“总上限”）；以及向同一最终用户提供优惠的次数（也称为“轮廓上限”）。

* **集合**：集合是指营销人员定义的预定义条件中的优惠子集，如优惠类别。

* **决策**：决策包含通知优惠选择的逻辑。

* **决策规则**：决策规则是添加到个性化优惠并应用于轮廓以确定资格的限制。

* **符合条件的优惠**：符合条件的优惠符合上游定义的限制，可以持续提供给轮廓。

* **决策管理**：您可以通过多个渠道，也可以通过使用了业务逻辑和决策规则的应用程序，来为最终用户创建和提供个性化的优惠体验。

* **后备优惠**：后备优惠是当最终用户没有资格获得集合中的任何个性化优惠时显示的默认优惠。

* **优惠**：优惠是营销消息，其中可能包含与其关联的规则，这些规则用于指定有资格查看优惠的人员。

* **优惠库**：优惠库是用于管理个性化和备用优惠、决策规则和决策的中央库。

* **个性化优惠**：个性化优惠是基于合格规则和约束的可定制营销消息。

* **投放位置**：投放位置是为最终用户显示优惠的位置和/或上下文。

* **优先级**：优先级用于对满足所有约束（如资格、日历和上限）的优惠进行排序。

* **呈现**：呈现是渠道使用的信息，如用于显示优惠的位置或语言。

## 操作说明视频{#video}

### 什么是决策管理？ {#what-is-offer-decisioning}

以下视频介绍了决策管理的关键功能、架构和使用案例：

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### 定义和管理优惠 {#use-offer-decisioning}

以下视频介绍了如何使用决策管理来定义和管理优惠，以及如何利用实时客户数据。

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


