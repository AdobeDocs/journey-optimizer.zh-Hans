---
solution: Journey Optimizer
product: journey optimizer
title: 优化活动
description: 了解优化活动
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 活动、条件、画布、历程、优化
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/hbDoGEHdCBcOe-e9h06kGY2Rvb129cIzto6jJAuGkX4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 470
ht-degree: 17%

---

# 开始使用优化活动 {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="优化活动"
>abstract="通过&#x200B;**优化**&#x200B;活动，您可以基于特定标准（包括实验、目标选择和特定条件）创建多条路径，由此定义个人在您的历程中的进度情况。 请注意，**优化**&#x200B;活动是创建历程中条件路径的新工具。 它取代了以前的&#x200B;**条件**&#x200B;活动。"

>[!IMPORTANT]
>
>**优化**&#x200B;活动是在历程中创建条件路径的新工具。 它取代了以前的&#x200B;**条件**&#x200B;活动，该活动已从 UI 中移除。 所有条件逻辑都将保留，并且现在通过&#x200B;**Optimize**&#x200B;活动的[条件](conditions.md)进行处理。
>
>如果您现有历程使用了&#x200B;**[!UICONTROL 条件]**&#x200B;活动，则可以继续像以前一样使用它们。 它们现在有一个新图标，显示为&#x200B;**[!UICONTROL 使用**&#x200B;[!UICONTROL &#x200B; Condition &#x200B;]&#x200B;**方法优化]**&#x200B;活动，但行为保持不变。 您在节点上设置的任何自定义标签都将保留。

通过&#x200B;**优化**&#x200B;活动，您可以根据特定条件（包括试验、定位和特定条件）创建多个&#x200B;**路径**，从而定义个人如何完成您的历程 — 确保最大程度的参与并成功创建高度自定义且有效的历程。

历程活动面板中的![优化按钮](assets/journey-optimize.png)

## 什么是历程路径？ {#journey-path}

历程&#x200B;**路径**&#x200B;可由以下任意项组成：通信排序、通信间隔时间、通信次数或这三个变量的任意组合。

例如，一个路径可以包含一封电子邮件，另一个路径可以包含两封短信消息，第三个路径可以包含一封电子邮件，两个小时的“等待”节点，然后是一封短信消息。

## 优化历程的三种方法 {#optimization-methods}

通过&#x200B;**优化**&#x200B;活动，您可以对历程路径执行以下操作：

* [运行路径实验](path-experimentation.md) — 根据随机拆分测试不同的路径，以确定哪些路径根据预定义的成功量度（例如：转化率、收入、参与度）表现最佳。

* [利用定位规则](path-targeting.md) — 根据受众区段、用户档案属性或上下文数据，定义客户必须符合的特定规则，以便有资格输入历程路径之一。 这可确保正确的受众进入指定的路径。

  >[!AVAILABILITY]
  >
  >此功能当前处于“有限可用”状态。 要请求访问权限，请与 Adobe 代表联系。

* [应用条件](conditions.md) — 根据特定条件（如数据源、时间、日期、百分比拆分或配置文件上限）创建条件路径。 这与之前的Condition活动相同。

## 工作原理 {#how-it-works}

历程上线后，系统会根据定义的标准评估用户档案，并根据匹配标准，将用户档案沿历程中的相应路径发送。

## 后续步骤 {#next-steps}

选择最适合您的用例的优化方法：

* 想要测试并了解哪条路径效果最佳？ →转到[路径试验](path-experimentation.md)
* 希望通过特定路径发送不同受众？ →转至[路径定位](path-targeting.md)
* 要创建条件逻辑（if/then方案）？ →转至[条件](conditions.md)
