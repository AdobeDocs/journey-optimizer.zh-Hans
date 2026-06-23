---
solution: Journey Optimizer
product: journey optimizer
title: 时区管理
description: 了解时区管理
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: 时区，属性，历程，条件，时间，日期，自定义
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/PdwGEuWqJcncbkokE0eOhMaEk9L0AmCJ--VZBxxtDDU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 996
ht-degree: 8%

---

# 时区管理 {#timezone_management}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何设置历程的时区（固定时区或从每个配置文件中获取的时区），以控制基于时间的活动（如时间条件、日期条件和自定义等待运行）的时间。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="历程时区"
>abstract="时区设置用于定义历程所使用的时区。 当使用固定时区时，对于所有进入历程的个人来说都是相同的。"


您可以在历程的[属性](../building-journeys/journey-properties.md#timezone)中定义时区。

要访问历程属性，请选择屏幕右上角的铅笔图标。

此时区将用于包含时间元素的历程的每个活动，例如：

* [时间条件](../building-journeys/conditions.md#time_condition)
* [日期条件](../building-journeys/conditions.md#date_condition)
* [自定义等待](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

您可以选择[固定时区](#fixed-timezone)或选择使用用户配置文件[&#128279;](#timezone-from-profiles)中定义的时区。

## 定义固定时区 {#fixed-timezone}

时区可以固定。 清除预定义的时区并从下拉列表中选择一个时区。 如果您使用固定时区，则所有进入旅程的个人都将使用相同的时区。

为此，请在&#x200B;**[!UICONTROL 历程属性]**&#x200B;窗格中选择时区。

历程属性中的![时区选择下拉列表](assets/journey72.png)

## 使用轮廓时区 {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="使用轮廓时区"
>abstract="此选项会在&#x200B;**等待**&#x200B;和&#x200B;**条件**&#x200B;活动中使用实时轮廓时区。 如果已为轮廓定义了时区，就会检索并在历程中使用这个时区。 否则，就会使用上面时区字段中定义的时区。"

如果历程的进入事件具有命名空间，这意味着历程可以访问[!DNL Adobe Experience Platform]的实时客户个人资料服务，则您可能希望使用在个人资料级别定义的时区。 为此，请在&#x200B;**属性**&#x200B;中选中&#x200B;**在等待和条件中使用配置文件时区**。 默认情况下不选中此选项。

如果为用户档案定义了时区，则历程会检索并使用它。 如果没有，则使用的时区是在时区字段中定义的时区。

![在数据源中配置个性化计时的时区](assets/journey73.png)

>[!NOTE]
>
>配置文件时区与&#x200B;**首选项详细信息**&#x200B;字段组中现有的&#x200B;**时区**&#x200B;字段一起使用。

## 在表达式中使用时区 {#timezone-in-expressions}

历程的开始和结束日期无法链接到特定时区。 它们会自动关联到实例的时区。

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页介绍如何在Adobe Journey Optimizer历程属性中配置时区设置，并选择应用于所有配置文件的固定时区，或者选择来自实时客户配置文件的每个配置文件的时区。

**意图：**
* 在历程中设置固定时区，以便所有用户档案遵循条件和等待的相同时间引用
* 启用每个配置文件的时区，以便“等待”和“条件”活动使用每个配置文件存储的时区首选项
* 了解哪些历程活动受历程时区设置影响
* 标识存储单个时区值的配置文件字段组

**术语表：**
* **固定时区**：在历程属性中选择的单个时区统一应用于进入历程&#x200B;*（产品特定）*&#x200B;的每个配置文件
* **配置文件时区**：存储在“首选项详细信息”字段组的`timeZone`字段中的每个人的时区，在“在等待和条件中使用配置文件时区”选项启用时使用&#x200B;*（产品特定）*
* **首选项详细信息字段组**：包含用于配置文件级时区解析的`timeZone`属性的XDM字段组

**护栏：**
* “在等待和条件中使用配置文件时区”选项仅在历程的进入事件具有命名空间（即，历程可以到达实时客户配置文件服务）时可用
* 默认情况下不选中该选项；除非明确启用，否则使用固定时区
* 如果启用了选项，但未在配置文件上定义时区，则历程将回退到历程属性中定义的固定时区
* 历程的开始和结束日期无法链接到特定时区；它们自动与实例的时区相关联

**术语：**
* 规范名称：时区管理 — 缩写：无 — 变体：时区配置、历程时区
* 同义词：“固定时区”=“对所有个人都相同”；“配置文件时区”=“在等待和条件中使用配置文件时区”
* 请勿混淆：“历程时区”（适用于活动）≠“实例时区”（适用于自动设置的历程开始/结束日期）

**常见问题解答：**
* **问：我该在何处设置历程的时区？**  — 在历程属性窗格中，可通过旅程画布右上角的铅笔图标访问。
* **问：哪些活动使用历程时区？**  — 时间条件、日期条件和自定义等待活动。
* **问：如何使每个配置文件都遵循自己的本地时区？**  — 在历程属性中，启用“在等待和条件中使用配置文件时区”选项。 这要求历程具有命名空间，以便能够访问实时客户档案服务。
* **问：如果配置文件未定义时区，并且配置文件时区选项已启用，会发生什么情况？**  — 历程回退到在历程属性的时区字段中定义的固定时区。
* **问：哪个配置文件字段存储了个人的时区？**  — 配置文件架构中“首选项详细信息”字段组内的`timeZone`字段。
* **问：我能否将历程的开始和结束日期设置为特定时区？**  — 不。 历程的开始日期和结束日期会自动与实例的时区关联，并且无法链接到自定义时区。

+++
