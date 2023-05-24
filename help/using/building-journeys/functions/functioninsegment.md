---
product: journey optimizer
title: inSegment
description: 瞭解inSegment函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment，函式，運算式，歷程
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 6%

---

# inSegment {#inSegment}

檢查個人是否屬於指定的區段。

>[!NOTE]
>
>您最多可以擷取100個區段。

區段名稱必須是字串常數。 它不能是欄位參考或運算式。

區段定義於 [Adobe Experience Platform](https://platform.adobe.com/segment/overview). 運算式編輯器提供自動完成的區段清單。

區段可以有三種狀態：

* existing： entity會繼續存在於區段中。
* 已實現：實體正在進入區段。
* 退出：實體正在退出區段。

只有具備下列條件的個人 **已實現** 和 **現有** 區段參與狀態會視為區段的成員。 如需如何評估區段的詳細資訊，請參閱 [Segment Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results).

`IF inSegment('segmentName') == true` 表示您擁有狀態為已輸入/現有狀態的segmentMembership。

`ELSE inSegment('segmentName') == false` 表示您擁有退出狀態的segmentMembership。

## 类别

Adobe Experience Platform

## 函式語法

`inSegment(<parameter>)`

## 参数

| 参数 | 描述 | 类型 |
|--- |--- |--- |
| 区段 | 區段名稱 | `<string>` |

## 簽章和傳回的型別

`inSegment(<string>)`

傳回布林值。

## 示例

`inSegment("men over 50")`

解释:

函式將傳回 **[!UICONTROL true]** 如果歷程例項中的個人屬於名為「50歲以上的男性」的Adobe Experience Platform區段， **[!UICONTROL false]** 否則。
