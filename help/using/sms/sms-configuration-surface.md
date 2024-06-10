---
solution: Journey Optimizer
product: journey optimizer
title: 配置短信表面
description: 了解如何使用Journey Optimizer配置短信/彩信界面以发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: 82c58753b0beb1c6c60b4e1a8188725b3cb83390
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---

# 创建短信/彩信表面 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定义消息类别"
>abstract="使用此表面选择文本消息的类型：促销消息的营销型（需要用户同意），或非商业消息的事务型（如密码重置）。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="营销文本消息中的选择退出"

配置短信/彩信渠道后，您必须创建一个渠道平面，以便能够从中发送短信和彩信消息 **[!DNL Journey Optimizer]**.

要创建渠道表面，请执行以下步骤：

1. 在左边栏中，浏览 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 并选择 **[!UICONTROL 品牌化]** > **[!UICONTROL 渠道表面]**. 单击 **[!UICONTROL 创建渠道表面]** 按钮。

   ![](assets/preset-create.png)

1. 输入表面的名称和描述（可选），然后选择短信渠道。

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您也可以使用下划线 `_`，点`.` 和连字符 `-` 个字符。

1. 定义 **短信设置**.

   ![](assets/sms-surface-settings.png)

   首先，选择 **[!UICONTROL 短信类型]** 将随表面一起发送的内容： **[!UICONTROL 事务性]** 或 **[!UICONTROL 营销]**.

   * 选择 **营销** 促销文本消息：这些消息需要用户同意。
   * 选择 **事务性** 用于非商业性消息，如订单确认、密码重置通知或投放信息。

   创建SMS/MMS时，必须选择与为消息选择的类别匹配的有效渠道平面。

   >[!CAUTION]
   >
   >**事务性** 消息可以发送给取消订阅营销通信的用户档案。 这些消息只能在特定上下文中发送。

1. 选择 **[!UICONTROL 短信配置]** 以与曲面相关联。

   有关如何配置环境以发送短信消息的更多信息，请参阅 [本节](#create-api).

1. 输入 **[!UICONTROL 发件人编号]** 您&#x200B;希望用于您的通信。

1. 选择您的 **[!UICONTROL 短信执行字段]** 以选择 **[!UICONTROL 配置文件属性]** 与用户档案的电话号码关联。

1. 如果要在短信消息中使用URL缩短功能，请从 **[!UICONTROL 子域]** 列表。

   >[!NOTE]
   >
   >要能够选择子域，请确保您之前已配置至少一个SMS/MMS子域。 [了解如何操作](sms-subdomains.md)

<!--
1. Enter the **[!UICONTROL Opt-out number]** you want to use for this surface. When profiles opt out from this number, you are still able to send them messages from other numbers you may be using to send out text messages with [!DNL Journey Optimizer].

    >[!NOTE]
    >
    >In [!DNL Journey Optimizer], opt-out for text messages is no longer managed at the channel level. It is now specific to a number.
-->
1. 配置完所有参数后，单击 **[!UICONTROL 提交]** 以确认。 也可以将渠道曲面另存为草稿，并稍后恢复其配置。

   ![](assets/sms-submit-surface.png)

1. 创建渠道表面后，它将显示在列表中，其中包含 **[!UICONTROL 正在处理]** 状态。

   >[!NOTE]
   >
   >如果检查不成功，请在中详细了解可能失败的原因 [本节](#monitor-channel-surfaces).

1. 检查成功后，渠道表面将获得 **[!UICONTROL 活动]** 状态。 它随时可用于投放消息。

   ![](assets/preset-active.png)

您现在可以使用Journey Optimizer发送短信。
