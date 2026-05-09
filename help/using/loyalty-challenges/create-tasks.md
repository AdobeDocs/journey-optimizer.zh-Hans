---
solution: Journey Optimizer
product: journey optimizer
title: 创建任务以应对忠诚度挑战
description: 了解如何在Adobe Journey Optimizer中创建和配置忠诚度挑战任务。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: c1e49173-69cc-4729-9f9a-afea2ccff3fa
source-git-commit: 384f4e4b4c3acd9f1f1d73d4b140845870b31289
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 18%

---

# 创建任务 {#create-tasks}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md)
* [访问和管理挑战和任务](access-loyalty-challenges.md)
* [创建挑战](create-challenges.md)
* **创建任务** ◀}︎**您在这里**
* [监测忠诚度挑战表现](loyalty-reporting.md)
* [忠诚度挑战API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](../rn/releases.md)。

任务定义客户在忠诚度挑战中必须完成的特定操作或里程碑以获取奖励。 您可以配置任务类型、数量和产品要求，以创建吸引人的个性化忠诚度体验。

每项任务都是可衡量的操作，有助于完成挑战。 任务是可重复使用的组件，可以独立创建，然后添加到一个或多个挑战，或直接在挑战中创建。

## 创建任务 {#create-task}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_create"
>title="创建任务"
>abstract="选择一个客户活动（购买或支出），然后配置此活动特有的属性：数量或金额、合格项和排除项，也可选择限制（如最少支出或最大交易数）。 在属性窗格中设置任务名称和描述。"

您可以从两个入口点创建任务。 无论从何处开始，配置过程都是相同的。

>[!BEGINTABS]

>任务清单中的[!TAB ]

选择&#x200B;**[!UICONTROL 任务]**&#x200B;选项卡，然后选择&#x200B;**[!UICONTROL 创建任务]**。 从清单中创建的任务将保存并可在多个难题中重复使用。

![](assets/task-create-inventory.png)

>从挑战中[!TAB 开始]

打开现有挑战或创建新挑战。 选择&#x200B;**[!UICONTROL 添加任务]**&#x200B;并单击&#x200B;**[!UICONTROL 新建]**&#x200B;按钮。 通过这种方式创建的任务会自动添加到您的挑战中，并保存到Tasks清单中，以供在其他挑战中重复使用。

![](assets/task-create-challenge.png)

>[!ENDTABS]

## 选择客户活动 {#choose-activity}

选择客户完成此任务必须执行的活动类型：

* **[!UICONTROL 购买]**：客户必须购买一个或多个项目才能完成此任务
* **[!UICONTROL 支出]**：客户必须支出指定的金额才能完成此任务

要选择活动，请单击&#x200B;**+**图标，然后选择与结果目标最一致的客户活动。 每种活动类型都有特定的可配置属性，以便进一步定义和形成任务需求。
![](assets/task-create-activity.png)

## 定义任务属性 {#define-attributes}

根据选定的活动类型配置任务属性。 浏览以下选项卡以查看每种活动类型的可用属性：

>[!BEGINTABS]

>[!TAB 购买活动]

**购买**&#x200B;活动的可用属性：

* **[!UICONTROL 数量]**：输入完成此任务必须购买的项目数。
* **[!UICONTROL 符合条件的项目和排除项]**：定义计入任务完成的项目或项目组以及未计入任务完成的项目或项目组，或者选择&#x200B;**[!UICONTROL 自带数据]**&#x200B;以从外部数据获取符合条件的项目。 [了解详情](#eligible-items-exclusions)
* **[!UICONTROL 最小支出值金额]**：设置最低采购金额要求。
* **[!UICONTROL 最大事务数]**：限制可用于完成任务的事务数。

![](assets/task-create-purchase.png)

>[!TAB 支出活动]

**支出**&#x200B;活动的可用属性：

