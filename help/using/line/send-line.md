---
solution: Journey Optimizer
product: journey optimizer
title: 检查并测试您的短信
description: 了解如何在Journey Optimizer中检查和发送LINE消息
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: fd8437c6-0052-4116-af60-5624569bda65
TQID: https://experienceleague.adobe.com/Bfu4AL1axI4XUq0PKXuN0PnnxNvq4MB-O7Bzz66mtbU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 236
ht-degree: 0%

---

# 检查并发送您的LINE消息 {#send-line}

## 预览您的短信 {#preview-line}

定义消息内容后，您可以使用以下任一模拟方法预览其内容：

* 单击&#x200B;**[!UICONTROL 模拟内容]**&#x200B;以测试内容变体与样本输入数据或AI自动生成。 [了解如何模拟内容变体](../test-approve/simulate-sample-input.md)
* 单击&#x200B;**[!UICONTROL 模拟内容]**，然后从下拉列表中选择&#x200B;**[!UICONTROL 模拟内容（AEP配置文件）]**&#x200B;以使用测试配置文件进行预览。

有关如何预览和测试内容的详细信息，请参阅[内容管理](../content-management/preview-test.md)部分。

## 验证您的内容 {#line-validate}

必须在编辑器的上半部分检查警报。 其中一些是简单的警告，但其他警告可能会阻止您发送消息。 可能会发生两种类型的警报：警告和错误。

* **警告**&#x200B;参考推荐和最佳实践。 例如，如果文本消息为空，则会显示警告消息。

* **错误**&#x200B;会阻止您测试或激活历程，或发布营销活动，前提是这些错误未解决。 例如，当主题行缺失时，会有一条错误消息警告您。

## 发送您的LINE消息 {#line-send}

>[!IMPORTANT]
>
> 如果您的营销活动受批准政策的约束，则需要请求批准才能发送短信。 [了解详情](../test-approve/gs-approval.md)

当LINE消息就绪时，请完成[历程](../building-journeys/journey-gs.md)或[营销活动](../campaigns/create-campaign.md)的配置以发送该消息。
