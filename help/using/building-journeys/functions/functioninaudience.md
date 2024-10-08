---
product: journey optimizer
title: 受众内
description: 了解inAudience中的函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience，函数，表达式，历程
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 6%

---

# 受众内 {#inAudience}

检查个人是否属于给定受众。

>[!NOTE]
>
>您最多可以检索100个受众。

受众名称必须是字符串常量。 它不能是字段引用，也不能是表达式。

受众是在[Adobe Experience Platform](https://platform.adobe.com/audience/overview)中定义的。 表达式编辑器提供自动完成的受众列表。

受众可以具有三种状态：

* 现有：实体继续位于受众中。
* 已实现：实体正在进入受众。
* 退出：实体正在退出受众。

只有具有&#x200B;**已实现**&#x200B;和&#x200B;**现有**&#x200B;受众参与状态的个人才会被视为受众的成员。 有关如何评估受众的更多信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results)。

`inAudience('audienceName') == true`表示您拥有segmentMembership状态为entered/existing。

`inAudience('audienceName') == false`表示您拥有退出状态的segmentMembership。

## 类别

Adobe Experience Platform

## 函数语法

`inAudience(<parameter>)`

## 参数

| 参数 | 描述 | 类型 |
|--- |--- |--- |
| 受众 | 受众名称 | `<string>` |

## 签名和返回的类型

`inAudience(<string>)`

返回布尔值。

## 示例

`inAudience("men over 50")`

说明：

如果历程实例中的个人是名为“50岁以上的男性”的Adobe Experience Platform受众的一部分，则函数将返回&#x200B;**[!UICONTROL true]**，否则返回&#x200B;**[!UICONTROL false]**。
