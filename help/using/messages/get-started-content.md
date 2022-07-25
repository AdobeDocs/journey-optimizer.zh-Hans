---
title: 消息入门
description: 了解如何在Journey Optimizer中创建和传递个性化消息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 5%

---

# 渠道操作入门 {#get-started-messages}

>[!CONTEXTUALHELP]
>id="ajo_journey_message"
>title="渠道操作"
>abstract="使用渠道操作发送推送、短信或电子邮件消息。"

使用 [!DNL Journey Optimizer] 创建和投放个性化的推送通知、短信和电子邮件消息。 在历程画布上的操作中，所有消息均可以内嵌编辑。  使用另存为模板功能可轻松重复使用您的内容。 您可以：

* 使用 [!DNL Journey Optimizer] **电子邮件设计功能** 创建或导入响应式电子邮件。

* 利用 **Adobe Experience Manager Assets Essentials** 要扩充您的电子邮件，请构建和管理您自己的资产数据库。

* 查找 **Adobe Stock照片** 以构建内容并改进电子邮件设计。

* 通过创建个性化的 **推送通知、短信和电子邮件** 基于其用户档案属性。

* **发送投放** 并跟踪客户行为。

>[!NOTE]
>
>用户可以访问、创建、编辑和/或发布历程，具体取决于其产品配置文件。 [在此部分中](../administration/permissions.md)了解有关用户权限的更多信息。


## 在您的历程中添加消息{#messages-in-journeys}

>[!CONTEXTUALHELP]
>id="ajo_message_category"
>title="消息类别"
>abstract="为商业消息选择营销，或为非商业消息选择事务型，如订单确认、密码重置通知或投放信息"

>[!CONTEXTUALHELP]
>id="ajo_message_surface"
>title="通道表面"
>abstract="渠道表面是该渠道的一个实例，具有通过营销活动或历程成功交付操作的所有设置。 它由系统管理员定义。"

要在您的历程中添加消息，只需在历程渠道中添加推送、短信或电子邮件活动。

1. 通过 [事件](../building-journeys/general-events.md) 或 [读取区段](../building-journeys/read-segment.md) 活动。

1. 从 **操作** ，拖放 **电子邮件**, **短信** 或 **推送** 活动。

   ![](assets/add-a-message.png)

1. 输入标签和描述。

1. 选择消息 **[!UICONTROL Category]**:选择 **营销** 用于商业报文，或 **事务型** 非商业消息（如订单确认、密码重置通知或投放信息）。

   >[!NOTE]
   >
   >如果您定义 [频率规则](../configuration/frequency-rules.md) 对于特定渠道和类别，在选择该渠道和类别时，它们会自动应用于消息。 当前仅 **[!UICONTROL Marketing]** 类别可用于频率规则。

   ![](assets/inline-message-category.png)

   >[!CAUTION]
   >
   >营销类型的消息必须包含 [选择退出链接](../messages/consent.md#opt-out-management). 事务型消息并非必需的，因为可以将这些消息发送给从营销通信中取消订阅的用户档案。

1. 选择渠道 **[!UICONTROL Surface]** （即消息预设）来发送消息。

   曲面是由 [系统管理员](../start/path/administrator.md). 它包含用于发送消息的所有技术参数，如标头参数、子域、移动设备应用程序等。 [了解详情](../configuration/message-presets.md)。

   >[!CAUTION]
   >
   >必须为所选消息类别和渠道选择有效的渠道表面。

   您可以随时使用 **[!UICONTROL Properties]** 按钮。

1. 创建消息内容。

   在以下页面中了解创建消息内容的详细步骤：

   * [创建电子邮件](create-email.md)
   * [创建推送通知](create-push.md)
   * [创建短信消息](create-sms.md)

## 启用发送时间优化{#sto-in-journeys}

对于电子邮件和推送通知，您可以启用 **[!UICONTROL Send-time optimization]**.

使用 **[!UICONTROL Send-time optimization]** 计划每个用户的个性化发送时间，以增加消息的打开率和点击率。 [了解详情](../messages/send-time-optimization.md)。


## 高级参数{#adv-settings}

默认情况下，高级参数为只读和隐藏参数。

要访问高级参数，请单击 **[!UICONTROL Show read-only fields]** 图标。

![](assets/show-read-only.png)

高级参数显示在消息窗格的底部。 这些参数由 [系统管理员](../start/path/administrator.md) 在 [通道表面](../configuration/message-presets.md) （即消息预设）。

对于推送通知，您可以显示以下参数：令牌、应用程序ID、应用程序平台。

![](assets/push-adv-parameters.png)

对于电子邮件，您可以显示主电子邮件地址。

为了具体使用，您可以在特定上下文中覆盖这些值。 要强制使用某个值，请单击 **启用参数覆盖** 图标。 此选项可能对以下用户非常有用：

* 测试电子邮件，可添加您的电子邮件地址。 发布历程后，将向您发送电子邮件。
* 请参阅列表订阅者的电子邮件地址。 在 [此用例](../building-journeys/message-to-subscribers-uc.md).

单击同一图标可重置为默认参数。


## 浏览消息{#browse-message}

当历程中使用多条消息时，您可以从 **编辑内容** 屏幕。

![](assets/inline-messages-multi-content.png)

然后，您可以 [检查警报](alerts.md) 和 [模拟](../design/preview.md) 每个内容。

## 复制消息 {#duplicate-message}

您可以从历程画布复制现有消息。

要执行此操作，请执行以下步骤：

1. 选择要复制的消息。

1. 使用 **[!UICONTROL Copy]** 按钮 **[!UICONTROL Action]** 中。

   ![](assets/message-duplicate.png)

1. 输入 **crtl+V** 来粘贴消息。

   消息将添加到历程卡纳。 所有设置和配置都将复制到新消息中。

   ![](assets/message-duplicated.png)

1. 重命名消息以便能够将初始消息与副本区分开，例如在编辑消息时，如下所示：

   ![](assets/multi-message.png)


>[!NOTE]
>
>对于电子邮件，您还可以将现有消息转换为模板。 [了解详情](../design/email-templates.md)。

## 删除消息

要删除消息，请使用渠道操作活动窗格顶部的垃圾桶图标。

![](assets/delete-message.png)

使用 **[!UICONTROL Confirm]** 按钮进行验证。
