---
solution: Journey Optimizer
product: journey optimizer
title: 配置短信配置
description: 了解如何配置短信/彩信配置以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
source-git-commit: 7ca149d420f802a6230e699cffefddc4117cb85e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 14%

---

# 创建 SMS/MMS 配置 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定义消息类别"
>abstract="选择使用此配置的短信的类型：营销型的推广短信（需要用户同意）或交易型的非商业短信，如密码重置。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=zh-Hans#sms-opt-out-management" text="选择禁用营销短信消息"

配置短信/彩信渠道后，您必须创建渠道配置才能从&#x200B;**[!DNL Journey Optimizer]**&#x200B;发送短信和彩信消息。

要创建渠道配置，请执行以下步骤：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;并选择&#x200B;**[!UICONTROL 常规设置]** > **[!UICONTROL 渠道配置]**。 单击&#x200B;**[!UICONTROL 创建渠道配置]**&#x200B;按钮。

   ![](assets/preset-create.png)

1. 输入配置的名称和描述（可选），然后选择短信渠道。

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线 `_`、点 `.` 和连字符 `-` 符号。

1. 定义&#x200B;**短信设置**。

   ![](assets/sms-surface-settings.png)

   首先，选择将随配置发送的&#x200B;**[!UICONTROL 短信类型]**： **[!UICONTROL 事务型]**&#x200B;或&#x200B;**[!UICONTROL 营销型]**。

   * 为促销文本消息选择&#x200B;**营销**：这些消息需要用户同意。
   * 为非商业消息（例如订单确认、密码重置通知或投放信息）选择&#x200B;**事务型**。

   创建短信/彩信时，您必须选择与为消息选择的类别匹配的有效渠道配置。

   >[!CAUTION]
   >
   >**事务型**&#x200B;消息可发送给取消订阅营销通信的用户档案。 这些消息只能在特定上下文中发送。

1. 选择要与配置关联的&#x200B;**[!UICONTROL 短信配置]**。

   有关如何配置环境以发送短信消息的更多信息，请参阅[此章节](#create-api)。

1. 输入&#x200B;要用于通信的&#x200B;**[!UICONTROL 发件人号码]**。

1. 选择您的&#x200B;**[!UICONTROL 短信执行字段]**&#x200B;以选择与用户档案电话号码关联的&#x200B;**[!UICONTROL 用户档案属性]**。

1. 如果要在短信消息中使用URL缩短功能，请从&#x200B;**[!UICONTROL 子域]**&#x200B;列表中选择一个项目。

   >[!NOTE]
   >
   >要能够选择子域，请确保您之前已配置至少一个SMS/MMS子域。 [了解如何操作](sms-subdomains.md)

1. 配置所有参数后，单击&#x200B;**[!UICONTROL 提交]**&#x200B;以确认。 您还可以将渠道配置另存为草稿，并稍后恢复其配置。

   ![](assets/sms-submit-surface.png)

1. 创建渠道配置后，它将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。

   >[!NOTE]
   >
   >如果检查不成功，请在[本节](../configuration/channel-surfaces.md)中进一步了解可能的失败原因。

1. 检查成功后，通道配置将获得&#x200B;**[!UICONTROL 活动]**&#x200B;状态。 它随时可用于投放消息。

   ![](assets/preset-active.png)

您现在可以使用Journey Optimizer发送短信。
