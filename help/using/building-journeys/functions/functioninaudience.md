---
product: journey optimizer
title: 受众内
description: 了解inAudience中的函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience，函数，表达式，历程
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 6e733e94e492fb46014e140b90e2aa47d64d584f
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 5%

---

# 受众内 {#inAudience}

检查个人是否属于给定受众。

>[!NOTE]
>
>您最多可以检索100个受众。

受众名称必须是字符串常量。 它不能是字段引用，也不能是表达式。

受众是在[Adobe Experience Platform](https://platform.adobe.com/audience/overview)中定义的。 表达式编辑器提供自动完成的受众列表。

受众可以有两种状态：

* 已实现：实体符合区段定义的条件。
* 退出：实体正在退出区段定义。

只有具有&#x200B;**已实现**&#x200B;受众参与状态的个人才会被视为受众的成员。 有关如何评估受众的更多信息，请参阅[分段服务文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results)。

`inAudience('audienceName') == true`表示您具有输入状态的segmentMembership。

`inAudience('audienceName') == false`表示您具有已退出状态的segmentMembership。

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


>[!CAUTION]
>
>更改现有受众的名称不会自动更新历程表达式中对该受众的任何引用。 如果条件节点使用inAudience(&#39;oldAudienceName&#39;)，则必须手动编辑表达式以使用新名称。 否则，将导致历程条件中断。