---
solution: Journey Optimizer
product: journey optimizer
title: 预览、验证和发送LINE消息
description: 了解如何预览和验证LINE消息、解决警告和错误、在需要时请求批准，以及在历程或营销活动中激活或发布它
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: fd8437c6-0052-4116-af60-5624569bda65
TQID: https://experienceleague.adobe.com/Bfu4AL1axI4XUq0PKXuN0PnnxNvq4MB-O7Bzz66mtbU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 94a7cd6e4e89b2c8a4a09cfb4fbfc173ca76c391
workflow-type: tm+mt
source-wordcount: 400
ht-degree: 2%

---


# 预览、验证和发送LINE消息 {#send-line}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;预览和验证LINE消息，解决警告和错误，必要时请求审批，并完成历程或营销活动配置以发送消息。

>[!ENDSHADEBOX]

## 开始之前 {#before-you-start}

在开始之前，请确保：

* 已为您的组织启用LINE。 如果LINE不可用，请联系您的Adobe代表以请求激活。
* Journey Optimizer中提供了LINE渠道配置。 请参阅[配置LINE频道](./line-configuration.md)。
* 您已将LINE操作添加到历程或营销策划并定义了消息内容。 请参阅[创建LINE消息](./create-line.md)。

## 预览LINE消息 {#preview-line}

定义消息内容后，使用&#x200B;**[!UICONTROL 模拟内容]**&#x200B;在发送之前预览消息。

您可以使用以下任一选项：

| 模拟选项 | 使用它可以 |
| --- | --- |
| **[!UICONTROL 模拟内容]** | 通过样本输入数据或AI自动生成测试内容变体。 |
| **[!UICONTROL 模拟内容]** > **[!UICONTROL 模拟内容（AEP配置文件）]** | 预览包含测试用户档案的消息。 |

查看每个变体并验证消息内容和个性化值是否按预期显示。

有关预览和测试内容的详细信息，请参阅[预览和测试内容](../content-management/preview-test.md)。

## 验证您的内容 {#line-validate}

在继续操作之前，请查看消息编辑器顶部显示的警报。

Journey Optimizer显示两种类型的警报：

* **警告**&#x200B;是推荐或最佳实践建议。 它们不会阻止您测试或发送消息。
* **错误**&#x200B;标识在测试或激活历程或发布营销活动之前必须解决的问题。

请先解决所有错误，然后再继续。 当警告指示消息可能无法提供预期客户体验时，解决该警告。

## 请求审批（如果需要） {#line-approval}

如果您的营销活动受批准政策的约束，则在发送消息之前请求批准。

请参阅[了解如何请求审批](../test-approve/gs-approval.md)。

## 发送您的LINE消息 {#line-send}

消息就绪后，返回包含LINE操作的历程或营销活动，并完成其配置：

* **历程：**&#x200B;完成历程配置，然后激活历程。
* **促销活动：**&#x200B;完成促销活动配置，然后发布促销活动。

如果无法激活历程或发布营销活动，请返回消息编辑器并解决任何剩余的错误。

## 相关任务 {#related-tasks}

* [LINE 快速入门](./get-started-line.md)
* [创建 LINE 消息](./create-line.md)
* [配置LINE](./line-configuration.md)

{{$include /help/_includes/do-not-localize/line/ai-augmented-send-line.md}}
