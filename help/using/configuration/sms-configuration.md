---
title: 短信配置
description: 了解如何配置环境以使用Journey Optimizer发送短信消息
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 47b1c2832f82a5c168cd03f1d1b43a9223c945b3
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 3%

---

# 配置短信渠道 {#sms-configuration}

[!DNL Journey Optimizer] 允许您创建历程并向目标受众发送消息。

发送短信之前，请配置您的实例。 您需要 [集成提供程序设置](#create-api) 与Journey Optimizer [创建短信预设](#message-preset-sms). 这些步骤必须由 [Adobe Journey Optimizer系统管理员](../start/path/administrator.md).

>[!AVAILABILITY]
>
>短信渠道当前仅适用于一组组织（有限可用性）。 有关更多信息，请联系您的Adobe代表。

## 创建新API凭据 {#create-api}

要使用Journey Optimizer配置短信供应商，请执行以下步骤：

1. 访问 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL API Credentials]** 菜单，然后单击 **[!UICONTROL Create API credential]**.

   ![](assets/sms_4.png)

1. 选择 **[!UICONTROL SMS vendor]**:

   * [!DNL Sinch]的问题。查找 **[!UICONTROL Service ID]** 和 **[!UICONTROL API Token]**，从您的Sinch帐户访问短信> API菜单。
   * [!DNL Twilio]的问题。查找 **[!UICONTROL Service ID]** 和 **[!UICONTROL API Token]**，访问控制台功能板页面的帐户信息窗格。

1. 输入 **[!UICONTROL Name]** API凭据。

1. 输入 **[!UICONTROL Service ID]** 和 **[!UICONTROL API Token]**.

   ![](assets/sms_5.png)

1. 单击 **[!UICONTROL Submit]** 完成API凭据的配置时，覆盖分类。

现在，创建和配置API凭据后，您需要为短信消息创建消息预设。

## 为短信消息创建消息预设 {#message-preset-sms}

配置短信渠道后，您需要创建消息预设，以便能够从 **[!DNL Journey Optimizer]**.

要创建消息预设，请执行以下步骤：

1. 访问 **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** 菜单，然后单击 **[!UICONTROL Create Message preset]**.

   ![](assets/preset-create.png)

1. 为预设输入名称和描述（可选），然后选择短信渠道。

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 还可以使用下划线 `_`，点`.` 和连字符 `-` 字符。

1. 配置 **短信** 设置。

   ![](assets/preset-sms.png)

   * 选择 **[!UICONTROL SMS Type]** 将随预设一起发送： **[!UICONTROL Transactional]** 或 **[!UICONTROL Marketing]**.

   * 选择 **[!UICONTROL SMS configuration]** 与预设关联。

      有关如何配置环境以发送短信消息的更多信息，请参阅 [此部分](#create-api).

   * 输入 **[!UICONTROL Sender number]** 你&#x200B;想用于你的通讯。

   * 选择 **[!UICONTROL SMS Execution Field]** 选择 **[!UICONTROL Profile attribute]** 与用户档案的电话号码关联。

1. 配置所有参数后，单击 **[!UICONTROL Submit]** 确认。 您还可以将消息预设另存为草稿，稍后恢复其配置。

   ![](assets/sms_preset_2.png)

1. 创建消息预设后，该消息预设会显示在列表中，其中 **[!UICONTROL Processing]** 状态。

   >[!NOTE]
   >
   >如果检查失败，请在 [此部分](#monitor-message-presets).

1. 检查成功后，消息预设将获取 **[!UICONTROL Active]** 状态。 它已准备好用于投放消息。

   ![](assets/preset-active.png)

现在，您可以使用Journey Optimizer发送短信消息。

**相关主题**

* [创建短信消息](../messages/create-sms.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
