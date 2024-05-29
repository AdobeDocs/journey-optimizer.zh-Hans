---
solution: Journey Optimizer
product: journey optimizer
title: 全局报告
description: 了解如何使用全局报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: 46d69dd422090a67c377acd6c8f44c4468e27f69
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 3%

---

# 全局报告入门 {#global-report}

>[!NOTE]
>
> 如果使用查询服务时通过API进行自定义查询，则报告可能会有延迟。

使用 **[!UICONTROL 全局报告]** 用于衡量选定时间段内历程和投放的影响。

* 如果要在历程上下文中定位历程或投放，请从 **[!UICONTROL 历程]** 菜单，访问您的旅程，然后单击 **[!UICONTROL 查看报告]** 按钮。 然后，您可以找到历程、电子邮件、短信和推送全局报表。

  ![](assets/report_journey.png)

* 如果要定位促销活动，请从 **[!UICONTROL 营销活动]** 菜单，访问您的营销策划，然后单击 **[!UICONTROL 报表]** 按钮。

  ![](assets/report_campaign.png)

* 如果要从 **[!UICONTROL 实时报告]** 到 **[!UICONTROL 全局报告]** 对于您的投放，请单击 **[!UICONTROL 所有时间]** 选项卡切换器中的。

  ![](assets/report_5.png)

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅 [此页面](#list-of-components-global)

## 自定义仪表板 {#modify-dashboard}

可以通过更改时间段、调整小组件大小或删除小组件来修改每个报表仪表板。 更改构件只会影响当前用户的仪表板。 其他用户将看到自己的功能板或默认设置的功能板。

1. 从全局报表中，选择开始和结束时间以定向特定数据。

   ![](assets/report_modify_1.png)

1. 对于涉及多个已配置的历程报表 **[!UICONTROL 操作]**，选择特定的 **[!UICONTROL 操作]** 从下拉菜单中。

1. 如果您只想定向一条或多条定期消息，请从 **[!UICONTROL 执行时间]** 下拉菜单。

   ![](assets/report_modify_12.png)

1. 选择是否要通过切换栏从报表中排除测试事件。 有关测试事件的详细信息，请参阅 [此页面](../building-journeys/testing-the-journey.md).

   请注意 **[!UICONTROL 排除测试事件]** 选项仅适用于历程报表。

   ![](assets/report_modify_2.png)

1. 单击 **[!UICONTROL 修改]** 以开始自定义您的仪表板。

   ![](assets/report_modify_3.png)

1. 通过拖动小部件的右下角调整其大小。

   ![](assets/report_modify_4.png)

1. 单击 **[!UICONTROL 移除]** 以删除任何您不需要的构件。

   ![](assets/report_modify_5.png)

1. 如果对小部件的显示顺序和大小满意，请单击 **[!UICONTROL 保存]**.

1. 要自定义数据的显示方式，可以从不同的可视化选项（如图形、表格和圆环图）进行切换。

   ![](assets/report_modify_10.png)

您的信息板现已保存。 您的不同更改将重新应用以供以后使用实时报告。 如果需要，请使用 **[!UICONTROL 重置]** 用于恢复默认构件和构件顺序的选项。

## 导出报告 {#export-reports}

您可以轻松地将不同的报表导出为PDF或CSV格式，以便您共享或打印它们。 导出报告的步骤详见以下选项卡。

➡️ [在视频中了解此功能](#video-csv)


>[!BEGINTABS]

>[!TAB 将报表导出为CSV文件]

1. 在报表中，单击 **[!UICONTROL 导出]** 并选择 **[!UICONTROL CSV文件]** 在整体报表级别生成CSV文件。

   ![](assets/export_1.png)

1. 您还可以选择从特定构件导出数据。 单击 **[!UICONTROL 将构件数据导出到CSV]** 在选定小组件旁边。

   ![](assets/export_3.png)

1. 您的文件会自动下载，并位于本地文件中。

   如果在报表级别生成文件，则它包含每个小组件的详细信息，包括其标题和数据。

   如果在小组件级别生成文件，则它会专门提供选定小组件的数据。

>[!TAB 将报表导出为PDF文件]

1. 在报表中，单击 **[!UICONTROL 导出]** 并选择 **[!UICONTROL PDF文件]**.

   ![](assets/export_2.png)

1. 在“打印”窗口中，根据需要配置文档。 请注意，选项可能因您的浏览器而异。

1. 选择打印报表或将报表另存为PDF。

1. 找到要保存文件的文件夹，根据需要重命名它，然后单击“保存”。

您的报表现在可以在PDF文件中查看或共享。



>[!ENDTABS]


### 导出报表（视频） {#video-csv}

请观看以下操作方法视频，了解如何下载适用于单个报表和单个小部件的CSV报表。

>[!VIDEO](https://video.tv.adobe.com/v/3424603?quality=12)



>[!CONTEXTUALHELP]
>id="ajo_report_campaign_CTR"
>title="CTR"
>abstract="CTR小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_clicks"
>title="点击次数"
>abstract="点击小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_delivered"
>title="已送达"
>abstract="投放的构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_overview"
>title="Campaign概述"
>abstract="Campaign概述构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_funnel"
>title="营销活动漏斗结果"
>abstract="Campaign漏斗结果构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_tracking_link"
>title="跟踪的链接标签"
>abstract="跟踪的链接标签小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_displays"
>title="显示"
>abstract="显示构件"

<!--campaign email-->

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_delivered_click"
>title="交付和点击趋势"
>abstract="已交付并点击趋势小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_delivery_status"
>title="投放状态"
>abstract="投放状态构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_sending_statistics"
>title="发送统计数据"
>abstract="发送统计构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracking_statistics"
>title="跟踪统计数据"
>abstract="跟踪统计构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_domains"
>title="电子邮件域"
>abstract="电子邮件域小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracked_link"
>title="跟踪的链接标签"
>abstract="跟踪链接标签小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracked_link_urls"
>title="跟踪的链接URL"
>abstract="跟踪的链接URL小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_subjects"
>title="电子邮件主题"
>abstract="电子邮件主题小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_bounce_reasons"
>title="退回原因"
>abstract="退回原因小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_exclude"
>title="排除原因"
>abstract="排除原因小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_error"
>title="错误原因"
>abstract="错误原因小组件"


<!--campaign push-->

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_sending_statistics"
>title="发送统计数据"
>abstract="发送统计构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracking_statistics"
>title="跟踪统计数据"
>abstract="跟踪统计构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracked_link"
>title="跟踪的链接标签"
>abstract="跟踪链接标签小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracked_link_urls"
>title="跟踪的链接URL"
>abstract="跟踪的链接URL小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_bounce_reasons"
>title="退回原因"
>abstract="退回原因小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_exclude"
>title="排除的原因"
>abstract="排除的原因小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_email_error"
>title="错误原因"
>abstract="错误原因小组件"

<!--campaign inapp-->


>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_impression"
>title="展示和点击趋势"
>abstract="Impression &amp; Click趋势构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_clicks"
>title="点击次数"
>abstract="点击小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_displays"
>title="显示"
>abstract="显示构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracking_data"
>title="跟踪数据"
>abstract="跟踪数据构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracked_link"
>title="跟踪的链接标签"
>abstract="跟踪的链接标签小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracked_link_urls"
>title="跟踪的链接URL"
>abstract="跟踪的链接URL小组件"

<!--campaign sms-->


>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_delivered_click"
>title="交付和点击趋势"
>abstract="已交付并点击趋势小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_delivery_status"
>title="投放状态"
>abstract="投放状态构件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_tracked_link"
>title="跟踪的链接标签"
>abstract="跟踪链接标签小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_tracked_link_urls"
>title="跟踪的链接URL"
>abstract="跟踪的链接URL小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_inbound"
>title="SMS入站消息"
>abstract="短信入站消息小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_message_type"
>title="SMS消息类型"
>abstract="短信消息类型小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_providers"
>title="短信提供商"
>abstract="短信提供商小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_bounce"
>title="退回原因"
>abstract="退回原因小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_exclude"
>title="排除原因"
>abstract="排除原因小组件"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_error"
>title="错误原因"
>abstract="错误原因小组件"
