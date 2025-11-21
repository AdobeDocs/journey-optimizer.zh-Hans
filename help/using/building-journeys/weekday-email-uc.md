---
solution: Journey Optimizer
product: journey optimizer
title: 仅在工作日发送电子邮件
description: 了解如何在Adobe Journey Optimizer中配置仅在工作日发送电子邮件的历程
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: 历程，用例，工作日，条件，电子邮件，计划
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: 46a46fb25c1ef985a0bdea8974aa009e3699c7a3
workflow-type: tm+mt
source-wordcount: '1833'
ht-degree: 0%

---

# 仅在工作日发送电子邮件 {#send-emails-only-on-weekdays}

此用例演示了如何在Adobe Journey Optimizer中配置仅在工作日（星期一到星期五）发送电子邮件的历程。 对于在周末（星期六或星期日）进入历程的用户档案，电子邮件会在星期一的指定时间自动排队并发送。 这通过在工作周期间传递消息来确保最佳参与。

## 用例概述

**挑战**：确保仅在工作日发送电子邮件，即使用户档案可能会在周末进入历程。 对于周末输入的内容，电子邮件应排队并在星期一特定时间发送。

**解决方案**：使用条件活动标识星期几。 对于周末的条目，具有自定义公式的等待活动会将电子邮件延迟到星期一。 工作日条目直接进入电子邮件发送步骤。

此方法向您展示如何使用条件活动来检查当天是星期六还是星期日，实施包含用于周末输入的自定义公式的等待活动，将周末电子邮件排入特定小时用于星期一投放的队列，以及立即发送用于工作日条目（星期一至星期五）的电子邮件。

这种方法非常适合于企业对企业(B2B)电子邮件促销活动、专业新闻通讯和通信、与企业相关的公告、与工作相关的产品更新，以及任何不希望周末交付的营销活动。

