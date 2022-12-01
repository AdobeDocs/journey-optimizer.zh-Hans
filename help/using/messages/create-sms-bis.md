---
solution: Journey Optimizer
product: journey optimizer
title: 创建短信消息
description: 了解如何在Journey Optimizer中创建短信消息
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 5e5b078fa61e2c615a2242f50439c2f20ea5216a
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 7%

---

# 创建短信消息 {#create-sms-bis}

>[!NOTE]
>
>根据行业标准和法规，所有短信营销消息都必须包含一种让接收者能够轻松取消订阅的方式。为此，短信收件人可以使用选择加入和选择退出关键词进行回复。

## 在历程或营销策划中创建短信消息

要开始个性化短信消息，请执行以下步骤：

>[!BEGINTABS]

>[!TAB 向历程添加短信消息]

1. 打开您的历程，然后从面板的操作部分拖放短信活动。

1. 提供有关消息的基本信息（标签、描述、类别），然后选择要使用的消息界面。

   有关如何配置历程的更多信息，请参阅。

您现在可以从 **[!UICONTROL 编辑内容]** 按钮。

>[!TAB 向营销活动添加短信消息]

1. 创建新的计划营销活动或API触发的营销活动，选择 **[!UICONTROL 短信]** 作为您的操作，然后选择 **[!UICONTROL 应用程序界面]** 。

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 从 **[!UICONTROL 属性]** ，编辑营销活动的 **[!UICONTROL 标题]** 和 **[!UICONTROL 描述]**.

1. 在 **[!UICONTROL 操作跟踪]** 部分，指定是否跟踪短信消息中链接的点击量。

1. 单击 **[!UICONTROL 选择受众]** 按钮，以从可用的Adobe Experience Platform区段列表中定义要定位的受众。

1. 在 **[!UICONTROL 身份命名空间]** 字段中，选择要用于识别选定区段中个人的命名空间。

1. 营销活动设计为在特定日期或定期频率执行。 了解如何配置 **[!UICONTROL 计划]** 你竞选的。

1. 从 **[!UICONTROL 操作触发器]** 菜单，选择 **[!UICONTROL 频率]** 短信消息：

   * 一次
   * 每日
   * 每周
   * 月

您现在可以从 **[!UICONTROL 编辑内容]** 按钮。

>[!ENDTABS]

## 定义短信内容

1. 在历程或营销活动配置屏幕中，单击 **[!UICONTROL 编辑内容]** 按钮来配置短信内容。

1. 单击 **[!UICONTROL 消息]** 字段来打开表达式编辑器。

1. 使用表达式编辑器定义内容并添加动态内容。 您可以使用任何属性，如配置文件名称或城市。

1. 单击 **[!UICONTROL 保存]** 并在预览中查看您的消息。

1. 当短信消息准备就绪时，完成要发送的配置。

## 验证短信

>[!NOTE]
>
> 为了更好地交付，您应始终使用提供商支持的格式的电话号码。 例如， Twilio和Sinch仅支持E.164格式的电话号码。

定义消息内容后，即可使用测试用户档案进行预览和测试。 如果插入，则可以使用测试用户档案数据检查此内容在消息中的显示方式。

要可视化显示您的短信消息在移动设备上的显示方式，请单击 **[!UICONTROL 模拟内容]** 选项卡。 在中了解有关内容模拟的更多信息。

您还必须检查编辑器上部的警报。  其中一些是简单的警告，但其他警告可能会阻止您使用消息。 在中了解更多信息。
