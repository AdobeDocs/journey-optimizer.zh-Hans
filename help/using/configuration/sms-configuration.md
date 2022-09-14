---
title: 短信配置
description: 了解如何配置环境以使用Journey Optimizer发送短信消息
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 2%

---

# 配置短信渠道 {#sms-configuration}

[!DNL Journey Optimizer] 允许您创建历程并向目标受众发送消息。

发送短信之前，请配置您的实例。 您需要 [集成提供程序设置](#create-api) 与Journey Optimizer [创建短信界面](#message-preset-sms) （即短信预设）。 这些步骤必须由 [Adobe Journey Optimizer系统管理员](../start/path/administrator.md).

>[!IMPORTANT]
>
>Adobe Journey Optimizer当前与Sinch和Twilio等第三方提供商集成，后者提供独立于Adobe Journey Optimizer的短信服务。  在短信配置之前，您必须与这些短信提供商之一创建一个帐户，以接收API令牌和服务ID，以便您能够在Adobe Journey Optimizer与适用的短信提供商之间建立连接。 您使用短信服务将受适用短信提供商的其他条款和条件的约束。 鉴于Sinch和Twilio是通过集成提供给Adobe Journey Optimizer用户的第三方产品，因此对于与短信服务相关的任何问题或查询，Sinch或Twilio的用户将需要联系适用的短信提供商以获取帮助。 Adobe不控制第三方产品，也不负责第三方产品。

## 创建新API凭据 {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="使用Journey Optimizer配置短信供应商"
>abstract="选择您的供应商并填写您的短信API凭据。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="使用Journey Optimizer配置短信供应商"
>abstract="选择您的供应商，并填写您的短信API凭据。"

<!--New contextual help content for September release: >abstract="Before sending SMS, you must integrate the provider settings with Journey Optimizer. Once done, you will need to create an SMS surface. These steps must be performed by an Adobe Journey Optimizer system administrator."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/sms-configuration.html#message-preset-sms" text="Create an SMS channel surface"-->

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="选择短信供应商配置"
>abstract="选择为短信供应商配置的API凭据。"

要使用Journey Optimizer配置短信供应商，请执行以下步骤：

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL API凭据]** 菜单，然后单击 **[!UICONTROL 创建API凭据]**.

   ![](assets/sms_4.png)

1. 选择 **[!UICONTROL 短信供应商]**:

   * [!DNL Sinch]的问题。查找 **[!UICONTROL 服务ID]** 和 **[!UICONTROL API令牌]**，从您的Sinch帐户访问短信> API菜单。
   * [!DNL Twilio]的问题。查找 **[!UICONTROL 服务ID]** 和 **[!UICONTROL API令牌]**，访问控制台功能板页面的帐户信息窗格。

1. 输入 **[!UICONTROL 名称]** API凭据。

1. 输入 **[!UICONTROL 服务ID]** 和 **[!UICONTROL API令牌]**.

   ![](assets/sms_5.png)

1. 单击 **[!UICONTROL 提交]** 完成API凭据的配置时，覆盖分类。

现在，创建和配置API凭据后，您需要为短信消息创建渠道表面（即消息预设）。

## 为短信消息创建渠道表面 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定义短信类别"
>abstract="选择使用此表面时将发送的短信消息类型：需要用户同意的促销短信消息，或非商业短信消息的交易型营销，也可以在特定环境中发送给未订阅的用户档案。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/create-sms.html#sms-opt-in-out" text="选择退出营销短信消息"

配置短信渠道后，您需要创建渠道表面，以便能够从 **[!DNL Journey Optimizer]**.

要创建通道曲面，请执行以下步骤：

1. 访问 **[!UICONTROL 渠道]** > **[!UICONTROL 品牌策略]** > **[!UICONTROL 通道曲面]** 菜单，然后单击 **[!UICONTROL 创建通道曲面]**.

   ![](assets/preset-create.png)

1. 为界面输入名称和描述（可选），然后选择短信渠道。

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 还可以使用下划线 `_`，点`.` 和连字符 `-` 字符。

1. 配置 **短信** 设置。

   ![](assets/preset-sms.png)

   * 选择 **[!UICONTROL 短信类型]** 将随表面一起发送： **[!UICONTROL 事务型]** 或 **[!UICONTROL 营销]**.

   * 选择 **[!UICONTROL 短信配置]** 与表面相关。

      有关如何配置环境以发送短信消息的更多信息，请参阅 [此部分](#create-api).

   * 输入 **[!UICONTROL 发件人编号]** 你&#x200B;想用于你的通讯。

   * 选择 **[!UICONTROL 短信执行字段]** 选择 **[!UICONTROL 配置文件属性]** 与用户档案的电话号码关联。

1. 配置所有参数后，单击 **[!UICONTROL 提交]** 确认。 您还可以将通道曲面另存为草稿，并稍后恢复其配置。

   ![](assets/sms_preset_2.png)

1. 创建通道曲面后，该曲面会显示在列表中，其中 **[!UICONTROL 处理]** 状态。

   >[!NOTE]
   >
   >如果检查失败，请在 [此部分](#monitor-channel-surfaces).

1. 检查成功后，通道曲面将 **[!UICONTROL 活动]** 状态。 它已准备好用于投放消息。

   ![](assets/preset-active.png)

现在，您可以使用Journey Optimizer发送短信消息。

**相关主题**

* [创建短信消息](../messages/create-sms.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
