---
solution: Journey Optimizer
product: journey optimizer
title: Create tasks for loyalty challenges
description: Learn how to create and configure tasks for loyalty challenges in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="私人测试版" type="Informative"
mini-toc-levels: 1
exl-id: c1e49173-69cc-4729-9f9a-afea2ccff3fa
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 24%

---

# 创建任务 {#create-tasks}

>[!BEGINSHADEBOX]

**忠诚度挑战文档：**

* [忠诚度挑战入门](get-started.md)
* [访问和管理挑战和任务](access-loyalty-challenges.md)
* [创建挑战](create-challenges.md)
* **Create tasks** ◀︎ **You are here**
* [忠诚度挑战API参考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前处于&#x200B;**私人测试版**&#x200B;中。 有关发行周期和可用性阶段的完整详细信息，请参阅 [Journey Optimizer 发行周期](../rn/releases.md)。

Tasks define the specific actions or milestones that customers must complete to earn rewards in a loyalty challenge. You can configure task types, quantities, and product requirements to create engaging and personalized loyalty experiences.

Each task represents a measurable action that contributes toward challenge completion. Tasks are reusable components that can be created independently and then added to one or more challenges, or created directly within a challenge.

## 创建任务 {#create-task}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_task_create"
>title="创建任务"
>abstract="选择一个客户活动（购买或支出），然后配置此活动特有的属性：数量或金额、合格项和排除项，也可选择限制（如最少支出或最大交易数）。 在属性窗格中设置任务名称和描述。"

You can create tasks from two entry points. The configuration process is the same regardless of where you start.

>[!BEGINTABS]

>[!TAB From the Tasks inventory]

Select the **[!UICONTROL Tasks]** tab and select **[!UICONTROL Create Task]**. Tasks created from the inventory are saved and available for reuse across multiple challenges.

![](assets/task-create-inventory.png)

>[!TAB From within a challenge]

Open an existing challenge or create a new one. Select **[!UICONTROL Add task]** and click the **[!UICONTROL New]** button. Tasks created this way are automatically added to your challenge and also saved to the Tasks inventory for reuse in other challenges.

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
* **[!UICONTROL 符合条件的项目和排除项]**：定义计入任务完成和不计入任务完成的项目或项目组。 [了解有关合格项目和排除项的更多信息](#eligible-items-exclusions)
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

例如，您可以将一项支出任务限制为特定的产品类别，或者将礼品卡或促销品排除在外，不算在任务完成中。

![](assets/tasks-create-eligible.png)

* 要定义合格项目，请在&#x200B;**[!UICONTROL 合格任务购买仅限于以下]**&#x200B;字段中输入以逗号分隔的特定项目ID、类别或目标ID。 如果您将此字段留空，则默认情况下所有购买均符合条件。 您还可以输入`*`以明确使所有购买都符合条件。

  示例：`SKU001, SKU002, CategoryA`

* 要从任务中排除项目，请在&#x200B;**[!UICONTROL 字段中输入特定的项目ID、类别或目标ID。以下内容将从此任务]**&#x200B;字段中排除。

  示例：`CLEARANCE01, GIFTCARD, SALE_CATEGORY`

## 定义任务属性 {#define-task-properties}

在任务&#x200B;**[!UICONTROL 属性]**&#x200B;窗格中，配置基本任务信息：

* **[!UICONTROL 任务名称]**：输入任务的描述性名称。
* **[!UICONTROL 任务描述]**：根据配置的活动和属性自动生成描述。 要输入自定义说明，请关闭自动生成选项，然后在文本字段中输入说明。

![](assets/tasks-create-properties.png)

配置所有属性和属性后，选择&#x200B;**[!UICONTROL 创建]**&#x200B;以保存任务。 任务将保存到Tasks清单中，如果是从挑战中创建的，则会自动添加到该挑战中。
