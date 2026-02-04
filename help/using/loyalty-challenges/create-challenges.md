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
source-git-commit: e683461c6adbf45cacb30692e23927175685f9fb
workflow-type: tm+mt
source-wordcount: '1445'
ht-degree: 0%

---


# 创建挑战 {#create-challenges}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md) — 概述、工作流程、先决条件
* [访问和管理忠诚度挑战](access-loyalty-challenges.md) — 库存、挑战和任务管理
* **创建挑战** ◀︎**您位于此处** — 生成并配置挑战
* [创建任务](create-tasks.md) — 定义挑战任务

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私有测试版**&#x200B;中，可能在您的环境中不可用。 要请求获取访问权限，请联系您的Adobe代表。 了解有关[可用性标签](../rn/releases.md#availability-labels)的更多信息。

## 创建挑战 {#create-the-challenge}

1. 在Journey Optimizer中导航到&#x200B;**[!UICONTROL 忠诚度挑战(Beta)]**。

1. 选择&#x200B;**[!UICONTROL 挑战]**&#x200B;选项卡，然后选择&#x200B;**[!UICONTROL 创建挑战]**。

   ![](assets/challenge-create.png)

1. 选择挑战类型：

   * **[!UICONTROL Standard]**：客户以任意顺序完成任意指定数量的任务\
     *示例：完成5个可用任务中的3个*

   * **[!UICONTROL 条纹]**：客户连续多次完成同一任务\
     *示例：连续7天购买*

   * **[!UICONTROL 顺序]**：客户按定义的顺序完成任务\
     *示例： Purchase → Review → Share（必须按此顺序完成）*

## 配置挑战结构 {#structure}

在&#x200B;**[!UICONTROL 结构]**&#x200B;选项卡中，定义挑战的组织方式：其属性、计划、要完成的任务和要提交的奖励。

### 定义质询属性并使用自定义元数据 {#properties}

1. 在&#x200B;**[!UICONTROL 质询属性]**&#x200B;窗格中，定义质询的全局设置：

   * **[!UICONTROL 名称]**：为您的质询输入描述性名称。 此名称显示在挑战清单中。
   * **[!UICONTROL 描述]**：输入描述来说明挑战的目的和目标。

   ![](assets/challenge-create-properties.png)

1. 使用&#x200B;**[!UICONTROL 自定义元数据]**&#x200B;部分添加使用键/值对的自定义元数据。 此元数据可用于跟踪或与外部系统集成。

### 安排挑战 {#schedule}

选择&#x200B;**[!UICONTROL 打开计划]**&#x200B;图标，配置质询运行时间：

![](assets/challenge-create-schedule.png)

* **[!UICONTROL 开始日期和时间]**：将质询设为可供客户使用。
* **[!UICONTROL 结束日期和时间]**：设置质询过期且不再接受新完成的时间。
* **[!UICONTROL 时区]**：默认情况下质询使用收件人的本地时区。
* **[!UICONTROL 任务必须完成]**：选择客户何时可以完成任务：

   * **[!UICONTROL 在挑战赛期间的任何时间]**：客户可以在挑战赛开始日期和结束日期之间的任何时间完成任务。
   * **[!UICONTROL 在一天中的特定小时内]**：通过设置&#x200B;**[!UICONTROL 开始时间]**&#x200B;和&#x200B;**[!UICONTROL 结束时间]**，将任务完成限制为特定的每日小时数。

挑战计划现已配置完成。 接下来，添加客户需要完成的任务。

### 添加任务 {#add-tasks}

任务定义客户要获得奖励必须完成的特定操作。 您可以配置任务类型（购买、支出）、数量、产品筛选器和其他属性。

要向挑战添加任务，请执行以下步骤：

1. 在&#x200B;**[!UICONTROL 任务]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 添加任务]**。

   ![](assets/challenge-create-add-task.png)

1. **[!UICONTROL 任务清单]**&#x200B;打开。 从列表中选择一个或多个任务，然后选择&#x200B;**[!UICONTROL 添加]**。 要创建新任务，请选择&#x200B;**[!UICONTROL 新建]**。 [了解如何创建和配置任务](create-tasks.md)。

