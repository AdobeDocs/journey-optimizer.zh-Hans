---
solution: Journey Optimizer
product: journey optimizer
title: 创建您的第一个历程
description: 使用 Adobe Journey Optimizer 生成您的首个历程的关键步骤
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 历程，第一，开始，快速入门，受众，事件，操作
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 25%

---

# 创建您的第一个历程 {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="创建历程"
>abstract="借助 **Adobe Journey Optimizer**，可以利用存储在事件或数据源中的上下文数据生成实时编排用例。"

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="历程"
>abstract="设计客户历程以营造个性化的上下文体验。Journey Optimizer使您可以利用存储在事件或数据源中的情境数据构建实时编排用例。 **概述**&#x200B;选项卡显示一个仪表板，其中包含与您的历程相关的关键量度。**浏览**&#x200B;选项卡显示现有历程的列表。"

Adobe Journey Optimizer 包含全渠道编排画布，使营销人员在开展营销推广和一对一客户互动时能够让这两项工作协调一致。利用用户界面，可轻松地将活动从面板拖放到画布中以构建历程。 此历程用户界面在[此页面](journey-ui.md)中有详细介绍。

![历程画布示例](assets/journey38.png)


此页面上详细描述了创建历程的主要步骤。 其简化如下：

![历程创建步骤：创建、设计、测试和发布](assets/journey-creation-process.png)


构建多步骤客户历程，实时启动跨渠道交互、优惠和消息序列。 此方法确保客户根据其行为和相关业务信号在最佳时刻参与。 根据行为、上下文数据和业务事件定义Target受众。 先决条件取决于您的用例以及您正在构建的[历程类型](entry-management.md#types-of-journeys)。

在开始构建历程之前，请确保已完成相关配置步骤：

* 如果要在收到事件时单独触发历程，请&#x200B;**配置事件**。 定义预期信息及其处理方式。 [了解详情](../event/about-events.md)。

<!--   ![](assets/jo-event7bis.png)  -->

* 您的历程还可以监听Adobe Experience Platform受众，以批量将消息发送到一组指定的用户档案。 为此，**创建受众**。 [了解详情](../audience/about-audiences.md)。

<!--   ![](assets/segment2.png)  -->

* 定义与系统的连接，以检索将在您的历程中使用的其他信息，例如在您的条件中。 此连接依赖于&#x200B;**数据源**。 [了解详情](../datasource/about-data-sources.md)。

<!--   ![](assets/jo-datasource.png)  -->

* Journey Optimizer附带[内置消息](../building-journeys/journeys-message.md)功能。 如果您使用第三方系统来发送消息，则可以&#x200B;**创建自定义操作**。 在此[部分](../action/action.md)中了解详情。

<!--    ![](assets/custom2.png)  -->


作为数据工程师，有关配置历程（包括数据源、事件和操作）的步骤详情，请参见[此部分](../configuration/about-data-sources-events-actions.md)。


>[!NOTE]
>
>可在[此页面](../start/guardrails.md)中找到有关历程护栏和限制的详细信息。

## 创建历程 {#jo-build}

要创建多步历程，请执行以下步骤：

1. 在“历程管理”菜单部分中，单击&#x200B;**[!UICONTROL 历程]**。

1. 单击&#x200B;**[!UICONTROL 创建历程]**&#x200B;按钮以创建新旅程。

1. 编辑历程的配置窗格以定义历程的名称并设置其属性。 了解如何在[此页面](journey-properties.md)上设置历程的属性。

   ![](assets/jo-properties.png)

然后，您可以开始设计历程。

## 设计旅程 {#jo-design}

全渠道历程设计器帮助您使用直观的拖放界面通过目标受众、基于实时客户或业务交互的更新以及全渠道消息来构建多步骤历程。

![](assets/journey38.png)

1. 首先，将事件或&#x200B;**读取受众**&#x200B;活动从调色板拖放到画布中。 要了解有关历程设计的更多信息，请参阅[此章节](using-the-journey-designer.md)。

   ![](assets/read-segment.png)

1. 首先，将事件或&#x200B;**读取受众**&#x200B;活动从调色板拖放到画布中。 要了解有关历程设计的更多信息，请参阅[此章节](using-the-journey-designer.md)。

## 测试历程 {#jo-test}

构建历程后，请在发布之前对其进行测试。 Journey Optimizer提供了&#x200B;**测试模式**，以便在测试配置文件在历程中移动时查看它们，并在激活之前检测潜在的错误。 运行快速测试可确保历程正确运行，以便您能够放心地发布它们。 在本节[&#128279;](testing-the-journey.md)中了解如何测试您的历程

您还可以在&#x200B;**练习**&#x200B;中执行您的历程。 历程试运行是 Adobe Journey Optimizer 中的一种特殊历程发布模式，使历程设计人员能够在不接触真实客户或更新轮廓信息的前提下，使用真实生产数据对历程进行测试。此功能有助于历程从业者在将其发布到实时状态之前获得对其历程设计和受众定位的信心。 在本节[&#128279;](journey-dry-run.md)中了解如何在练习模式下发布历程。

## 发布历程 {#jo-pub}

您必须发布历程以激活它，并使其可供新配置文件进入该历程。 在发布历程之前，请验证其是否有效并且没有错误。 您无法发布包含错误的历程。 在此[部分](publishing-the-journey.md)中了解有关历程发布的更多信息。

![](assets/jo-journeyuc2_32bis.png)

发布后，您可以使用专用的报告工具监控旅程，以衡量旅程的有效性。

![](assets/jo-dynamic_report_journey_12.png)

在此[部分](../reports/live-report.md)中了解有关历程报告的更多信息。

>[!NOTE]
>
>如果需要修改&#x200B;**实时**&#x200B;历程，请[创建历程的新版本](journey-ui.md#journey-versions)。
