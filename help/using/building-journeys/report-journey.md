---
solution: Journey Optimizer
product: journey optimizer
title: 发布历程
description: 了解如何报告您的历程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 发布，历程，实时，有效性，检查
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
source-git-commit: 62525caa9b065538c090b98d38c15dbd960dafe7
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 2%

---

# 历程画布中的实时报告 {#report-journey}

发布历程后，一旦激活[练习模式](journey-dry-run.md)，**实时报告**&#x200B;将直接在历程画布中提供过去24小时的量度。


>[!AVAILABILITY]
>
>如果您在历程实时报告中看不到数据，则必须扩展您的访问权限以包含&#x200B;**[!UICONTROL 查看历程报告]**&#x200B;权限。 [了解详情](../administration/permissions.md)


显示的事件发生在过去24小时内，事件与其显示之间至少间隔2分钟，通常在5分钟内。

![](assets/journey_live_report.png)

对于处于实时或[练习模式](journey-dry-run.md)的历程，您可以检查：

* **[!UICONTROL 输入的配置文件]**：进入历程的个人总数。
* **[!UICONTROL 退出配置文件]**：退出历程的个人总数（包括错误）。
* **[!UICONTROL 有错误的配置文件]**：历程中遇到错误的个人总数。
* **[!UICONTROL 丢弃的用户档案]**：由于以下原因之一从历程丢弃的个人总数：

   * 对于&#x200B;**受众资格**&#x200B;活动，如果受众资格的预期动词与历程收到的动词不匹配（例如，“已退出”而不是“已实现”），则可能会发生放弃。
   * 对于&#x200B;**事件触发的**&#x200B;历程，如果个人过早尝试重新进入历程或不允许重新进入，则可能发生放弃。
   * 在&#x200B;**循环**&#x200B;历程中，如果个人已在历程中，并且再次进入策略未设置为“强制再次进入”，则会在每个循环中计入放弃。
   * 在&#x200B;**读取受众**&#x200B;活动中，如果没有为导出的个人设置标识，或者收到的标识命名空间与历程的预期命名空间不匹配，则会发生放弃。

对于处于实时或[练习模式](journey-dry-run.md)的每个历程中的每个活动，您都可以访问：

* **[!UICONTROL 已输入]**：进入此活动的个人总数。 对于&#x200B;**操作**&#x200B;活动，由于它们不是在练习模式下执行，因此此量度表示用户档案通过。
* **[!UICONTROL 已退出（符合退出条件）]**：由于退出条件（包括错误）而退出该活动的个人总数。
* **[!UICONTROL 已退出（强制退出）]**：由于历程从业者配置而暂停历程时退出历程的个人总数。 对于处于练习模式的历程，此量度始终等于零。
* **[!UICONTROL 错误]**：在该活动上发生错误的个人总数。


>[!MORELIKETHIS]
>
>* [开始使用报告](../reports/gs-reports.md)
>* [发布您的历程](publishing-the-journey.md)
>* [历程练习](journey-dry-run.md)
>* [配置和跟踪您的历程量度](success-metrics.md)
>* [自定义历程报告](../reports/sharing-overview.md)