1. 指定何时将质询视为已完成。 可用的设置取决于质询类型：

   +++标准挑战

   **[!UICONTROL 任务完成要求]** — 选择：

   * **[!UICONTROL 客户选择完成1项任务]**：客户可以选择并完成任何一项任务以获得奖励
   * **[!UICONTROL 客户完成特定数量的任务]**：客户必须完成定义数量的任务。 指定所需数字 — *示例：完成5项任务中的3项*

   +++

   +++Streak挑战

   * **[!UICONTROL 条纹]**：

      * **连续**：客户必须在连续几天无中断地完成任务 — *示例：在星期一、星期二、星期三购买 — 错过一天有中断现象*

      * **非连续**：客户可以在完成之间有间隔的情况下完成任务 — *示例：在30天内完成了7次购买，允许中断*

   * **[!UICONTROL 连续长度]**：指定任务必须完成的次数 — *示例：对于“7天购买连续”，设置为7*

   +++

   +++顺序挑战

   **[!UICONTROL 任务完成要求]** — 选择：

   * **[!UICONTROL 客户选择完成1项任务]**：客户可以选择并完成任何一项任务以获得奖励
   * **[!UICONTROL 客户完成特定数量的任务]**：客户必须按照您定义的确切顺序完成已定义的数量任务。 缺少任务或跳过任务会中断序列。 指定所需的编号（例如，完成5个任务中的3个）

   *示例：任务1 （购买）→任务2 （审阅）→任务3 （共享） — 必须按此顺序完成*

   +++

1. 默认情况下，标准和顺序难题允许客户跨多个事务处理完成任务。 要要求在一项事务中完成所有任务，请选择![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL 设置]**&#x200B;图标并切换下面的选项。

   ![](assets/challenge-create-single-transaction.png)

将任务添加到挑战后，配置客户完成这些任务将获得的奖励。

### 配置奖励 {#rewards}

奖励是客户在完成挑战后获得的忠诚度积分或福利。 配置何时以及如何提供奖励。

1. 在&#x200B;**[!UICONTROL 奖励投放]**&#x200B;下拉列表中，选择何时投放奖励：

   * **[!UICONTROL 在挑战完成时提供奖励]**：在客户完成整个挑战时提供奖励\
     *示例：完成所有5项任务后奖励100分*

   * **[!UICONTROL 在任务完成里程碑完成时提供奖励，因为挑战已取得进展]**：奖励在客户完成单个任务时递增（仅适用于需要多个任务的挑战）\
     *示例：任务1后奖励10分，任务2后奖励20分，任务3后奖励50分*

1. 选择您的奖励提供者。 这是您的忠诚度解决方案，用于管理客户点数和奖励。

1. 根据您选择的投放方式配置奖励金额：

   +++完成质询后提供奖励

   指定客户完成整个质询时要给予的总奖励金额。

   ![](assets/challenge-create-reward-total.png)

   **示例**：客户在完成挑战时获得100分。

   +++

   +++在任务完成里程碑时交付奖励

   指定任务完成里程碑的奖励金额。 此选项允许您创建渐进式奖励，当客户完成挑战时提高他们的积极性。

   对于您想要提供奖励的任何任务，切换奖励选项，并指定客户完成该特定任务时要奖励的点数。 您可以选择仅奖励某些任务完成 — 例如，如果您有10个任务，则可能仅奖励任务1、5和10。

   ![](assets/challenge-create-reward-milestones.png)

   **示例**：完成第一个任务时客户可获得10分，完成第二个任务后可获得50分，完成质询后可获得60分。

   >[!TIP]
   >
   >考虑提高后续任务的奖励值，以在整个挑战中保持客户参与。

   +++

在配置包含任务和奖励的挑战结构后，设计内容卡以向客户显示挑战。

## 配置内容卡片 {#configure-content-cards}

