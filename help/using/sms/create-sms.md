---
solution: Journey Optimizer
product: journey optimizer
title: 创建短信消息
description: 了解如何在Journey Optimizer中创建短信消息
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: f275820c3f79bb4c9aca8593c2c761ccd4283795
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 14%

---

# 创建文本消息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="创建文本消息"
>abstract="要创建短信，请在历程或营销活动中添加短信操作，然后开始用表达式编辑器使其个性化。"

您可以使用Adobe Journey Optimizer设计和发送文本(SMS)。 您首先需要在历程或营销策划中添加短信操作，然后定义文本消息的内容，如下所述。 Adobe Journey Optimizer还提供了在发送之前测试文本消息的功能，以便您检查渲染、个性化属性和所有其他设置。

>[!NOTE]
>
>根据行业标准和法规，所有短信营销消息都必须包含一种让接收者能够轻松取消订阅的方式。要实现此目的，短信收件人可以使用选择启用和选择禁用关键词进行回复。 [了解如何管理选择退出](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)


## 添加短信 {#create-sms-journey-campaign}

浏览以下选项卡，了解如何在活动或历程中添加短信。

>[!BEGINTABS]

>[!TAB 向历程添加短信]

1. 打开您的历程，然后从拖放短信活动 **操作** 面板的部分。

   ![](assets/sms_create_1.png)

1. 提供有关消息的基本信息（标签、描述、类别），然后选择要使用的消息界面。

   ![](assets/sms_create_2.png)

   有关如何配置旅程的更多信息，请参阅 [此页面](../building-journeys/journey-gs.md)

   此 **[!UICONTROL 表面]** 默认情况下，字段会使用用户用于该渠道的最后一个表面进行预填充。

您现在可以从以下网址开始设计短信消息的内容 **[!UICONTROL 编辑内容]** 按钮，如下所述。

>[!TAB 向营销活动添加短信]

1. 创建新的计划或API触发的营销活动，请选择 **[!UICONTROL 短信]** 作为您的操作，然后选择 **[!UICONTROL 应用程序表面]** 以使用。 在中了解有关短信配置的更多信息 [此页面](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。

1. 从 **[!UICONTROL 属性]** 部分，编辑您的营销活动的 **[!UICONTROL 标题]** 和 **[!UICONTROL 描述]**.

   ![](assets/sms_create_4.png)

1. 单击 **[!UICONTROL 选择受众]** 按钮，从可用的Adobe Experience Platform受众列表中定义要定位的受众。 [了解详情](../audience/about-audiences.md)。

1. 在 **[!UICONTROL 身份命名空间]** 字段中，选择要使用的命名空间，以便识别所选受众中的个人。 [了解详情](../event/about-creating.md#select-the-namespace)。

   ![](assets/sms_create_5.png)

1. 单击 **[!UICONTROL 创建试验]** 开始配置内容实验并创建处理方式以测量其性能并为目标受众确定最佳选项。 [了解详情](../campaigns/content-experiment.md)

1. 在 **[!UICONTROL 操作跟踪]** 部分，指定是否要跟踪短信消息中的链接点击次数。

1. 营销活动旨在按特定日期或循环频率执行。 了解如何配置 **[!UICONTROL 计划]** 中的促销活动 [本节](../campaigns/create-campaign.md#schedule).

1. 从 **[!UICONTROL 操作触发器]** 菜单，选择 **[!UICONTROL 频率]** 短信消息的：

   * 一次
   * 每日
   * 每周
   * 月

您现在可以从以下网址开始设计短信的内容： **[!UICONTROL 编辑内容]** 按钮，如下所述。

>[!ENDTABS]

## 定义短信内容{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="定义短信内容"
>abstract="通过使用表达式编辑器定义内容并纳入动态元素而自定义短信并使其个性化。"

要配置短信内容，请执行以下步骤。

1. 在历程或营销策划配置屏幕中，单击 **[!UICONTROL 编辑内容]** 按钮以配置文本消息内容。

1. 单击 **[!UICONTROL 消息]** 用于打开表达式编辑器的字段。

   ![](assets/sms-content.png)

1. 使用表达式编辑器定义内容、添加个性化和动态内容。 您可以使用任何属性，例如配置文件名称或城市。 您还可以定义条件规则。 浏览到以下页面，了解更多关于 [个性化](../personalization/personalize.md) 和 [动态内容](../personalization/get-started-dynamic-content.md) 在表达式编辑器中。

1. 定义内容后，您可以在消息中添加跟踪的URL。 为此，请访问 **[!UICONTROL 辅助函数]** 菜单并选择 **[!UICONTROL 辅助函数]**.

   请注意，要使用URL缩短功能，您必须首先配置子域，然后该子域将链接到您的表面。 [了解详情](sms-subdomains.md)

   >[!CAUTION]
   >
   > 要访问和编辑短信子域，您必须拥有 **[!UICONTROL 管理短信子域]** 生产沙盒的权限。 可在[此部分](../administration/high-low-permissions.md)中详细了解权限。

   ![](assets/sms_tracking_1.png)

1. 在 **[!UICONTROL 辅助函数]** 菜单，单击 **[!UICONTROL URL函数]** 然后选择 **[!UICONTROL 添加URL]**.

   ![](assets/sms_tracking_2.png)

1. 在 `originalUrl` 字段中，粘贴要缩短的URL并单击 **[!UICONTROL 保存]**.

1. 单击 **[!UICONTROL 保存]** 并在预览中查看您的消息。 您现在可以测试和检查消息内容，如中所述 [本节](#sms-mms-test).

<!--
## Define your MMS content{#mms-content}

You can enhance your communication by sending Multimedia Message Service (MMS) messages, enabling the sharing of media such as videos, pictures, audio clips and GIFs, and more. Additionally, MMS allows for up to 1600 characters of text in your message.


>[!NOTE]
>
>* This feature is currently available with **Sinch** only.
>
>* MMS channel comes with a few limitations listed in [this page](../start/guardrails.md#sms-guardrails).
>

To create MMS content, follow these steps:

1. Create a SMS as described in [this section](#create-sms-journey-campaign).

1. Edit your SMS content as detailed in [this section](#sms-content).

1. Enable the MMS option to add media to your SMS content.

    ![](assets/sms_create_6.png)

1. Add a **[!UICONTROL Title]** to your media.

1. Enter the URL of your media in the **[!UICONTROL Media]** field.

    ![](assets/sms_create_7.png)

1. Click **[!UICONTROL Save]** and check your message in the preview. You can now test and check your message content as detailed below.
-->

## 测试和发送消息 {#sms-mms-test}

使用 **[!UICONTROL 模拟内容]** 按钮以预览短信内容、缩短的URL和个性化内容。

![](assets/sms-content-preview.png)

执行测试并验证内容后，即可向受众发送短信。 这些步骤详见 [此页面](send-sms.md)

发送后，您可以在促销活动或历程报表中测量短信的影响。 有关报告的更多信息，请参考[此章节](../reports/campaign-global-report.md#sms-tab)。

**相关主题**

* [预览、测试和发送短信](send-sms.md)
* [配置短信渠道](sms-configuration.md)
* [短信报告](../reports/journey-global-report.md#sms-global)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在营销活动中添加消息](../campaigns/create-campaign.md)
