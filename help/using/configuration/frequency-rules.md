---
solution: Journey Optimizer
product: journey optimizer
title: 配置业务规则
description: 了解如何定义业务频率规则
feature: Rules
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
robots: noindex
googlebot: noindex
keywords: 消息，频率，规则，压力
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 14%

---

# 配置业务规则 {#frequency-rules}

>[!CONTEXTUALHELP]
>id="ajo_business_rules_message_frequency_rules"
>title="业务规则"
>abstract="消息频率规则是一种业务规则，用于限制用户通过一个或多个渠道接收消息或进入历程的次数。这些跨渠道规则会自动从消息和操作中排除过度请求的轮廓。"

[!DNL Journey Optimizer]允许您控制用户通过一个或多个渠道接收消息或进入历程的频率。 消息频率规则，用于从消息和操作中自动排除过度请求的用户档案。

例如，对于品牌，规则不能每月向客户发送超过4条营销消息。 要实现此目的，您可以使用业务规则，该规则将限制每月日历期间根据一个或多个渠道发送的消息数。

![](assets/do-not-localize/sms-dm-rules.gif)

>[!NOTE]
>
>业务规则与选择退出管理不同，后者允许用户取消订阅以停止接收来自品牌的通信。 [了解详情](../privacy/opt-out.md#opt-out-management)

➡️ [通过观看视频了解此功能](#video)

## 访问业务规则 {#access-rules}

可从&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 业务规则]**&#x200B;菜单访问业务规则。 将列出所有规则，并按修改日期排序。 使用过滤器图标可按类别、状态和/或渠道进行过滤。 您还可以搜索消息标签。

![](assets/message-rules-filter.png)

### 权限{#permissions-frequency-rules}

要访问、创建、编辑或删除业务规则，您必须具有&#x200B;**[!UICONTROL 管理频率规则]**&#x200B;权限。

具有&#x200B;**[!UICONTROL 查看频率规则]**&#x200B;权限的用户可以查看规则，但不能修改或删除规则。

![](assets/message-rules-access.png)

可在[此部分](../administration/high-low-permissions.md)中详细了解权限。

## 创建业务规则 {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="选择消息规则类别"
>abstract="在规则激活并应用到一条消息时，与所选类别匹配的所有业务规则将自动应用于该消息。目前只有营销类别可用。"

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="设置业务规则的频次封顶"
>abstract="指定在所选时间范围内发给某个客户轮廓的最大消息数。频率上限将基于所选的日程表期间，并将在相应的时间范围开始时重置它。"

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="定义业务规则应用到的渠道"
>abstract="请至少选择一个渠道。对所有渠道的总计数应用频次封顶。"

要创建新的业务规则，请执行以下步骤。

1. 访问&#x200B;**[!UICONTROL 业务规则]**&#x200B;列表，然后单击&#x200B;**[!UICONTROL 创建规则]**。

   ![](assets/message-rules-create.png)

1. 定义规则名称并选择消息规则类别。

   >[!NOTE]
   >
   >仅&#x200B;**[!UICONTROL Marketing]**&#x200B;类别可用。

   ![](assets/message-rules-details.png)

1. 从&#x200B;**[!UICONTROL 持续时间]**&#x200B;下拉列表中，选择要应用的上限的时间范围。 [了解详情](#frequency-cap)

1. 设置规则的上限，即根据以上选择，每月或第<!--or day-->周可以发送到单个用户配置文件的最大消息数。

   <!--![](assets/message-rules-capping.png)-->

1. 选择要用于此规则的渠道： **[!UICONTROL 电子邮件]**、**[!UICONTROL 推送通知]**、**[!UICONTROL 短信]**&#x200B;或&#x200B;**[!UICONTROL 直邮]**。

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >您必须至少选择一个渠道才能创建规则。

1. 如果要将上限应用到所有选定渠道的总数，请选择多个渠道。

   例如，将上限设置为15，然后选择电子邮件和推送渠道。 如果某用户档案在选定时间段内已收到10封营销电子邮件和5封营销推送通知，则将从任何营销电子邮件或推送通知的下一个投放中排除该用户档案。

1. 单击&#x200B;**[!UICONTROL 另存为草稿]**&#x200B;以确认创建规则。 您的消息已添加到规则列表，状态为&#x200B;**[!UICONTROL 草稿]**。

   ![](assets/message-rules-created.png)

### 频率上限 {#frequency-cap}

从&#x200B;**[!UICONTROL 持续时间]**&#x200B;下拉列表中，选择要每月还是每周应用上限。

>[!NOTE]
>
>还可根据需要使用每日频率上限。 [了解详情](#daily-frequency-cap)

频率上限基于所选的日历期间。 它会在相应时间范围的开头重置。

![](assets/message-rules-capping-duration.png)

各期间计数器到期如下：

* **[!UICONTROL 每月]**：频率上限在每月最后一天23:59:59 UTC之前有效。 例如，1月的每月到期时间为01-31 23:59:59 UTC。

* **[!UICONTROL 每周]**：频率上限有效期到星期六23:59:59 UTC，因为日历周从星期日开始。 无论规则如何创建，都会过期。 例如，如果规则是在星期四创建的，则此规则的有效期到星期六23:59:59。

### 每日频率上限 {#daily-frequency-cap}

除了每月和每周外，还可按需提供每日频率上限。 有关更多信息，请联系您的Adobe代表。

每日频率上限在23:59:59 UTC之前的一天有效，并在第二天开始时重置为0。

>[!NOTE]
>
>为确保每日频率上限规则的准确性，建议使用[流式分段](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html?lang=zh-Hans){target="_blank"}。 在[本节](../audience/about-audiences.md#evaluation-method-in-journey-optimizer)中了解有关受众评估方法的更多信息。

## 激活业务规则 {#activate-rule}

创建后，业务规则处于&#x200B;**[!UICONTROL 草稿]**&#x200B;状态，尚未影响任何消息。 要启用它，请单击规则旁边的省略号，然后选择&#x200B;**[!UICONTROL 激活]**。

![](assets/message-rules-activate.png)

激活规则将影响它在下次执行时应用到的任何消息。 了解如何[将业务规则应用于消息](#apply-frequency-rule)。

>[!NOTE]
>
>完全激活规则最多可能需要10分钟。 您无需修改消息或重新发布历程，规则即可生效。

要停用业务规则，请单击该规则旁边的省略号，然后选择&#x200B;**[!UICONTROL 停用]**。

![](assets/message-rules-deactivate.png)

规则的状态将更改为&#x200B;**[!UICONTROL 不活动]**，并且该规则将不应用于未来的消息执行。 当前正在执行的任何消息都不会受到影响。

>[!NOTE]
>
>停用规则不会影响或重置单个配置文件上的任何计数。

## 将业务规则应用于消息 {#apply-frequency-rule}

要将业务规则应用于消息，请执行以下步骤。

1. 创建[历程](../building-journeys/journey-gs.md)时，通过选择为规则定义的渠道之一来添加消息。

1. 选择您为创建的[规则](#create-new-rule)定义的类别。

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >当前仅&#x200B;**[!UICONTROL Marketing]**&#x200B;类别可用于业务规则。

1. 您可以单击&#x200B;**[!UICONTROL 频率规则]**&#x200B;链接以在新选项卡中查看频率规则屏幕。 [了解详情](#access-rules)

   与所选类别和渠道匹配的所有规则将自动应用于此消息。

   >[!NOTE]
   >
   >不会根据频率规则评估选定类别为&#x200B;**[!UICONTROL 事务型]**&#x200B;的消息。

1. 您可以在[Customer Journey Analytics报告](../reports/report-gs-cja.md)和[实时报告](../reports/live-report.md)中查看从投放中排除的用户档案数，在这些报告中，业务规则将列为从投放中排除的用户的可能原因。

>[!NOTE]
>
>同一渠道可以应用多个规则，但一旦到达下限，用户档案将从下次投放中排除。

## 示例：合并多个规则 {#frequency-rule-example}

您可以合并多个业务规则，如下面的示例所述。

1. [创建名为&#x200B;*整体营销上限*&#x200B;的业务规则](#create-new-rule)：

   * 选择所有渠道。
   * 将上限设置为每月12次。

   ![](assets/message-rules-ex-overall-cap.png)

1. 要进一步限制发送用户的基于营销的推送通知的数量，请创建名为&#x200B;*推送营销上限*&#x200B;的第二个规则：

   * 选择推送渠道。
   * 将上限设置为4个月。

   ![](assets/message-rules-ex-push-cap.png)

1. 保存并[激活](#activate-rule)规则。

1. [为要与之通信的每个渠道创建消息](../building-journeys/journeys-message.md)，并为每个消息选择&#x200B;**[!UICONTROL 营销]**&#x200B;类别。 [了解如何应用业务规则](#apply-frequency-rule)

   ![](assets/journey-message-category.png)


<!--
Learn how to create a message for the different channels in the following sections:
* [Create an email](../email/create-email.md)
* [Create a push notification](../push/create-push.md)
* [Create an SMS](../sms/create-sms.md)
* [Create a direct mail](../direct-mail/create-direct-mail.md)

Create an email and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../email/create-email.md)

Create a push notification and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../push/create-push.md)

Create an SMS and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../sms/create-sms.md)

Create a direct mail and select the **[!UICONTROL Marketing]** category for that message. [Learn more](../direct-mail/create-direct-mail.md)
-->

在此方案中，单个配置文件：
* 每月最多可接收12条营销消息；
* 但是，在收到4个推送通知后，这些通知将被排除在营销推送通知之外。

>[!NOTE]
>
>测试业务规则时，建议使用新创建的[测试配置文件](../audience/creating-test-profiles.md)，因为一旦达到配置文件的频率上限，就无法在下个月之前重置计数器。 停用规则将允许有上限的用户档案接收消息，但不会移除或删除任何计数器增量。

## 操作说明视频 {#video}

了解如何创建、激活、测试和报告业务规则。

>[!VIDEO](https://video.tv.adobe.com/v/3411120?quality=12&captions=chi_hans)