内容卡以可视方式展示您在客户设备上的挑战，显示挑战信息、进度和奖励。 [了解有关内容卡的更多信息](../content-card/create-content-card.md)。

要为挑战配置内容卡，请执行以下操作：

1. 导航到&#x200B;**[!UICONTROL Content]**&#x200B;选项卡，并为内容卡输入&#x200B;**[!UICONTROL Name]**。

1. 选择&#x200B;**[!UICONTROL 渠道配置]**。 渠道配置包含用于发送消息的所有技术参数，如标头参数、子域、移动应用程序等。 [了解有关渠道配置的更多信息](../configuration/channel-surfaces.md)。

1. 选择&#x200B;**[!UICONTROL 编辑内容]**&#x200B;以设计内容卡。 [了解如何设计和个性化内容卡](../content-card/design-content-card.md)。

   ![](assets/challenge-create-content.png)

配置内容卡后，设置消息传送功能，在整个挑战生命周期中吸引客户。

### 配置消息传送 {#configure-messaging}

设置多渠道消息，在挑战生命周期的关键阶段吸引客户。 消息传送是可选的，但建议设置此消息以最大限度地提高客户参与度。

1. 导航到&#x200B;**[!UICONTROL 消息]**&#x200B;选项卡，并为每个生命周期阶段配置消息：

   * **启动**&#x200B;消息：在挑战开始时通知客户
   * **进行中**&#x200B;消息：让客户参与提醒和进度更新
   * **完成**&#x200B;消息：庆祝成功并确认奖励分配

1. 对于每个阶段，选择&#x200B;**[!UICONTROL 添加[阶段]消息]**（其中[阶段]表示Launch、In-progress或Completion）以创建该阶段的消息。

1. 选择所需的渠道： **[!UICONTROL 应用程序内]**、**[!UICONTROL 电子邮件]**&#x200B;或&#x200B;**[!UICONTROL 推送通知]**，然后选择相关的渠道配置。

1. 选择![](assets/do-not-localize/Smock_More_18_N.svg)图标并选择&#x200B;**[!UICONTROL 编辑]**&#x200B;来设计您的消息内容。

   ![](assets/challenge-create-messaging.png)

了解如何为特定渠道创建消息：

* [应用程序内消息](../in-app/get-started-in-app.md)
* [电子邮件消息](../email/get-started-email.md)
* [推送通知](../push/get-started-push.md)

完成报文传送配置后，定义哪些客户有资格参与该挑战。

## 选择挑战受众 {#audience}

定义哪些客户可以参与您的忠诚度挑战。

1. 导航到&#x200B;**[!UICONTROL 受众]**&#x200B;选项卡，然后选择&#x200B;**[!UICONTROL 选择受众]**&#x200B;按钮。

   ![](assets/challenge-create-audience.png)

1. 从可用的Adobe Experience Platform受众列表中选择您的目标受众。 [了解如何使用受众](../audience/about-audiences.md)。

1. 选择&#x200B;**[!UICONTROL 添加受众]**。

您的挑战现已完全配置其结构、内容、消息传递和目标受众。 最后一步是生成和发布旅程。

## 生成并发布历程 {#review-and-publish}

生成历程，以编排挑战交付和客户互动。 为此，请选择&#x200B;**[!UICONTROL 生成历程]**。

![](assets/challenge-create-generate-journey.png)

Journey Optimizer会自动创建处于草稿状态的[历程](../building-journeys/journey-gs.md)。 自动生成历程以名称格式“挑战： [挑战名称]”显示在历程清单中。

![](assets/challenge-create-journey.png)

审查历程配置（如果需要），然后发布历程，以便客户能够提出挑战。 [了解如何发布历程](../building-journeys/publish-journey.md)。

该历程将在您指定的挑战开始日期自动开始，并根据您的配置交付内容和消息。

>[!NOTE]
>
>可以自定义自动生成的历程以添加其他逻辑或消息传递。 但是，直接对历程所做的更改不会同步回挑战配置。 如果您稍后编辑挑战，则在重新生成历程时，所有历程自定义项都将丢失。
