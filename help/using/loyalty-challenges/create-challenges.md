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
source-git-commit: fd87aeabfae1f07d8f7bea7057f0c6dd0559d024
workflow-type: tm+mt
source-wordcount: '1521'
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

按照以下工作流程创建和启动忠诚度挑战：

1. **[创建挑战](#create-the-challenge)** — 选择最符合您的忠诚度计划目标的挑战类型（标准、连续或顺序）。

1. **[配置挑战结构](#structure)** — 定义客户必须完成的挑战属性、计划、任务以及他们将获得的奖励。

1. **[配置内容信息卡](#configure-content-cards)** — 设计内容信息卡以直观地展示您在客户设备上的挑战，显示挑战信息、进度和奖励。

1. **[配置消息](#configure-messaging)**（可选） — 为关键阶段（启动、进行中和完成）设置多渠道消息（应用程序内、电子邮件、推送）。

1. **[选择挑战受众](#audience)** — 定义哪些客户有资格参与挑战。

1. **[生成并激活历程](#review-and-publish)** — 生成并激活关联的历程，以使您的目标受众能够看到挑战。

## 创建挑战 {#create-the-challenge}

1. 在Journey Optimizer中导航到&#x200B;**[!UICONTROL 忠诚度挑战(Beta)]**。

1. 选择&#x200B;**[!UICONTROL 挑战]**&#x200B;选项卡，然后选择&#x200B;**[!UICONTROL 创建挑战]**。

   ![](assets/challenge-create.png)

1. 选择挑战类型：

   * **[!UICONTROL Standard]**：客户以任意顺序完成任意指定数量的任务
   * **[!UICONTROL 条纹]**：客户连续多次完成同一任务
   * **[!UICONTROL 顺序]**：客户按定义的顺序完成任务

## 配置挑战结构 {#structure}

在“结构”选项卡中，您可以定义如何组织挑战：其属性、计划、要完成的任务以及要给予的奖励。

### 定义质询属性并使用自定义元数据 {#properties}

1. 在“质询属性”窗格中，配置质询属性：

   ![](assets/challenge-create-properties.png)

   **名称**：为您的质询输入描述性名称。 此名称显示在挑战清单中，可帮助您识别挑战。

   **描述**：输入质询的描述。

1. 使用&#x200B;**[!UICONTROL 自定义元数据]**&#x200B;部分添加使用键/值对的自定义元数据。 此元数据可用于跟踪、分段或与外部系统集成。

### 安排挑战 {#schedule}

通过选择![](assets/do-not-localize/schedule-icon.svg) **[!UICONTROL 打开计划]**&#x200B;图标计划挑战。

* **开始日期和时间**：向客户发出质询时设置（格式： mm/dd/yyyy， —：— AM/PM）。

* **结束日期和时间**：设置质询过期且不再接受新完成的时间（格式： mm/dd/yyyy， —：— AM/PM）。

* **时区**：默认情况下挑战使用收件人的本地时区。

* **任务必须完成**：选择客户何时可以完成任务：

   * **[!UICONTROL 在挑战赛期间的任何时间]**：客户可以在挑战赛开始日期和结束日期之间的任何时间完成任务
   * **[!UICONTROL 在一天中的特定小时内]**：通过设置&#x200B;**[!UICONTROL 开始时间]**&#x200B;和&#x200B;**[!UICONTROL 结束时间]**，将任务完成限制为特定的每日小时数

挑战计划现已配置完成。 您现在可以添加客户需要完成的任务。

### 添加任务 {#add-tasks}

任务定义客户为了获得奖励必须完成的特定操作或里程碑。 您可以配置任务类型（购买、支出、访问、参与、自定义事件）、数量、产品过滤器和奖励。

根据您的挑战类型，客户完成任务的方式有所不同：

* **标准挑战**：以任意顺序完成任意指定数量的任务
* **连续挑战**：连续多次完成同一任务
* **连续挑战**：按定义的顺序完成任务

要向挑战添加任务，请执行以下步骤：

1. 在&#x200B;**[!UICONTROL 任务]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 添加任务]**。

   ![](assets/challenge-create-add-task.png)

1. 此时将打开Tasks清单。 从列表中选择一个或多个任务，然后选择&#x200B;**[!UICONTROL 添加]**。 要创建新任务，请选择&#x200B;**[!UICONTROL 新建]**。

   有关创建和配置任务的详细说明，请参阅[创建任务](create-tasks.md)。

1. 在&#x200B;**[!UICONTROL 任务完成要求]**&#x200B;部分中，指定何时应将挑战视为已完成：

   * **[!UICONTROL 客户选择完成1项任务]**：客户可以选择并完成挑战中的任意一项任务以获得奖励
   * **[!UICONTROL 客户完成特定数量的任务]**：客户必须完成定义数量的任务。 输入所需的任务完成数。

1. 默认情况下，客户可通过多次交易完成任务。 若要要求在一个事务中完成所有任务，请选择![](assets/do-not-localize/settings-icon.svg) **[!UICONTROL 设置]**&#x200B;图标，然后打开&#x200B;**[!UICONTROL 单个事务]**&#x200B;选项。

   ![](assets/challenge-create-single-transaction.png)

### 配置奖励 {#rewards}

奖励是客户在完成挑战后获得的忠诚度积分或福利。 配置如何以及何时提供奖励以激励客户参与。

1. 在&#x200B;**[!UICONTROL 奖励投放]**&#x200B;下拉列表中，选择何时应投放奖励：

   * **[!UICONTROL 完成质询后提供奖励]**：当客户完成整个质询后，给予所有奖励
   * **[!UICONTROL 在任务完成里程碑完成时提供奖励，挑战进度已达]**：奖励在客户完成单个任务时递增（仅当挑战需要完成多个任务时可用）

1. 从下拉列表中选择您的奖励提供者。 这是您的忠诚度解决方案，用于管理客户点数和奖励。

1. 根据您选择的投放方式配置奖励金额：

   +++完成质询后提供奖励

   在挑战完成&#x200B;**的[会员积分数]积分**&#x200B;字段中，指定客户完成整个挑战时要给予的总奖励金额。

   字段名称显示您的会员积分名称，如所选提供商中所定义。 例如，如果您的提供商使用“Luma点数”，则字段显示“完成挑战时的Luma点数”。

   ![](assets/challenge-create-reward-total.png)

   **示例**：在上面的屏幕快照中，客户在完成挑战时获得100分。

   +++

   +++在任务完成里程碑时交付奖励

   指定任务完成里程碑的奖励金额。 此选项允许您创建渐进式奖励，当客户完成挑战时提高他们的积极性。

   对于您想要提供奖励的任何任务，切换奖励选项，并指定客户完成该特定任务时要奖励的点数。 您可以选择仅奖励某些任务完成 — 例如，如果您有10个任务，则可能仅奖励任务1、5和10。

   ![](assets/challenge-create-reward-milestones.png)

   **示例**：在上面的屏幕截图中，客户在完成第一个任务时可获得10分，在完成第二个任务后可获得50分，当挑战完成时可获得60分。

   >[!TIP]
   >
   >考虑提高后续任务的奖励值，以在整个挑战中保持客户参与。

   +++

挑战结构现在配置了任务和奖励。 您现在可以设计内容卡以向客户显示挑战。

## 配置内容卡片 {#configure-content-cards}

内容卡在客户设备上提供了挑战的可视化表示形式，显示了挑战信息、进展和奖励。 了解有关[内容卡](../content-card/create-content-card.md)的更多信息。

要为挑战配置内容卡，请执行以下操作：

1. 在挑战编辑器中，导航到&#x200B;**[!UICONTROL Content]**&#x200B;选项卡。

1. 输入内容卡的&#x200B;**[!UICONTROL 名称]**。

1. 选择关联的&#x200B;**[!UICONTROL 渠道配置]**。 渠道配置定义将内容交付给客户的方式和位置。 有关详细信息，请参阅[渠道配置](../configuration/channel-surfaces.md)。

1. 选择&#x200B;**[!UICONTROL 编辑内容]**&#x200B;以设计内容卡。

   ![](assets/challenge-create-content.png)

有关设计和个性化内容卡的更多信息，请参阅[设计内容卡](../content-card/design-content-card.md)。

内容卡现在已配置完成。 您现在可以设置报文传送服务，在整个挑战生命周期中吸引客户。

### 配置消息传送 {#configure-messaging}

设置多渠道消息，在挑战生命周期的关键阶段吸引客户。

1. 导航到&#x200B;**[!UICONTROL 消息]**&#x200B;选项卡。

1. 为每个生命周期阶段配置消息：

   ![](assets/challenge-create-messaging.png)

   * **启动邮件**：在挑战开始时通知客户并提供初始详细信息
   * **正在进行的消息**：通过提醒、进度更新和鼓励继续让客户参与挑战
   * **完成消息**：庆祝成功，确认奖励分配，并提出后续挑战或操作建议

1. 对于每个阶段，选择&#x200B;**[!UICONTROL 添加&#x200B;*阶段*消息]**&#x200B;为该阶段创建消息。

1. 选择所需的渠道： **[!UICONTROL 应用程序内]**、**[!UICONTROL 电子邮件]**&#x200B;或&#x200B;**[!UICONTROL 推送通知]**，然后选择相关的渠道配置。

1. 选择![](assets/do-not-localize/Smock_More_18_N.svg)图标并选择&#x200B;**[!UICONTROL 编辑]**&#x200B;来设计您的消息内容。

   有关为特定渠道创建消息的更多信息，请参阅：

   * [应用程序内消息文档](../in-app/get-started-in-app.md)
   * [电子邮件文档](../email/get-started-email.md)
   * [推送通知文档](../push/get-started-push.md)

1. 根据需要对每个阶段和渠道重复这些步骤。

消息传送配置现已完成。 您现在可以定义哪些客户有资格参与该挑战。

## 选择挑战受众 {#audience}

定义哪些客户有资格参与您的忠诚度挑战。

1. 导航到&#x200B;**[!UICONTROL 受众]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 选择受众]**&#x200B;按钮。

   ![](assets/challenge-create-audience.png)

1. 此时将显示所有可用的Adobe Experience Platform受众。 从列表中选择所需的受众。

1. 选择&#x200B;**[!UICONTROL 添加受众]**&#x200B;以确认您的选择。

您的挑战配置现已完成。 您现在可以生成历程以编排挑战投放。

## 生成并激活历程 {#review-and-publish}

完成挑战配置后，生成关联的历程，以编排挑战交付和客户交互。 为此，请选择&#x200B;**[!UICONTROL 生成历程]**。

![](assets/challenge-create-generate-journey.png)

Journey Optimizer会自动创建处于草稿状态的[历程](../building-journeys/journey-gs.md)。 自动生成历程以名称格式“挑战： [挑战名称]”显示在历程清单中。

根据需要查看历程配置，然后[激活历程](../building-journeys/publish-journey.md)以使客户能够查看挑战。

该历程将在您指定的挑战开始日期自动开始，并根据您的配置交付内容和消息。

>[!NOTE]
>
>如果需要，可以自定义自动生成的历程，以添加其他逻辑或消息传递。 但是，直接对历程所做的更改不会同步回挑战配置。 如果您稍后编辑挑战，则在重新生成历程时，所有历程自定义项都将丢失。

## 后续步骤 {#next-steps}

* [管理挑战](manage-challenges.md) — 了解如何编辑、监控和优化挑战
* [了解忠诚度挑战](get-started.md) — 查看特性和功能
