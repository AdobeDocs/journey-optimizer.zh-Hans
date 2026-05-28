---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 上下文数据入门
description: 了解如何在决策管理中利用上下文数据。
badge: label="旧版" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/aVm2FFqkJWN-k1qngYsp94FgKIZWaLCMUneFd0rVNpA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 12%

---

# 上下文数据入门 {#context-data}

>[!TIP]
>
>决策是 [!DNL Adobe Journey Optimizer] 的全新决策功能，现已通过基于代码的体验和电子邮件渠道提供！ [了解详情](../experience-decisioning/gs-experience-decisioning.md)

作为决策请求的一部分发送的数据被视为上下文数据。 您可以在决策引擎中利用上下文数据，例如，设计一个决策规则，要求在发出决策请求时当前天气为≥80度。

上下文数据在&#x200B;**Decisioning**&#x200B;和&#x200B;**Edge Decisioning** API请求中的定义有所不同。 对于这两种类型的请求，上下文数据可用于资格规则或排名公式，但只有Edge Decisioning API请求可以使用上下文数据来个性化内容。

开始之前，请检查以下护栏和限制：

* 由于在Decisioning调用和Edge Decisioning调用之间传递上下文的方式不同，因此基于上下文的资格规则和排名公式在Decisioning调用和Edge Decisioning调用之间不可互换。
* 只能在Decisioning API中使用`dryrun`参数进行测试。 在Edge Decisioning API中不可用。 请注意，使用Decisioning API将此参数设置为`true`不会影响上限和建议数量。

有关如何在每个API中使用上下文数据的详细信息，请参阅以下章节：

* [在Edge Decisioning请求中使用上下文数据](context-data-edge.md)
* [在Decisioning请求中使用上下文数据](context-data-decisioning.md)
