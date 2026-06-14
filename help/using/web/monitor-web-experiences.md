---
title: 监测 Web 体验
description: 了解如何在Journey Optimizer中监控Web体验
feature: Web Channel, Reporting, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: d89795bb-c51d-4d1f-b7ed-2b2c5d278922
TQID: https://experienceleague.adobe.com/CEjKwnKx1ixUKA-mO7FfWGXaW9FyO-I-ZYyYm0scs88
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c618a0dc-1818-4c6d-9916-0d92e6796f24
  - id: d056adbe-402d-4f42-9746-f3d424e598b1
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
source-git-commit: a5a700893cc89b29f5fbc214cf3e73f6069144c2
workflow-type: tm+mt
source-wordcount: 317
ht-degree: 3%

---

# 监测 Web 体验 {#monitor-web-experiences}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何通过检查Web报表并在特定页面元素上设置点击跟踪来监控Adobe Journey Optimizer中的实时Web体验。

>[!ENDSHADEBOX]

## 检查Web报告 {#check-web-reports}

在Web体验上线后，您可以检查[历程报告](../reports/journey-global-report-cja-web.md)和[促销活动报告](../reports/campaign-global-report-cja-web.md)的&#x200B;**[!UICONTROL Web]**&#x200B;选项卡，以比较展示次数、点击率和与网页的互动次数等元素。

<!--You can check the **[!UICONTROL Web]** tab of the campaign reports. Learn more about the campaign web [live report](../reports/campaign-live-report.md#web-tab) and [global report](../reports/campaign-global-report-cja.md#web).-->

要进一步改进Web体验监控，您还可以跟踪网站任何特定元素的点击次数。 这样，您就可以在Web报表中显示对该元素的点击次数。 [了解如何操作](#use-click-tracing)

## 使用点击跟踪 {#use-click-tracking}

Web设计器允许您选择网站的任何元素并跟踪对该元素的点击。

此信息对于改善网站用户的体验非常有用。 例如，如果[Web报表](../reports/campaign-global-report-cja-web.md)显示有许多用户单击了一个实际上不可点击的元素，则您可能希望添加指向该元素的链接。

1. 在页面中选择元素，然后从上下文菜单中选择&#x200B;**[!UICONTROL 单击跟踪元素]**。

   ![](assets/web-designer-click-track.png)

   >[!NOTE]
   >
   >可以选择任何项目（无论是否可单击）。

1. 相应的跟踪操作会自动显示在左侧的&#x200B;**[!UICONTROL 单击跟踪]**&#x200B;窗格中。

   ![](assets/web-designer-click-track-pane.png)

1. 添加有意义的标签以管理所有跟踪的元素并轻松地在报表中找到它们。 **[!UICONTROL CSS选择器]**&#x200B;字段显示用于查找所选元素的信息。

1. 重复上述步骤，根据需要选择点击跟踪所需数量的其他元素。 相应的操作全部列在左窗格中。

   ![](assets/web-designer-click-tracking-actions.png)

1. 要删除某个元素的点击跟踪，请选择相应的删除图标。

一旦您的营销活动开始，您就可以检查营销活动网站[实时报告](../reports/campaign-live-report.md#web-tab)和[Customer Journey Analytics报告](../reports/campaign-global-report-cja-web.md)中每个元素的点击次数。
