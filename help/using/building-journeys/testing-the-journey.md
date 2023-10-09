---
solution: Journey Optimizer
product: journey optimizer
title: 测试您的历程
description: 了解如何测试您的历程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 测试，历程，检查，错误，故障排除
exl-id: 9937d9b5-df5e-4686-83ac-573c4eba983a
source-git-commit: 7c0b0fe67a5a2665f7cf7bdce4a36207d7bcef56
workflow-type: tm+mt
source-wordcount: '1522'
ht-degree: 11%

---

# 测试您的历程{#testing_the_journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_test"
>title="测试您的历程"
>abstract="在发布历程之前，使用测试配置文件来测试历程。这使您可以分析个人如何在历程中流动，并在发布前进行故障排除。"

在发布历程之前，使用测试配置文件来测试历程。此模式允许您运行历程测试并使用测试配置文件识别问题。

只有测试配置文件才能进入处于测试模式的历程。您可以创建新的测试用户档案，也可以将现有用户档案转换为测试用户档案。 在中了解有关测试用户档案的更多信息 [本节](../audience/creating-test-profiles.md).

>[!NOTE]
>
>在测试历程之前，必须解决所有错误（如果有）。 了解在测试之前如何检查错误 [本节](../building-journeys/troubleshooting.md#checking-for-errors-before-testing).

要使用测试模式，请执行以下步骤：

1. 要激活测试模式，请激活 **[!UICONTROL 测试]** 切换，位于右上角。

   ![](assets/journeytest1.png)

1. 如果历程至少有一个 **等待** 活动，设置 **[!UICONTROL 等待时间]** 参数来定义每个等待活动和事件超时在测试模式下的停留时间。 等待和事件超时的默认时间为10秒。 这将确保您快速获得测试结果。

   ![](assets/journeytest_wait.png)

   >[!NOTE]
   >
   >当在历程中使用具有超时的反应事件时，等待时间的默认值和最小值为40秒。 请参阅[此章节](../building-journeys/reaction-events.md)。

1. 使用 **[!UICONTROL 触发事件]** 按钮以配置事件并将其发送到历程。

   ![](assets/journeyuctest1.png)

1. 配置所需的不同字段。 在 **配置文件标识符** 字段中，输入用于标识测试用户档案的字段值。 例如，它可以是电子邮件地址。 确保发送与测试用户档案相关的事件。 请参阅[此章节](#firing_events)。

   ![](assets/journeyuctest1-bis.png)

1. 收到事件后，单击 **[!UICONTROL 显示日志]** 按钮查看测试结果并进行验证。 请参阅[此章节](#viewing_logs)。

   ![](assets/journeyuctest2.png)

1. 如果有任何错误，请取消激活测试模式，修改历程并再次进行测试。完成测试后，即可发布旅程。 请参阅[此页](../building-journeys/publishing-the-journey.md)。

## 重要说明 {#important_notes}

* 在测试模式下，您可以使用界面触发事件。
* 只有在Real-time Customer Profile Service中标记为“测试配置文件”的个人才能进入测试历程。 请参阅此[章节](../audience/creating-test-profiles.md)。
* 测试模式仅适用于使用命名空间的草稿历程。 测试模式需要检查进入旅程的人员是否为测试用户档案，因此必须能够访问Adobe Experience Platform。
* 在测试会话期间可进入历程的测试用户档案的最大数量为100。
* 禁用测试模式时，它会从过去进入该模式或当前进入该模式的所有人员中清空历程。 它还会清除报表。
* 您可以根据需要多次启用/禁用测试模式。
* 激活测试模式后，您无法修改历程。 在测试模式下时，您可以直接发布历程，而无需先停用测试模式。
* 在达到拆分时，始终选择顶部分支。 如果希望测试选择其他路径，可以重新组织拆分分支的位置。
* 为优化性能并防止使用过时资源，所有处于测试模式且一周内未触发的历程都将切换回 **草稿** 状态。
* 测试模式触发的事件存储在专用数据集中。 这些数据集的标签如下： `JOtestmode - <schema of your event>`

## 触发您的事件 {#firing_events}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_configuration"
>title="配置测试模式"
>abstract="如果您的历程包含多个事件，请使用下拉列表选择一个事件。然后，对于每个事件，配置传递的字段和事件发送的执行。"

使用 **[!UICONTROL 触发事件]** 按钮来配置将促使人员进入历程的事件。

>[!NOTE]
>
>在测试模式下触发事件时，将生成一个实际事件，这意味着该事件还将点击侦听此事件的其他历程。

作为先决条件，您必须知道哪些配置文件在Adobe Experience Platform中标记为测试配置文件。 事实上，测试模式仅在历程中允许这些用户档案，并且事件必须包含ID。 预期ID取决于事件配置。 例如，它可以是ECID或电子邮件地址。 需要将此键的值添加到 **配置文件标识符** 字段。

如果您的历程包含多个事件，请使用下拉列表选择一个事件。然后，对于每个事件，配置传递的字段和事件发送的执行。界面可帮助您在事件有效载荷中传递正确的信息并确保信息类型正确无误。 测试模式会保存测试会话中使用的最后一个参数以供将来使用。

![](assets/journeytest4.png)

利用接口，可传递简单的事件参数。 如果要在事件中传递收藏集或其他高级对象，可以单击 **[!UICONTROL 代码视图]** 查看有效负载的整个代码并对其进行修改。 例如，您可以复制并粘贴技术用户准备的事件信息。

![](assets/journeytest5.png)

技术用户还可以使用此界面来撰写事件负载和触发事件，而无需使用第三方工具。

单击 **[!UICONTROL 发送]** 按钮，测试开始。 个人在历程中的进度由视觉流表示。 当个人在历程中移动时，路径将逐渐变为绿色。 如果发生错误，则会在相应的步骤上显示警告符号。 您可以将光标放在错误上以显示有关错误的更多信息，并访问完整的详细信息（如果可用）。

![](assets/journeytest6.png)

当您在事件配置屏幕中选择不同的测试用户档案并再次运行测试时，可视流将被清除并显示新用户的路径。

在测试中打开历程时，显示的路径对应于上次执行的测试。

## 基于规则的历程的测试模式 {#test-rule-based}

测试模式也可用于使用基于规则的事件的历程。 有关基于规则的事件的详细信息，请参阅 [此页面](../event/about-events.md).

触发事件时， **事件配置** 屏幕允许您定义要在测试中传递的事件参数。 您可以单击右上角的工具提示图标来查看事件ID条件。 作为规则评估一部分的每个字段旁边还提供了工具提示。

![](assets/jo-event8.png)

## 业务事件的测试模式 {#test-business}

使用 [业务事件](../event/about-events.md)，使用测试模式在历程中触发单个测试用户档案入口、模拟事件并传递正确的用户档案ID。 您必须传递事件参数和将进入测试历程的测试用户档案的标识符。 在测试模式下，对于基于业务事件的历程，没有“代码视图”模式可用。

请注意，首次触发业务事件时，不能在同一测试会话中更改业务事件定义。 您只能让同一个人或不同人通过相同或其他标识符进入历程。 如果要更改业务事件参数，则必须停止并重新启动测试模式。

## 查看日志 {#viewing_logs}

>[!CONTEXTUALHELP]
>id="ajo_journey_test_logs"
>title="测试模式日志"
>abstract="“显示日志”按钮以 JSON 格式显示测试结果。这些结果显示历程中的人数及个人的状态。"

此 **[!UICONTROL 显示日志]** 按钮以查看测试结果。 此页面以JSON格式显示历程的当前信息。 使用按钮可复制整个节点。 您需要手动刷新页面以更新历程的测试结果。

![](assets/journeytest3.png)


>[!NOTE]
>
>在测试日志中，如果在调用第三方系统（数据源或操作）时出错，则显示错误代码和错误响应。

将显示历程中当前存在的个人（技术上称为实例）的数量。 以下是为每个人显示的有用信息：

* _Id_：历程中的个人的内部ID。 这可用于调试目的。
* _currentstep_：个人在历程中的步骤。 我们建议向您的活动添加标签以更轻松地对其进行识别。
* _currentstep_ >阶段：个人历程的状态（正在运行、已完成、错误或超时）。 有关详细信息，请参阅下文。
* _currentstep_ > _extraInfo_：错误描述和其他上下文信息。
* _currentstep_ > _fetchErrors_：有关获取此步骤期间发生的数据错误的信息。
* _externalKey_：事件中定义的键公式的值。
* _扩充数据_：历程使用数据源时历程已检索的数据。
* _transitionHistory_：个人执行的步骤列表。 对于事件，将显示有效负载。
* _actionExecutionErrors_ ：有关所发生错误的信息。

以下是个人旅程的不同状态：

* _正在运行_：个人当前在历程中。
* _已完成_：个人位于历程的结尾。
* _错误_：由于错误，个人在历程中停止。
* _已超时_：个人在历程中停止，因为步骤耗时过长。

当使用测试模式触发事件时，将自动使用源名称生成数据集。

测试模式会自动创建体验事件并将其发送到Adobe Experience Platform。 此Experience Event的源名称为“Journey Orchestration测试事件”。

