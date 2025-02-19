---
product: experience platform
solution: Experience Platform
title: 上下文数据入门
description: 了解如何在决策管理中利用上下文数据。
feature: Decision Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 9b66f4871d8b539bf0201b2974590672205a3243
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# 上下文数据入门 {#context-data}

作为决策请求的一部分发送的数据被视为上下文数据。 您可以在决策引擎中利用上下文数据，例如，设计一个决策规则，要求在发出决策请求时当前天气为≥80度。

上下文数据在&#x200B;**Decisioning**&#x200B;和&#x200B;**Edge Decisioning** API请求中的定义有所不同。 对于这两种类型的请求，上下文数据可用于资格规则或排名公式，但只有Edge Decisioning API请求可以使用上下文数据来个性化内容。

开始之前，请检查以下护栏和限制：

* 由于在Decisioning调用和Edge Decisioning调用之间传递上下文的方式不同，因此基于上下文的资格规则和排名公式在Decisioning调用和Edge Decisioning调用之间不可互换。
* 只能在Decisioning API中使用`dryrun`参数进行测试。 在Edge Decisioning API中不可用。 请注意，使用Decisioning API将此参数设置为`true`不会影响上限和建议数量。

有关如何在每个API中使用上下文数据的详细信息，请参阅以下章节：

* [在Edge Decisioning请求中使用上下文数据](context-data-edge.md)
* [在Decisioning请求中使用上下文数据](context-data-decisioning.md)

