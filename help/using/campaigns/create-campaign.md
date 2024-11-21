---
solution: Journey Optimizer
product: journey optimizer
title: 创建营销活动
description: 了解如何在Journey Optimizer中创建营销活动
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 创建，优化器，营销活动，界面，消息
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: f9f2cd339680d0dbff1812e64c5082ca97a34771
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 19%

---

# 创建营销活动 {#create-campaign}

要创建新营销活动，请访问&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。 您还可以复制现有的实时营销活动以创建新营销活动。 [了解详情](modify-stop-campaign.md#duplicate)

>[!NOTE]
>
>在创建新营销活动之前，请确保您具有可供使用的渠道配置（即消息平面）和Adobe Experience Platform受众。 请参阅以下部分以了解详情：
>
>* [创建渠道配置](../configuration/channel-surfaces.md)
>* [开始使用受众](../audience/about-audiences.md)

## 选择营销活动类型 {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="营销活动类型"
>abstract="立即执行或在指定日期执行&#x200B;**计划的营销活动**，其旨在发送市场营销类型的消息。使用 API 调用执行 **API 触发的**&#x200B;活动。它们旨在发送营销性消息（需要用户同意的推广消息）或交易型消息（非商业消息，在特定上下文中，也可以发送到未订阅的轮廓）。"

1. 选择要执行的营销活动类型

   * **[!UICONTROL 已计划 — 营销]**：立即或在指定日期执行营销活动。 计划的营销活动旨在发送&#x200B;**营销**&#x200B;消息。 它们从用户界面配置和执行。

   * **[!UICONTROL API触发 — 营销/事务性]**：使用API调用执行营销活动。 API触发的营销活动旨在发送&#x200B;**营销**&#x200B;或&#x200B;**事务性**&#x200B;消息，即，在个人执行的操作（密码重置、购物车购买等）之后发送的消息。 [了解如何使用API触发营销活动](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;以创建营销活动。

## 定义营销活动属性 {#create}

1. 在&#x200B;**[!UICONTROL 属性]**&#x200B;部分中，输入营销策划的名称和描述。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. 使用&#x200B;**标记**&#x200B;字段将Adobe Experience Platform统一标记分配给您的营销活动。 这样，您就可以轻松地对营销活动进行分类，并改进营销活动列表中的搜索。[了解如何使用标记](../start/search-filter-categorize.md#tags)。

1. 您可以根据访问标签限制对此营销活动的访问。 要添加访问限制，请浏览至此页顶部的&#x200B;**[!UICONTROL 管理访问]**&#x200B;按钮。 确保仅选择您具有权限的标签。 [了解有关对象级访问控制的更多信息](../administration/object-based-access.md)。

## 定义活动受众 {#audience}

受众是指一组具有相似行为和/或特征的人员。 要定义营销活动定向的群体，请执行以下步骤：

1. 在&#x200B;**受众**&#x200B;部分中，单击&#x200B;**[!UICONTROL 选择受众]**&#x200B;按钮以显示可用Adobe Experience Platform受众列表。 在[本节](../audience/about-audiences.md)中了解有关受众的更多信息。

1. 在&#x200B;**[!UICONTROL 标识类型]**&#x200B;字段中，选择要用于标识选定受众中个人的密钥类型。 您可以使用现有的身份类型或使用Adobe Experience Platform Identity服务创建新身份类型。 [此页面](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}中列出了标准身份命名空间。

   每个营销活动只允许一个标识类型。 如果属于区段的个人在不同的身份中没有选定的身份类型，则无法将该群体作为目标。

   ![](assets/create-campaign-namespace.png)

   在[Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hans){target="_blank"}中了解有关身份类型和命名空间的更多信息。

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

>[!IMPORTANT]
>
>* 来自[受众合成](../audience/get-started-audience-orchestration.md)的受众和属性当前不可用于Healthcare Shield或Privacy and Security Shield。
>
>* 对于API触发的营销活动，需要通过API调用设置受众。


## 创建消息并配置跟踪 {#content}

1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;部分中，选择渠道。

   可用渠道的列表取决于您的许可模式。 对于API触发的事务型营销活动，只有电子邮件、短信和推送通知渠道可用。

1. 选择渠道配置。

   配置由[系统管理员](../start/path/administrator.md)定义。 它包含用于发送消息的所有技术参数，如标头参数、子域、移动应用程序等。[了解详情](../configuration/channel-surfaces.md)。

   下拉列表中只列出与营销活动类型兼容的渠道配置。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >如果您正在创建推送通知营销活动，则可以启用&#x200B;**[!UICONTROL 快速传递模式]**，这是Journey Optimizer的一个加载项，允许以非常快的速度大量发送推送消息。 [了解详情](../push/create-push.md#rapid-delivery)

1. 单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮创建和设计您的消息。 在以下页面中了解创建消息内容的详细步骤：

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="潜在客户" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>创建电子邮件</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="不频繁" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>创建推送通知</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="验证" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>创建短信消息</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

   定义内容后，使用&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮预览和测试包含测试用户档案的内容。 [了解详情](../content-management/preview-test.md)。要浏览回促销活动创建屏幕，请单击向左箭头。

   ![](assets/create-campaign-design.png)

1. 在&#x200B;**[!UICONTROL 内容试验]**&#x200B;部分中，您可以使用&#x200B;**[!UICONTROL 创建试验]**&#x200B;按钮来测试哪些内容效果更好。 [此部分](../content-management/content-experiment.md)中详细介绍了内容试验功能。

1. 在&#x200B;**[!UICONTROL 操作跟踪]**&#x200B;部分中，指定是否要跟踪收件人对投放的反应：您可以跟踪点击次数和/或打开次数。

   执行营销活动后，即可从营销活动报表访问跟踪结果。 [了解有关营销活动报告的更多信息](../reports/campaign-global-report-cja.md)

## 安排营销活动 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="营销活动计划"
>abstract="默认情况下，营销活动在手动激活时开始，并在发送一次消息后立即结束。 您可以灵活地为要发送的消息设置特定的日期和时间。 此外，还可为定期营销活动或 API 触发的营销活动指定结束日期。在操作触发器中，您还可以配置消息发送频率以满足您的偏好。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="营销活动开始"
>abstract="指定应发送消息的日期和时间。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="营销活动结束"
>abstract="指定应停止执行周期性营销活动的时间。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="营销活动操作触发器"
>abstract="定义营销活动消息的发送频率。"

默认情况下，营销活动在手动激活后开始，在发送一次消息后结束。

您可以定义营销活动消息的发送频率。 为此，请在营销活动创建屏幕中使用&#x200B;**[!UICONTROL 操作触发器]**&#x200B;选项来指定是否应每天、每周或每月执行营销活动。

如果不想在营销活动激活后立即执行营销活动，则可以使用&#x200B;**[!UICONTROL 营销活动开始]**&#x200B;选项指定发送消息的日期和时间。 **[!UICONTROL 营销活动结束]**&#x200B;选项允许您指定何时应停止执行定期营销活动。

![](assets/create-campaign-schedule.png)

营销活动准备就绪后，即可进行审查和激活。 [了解详情](review-activate-campaign.md)
