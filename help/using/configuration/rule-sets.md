---
solution: Journey Optimizer
product: journey optimizer
title: 使用规则集
description: 了解如何创建和应用规则集
feature: Rules
topic: Content Management
role: User
level: Intermediate
keywords: 消息，频率，规则，压力
badge: label="Beta 版"
hide: true
hidefromtoc: true
exl-id: 07f5f0b4-417e-408e-8d9e-86615c8a3fbf
source-git-commit: b69c75e0a8a35635a67065412e443a2af0d3b09f
workflow-type: tm+mt
source-wordcount: '1630'
ht-degree: 8%

---

# 使用规则集 {#rule-sets}

>[!CONTEXTUALHELP]
>id="ajo_business_rules_rule_sets"
>title="规则集"
>abstract="使用规则集将频率上限应用于不同类型的营销通信。 例如，您可以创建一个规则集以限制 **促销通信** 发送给您的客户，并创建另一个规则集以限制 **快讯** 发送给他们。 规则集目前作为测试版提供，仅供选择用户使用。"

>[!AVAILABILITY]
>
>规则集当前仅作为测试版提供给选定用户。 请联系您的Adobe代表以加入测试版。

## 什么是规则集？ {#what}

除了限制用户跨一个或多个渠道接收消息次数的全局业务规则之外，通过规则集您还可以 **将多个规则分组到规则集中** 并将其应用于您选择的营销策划。 这提高了粒度，以便根据通信类型控制用户接收消息的频率。

例如，您可以创建一个规则集以限制 **促销通信** 发送给您的客户，并且设置了另一个规则来限制 **快讯** 发送给他们。 根据要创建的促销活动类型，您可以选择应用促销通信或新闻稿规则集。

## 全局和自定义规则集 {#global-custom}

首次从访问规则集时 **[!UICONTROL 管理]** > **[!UICONTROL 业务规则（测试版）]** 菜单上，默认规则集已预先创建并处于活动状态： **全局默认规则集**.

此规则集包含全局规则，您可以应用这些规则来控制用户通过一个或多个渠道接收消息的频率，类似于当前业务规则的操作方式。 此规则集中定义的所有规则都适用于所有选定的渠道，无论通信是从历程还是营销活动发送。 [了解如何使用业务规则](frequency-rules.md)

