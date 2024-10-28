---
solution: Journey Optimizer
product: journey optimizer
title: Publish历程
description: 了解如何报告您的历程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 发布，历程，实时，有效性，检查
source-git-commit: 9b4ff0325d099252a5785aa13cfe0f1fe42acac6
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# 历程画布中的实时报告 {#report-journey}

>[!NOTE]
>
>如果您在历程实时报告中看不到数据，则必须扩展您的访问权限以包含&#x200B;**[!UICONTROL 查看历程报告]**&#x200B;权限。 [了解详情](../administration/permissions.md)

发布历程后，**实时报告**&#x200B;直接在历程画布中提供过去24小时的量度。

显示的事件发生在过去24小时内，事件与其显示之间至少间隔2分钟，通常在5分钟内。

![](assets/journey_live_report.png)

对于您的实时历程，您有权访问：

* **[!UICONTROL 输入的配置文件]**：退出历程的个人总数（包括错误）。
* **[!UICONTROL 已退出分析]**：由于退出条件而退出该活动的个人总数。
* **[!UICONTROL 有错误的配置文件]**：历程中遇到错误的个人总数。
* **[!UICONTROL 丢弃的用户档案]**：由于以下原因之一从历程丢弃的个人总数：

   * 对于&#x200B;**受众资格**&#x200B;活动，如果受众资格的预期动词与历程收到的动词不匹配（例如，“已退出”而不是“已实现”），则可能会发生放弃。
   * 对于&#x200B;**事件触发的**&#x200B;历程，如果个人过早尝试重新进入历程或不允许重新进入，则可能发生放弃。
   * 在&#x200B;**循环**&#x200B;历程中，如果个人已在历程中，并且再次进入策略未设置为“强制再次进入”，则会在每个循环中计入放弃。
   * 在&#x200B;**读取受众**&#x200B;活动中，如果没有为导出的个人设置标识，或者收到的标识命名空间与历程的预期命名空间不匹配，则会发生放弃。

对于每个实时历程中的每项活动，您均有权访问：

* **[!UICONTROL 已输入]**：进入此活动的个人总数。
* **[!UICONTROL 已退出（符合退出条件）]**：由于退出条件而退出该活动的个人总数。
* **[!UICONTROL 错误]**：在该活动上发生错误的个人总数。
