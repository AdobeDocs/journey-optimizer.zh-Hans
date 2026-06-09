---
solution: Journey Optimizer
product: journey optimizer
title: 检查并测试您的WhatsApp消息
description: 了解如何在Journey Optimizer中检查和发送WhatsApp消息
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 31acb095-de90-495f-8e8c-43a78dedfa06
TQID: https://experienceleague.adobe.com/u2OevVu38fPdytpuTmHeSdEx3Wvpih7ifk-j88rhDFI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: b8df23d2-98a2-4406-86cc-2babe8728d36
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 07322bd265647528f8e2e4a5f39d7806fd03b565
workflow-type: tm+mt
source-wordcount: 420
ht-degree: 2%

---

# 检查并发送 WhatsApp 消息 {#send-whatsapp}

## 预览WhatsApp消息 {#preview-whatsapp}

定义消息内容后，您可以使用测试用户档案或从CSV/JSON文件上传的示例输入数据，或手动添加来预览其内容。 如果插入个性化内容，则可以检查此内容在消息中的显示方式。

为此，请单击&#x200B;**[!UICONTROL 模拟内容]**，然后使用测试用户档案数据检查您的消息。

有关如何预览和测试内容的详细信息，请参阅[内容管理](../content-management/preview-test.md)部分。

## 验证您的内容 {#whatsapp-validate}

必须在编辑器的上半部分检查警报。 其中一些是简单的警告，但其他警告可能会阻止您发送消息。 可能会发生两种类型的警报：警告和错误。

* **警告**&#x200B;参考推荐和最佳实践。 例如，如果文本消息为空，则会显示警告消息。

* **错误**&#x200B;会阻止您测试或激活历程，或发布营销活动，前提是这些错误未解决。 例如，当主题行缺失时，会有一条错误消息警告您。

## 发送您的WhatsApp消息 {#whatsapp-send}

>[!IMPORTANT]
>
> 如果您的营销活动受批准政策的约束，则需要请求批准才能发送短信。 [了解详情](../test-approve/gs-approval.md)

当WhatsApp消息就绪时，请完成您的[历程](../building-journeys/publish-journey.md)或[促销活动](../campaigns/review-activate-campaign.md)的配置以发送该消息。

## 分析WhatsApp交互 {#whatsapp-channel-context}

Journey Optimizer会捕获从WhatsApp渠道返回的其他交互数据，并将其存储在`whatsAppChannelContext`字段组下的&#x200B;**AJO — 电子邮件跟踪体验事件数据集**&#x200B;中。 使用这些字段构建[受众](../audience/about-audiences.md)，运行[查询](../data/get-started-queries.md)，并分析WhatsApp参与度。 [了解有关系统数据集的更多信息](../data/get-started-datasets.md#system-datasets)。

捕获以下字段：

| 字段 | 描述 |
|-|-|
| `messageType` | WhatsApp消息类型（例如，`templateBased`，`response`）。 |
| `inboundMessage` | 入站回复内容（例如，`stop`、`start`、`subscribe`）。 |
| `inboundNumber` | 接收入站消息的发件人ID。 |
| `channelType` | 渠道类别（`Utility`、`Marketing`或`Promotional`）。 |
| `profileNumber` | 从中接收入站消息的电话号码。 |
| `origTimestamp` | 来自Meta / WhatsApp的原始时间戳。 |
| `status` | 传递状态，包括标准化的提供商反馈（`sent`、`delivered`、`bounce`、`error`、`delay`、`duplicate`、`denylist`、`exclude`或`unknown`）和原始提供商状态消息。 |
| `reactionEvent` | 用户响应的内容：用于回应的表情符号，或用于回复特定消息的消息文本。 |
| `reactionMessageID` | 要响应的原始消息的ID。 |
| `reactionActionName` | 响应操作的类型（`react`、`unreact`或`reply`）。 |
| `interactiveSelectedTitle` | WhatsApp交互式消息中用户选择的标题。 |
| `interactiveType` | 交互式消息类型（`list reply`、`button reply`或`button`）。 |
| `interactiveSelectedDescription` | 所选WhatsApp交互式选项的说明。 |
| `interactiveSelectedID` | WhatsApp中选定选项的ID。 |

要查询此数据集，请使用查询服务中的`ajo_email_tracking_experience_event_dataset`表。 有关查询模式和相关用例，请参阅[数据集查询示例](../data/datasets-query-examples.md)。
