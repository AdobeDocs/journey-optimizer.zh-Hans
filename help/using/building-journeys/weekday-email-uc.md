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
source-git-commit: 970712614b0d4da37d9ecbe45701f93147b1428c
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 1%

---

# 仅在工作日发送电子邮件 {#send-emails-only-on-weekdays}

此用例演示了如何在Adobe Journey Optimizer中配置仅在工作日（星期一到星期五）发送电子邮件的历程。 对于在周末（星期六或星期日）进入历程的用户档案，电子邮件会在星期一的指定时间自动排队并发送。 这通过在工作周期间传递消息来确保最佳参与。

## 用例概述

**挑战**：确保仅在工作日发送电子邮件，即使用户档案可能会在周末进入历程。 对于周末输入的内容，电子邮件应排队并在星期一特定时间发送。

**解决方案**：使用条件活动标识星期几。 对于周末的条目，具有自定义公式的等待活动会将电子邮件延迟到星期一。 工作日条目直接进入电子邮件发送步骤。

此方法向您展示如何使用条件活动来检查当天是星期六还是星期日，实施包含用于周末输入的自定义公式的等待活动，将周末电子邮件排入特定小时用于星期一投放的队列，以及立即发送用于工作日条目（星期一至星期五）的电子邮件。

这种方法非常适合于企业对企业(B2B)电子邮件促销活动、专业新闻通讯和通信、与企业相关的公告、与工作相关的产品更新，以及任何不希望周末交付的营销活动。

>[!NOTE]
>
>要实施此用例，您需要一个活动的Adobe Journey Optimizer实例，该实例具有配置的[电子邮件渠道表面](../configuration/channel-surfaces.md)、[受众](../audience/about-audiences.md)或[事件](../event/about-events.md)以触发历程，以及对[历程条件](condition-activity.md)和[表达式](expression/expressionadvanced.md)的基本了解。


## 实施步骤

### 步骤1：创建旅程

1. 在Adobe Journey Optimizer中导航到&#x200B;**[!UICONTROL 历程管理]** > **[!UICONTROL 历程]**。

1. 单击&#x200B;**[!UICONTROL 创建历程]**&#x200B;以[创建新旅程](journey-gs.md)。

1. 配置[历程属性](journey-properties.md)。

1. 选择您的历程入口点：
   * **[读取受众](read-audience.md)**：针对特定受众的批量营销活动
   * **[事件](../event/about-events.md)**：对于基于客户行为的实时触发的历程

### 第2步：添加条件活动以检查每周时间

在历程开始之后，立即添加&#x200B;**[!UICONTROL 条件]**&#x200B;活动以检查当天是星期六还是星期日。 这将相应地分支工作流。