除了此“全局默认规则集”规则集之外，您还可以创建 **自定义规则** 设置，可将其应用于任何营销活动以限制在该营销活动中发送的消息数。 [了解如何创建自定义规则集](#create)

![](assets/rule-sets-default.png)

>[!IMPORTANT]
>
>目前，可将自定义规则集应用于 **营销活动** 仅限。 仅“全局默认规则集”规则集中定义的规则适用于历程和营销活动通信。

## 创建您的第一个自定义规则集 {#create-rule-set}

### 创建规则集 {#create}

要创建规则集，请执行以下步骤。

>[!NOTE]
>
>您最多可以创建3个自定义规则集。

1. 访问 **[!UICONTROL 规则集]** 列表，然后单击 **[!UICONTROL 创建规则集]**.

   ![](assets/rule-sets-create-button.png)

1. 定义规则集名称，根据需要添加描述并单击 **[!UICONTROL 保存]**.

   ![](assets/rule-sets-create.png)

   >[!NOTE]
   >
   >规则集名称必须是唯一的。

1. 现在您可以 [定义规则](#create-new-rule) 要添加到此规则集。

### 将规则添加到规则集 {#create-new-rule}

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

>[!CONTEXTUALHELP]
>id="ajo_rule_sets_duration"
>title="选择消息规则类别"
>abstract="在规则激活并应用到一条消息时，与所选类别匹配的所有频率规则将自动应用于该消息。目前只有营销类别可用。"

要将规则添加到规则集，请执行以下步骤。

1. 在刚刚创建的规则集中，单击 **[!UICONTROL 添加规则]**.

   ![](assets/rule-sets-create-rule-button.png)

1. 定义唯一 **规则名称**.

1. 此 **类别** 字段指定规则适用的消息类别。 目前，此字段是只读的，因为 **[!UICONTROL 营销]** 类别可用。

1. 从 **[!UICONTROL 持续时间]** 下拉列表中，选择是每月、每周还是每日应用上限。 频率上限基于所选的日历期间。 它会在相应时间范围的开头重置。

   ![](assets/rule-set-capping-duration.png)

   各期间计数器到期如下：

   * **[!UICONTROL 每月]**：频率上限有效期到每月最后一天23点:59:世界协调时59分 例如，1月的每月到期时间为01-31 23:59:世界协调时59分

   * **[!UICONTROL 每周]**：频率上限有效期到星期六23日:59:作为日历周的那一周的59 UTC从星期日开始。 无论规则如何创建，都会过期。 例如，如果规则在星期四创建，则此规则的有效期到星期六23:59:59.

   * **[!UICONTROL 每日]**：每日频率上限的有效期为一天，截止日期为23日:59:59 UTC时间，并在第二天开始时重置为0。

     >[!CAUTION]
     >
     >要确保每日频率限定规则的准确性，请使用 [流式分段](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"} 为必填项。 在中了解有关受众评估方法的更多信息 [本节](../audience/about-audiences.md#evaluation-method-in-journey-optimizer).

   请注意，一旦传递通信，配置文件计数器值将更新。 当您发送大量通信时，请注意这一点，因为吞吐量可能导致收件人收到电子邮件时间达到通信启动后的几分钟甚至几小时（如果您同时发送数百万条通信）。

   如果收件人收到两个彼此靠近的通信，则这一点很重要。 我们建议将通信间隔至少两小时，在可能的情况下，为收件人提供充足的时间来接收通信，并相应地更新计数器值。

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

### 激活规则和规则集 {#activate-rule}

创建规则后，该规则具有 **[!UICONTROL 草稿]** 状态，尚未影响任何消息。 要启用该功能，请单击 **[!UICONTROL 更多操作]** 按钮，然后选择 **[!UICONTROL 激活]**.

![](assets/rule-set-activate-rule.png)

您还必须激活规则集才能在营销活动/历程中访问它，并将其应用于消息。

![](assets/rule-set-activate-set.png)

激活规则集将会影响它在下次执行时应用到的任何消息。 了解如何 [将规则集应用到消息](#apply-rule-set).

>[!NOTE]
>
>完全激活规则或规则集最多可能需要10分钟。 您无需修改消息或重新发布历程，规则即可生效。

<!--Currently, once a rule set is activated, no more rules can be added to that rule set.-->

要停用规则或规则集，请单击 **[!UICONTROL 更多操作]** 按钮，然后选择 **[!UICONTROL 取消激活]**.

![](assets/rule-set-inactive-rule.png)

其状态将更改为 **[!UICONTROL 不活动]** 并且该规则不适用于未来的消息执行。 当前正在执行的任何消息都不会受到影响。

>[!NOTE]
>
>停用规则或规则集不会影响或重置单个配置文件上的任何计数。

## 访问和管理规则集 {#access-rule-sets}

所有创建的规则集都将显示在 **[!UICONTROL 管理]** > **[!UICONTROL 业务规则（测试版）]** 菜单。 它们按上次修改日期排序。

![](assets/rule-sets-list.png)

单击规则集名称可查看和编辑其内容。 将列出该规则集中包含的所有规则。 通过右上方的上下文菜单，您可以：

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

## 将规则集应用到消息 {#apply-frequency-rule}

要将业务规则应用于消息，请执行以下步骤。

1. 创建时 [营销活动](../campaigns/create-campaign.md)，选择为规则集定义的渠道之一并编辑消息的内容。

1. 在内容版本屏幕中，单击 **[!UICONTROL 添加业务规则]** 按钮。

1. 选择 [您创建的规则集](#create-rule-set).

   ![](assets/rule-set-campaign-add-rule-button.png)

   >[!NOTE]
   >
   >仅 [已激活](#activate-rule) 规则集将显示在列表中。

   <!--Messages where the category selected is **[!UICONTROL Transactional]** will not be evaluated against business rules.-->

1. 在激活营销活动之前，请确保将其计划在将来的至少10分钟后执行。

   这样就有足够的时间在配置文件上为您选择的业务规则填充计数器值。 如果立即激活营销活动，规则集计数器值将不会填充在收件人的用户档案中，并且消息将不会计入其自定义规则集的频率上限规则中。

   ![](assets/rule-set-schedule-campaign.png)

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
