---
solution: Journey Optimizer
product: journey optimizer
title: 创建移动设备消息
description: 了解如何在Journey Optimizer中创建移动消息
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
TQID: https://experienceleague.adobe.com/xgPlWorA3lsIF8ZBPHdg2UAK8cLKUsJO-2ONc7ZG8AU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4c82775044b5a0a3a48920f59b0afb8a3c6a6d80
workflow-type: tm+mt
source-wordcount: 889
ht-degree: 6%

---

# 创建移动设备消息 {#create-sms}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何在Adobe Journey Optimizer中将移动消息操作添加到历程或营销活动，然后选择配置并编辑内容以发送文本、富格通信和多媒体消息。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="创建移动设备消息"
>abstract="要创建移动设备消息，请将 SMS 操作添加到历程或营销活动中，并使用个性化编辑器开始进行个性化设置。"

>[!AVAILABILITY]
>
>RCS不是HIPAA就绪服务，不得用于收集、存储或处理您的组织可能获准在Journey Optimizer中处理的任何敏感个人数据，包括允许的健康数据，例如个人健康信息。

您可以使用Adobe Journey Optimizer设计和发送文本(SMS)、富通信(RCS)和多媒体(MMS)消息。 您首先需要在历程或营销策划中添加移动消息操作，然后定义移动消息的内容，如下所述。 Adobe Journey Optimizer还提供了在发送之前测试移动消息的功能，以便您检查渲染、个性化属性和所有其他设置。

根据行业标准和法规，所有SMS/RCS/MMS营销消息都必须包含一种让接收者轻松取消订阅的方式。 要实现此目的，短信收件人可以使用选择启用和选择禁用关键词进行回复。 [了解如何管理选择退出](../privacy/opt-out.md#opt-out-decision-management)

## 添加移动消息 {#create-sms-journey-campaign}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_sms"
>title="移动消息操作"
>abstract="移动消息渠道操作在用户档案到达历程的此步骤时，向用户档案发送文本(SMS)、多媒体(MMS)或富通信(RCS)消息。 标签在历程画布中标识活动，并且操作引用定义交付内容的移动设备消息配置。 **优化**&#x200B;部分可以包含内容实验或定位规则，**多语言**&#x200B;部分可以投放多种语言的内容，并且&#x200B;**超时或错误**&#x200B;部分可以定义在操作失败时的替代路径。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/journey-action#add-action" text="渠道操作入门"

浏览以下选项卡，了解如何在营销活动或历程中添加移动消息。

>[!BEGINTABS]

>[!TAB 向历程添加移动消息]

1. 打开您的历程，然后从面板的&#x200B;**[!UICONTROL 操作]**&#x200B;部分拖放&#x200B;**[!UICONTROL 操作]**&#x200B;活动。 了解有关[操作活动](../building-journeys/journey-action.md)的详细信息。

   >[!IMPORTANT]
   >
   >自2026年3月发行版起，弃用旧版本机渠道活动（电子邮件、推送、短信、应用程序内、Web、基于代码的体验和内容卡）。 使用这些活动的现有历程可以继续工作，且不会发生任何更改 — 无需迁移。

1. 选择&#x200B;**[!UICONTROL 手机消息]**&#x200B;作为操作类型，然后单击&#x200B;**[!UICONTROL 添加]**。

   ![](assets/sms_create_1.png)

1. 输入&#x200B;**[!UICONTROL 标签]**&#x200B;以在历程画布中标识您的操作。

1. 单击&#x200B;**[!UICONTROL 配置操作]**&#x200B;按钮。

1. 您被定向到&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡。 从该位置，选择或创建要使用的移动设备消息配置。 [了解详情](mobile-configuration.md)

   ![](assets/sms_create_2.png)

1. 此外，您还可以通过在&#x200B;**[!UICONTROL 业务规则]**&#x200B;下拉列表中选择一个规则集，将上限规则应用于您的移动设备消息操作。 [了解详情](../conflict-prioritization/channel-capping.md)

1. 选择&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮并根据需要创建内容。 [了解详情](design-mobile.md)

1. 返回历程画布。 如有必要，请通过拖放其他操作或事件来完成旅程流程。 [了解详情](../building-journeys/about-journey-activities.md)

有关如何创建、配置和发布历程的详细信息，请参阅[此页面](../building-journeys/journey-gs.md)。

>[!TAB 向营销活动添加移动消息]

1. 访问&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。

1. 选择要执行的营销活动类型

   * **已计划 — 营销**：立即或在指定日期执行营销活动。 计划的营销活动旨在发送营销消息。 它们从用户界面配置和执行。

   * **API触发 — 营销/事务性**：使用API调用执行营销活动。 API触发的营销活动旨在发送营销或事务型消息，即，在个人执行操作（密码重置、购物车购买等）之后发送的消息。

1. 从&#x200B;**[!UICONTROL 属性]**&#x200B;部分，编辑营销活动的&#x200B;**[!UICONTROL 标题]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;选项卡中，单击&#x200B;**[!UICONTROL 添加操作]**，然后选择&#x200B;**[!UICONTROL 手机消息]**。 然后，选择或创建新配置。

   在[此页面](mobile-configuration.md)上了解有关移动消息配置的更多信息。

   ![](assets/sms_create_3.png)

1. 单击&#x200B;**[!UICONTROL 创建试验]**&#x200B;开始配置内容试验并创建处理以测量其性能并为目标受众确定最佳选项。 [了解详情](../content-management/content-experiment.md)

1. 在&#x200B;**[!UICONTROL 操作跟踪]**&#x200B;部分中，指定是否要跟踪移动设备消息中的链接点击次数。

1. 在&#x200B;**[!UICONTROL 受众]**&#x200B;选项卡中，单击&#x200B;**[!UICONTROL 选择受众]**&#x200B;按钮，以从可用Adobe Experience Platform受众列表中定义要定位的受众。 [了解详情](../audience/about-audiences.md)。

1. 在&#x200B;**[!UICONTROL 身份命名空间]**&#x200B;字段中，选择要使用的命名空间，以便识别所选受众中的个人。 [了解详情](../event/about-creating.md#select-the-namespace)。

1. 从&#x200B;**[!UICONTROL 计划]**&#x200B;选项卡，您可以将营销活动设计为在特定的日期或循环频率执行。 在[本节](../campaigns/campaign-schedule.md#action-campaign-schedule)中了解如何配置促销活动的&#x200B;**[!UICONTROL 计划]**。

1. 从&#x200B;**[!UICONTROL 操作触发器]**&#x200B;菜单中，选择手机消息的&#x200B;**[!UICONTROL 频率]**：

   * 一次
   * 每日
   * 每周
   * Month

您现在可以从&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮开始设计移动消息的内容，如下所述。 [了解详情](design-mobile.md)

有关如何创建、配置和激活促销活动的详细信息，请参阅[此页面](../campaigns/get-started-with-campaigns.md)。

>[!ENDTABS]

**相关主题**

* [设计移动消息](design-mobile.md)
* [在营销活动中添加消息](../campaigns/create-campaign.md)
* [预览、测试和发送您的移动消息](send-mobile-message.md)
* [配置移动消息渠道](mobile-configuration.md)
* [移动消息报表](../reports/journey-global-report-cja-sms.md)