1. 将[**[!UICONTROL 条件&#x200B;]**&#x200B;活动](condition-activity.md)拖放到画布上的入口点之后。

1. 单击&#x200B;**[!UICONTROL 条件]**&#x200B;活动以打开其配置面板。

1. 选择&#x200B;**[!UICONTROL 时间条件]**&#x200B;作为条件类型。

1. 选择&#x200B;**[!UICONTROL 一周中的某天]**&#x200B;作为时间过滤选项。

1. 对于&#x200B;**第一个路径（星期六）**，仅选择&#x200B;**星期六**。 将此路径标记为“星期六”。

1. 单击&#x200B;**[!UICONTROL 添加路径]**&#x200B;以创建第二个条件。

1. 对于&#x200B;**秒路径（星期日）**，选择&#x200B;**[!UICONTROL 一周的某天]**，然后选择&#x200B;**仅星期日**。 将此路径标记为“Sunday”。

   ![在表达式编辑器中配置星期六和星期日条件](assets/weekday-email-uc-condition-expression.png)


1. 选中&#x200B;**[!UICONTROL 为上述情况以外的其他情况显示路径]**&#x200B;以创建工作日条目（星期一至星期五）的路径。

>[!NOTE]
>
>用于星期评估的时区在历程属性中的历程级别而不是条件级别定义。 公式中使用的历程[时区](timezone-management.md)是历程配置的时区，而不是收件人的时区。

### 步骤3：为周末条目配置等待活动

对于在星期六或星期日输入的用户档案，请使用带有自定义公式的&#x200B;**[!UICONTROL 等待]**&#x200B;活动将电子邮件延迟到星期一（所需时间）。

在&#x200B;**[!UICONTROL 等待]**&#x200B;活动中，使用以下公式：

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

其中：

* **X**&#x200B;是等待的天数：
   * 在星期六使用&#x200B;**2**（等到星期一）
   * 将&#x200B;**1**&#x200B;用于星期日（等到星期一）
* **H**&#x200B;是您要发送的小时（例如，上午9点为&#x200B;**9**）


**星期六的示例：**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

**星期日示例：**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

要在历程中实施此功能，请执行以下操作：

1. 在&#x200B;**星期六路径**&#x200B;上，在该条件后添加&#x200B;**[!UICONTROL 等待]**&#x200B;活动。

1. 选择&#x200B;**[!UICONTROL 持续时间]**&#x200B;作为等待类型。

1. 单击&#x200B;**[!UICONTROL 高级模式]**&#x200B;以输入自定义公式。

1. 输入： `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![具有三个条件路径的历程 — 星期六、星期日和工作日](assets/weekday-email-uc-paths.png)

1. 对&#x200B;**星期日路径**&#x200B;重复相同的步骤，使用： `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`

>[!TIP]
>
>对于更复杂的营业时间（例如，仅在工作日上午9点至下午5点之间发送），您可以进一步改进公式和条件。

### 步骤4：工作日分支

对于周一到周五输入的用户档案，照常进入电子邮件发送步骤。

1. 在&#x200B;**工作日路径**（“其他案例”路径）中，直接继续添加&#x200B;**[!UICONTROL 电子邮件]**&#x200B;操作活动。 工作日条目不需要&#x200B;**[!UICONTROL 等待]**&#x200B;活动。

1. 根据需要配置电子邮件。

### 步骤5：完成历程流

在星期六和星期日路径上的&#x200B;**[!UICONTROL 等待]**&#x200B;活动后，所有三个路径（星期六、星期日和工作日）都应流向相同的&#x200B;**[!UICONTROL 电子邮件]**&#x200B;操作活动。 在电子邮件后添加&#x200B;**[!UICONTROL 结束]**&#x200B;活动。

### 可视化工作流概述

完整历程工作流遵循以下逻辑：

* **开始** → **[!UICONTROL 条件]**：是星期六还是星期日？
   * **是（星期六）：** **[!UICONTROL 等待]**&#x200B;至星期一上午9点→**[!UICONTROL 发送电子邮件]**
   * **是（星期日）：** **[!UICONTROL 等待]**&#x200B;到星期一上午9点→**[!UICONTROL 发送电子邮件]**
   * **否（星期一至星期五）：**&#x200B;**[!UICONTROL 立即发送电子邮件]**

这可确保所有电子邮件仅在工作日发送，周末条目会自动排队等待星期一投放。

### 步骤6：测试您的历程

在发布之前，请在Adobe Journey Optimizer的测试模式下彻底测试旅程逻辑，以确认所有内容均可按预期运行：

1. 单击右上角的&#x200B;**[!UICONTROL 测试]**&#x200B;按钮。

1. 启用[测试模式](testing-the-journey.md)。

1. 创建[测试用户档案](../audience/creating-test-profiles.md)，模拟一周中不同日期的进入时间：
   * **星期六条目**：验证配置文件是否遵循星期六路径，在星期一指定的时间等待并接收电子邮件
   * **星期日条目**：验证配置文件是否遵循星期日路径、在星期一的指定小时等待并接收电子邮件
   * **星期一至星期五的条目**：验证是否立即发送电子邮件而不等待任何时间

1. 查看历程可视化以确保用户档案遵循正确的条件路径（星期六、星期日或工作日）。

1. 检查历程中是否有任何[错误或警告](troubleshooting.md)。

1. 验证“等待”公式是否为所需的星期一交货时间计算正确的持续时间。

>[!IMPORTANT]
>
>请始终在测试模式下测试历程逻辑，以确保等待活动按预期运行。 使用测试模式模拟不同的进入场景，并验证周末条目是否正确排队等候星期一的传递。 有关更多详细信息，请参阅[历程测试最佳实践](testing-the-journey.md)。

### 步骤7：发布历程

测试完成后：

1. 单击右上角的&#x200B;**[!UICONTROL 发布]**。

1. 确认[发布](publish-journey.md)。

1. 使用[历程报告](report-journey.md)和[实时报告](../reports/journey-live-report.md)监视旅程性能。


## 相关主题

* [条件活动](condition-activity.md) — 了解如何在历程中创建不同的路径
* [在历程中使用条件](conditions.md) — 历程条件的详细指南
* [等待活动](wait-activity.md) — 配置等待持续时间和公式
* [日期函数](functions/date-functions.md) — 完成日期和时间函数的引用
* [表达式编辑器](expression/expressionadvanced.md) — 生成复杂表达式
* [历程最佳实践](journey-gs.md#best-practices) — 历程设计的推荐方法
