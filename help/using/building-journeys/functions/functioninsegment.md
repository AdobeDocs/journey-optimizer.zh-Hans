---
product: journey optimizer
title: inSegment
description: 了解inSegment中的函数
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment，函数，表达式，历程
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: be372f8f80d304067748d539fb8e210df6280721
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 6%

---

# inSegment {#inSegment}

检查个人是否属于给定受众。

>[!NOTE]
>
>您最多可以检索100个受众。

受众名称必须是字符串常量。 它不能是字段引用，也不能是表达式。

受众可在以下位置定义： [Adobe Experience Platform](https://platform.adobe.com/audience/overview). 表达式编辑器提供自动完成的受众列表。

受众可以具有三种状态：

* 现有：实体继续位于受众中。
* 已实现：实体正在进入受众。
* 退出：实体正在退出受众。

仅具有 **已实现** 和 **现有** 受众参与状态将被视为受众的成员。 有关如何评估受众的更多信息，请参阅 [Segmentation Service文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results).

`IF inSegment('segmentName') == true` 表示您拥有segmentMembership且状态为entered/existing。

`ELSE inSegment('segmentName') == false` 表示您具有已退出状态的segmentMembership。

## 类别

Adobe Experience Platform

## 函数语法

`inSegment(<parameter>)`

## 参数

| 参数 | 描述 | 类型 |
|--- |--- |--- |
| 区段 | 受众名称 | `<string>` |

## 签名和返回的类型

`inSegment(<string>)`

返回布尔值。

## 示例

`inSegment("men over 50")`

说明：

函数将返回 **[!UICONTROL true]** 如果旅程实例中的个人是名为“50岁以上的男性”的Adobe Experience Platform受众的一部分， **[!UICONTROL false]** 否则。
