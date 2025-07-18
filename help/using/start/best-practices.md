---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer最佳实践
description: 详细了解Journey Optimizer最佳实践
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 271fb85d-5621-4a12-b3d1-65cf6021b174
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 4%

---

# 最佳实践 {#best-practices}

## 实时用例和全渠道个性化指南 {#real-time-guidance}

在Identity Service 2.0更新后，实时身份拼接发生了变化。

Adobe Journey Optimizer利用Identity Service来合并用户档案并个性化用户体验。 因此，在您构建用例时，需要注意该服务的一些重要方面。 作为品牌，您希望向个人交付体验。 通过身份图，营销人员能够了解人员跨各种渠道与哪些设备相关联。 图形可以包含表示人员(CRMID)或Web浏览器(ECID)的身份。 Identity Service会将这些信息拼合在一起，以创建人员的“360度视图”或合并的个人资料。 这意味着，当有人浏览您的网站并登录时，该会话中的所有先前数据都可以与该登录用户相关联。 此操作可通过几个不同的步骤执行：

1. 身份的初始拼合 — 当人员登录时，登录标识符(CRMID)与Web浏览器标识符（Web或移动应用程序会话）相关联：

   * 完成此过程可能需要30分钟 — 4小时。
   * 通常，此登录事件将生成一个标识图，用于将CRMID与ECID链接在一起。

1. 初次拼合后，使用两个身份之一发送的任何数据都将关联到合并的个人资料，并可用于在Journey Optimizer中实时个性化。 使用最新行为数据更新用户档案最多可能需要1分钟才能完成。 请参见[此页面](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=zh-Hans)。

构建用例时，请考虑以下事项：

1. 品牌希望在放弃30分钟后重新吸引网站访客(例如， 已放弃的购物车电子邮件)：

   对数据 — ECID使用身份。 如果您希望捕获最近30分钟内给出其电子邮件地址/应用程序安装的全部访客，则应当使用基于Cookie的标识来启动此历程(ECID)。 这假定您的电子邮件地址、推送令牌或体验的其他地址已与ECID关联。

1. Web、电子邮件、推送等上的全渠道参与。：

   * 参与时，您必须在用户档案上提供通信地址。 为了确保一致且及时地发生这种情况，请确保您的数据与要使用的身份相关联。
   * 如果您需要使用来自新安装的应用程序或浏览器会话的信息以及已知或已登录的信息，则需要在这些身份拼合后发送此通信。 这可能因客户而异，我们建议至少等待30分钟以获取最大数量的用户档案。

## 使用历程护栏缩放 {#scale}

本节将指导您如何根据以下两个限制进行扩展：

* Journey Optimizer在旅程画布中包含50个活动的护栏。 此护栏旨在帮助提高可读性、QA和疑难解答。 当您将活动数量限制在10个以内时，历程中的活动数量将显示在历程画布的左上部分。

* 当您发布历程时，Journey Optimizer会自动进行扩展和调整，以确保最大吞吐量和稳定性。 当您在沙盒中一次接近100个实时历程的里程碑时，您将看到此成就的界面中显示一个橙色叠加和警告标记。 如果您看到此通知，并且需要将每次的历程扩展到多于 100 个实时历程，请创建客户关怀支持工单，我们将帮助您实现目标。

<!--DOCAC-10977

* As you publish journeys, Journey Optimizer automatically scales and adjusts to ensure maximum throughput and stability. As you near the milestone of 500 live journeys at one time in a sandbox, you will see an orange overlay and warning sign appear in the interface on this achievement. If you see this notification and have a need to extend your journeys beyond 500 live journeys at a time, please create a ticket for customer care and we will help you reach your goals.-->


您可以采用许多最佳实践，帮助您保持在护栏内并高效使用系统。

* 如果您即将达到实时历程的限制，您可以采取的第一个步骤是转到&#x200B;**历程**&#x200B;下的&#x200B;**概述**&#x200B;选项卡，以查看过去24小时内有多少具有活动用户档案的历程处于活动状态。 您可以在此部分中检查进入和退出历程的用户档案数，以确定这一点。

  ![](assets/journey-guardrails2.png)

* 接下来，在历程清单部分中，您可以按状态=“实时”和类型=“读取受众”筛选所有历程。 然后按发布日期（从最旧到最新）排序。 单击进入历程，然后转到计划。 停止所有计划运行&#x200B;**一次**&#x200B;或&#x200B;**尽快**&#x200B;且时间超过一天的实时历程，并且只执行一个操作。

  ![](assets/journey-guardrails1.png)

* 如果您的&#x200B;**读取受众**&#x200B;历程只执行一项操作、不等待/做出决策或发送时间优化，请考虑将它们移动到Journey Optimizer营销活动。 营销活动更适合单步参与。 Campaign和历程之间的主要区别之一是，您是否认为积极倾听用户参与以确定下一步并参与其他操作很重要。
* 要减少历程中的活动数，请检查条件步骤。 在许多情况下，您可以将条件移动到区段定义或受众构成中。
* 如果在多个历程（同意检查、抑制）中重复存在相同的条件，请考虑在区段定义中移动它们。 例如，如果您有一个条件来检查多个历程中的“电子邮件地址不为空”，则将该条件作为区段定义的一部分包含。
* 如果您的历程存在多个条件，需要拆分受众才能查看每个步骤的数字，请考虑使用更适合分析的Customer Journey Analytics或其他报表解决方案。
* 如果接近画布上的节点限制，请考虑使用动态参数或内容合并操作以提供正确的内容，而不是显式节点。

* 如果您有一个包含批处理区段(A)的&#x200B;**读取受众**&#x200B;历程，并且您在历程中使用的inAudience流区段(B)进行排除（即执行A-B），请考虑将该逻辑移动到分段逻辑，并将排除项用作分段逻辑本身的一部分。