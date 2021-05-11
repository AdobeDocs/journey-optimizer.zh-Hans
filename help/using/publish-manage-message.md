---
title: 发布和修改消息
description: 了解如何发布和更新消息
snippet: y
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---

# 发布消息{#publish-manage-messages}

![](assets/do-not-localize/badge.png)

## 发布消息{#publish-message}

创建消息后，您可以发布消息以使其可供执行。

>[!CAUTION]
>
>在发布之前，请检查并解决警报。 [了解详情](alerts.md)。

![](assets/publish-message.png)

发布消息后，该消息将添加到消息列表中，其状态为&#x200B;**[!UICONTROL Published]**。

现在，它已准备好由一个或多个[rourneys](building-journeys/journey.md)触发。

## 更新只读消息{#modify-message}

发布后，消息处于只读模式。 您仍然可以通过创建该消息的新草稿来更新它。

这使您能够更新内容或修复问题，例如，无需重新发布整个使用消息的旅程。

>[!NOTE]
>
>在已发布的版本仍处于发布和活动状态时，可以编辑草稿版本。

要更新已发布的消息，请执行以下操作：

1. 在消息列表中，选择要打开的消息。

1. 单击 **[!UICONTROL Modify]**。

   ![](assets/message-modify.png)

1. 确认您的选择。将创建消息的草稿版本。

   ![](assets/message-modify-v2.png)

1. 编辑内容或根据需要更改设置。
1. 单击 **[!UICONTROL Publish]**。此操作将发布将用于下一个执行的消息的新版本。

新版本一经发布，在下次API调用时，将生成新消息执行。 下一个传入用户档案将接收新版本。

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version.-->