➡️观看分步[视频教程](#how-to-video)

>[!NOTE]
>
>要实施此用例，您需要一个活动的Adobe Journey Optimizer实例，该实例具有配置的[电子邮件渠道表面](../configuration/channel-surfaces.md)、[受众](../audience/about-audiences.md)或[事件](../event/about-events.md)以触发历程，以及对[历程条件](condition-activity.md)和[表达式](expression/expressionadvanced.md)的基本了解。





## 实施步骤

### 步骤1：创建旅程

1. 在Adobe Journey Optimizer中导航到&#x200B;**[!UICONTROL 历程管理]** > **[!UICONTROL 历程]**。

1. 单击&#x200B;**[!UICONTROL 创建历程]**&#x200B;以创建新旅程。 [了解有关创建历程的更多信息](journey-gs.md)

1. 配置历程属性：
   * **名称**：工作日电子邮件营销活动
   * **描述**：仅在工作日发送电子邮件（星期一至星期五）
   * 为您的用例设置适当的命名空间

[了解有关历程属性的更多信息](journey-properties.md)

1. 选择您的历程入口点：
   * **[读取受众](read-audience.md)**：针对特定受众的批量营销活动
   * **[事件](../event/about-events.md)**：对于基于客户行为的实时触发的历程

### 第2步：添加条件活动以检查每周时间

在历程开始之后，立即添加&#x200B;**[!UICONTROL 条件]**&#x200B;活动以检查当天是星期六还是星期日。 这将相应地分支工作流。

1. 将&#x200B;**[!UICONTROL 条件]**&#x200B;活动拖放到画布上的入口点之后。 [了解有关条件活动的更多信息](condition-activity.md)

1. 单击Condition活动以打开其配置面板。

1. 在&#x200B;**[!UICONTROL 条件类型]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 数据Source条件]**。 [了解有关条件类型的更多信息](condition-activity.md#data_source_condition)

   ![在表达式编辑器中配置星期六条件](assets/weekday-email-uc-condition-expression.png)


### 步骤3：配置条件以标识星期六

创建第一个条件路径以标识星期六条目。

1. 单击&#x200B;**[!UICONTROL 高级模式]**&#x200B;以打开表达式编辑器。 [了解有关表达式编辑器的更多信息](expression/expressionadvanced.md)

1. 输入以下表达式以检查当天是否为星期六：

   ```javascript
   dayOfWeek(now()) == 7
   ```

   这会使用带`dayOfWeek()`的`now()`函数来获取当前日期。 [了解有关日期函数的更多信息](functions/date-functions.md)


1. 单击&#x200B;**[!UICONTROL 确定]**&#x200B;保存条件。

1. 将此路径标记为“星期六”。

### 步骤4：为星期日添加第二个条件路径

1. 在Condition活动中，单击&#x200B;**[!UICONTROL 添加路径]**&#x200B;以创建第二个条件。

1. 在第二个路径的表达式编辑器中，输入：

   ```javascript
   dayOfWeek(now()) == 1
   ```

   这会检查当天是否为星期日。

1. 将此路径标记为“Sunday”。

1. 选中&#x200B;**[!UICONTROL 为上述情况以外的其他情况显示路径]**&#x200B;以创建工作日条目（星期一至星期五）的路径。


>[!NOTE]
>
>`dayOfWeek()`函数返回一个表示一周中某天的整数，其中1表示周日，7表示周六。 这遵循ISO-8601天编号标准。

### 步骤5：为周末条目配置等待活动

对于在星期六或星期日输入的用户档案，请使用带有自定义公式的等待活动将电子邮件延迟到星期一（所需时间）。


**对于星期六路径：**

1. 添加&#x200B;**[!UICONTROL 等待]**&#x200B;活动。 [了解有关等待活动的更多信息](wait-activity.md)

1. 选择&#x200B;**[!UICONTROL 持续时间]**&#x200B;作为等待类型。

1. 单击&#x200B;**[!UICONTROL 高级模式]**&#x200B;输入自定义公式。

1. 输入以下公式以等到星期一上午9点：

   ```javascript
   toDuration("PT" + (48 - getHourOfDay(now())) + "H")
   ```

   或者使用此替代公式：

   ```javascript
   setHours(nowWithDelta(2, "days"), 9)
   ```

   ![具有三个条件路径的历程 — 星期六、星期日和工作日](assets/weekday-email-uc-paths.png)

   **解释**：此公式计算从星期六到星期一上午9点的等待时间。 值X=2表示未来2天（星期六+ 2天=星期一）。 [了解有关日期函数的更多信息](functions/date-functions.md#nowWithDelta)

星期日路径的&#x200B;**：**

1. 添加&#x200B;**[!UICONTROL 等待]**&#x200B;活动。

1. 选择&#x200B;**[!UICONTROL 持续时间]**&#x200B;作为等待类型。

1. 单击&#x200B;**[!UICONTROL 高级模式]**&#x200B;输入自定义公式。

1. 输入以下公式以等到星期一上午9点：

   ```javascript
   setHours(nowWithDelta(1, "days"), 9)
   ```

   **解释**：此公式等待1天（星期日+ 1天=星期一），并将时间设置为上午9点。 值X=1表示前移1天，H=9表示上午9点。

>[!TIP]
>
>您可以根据需要在星期一发送电子邮件的任何时间自定义小时数(H)参数。 例如，将上午10点更改为9到10，将下午2点更改为14。

### 步骤6：配置工作日路径

对于&#x200B;**工作日路径**（星期一至星期五）：

1. 直接继续添加&#x200B;**[!UICONTROL 电子邮件]**&#x200B;操作活动。 工作日条目不需要等待活动。 [了解有关电子邮件操作的更多信息](journeys-message.md)

1. 配置您的电子邮件：
   * 选择或创建您的[电子邮件内容](../email/get-started-email-design.md)
   * 配置[电子邮件参数](../email/email-settings.md)
   * 根据需要设置[个性化](../personalization/personalize.md)

1. 在电子邮件后添加&#x200B;**[!UICONTROL 结束]**&#x200B;活动。

### 步骤7：将周末路径合并为电子邮件

在星期六和星期日路径上的等待活动后，将它们合并到同一电子邮件操作活动：

1. 从星期六等待活动中，添加&#x200B;**[!UICONTROL 电子邮件]**&#x200B;操作。

1. 从星期日等待活动中，连接到同一电子邮件操作。

1. 工作日路径也应流向此电子邮件操作。

### 步骤8：测试您的历程

在发布之前，请在Adobe Journey Optimizer的测试模式下彻底测试旅程逻辑，以确认所有内容均可按预期运行：

1. 单击右上角的&#x200B;**[!UICONTROL 测试]**&#x200B;按钮。

1. 启用测试模式。 [了解如何测试您的历程](testing-the-journey.md)

1. 创建[测试用户档案](../audience/creating-test-profiles.md)，模拟一周中不同日期的进入时间：
   * **星期六条目**：验证配置文件是否遵循星期六路径，在星期一指定的时间等待并接收电子邮件
   * **星期日条目**：验证配置文件是否遵循星期日路径、在星期一的指定小时等待并接收电子邮件
   * **星期一至星期五的条目**：验证是否立即发送电子邮件而不等待任何时间

1. 查看历程可视化以确保用户档案遵循正确的条件路径（星期六、星期日或工作日）。

1. 检查历程中的任何错误或警告。 [了解历程疑难解答](troubleshooting.md)

1. 验证“等待”公式是否为所需的星期一交货时间计算正确的持续时间。

>[!IMPORTANT]
>
>始终在发布到生产环境之前彻底测试历程逻辑。 使用测试模式模拟不同的进入场景，并验证周末条目是否正确排队等候星期一的传递。 [了解有关历程测试最佳实践的更多信息](testing-the-journey.md)

### 步骤9：发布旅程

测试完成后：

1. 单击右上角的&#x200B;**[!UICONTROL 发布]**。

1. 确认发布。 [了解有关发布历程的更多信息](publish-journey.md)

1. 使用[历程报告](report-journey.md)和[实时报告](../reports/journey-live-report.md)监视旅程性能。

## 最佳实践和注意事项

+++**使用增强的公式优化工作流**

为了增强您的工作流并处理更复杂的业务要求，您可以将公式扩展到除基本工作日检查之外的假日、时区或特定工作时间。 调整等待公式中的小时数参数(H)以匹配最佳发送时间 — 例如，如果上午10点显示更好的参与率，则将公式更改为使用小时10。 对于多时区支持，请考虑为不同地理区域创建单独的历程，以确保星期一按每个收件人的当地时区交付。

+++

+++**时区管理**

`now()`函数和历程执行使用在历程级别配置的时区。 在发布之前，通过在历程属性中配置此设置，确保历程时区与您的需求相匹配（[了解有关时区管理的更多信息](timezone-management.md)）。 如果您的受众跨越多个时区，请注意，星期几检查在历程配置的时区中进行，而不是在收件人的本地时区中进行。 对于特定于时区的投放，请为不同区域创建单独的历程，或在读取受众活动中使用时区设置。

+++

+++**历程条目和计时**

对于批处理历程，[安排读取受众](read-audience.md#schedule)在对受众有意义的时间触发 — 早上执行（例如，上午6:00）是业务通信中常见的。 对于基于事件的历程，将在收到事件后立即评估条件，周末输入的配置文件将自动等到星期一（[了解有关事件的更多信息](../event/about-events.md)）。 确保您的[历程超时设置](journey-properties.md#timeout)满足最长等待时间（从星期六到星期一，最长2天）。

+++

+++**测试是必需的**

正如实施指南中强调的，请始终测试历程逻辑，以确认所有内容均可按预期运行。 使用&#x200B;**测试模式**&#x200B;模拟不同的进入方案，而不发送真正的电子邮件。 测试所有三个路径（星期六条目、星期日条目和工作日条目），验证等待持续时间计算是否正确，确认星期一的交付发生在指定的小时，并检查历程可视化图表以确保正确的路径路由。

+++

+++**再次进入和频率**

对于周期性营销活动，请正确配置&#x200B;**[!UICONTROL 重新进入]**&#x200B;设置（[了解有关重新进入设置的更多信息](entry-management.md)）。 如果用户档案可以重新进入历程，则每次都将接受星期几检查，确保周末条目始终排队等待星期一。 考虑添加[频率上限规则](../conflict-prioritization/journey-capping.md)，以避免用户档案可以频繁地重新输入时过度发送消息。

+++

## 高级变量

+++**特定日期定位**

要仅在特定日期（例如，星期二和星期四）发送电子邮件，请修改条件：

```javascript
dayOfWeek(now()) == 3 or dayOfWeek(now()) == 5
```

对于所有其他天，添加一个等待活动，用于计算到下个星期二或星期四的天数。

+++

+++**不同日期的不同发送时间**

您可以使用不同的等待公式为不同的周末行为创建多个路径。 例如，将`nowWithDelta(4, "days")`用于星期六到星期三的投放，或将`nowWithDelta(2, "days")`用于星期日到星期二的投放。 这可以提高发送计划的灵活性。

+++

+++**营业时间交付**

要确保在工作时间交付，请调整等待公式中的小时参数。 例如，对于在下午2点（而不是上午9点）投放：

```javascript
setHours(nowWithDelta(1, "days"), 14)
```

您还可以在“等待”后添加第二个条件，以检查当前时间是否在发送前的营业时间内。

+++

+++**假日排除**

要排除假日，请添加其他检查特定日期的条件路径：

```javascript
toDateTimeOnly(now()) == toDateTimeOnly("2024-12-25T00:00:00")
```

如果条件与假日匹配，请添加等待活动以延迟到下一个工作日。 [了解有关日期比较函数的更多信息](functions/date-functions.md)

+++

## 相关主题

* [关于条件活动](condition-activity.md) — 了解如何在历程中创建不同的路径
* [在历程中使用条件](conditions.md) — 历程条件的详细指南
* [等待活动](wait-activity.md) — 配置等待持续时间和公式
* [日期函数](functions/date-functions.md) — 完成日期和时间函数的引用
* [表达式编辑器](expression/expressionadvanced.md) — 生成复杂表达式
* [测试您的历程](testing-the-journey.md) — 在发布之前验证历程逻辑
* [时区管理](timezone-management.md) — 处理历程中的不同时区
* [历程最佳实践](journey-gs.md#best-practices) — 历程设计的推荐方法

## 操作说明视频

了解如何使用Adobe Journey Optimizer仅在工作日发送电子邮件。 此视频演示了条件活动和等待公式的分步实施，这些公式用于将周末条目排入队列以供星期一投放。

>[!VIDEO](https://video.tv.adobe.com/v/3469330?quality=12&learn=on)

## 其他资源

* [表达式编辑器文档](expression/expressionadvanced.md) — 生成并验证历程表达式
* [历程设计器指南](using-the-journey-designer.md) — 熟悉历程画布
* [历程用例概述](jo-use-cases.md) — 探索更多历程模式和示例
* [社区博客帖子：如何仅在工作日发送电子邮件](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400){target="_blank"} — 包含详细示例的原始博客帖子

