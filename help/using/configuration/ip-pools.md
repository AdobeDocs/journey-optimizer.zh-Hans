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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 7d7c1b72530d99b8cceb1067f2576ad66c0052a6
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---

# 创建 IP 池

## 关于IP池 {#about-ip-pools}

使用Journey Optimizer，您可以创建IP池以将子域的IP地址分组到一起。

强烈建议创建IP池，以便电子邮件可投放。 这样，您就可以防止子域的声誉影响您的其他子域。

例如，一个最佳实践是为营销消息提供一个IP池，为事务型消息设置一个IP池。 这样，如果您的其中一条营销消息性能不佳，且客户声明为垃圾邮件，则不会影响发送给该客户的事务型消息，该客户仍将接收事务型消息（购买确认、密码恢复消息等）。

## 创建IP池 {#create-ip-pool}

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

## 编辑IP池 {#edit-ip-pool}

要编辑IP池，请执行以下操作：

1. 在列表中，单击IP池名称以将其打开。

   ![](../assets/ip-pool-list.png)

1. 根据需要编辑其属性。 您可以修改描述，并添加或删除IP地址。

   ![](../assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >考虑删除IP时请格外小心，因为这会给其他IP带来额外负载，并且可能会对您的投放能力造成严重影响。 如有疑问，请联系可投放性专家。

1. 保存更改。

>[!NOTE]
>
>IP池名称不可编辑。 如果要修改IP池，您需要删除该IP池，然后使用您选择的名称创建另一个IP池。

根据与[消息预设](message-presets.md)关联的IP池是否关联，更新会立即或异步生效：

* 如果在消息预设中选择的IP池为&#x200B;**未**，则更新为即时（**[!UICONTROL Success]**&#x200B;状态）。
* 如果在消息预设中选择了IP池&#x200B;****，则更新最长可能需要7-10个工作日（**[!UICONTROL Processing]**&#x200B;状态）。

<!--If a message preset has been associated with the IP pool, you first need to remove it before editing the IP pool. Once the your modifications have been done, you can associate the message preset again.-->

要检查IP池更新状态，请单击&#x200B;**[!UICONTROL More actions]**&#x200B;按钮并选择&#x200B;**[!UICONTROL Recent updates]**。

![](../assets/ip-pool-recent-update.png)

>[!NOTE]
>
>成功更新IP池后，您可能需要等待：
>* 在被单一报文使用前几分钟，
>* 直到IP池的下一个批处理消息生效。


您还可以使用&#x200B;**[!UICONTROL Delete]**&#x200B;按钮删除IP池。 请注意，您无法删除已与消息预设关联的IP池。

