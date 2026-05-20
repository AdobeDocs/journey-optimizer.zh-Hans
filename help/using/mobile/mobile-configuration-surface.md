---
solution: Journey Optimizer
product: journey optimizer
title: 配置短信配置
description: 了解如何配置短信/彩信配置以使用Journey Optimizer发送短信
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 0d541520-016e-468f-b011-808712847556
TQID: https://experienceleague.adobe.com/J5h64ccVVJUTCIk7FMMolKfEZy6rjEn-jwj1dEntnRM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9a68782b0ca1a9a65db621209cf4f39ea5ce911d
workflow-type: tm+mt
source-wordcount: 520
ht-degree: 12%

---

# 创建移动消息配置 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定义消息类别"
>abstract="选择使用此配置的短信的类型：营销型的推广短信（需要用户同意）或事务性的非商业短信，如密码重置。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=zh-Hans#sms-opt-out-management" text="选择禁用营销短信消息"

配置移动消息渠道后，必须创建渠道配置才能从&#x200B;**[!DNL Journey Optimizer]**&#x200B;发送SMS、RCS和MMS消息。

要创建渠道配置，请执行以下步骤：

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]**&#x200B;并选择&#x200B;**[!UICONTROL 常规设置]** > **[!UICONTROL 渠道配置]**。 单击&#x200B;**[!UICONTROL 创建渠道配置]**&#x200B;按钮。

   ![](assets/preset-create.png)

1. 输入配置的名称和描述（可选），然后选择移动设备渠道。

   ![](assets/sms-create-surface.png)

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线 `_`、点 `.` 和连字符 `-` 符号。

1. 为此配置选择&#x200B;**[!UICONTROL 短信类型]**：

   * **[!UICONTROL 营销]**：对于需要用户同意的促销消息。
   * **[!UICONTROL 事务型]**：用于非商业消息，如订单确认、密码重置或投放更新。

   >[!CAUTION]
   >
   >**事务型**&#x200B;消息可以发送给已从营销通信中取消订阅的用户档案，但只能在特定上下文中发送。

   ![](assets/sms-surface-settings.png){width=80%}

1. 选择要与配置关联的&#x200B;**[!UICONTROL 移动设备配置]**。

   有关如何配置环境以发送移动消息的更多信息，请参阅[此章节](#create-api)。

1. 输入&#x200B;要用于通信的&#x200B;**[!UICONTROL 发件人号码]**。

1. 如果要在手机消息中使用URL缩短功能，请从&#x200B;**[!UICONTROL 子域]**&#x200B;列表中选择一个项目。

   >[!NOTE]
   >
   >要能够选择子域，请确保您之前已配置至少一个SMS/MMS子域。 [了解如何操作](mobile-subdomains.md)

1. 在&#x200B;**[!UICONTROL 执行维度]**&#x200B;部分中，使用&#x200B;**[!UICONTROL 短信执行字段]**&#x200B;在配置文件属性中选择要优先使用的电话号码（如果数据库中有多个号码可用）。 [了解详情](../configuration/primary-email-addresses.md#override-execution-address-channel-config)

   >[!NOTE]
   >
   >默认情况下，[!DNL Journey Optimizer]在沙盒级别使用[常规设置](../configuration/primary-email-addresses.md)中指定的电话号码。 更新此字段将覆盖使用此配置的历程和营销活动的默认值。

1. 选择&#x200B;**[!UICONTROL 对入站]**&#x200B;使用自定义数据集，将此凭据的入站SMS路由到您从下拉列表选择的预创建的数据集。 [了解有关对入站关键字使用自定义数据集的更多信息](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >数据集架构必须是&#x200B;**[!UICONTROL XDM ExperienceEvent]**，并且至少包括以下字段组：
   >* Adobe CJM ExperienceEvent — 消息交互详细信息
   >* Adobe CJM ExperienceEvent — 消息执行详细信息
   >* Adobe CJM ExperienceEvent — 消息配置文件详细信息
   >
   >必须为配置文件启用架构和数据集。

1. 配置所有参数后，单击&#x200B;**[!UICONTROL 提交]**&#x200B;以确认。 您还可以将渠道配置另存为草稿，并稍后恢复其配置。

   ![](assets/sms-submit-surface.png)

1. 创建渠道配置后，它将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。

   >[!NOTE]
   >
   >如果检查不成功，请在[本节](../configuration/channel-surfaces.md)中进一步了解可能的失败原因。

1. 检查成功后，通道配置将获得&#x200B;**[!UICONTROL 活动]**&#x200B;状态。 它随时可用于投放消息。

   ![](assets/preset-active.png)

您现在可以使用Journey Optimizer发送短信。
