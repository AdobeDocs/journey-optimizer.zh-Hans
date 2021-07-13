---
title: 创建 IP 池
description: '"了解如何管理ip池"'
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: 应用程序设置
topic: 管理
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 3%

---


# 创建 IP 池

## 关于IP池

使用Journey Optimizer，您可以创建IP池以将子域的IP地址分组到一起。

强烈建议创建IP池，以便电子邮件可投放。 这样，您就可以防止子域的声誉影响您的其他子域。

例如，一个最佳实践是为营销消息提供一个IP池，为事务型消息设置一个IP池。 这样，如果您的其中一条营销消息性能不佳，且客户声明为垃圾邮件，则不会影响发送给该客户的事务型消息，该客户仍将接收事务型消息（购买确认、密码恢复消息等）。

## 创建IP池

要创建IP池，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL IP pools]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL Create IP Pool]**。

   ![](../assets/ip-pool-create.png)

1. 为IP池提供名称和描述（可选）。

   >[!NOTE]
   >
   >子域的名称必须以字母(A-Z)开头，并且只包含字母数字字符或特殊字符(_、 ., -)。

1. 从下拉列表中选择要包含在池中的IP地址，然后单击&#x200B;**[!UICONTROL Submit]**。

   ![](../assets/ip-pool-config.png)

   >[!NOTE]
   >
   >随您的实例配置的所有IP地址都可在列表中找到。

IP池现已创建并显示在列表中。 您可以选择它以访问其属性并显示关联的消息预设。 有关如何将消息预设与IP池关联的更多信息，请参阅[此部分](message-presets.md))。

![](../assets/ip-pool-created.png)

要编辑IP池，请将其打开，然后根据需要编辑其属性。

>[!NOTE]
>
>如果消息预设已与IP池关联，则您首先需要先将其删除，然后再编辑IP池。 完成修改后，您可以再次关联消息预设。
