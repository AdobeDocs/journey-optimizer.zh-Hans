---
solution: Journey Optimizer
product: journey optimizer
title: 允许列表
description: 了解如何使用允许列表
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
keywords: 允许列表，列表，安全，配置
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 14%

---

# 允许列表 {#allow-list}

可以在以下位置定义特定的安全发送列表 [沙盒](../administration/sandboxes.md) 级别。

利用此允许列表，可指定单独的电子邮件地址或域，这些地址或域将是唯一有权接收您从特定沙盒发送的电子邮件的收件人或域。

>[!NOTE]
>
>此功能在生产沙盒和非生产沙盒上可用。

例如，在可能出现错误的非生产实例上，该允许列表可确保不会出现将不需要的报文发送到真实客户地址的风险，从而为测试目的提供安全的环境。

此外，当允许列表处于活动状态但为空时，不会发出任何邮件。 因此，如果您遇到一些严重问题，可以使用此功能停止所有传出通信 [!DNL Journey Optimizer] 直到你把问题解决了。 了解更多关于 [允许列表逻辑](#logic).

>[!CAUTION]
>
>此功能仅适用于电子邮件渠道。

## 访问允许列表 {#access-allowed-list}

要访问允许的电子邮件地址和域的详细列表，请转到 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件配置]**，并选择 **[!UICONTROL 允许列表]**.

![](assets/allow-list-access.png)

>[!CAUTION]
>
>查看、导出和管理允许列表的权限仅限于 [历程管理员](../administration/ootb-product-profiles.md#journey-administrator). 了解有关管理的更多信息 [!DNL Journey Optimizer] 用户在中拥有的访问权限 [本节](../administration/permissions-overview.md).

要将允许列表导出为CSV文件，请选择 **[!UICONTROL 下载CSV]** 按钮。

使用 **[!UICONTROL 删除]** 按钮以永久删除条目。

您可以搜索电子邮件地址或域，并筛选 **[!UICONTROL 地址类型]**. 选中后，您可以清除显示在列表顶部的筛选器。

![](assets/allowed-list-filtering-example.png)

## 激活允许列表 {#enable-allow-list}

要激活允许列表，请执行以下步骤。

1. 访问  **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件配置]** > **[!UICONTROL 允许列表]** 菜单。

1. 选择切换按钮。

   ![](assets/allow-list-edit.png)

1. 选择 **[!UICONTROL 激活允许列表]**. 允许列表现在处于活动状态。

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >激活允许列表后，它需要5分钟才能在您的历程和营销活动中生效。

