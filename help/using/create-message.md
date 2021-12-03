---
title: 创建消息
description: 了解如何创建消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 186a43cd-c5eb-4de1-8713-95399d802d36
source-git-commit: d8c95350ac17658ce477d6aec50a9f418f4af0f2
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 3%

---

# 创建消息 {#create-message}

可从 **[!UICONTROL Messages]** 快捷键。 所有消息均按发布日期（对于已发布的消息）或创建日期（对于草稿消息）排序。

>[!NOTE]
>
>用户可以访问、创建、编辑和/或发布消息，具体取决于其产品配置文件。 了解有关用户权限的更多信息 [在此部分中](administration/permissions.md).

![](assets/messages-list.png)

使用 **[!UICONTROL Show recents]** 切换以向您在过去5天内访问的消息添加直接链接。

![](assets/show-recent-messages.png)

使用过滤器图标可仅显示草拟、已发布或正在发布的消息。 您还可以在消息标签上搜索，如下所示：

![](assets/filter-messages.png)

## 创建新消息

要创建新消息，请执行以下步骤：

1. 访问消息列表，然后单击 **[!UICONTROL Create Message]**.

1. 定义消息属性。

   ![](assets/create-message-properties.png)

   * 输入 **[!UICONTROL Title]** （必需）和 **[!UICONTROL Description]**.

   * 选择 **[!UICONTROL Message category]**:营销或交易。

   * 选择 **[!UICONTROL Preset]** 用于消息。

      预设包含根据您的品牌发送电子邮件和/或推送通知所需的所有参数。 [了解有关预设的更多信息](configuration/message-presets.md).

   * 选择要用于该消息的渠道：电子邮件和/或推送通知。 您必须至少选择一个渠道才能创建消息。
   请注意，您可以随时使用 **[!UICONTROL Properties]** 按钮。

1. 单击 **[!UICONTROL Create]** 确认消息创建。 您的消息会添加在消息列表中，即 **[!UICONTROL Draft]** 状态。

   每个选定的渠道都有一个选项卡。 使用这些选项卡为每个渠道配置内容。 您可以通过选择某个选项卡并单击 **[!UICONTROL Delete channel]** 按钮。

   ![](assets/create-messages-content.png)

   您现在可以创建消息的内容并调整设置。 以下部分提供了有关电子邮件和推送通知配置的详细信息：

   * [创建电子邮件](create-email.md)
   * [创建推送通知](create-push.md)

   >[!NOTE]
   >   
   >您可以使用表达式编辑器使用用户档案数据个性化您的消息。 有关个性化的更多信息，请参阅 [此部分](personalization/personalize.md).


1. 使用左侧的预览部分控制消息的呈现，并使用测试用户档案检查个性化设置。 如需详细信息，请参阅[此部分](preview.md)。

   ![](assets/messages-simple-preview.png)

1. 在编辑器的上部检查警报。  其中一些是简单的警告，但其他警告可能会阻止您发布消息。 在 [此部分](alerts.md).

1. 您现在可以通过单击 **[!UICONTROL Publish]** 按钮，或将其保留为草稿并稍后发布。 有关如何发布消息的更多信息，请参阅 [此部分](publish-manage-message.md).

## 复制消息

要从现有消息创建消息，请使用 **[!UICONTROL Duplicate]** 按钮。 所有设置和配置都将复制到新消息中

![](assets/message-duplicate.png)

您可以在确认复制之前重命名消息。

![](assets/message-duplicate-confirm.png)

创建新消息后，窗口底部会显示确认消息。

您还可以使用专用图标从消息列表中复制消息。

![](assets/message-duplicate-from-list.png)

同一确认过程适用。
