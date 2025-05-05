---
solution: Journey Optimizer
product: journey optimizer
title: 允许列表
description: 了解如何使用允许列表
feature: Deliverability
topic: Content Management
role: Admin
level: Experienced
keywords: 允许列表，列表，安全，配置
exl-id: 70ab8f57-c132-4de1-847b-11f0ab14f422
source-git-commit: 2af0e9237bbcc79456a31042ed8e42233bbccac3
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 15%

---

# 允许列表 {#allow-list}

可以在[沙盒](../administration/sandboxes.md)级别定义特定的安全发送列表。

利用此允许列表，可指定单独的电子邮件地址或域，这些地址或域将是唯一有权接收您从特定沙盒发送的电子邮件的收件人或域。

>[!CAUTION]
>
>此功能仅适用于电子邮件渠道。 它在生产沙盒和非生产沙盒上可用。

例如，在可能出现错误的非生产实例上，该允许列表可确保不会出现将不需要的消息发送到真实客户地址的风险，从而提供了一个用于测试的安全环境。

此外，当允许列表处于活动状态但为空时，不会发出任何邮件。 因此，如果您遇到一些严重问题，可以使用此功能停止来自[!DNL Journey Optimizer]的所有传出通信，直到您修复问题为止。 了解有关[允许列表逻辑](#logic)的更多信息。

此外，您还可以利用 Journey Optimizer **禁止 REST API** 来使用禁止和允许列表控制传出消息。[了解如何使用禁止 REST API](https://developer.adobe.com/journey-optimizer-apis/references/suppression/){target="_blank"}

## 访问允许的列表 {#access-allowed-list}

要访问允许的电子邮件地址和域的详细列表，请转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件设置]**，然后选择&#x200B;**[!UICONTROL 允许列表]**。

![](assets/allow-list-access.png)

>[!CAUTION]
>
>查看、导出和管理允许列表的权限仅限于[Journey Administrators](../administration/ootb-product-profiles.md#journey-administrator)。 了解有关在[此部分](../administration/permissions-overview.md)中管理[!DNL Journey Optimizer]个用户的访问权限的更多信息。

要将允许列表导出为CSV文件，请选择&#x200B;**[!UICONTROL 下载CSV]**&#x200B;按钮。

使用&#x200B;**[!UICONTROL 删除]**&#x200B;按钮永久删除条目。

您可以搜索电子邮件地址或域，并筛选&#x200B;**[!UICONTROL 地址类型]**。 选择后，您可以清除显示在列表顶部的过滤器。

![](assets/allowed-list-filtering-example.png)

## 激活允许列表 {#enable-allow-list}

要激活允许列表，请执行以下步骤。

1. 访问&#x200B;**[!UICONTROL 频道]** > **[!UICONTROL 电子邮件配置]** > **[!UICONTROL 允许列表]**&#x200B;菜单。

1. 选择“切换”按钮。

   ![](assets/allow-list-edit.png)

1. 选择&#x200B;**[!UICONTROL 激活允许列表]**。 允许列表现在处于活动状态。

   ![](assets/allow-list-enable.png)

   >[!NOTE]
   >
   >激活允许列表后，它将延迟10分钟，然后才能在您的历程和营销活动中生效。 同样，对允许列表和禁止列表进行的更新最多可能需要10分钟才能反映出来。

当功能处于活动状态时，将应用允许列表逻辑。 有关详细信息，请参阅[此部分](#logic)。

>[!NOTE]
>
>激活后，在执行历程时，以及在测试带有[校样](../content-management/proofs.md)的消息和使用[测试模式](../building-journeys/testing-the-journey.md)测试历程时，将应用允许列表功能。

## 取消激活允许列表 {#deactivate-allow-list}

要取消激活允许列表，请执行以下步骤。

1. 访问&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件配置]** > **[!UICONTROL 允许列表]**&#x200B;菜单。

1. 选择切换按钮。

   ![](assets/allow-list-edit-active.png)

1. 选择&#x200B;**[!UICONTROL 取消激活允许列表]**。 该允许列表不再处于活动状态。

   ![](assets/allow-list-deactivate.png)

   >[!NOTE]
   >
   >停用允许列表后，该列表将在您的旅程和营销活动中生效，并会延迟10分钟。 同样，更新允许列表和禁止显示列表可能需要10分钟才能反映出来。

当停用该功能时，允许的列表逻辑不适用。 有关详细信息，请参阅[此部分](#logic)。

## 将实体添加到允许列表 {#add-entities}

要向特定沙盒的允许列表中添加新的电子邮件地址或域，您可以[手动填充列表](#manually-populate-list)，或使用[API调用](#api-call-allowed-list)。

>[!NOTE]
>
>允许列表最多可包含1,000个条目。

### 手动为允许列表填充数据 {#manually-populate-list}

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add_header"
>title="将地址或域添加到允许列表"
>abstract="您可以通过逐个选择新电子邮件地址或域，将它们手动添加到允许列表中。"

>[!CONTEXTUALHELP]
>id="ajo_admin_allowed_list_add"
>title="将地址或域添加到允许列表"
>abstract="您可以通过逐个选择新电子邮件地址或域，将它们手动添加到允许列表中。"

您可以通过用户界面添加电子邮件地址或域，手动填充[!DNL Journey Optimizer]允许列表。

>[!NOTE]
>
>一次只能添加一个电子邮件地址或域。

为此，请执行以下步骤。

1. 选择&#x200B;**[!UICONTROL 添加电子邮件或域]**&#x200B;按钮。

   ![](assets/allowed-list-add-email.png)

1. 选择地址类型：**[!UICONTROL 电子邮件地址]**&#x200B;或&#x200B;**[!UICONTROL 域地址]**。

1. 输入您要向其发送电子邮件的电子邮件地址或域。

   >[!NOTE]
   >
   >确保输入有效的电子邮件地址（例如 abc@company.com）或域（例如 abc.company.com）。

1. 如果需要，请指定原因。

   ![](assets/allowed-list-add-email-address.png)

   >[!NOTE]
   >
   >在&#x200B;**[!UICONTROL 原因]**&#x200B;字段中允许包含介于32和126之间的所有ASCII字符。 例如，可以在[此页面](https://en.wikipedia.org/wiki/ASCII#Printable_characters){target="_blank"}上找到完整列表。

1. 单击&#x200B;**[!UICONTROL 提交]**。

### 使用API调用添加实体 {#api-call-allowed-list}

若要填充允许列表，您还可以使用`listType`属性的`ALLOWED`值调用禁止显示API。 例如：

![](assets/allow-list-api.png)

您可以执行&#x200B;**添加**、**删除**&#x200B;和&#x200B;**获取**&#x200B;操作。

了解有关在[Adobe Experience Platform API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=zh-Hans){target="_blank"}参考文档中进行API调用的更多信息。

## 下载允许列表 {#download-allowed-list}

要将允许列表导出为CSV文件，请执行以下步骤：

1. 选择&#x200B;**[!UICONTROL 下载CSV]**&#x200B;按钮。

   ![](assets/allowed-list-download-csv.png)

1. 等待文件生成。

   ![](assets/allowed-list-download-generate.png)

   >[!NOTE]
   >
   >下载时间取决于文件大小，即允许列表上的地址数。
   >
   >对于给定的沙盒，一次可处理一个下载请求。

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

当允许列表为[活动](#enable-allow-list)时，将应用以下逻辑：

* 如果允许列表为&#x200B;**空**，则不会发送电子邮件。

* 如果实体在允许列表&#x200B;**中是**&#x200B;而不是在禁止显示列表中，则电子邮件将发送给相应的收件人。 但是，如果该实体也在[禁止显示列表](../reports/suppression-list.md)中，则对应的收件人将不会收到电子邮件，原因是&#x200B;**[!UICONTROL 禁止显示]**。

* 如果实体不在允许列表&#x200B;**上（不在禁止列表上），则相应的收件人将不会收到电子邮件，原因是**&#x200B;[!UICONTROL &#x200B;不允许&#x200B;]&#x200B;**。**

>[!NOTE]
>
>在邮件发送过程中排除状态为&#x200B;**[!UICONTROL 不允许]**&#x200B;的用户档案。 因此，虽然&#x200B;**历程报告**&#x200B;会显示这些用户档案在历程中移动（[读取受众](../building-journeys/read-audience.md)和[消息活动](../building-journeys/journeys-message.md)），但&#x200B;**电子邮件报告**&#x200B;不会将它们包含在&#x200B;**[!UICONTROL 已发送]**&#x200B;指标中，因为在发送电子邮件之前已将它们过滤掉。
>
>了解有关[实时报告](../reports/live-report.md)和[Customer Journey Analytics报告](../reports/report-gs-cja.md)的更多信息。

当允许列表为[已停用](#deactivate-allow-list)时，您从当前沙箱发送的所有电子邮件都将发送给所有收件人（前提是它们不在禁止列表中），包括真正的客户地址。

## 排除报告 {#reporting}

当允许列表处于活动状态时，您可以检索由于不在允许列表中而从发送中排除的电子邮件地址或域。 为此，您可以使用[Adobe Experience Platform查询服务](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=zh-Hans){target="_blank"}进行下面的API调用。

要获取由于收件人不在允许列表上而未发送的&#x200B;**个电子邮件**，请使用以下查询：

```sql
SELECT count(distinct _id) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID = '<MESSAGE_EXECUTION_ID>' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```

要获取由于收件人不在允许列表上而未发送的&#x200B;**电子邮件地址**&#x200B;列表，请使用以下查询：

```sql
SELECT distinct(_experience.customerJourneyManagement.emailChannelContext.address) from cjm_message_feedback_event_dataset WHERE
_experience.customerJourneyManagement.messageExecution.messageExecutionID IS NOT NULL AND
_experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus = 'exclude' AND
_experience.customerJourneyManagement.messageDeliveryfeedback.messageExclusion.reason = 'EmailNotAllowed'
```
