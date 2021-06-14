---
title: 发布和修改消息
description: 了解如何发布和更新消息
snippet: y
feature: 历程
topic: 内容管理
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 4%

---

# 发布消息{#publish-manage-messages}

![](assets/do-not-localize/badge.png)

## 发布消息{#publish-message}

创建消息后，可以将其发布以供执行。

>[!CAUTION]
>
>在发布之前，请检查并解析警报。 [了解详情](alerts.md)。

![](assets/publish-message.png)

发布消息后，该消息将添加到消息列表，并显示&#x200B;**[!UICONTROL Published]**&#x200B;状态。

现在，它已准备好由一个或多个[journeys](building-journeys/journey.md)触发。

## 更新只读消息{#modify-message}

发布后，消息将处于只读模式。 您仍可以通过创建该消息的新草稿来更新它。

例如，这样，您就可以更新内容或修复问题，而无需重新发布使用消息的整个历程。

>[!NOTE]
>
>在已发布版本仍处于发布状态且处于活动状态时，可以编辑草稿版本。

要更新已发布的消息，请执行以下操作：

1. 从消息列表中，选择您的消息以将其打开。

1. 单击 **[!UICONTROL Modify]**。

   ![](assets/message-modify.png)

1. 确认您的选择。将创建消息的草稿版本。

   ![](assets/message-modify-v2.png)

1. 编辑内容或根据需要更改设置。
1. 单击 **[!UICONTROL Publish]**。此操作将发布将用于下次执行的消息的新版本。

新版本一经发布，下次调用API时，将生成新消息执行。 下一个传入用户档案将接收新版本。

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version.-->
