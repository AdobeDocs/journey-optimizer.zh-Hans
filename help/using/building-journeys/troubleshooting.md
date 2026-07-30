---
solution: Journey Optimizer
product: journey optimizer
title: 在测试或发布历程之前排除错误
description: 了解如何在测试或发布历程之前对错误进行故障排除
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: 故障排除，故障排除，历程，检查，错误
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DorhpVm3trSxHG-l77-DpwbLTNQQxET1SIMYX-8ClQc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 995
ht-degree: 18%

---

# 在测试历程之前排除错误 {#troubleshooting}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何在测试或发布之前查找和修复活动和历程配置错误，以使您的历程可以顺利运行。

>[!ENDSHADEBOX]

在此部分中，了解如何在测试或发布之前对历程进行故障排除。 当历程处于测试模式或历程处于实时状态时，可以执行以下列出的所有检查。 建议在测试模式下进行以下所有检查，然后继续发布。 在[此页面](../building-journeys/testing-the-journey.md)上了解有关测试模式的更多信息。

了解如何排查历程事件、检查用户档案是否进入您的历程、用户档案如何浏览历程以及是否在此页面](troubleshooting-execution.md)上发送[消息。 如果尽管已摄取事件，但没有配置文件进入您的基于事件的历程，请确保[事件条件数据类型与事件架构](troubleshooting-execution.md#verify-event-identity-and-rule-data-types)匹配。

如果您使用入站操作，请在此页面](troubleshooting-inbound.md)上了解如何对其进行故障排除[。

## 活动中的错误 {#activity-errors}

测试和发布历程之前，请验证所有活动均已正确配置。 如果系统仍检测到错误，则无法执行测试或发布。

出现错误时，画布上的活动本身会显示警告符号。 将光标放在感叹号上以显示错误消息。 如果选择活动，您应该会看到带警告的错误行。 例如：

* 如果必填字段为空，则会显示错误

  ![历程验证错误显示在带有错误指示器的画布中](assets/journey63.png)

* 在画布中，当两个活动断开连接时，会显示警告

  ![警告图标在历程画布中显示断开连接的活动](assets/canvas-disconnected.png)

## 历程中的错误 {#canvas-errors}

画布上方的&#x200B;**[!UICONTROL 警报]**&#x200B;按钮上也显示错误。 此按钮让您看到系统检测到的错误，这些错误会阻止测试模式激活或历程发布。

系统检测到两种问题：**错误**&#x200B;和&#x200B;**警告**。 错误阻止发布和测试激活。 警告指示未阻止测试激活或发布的潜在问题。 您将看到问题的描述和 ERR_XXX_XXX 类型的问题日志 ID。 这有助于确定问题。

![历程中的错误和警告指示器，带有描述工具提示](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

历程全局的错误和警告首先在列表中显示。 之后，与特定活动相关的错误和警告按活动顺序或在历程中的出现顺序从左到右列出。 在警报列表的底部，**[!UICONTROL 复制详细信息]**&#x200B;按钮允许您复制有关历程的技术信息，这些信息对解决问题很有用。 有关复制的字段列表（包括暂停和恢复信息），请参阅历程属性中的[复制技术详细信息](journey-properties.md#access-properties)。

## 添加替代路径 {#canvas-add-path}

您可以为以下历程活动定义一个在发生错误时的回退操作： **[!UICONTROL 优化]**&#x200B;和&#x200B;**[!UICONTROL 操作]**。

当操作或条件中发生错误时，个人历程将停止。 使其得以继续的唯一方法是解决问题。 为避免中断历程，您还可以选中选项&#x200B;**[!UICONTROL 在活动属性中出现超时或错误时添加替代路径]**。 可在[此部分](../building-journeys/using-the-journey-designer.md#paths)中了解详情。

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页介绍在进入测试模式或发布之前，如何识别和解决历程中的配置错误和警告。

**意图：**

* 在测试或发布历程之前识别活动级配置错误
* 在“警报”面板中区分阻止错误和非阻止警告
* 使用错误日志ID（ERR_XXX_XXX格式）诊断历程问题
* 复制技术历程详细信息并与管理员共享以进行故障排除
* 添加替代路径以防止单个历程在错误或超时时停止

**术语表：**

* **警报按钮**：显示阻止发布或测试激活&#x200B;*（产品特定）的所有系统检测到的错误和警告的画布控件*
* **ERR_XXX_XXX**：分配给每个检测到的问题的问题日志ID格式，用于识别和传达错误&#x200B;*（产品特定）*
* **备用路径**：向操作或条件活动添加了备用分支，当发生错误或超时时，该备用分支将继续历程&#x200B;*（产品特定）*

**护栏：**

* 如果阻止错误仍然未解决，则您无法激活测试模式或发布历程。
* 警告不会阻止发布或测试激活，但会指示潜在问题。
* 替代路径仅适用于优化和操作活动。

**术语：**

* 规范名称：警报 — 缩写：无 — 变体：“警报”面板，“警报”按钮
* 同义词： &quot;errors&quot; = &quot;blocking issues&quot;；&quot;warnings&quot; = &quot;non-blocking issues&quot;
* 请勿混淆：“错误”（阻止发布）≠“警告”（不阻止发布）

**常见问题解答：**

* **问：Journey Optimizer中的错误和警告有何区别？**  — 错误会阻止测试模式激活和历程发布；警告指示潜在问题，但不会阻止测试或发布。
* **问：在哪里可以查看影响我的旅程的所有错误？**  — 单击画布上方的“警报”按钮可查看所有系统检测到的错误和警告的统一列表。
* **问：如果无法从错误描述中识别问题，应该怎么做？**  — 使用“警报”列表底部的“复制详细信息”按钮捕获技术信息并将其发送给管理员。
* **问：即使操作遇到错误，我是否可以为个人保持历程运行？**  — 是，在活动属性中启用“在超时或错误的情况下添加替代路径”选项以定义回退路径。
* **问：何时应该执行这些疑难解答检查？**  — 所有检查都可以在测试模式下或历程处于实时状态时执行；建议先在测试模式下解决所有问题，然后再发布。

+++
