---
solution: Journey Optimizer
product: journey optimizer
title: 与智能服务集成
description: 了解如何在Journey Optimizer中利用Adobe智能服务和客户人工智能预测
feature: Journeys, Integrations
topic: Artificial Intelligence
role: User
level: Intermediate
keywords: 人工，人工智能，智能，旅程，服务
exl-id: 20da09e1-0611-4d27-a589-30552011e06c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/rTKcWHwfwleQtD68fcdeqYK2AMQHVaknKtsNDFsOldI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eb30f47f-d87a-400f-8f78-63ce7979ff56
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 0%

---

# 与智能服务集成 {#ai-overview}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何将Adobe Intelligent Services和客户人工智能预测与Journey Optimizer集成，以将流失和转化得分用作用于决策、操作和区段构建的个人资料属性。

>[!ENDSHADEBOX]

与&#x200B;**[!DNL Adobe Intelligent Services]**&#x200B;的集成使您能够将人工智能和机器学习用于客户体验用例。 这允许营销分析人员使用业务级配置根据公司需求设置预测，而无需数据科学专业知识。

[!DNL Intelligent Services]基于[!DNL Adobe Experience Platform]构建，为客户体验团队提供AI-as-a-service。 它有助于预测客户行为、衡量促销活动影响以及提高投资回报。 有关详细信息，请参阅[[!DNL Adobe Experience Platform] 文档](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/home.html){target="_blank"}。

[!DNL Journey Optimizer]和[!DNL Intelligent Services]之间的集成允许您利用客户预测。

[!DNL Adobe Intelligent Services]的组件Customer AI可预测可能的客户操作。 请参阅[[!DNL Adobe Experience Platform] 文档](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/customer-ai/overview.html){target="_blank"}。

客户人工智能允许品牌创建基于流失率或转化率机器学习的分数。 这些得分可作为[!DNL Adobe Experience Platform]个人资料（实时客户个人资料）中的个人资料属性使用。

因此，这些属性可以与Journey Optimizer中的任何其他配置文件属性一样使用。 在用于决策、操作或构建区段的条件中使用它们。

![显示倾向分数和预测的Customer AI集成](assets/customer-ai.png)

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

- **TL；DR：**&#x200B;本页介绍Journey Optimizer如何与Adobe智能服务（尤其是客户人工智能）集成，以利用基于机器学习的倾向得分作为历程中的配置文件属性。

**意图：**
- 了解Adobe智能服务如何与Journey Optimizer集成
- 在历程条件或操作中将客户人工智能倾向得分用作用户档案属性
- 支持人工智能驱动的流失或转化预测，而无需数据科学专业知识
- 将机器学习得分应用于Journey Optimizer中的区段构建

**术语表：**
- **Adobe Intelligent Services**：一套基于Adobe Experience Platform构建的AI/ML服务，它支持客户体验预测，而无需数据科学专业知识&#x200B;*（产品特定）*
- **客户人工智能**： Adobe Intelligent Services的一个组件，可生成客户个人资料的基于机器学习的流失或转化倾向分数&#x200B;*（产品特定）*
- **倾向分数**：基于机器学习的分数，表示客户执行特定操作（例如，流失或转化）的可能性，存储为配置文件属性&#x200B;*（产品特定）*

**护栏：**
- 无需具备数据科学专业知识，但营销分析师必须完成业务级配置
- 必须先在Adobe Experience Platform中配置客户人工智能分数，然后才能在Journey Optimizer中用作配置文件属性

**术语：**
- 规范名称：Adobe Intelligent Services — 缩写：none — 变体：Intelligent Services、AI服务
- 规范名称：客户人工智能 — 首字母缩略词：none — 变体：客户人工智能分数、倾向分数
- 同义词：“流失分数”=“流失倾向”；“转化分数”=“转化倾向”
- 请勿混淆：“Adobe智能服务”≠“AI助手”（智能服务是一个预测性ML平台；AI助手是一个对话界面）

**常见问题解答：**
- **问：在Journey Optimizer的上下文中什么是客户人工智能？**  — 客户人工智能是Adobe智能服务组件，它创建基于机器学习的流失或转化分数，这些分数作为配置文件属性在Journey Optimizer条件、操作和区段构建中可用。
- **问：要使用Adobe智能服务，我是否需要数据科学技能？**  — 不可以，营销分析人员可以使用业务级设置配置预测，而无需具备数据科学专业知识。
- **问：客户人工智能得分存储在何处？**  — 它们作为配置文件属性存储在Adobe Experience Platform Real-time Customer Profile中，可供访问，就像Journey Optimizer中的任何其他配置文件属性一样。
- **问：如何在历程中使用客户人工智能分数？**  — 一旦得分可用作用户档案属性，便可在用于决策、操作配置或构建受众区段的条件中使用得分。

+++
