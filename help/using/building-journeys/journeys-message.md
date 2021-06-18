---
title: 在历程中添加消息
description: 在历程中添加消息
feature: 历程
topic: 内容管理
role: User
level: Intermediate
source-git-commit: d76eee0efa6735d6d81d7d7c752ed253b4cbebb5
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---

# 在历程中添加消息

[!DNL Journey Optimizer] 消息功能是内置的，您只需设计内容并发布消息即可。请参阅[此小节](../get-started-content.md)。然后，您只需在历程中添加使用Journey Optimizer设计的推送或电子邮件消息即可。

如果您使用第三方系统发送消息，则可以创建自定义操作。 在此[部分](../action/action.md)中了解详情。

## 添加消息活动

1. 与往常一样，从事件或&#x200B;**读取区段**&#x200B;活动开始您的历程。

   ![](../assets/jo-message0.png)

1. 从面板的&#x200B;**Actions**&#x200B;部分，将&#x200B;**Message**&#x200B;活动拖放到画布中。

   ![](../assets/jo-message1.png)

1. 添加标签和描述。

   ![](../assets/jo-message2.png)

1. 在&#x200B;**Message**&#x200B;字段内单击。 将显示在Journey Optimizer中设计的可用消息列表。 您可以按状态过滤列表。

   ![](../assets/jo-message3.png)

1. 选择消息并单击&#x200B;**选择**。 您还可以通过单击&#x200B;**创建消息**，直接从此屏幕创建新消息。

   ![](../assets/jo-message4-ter.png)

   如果要检查消息，可以单击&#x200B;**消息**&#x200B;字段中的&#x200B;**打开消息**&#x200B;图标。 该消息将在新选项卡中打开。

   ![](../assets/jo-message4-bis.png)

1. 向历程中添加后续步骤。

## 电子邮件参数和推送参数

**[!UICONTROL Email parameters]**&#x200B;和&#x200B;**[!UICONTROL Push parameters]**&#x200B;部分显示只读字段。 通常在创建消息时执行此配置。 请参阅[此小节](../get-started-content.md)。

![](../assets/jo-message4.png)

要强制使用特定值，可以使用字段右侧的&#x200B;**启用参数覆盖**&#x200B;图标。 此选项可用于测试目的。 例如，对于电子邮件，您可以添加电子邮件地址。 发布历程后，将向您发送电子邮件。
