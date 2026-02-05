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
mini-toc-levels: 1
source-git-commit: 5ccbddb37c0f45b6dd004cb4b70378b300228c0c
workflow-type: tm+mt
source-wordcount: '1503'
ht-degree: 0%

---


# 创建挑战 {#create-challenges}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md)
* [访问和管理挑战和任务](access-loyalty-challenges.md)
* **创建挑战** ◀︎**您在这里**
* [创建任务](create-tasks.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 了解有关[可用性标签](../rn/releases.md#availability-labels)的更多信息。

本页介绍了创建忠诚度挑战的完整过程，从选择挑战类型和配置其属性到生成和发布将为客户带来挑战的历程。

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

   选择质询类型后，质询创建界面会打开，并显示多个配置选项卡。 首先配置挑战结构。

## 配置挑战结构 {#structure}

在&#x200B;**[!UICONTROL 结构]**&#x200B;选项卡中，定义挑战的组织方式：其属性、计划、要完成的任务和要提交的奖励。

### 定义质询属性并使用自定义元数据 {#properties}

1. 在&#x200B;**[!UICONTROL 质询属性]**&#x200B;窗格中，定义质询的全局设置：

   * **[!UICONTROL 名称]**：为您的质询输入描述性名称。 此名称显示在挑战清单中。
   * **[!UICONTROL 描述]**：输入描述来说明挑战的目的和目标。

1. 使用&#x200B;**[!UICONTROL 自定义元数据]**&#x200B;部分添加使用键/值对的自定义元数据。 此元数据可用于跟踪或与外部系统集成。

   ![](assets/challenge-create-properties.png)

### 安排挑战 {#schedule}

配置质询运行时间：

1. 选择&#x200B;**[!UICONTROL 打开计划]**&#x200B;图标：

   ![](assets/challenge-create-schedule.png)

1. 配置以下计划选项：

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

   在&#x200B;**[!UICONTROL 任务完成要求]**&#x200B;下拉列表中，选择：

   * **[!UICONTROL 客户选择完成1项任务]** - *客户可以选择并完成任何一项任务以获得奖励*
   * **[!UICONTROL 客户完成特定数量的任务]** - *客户必须完成定义数量的任务。 指定要完成的所需任务数。*

   +++

   +++Streak挑战

   在&#x200B;**[!UICONTROL Streak type]**&#x200B;下拉列表中，选择：

   * **连续**：客户必须在连续几天不间断地完成任务。 *示例：在星期一、星期二、星期三购买 — 错过一天就打破了条条纹。*

   * **非连续**：客户可以在完成之间有间隔的情况下完成任务。 *示例：在30天内完成7次购买，允许中断。*

   在&#x200B;**[!UICONTROL 条纹长度]**&#x200B;字段中，指定任务必须完成的次数。 *示例：将“7天购买连锁”设置为7。*

   +++

   +++顺序挑战

   在&#x200B;**[!UICONTROL 任务完成要求]**&#x200B;下拉列表中，选择：

   * **[!UICONTROL 客户选择完成1项任务]** - *客户可以选择并完成任何一项任务以获得奖励*
   * **[!UICONTROL 客户完成特定数量的任务]** - *客户必须按照您定义的确切顺序完成定义的数量任务。 缺少任务或跳过任务会中断序列。 指定要完成的所需任务数*

   +++

1. 默认情况下，标准和顺序难题允许客户跨多个事务处理完成任务。 要要求在一项事务中完成所有任务，请选择&#x200B;**[!UICONTROL 设置]**&#x200B;图标并打开下面的选项。

   ![](assets/challenge-create-single-transaction.png)

将任务添加到挑战后，配置客户完成这些任务将获得的奖励。

### 配置奖励 {#rewards}

奖励是客户在完成挑战后获得的忠诚度积分或福利。

要配置何时以及如何提供奖励，请执行以下操作：

1. 在&#x200B;**[!UICONTROL 奖励投放]**&#x200B;下拉菜单中，选择何时投放奖励：

   * **[!UICONTROL 在挑战完成时提供奖励]**：在客户完成整个挑战时提供奖励\
     *示例：完成所有5项任务后奖励100分*

   * **[!UICONTROL 在任务完成里程碑完成时提供奖励，因为挑战已取得进展]**：奖励在客户完成单个任务时递增（仅适用于需要多个任务的挑战）\
     *示例：任务1后奖励10分，任务2后奖励20分，任务3后奖励50分*

1. 选择您的奖励提供者。 这是您的忠诚度解决方案，用于管理客户点数和奖励。

   ![](assets/challenge-create-reward-type.png)

1. 根据您选择的投放方式配置奖励金额：

   +++完成质询后提供奖励

   指定客户完成整个质询时要给予的总奖励金额。

   *在以下示例中，完成挑战后，客户将获得100分。*

   ![](assets/challenge-create-reward-total.png)

   +++

   +++在任务完成里程碑时交付奖励

   指定任务完成里程碑的奖励金额。 此选项允许您创建渐进式奖励，当客户完成挑战时提高他们的积极性。

   对于您想要提供奖励的任何任务，切换奖励选项，并指定客户完成该特定任务时要奖励的点数。 您可以选择仅奖励某些任务完成 — 例如，如果您有10个任务，则可能仅奖励任务1、5和10。

   *在以下示例中，完成第一个任务时客户会获得10分，完成第二个任务后会再获得50分。*

   ![](assets/challenge-create-reward-milestones.png)

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

1. 对于每个阶段，单击添加消息按钮为该阶段创建消息。

1. 选择所需的渠道： **[!UICONTROL 应用程序内]**、**[!UICONTROL 电子邮件]**&#x200B;或&#x200B;**[!UICONTROL 推送通知]**，然后选择相关的渠道配置。

1. 选择![](assets/do-not-localize/Smock_More_18_N.svg)图标并选择&#x200B;**[!UICONTROL 编辑]**&#x200B;来设计您的消息内容。

   ![](assets/challenge-create-messaging.png)

在以下部分中了解如何为特定渠道创建消息： [应用程序内消息](../in-app/get-started-in-app.md) - [电子邮件](../email/get-started-email.md) - [推送通知](../push/get-started-push.md)

完成报文传送配置后，定义哪些客户有资格参与该挑战。

## 选择挑战受众 {#audience}

定义哪些客户可以参与您的忠诚度挑战。

1. 导航到&#x200B;**[!UICONTROL 受众]**&#x200B;选项卡，然后单击&#x200B;**[!UICONTROL 选择受众]**&#x200B;按钮。

   ![](assets/challenge-create-audience.png)

1. 在受众选择对话框中，从可用Adobe Experience Platform受众列表中选择您的目标受众，然后选择&#x200B;**[!UICONTROL 添加受众]**。 [了解如何使用受众](../audience/about-audiences.md)。

您的挑战现已完全配置其结构、内容、消息传递和目标受众。 要启动它，您必须发布挑战及其关联的历程。

## 发起挑战 {#launch}

启动质询需要&#x200B;**三个步骤**：(1)发布质询，(2)生成历程，(3)发布历程。 必须完成所有这三个步骤，才能将挑战传递给客户。

1. 查看您的挑战配置以确保已完成所有必填字段。

1. 单击![](assets/do-not-localize/Smock_More_18_N.svg)图标并选择&#x200B;**[!UICONTROL 发布]**。

   ![](assets/challenge-create-publish.png)

1. 选择&#x200B;**[!UICONTROL 生成历程]**&#x200B;以创建将编排质询投放的历程。

   ![](assets/challenge-create-generate-journey.png)

1. Journey Optimizer会自动创建处于“草稿”状态的旅程。 历程以名称格式&#x200B;*&quot;历程： [挑战名称]&quot;*&#x200B;显示在历程清单中。 [了解有关历程清单的更多信息](../building-journeys/journey-ui.md)。

   ![](assets/challenge-create-journey.png)

1. 打开旅程并发布。 该历程将在您指定的挑战开始日期自动开始，并根据您的配置交付内容和消息。 [了解如何发布历程](../building-journeys/publish-journey.md)。

1. 挑战开始后，在[历程报告](../reports/journey-global-report-cja.md)中监控性能和消息投放。

>[!NOTE]
>
>可以自定义自动生成的历程以添加其他逻辑或消息传递。 但是，直接对历程所做的更改不会同步回挑战配置。 如果您稍后编辑挑战，则在重新生成历程时，所有历程自定义项都将丢失。
