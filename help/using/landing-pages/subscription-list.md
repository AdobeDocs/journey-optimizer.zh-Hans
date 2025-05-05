---
solution: Journey Optimizer
product: journey optimizer
title: 创建订阅列表
description: 了解如何在Journey Optimizer中设置订阅列表
feature: Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: 登录，登陆页面，列表，订阅，服务
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: c66fe22f0cf81cf8e14592df1433739735afbe43
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 7%

---

# 订阅列表 {#create-subscription-list}

>[!CONTEXTUALHELP]
>id="ajo_subscription_list"
>title="设置订阅列表"
>abstract="创建订阅列表，用于收集已选择接收特定主题或事件通信的轮廓。 "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/subscription-list.html?lang=zh-Hans#define-subscription-list" text="创建订阅列表"

订阅服务是指向选择接收有关特定主题/事件/兴趣/等的通信的客户提供的营销商品和服务。 持续进行。 在[!DNL Journey Optimizer]中，这些选择加入的客户被收集到订阅列表中。

订阅服务可用于：

* 新闻稿，例如：“Running series”
* 例如，活动：“Summit 2021”
* 网络研讨会，例如：“了解有关加密编译的更多信息”
* 对特定产品/运动/服务/等的兴趣，例如：“有兴趣在未来12个月内购买房屋”
* 关于通知方式的首选项，例如：“通过电子邮件接收新歌曲通知”

可以通过[登陆页面](create-lp.md)将配置文件添加到订阅列表。 [此部分](lp-use-cases.md#subscription-to-a-service)中提供了一个示例。

## 创建订阅列表 {#define-subscription-list}

要创建订阅列表，请执行以下步骤。

1. 要访问订阅列表，请选择&#x200B;**[!UICONTROL 客户]** > **[!UICONTROL 订阅列表]**。

   ![](assets/lp_subscription-lists.png)

1. 选择&#x200B;**[!UICONTROL 创建订阅列表]**&#x200B;按钮。

   ![](assets/lp_create-subscription-list.png)

1. 添加标题和描述。 这些字段为必填字段。

   ![](assets/lp_subscription-list-name.png)

   >[!CAUTION]
   >
   >当前不能在&#x200B;**[!UICONTROL 标题]**&#x200B;字段中为其他订阅列表使用空格或输入已存在的名称。

1. 您可以定义开始日期和结束日期。

   ![](assets/lp_subscription-list-dates.png)

1. 从&#x200B;**[!UICONTROL 标记]**&#x200B;字段中选择或创建Adobe Experience Platform标记以对您的登陆页面进行分类，从而改进搜索。 [了解详情](../start/search-filter-categorize.md#tags)

1. 单击&#x200B;**[!UICONTROL 保存]**。

## 使用订阅列表 {#use-subscription-lists}

创建订阅列表后，您可以：

* 将配置文件添加到订阅列表

  您可以通过订阅新闻稿或注册活动来邀请人员&#x200B;**加入列表**。 您也可以&#x200B;**向订阅者发送个性化邮件**。

  例如，要邀请受众注册事件或订阅新闻稿，您可以向他们发送消息，其中包含指向登陆页面的链接，以便他们加入事件或订阅。 通过登陆页面表单选择加入的用户档案会添加到您为此目的创建的订阅列表中。

* 向订阅者发送消息

  在构建历程和添加个性化时，您还可以使用订阅列表作为受众。

  例如，当客户订阅流服务时，它可以触发立即发送欢迎电子邮件系列，鼓励他们首次登录应用程序并设置查看首选项。

在[此用例](lp-use-cases.md#subscription-to-a-service)中了解如何使用您的订阅列表。


## 浏览您的订阅列表 {#browse-subscription-lists}

该列表显示了创建的所有订阅列表。 您可以根据创建日期或修改日期及其状态筛选它们。

![](assets/lp_subscription-filters.png)

可能的状态如下：

* **[!UICONTROL 未开始]**：您定义的开始日期晚于当前日期。 订阅的用户档案将尚未收到与此订阅列表相关的通信。
* **[!UICONTROL 实时]**：当天包含在订阅列表开始日期和结束日期之间，或者您未定义结束/开始日期，这意味着订阅列表始终实时。
* **[!UICONTROL 已过期]**：已超过结束日期，因此订阅列表不再有效。 任何订阅的配置文件都不会再收到与此订阅列表相关的任何通信。


## 监测您的订阅列表 {#monitor-subscription-lists}

您可以通过专用报告监控订阅列表的影响。 您可以访问两种类型的报表：

* 订阅列表实时报告

  实时报告可从“最近24小时”选项卡访问，它显示过去24小时内发生的事件，最小时间间隔为距事件发生两分钟。 [了解详情](../reports/subscription-report-live.md)

* 订阅列表所有时间报表，带Customer Journey Analytics

  这些报表重点关注至少两小时前发生的事件，并涵盖选定时间段内的事件。 **订阅报告**&#x200B;提供了与特定列表关联的用户档案订阅和退订的基本见解，可帮助您了解不同的订阅活动和计划对于提高参与度和转化率的有效性。 [了解详情](../reports/subscription-report-global-cja.md)
