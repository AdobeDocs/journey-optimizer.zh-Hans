---
solution: Journey Optimizer
product: journey optimizer
title: 带来忠诚度挑战
description: 了解如何在Adobe Journey Optimizer中创建和配置忠诚度挑战。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="私人测试版" type="Informative"
source-git-commit: dbed4ffeb63ec3c58ff61845bbdb91fd2d51e69b
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---


# 创建挑战 {#create-challenges}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md) — 概述、工作流程、先决条件
* [访问忠诚度挑战](access-loyalty-challenges.md) — 清点和筛选
* **创建挑战** ◀︎**您位于此处** — 生成并配置挑战
* [创建任务](create-tasks.md) — 定义挑战任务
* [管理挑战](manage-challenges.md) — 编辑、监视、优化

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私有测试版**&#x200B;中，可能在您的环境中不可用。 要请求获取访问权限，请联系您的Adobe代表。 了解有关[可用性标签](../rn/releases.md#availability-labels)的更多信息。

## 工作原理 {#how-it-works}

<!-- SCHEMA: Visual workflow showing the 5 main steps with icons: Create challenge → Add tasks → Design content cards → Configure messaging → Review and publish -->

按照以下工作流程创建和启动忠诚度挑战：

1. **创建挑战** — 定义基本挑战属性，包括名称、类型（标准、条纹或顺序）、受众和日期范围。

1. **添加任务** — 定义客户必须完成的特定操作，包括任务类型（购买、支出、访问等）、数量、产品过滤器和奖励。

1. **设计内容卡** — 使用客户设备上显示的Journey Optimizer内容卡创建挑战的可视化表示形式。

1. **配置消息传送**（可选） — 为关键阶段（启动、进行中和完成）设置多渠道消息（应用程序内、电子邮件、推送、短信）。

1. **审核并发布** — 使用测试配置文件测试您的挑战，然后发布该挑战以供您的目标受众使用。

## 创建挑战 {#create-challenge}

<!-- SCREENSHOT: Challenge creation screen showing challenge properties form with fields for name, type, audience, dates -->

要创建新的忠诚度挑战，请执行以下操作：

1. 导航到Journey Optimizer中的&#x200B;**[!UICONTROL 忠诚度挑战]**。

1. 选择&#x200B;**[!UICONTROL 挑战]**&#x200B;选项卡。

1. 选择&#x200B;**[!UICONTROL 创建挑战]**。

1. 配置质询属性：

   **质询名称**：输入质询的描述性名称。 此名称显示在挑战清单中，可帮助您识别挑战。

   **质询类型**：选择以下类型之一：
   * **[!UICONTROL Standard]**：客户以任意顺序完成任意指定数量的任务
   * **[!UICONTROL 条纹]**：客户连续多次完成同一任务
   * **[!UICONTROL 顺序]**：客户按定义的顺序完成任务

   **目标受众**：选择定义谁可以参与此质询的受众区段。 在创建挑战之前，必须在Experience Platform中创建受众。 有关详细信息，请参阅[受众入门](../audience/about-audiences.md)。

   **开始日期**：将质询设为可供客户使用。

   **结束日期**：设置质询过期且不再接受新完成的时间。

<!-- VISUAL: Comparison table or diagram showing the three challenge types (Standard, Streak, Sequential) with examples of each -->

### 添加任务 {#add-tasks}

任务定义客户为了获得奖励必须完成的特定操作或里程碑。 您可以配置任务类型（购买、支出、访问、参与、自定义事件）、数量、产品过滤器和奖励。

根据您的挑战类型，客户完成任务的方式有所不同：

* **标准挑战**：以任意顺序完成任意指定数量的任务
* **连续挑战**：连续多次完成同一任务
* **连续挑战**：按定义的顺序完成任务

若要向挑战添加任务，请选择“任务”部分中的&#x200B;**[!UICONTROL 添加任务]**，然后配置任务属性。

有关创建和配置任务的详细说明，请参阅[创建任务](create-tasks.md)。

### 配置内容卡片 {#configure-content-cards}

<!-- SCREENSHOT: Content cards configuration section in the challenge editor -->

内容卡在客户设备上提供了挑战的可视化表示形式，显示了挑战信息、进展和奖励。 了解有关[内容卡](../content-card/get-started-content-card.md)的更多信息。