当功能处于活动状态时，将应用允许列表逻辑。 有关详细信息，请参阅[此部分](#logic)。

>[!NOTE]
>
>激活后，在执行历程时，以及在使用测试消息时，将应用允许列表功能 [验证](../email/preview.md#send-proofs) 和测试历程 [测试模式](../building-journeys/testing-the-journey.md).

## 取消激活允许列表 {#deactivate-allow-list}

要取消激活允许列表，请执行以下步骤。

1. 访问  **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件配置]** > **[!UICONTROL 允许列表]** 菜单。

1. 选择切换按钮。

   ![](assets/allow-list-edit-active.png)

1. 选择 **[!UICONTROL 取消激活允许列表]**. 该允许列表不再处于活动状态。

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >停用允许列表后，它需要5分钟才能在您的历程和营销活动中生效。

停用该功能时，不应用允许列表逻辑。 有关详细信息，请参阅[此部分](#logic)。

## 将实体添加到允许列表 {#add-entities}

要向特定沙盒的允许列表中添加新的电子邮件地址或域，您可以 [手动填充列表](#manually-populate-list)，或使用 [API调用](#api-call-allowed-list).

>[!NOTE]
>
>允许列表最多可包含1,000个条目。

### 手动填充允许列表 {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="将地址或域添加到允许列表"
>abstract="您可以通过逐个选择新电子邮件地址或域，将它们手动添加到允许列表中。"

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="将地址或域添加到允许列表"
>abstract="您可以通过逐个选择新电子邮件地址或域，将它们手动添加到允许列表中。"

您可以手动填充 [!DNL Journey Optimizer] 通过允许列表界面添加电子邮件地址或域。

>[!NOTE]
>
>您一次只能添加一个电子邮件地址或域。

为此，请执行以下步骤。

1. 选择 **[!UICONTROL 添加电子邮件或域]** 按钮。

   ![](assets/allowed-list-add-email.png)

1. 选择地址类型：**[!UICONTROL 电子邮件地址]**&#x200B;或&#x200B;**[!UICONTROL 域地址]**。

1. 输入要向其发送电子邮件的电子邮件地址或域。

   >[!NOTE]
   >
   >确保输入有效的电子邮件地址（例如 abc@company.com）或域（例如 abc.company.com）。

1. 如果需要，请指定原因。

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >中允许包含32到126之间的所有ASCII字符 **[!UICONTROL 原因]** 字段。 可在[此页面](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters){target="_blank"}上找到完整列表以供参考。

1. 单击&#x200B;**[!UICONTROL 提交]**。

### 使用API调用添加实体 {#api-call-allowed-list}

要填充允许列表，您还可以使用调用禁止API `ALLOWED` 的值 `listType` 属性。 例如：

![](assets/allow-list-api.png)

您可以执行 **添加**， **删除** 和 **Get** 操作。

了解有关在中进行API调用的更多信息 [ADOBE EXPERIENCE PLATFORM API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html){target="_blank"} 参考文档。

## 下载允许列表 {#download-allowed-list}

要将允许列表导出为CSV文件，请执行以下步骤：

1. 选择 **[!UICONTROL 下载CSV]** 按钮。

   ![](assets/allowed-list-download-csv.png)

1. 等待文件生成。

   ![](assets/allowed-list-download-generate.png)

   >[!NOTE]
   >
   >下载时间取决于文件大小，即允许列表上的地址数量。
   >
   >对于给定的沙盒，一次可以处理一个下载请求。

1. 文件生成后，您将收到通知。 单击屏幕右上方的铃铛图标可显示铃铛图标。

1. 单击通知本身以下载文件。

   ![](assets/allowed-list-download-notification.png)

   >[!NOTE]
   >
   >该链接的有效期限为24小时。

## 允许列表逻辑 {#logic}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_logic"
>title="管理允许列表"
>abstract="激活允许列表后，只有包含在允许列表中的收件人才能收到来自此沙盒的电子邮件。如果停用，则所有收件人都将收到电子邮件。"

当允许列表为 [活动](#enable-allow-list)，则以下逻辑适用：

* 如果允许列表为 **空**，将不会发送电子邮件。

* 如果实体为 **在允许列表上**，而不是禁止列表上，则电子邮件将发送给对应的收件人。 但是，如果实体也在 [禁止显示列表](../reports/suppression-list.md)，相应的收件人将不会收到电子邮件，原因是 **[!UICONTROL 已隐藏]**.

* 如果实体为 **不在允许列表上** （不在禁止列表上），相应的收件人将不会收到电子邮件，原因是 **[!UICONTROL 不允许]**.

>[!NOTE]
>
>具有的配置文件 **[!UICONTROL 不允许]** 在消息发送过程中排除状态。 因此，虽然 **历程报表** 将显示这些用户档案在整个历程中移动([读取区段](../building-journeys/read-segment.md) 和 [消息活动](../building-journeys/journeys-message.md))，则 **电子邮件报告** 不会将它们包含在 **[!UICONTROL 已发送]** 量度，因为在发送电子邮件之前已将它们过滤掉。
>
>了解更多关于 [实时报告](../reports/live-report.md) 和 [全局报告](../reports/global-report.md).

当允许列表为 [已停用](#deactivate-allow-list)，您从当前沙盒发送的所有电子邮件都会发送给所有收件人（前提是它们不在禁止列表上），包括真实的客户地址。

## 排除报告 {#reporting}

当允许列表处于活动状态时，您可以检索由于不在允许列表中而未发送的电子邮件地址或域。 为此，您可以使用 [Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target="_blank"} 进行以下API调用。

获取 **电子邮件数量** 由于收件人不在允许列表上而未发送，请使用以下查询：

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

获取 **电子邮件地址列表** 由于收件人不在允许列表上而未发送，请使用以下查询：

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
