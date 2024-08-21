---
solution: Journey Optimizer
product: journey optimizer
title: 实时报告
description: 了解如何使用实时报告中的数据
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 8dd48bb2-a805-4c46-a16c-c68173a9ac08
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 1%

---

# 实时报告入门 {#live-report}

>[!AVAILABILITY]
>
>当前的报告体验将从10月版起停用。 在此日期之后，新的报告体验将成为标准。 我们建议您熟悉新特性和功能，以确保顺利过渡。 [开始使用Journey Optimizer的新报告界面。](report-gs-cja.md)

使用&#x200B;**[!UICONTROL 实时报告]**在内置仪表板中实时衡量和可视化您的历程和消息的影响和性能。
在发送投放或从**[!UICONTROL 最近24小时]**&#x200B;选项卡执行历程后，**[!UICONTROL 实时报告]**&#x200B;中的数据可用。

* 如果要在历程上下文中定位历程，请从&#x200B;**[!UICONTROL 历程]**&#x200B;菜单访问您的历程，然后单击&#x200B;**[!UICONTROL 查看报告]**&#x200B;按钮。

  ![](assets/report_journey.png)

* 如果要定位促销活动，请从&#x200B;**[!UICONTROL 促销活动]**&#x200B;菜单访问您的促销活动，然后单击&#x200B;**[!UICONTROL 报表]**&#x200B;按钮。

  ![](assets/report_campaign.png)

* 如果要将投放从&#x200B;**[!UICONTROL 全局报告]**&#x200B;切换到&#x200B;**[!UICONTROL 实时报告]**，请从选项卡切换器中单击&#x200B;**[!UICONTROL 最近24小时]**。

  ![](assets/report_3.png)

有关Adobe Journey Optimizer中可用的每个量度的详细列表，请参阅[此页面](#list-of-components-live)。

## 自定义仪表板 {#modify-dashboard}

可以通过调整小部件的大小或删除小部件来修改每个报表仪表板。 更改构件只会影响当前用户的仪表板。 其他用户将看到自己的功能板或默认设置的功能板。

1. 从&#x200B;**[!UICONTROL 操作]**&#x200B;下拉列表中，选择是否要报告历程的一个特定操作。

1. 选择是否要通过切换栏从报表中排除测试事件。 有关测试事件的详细信息，请参阅[此页面](../building-journeys/testing-the-journey.md)。

   请注意，**[!UICONTROL 排除测试事件]**&#x200B;选项仅适用于历程报表。

   ![](assets/report_modify_6.png)

1. 要调整小部件的大小或删除小部件，请单击&#x200B;**[!UICONTROL 修改]**。

   ![](assets/report_modify_7.png)

1. 通过拖动小部件的右下角调整其大小。

   ![](assets/report_modify_8.png)

1. 单击&#x200B;**[!UICONTROL 删除]**&#x200B;可删除不需要的任何构件。

   ![](assets/report_modify_9.png)

1. 如果对显示顺序和小部件的大小满意，请单击&#x200B;**[!UICONTROL 保存]**。

1. 要自定义数据的显示方式，可以从不同的可视化选项（如图形、表格和圆环图）进行切换。

   ![](assets/report_modify_11.png)

您的信息板现已保存。 您的不同更改将重新应用以供以后使用实时报告。 如果需要，请使用&#x200B;**[!UICONTROL 重置]**&#x200B;选项恢复默认小部件和小部件的顺序。

## 导出您的报告 {#export-reports}

您可以轻松地将不同的报表导出为PDF或CSV格式，以便您共享或打印它们。

>[!BEGINTABS]

>[!TAB 将报告导出为PDF文件]

1. 在报表中，单击&#x200B;**[!UICONTROL 导出]**&#x200B;并选择&#x200B;**[!UICONTROL PDF文件]**。

   ![](assets/export_6.png)

1. 在“打印”窗口中，根据需要配置文档。 请注意，选项可能因您的浏览器而异。

1. 选择打印报表或将报表另存为PDF。

1. 找到要保存文件的文件夹，根据需要重命名它，然后单击“保存”。

您的报表现在可以在PDF文件中查看或共享。

>[!TAB 将报告导出为CSV文件]

1. 在报表中，单击&#x200B;**[!UICONTROL 导出]**&#x200B;并选择&#x200B;**[!UICONTROL CSV文件]**&#x200B;以生成整个报表级别的CSV文件。

   ![](assets/export_4.png)

1. 您还可以选择从特定构件导出数据。 单击所选构件旁边的&#x200B;**[!UICONTROL 将构件数据导出到CSV]**。

   ![](assets/export_5.png)

1. 您的文件会自动下载，并位于本地文件中。

   如果在报表级别生成文件，则它包含每个小组件的详细信息，包括其标题和数据。

   如果在小组件级别生成文件，则它会专门提供选定小组件的数据。

>[!ENDTABS]