* **[!UICONTROL 金额]**：输入完成任务所需的总支出金额。
* **[!UICONTROL 符合条件的项目和排除项]**：定义计入任务完成和不计入任务完成的项目或项目组。 [了解有关合格项目和排除项的更多信息](#eligible-items-exclusions)
* **[!UICONTROL 最大事务数]**：指定允许满足支出要求的事务数。 您可以从参数图标激活此属性。

![](assets/task-create-spend.png)

>[!ENDTABS]

## 定义合格项和排除项 {#eligible-items-exclusions}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_eligible_items_exclusion"
>title="合格项和排除项"
>abstract="对于&#x200B;**购买**&#x200B;和&#x200B;**支出**&#x200B;这两个活动，您都可以使用&#x200B;**[!UICONTROL 合格项和排除项]**&#x200B;属性来定义哪些是合格的项和组、哪些是要排除的。 这样，您就可以根据您的挑战目标来针对特定的产品、类别或地点。 例如，您可以将一项支出任务限制为特定的产品类别，或者将礼品卡或促销品排除在外，不算在任务完成中。"

<!-- SCREENSHOT: Eligible items & exclusions popup showing the two sections: "Eligible task purchases are limited to the following" and "The following are excluded from this task" with text input fields -->

对于&#x200B;**购买**&#x200B;和&#x200B;**支出**&#x200B;这两个活动，您都可以使用&#x200B;**[!UICONTROL 合格项和排除项]**&#x200B;属性来定义哪些是合格的项和组、哪些是要排除的。 这样，您就可以根据您的挑战目标来针对特定的产品、类别或地点。

例如，您可以将任务限制在特定产品类别中，或者将礼品卡或促销项目排除在任务完成计算之外。

![](assets/tasks-create-eligible.png)

### 为任务设置符合条件的项目

要定义合格项目，请在&#x200B;**[!UICONTROL 合格任务购买仅限于以下]**&#x200B;字段中输入以逗号分隔的特定项目ID、类别或目标ID。 如果您将此字段留空，则默认情况下所有购买均符合条件。 您还可以输入`*`以明确使所有购买都符合条件。

示例：`SKU001, SKU002, CategoryA`

### 从任务中排除项目

要从任务中排除项目，请在&#x200B;**[!UICONTROL 字段中输入特定的项目ID、类别或目标ID。以下内容将从此任务]**&#x200B;字段中排除。

示例：`CLEARANCE01, GIFTCARD, SALE_CATEGORY`

### 自带资格和排除数据 {#byod-personalization}

>[!AVAILABILITY]
>
>**[!UICONTROL 自带数据]**&#x200B;选项当前可供有限的组织使用，并将在未来版本中更广泛地提供。

除了输入项目ID以使其符合条件或排除外，您还可以在运行时使用&#x200B;**[!UICONTROL 自带数据]**&#x200B;选项从外部忠诚度挑战数据中提升资格。

选择&#x200B;**[!UICONTROL 自带数据]**&#x200B;后，运行时将从与您的忠诚度挑战环境同步的数据中解析每位参与者的资格，而不是项目ID的列表。

要使用此选项，请在&#x200B;**[!UICONTROL 合格项目和排除项]**&#x200B;中选择个性化图标，然后选择&#x200B;**[!UICONTROL 自带数据]**。

![](assets/tasks-create-eligible-bring.png)

>[!IMPORTANT]
>
>将此任务分配给质询时，选择&#x200B;**[!UICONTROL 标准]**&#x200B;作为质询类型。 请勿在挑战级别选择&#x200B;**[!UICONTROL 自带数据]**，因为该选项是为完全数据驱动的挑战保留的，在该挑战中，整个结构（包括任务和奖励）都由外部提供。

## 定义任务属性 {#define-task-properties}

在任务&#x200B;**[!UICONTROL 属性]**&#x200B;窗格中，配置基本任务信息：

* **[!UICONTROL 任务名称]**：输入任务的描述性名称。
* **[!UICONTROL 任务描述]**：根据配置的活动和属性自动生成描述。 要输入自定义说明，请关闭自动生成选项，然后在文本字段中输入说明。

![](assets/tasks-create-properties.png)

配置所有属性和属性后，选择&#x200B;**[!UICONTROL 创建]**&#x200B;以保存任务。 任务将保存到Tasks清单中，如果是从挑战中创建的，则会自动添加到该挑战中。