<!-- VISUAL: Example content card designs showing different states: challenge start, in-progress with progress bar, completion with reward -->

要为挑战配置内容卡，请执行以下操作：

1. 在挑战编辑器中，导航到&#x200B;**[!UICONTROL 内容卡]**&#x200B;部分。

1. 选择&#x200B;**[!UICONTROL 创建内容卡]**&#x200B;或选择现有模板。

1. 设计内容卡：
   * 添加图像、文本和品牌元素
   * 包含[个性化令牌](../personalization/personalization-syntax.md)以显示特定于客户的信息
   * 显示挑战进度指示器
   * 显示奖励和激励

1. 配置内容卡片的显示时间：
   * **质询开始**：当质询可用时显示
   * **进行中**：客户积极参与时显示
   * **完成**：在客户完成所有任务后显示

1. 预览不同设备上的内容卡以确保正确显示。

1. 保存内容卡配置。

有关设计和个性化内容卡的更多信息，请参阅[设计内容卡](../content-card/design-content-card.md)。

### 配置消息传送 {#configure-messaging}

<!-- SCREENSHOT: Messaging configuration section showing the three lifecycle stages: Launch, In-progress, Completion -->

设置多渠道消息，在挑战生命周期的关键阶段吸引客户。

<!-- VISUAL: Timeline diagram showing when each message type is sent during the challenge lifecycle -->

要针对您的挑战配置消息传送，请执行以下操作：

1. 在挑战编辑器中，导航到&#x200B;**[!UICONTROL 消息传送]**&#x200B;部分。

1. 为每个生命周期阶段配置消息：

   **启动邮件** — 在挑战开始时通知客户：
   * 选择渠道： [应用程序内](../in-app/get-started-in-app.md)、[电子邮件](../email/get-started-email.md)、[推送通知](../push/get-started-push.md)或[短信](../sms/get-started-sms.md)
   * 设计包含挑战详细信息和call-to-action的消息
   * 设置时间：当质询开始或安排在特定时间后立即发送

   **正在进行的消息** — 在挑战期间保持客户参与：
   * 定义触发器条件（例如，50%完成、特定任务完成）
   * 创建提醒消息以鼓励继续参与
   * 包括进度更新和后续步骤

   **完成消息** — 庆祝成功并提供奖励：
   * 祝贺客户完成挑战
   * 确认奖励分配
   * 提供申请奖励的说明
   * 建议下一个挑战或行动

有关为特定渠道创建消息的更多信息，请参阅：

* [应用程序内消息文档](../in-app/get-started-in-app.md)
* [电子邮件文档](../email/get-started-email.md)
* [推送通知文档](../push/get-started-push.md)
* [SMS消息文档](../sms/get-started-sms.md)

## 查看并发布挑战 {#review-and-publish}

<!-- SCREENSHOT: Review screen showing summary of challenge configuration with all components listed -->

在发布挑战之前：

1. **查看所有组件**：验证质询属性、任务、奖励、内容卡和消息发送配置。

1. **测试体验**：使用[测试配置文件](../test-approve/test-profiles.md)验证内容卡显示和任务触发器行为。

1. **发布**：选择&#x200B;**[!UICONTROL 发布]**，使您的目标受众可以使用质询。

<!-- SCREENSHOT: Journeys inventory showing the auto-generated journey in Draft status with name format "Challenge: [Challenge Name]" -->

当您发布质询时，Journey Optimizer会自动创建处于草稿状态的[历程](../building-journeys/journey-gs.md)。 自动生成历程以名称格式“挑战： [挑战名称]”显示在历程清单中。

要让客户了解此难题，请执行以下操作：

1. 导航到Journey Optimizer中的&#x200B;**[!UICONTROL 历程]**&#x200B;清单。

1. 找到自动生成的历程（其名称将以“Challenge：”作为前缀）。

1. [激活历程](../building-journeys/publishing-the-journey.md)。

历程会在您指定的质询开始日期自动开始。

>[!NOTE]
>
>自动生成的历程显示在历程清单中，并且可以根据需要进行自定义。 但是，直接对历程所做的更改不会同步回挑战配置。

## 后续步骤 {#next-steps}

* [管理挑战](manage-challenges.md) — 了解如何编辑、监控和优化挑战
* [了解忠诚度挑战](get-started.md) — 查看特性和功能

