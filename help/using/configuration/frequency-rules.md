---
title: 频度规则
description: 了解如何定义频度规则
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 2%

---

# 消息频度规则 {#frequency-rules}

[!DNL Journey Optimizer] 允许您通过设置跨渠道规则来控制用户接收消息或进入历程的频率，该规则将自动从消息和操作中排除发送过量请求的用户档案。

例如，您不希望您的品牌每月向其客户发送超过3条营销消息。

为此，您可以使用频度规则来限制在每月日历期间根据一个或多个渠道发送的消息数量。

>[!NOTE]
>
>消息频度规则与选择退出管理不同，选择退出管理允许用户取消订阅以接收来自品牌的通信。 [了解详情](../messages/consent.md#opt-out-management)

## 访问规则 {#access-rules}

规则可从 **[!UICONTROL Administration]** > **[!UICONTROL Rules]** 菜单。 将列出所有规则，并按修改日期排序。

![](assets/message-rules-access.png)

<!--To access, create, edit or delete message frequency rules, you must have the message configuration permission. [Learn more](../administration/high-low-permissions.md#administration-permissions)-->

使用过滤器图标可对类别、状态和/或渠道进行过滤。 您还可以在消息标签上搜索。

![](assets/message-rules-filter.png)

## 创建规则 {#create-new-rule}

要创建新规则，请执行以下步骤。

1. 访问 **[!UICONTROL Message frequency rules]** 列表，然后单击 **[!UICONTROL Create rule]**.

   ![](assets/message-rules-create.png)

1. 定义规则名称。

   ![](assets/message-rules-details.png)

1. 选择消息规则类别。

   >[!NOTE]
   >
   >当前仅 **[!UICONTROL Marketing]** 类别。

1. 设置规则的上限，即每月可发送到单个用户配置文件的消息数上限。

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >频度上限基于月度日历周期。 它会在每月初重置。

1. 选择要用于此规则的渠道： **[!UICONTROL Email]** 或 **[!UICONTROL Push notification]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >您必须至少选择一个渠道才能创建规则。

1. 如果要将上限作为总计数应用于所有选定渠道，请选择多个渠道。

   例如，将上限设置为15，然后选择电子邮件和推送渠道。 如果用户档案已收到10封营销电子邮件和5条营销推送通知，则此用户档案将从任何营销电子邮件或推送通知的下一次投放中排除。

1. 单击 **[!UICONTROL Save as draft]** 以确认创建规则。 您的消息将添加到规则列表中，其中 **[!UICONTROL Draft]** 状态。

   ![](assets/message-rules-created.png)

## 激活规则 {#activate-rule}

创建消息频度规则后，该规则的 **[!UICONTROL Draft]** 状态和尚未影响任何消息。 要启用它，请单击规则旁边的省略号，然后选择 **[!UICONTROL Activate]**.

![](assets/message-rules-activate.png)

激活规则将影响规则应用于其下次执行的任何消息。 了解如何 [将频度规则应用于消息](#apply-frequency-rule).

>[!NOTE]
>
>您无需修改或重新发布消息或历程，规则即可生效。

要停用消息频度规则，请单击规则旁边的省略号，然后选择 **[!UICONTROL Deactivate]**.

![](assets/message-rules-deactivate.png)

规则的状态将更改为 **[!UICONTROL Inactive]** 并且该规则将不适用于将来的消息执行。 当前正在执行的任何消息都不会受到影响。

>[!NOTE]
>
>取消激活规则不会影响或重置单个用户档案的任何计数。

## 将频度规则应用于消息 {#apply-frequency-rule}

要将频度规则应用于消息，请执行以下步骤。

1. 创建消息. [了解详情](../messages/get-started-content.md#create-new-message)

1. 选择为 [创建的规则](#create-new-rule).

   ![](assets/message-rules-msg-properties.png)

   >[!NOTE]
   >
   >当前仅 **[!UICONTROL Marketing]** 类别可用于消息频度规则。

1. 选择您为消息选择的渠道。

   ![](assets/message-rules-msg-channels.png)

1. 您可以单击 **[!UICONTROL Frequency rule]** 链接以查看将应用于所选类别和渠道的频率规则。

   ![](assets/message-rules-msg-link.png)

   将打开一个新选项卡，以显示匹配的消息频度规则。

1. [设计](../design/design-emails.md) 和 [发布](../messages/publish-manage-message.md) 你的留言。

与所选类别和渠道匹配的所有频率规则都将自动应用于此消息。

<!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

您可以在 [实时视图和全局视图](../reports/message-monitoring.md)和 [电子邮件实时报表](../reports/email-live-report.md)，其中频度规则将列为用户被排除在投放之外的可能原因。

## 示例：合并多个规则 {#frequency-rule-example}

您可以组合多个消息频率规则，如以下示例中所述。

1. [创建规则](#create-new-rule) 调用 *整体营销上限*:

   * 选择所有渠道（电子邮件、推送）。
   * 将上限设置为12。

   ![](assets/message-rules-ex-overall-cap.png)

1. 要进一步限制用户发送的基于营销的推送通知数量，请再创建一个名为 *推送营销上限*:

   * 选择推送渠道。
   * 将上限设置为4。

   ![](assets/message-rules-ex-push-cap.png)

1. 保存并 [激活](#activate-rule) 规则。

1. 创建消息. [了解详情](../messages/get-started-content.md#create-new-message)

1. 选择 **[!UICONTROL Marketing]** 类别。

   ![](assets/message-rules-ex-category-maktg.png)

1. 选择 **[!UICONTROL Email]** 和 **[!UICONTROL Push Notification]** 渠道。

   ![](assets/message-rules-ex-channels.png)

1. 您可以单击 **[!UICONTROL Frequency rule]** 链接以查看将应用于所选类别和渠道的频率规则。

1. [设计](../design/design-emails.md) 和 [发布](../messages/publish-manage-message.md) 你的留言。

在此方案中，单个用户档案：
* 每月最多可接收12条营销消息；
* 但在收到4个推送通知后，将从营销推送通知中排除。
