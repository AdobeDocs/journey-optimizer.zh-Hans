---
solution: Journey Optimizer
product: journey optimizer
title: 创建您的第一个历程
description: 使用 Adobe Journey Optimizer 构建您的首个历程的关键步骤
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 历程，第一，开始，快速入门，受众，事件，操作
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 99099cb6b705cb5a7b97652154c42f0565fdfdb9
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 33%

---

# 创建您的第一个历程 {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="创建历程"
>abstract="借助 **Adobe Journey Optimizer**，可以利用存储在事件或数据源中的上下文数据构建实时编排用例。"

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="历程"
>abstract="设计客户历程以营造个性化的上下文体验。通过 Journey Optimizer，可用存储在事件或数据源中的上下文数据构建实时编排用例。**概述**&#x200B;选项卡显示一个仪表板，其中包含与您的历程相关的关键量度。**浏览**&#x200B;选项卡显示现有历程的列表。"


Adobe Journey Optimizer 包含全渠道编排画布，使营销人员在开展营销推广和一对一客户互动时能够让这两项工作协调一致。用户界面让您可以轻松地将活动从调色板拖放到画布中以构建历程。

![](assets/journey38.png)

创建历程的主要步骤如下：

![](assets/journey-creation-process.png)

➡️ [在视频中了解此功能](#video)

[此页面](journey-ui.md)中详细介绍了历程用户界面。


## 先决条件 {#start-prerequisites}

要在历程中发送消息，需要满足以下先决条件：

1. **配置事件**：如果要在收到事件时统一触发历程，则需要配置事件。 您可以定义预期信息及其处理方式。 此步骤由&#x200B;**技术用户**&#x200B;执行。 [了解更多信息](../event/about-events.md)。

   ![](assets/jo-event7bis.png)

1. **创建受众**：您的历程还可以侦听Adobe Experience Platform受众，以便向一组指定的用户档案批量发送消息。 为此，您需要创建受众。 [了解更多信息](../audience/about-audiences.md)。

   ![](assets/segment2.png)

1. **配置数据源**：您可以定义与系统的连接，以检索将在您的历程中使用的其他信息，例如在您的条件中。 在预配时还会配置内置 Adobe Experience Platform 数据源。如果您仅利用历程中事件的数据，则不需要执行此步骤。此步骤由&#x200B;**技术用户**&#x200B;执行。 [了解详情](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **配置操作**：如果您使用第三方系统发送消息，则可以创建自定义操作。 在此[部分](../action/action.md)中了解详情。 此步骤由&#x200B;**技术用户**&#x200B;执行。 如果您使用Journey Optimizer内置消息功能，则只需将渠道操作添加到历程并设计内容即可。

   ![](assets/custom2.png)



作为数据工程师，有关配置历程（包括数据源、事件和操作）的步骤详情，请参见[此部分](../configuration/about-data-sources-events-actions.md)。


>[!NOTE]
>
>可在[此页面](../start/guardrails.md)中找到有关历程护栏和限制的详细信息。

## 创建多步历程 {#jo-build}

要创建多步历程，请执行以下步骤：

1. 在“历程管理”菜单部分中，单击&#x200B;**[!UICONTROL 历程]**。

1. 单击&#x200B;**[!UICONTROL 创建历程]**&#x200B;按钮以创建新旅程。

1. 编辑历程的配置窗格以定义历程的名称并设置其属性。 在[此页面](journey-properties.md)中了解如何设置历程的属性。

   ![](assets/jo-properties.png)

然后，您可以开始设计历程。

## 设计旅程 {#jo-design}

全渠道历程设计器帮助您使用直观的拖放界面通过目标受众、基于实时客户或业务交互的更新以及全渠道消息来构建多步骤历程。

![](assets/journey38.png)

1. 首先，将事件或&#x200B;**读取受众**&#x200B;活动从调色板拖放到画布中。 要了解有关历程设计的更多信息，请参阅[此章节](using-the-journey-designer.md)。

   ![](assets/read-segment.png)

1. 拖放个人将执行的后续步骤。 例如，您可以添加一个条件，后跟一个渠道操作。 要了解有关活动的更多信息，请参阅[此章节](about-journey-activities.md)。

## 测试历程 {#jo-test}

构建历程后，您可以在发布之前对其进行测试。 Journey Optimizer提供“测试模式”，当测试用户档案在旅程中移动时查看测试用户档案，并在激活之前检测潜在错误。 通过运行快速测试，您可以检查历程是否正确运行，以便您能够放心地发布它们。

在此[部分](testing-the-journey.md)中了解详情

## 发布历程 {#jo-pub}

您必须发布历程以激活它，并使其可供新配置文件进入该历程。 在发布历程之前，请验证其是否有效以及是否没有错误。 您无法发布包含错误的历程。 在此[部分](publishing-the-journey.md)中了解有关历程发布的更多信息。

![](assets/jo-journeyuc2_32bis.png)

发布后，您可以使用专用的报告工具监控旅程，以衡量旅程的有效性。

![](assets/jo-dynamic_report_journey_12.png)

在此[部分](../reports/live-report.md)中了解有关历程报告的更多信息。

请注意，您可以复制现有历程或创建新版本的历程。 在[此页面](journey-ui.md)中了解详情