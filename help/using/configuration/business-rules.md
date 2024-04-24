---
solution: Journey Optimizer
product: journey optimizer
title: 业务规则
description: 了解如何创建和应用业务规则
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: 消息，频率，规则，压力
hide: true
hidefromtoc: true
badge: label="Beta 版"
source-git-commit: c1eef06b0edc4e1bcd1b145f8f822295924b205c
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 10%

---

# 业务规则 {#business-rules}

>[!AVAILABILITY]
>
>目前，业务规则仅作为测试版提供给选定用户。

[!DNL Journey Optimizer] 允许您通过设置跨渠道规则来控制用户接收消息的频率，这些规则会自动从消息和操作中排除过度请求的用户档案。

例如，对于品牌，规则可以是：每月向其客户发送的营销消息不超过4条。 为此，您可以使用频率规则，该规则将限制每月日历期间根据一个或多个渠道发送的消息数。

通过创建不同的规则集来提高粒度， [!DNL Journey Optimizer] 使您可将频率上限应用于不同类型的营销通信。 例如，您可以创建一个规则集以限制 **促销通信** 发送给您的客户，并创建另一个规则集以限制 **快讯** 发送给他们。

>[!NOTE]
>
>业务规则与选择退出管理不同，后者允许用户取消订阅以停止接收来自品牌的通信。 [了解详情](../privacy/opt-out.md#opt-out-management)

## 访问规则集 {#access-rule-sets}

规则集可从 **[!UICONTROL 管理]** > **[!UICONTROL 业务规则（测试版）]** 菜单。 将列出所有规则，按创建日期排序。

![](assets/rule-sets-list.png)

单击规则集名称可查看和编辑其内容。 将列出该规则集中包含的所有规则。

通过右上方的上下文菜单，您可以：

* 编辑规则集的名称和描述
* 激活规则集 —  [了解详情](#activate-rule)
* 删除规则集

![](assets/rule-set-example.png)

对于规则集中的每个规则， **[!UICONTROL 更多操作]** 按钮使您能够：

* 编辑规则
* 激活规则 [了解详情](#activate-rule)
* 删除规则

![](assets/rule-set-example-rules.png)

<!--### Permissions{#permissions-frequency-rules}

To access, create, edit or delete message frequency rules, you must have the **[!UICONTROL Manage frequency rules]** permission. 

Users with the **[!UICONTROL View frequency rules]** permission are able to view rules, but not to modify or delete them.

![](assets/message-rules-access.png)

Learn more about permissions in [this section](../administration/high-low-permissions.md).-->

## 创建规则集 {#create-rule-set}

要创建规则集，请执行以下步骤。

1. 访问 **[!UICONTROL 规则集]** 列表，然后单击 **[!UICONTROL 创建规则集]**.

   ![](assets/rule-sets-create-button.png)

1. 定义规则集名称，根据需要添加描述并单击 **[!UICONTROL 保存]**.

   ![](assets/rule-sets-create.png)

   >[!NOTE]
   >
   >规则集名称必须是唯一的。

1. 现在您可以 [定义规则](#create-new-rule) 要添加到此规则集，并且 [激活](#activate-rule) 它。

   >[!NOTE]
   >
   >确保在规则集中也激活要应用于消息的所有规则。

## 创建规则 {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_category"
>title="选择消息规则类别"
>abstract="在规则激活并应用到一条消息时，与所选类别匹配的所有频率规则将自动应用于该消息。目前只有营销类别可用。"

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_capping"
>title="设置规则的频次封顶"
>abstract="指定在所选时间范围内发给某个客户配置文件的最大消息数。频率上限将基于所选的日历期间，并将在相应的时间范围开始时重置它。"

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_channel"
>title="定义规则应用到的渠道"
>abstract="请至少选择一个渠道。对所有渠道的总计数应用频次封顶。"

要将规则添加到规则集，请执行以下步骤。

1. 在刚刚创建的规则集中，单击 **[!UICONTROL 添加规则]**.

   ![](assets/rule-sets-create-rule-button.png)

1. 定义规则名称。

   >[!NOTE]
   >
   >规则集名称必须是唯一的。

1. 选择消息规则类别。

   >[!NOTE]
   >
   >当前仅 **[!UICONTROL 营销]** 类别可用。

1. 从 **[!UICONTROL 持续时间]** 下拉列表中，选择要应用的上限的时间范围。 [了解详情](#frequency-cap)

1. 设置规则的上限，即根据您在上面的选择，每月、每周或每天可以向单个用户配置文件发送的最大消息数。

1. 选择要用于此规则的渠道： **[!UICONTROL 电子邮件]**， **[!UICONTROL 短信]**， **[!UICONTROL 推送通知]** 或 **[!UICONTROL 直邮]**.

   ![](assets/rule-set-channels.png)

   >[!NOTE]
   >
   >您必须至少选择一个渠道才能创建规则。

1. 如果要将上限应用到所有选定渠道的总数，请选择多个渠道。

   例如，将上限设置为5，然后选择电子邮件和短信渠道。 如果某个用户档案在选定时间段内已收到3封营销电子邮件和2封营销短信，则该用户档案将从任何营销电子邮件或短信的下一个投放中排除。

1. 单击 **[!UICONTROL 保存]** 以确认创建规则。 您的消息将添加到规则集，并使用 **[!UICONTROL 草稿]** 状态。

   ![](assets/rule-set-rule-created.png)

1. 重复上述步骤，根据需要向规则集添加任意数量的规则。

现在，您需要先激活每个规则，然后才能将其应用于任何消息。 [了解详情](#activate-rule)

>[!NOTE]
>
>确保已激活规则集，以便能够在消息中选择它。

### 频率限制 {#frequency-cap}

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_duration"
>title="选择消息规则类别"
>abstract="在规则激活并应用到一条消息时，与所选类别匹配的所有频率规则将自动应用于该消息。目前只有营销类别可用。"

从 **[!UICONTROL 持续时间]** 下拉列表中，选择是每月、每周还是每日应用上限。

频率上限基于所选的日历期间。 它会在相应时间范围的开头重置。

![](assets/rule-set-capping-duration.png)

各期间计数器到期如下：

* **[!UICONTROL 每月]**：频率上限有效期到每月最后一天23点:59:世界协调时59分 例如，1月的每月到期时间为01-31 23:59:世界协调时59分

* **[!UICONTROL 每周]**：频率上限有效期到星期六23日:59:作为日历周的那一周的59 UTC从星期日开始。 无论规则如何创建，都会过期。 例如，如果规则在星期四创建，则此规则的有效期到星期六23:59:59.

* **[!UICONTROL 每日]**：每日频率上限的有效期为一天，截止日期为23日:59:59 UTC时间，并在第二天开始时重置为0。

### 每日频率上限 {#daily-frequency-cap}

>[!CAUTION]
>
>要确保每日频率限定规则的准确性，请使用 [流式分段](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"} 为必填项。 在中了解有关受众评估方法的更多信息 [本节](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

任何区段大小，每小时报文数量不超过6,000万条<!--not clear-->，确保您的营销活动至少间隔2小时。


<!-- Journey example:

* If customer sets a Daily rule under the Global Ruleset for email <= 2/day:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for noon)
   * Journey 789 (scheduled for 1 pm)

   In this example, the Daily Frequency cap will not guarantee <= 2/day. The rule will only be guaranteed when Journeys are at least 2 hours apart:
   * Journey 123 (scheduled for noon)
   * Journey 456 (scheduled for 2 pm)
   * Journey 789 (scheduled for 4 pm)-->

例如，如果在为电子邮件渠道设置的规则下设置了每天规则，该规则少于或等于2天，并且创建了以下营销活动：
* 营销活动A（计划在中午）
* 营销活动A（计划于下午3点）
* 营销活动B（计划于下午1点）

此设置不起作用，原因有二：
* 由于营销活动之间没有间隔2小时，因此不保证每日频率上限。
* 利用每日上限在一天内多次计划同一营销活动不是最佳实践。

每日频率上限应遵循以下示例：
* 营销活动A（计划在中午）
* 营销活动B（计划于下午2点）

<!--* To use the Daily Cap with a Journey, customers can use either an Event Triggered Journey or an Audience Qualified Journey. If customers wish to use the Daily Cap with a Read Audience Journey, they should use a Campaign instead and associate a Local Ruleset with the campaign, following the example given above.-->

## 激活规则和规则集 {#activate-rule}

创建规则后，该规则具有 **[!UICONTROL 草稿]** 状态，尚未影响任何消息。 要启用该功能，请单击 **[!UICONTROL 更多操作]** 按钮，然后选择 **[!UICONTROL 激活]**.

![](assets/rule-set-activate-rule.png)

您还必须激活规则集才能在营销活动/历程中访问它，并将其应用于消息。

![](assets/rule-set-activate-set.png)

激活规则集将会影响它在下次执行时应用到的任何消息。 了解如何 [将规则集应用到消息](#apply-rule-set).

>[!NOTE]
>
>完全激活规则或规则集最多可能需要10分钟。 您无需修改消息或重新发布历程，规则即可生效。

<!--Currently, once a rule set is activated, no more rules can be added to that rule set.-->

## 停用规则和规则集 {#deactivate-rule}

要停用规则或规则集，请单击 **[!UICONTROL 更多操作]** 按钮，然后选择 **[!UICONTROL 取消激活]**.

![](assets/rule-set-inactive-rule.png)

其状态将更改为 **[!UICONTROL 不活动]** 并且该规则不适用于未来的消息执行。 当前正在执行的任何消息都不会受到影响。

>[!NOTE]
>
>停用规则或规则集不会影响或重置单个配置文件上的任何计数。

## 将频率规则应用于消息 {#apply-frequency-rule}

要向消息应用频率规则，请执行以下步骤。

1. 创建时 [营销活动](../campaigns/create-campaign.md)，选择为规则集定义的渠道之一并编辑消息的内容。

1. 在内容版本屏幕中，单击 **[!UICONTROL 添加业务规则]** 按钮。

1. 选择 [您创建的规则集](#create-rule-set).

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >仅 [已激活](#activate-rule) 规则集将显示在列表中。

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. 您可以在中查看从投放中排除的用户档案数 [全局报告](../reports/global-report.md)、和 [实时报告](../reports/live-report.md)，其中频率规则将列为从投放中排除的用户的可能原因。

>[!NOTE]
>
>同一渠道可以应用多个规则，但一旦到达下限，用户档案将从下次投放中排除。

<!--
## Example: combine several rules {#frequency-rule-example}

You can combine several message frequency rules, such as described in the example below.

1. [Create a rule](#create-new-rule) called *Overall Marketing Capping*:

   * Select all channels.
   * Set capping to 12 monthly.

   ![](assets/message-rules-ex-overall-cap.png)

1. To further restrict the number of marketing-based push notifications that a user is sent, create a second rule called *Push Marketing Cap*:

   * Select Push channel.
   * Set capping to 4 monthly.

   ![](assets/message-rules-ex-push-cap.png)

1. Save and [activate](#activate-rule) the rule.

1. [Create a message](../building-journeys/journeys-message.md) for every channel you want to communicate through and select the **[!UICONTROL Marketing]** category for each message. [Learn how to apply a frequency rule](#apply-frequency-rule)

   ![](assets/journey-message-category.png)

In this scenario, an individual profile:
* can receive up to 12 marketing messages per month;
* but will be excluded from marketing push notifications after they have received 4 push notifications.-->

测试频率规则时，建议使用新创建的 [测试配置文件](../audience/creating-test-profiles.md)，因为一旦达到用户档案的频度上限，就无法在下一时段之前重置计数器。 停用规则将允许有上限的用户档案接收消息，但不会移除或删除任何计数器增量。

